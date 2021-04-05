---
title: Получение сведений о сетевом ресурсе
description: Чтобы узнать, какой поставщик сети владеет ресурсом, приложение может вызвать функцию Внетжетресаурцеинформатион, как показано в следующем примере кода.
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134202"
---
# <a name="retrieving-information-about-a-network-resource"></a>Получение сведений о сетевом ресурсе

Чтобы узнать, какой поставщик сети владеет ресурсом, приложение может вызвать функцию [**внетжетресаурцеинформатион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , как показано в следующем примере кода.

Следующий пример представляет собой функцию (Чекксервер), которая принимает имя сервера в качестве параметра и возвращает сведения об этом сервере. Сначала функция вызывает функцию [**зеромемори**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) для инициализации содержимого блока памяти до нуля. Затем в примере вызывается функция [**внетжетресаурцеинформатион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , указывающая буфер, достаточно большой для хранения структуры [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . Подпрограммы включают обработку ошибок для обработки ситуации, когда буфер этого размера недостаточен для хранения строк переменной длины, в которые входят члены точки структуры **нетресаурце** . Если эта ошибка возникает, пример выделяет достаточно памяти и снова вызывает **внетжетресаурцеинформатион** . Наконец, в примере освобождается выделенная память.

Обратите внимание, что в примере предполагается, что параметр *псзсервер* указывает на имя сервера, распознаваемый одним из сетевых поставщиков на локальном компьютере.


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 