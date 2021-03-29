---
description: Пример кода, демонстрирующий использование функции CreateFile для создания нового файла или открытия существующего файла.
ms.assetid: 04e089a7-c559-4a35-a38b-e1acdf3438d1
title: Открытие файла для чтения или записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254684538a64a37cd94841812df84808da8374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810768"
---
# <a name="opening-a-file-for-reading-or-writing"></a>Открытие файла для чтения или записи

Функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) может создать новый файл или открыть существующий файл. Необходимо указать имя файла, инструкции по созданию и другие атрибуты. Когда приложение создает новый файл, операционная система добавляет его в указанный каталог.

## <a name="example-open-a-file-for-writing"></a>Пример. Открытие файла для записи

В следующем примере функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) используется для создания нового файла и открытия для записи и [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) для синхронной записи простой строки в файл.

Последующий вызов для открытия этого файла с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) завершится ошибкой, пока не закроется обработчик.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void DisplayError(LPTSTR lpszFunction);

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    char DataBuffer[] = "This is some test data to write to the file.";
    DWORD dwBytesToWrite = (DWORD)strlen(DataBuffer);
    DWORD dwBytesWritten = 0;
    BOOL bErrorFlag = FALSE;

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error:\tIncorrect number of arguments\n\n");
        _tprintf(TEXT("%s <file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // name of the write
                       GENERIC_WRITE,          // open for writing
                       0,                      // do not share
                       NULL,                   // default security
                       CREATE_NEW,             // create new file only
                       FILE_ATTRIBUTE_NORMAL,  // normal file
                       NULL);                  // no attr. template

    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: Unable to open file \"%s\" for write.\n"), argv[1]);
        return;
    }

    _tprintf(TEXT("Writing %d bytes to %s.\n"), dwBytesToWrite, argv[1]);

    bErrorFlag = WriteFile( 
                    hFile,           // open file handle
                    DataBuffer,      // start of data to write
                    dwBytesToWrite,  // number of bytes to write
                    &dwBytesWritten, // number of bytes that were written
                    NULL);            // no overlapped structure

    if (FALSE == bErrorFlag)
    {
        DisplayError(TEXT("WriteFile"));
        printf("Terminal failure: Unable to write to file.\n");
    }
    else
    {
        if (dwBytesWritten != dwBytesToWrite)
        {
            // This is an error because a synchronous write that results in
            // success (WriteFile returns TRUE) should write all data as
            // requested. This would not necessarily be the case for
            // asynchronous writes.
            printf("Error: dwBytesWritten != dwBytesToWrite\n");
        }
        else
        {
            _tprintf(TEXT("Wrote %d bytes to %s successfully.\n"), dwBytesWritten, argv[1]);
        }
    }

    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
```



## <a name="example-open-a-file-for-reading"></a>Пример: Открытие файла для чтения

В следующем примере функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) используется для открытия существующего файла для чтения и [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) для считывания до 80 символов синхронно из файла.

В этом случае [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) выполняется, только если указанный файл уже существует в текущем каталоге. Последующий вызов для открытия этого файла с помощью функции **CreateFile** будет выполнен, если вызов использует тот же режим доступа и общий доступ.

Совет. для проверки этого примера можно использовать созданный вами файл с предыдущим примером WriteFile.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFFERSIZE 5
DWORD g_BytesTransferred = 0;

void DisplayError(LPTSTR lpszFunction);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped
);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped )
 {
  _tprintf(TEXT("Error code:\t%x\n"), dwErrorCode);
  _tprintf(TEXT("Number of bytes:\t%x\n"), dwNumberOfBytesTransfered);
  g_BytesTransferred = dwNumberOfBytesTransfered;
 }

//
// Note: this simplified sample assumes the file to read is an ANSI text file
// only for the purposes of output to the screen. CreateFile and ReadFile
// do not use parameters to differentiate between text and binary file types.
//

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    DWORD  dwBytesRead = 0;
    char   ReadBuffer[BUFFERSIZE] = {0};
    OVERLAPPED ol = {0};

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error: Incorrect number of arguments\n\n");
        _tprintf(TEXT("Usage:\n\t%s <text_file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],               // file to open
                       GENERIC_READ,          // open for reading
                       FILE_SHARE_READ,       // share for reading
                       NULL,                  // default security
                       OPEN_EXISTING,         // existing file only
                       FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED, // normal file
                       NULL);                 // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: unable to open file \"%s\" for read.\n"), argv[1]);
        return; 
    }

    // Read one character less than the buffer size to save room for
    // the terminating NULL character. 

    if( FALSE == ReadFileEx(hFile, ReadBuffer, BUFFERSIZE-1, &ol, FileIOCompletionRoutine) )
    {
        DisplayError(TEXT("ReadFile"));
        printf("Terminal failure: Unable to read from file.\n GetLastError=%08x\n", GetLastError());
        CloseHandle(hFile);
        return;
    }
    SleepEx(5000, TRUE);
    dwBytesRead = g_BytesTransferred;
    // This is the section of code that assumes the file is ANSI text. 
    // Modify this block for other data types if needed.

    if (dwBytesRead > 0 && dwBytesRead <= BUFFERSIZE-1)
    {
        ReadBuffer[dwBytesRead]='\0'; // NULL character

        _tprintf(TEXT("Data read from %s (%d bytes): \n"), argv[1], dwBytesRead);
        printf("%s\n", ReadBuffer);
    }
    else if (dwBytesRead == 0)
    {
        _tprintf(TEXT("No data read from file %s\n"), argv[1]);
    }
    else
    {
        printf("\n ** Unexpected value for dwBytesRead ** \n");
    }

    // It is always good practice to close the open file handles even though
    // the app will exit here and clean up open handles anyway.
    
    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание и открытие файлов](creating-and-opening-files.md)
</dt> </dl>

 

 



