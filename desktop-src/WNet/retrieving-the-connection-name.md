---
title: Получение имени подключения
description: Чтобы получить имя сетевого ресурса, связанного с локальным устройством, приложение может вызвать функцию Внетжетконнектион, как показано в следующем примере.
ms.assetid: 7c02cf9a-cca3-47d8-8a4b-f2245f1db92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac84aec3c6aafb8a5113ea29251247a1de35aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134199"
---
# <a name="retrieving-the-connection-name"></a><span data-ttu-id="b2a96-103">Получение имени подключения</span><span class="sxs-lookup"><span data-stu-id="b2a96-103">Retrieving the Connection Name</span></span>

<span data-ttu-id="b2a96-104">Чтобы получить имя сетевого ресурса, связанного с локальным устройством, приложение может вызвать функцию [**внетжетконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b2a96-104">To retrieve the name of the network resource associated with a local device, an application can call the [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) function, as shown in the following sample.</span></span>

<span data-ttu-id="b2a96-105">В следующем примере вызывается определяемый приложением обработчик ошибок для обработки ошибок и функция [**текста**](/windows/desktop/api/wingdi/nf-wingdi-textouta) для печати.</span><span class="sxs-lookup"><span data-stu-id="b2a96-105">The following sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
TCHAR szDeviceName[80]; 
DWORD dwResult, cchBuff = sizeof(szDeviceName); 
 
// Call the WNetGetConnection function.
//
dwResult = WNetGetConnection(_T("z:"), 
    szDeviceName, 
    &cchBuff); 
 
switch (dwResult) 
{ 
    //
    // Print the connection name or process errors.
    //
    case NO_ERROR: 
        printf("Connection name: %s\n", szDeviceName); 
        break; 
    //
    // The device is not a redirected device.
    //
    case ERROR_NOT_CONNECTED: 
        printf("Device z: not connected.\n"); 
        break;
    //
    // The device is not currently connected, but it is a persistent connection.
    //
    case ERROR_CONNECTION_UNAVAIL: 
        printf("Connection unavailable.\n"); 
        break;
    //
    // Handle the error.
    //
    default: 
        printf("WNetGetConnection failed.\n"); 
}
```



<span data-ttu-id="b2a96-106">Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b2a96-106">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 