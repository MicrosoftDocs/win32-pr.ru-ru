---
title: Получение имени пользователя
description: Чтобы получить имя пользователя, связанного с локальным устройством, подключенным к сетевому ресурсу или с именем сети, приложение может вызвать функцию Внетжетусер.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260954"
---
# <a name="retrieving-the-user-name"></a>Получение имени пользователя

Чтобы получить имя пользователя, связанного с локальным устройством, подключенным к сетевому ресурсу или с именем сети, приложение может вызвать функцию [**внетжетусер**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .

В следующем примере имя устройства используется для получения имени пользователя. В примере вызывается определяемый приложением обработчик ошибок для обработки ошибок и функция [**текста**](/windows/desktop/api/wingdi/nf-wingdi-textouta) для печати.


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).

 

 