---
description: Пример кода, демонстрирующий использование базовых потоков файловой системы NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Использование потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265847"
---
# <a name="using-streams"></a><span data-ttu-id="4429a-103">Использование потоков</span><span class="sxs-lookup"><span data-stu-id="4429a-103">Using Streams</span></span>

<span data-ttu-id="4429a-104">В примере в этом разделе показано, как использовать базовые потоки файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="4429a-104">The example in this topic demonstrates how to use basic NTFS file system streams.</span></span>

<span data-ttu-id="4429a-105">В этом примере создается файл с именем "TestFile" и размером 16 байт.</span><span class="sxs-lookup"><span data-stu-id="4429a-105">This example creates a file, called "TestFile," with a size of 16 bytes.</span></span> <span data-ttu-id="4429a-106">Однако файл также имеет дополнительный тип потока:: $DATA с именем Stream, который добавляет дополнительные 23 байта, не сообщаемые операционной системой.</span><span class="sxs-lookup"><span data-stu-id="4429a-106">However, the file also has an additional ::$DATA stream type, named "Stream" which adds an additional 23 bytes that is not reported by the operating system.</span></span> <span data-ttu-id="4429a-107">Поэтому при просмотре свойства Размер файла для файла отображается только размер потока Default:: $DATA для файла.</span><span class="sxs-lookup"><span data-stu-id="4429a-107">Therefore, when you view the file size property for the file, you see only the size of default ::$DATA stream for the file.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



<span data-ttu-id="4429a-108">Если ввести в командной строке **тип TestFile** , он отобразит следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="4429a-108">If you type **Type TestFile** at a command prompt, it displays the following output:</span></span>

``` syntax
This is TestFile
```

<span data-ttu-id="4429a-109">Однако если ввести слова **типа TestFile: Stream**, выдается следующая ошибка:</span><span class="sxs-lookup"><span data-stu-id="4429a-109">However, if you type the words **Type TestFile:Stream**, it generates the following error:</span></span>

<span data-ttu-id="4429a-110">Неверный синтаксис имени файла, имени каталога или метки тома ".</span><span class="sxs-lookup"><span data-stu-id="4429a-110">"The filename, directory name, or volume label syntax is incorrect."</span></span>

<span data-ttu-id="4429a-111">Чтобы просмотреть содержимое файла TestFile: Stream, используйте одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="4429a-111">To view what is in TestFile:stream, use one of the following commands:</span></span>

<span data-ttu-id="4429a-112">**Дополнительные < TestFile: Stream**</span><span class="sxs-lookup"><span data-stu-id="4429a-112">**More < TestFile:Stream**</span></span>

<span data-ttu-id="4429a-113">**Дополнительные < TestFile: Stream: $DATA**</span><span class="sxs-lookup"><span data-stu-id="4429a-113">**More < TestFile:Stream:$DATA**</span></span>

<span data-ttu-id="4429a-114">Отображаемый текст выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4429a-114">The text displayed is as follows:</span></span>

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a><span data-ttu-id="4429a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4429a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4429a-116">Файловые потоки</span><span class="sxs-lookup"><span data-stu-id="4429a-116">File Streams</span></span>](file-streams.md)
</dt> </dl>

 

 



