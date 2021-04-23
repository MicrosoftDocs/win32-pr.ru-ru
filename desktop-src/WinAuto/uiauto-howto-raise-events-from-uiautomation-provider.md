---
title: Как вызывать события из поставщика автоматизации пользовательского интерфейса
description: В этом разделе содержится пример кода, показывающий, как поставщик автоматизации пользовательского интерфейса Майкрософт вызывает событие.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710131"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a><span data-ttu-id="192e0-103">Как вызывать события из поставщика автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="192e0-103">How to Raise Events from a UI Automation Provider</span></span>

<span data-ttu-id="192e0-104">В этом разделе содержится пример кода, показывающий, как поставщик автоматизации пользовательского интерфейса Майкрософт вызывает событие.</span><span class="sxs-lookup"><span data-stu-id="192e0-104">This topic contains example code that shows how a Microsoft UI Automation provider raises an event.</span></span>

<span data-ttu-id="192e0-105">В следующем примере кода показан метод из приложения, реализующего пользовательскую кнопку.</span><span class="sxs-lookup"><span data-stu-id="192e0-105">The following example code shows a method from an application that implements a custom button.</span></span> <span data-ttu-id="192e0-106">Приложение вызывает метод при каждом вызове пользовательской кнопки.</span><span class="sxs-lookup"><span data-stu-id="192e0-106">The application calls the method whenever the custom button is invoked.</span></span> <span data-ttu-id="192e0-107">Метод проверяет, прослушивают ли какие либо клиенты события, и, если это так, вызывает событие [**UIA \_ Invoke \_ инвокедевентид**](uiauto-event-ids.md) для уведомления клиентов о том, что была вызвана кнопка.</span><span class="sxs-lookup"><span data-stu-id="192e0-107">The method checks whether any clients are listening for events and, if so, raises the [**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md) event to notify the clients that the button was invoked.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="192e0-108">См. также</span><span class="sxs-lookup"><span data-stu-id="192e0-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="192e0-109">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="192e0-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="192e0-110">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="192e0-110">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="192e0-111">Разделы руководства для поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="192e0-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




