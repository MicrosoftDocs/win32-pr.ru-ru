---
title: Секции
description: Секции
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Платформа текстовых служб (TSF), секции
- TSF (платформа текстовых служб), секции
- текстовые службы, секции
- Приложения с поддержкой TSF, секции
- секции
- Платформа текстовых служб (TSF), типы секций
- TSF (платформа текстовых служб), типы секций
- текстовые службы, типы секций
- Приложения с поддержкой TSF, типы секций
- Типы секций
- Платформа текстовых служб (TSF), уведомления об изменении секций
- TSF (платформа текстовых служб), уведомления об изменении секций
- текстовые службы, уведомления об изменении секций
- Приложения с поддержкой TSF, уведомления об изменении секций
- уведомления об изменении секций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253028"
---
# <a name="compartments"></a><span data-ttu-id="e0c3a-118">Секции</span><span class="sxs-lookup"><span data-stu-id="e0c3a-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="e0c3a-119">Типы секций</span><span class="sxs-lookup"><span data-stu-id="e0c3a-119">Compartment Types</span></span>

<span data-ttu-id="e0c3a-120">Существует несколько различных типов секций.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-120">There are several different types of compartments.</span></span> <span data-ttu-id="e0c3a-121">Существует глобальная секция, и каждый диспетчер потоков, диспетчер документов и контекст могут содержать секцию.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="e0c3a-122">Глобальная секция позволяет клиентам обмениваться данными между процессами.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="e0c3a-123">Чтобы получить глобальный Диспетчер секций, вызовите [**ITfThreadMgr:: жетглобалкомпартмент**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span><span class="sxs-lookup"><span data-stu-id="e0c3a-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="e0c3a-124">Диспетчер потоков содержит Диспетчер секций, который содержит секции для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="e0c3a-125">Это позволяет совместно использовать данные в потоке.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="e0c3a-126">Чтобы получить Диспетчер секций диспетчера потоков, вызовите **ITfThreadMgr:: QueryInterface** с IID \_ итфкомпартментмгр.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="e0c3a-127">Каждый созданный диспетчер документов также содержит Диспетчер секций.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="e0c3a-128">Это позволяет предоставлять общий доступ к данным в определенном диспетчере документов.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="e0c3a-129">Чтобы получить Диспетчер секций диспетчера документов, вызовите **ITfDocumentMgr:: QueryInterface** с IID \_ итфкомпартментмгр.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="e0c3a-130">Каждый созданный контекст также содержит Диспетчер секций.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="e0c3a-131">Это позволяет совместно использовать данные в определенном контексте.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="e0c3a-132">Чтобы получить Диспетчер секций контекста, вызовите **ITfContext:: QueryInterface** с IID \_ итфкомпартментмгр.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="e0c3a-133">Создание и удаление секции</span><span class="sxs-lookup"><span data-stu-id="e0c3a-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="e0c3a-134">Секция создается при первом вызове [**итфкомпартментмгр::-секции**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) с идентификатором GUID секции.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="e0c3a-135">Клиент установки должен задать начальное значение секции с помощью [**итфкомпартмент:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span><span class="sxs-lookup"><span data-stu-id="e0c3a-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="e0c3a-136">Пока значение не будет задано, значение секции будет пустым.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="e0c3a-137">В связи с этим нет способа проверить, существовала ли секция до вызова методаического **отделения** .</span><span class="sxs-lookup"><span data-stu-id="e0c3a-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="e0c3a-138">Чтобы избежать такой ситуации, при установке клиента следует задать некоторое начальное значение, чтобы другие клиенты могли определить, существует ли уже секция.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="e0c3a-139">Метод [**итфкомпартментмгр:: клеаркомпартмент**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) используется для удаления секции.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="e0c3a-140">Все существующие ссылки на секцию помечаются как недопустимые.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="e0c3a-141">Получение секций</span><span class="sxs-lookup"><span data-stu-id="e0c3a-141">Obtaining Compartments</span></span>

<span data-ttu-id="e0c3a-142">С помощью интерфейса [**итфкомпартментмгр**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) клиент может перечислить секции, вызвав [**Итфкомпартментмгр:: енумкомпартментс**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span><span class="sxs-lookup"><span data-stu-id="e0c3a-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="e0c3a-143">Этот метод предоставляет объект **иенумгуид** , содержащий идентификаторы GUID всех установленных секций.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="e0c3a-144">С помощью GUID секции **итфкомпартментмгр::-Секция** используется для получения определенной секции.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="e0c3a-145">Этот метод предоставляет вызывающему объекту объект [**итфкомпартмент**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) , который может получать и задавать данные секции.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="e0c3a-146">Получение уведомлений об изменениях секций</span><span class="sxs-lookup"><span data-stu-id="e0c3a-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="e0c3a-147">При изменении значения секции диспетчер TSF уведомляет все установленные приемники уведомлений о том, что Секция изменилась.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="e0c3a-148">Чтобы установить приемник рекомендаций для изменения секции, создайте объект, реализующий [**итфкомпартментевентсинк**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span><span class="sxs-lookup"><span data-stu-id="e0c3a-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="e0c3a-149">Затем вызовите **итфкомпартмент:: QueryInterface** с IID \_ итфсаурце в объекте секции для отслеживания, чтобы получить интерфейс [**итфсаурце**](/windows/desktop/api/Msctf/nn-msctf-itfsource) .</span><span class="sxs-lookup"><span data-stu-id="e0c3a-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="e0c3a-150">Теперь вызовите [**итфсаурце:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) с IID \_ итфкомпартментевентсинк и указателем на объект **итфкомпартментевентсинк** .</span><span class="sxs-lookup"><span data-stu-id="e0c3a-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="e0c3a-151">При изменении значения секции [**итфкомпартментевентсинк:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) приемника уведомлений вызывается с идентификатором GUID секции.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="e0c3a-152">Приемник уведомлений может вызвать метод [**итфкомпартмент:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) , чтобы получить новое значение.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c3a-153">См. также</span><span class="sxs-lookup"><span data-stu-id="e0c3a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c3a-154">**итфкомпартментмгр**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="e0c3a-155">**итфкомпартмент**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="e0c3a-156">**итфкомпартментевентсинк**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="e0c3a-157">**тфклиентид**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="e0c3a-158">**ITfThreadMgr:: Жетглобалкомпартмент**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="e0c3a-159">**Итфкомпартментмгр:: "Секция"**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="e0c3a-160">**Итфкомпартмент:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="e0c3a-161">**Итфкомпартментмгр:: Клеаркомпартмент**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="e0c3a-162">**Итфкомпартментмгр:: Енумкомпартментс**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="e0c3a-163">**итфсаурце**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="e0c3a-164">**Итфсаурце:: AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="e0c3a-165">**Итфкомпартментевентсинк:: OnChange**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




