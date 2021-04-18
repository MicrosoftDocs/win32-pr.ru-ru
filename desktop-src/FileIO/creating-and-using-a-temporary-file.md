---
description: Пример кода, показывающий, как создать временный файл для обработки данных с помощью функций метода GetTempFileName и Жеттемппас.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Создание и использование временного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca18b7b72aab7c53bea95c38147af66f2b7fef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682652"
---
# <a name="creating-and-using-a-temporary-file"></a>Создание и использование временного файла

Приложения могут получать уникальные имена файлов и путей для временных файлов с помощью функций [**метода GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) и [**жеттемппас**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) . Функция **метода GetTempFileName** создает уникальное имя файла, а функция **жеттемппас** извлекает путь к каталогу, в котором необходимо создать временные файлы.

Следующая процедура описывает, как приложение создает временный файл для обработки данных.

**Создание и использование временного файла**

1.  Приложение открывает файл исходного текста, предоставленный пользователем, с помощью [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
2.  Приложение получает путь к временному файлу и имя файла с помощью функций [**жеттемппас**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) и [**метода GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) , а затем использует [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) для создания временного файла.
3.  Приложение считывает блоки текстовых данных в буфер, преобразует содержимое буфера в верхний регистр с помощью функции [чаруппербуффа](/windows/win32/api/winuser/nf-winuser-charupperbuffa) и записывает преобразованный буфер во временный файл.
4.  Когда весь исходный файл записывается во временный файл, приложение закрывает оба файла и переименовывает временный файл в "allcaps.txt" с помощью функции [**мовефиликс**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) .

Каждый из предыдущих шагов проверяется на успешное выполнение перед переходом к следующему шагу, а в случае возникновения ошибки отображается описание сбоя. Приложение будет завершено сразу после отображения сообщения об ошибке.

Обратите внимание, что Управление текстовыми файлами было выбрано только для простоты демонстрации и может быть заменено любой необходимой процедурой обработки данных. Файл данных может иметь любой тип данных, а не только текст.

Функция [**жеттемппас**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) извлекает полный путь к строке из переменной среды, но не проверяет наличие пути или достаточных прав доступа к этому пути, что является обязанностью разработчика приложения. Дополнительные сведения см. в разделе [**жеттемппас**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha). В следующем примере ошибка рассматривается как условие терминала, и приложение завершает работу после отправки описательного сообщения в стандартный вывод. Однако существует множество других вариантов, таких как запрос на ввод во временный каталог или простая попытка использовать текущий каталог.

> [!Note]  
> Функция [**метода GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) не требует использования функции [**жеттемппас**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .

 

В следующем примере C++ показано, как создать временный файл для обработки данных.


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
