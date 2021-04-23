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
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="55284-103">Проход по буферу записей журнала изменений</span><span class="sxs-lookup"><span data-stu-id="55284-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="55284-104">Управляющие коды, возвращающие записи журнала изменений номеров последовательных обновлений (USN), [**фсктл \_ Read \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) и [**фсктл \_ Enum \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), возвращают аналогичные данные в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="55284-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="55284-105">Оба возвращают USN, за которым следует ноль или более записей журнала изменений, каждый в структуре записи USN v2 или [**USN с \_ записью \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) [**\_ \_ версии**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 3.</span><span class="sxs-lookup"><span data-stu-id="55284-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="55284-106">Целевой том для операций USN должен быть ReFS или NTFS 3,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="55284-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="55284-107">Чтобы получить версию тома NTFS, откройте командную строку с правами доступа администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="55284-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="55284-108">**FSUtil.exe FSInfo NTFSInfo** *X \* \* *:**</span><span class="sxs-lookup"><span data-stu-id="55284-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="55284-109">где *X* — буква диска тома.</span><span class="sxs-lookup"><span data-stu-id="55284-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="55284-110">В следующем списке приведены способы получения записей журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="55284-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="55284-111">Используйте [**\_ Перечисление \_ \_ данных USN фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) , чтобы получить список (перечисление) всех записей журнала изменений между двумя USN.</span><span class="sxs-lookup"><span data-stu-id="55284-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="55284-112">Используйте [**фсктл \_ Чтение \_ \_ журнала USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) , чтобы быть более селективным, например для выбора конкретных причин изменений или возврата при закрытии файла.</span><span class="sxs-lookup"><span data-stu-id="55284-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="55284-113">Обе эти операции возвращают только подмножество записей журнала изменений, соответствующих указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="55284-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="55284-114">USN, возвращенный в качестве первого элемента в выходном буфере, — это USN номера следующей записи, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="55284-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="55284-115">Используйте это значение, чтобы продолжить чтение записей с конечной границы вперед.</span><span class="sxs-lookup"><span data-stu-id="55284-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="55284-116">Элемент **filename** [**\_ записи USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) или [**USN \_ запись \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) содержит имя файла, к которому применяется рассматриваемая запись.</span><span class="sxs-lookup"><span data-stu-id="55284-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="55284-117">Имя файла зависит от длины, поэтому **запись USN \_ \_ v2** и **USN запись версии \_ \_ 3** являются структурами переменной длины.</span><span class="sxs-lookup"><span data-stu-id="55284-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="55284-118">Их первый член, **RecordLength**, — это длина структуры (включая имя файла) в байтах.</span><span class="sxs-lookup"><span data-stu-id="55284-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="55284-119">При работе с членом **имени файла** в структурах записи [**USN v2 и USN \_ \_ версии**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**\_ \_ 3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) не следует считать, что имя файла содержит замыкающий разделитель " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="55284-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="55284-120">Чтобы определить длину имени файла, используйте элемент **филенамеленгс** .</span><span class="sxs-lookup"><span data-stu-id="55284-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="55284-121">В следующем примере вызывается [**фсктл \_ Read \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) и выполняется обход буфера записей журнала изменений, возвращаемых операцией.</span><span class="sxs-lookup"><span data-stu-id="55284-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


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



<span data-ttu-id="55284-122">Размер в байтах любой записи, указанной в структуре записи [**USN v2 или USN \_ \_ версии**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**\_ \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , не превышает `((MaxComponentLength - 1) * Width) + Size` максимально допустимой длины в символах имени файла записи *макскомпонентленгс* .</span><span class="sxs-lookup"><span data-stu-id="55284-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="55284-123">Ширина — это размер расширенного символа, а *Размер* — размер структуры.</span><span class="sxs-lookup"><span data-stu-id="55284-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="55284-124">Чтобы получить максимальную длину, вызовите функцию [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и изучите значение, на которое указывает параметр *лпмаксимумкомпонентленгс* .</span><span class="sxs-lookup"><span data-stu-id="55284-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="55284-125">Вычтите один из *макскомпонентленгс* для учета того факта, что определение [**\_ записи USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) и [**записи USN \_ \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) содержит один символ имени файла.</span><span class="sxs-lookup"><span data-stu-id="55284-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="55284-126">В языке программирования C наиболее вероятным размером записи является следующий:</span><span class="sxs-lookup"><span data-stu-id="55284-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
