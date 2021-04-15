---
description: В следующем примере показан исходный код, необходимый для создания простой библиотеки DLL, Myputs.dll.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Создание простой библиотеки Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572c25c87a3130739a55fcccfc9d8f9c6514d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683053"
---
# <a name="creating-a-simple-dynamic-link-library"></a><span data-ttu-id="51dc9-103">Создание простой библиотеки Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="51dc9-103">Creating a Simple Dynamic-Link Library</span></span>

<span data-ttu-id="51dc9-104">В следующем примере показан исходный код, необходимый для создания простой библиотеки DLL, Myputs.dll.</span><span class="sxs-lookup"><span data-stu-id="51dc9-104">The following example is the source code needed to create a simple DLL, Myputs.dll.</span></span> <span data-ttu-id="51dc9-105">Он определяет простую функцию печати строк с именем Мипутс.</span><span class="sxs-lookup"><span data-stu-id="51dc9-105">It defines a simple string-printing function called myPuts.</span></span> <span data-ttu-id="51dc9-106">Библиотека DLL Мипутс не определяет функцию точки входа, так как она связана с библиотекой времени выполнения языка C и не имеет собственных функций инициализации или очистки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="51dc9-106">The Myputs DLL does not define an entry-point function, because it is linked with the C run-time library and has no initialization or cleanup functions of its own to perform.</span></span>

<span data-ttu-id="51dc9-107">Чтобы создать библиотеку DLL, следуйте указаниям в документации, входящей в состав средств разработки.</span><span class="sxs-lookup"><span data-stu-id="51dc9-107">To build the DLL, follow the directions in the documentation included with your development tools.</span></span>

<span data-ttu-id="51dc9-108">Пример использования Мипутс см. в разделе [использование Load-Time динамической компоновки](using-load-time-dynamic-linking.md) или [Использование Run-Time динамической компоновки](using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="51dc9-108">For an example that uses myPuts, see [Using Load-Time Dynamic Linking](using-load-time-dynamic-linking.md) or [Using Run-Time Dynamic Linking](using-run-time-dynamic-linking.md).</span></span>


```C++
// The myPuts function writes a null-terminated string to
// the standard output device.
 
// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.
 
 
#include <windows.h>
 
#define EOF (-1)
 
#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif
 
__declspec(dllexport) int __cdecl myPuts(LPWSTR lpszMsg)
{
    DWORD cchWritten;
    HANDLE hConout;
    BOOL fRet;
 
    // Get a handle to the console output device.

    hConout = CreateFileW(L"CONOUT$",
                         GENERIC_WRITE,
                         FILE_SHARE_WRITE,
                         NULL,
                         OPEN_EXISTING,
                         FILE_ATTRIBUTE_NORMAL,
                         NULL);

    if (INVALID_HANDLE_VALUE == hConout)
        return EOF;
 
    // Write a null-terminated string to the console output device.
 
    while (*lpszMsg != L'\0')
    {
        fRet = WriteConsole(hConout, lpszMsg, 1, &cchWritten, NULL);
        if( (FALSE == fRet) || (1 != cchWritten) )
            return EOF;
        lpszMsg++;
    }
    return 1;
}
 
#ifdef __cplusplus
}
#endif
```



 

 



