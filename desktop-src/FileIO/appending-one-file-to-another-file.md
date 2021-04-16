---
description: Пример кода, демонстрирующий, как приложение может добавлять один файл в конец другого файла, включая открытие и закрытие файлов, чтение и запись в файлы, а также блокировку и разблокировку файлов.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Добавление одного файла в другой файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683565"
---
# <a name="appending-one-file-to-another-file"></a><span data-ttu-id="3709e-103">Добавление одного файла в другой файл</span><span class="sxs-lookup"><span data-stu-id="3709e-103">Appending One File to Another File</span></span>

<span data-ttu-id="3709e-104">В примере кода в этом разделе показано, как открывать и закрывать файлы, читать и записывать файлы, а также блокировать и разблокировать файлы.</span><span class="sxs-lookup"><span data-stu-id="3709e-104">The code example in this topic shows you how to open and close files, read and write to files, and lock and unlock files.</span></span>

<span data-ttu-id="3709e-105">В этом примере приложение добавляет один файл в конец другого файла.</span><span class="sxs-lookup"><span data-stu-id="3709e-105">In the example, the application appends one file to the end of another file.</span></span> <span data-ttu-id="3709e-106">Сначала приложение открывает файл, который добавляется с разрешениями, которые позволяют приложению выполнять запись только в него.</span><span class="sxs-lookup"><span data-stu-id="3709e-106">First, the application opens the file being appended with permissions that allow only the application to write to it.</span></span> <span data-ttu-id="3709e-107">Однако в процессе добавления другие процессы могут открыть файл с разрешением только для чтения, который предоставляет представление моментального снимка добавляемого файла.</span><span class="sxs-lookup"><span data-stu-id="3709e-107">However, during the append process other processes can open the file with read-only permission, which provides a snapshot view of the file being appended.</span></span> <span data-ttu-id="3709e-108">Затем файл блокируется во время фактического процесса добавления, чтобы обеспечить целостность данных, записываемых в файл.</span><span class="sxs-lookup"><span data-stu-id="3709e-108">Then, the file is locked during the actual append process to ensure the integrity of the data being written to the file.</span></span>

<span data-ttu-id="3709e-109">В этом примере транзакции не используются.</span><span class="sxs-lookup"><span data-stu-id="3709e-109">This example does not use transactions.</span></span> <span data-ttu-id="3709e-110">Если вы использовали транзакционные операции, доступ будет возможен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3709e-110">If you were using transacted operations, you would only be able have read-only access.</span></span> <span data-ttu-id="3709e-111">В этом случае добавленные данные будут отображаться только после завершения операции фиксации транзакции.</span><span class="sxs-lookup"><span data-stu-id="3709e-111">In this case, you would only see the appended data after the transaction commit operation completed.</span></span>

<span data-ttu-id="3709e-112">В примере также показано, что приложение открывает два файла с помощью [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span><span class="sxs-lookup"><span data-stu-id="3709e-112">The example also shows that the application opens two files by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span></span>

-   <span data-ttu-id="3709e-113">One.txt открыт для чтения.</span><span class="sxs-lookup"><span data-stu-id="3709e-113">One.txt is opened for reading.</span></span>
-   <span data-ttu-id="3709e-114">Two.txt открывается для записи и совместного чтения.</span><span class="sxs-lookup"><span data-stu-id="3709e-114">Two.txt is opened for writing and shared reading.</span></span>

<span data-ttu-id="3709e-115">Затем приложение использует [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) и [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) для добавления содержимого One.txt в конец Two.txt путем чтения и записи блоков размером 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="3709e-115">Then the application uses [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to append the contents of One.txt to the end of Two.txt by reading and writing the 4 KB blocks.</span></span> <span data-ttu-id="3709e-116">Однако перед записью во второй файл приложение использует [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) для установки указателя второго файла на конец этого файла и использует [**локкфиле**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) для блокировки области для записи.</span><span class="sxs-lookup"><span data-stu-id="3709e-116">However, before writing to the second file, the application uses [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) to set the pointer of the second file to the end of that file, and uses [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) to lock the area to be written.</span></span> <span data-ttu-id="3709e-117">Это предотвращает доступ другого потока или процесса к области с помощью повторяющегося маркера, пока выполняется операция записи.</span><span class="sxs-lookup"><span data-stu-id="3709e-117">This prevents another thread or process with a duplicate handle from accessing the area while the write operation is in progress.</span></span> <span data-ttu-id="3709e-118">По завершении каждой операции записи [**унлоккфиле**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) используется для разблокировки заблокированной области.</span><span class="sxs-lookup"><span data-stu-id="3709e-118">When each write operation is complete, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) is used to unlock the locked area.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



