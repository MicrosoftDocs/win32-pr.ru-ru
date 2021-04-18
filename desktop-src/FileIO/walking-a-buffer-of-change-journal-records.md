---
description: Как вернуть записи журнала изменений, соответствующие указанным критериям.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Проход по буферу записей журнала изменений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663597"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Проход по буферу записей журнала изменений

Управляющие коды, возвращающие записи журнала изменений номеров последовательных обновлений (USN), [**фсктл \_ Read \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) и [**фсктл \_ Enum \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), возвращают аналогичные данные в выходной буфер. Оба возвращают USN, за которым следует ноль или более записей журнала изменений, каждый в структуре записи USN v2 или [**USN с \_ записью \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) [**\_ \_ версии**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 3.

Целевой том для операций USN должен быть ReFS или NTFS 3,0 или более поздней версии. Чтобы получить версию тома NTFS, откройте командную строку с правами доступа администратора и выполните следующую команду:

**FSUtil.exe FSInfo NTFSInfo** *X * * *:**

где *X* — буква диска тома.

В следующем списке приведены способы получения записей журнала изменений.

-   Используйте [**\_ Перечисление \_ \_ данных USN фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) , чтобы получить список (перечисление) всех записей журнала изменений между двумя USN.
-   Используйте [**фсктл \_ Чтение \_ \_ журнала USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) , чтобы быть более селективным, например для выбора конкретных причин изменений или возврата при закрытии файла.

> [!Note]  
> Обе эти операции возвращают только подмножество записей журнала изменений, соответствующих указанным критериям.

 

USN, возвращенный в качестве первого элемента в выходном буфере, — это USN номера следующей записи, которую необходимо получить. Используйте это значение, чтобы продолжить чтение записей с конечной границы вперед.

Элемент **filename** [**\_ записи USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) или [**USN \_ запись \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) содержит имя файла, к которому применяется рассматриваемая запись. Имя файла зависит от длины, поэтому **запись USN \_ \_ v2** и **USN запись версии \_ \_ 3** являются структурами переменной длины. Их первый член, **RecordLength**, — это длина структуры (включая имя файла) в байтах.

При работе с членом **имени файла** в структурах записи [**USN v2 и USN \_ \_ версии**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**\_ \_ 3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) не следует считать, что имя файла содержит замыкающий разделитель " \\ 0". Чтобы определить длину имени файла, используйте элемент **филенамеленгс** .

В следующем примере вызывается [**фсктл \_ Read \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) и выполняется обход буфера записей журнала изменений, возвращаемых операцией.


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



Размер в байтах любой записи, указанной в структуре записи [**USN v2 или USN \_ \_ версии**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**\_ \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , не превышает `((MaxComponentLength - 1) * Width) + Size` максимально допустимой длины в символах имени файла записи *макскомпонентленгс* . Ширина — это размер расширенного символа, а *Размер* — размер структуры.

Чтобы получить максимальную длину, вызовите функцию [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и изучите значение, на которое указывает параметр *лпмаксимумкомпонентленгс* . Вычтите один из *макскомпонентленгс* для учета того факта, что определение [**\_ записи USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) и [**записи USN \_ \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) содержит один символ имени файла.

В языке программирования C наиболее вероятным размером записи является следующий:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
