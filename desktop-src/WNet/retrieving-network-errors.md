---
title: Получение сетевых ошибок
description: Функции Внет возвращают коды ошибок для совместимости с Windows для рабочих групп. Каждая функция Внет также задает значение кода ошибки, возвращаемое GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436d63b51d0f57698403d206774710450eee1c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700896"
---
# <a name="retrieving-network-errors"></a>Получение сетевых ошибок

Функции Внет возвращают коды ошибок для совместимости с Windows для рабочих групп. Каждая функция Внет также задает значение кода ошибки, возвращаемое [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Когда одна из функций Внет возвращает ошибку \_ расширенной \_ ошибки, приложение может вызвать функцию [**внетжетластеррор**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) для получения дополнительных сведений об ошибке. Эти сведения обычно относятся к поставщику сети.

В следующем примере показана определенная приложением функция обработки ошибок (Нетеррорхандлер). Функция принимает три аргумента: обработчик окна, код ошибки, возвращенный одной из функций Внет, и имя функции, вызвавшей ошибку. Если код ошибки \_ расширенной \_ ошибки, Нетеррорхандлер вызывает **внетжетластеррор** для получения расширенных сведений об ошибке и выводит сведения. В примере вызывается функция [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) для обработки сообщений.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 