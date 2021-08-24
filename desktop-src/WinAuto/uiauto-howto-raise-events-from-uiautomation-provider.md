---
title: Как вызывать события из поставщика автоматизации пользовательского интерфейса
description: В этом разделе содержится пример кода, показывающий, как поставщик автоматизации пользовательского интерфейса Майкрософт вызывает событие.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75717dfcccaca5f62ac3431f9b3decb01842ce9bc696d07bfff54f35ffc13640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133297"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Как вызывать события из поставщика автоматизации пользовательского интерфейса

В этом разделе содержится пример кода, показывающий, как поставщик автоматизации пользовательского интерфейса Майкрософт вызывает событие.

В следующем примере кода показан метод из приложения, реализующего пользовательскую кнопку. Приложение вызывает метод при каждом вызове пользовательской кнопки. Метод проверяет, прослушивают ли какие либо клиенты события, и, если это так, вызывает событие [**UIA \_ Invoke \_ инвокедевентид**](uiauto-event-ids.md) для уведомления клиентов о том, что была вызвана кнопка.


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Обзор событий автоматизации пользовательского интерфейса](uiauto-eventsoverview.md)
</dt> <dt>

[Разделы руководства для поставщиков автоматизации пользовательского интерфейса](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




