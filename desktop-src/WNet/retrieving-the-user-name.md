---
title: Получение имени пользователя
description: Чтобы получить имя пользователя, связанного с локальным устройством, подключенным к сетевому ресурсу или с именем сети, приложение может вызвать функцию Внетжетусер.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98aeafc849e1a66b373fcb81af46ec47b49644c4b9c753fad480876180a5592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566482"
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

 

 