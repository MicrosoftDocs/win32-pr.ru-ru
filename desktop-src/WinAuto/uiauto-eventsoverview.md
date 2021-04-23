---
title: Обзор событий автоматизации пользовательского интерфейса
description: Уведомление о событиях автоматизации пользовательского интерфейса Майкрософт — это ключевая функция для вспомогательных технологий, таких как средства чтения с экрана и экранные лупы.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Модель автоматизации пользовательского интерфейса, общие сведения о событиях
- Модель автоматизации пользовательского интерфейса, категории событий
- Автоматизация пользовательского интерфейса, уведомления о событиях
- уведомления о событиях
- события, категории
- события, уведомления о событиях
- События изменения свойств
- События действия элемента
- События изменения структуры
- Глобальные события изменения рабочего стола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337660"
---
# <a name="ui-automation-events-overview"></a><span data-ttu-id="e8c74-113">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8c74-113">UI Automation Events Overview</span></span>

<span data-ttu-id="e8c74-114">Уведомление о событиях автоматизации пользовательского интерфейса Майкрософт — это ключевая функция для вспомогательных технологий, таких как средства чтения с экрана и экранные лупы.</span><span class="sxs-lookup"><span data-stu-id="e8c74-114">Microsoft UI Automation event notification is a key feature for assistive technologies, such as screen readers and screen magnifiers.</span></span> <span data-ttu-id="e8c74-115">Эти клиенты автоматизации пользовательского интерфейса отправляют события, которые вызываются поставщиками автоматизации пользовательского интерфейса, когда что-либо происходит в пользовательском интерфейсе, и используют эти сведения для уведомления конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="e8c74-115">These UI Automation clients track events that are raised by UI Automation providers when something happens in the UI and use the information to notify end users.</span></span>

<span data-ttu-id="e8c74-116">Повысить эффективность можно, позволяя приложениям поставщика вызывать события выборочно в зависимости от того, было ли все клиенты подписаны на эти события или прослушивают ли клиенты события.</span><span class="sxs-lookup"><span data-stu-id="e8c74-116">Efficiency is improved by allowing provider applications to raise events selectively, depending on whether any clients are subscribed to those events, or not at all, if no clients are listening for any events.</span></span>

<span data-ttu-id="e8c74-117">События модели автоматизации пользовательского интерфейса делятся на следующие категории.</span><span class="sxs-lookup"><span data-stu-id="e8c74-117">UI Automation events fall into the following categories.</span></span>



