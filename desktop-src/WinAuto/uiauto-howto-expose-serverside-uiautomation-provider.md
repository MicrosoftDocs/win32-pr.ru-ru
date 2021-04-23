---
title: Как предоставить поставщик автоматизации пользовательского интерфейса Server-Side
description: Этот раздел содержит пример кода, показывающий, как предоставить поставщик автоматизации пользовательского интерфейса Майкрософт на стороне сервера для пользовательского элемента управления.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258625"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="2b7de-103">Как предоставить поставщик автоматизации пользовательского интерфейса Server-Side</span><span class="sxs-lookup"><span data-stu-id="2b7de-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="2b7de-104">Этот раздел содержит пример кода, показывающий, как предоставить поставщик автоматизации пользовательского интерфейса Майкрософт на стороне сервера для пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2b7de-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="2b7de-105">Служба автоматизации пользовательского интерфейса Майкрософт отправляет сообщение [**WM \_ GetObject**](wm-getobject.md) в приложение поставщика для получения сведений о доступном объекте, поддерживаемом поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2b7de-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="2b7de-106">Автоматизация пользовательского интерфейса **отправляет \_ объект WM GetObject** , когда клиент [**вызывает иуиаутоматион:: Елементфромхандле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**елементфромпоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)и [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), а также при обработке событий, для которых зарегистрирован клиент.</span><span class="sxs-lookup"><span data-stu-id="2b7de-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="2b7de-107">Когда поставщик получает сообщение [**WM \_ GetObject**](wm-getobject.md) , он должен проверить, равен ли параметр *lParam* значению **уиарутобжектид**.</span><span class="sxs-lookup"><span data-stu-id="2b7de-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="2b7de-108">Если это так, поставщик должен вернуть интерфейс [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) объекта.</span><span class="sxs-lookup"><span data-stu-id="2b7de-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="2b7de-109">Поставщик возвращает интерфейс путем вызова функции [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="2b7de-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="2b7de-110">В следующем примере показано, как реагировать на [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="2b7de-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a><span data-ttu-id="2b7de-111">См. также</span><span class="sxs-lookup"><span data-stu-id="2b7de-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2b7de-112">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2b7de-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b7de-113">Реализация поставщика автоматизации пользовательского интерфейса Server-Side</span><span class="sxs-lookup"><span data-stu-id="2b7de-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="2b7de-114">Сообщение WM \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="2b7de-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="2b7de-115">Разделы руководства для поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b7de-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




