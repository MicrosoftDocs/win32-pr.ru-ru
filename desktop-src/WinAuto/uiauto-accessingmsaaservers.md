---
title: Доступ к серверам Microsoft Active Accessibility
description: Прокси-сервер автоматизации пользовательского интерфейса Microsoft Active Accessibility — это программный компонент, который позволяет клиентам автоматизации пользовательского интерфейса Майкрософт взаимодействовать с серверами Microsoft Active Accessibility, которые реализуют интерфейс IAccessible изначально.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Автоматизация пользовательского интерфейса, доступ Active Accessibility
- Модель автоматизации пользовательского интерфейса, Active Accessibility
- Прокси-сервер автоматизации пользовательского интерфейса
- Модель автоматизации пользовательского интерфейса, прокси-сервер автоматизации пользовательского интерфейса
- Шаблон элемента управления Легацииакцессибле
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Легацииакцессибле
- Microsoft Active Accessibility
- Active Accessibility
- Клиенты, доступ к Active Accessibility серверам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067673"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="d3ead-112">Доступ к серверам Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="d3ead-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="d3ead-113">Прокси-сервер автоматизации пользовательского интерфейса Microsoft Active Accessibility — это программный компонент, который позволяет клиентам автоматизации пользовательского интерфейса Майкрософт взаимодействовать с серверами Microsoft Active Accessibility, которые реализуют интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) изначально.</span><span class="sxs-lookup"><span data-stu-id="d3ead-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="d3ead-114">Прокси-сервер поддерживает шаблон элемента управления [легацииакцессибле](uiauto-implementinglegacyiaccessible.md) и предоставляет экземпляр интерфейса [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) для каждого обнаруженного сервера Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d3ead-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="d3ead-115">Клиенты автоматизации пользовательского интерфейса используют методы, предоставляемые **иуиаутоматионлегацииакцессиблепаттерн** для доступа к свойствам и объектам Microsoft Active Accessibility, поддерживаемым сервером.</span><span class="sxs-lookup"><span data-stu-id="d3ead-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="d3ead-116">Если элемент модели автоматизации пользовательского интерфейса имеет базовую реализацию Microsoft Active Accessibility, клиент может получить указатель интерфейса [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) для элемента, передав идентификатор шаблона элемента управления [**UIA \_ легацииакцессиблепаттернид**](uiauto-controlpattern-ids.md) одному из следующих методов [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :</span><span class="sxs-lookup"><span data-stu-id="d3ead-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="d3ead-117">**жеткачедпаттерн**</span><span class="sxs-lookup"><span data-stu-id="d3ead-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="d3ead-118">**жеткачедпаттернас**</span><span class="sxs-lookup"><span data-stu-id="d3ead-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="d3ead-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="d3ead-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="d3ead-120">**жеткуррентпаттернас**</span><span class="sxs-lookup"><span data-stu-id="d3ead-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="d3ead-121">Интерфейс [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) недоступен для элементов управления, основанных на модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d3ead-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="d3ead-122">Интерфейс [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) позволяет клиентам автоматизации пользовательского интерфейса получать доступ к базовой реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) элемента Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d3ead-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="d3ead-123">Однако интерфейс не поддерживает устаревшие или избыточные методы, имеющие функции автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d3ead-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="d3ead-124">Например, **иуиаутоматионлегацииакцессиблепаттерн** не имеет метода, эквивалентного [**IAccessible:: акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , так как текущее расположение элемента пользовательского интерфейса доступно из свойства баундингректангле UI Automation.</span><span class="sxs-lookup"><span data-stu-id="d3ead-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="d3ead-125">Метод [**иуиаутоматионлегацииакцессиблепаттерн:: жетиакцессибле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) позволяет клиенту получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) из элемента модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d3ead-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="d3ead-126">Обратная возможность также возможна с помощью методов [**иуиаутоматион:: елементфромиакцессибле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) и [**Иуиаутоматион:: елементфромиакцессиблебуилдкаче**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .</span><span class="sxs-lookup"><span data-stu-id="d3ead-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="d3ead-127">[**Иуиаутоматионлегацииакцессиблепаттерн:: жетиакцессибле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) возвращает **значение NULL** , если интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента предоставлен прокси-объектом из OLEACC.dll или из модели автоматизации пользовательского интерфейса в Microsoft Active Accessibility Bridge.</span><span class="sxs-lookup"><span data-stu-id="d3ead-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3ead-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d3ead-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d3ead-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d3ead-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d3ead-130">Модель автоматизации пользовательского интерфейса и Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="d3ead-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="d3ead-131">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d3ead-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




