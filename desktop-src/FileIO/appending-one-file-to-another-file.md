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
# <a name="appending-one-file-to-another-file"></a>Добавление одного файла в другой файл

В примере кода в этом разделе показано, как открывать и закрывать файлы, читать и записывать файлы, а также блокировать и разблокировать файлы.

В этом примере приложение добавляет один файл в конец другого файла. Сначала приложение открывает файл, который добавляется с разрешениями, которые позволяют приложению выполнять запись только в него. Однако в процессе добавления другие процессы могут открыть файл с разрешением только для чтения, который предоставляет представление моментального снимка добавляемого файла. Затем файл блокируется во время фактического процесса добавления, чтобы обеспечить целостность данных, записываемых в файл.

В этом примере транзакции не используются. Если вы использовали транзакционные операции, доступ будет возможен только для чтения. В этом случае добавленные данные будут отображаться только после завершения операции фиксации транзакции.

В примере также показано, что приложение открывает два файла с помощью [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):

-   One.txt открыт для чтения.
-   Two.txt открывается для записи и совместного чтения.

Затем приложение использует [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) и [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) для добавления содержимого One.txt в конец Two.txt путем чтения и записи блоков размером 4 КБ. Однако перед записью во второй файл приложение использует [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) для установки указателя второго файла на конец этого файла и использует [**локкфиле**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) для блокировки области для записи. Это предотвращает доступ другого потока или процесса к области с помощью повторяющегося маркера, пока выполняется операция записи. По завершении каждой операции записи [**унлоккфиле**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) используется для разблокировки заблокированной области.


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



 

 



