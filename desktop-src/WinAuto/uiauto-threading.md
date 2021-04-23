---
title: Основные сведения о проблемах с потоками
description: В этом разделе описываются распространенные сценарии работы с потоками для реализации клиентов автоматизации пользовательского интерфейса Майкрософт и объясняется, как избежать проблем, которые могут возникать в случае неправильного использования потоков клиентом.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- Клиенты, проблемы с потоками модели автоматизации пользовательского интерфейса
- Клиенты, проблемы с потоками
- Клиенты, потоковая модель обработчика событий
- Клиенты, потоковая модель обработчика событий модели автоматизации пользовательского интерфейса
- Клиенты, сходство модели автоматизации пользовательского интерфейса
- Клиенты, сходство
- Автоматизация пользовательского интерфейса, проблемы с потоками
- Автоматизация пользовательского интерфейса, потоковая модель обработчика событий
- Модель автоматизации пользовательского интерфейса, сходство
- вопросы, связанные с потоками
- Потоковая модель обработчика событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070057"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="17e57-114">Основные сведения о проблемах с потоками</span><span class="sxs-lookup"><span data-stu-id="17e57-114">Understanding Threading Issues</span></span>

<span data-ttu-id="17e57-115">В этом разделе описываются распространенные сценарии работы с потоками для реализации клиентов автоматизации пользовательского интерфейса Майкрософт и объясняется, как избежать проблем, которые могут возникать в случае неправильного использования потоков клиентом.</span><span class="sxs-lookup"><span data-stu-id="17e57-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="17e57-116">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="17e57-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="17e57-117">Модель автоматизации пользовательского интерфейса и поток пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="17e57-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="17e57-118">Потоковая модель для обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="17e57-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="17e57-119">Сходство апартамента COM в 64-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="17e57-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="17e57-120">См. также</span><span class="sxs-lookup"><span data-stu-id="17e57-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="17e57-121">Модель автоматизации пользовательского интерфейса и поток пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="17e57-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="17e57-122">В связи с тем, что модель автоматизации пользовательского интерфейса использует сообщения Windows, конфликты могут возникать, когда клиентское приложение пытается взаимодействовать с собственным ИНТЕРФЕЙСом в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="17e57-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="17e57-123">Эти конфликты могут привести к очень низкому снижению производительности или даже вызвать зависание приложения.</span><span class="sxs-lookup"><span data-stu-id="17e57-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="17e57-124">Если клиентское приложение предназначено для взаимодействия со всеми элементами на рабочем столе, включая собственный пользовательский интерфейс, все вызовы автоматизации пользовательского интерфейса следует выполнять из отдельного потока.</span><span class="sxs-lookup"><span data-stu-id="17e57-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="17e57-125">Это включает в себя поиск элементов, например с помощью [**иуиаутоматионтривалкер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) или метода [**Иуиаутоматионелемент:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) и использование шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="17e57-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="17e57-126">Этот поток не должен владеть ни одним из окон, а должен быть потоком модели многопотокового апартамента (MTA) модели COM (в котором инициализируется COM путем вызова [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) с флагом " **\_ многопотоковый** ".)</span><span class="sxs-lookup"><span data-stu-id="17e57-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="17e57-127">Вызовы автоматизации пользовательского интерфейса можно использовать в обработчике событий автоматизации пользовательского интерфейса, так как обработчик событий всегда вызывается в потоке, не являющемся интерфейсом пользователя.</span><span class="sxs-lookup"><span data-stu-id="17e57-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="17e57-128">Однако при подписке на события, которые могут поступать из пользовательского интерфейса клиентского приложения, необходимо выполнить вызов [**иуиаутоматион:: аддаутоматионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)или связанного метода в потоке, отличном от пользовательского интерфейса (который также должен быть потоком MTA).</span><span class="sxs-lookup"><span data-stu-id="17e57-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="17e57-129">Удалите обработчики событий в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="17e57-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="17e57-130">Клиент автоматизации пользовательского интерфейса не должен использовать несколько потоков для добавления или удаления обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="17e57-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="17e57-131">Непредвиденное поведение может возникнуть, если один или несколько обработчиков событий добавляются или удаляются в рамках одного и того же клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="17e57-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="17e57-132">Потоковая модель для обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="17e57-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="17e57-133">Клиент автоматизации пользовательского интерфейса должен использовать модель потоков COM MTA для потоков, реализующих обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="17e57-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="17e57-134">Использование модели однопотокового подразделения (STA) может вызвать такие проблемы, как предотвращение удаления клиентами обработчиков событий из потока.</span><span class="sxs-lookup"><span data-stu-id="17e57-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="17e57-135">Сходство апартамента COM в 64-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="17e57-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="17e57-136">В соответствии со спецификацией COM время существования удаленного объекта регулируется временем существования апартамента, в котором вызывается функция [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="17e57-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="17e57-137">Когда исходный апартамент завершает работу, удаленный объект также освобождается.</span><span class="sxs-lookup"><span data-stu-id="17e57-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="17e57-138">Для клиентов автоматизации пользовательского интерфейса это поведение COM может означать, что время существования удаленного вспомогательного метода 32/64 (созданного UIAutomationCore.dll), используемого 32-битным элементом, регулируется временем существования апартамента потока, создавшего элемент.</span><span class="sxs-lookup"><span data-stu-id="17e57-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="17e57-139">Если клиент автоматизации пользовательского интерфейса маршалирует элемент в другой поток, элемент может стать недействительным при завершении работы исходного апартамента.</span><span class="sxs-lookup"><span data-stu-id="17e57-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="17e57-140">Клиент автоматизации пользовательского интерфейса должен надлежащим образом обработать эти проблемы за счет перехвата ошибок при использовании упакованных элементов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="17e57-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="17e57-141">Эта же ошибка может возникнуть в 32-разрядном клиенте автоматизации пользовательского интерфейса с 64-разрядными элементами.</span><span class="sxs-lookup"><span data-stu-id="17e57-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17e57-142">См. также</span><span class="sxs-lookup"><span data-stu-id="17e57-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="17e57-143">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="17e57-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17e57-144">Получение элементов автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="17e57-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="17e57-145">Подписка на события модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="17e57-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="17e57-146">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="17e57-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="17e57-147">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="17e57-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="17e57-148">СВЕДЕНИЯ: описания и работа моделей потоков OLE</span><span class="sxs-lookup"><span data-stu-id="17e57-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 