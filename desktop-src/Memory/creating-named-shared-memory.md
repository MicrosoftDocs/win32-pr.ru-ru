---
description: Для совместного использования данных несколько процессов могут использовать размещенные в памяти файлы, которые хранятся в файле подкачки системы.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Создание именованной общей памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682609"
---
# <a name="creating-named-shared-memory"></a>Создание именованной общей памяти

Для совместного использования данных несколько процессов могут использовать размещенные в памяти файлы, которые хранятся в файле подкачки системы.

## <a name="first-process"></a>Первый процесс

Первый процесс создает объект сопоставления файлов, вызывая функцию [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) с **недопустимым \_ \_ значением Handle** и именем для объекта. При использовании флага чтения с помощью **страницы \_** у процесса есть разрешение на чтение и запись в памяти с помощью любых созданных представлений файлов.

Затем процесс использует объект сопоставления файлов, который [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) возвращает в вызове [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , чтобы создать представление файла в адресном пространстве процесса. Функция **MapViewOfFile** возвращает указатель на представление файла, `pBuf` . Затем процесс использует функцию [**копимемори**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) для записи строки в представление, доступ к которому могут получить другие процессы.

При использовании префикса "Global" имена объектов сопоставления файлов \\ позволяют процессам взаимодействовать друг с другом, даже если они находятся в разных сеансах сервера терминалов. Для этого необходимо, чтобы первый процесс имел привилегию [**секреатеглобалпривилеже**](../secauthz/privilege-constants.md) .

Когда процессу больше не требуется доступ к объекту сопоставления файлов, он должен вызвать функцию [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . Когда все дескрипторы закрыты, система может освободить раздел файла подкачки, который использует объект.


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a>Второй процесс

Второй процесс может получить доступ к строке, записанной в общую память, с помощью вызова функции [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) , указывающей то же имя для объекта сопоставления, что и первый процесс. Затем он может использовать функцию [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) для получения указателя на представление файла, `pBuf` . Процесс может отобразить эту строку так же, как и любую другую строку. В этом примере отображается окно сообщения с сообщением "сообщение от первого процесса", записанное первым процессом.


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Совместное использование файлов и памяти](sharing-files-and-memory.md)
</dt> </dl>

 

 
