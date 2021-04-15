---
title: Использование диалогового окна «соединения»
description: Функция Внетконнектиондиалог создает диалоговое окно, позволяющее пользователю просматривать сетевые ресурсы и подключаться к ним.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338204"
---
# <a name="using-the-connections-dialog-box"></a>Использование диалогового окна «соединения»

Функция [**внетконнектиондиалог**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) создает диалоговое окно, позволяющее пользователю просматривать сетевые ресурсы и подключаться к ним. Вы также можете вызвать функцию [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) , чтобы создать диалоговое окно "соединения". Для **WNetConnectionDialog1** требуется структура [**коннектдлгструкт**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .

Функция [**внетдисконнектдиалог**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) создает диалоговое окно, позволяющее пользователю отключиться от сетевых ресурсов.

В следующем примере кода показано, как вызвать функцию **внетконнектиондиалог** для создания диалогового окна, отображающего дисковые ресурсы. Если вызов завершается неудачей, пример вызывает обработчик ошибок, определенный приложением.


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).

 

 