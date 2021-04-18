---
title: Добавление сетевого подключения
description: Чтобы установить соединение с сетевым ресурсом, описанным структурой НЕТРЕСАУРЦЕ, приложение может вызвать функцию WNetAddConnection2, WNetAddConnection3 или Внетусеконнектион.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710325"
---
# <a name="adding-a-network-connection"></a>Добавление сетевого подключения

Чтобы установить соединение с сетевым ресурсом, описанным структурой [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , приложение может вызвать функцию [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)или [**внетусеконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) . В следующем примере демонстрируется использование функции **WNetAddConnection2** .

В примере кода вызывается функция **WNetAddConnection2** , указывающая, что система должна обновить профиль пользователя с информацией, создав "сохраненное" или постоянное подключение. В примере вызывается определяемый приложением обработчик ошибок для обработки ошибок и функция [**текста**](/windows/desktop/api/wingdi/nf-wingdi-textouta) для печати.


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



Функция [**внетаддконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) поддерживается для совместимости с более ранними версиями Windows для рабочих групп. Новые приложения должны вызывать функцию [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) или функцию [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .

Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).

 

 