---
title: Отмена сетевого подключения
description: Чтобы отменить подключение к сетевому ресурсу, приложение может вызвать функцию WNetCancelConnection2, как показано в следующем примере.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb5c74faa1e1f8b75d0e3b604d89615c6ad1481384a661253ee204dd3ee6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566924"
---
# <a name="canceling-a-network-connection"></a>Отмена сетевого подключения

Чтобы отменить подключение к сетевому ресурсу, приложение может вызвать функцию [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , как показано в следующем примере.

Вызов **WNetCancelConnection2** указывает, что сетевое подключение больше не должно быть постоянным. В примере вызывается определяемый приложением обработчик ошибок для обработки ошибок и функция [**текста**](/windows/desktop/api/wingdi/nf-wingdi-textouta) для печати.


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



функция [**внетканцелконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) поддерживается для совместимости с более ранними версиями Windows для рабочих групп. Для новых приложений используйте [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).

 

 