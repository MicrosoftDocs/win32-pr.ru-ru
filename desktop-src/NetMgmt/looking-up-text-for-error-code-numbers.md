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
# <a name="looking-up-text-for-error-code-numbers"></a><span data-ttu-id="2ceda-104">Поиск текста с кодами ошибок</span><span class="sxs-lookup"><span data-stu-id="2ceda-104">Looking Up Text for Error Code Numbers</span></span>

<span data-ttu-id="2ceda-105">Иногда необходимо отобразить текст ошибки, связанный с кодами ошибок, возвращаемыми функциями, связанными с сетью.</span><span class="sxs-lookup"><span data-stu-id="2ceda-105">It is sometimes necessary to display error text associated with error codes returned from networking-related functions.</span></span> <span data-ttu-id="2ceda-106">Может потребоваться выполнить эту задачу с помощью функций управления сетью, предоставляемых системой.</span><span class="sxs-lookup"><span data-stu-id="2ceda-106">You may need to perform this task with the network management functions provided by the system.</span></span>

<span data-ttu-id="2ceda-107">Текст ошибки для этих сообщений находится в файле таблицы сообщений с именем Netmsg.dll, который находится в папке% systemroot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="2ceda-107">The error text for these messages is found in the message table file named Netmsg.dll, which is found in %systemroot%\\system32.</span></span> <span data-ttu-id="2ceda-108">Этот файл содержит сообщения об ошибках в диапазоне НЕРР \_ base (от 2100) до Max \_ НЕРР (Нерр \_ base + 899).</span><span class="sxs-lookup"><span data-stu-id="2ceda-108">This file contains error messages in the range NERR\_BASE (2100) through MAX\_NERR(NERR\_BASE+899).</span></span> <span data-ttu-id="2ceda-109">Эти коды ошибок определены в файле заголовка пакета SDK лмерр. h.</span><span class="sxs-lookup"><span data-stu-id="2ceda-109">These error codes are defined in the SDK header file lmerr.h.</span></span>

<span data-ttu-id="2ceda-110">Функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) могут загружать Netmsg.dll.</span><span class="sxs-lookup"><span data-stu-id="2ceda-110">The [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) functions can load Netmsg.dll.</span></span> <span data-ttu-id="2ceda-111">Функция [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) сопоставляет код ошибки с текстом сообщения при наличии обработчика модуля для файла Netmsg.dll.</span><span class="sxs-lookup"><span data-stu-id="2ceda-111">The [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function maps an error code to message text, given a module handle to the Netmsg.dll file.</span></span>

<span data-ttu-id="2ceda-112">В следующем примере показано, как отобразить текст ошибки, связанный с функциями управления сетью, в дополнение к отображению текста ошибки, связанного с кодами ошибок, связанными с системой.</span><span class="sxs-lookup"><span data-stu-id="2ceda-112">The following sample illustrates how to display error text associated with network management functions, in addition to displaying error text associated with system-related error codes.</span></span> <span data-ttu-id="2ceda-113">Если указанный номер ошибки находится в определенном диапазоне, то модуль сообщения netmsg.dll загружается и используется для поиска указанного номера ошибки с помощью функции [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="2ceda-113">If the supplied error number is in a specific range, the netmsg.dll message module is loaded and used to look up the specified error number with the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function.</span></span>


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



<span data-ttu-id="2ceda-114">После компиляции этой программы можно вставить номер кода ошибки в качестве аргумента, и программа отобразит текст.</span><span class="sxs-lookup"><span data-stu-id="2ceda-114">After you compile this program, you can insert the error code number as an argument and the program will display the text.</span></span> <span data-ttu-id="2ceda-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="2ceda-115">For example:</span></span>

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 