| <span data-ttu-id="e8c74-118">Категория событий</span><span class="sxs-lookup"><span data-stu-id="e8c74-118">Event Category</span></span>        | <span data-ttu-id="e8c74-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e8c74-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c74-120">Изменение свойства</span><span class="sxs-lookup"><span data-stu-id="e8c74-120">Property change</span></span>       | <span data-ttu-id="e8c74-121">Вызывается при изменении свойства элемента модели автоматизации пользовательского интерфейса или шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e8c74-121">Raised when a property on UI Automation element or control pattern changes.</span></span> <span data-ttu-id="e8c74-122">Например, если клиенту необходимо отслеживать элемент управления "флажок приложения", он может зарегистрироваться для прослушивания события изменения свойства в свойстве [**иуиаутоматионтогглепаттерн:: курренттогглестате**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) .</span><span class="sxs-lookup"><span data-stu-id="e8c74-122">For example, if a client needs to monitor an application check box control, it can register to listen for a property change event on the [**IUIAutomationTogglePattern::CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) property.</span></span> <span data-ttu-id="e8c74-123">Когда флажок устанавливается или снимается, поставщик вызывает событие и клиент может выполнить необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="e8c74-123">When the check box control is checked or unchecked, the provider raises the event and the client can act as necessary.</span></span> |
| <span data-ttu-id="e8c74-124">Действие элемента</span><span class="sxs-lookup"><span data-stu-id="e8c74-124">Element action</span></span>        | <span data-ttu-id="e8c74-125">Возникает при изменении в пользовательском интерфейсе в результате изменения пользовательского интерфейса или программного действия, например при нажатии кнопки или вызове через [**иуиаутоматионинвокепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="e8c74-125">Raised when a change in the UI results from end user or programmatic activity, for example, when a button is clicked or invoked through [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e8c74-126">Изменение структуры</span><span class="sxs-lookup"><span data-stu-id="e8c74-126">Structure change</span></span>      | <span data-ttu-id="e8c74-127">Возникает при изменении структуры дерева автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e8c74-127">Raised when the structure of the UI Automation tree changes.</span></span> <span data-ttu-id="e8c74-128">Структура меняется, когда новые элементы пользовательского интерфейса отображаются, скрываются или удаляются с рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e8c74-128">The structure changes when new UI items become visible, hidden, or removed on the desktop.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e8c74-129">Глобальное изменение рабочего стола</span><span class="sxs-lookup"><span data-stu-id="e8c74-129">Global desktop change</span></span> | <span data-ttu-id="e8c74-130">Вызывается, когда выполняются глобальные действия для клиента, например когда фокус переходит от одного элемента к другому или при закрытии окна.</span><span class="sxs-lookup"><span data-stu-id="e8c74-130">Raised when actions of global interest to the client occur, such as when the focus shifts from one element to another, or when a window closes.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e8c74-131">Уведомление</span><span class="sxs-lookup"><span data-stu-id="e8c74-131">Notification</span></span>          | <span data-ttu-id="e8c74-132">Вызывается, когда приложение вызывает функцию [**уиараисенотификатионевент**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) .</span><span class="sxs-lookup"><span data-stu-id="e8c74-132">Raised when an app calls the [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) function.</span></span> <span data-ttu-id="e8c74-133">[**Нотификатионкинд**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) указывает тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="e8c74-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indicates the type of the notification.</span></span>                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="e8c74-134">Некоторые события необязательно означают, что состояние пользовательского интерфейса изменилось.</span><span class="sxs-lookup"><span data-stu-id="e8c74-134">Some events do not necessarily mean that the state of the UI has changed.</span></span> <span data-ttu-id="e8c74-135">Например, если пользователь запустил вкладку в поле ввода текста, а затем нажимает кнопку для обновления поля, то возникает событие [**UIA \_ Text \_ текстчанжедевентид**](uiauto-event-ids.md) , даже если пользователь фактически не изменил текст.</span><span class="sxs-lookup"><span data-stu-id="e8c74-135">For example, if the user tabs to a text entry field, and then clicks a button to update the field, a [**UIA\_Text\_TextChangedEventId**](uiauto-event-ids.md) event is raised, even if the user did not actually change the text.</span></span> <span data-ttu-id="e8c74-136">При обработке события клиентскому приложению может потребоваться проверить, действительно ли что-либо изменилось, перед выполнением действия.</span><span class="sxs-lookup"><span data-stu-id="e8c74-136">When processing an event, it may be necessary for a client application to check whether anything has actually changed before taking action.</span></span>

<span data-ttu-id="e8c74-137">Следующие события могут возникать, даже если состояние пользовательского интерфейса не изменилось.</span><span class="sxs-lookup"><span data-stu-id="e8c74-137">The following events may be raised even when the state of the UI has not changed.</span></span>

-   <span data-ttu-id="e8c74-138">[**UIA \_ Аутоматионпропертичанжедевентид**](uiauto-event-ids.md) (в зависимости от измененного свойства)</span><span class="sxs-lookup"><span data-stu-id="e8c74-138">[**UIA\_AutomationPropertyChangedEventId**](uiauto-event-ids.md) (depending on the property that has changed)</span></span>
-   [<span data-ttu-id="e8c74-139">**UIA \_ SelectionItem \_ елементселектедевентид**</span><span class="sxs-lookup"><span data-stu-id="e8c74-139">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="e8c74-140">**\_Выбор UIA \_ инвалидатедевентид**</span><span class="sxs-lookup"><span data-stu-id="e8c74-140">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="e8c74-141">**\_Текстовая \_ ТЕКСТЧАНЖЕДЕВЕНТИДа UIA**</span><span class="sxs-lookup"><span data-stu-id="e8c74-141">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)

<span data-ttu-id="e8c74-142">Описание всех событий модели автоматизации пользовательского интерфейса см. в разделе [идентификаторы событий](uiauto-event-ids.md).</span><span class="sxs-lookup"><span data-stu-id="e8c74-142">For a description of all UI Automation events, see [Event Identifiers](uiauto-event-ids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8c74-143">См. также</span><span class="sxs-lookup"><span data-stu-id="e8c74-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8c74-144">Подписка на события модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8c74-144">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> </dl>

 

 