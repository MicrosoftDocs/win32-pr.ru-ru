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
# <a name="creating-named-shared-memory"></a><span data-ttu-id="3f0cd-103">Создание именованной общей памяти</span><span class="sxs-lookup"><span data-stu-id="3f0cd-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="3f0cd-104">Для совместного использования данных несколько процессов могут использовать размещенные в памяти файлы, которые хранятся в файле подкачки системы.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="3f0cd-105">Первый процесс</span><span class="sxs-lookup"><span data-stu-id="3f0cd-105">First Process</span></span>

<span data-ttu-id="3f0cd-106">Первый процесс создает объект сопоставления файлов, вызывая функцию [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) с **недопустимым \_ \_ значением Handle** и именем для объекта.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="3f0cd-107">При использовании флага чтения с помощью **страницы \_** у процесса есть разрешение на чтение и запись в памяти с помощью любых созданных представлений файлов.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="3f0cd-108">Затем процесс использует объект сопоставления файлов, который [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) возвращает в вызове [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , чтобы создать представление файла в адресном пространстве процесса.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="3f0cd-109">Функция **MapViewOfFile** возвращает указатель на представление файла, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="3f0cd-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="3f0cd-110">Затем процесс использует функцию [**копимемори**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) для записи строки в представление, доступ к которому могут получить другие процессы.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="3f0cd-111">При использовании префикса "Global" имена объектов сопоставления файлов \\ позволяют процессам взаимодействовать друг с другом, даже если они находятся в разных сеансах сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="3f0cd-112">Для этого необходимо, чтобы первый процесс имел привилегию [**секреатеглобалпривилеже**](../secauthz/privilege-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0cd-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="3f0cd-113">Когда процессу больше не требуется доступ к объекту сопоставления файлов, он должен вызвать функцию [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="3f0cd-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="3f0cd-114">Когда все дескрипторы закрыты, система может освободить раздел файла подкачки, который использует объект.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


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



## <a name="second-process"></a><span data-ttu-id="3f0cd-115">Второй процесс</span><span class="sxs-lookup"><span data-stu-id="3f0cd-115">Second Process</span></span>

<span data-ttu-id="3f0cd-116">Второй процесс может получить доступ к строке, записанной в общую память, с помощью вызова функции [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) , указывающей то же имя для объекта сопоставления, что и первый процесс.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="3f0cd-117">Затем он может использовать функцию [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) для получения указателя на представление файла, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="3f0cd-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="3f0cd-118">Процесс может отобразить эту строку так же, как и любую другую строку.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="3f0cd-119">В этом примере отображается окно сообщения с сообщением "сообщение от первого процесса", записанное первым процессом.</span><span class="sxs-lookup"><span data-stu-id="3f0cd-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3f0cd-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3f0cd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f0cd-121">Совместное использование файлов и памяти</span><span class="sxs-lookup"><span data-stu-id="3f0cd-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
