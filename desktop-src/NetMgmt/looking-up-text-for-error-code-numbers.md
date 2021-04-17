---
title: Поиск текста с кодами ошибок
description: Иногда необходимо отобразить текст ошибки, связанный с кодами ошибок, возвращаемыми функциями, связанными с сетью. Может потребоваться выполнить эту задачу с помощью функций управления сетью, предоставляемых системой.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681638"
---
# <a name="looking-up-text-for-error-code-numbers"></a>Поиск текста с кодами ошибок

Иногда необходимо отобразить текст ошибки, связанный с кодами ошибок, возвращаемыми функциями, связанными с сетью. Может потребоваться выполнить эту задачу с помощью функций управления сетью, предоставляемых системой.

Текст ошибки для этих сообщений находится в файле таблицы сообщений с именем Netmsg.dll, который находится в папке% systemroot% \\ System32. Этот файл содержит сообщения об ошибках в диапазоне НЕРР \_ base (от 2100) до Max \_ НЕРР (Нерр \_ base + 899). Эти коды ошибок определены в файле заголовка пакета SDK лмерр. h.

Функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) могут загружать Netmsg.dll. Функция [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) сопоставляет код ошибки с текстом сообщения при наличии обработчика модуля для файла Netmsg.dll.

В следующем примере показано, как отобразить текст ошибки, связанный с функциями управления сетью, в дополнение к отображению текста ошибки, связанного с кодами ошибок, связанными с системой. Если указанный номер ошибки находится в определенном диапазоне, то модуль сообщения netmsg.dll загружается и используется для поиска указанного номера ошибки с помощью функции [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



После компиляции этой программы можно вставить номер кода ошибки в качестве аргумента, и программа отобразит текст. Пример:

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 