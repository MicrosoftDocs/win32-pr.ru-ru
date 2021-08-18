---
description: Когда вызов метода вызывает ошибку, многие функции возвращают код ошибки.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Получение сообщений об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96ffb6627dac4f8612a80c68b1a227516ec645440c56dd7c58672cd8222c23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900515"
---
# <a name="retrieving-error-messages"></a>Получение сообщений об ошибках

Когда вызов метода вызывает ошибку, многие функции возвращают код ошибки. Для большинства интерфейсов служб сертификации и элементов API, которые возвращают код ошибки, текст сообщения об ошибке можно получить, вызвав метод [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) с **нулевым** маркером модуля. Если **FormatMessage** не удается, код ошибки, скорее всего, привел к появлению элемента API резервного копирования или ошибки, связанной с базой данных; вызов **FormatMessage** с помощью обработчика модуля, соответствующего библиотеке Ntdsbmsg.dll, должен получить текст сообщения об ошибке. В следующем примере показано, как получить текст сообщения об ошибке в приложении служб сертификации.


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
