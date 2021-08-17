---
description: В следующем примере показан исходный код, необходимый для создания простой библиотеки DLL, Myputs.dll.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Создание простой библиотеки Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c3708f98c6b916c54940bc1667ebc4827b29c78596f55102331491aca29e65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963794"
---
# <a name="creating-a-simple-dynamic-link-library"></a>Создание простой библиотеки Dynamic-Link

В следующем примере показан исходный код, необходимый для создания простой библиотеки DLL, Myputs.dll. Он определяет простую функцию печати строк с именем Мипутс. Библиотека DLL Мипутс не определяет функцию точки входа, так как она связана с библиотекой времени выполнения языка C и не имеет собственных функций инициализации или очистки для выполнения.

Чтобы создать библиотеку DLL, следуйте указаниям в документации, входящей в состав средств разработки.

Пример использования Мипутс см. в разделе [использование Load-Time динамической компоновки](using-load-time-dynamic-linking.md) или [Использование Run-Time динамической компоновки](using-run-time-dynamic-linking.md).


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



 

 



