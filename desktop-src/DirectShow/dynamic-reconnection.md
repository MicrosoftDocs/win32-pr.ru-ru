---
description: Динамическое повторное подключение
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Динамическое повторное подключение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495141"
---
# <a name="dynamic-reconnection"></a><span data-ttu-id="a332c-103">Динамическое повторное подключение</span><span class="sxs-lookup"><span data-stu-id="a332c-103">Dynamic Reconnection</span></span>

<span data-ttu-id="a332c-104">В большинстве фильтров DirectShow ПИН-коды не могут быть повторно подключены, пока граф активно потоковая передача данных.</span><span class="sxs-lookup"><span data-stu-id="a332c-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="a332c-105">Приложение должно прерывать граф перед повторной подсоединением ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="a332c-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="a332c-106">Однако некоторые фильтры поддерживают повторное подключение ПИН-кода во время работы графа, процесс, называемый динамическим повторным подключением.</span><span class="sxs-lookup"><span data-stu-id="a332c-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="a332c-107">Это можно сделать либо с помощью приложения, либо с помощью фильтра в графе.</span><span class="sxs-lookup"><span data-stu-id="a332c-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="a332c-108">В качестве примера рассмотрим диаграмму, показанную на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="a332c-108">As an example, consider the graph in the following illustration.</span></span>

![Схема создания динамических диаграмм](images/dyngraph.png)

<span data-ttu-id="a332c-110">Одним из сценариев динамического повторного подключения может быть удаление фильтра 2 из диаграммы, во время работы графа и замена его другим фильтром.</span><span class="sxs-lookup"><span data-stu-id="a332c-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="a332c-111">Для работы этого сценария должны выполняться следующие условия.</span><span class="sxs-lookup"><span data-stu-id="a332c-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="a332c-112">Входной ПИН-код фильтра 3 (ПИН-код D) должен поддерживать интерфейс [**ипинконнектион**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="a332c-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="a332c-113">Этот интерфейс позволяет повторно подключить ПИН-код без остановки фильтра.</span><span class="sxs-lookup"><span data-stu-id="a332c-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="a332c-114">Закрепление вывода на фильтре 1 (ПИН-код A) должно иметь возможность блокировать поток данных мультимедиа во время повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="a332c-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="a332c-115">Никакие данные не перемещаются между закреплением A и ПИН-кодом D во время повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="a332c-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="a332c-116">Как правило, это означает, что выходной ПИН-код должен поддерживать интерфейс [**ипинфловконтрол**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) .</span><span class="sxs-lookup"><span data-stu-id="a332c-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="a332c-117">Однако если фильтр 1 является фильтром, который инициирует повторное подключение, он может иметь некоторый внутренний механизм для блокировки собственного потока данных.</span><span class="sxs-lookup"><span data-stu-id="a332c-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="a332c-118">Динамическое повторное подключение будет состоять из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="a332c-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="a332c-119">Блокировка потока данных от закрепления.</span><span class="sxs-lookup"><span data-stu-id="a332c-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="a332c-120">Повторно подключите ПИН-код A к ПИН-коду D, возможно, через новый промежуточный фильтр.</span><span class="sxs-lookup"><span data-stu-id="a332c-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="a332c-121">Разблокируйте ПИН-код A, чтобы начать потоковую передачу данных.</span><span class="sxs-lookup"><span data-stu-id="a332c-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="a332c-122">**Шаг 1. Блокировка потока данных**</span><span class="sxs-lookup"><span data-stu-id="a332c-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="a332c-123">Чтобы заблокировать поток данных, вызовите [**ипинфловконтрол:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) при закреплении A. Этот метод может вызываться либо асинхронно, либо синхронно.</span><span class="sxs-lookup"><span data-stu-id="a332c-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="a332c-124">Для *асинхронного* вызова метода создайте объект события Win32 и передайте его в метод **Block** .</span><span class="sxs-lookup"><span data-stu-id="a332c-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="a332c-125">Метод будет возвращаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="a332c-125">The method will return immediately.</span></span> <span data-ttu-id="a332c-126">Дождитесь получения сигнала о событии, используя функцию, такую как **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="a332c-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="a332c-127">ПИН-код сигнализирует о событии, когда оно заблокировало поток данных.</span><span class="sxs-lookup"><span data-stu-id="a332c-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="a332c-128">Пример:</span><span class="sxs-lookup"><span data-stu-id="a332c-128">For example:</span></span>


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



<span data-ttu-id="a332c-129">Для *синхронного* вызова метода просто передайте значение **null** вместо обработчика события.</span><span class="sxs-lookup"><span data-stu-id="a332c-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="a332c-130">Теперь метод будет блокироваться до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a332c-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="a332c-131">Это может произойти, пока ПИН-код не будет готов к доставке нового примера.</span><span class="sxs-lookup"><span data-stu-id="a332c-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="a332c-132">Если фильтр приостановлен, это может занять произвольный промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="a332c-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="a332c-133">Поэтому не следует выполнять синхронный вызов из основного потока приложения.</span><span class="sxs-lookup"><span data-stu-id="a332c-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="a332c-134">Используйте Рабочий поток или иначе вызовите метод асинхронно.</span><span class="sxs-lookup"><span data-stu-id="a332c-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="a332c-135">**Шаг 2. Повторное подключение ПИН-кодов**</span><span class="sxs-lookup"><span data-stu-id="a332c-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="a332c-136">Чтобы повторно подключить ПИН-коды, выполните запрос к диспетчеру графа фильтров для интерфейса **играфконфиг** и вызовите либо [**играфконфиг:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) , либо [**играфконфиг:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span><span class="sxs-lookup"><span data-stu-id="a332c-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="a332c-137">Метод **Reconnect** проще использовать; Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a332c-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="a332c-138">Останавливает промежуточные фильтры (фильтр 2 в примере) и удаляет их из диаграммы.</span><span class="sxs-lookup"><span data-stu-id="a332c-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="a332c-139">При необходимости добавляет новые промежуточные фильтры.</span><span class="sxs-lookup"><span data-stu-id="a332c-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="a332c-140">Подключает все контакты.</span><span class="sxs-lookup"><span data-stu-id="a332c-140">Connects all the pins.</span></span>
-   <span data-ttu-id="a332c-141">Приостанавливает или запускает новые фильтры для сопоставления с состоянием графа.</span><span class="sxs-lookup"><span data-stu-id="a332c-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="a332c-142">Метод **Reconnect** имеет несколько необязательных параметров, которые можно использовать для указания типа носителя для соединения с ПИН-кодом и промежуточного фильтра для использования.</span><span class="sxs-lookup"><span data-stu-id="a332c-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="a332c-143">Пример:</span><span class="sxs-lookup"><span data-stu-id="a332c-143">For example:</span></span>


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



<span data-ttu-id="a332c-144">Дополнительные сведения см. на странице справки.</span><span class="sxs-lookup"><span data-stu-id="a332c-144">For details, consult the reference page.</span></span> <span data-ttu-id="a332c-145">Если метод **Reconnect** недостаточно гибок, можно использовать метод **Reconnect** , который вызывает определенный приложением метод обратного вызова для повторного подключения ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="a332c-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="a332c-146">Чтобы использовать этот метод, реализуйте интерфейс [**играфконфигкаллбакк**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) в приложении.</span><span class="sxs-lookup"><span data-stu-id="a332c-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="a332c-147">Перед вызовом функции **перенастройки** заблокируйте поток данных из выходного ПИН-кода, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="a332c-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="a332c-148">Затем отправьте все данные, которые все еще ожидают, в разделе графа, к которому выполняется повторное подключение, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a332c-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="a332c-149">Вызовите [**ипинконнектион:: нотифендофстреам**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) для входного ПИН-кода, расположенного в самом низком направлении в цепочке повторного подключения (в примере это ПИН-код D).</span><span class="sxs-lookup"><span data-stu-id="a332c-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="a332c-150">Передайте маркер в событие Win32.</span><span class="sxs-lookup"><span data-stu-id="a332c-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="a332c-151">Вызовите [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для входного ПИН-кода, который непосредственно находится за выходным закреплением, в котором поток данных заблокирован.</span><span class="sxs-lookup"><span data-stu-id="a332c-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="a332c-152">(В этом примере поток данных был заблокирован на закрепление A, поэтому вы бы вызывали **EndOfStream** для контакта B.)</span><span class="sxs-lookup"><span data-stu-id="a332c-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="a332c-153">Дождитесь получения сигнала о событии.</span><span class="sxs-lookup"><span data-stu-id="a332c-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="a332c-154">Входной ПИН-код (ПИН-код D) сигнализирует о событии при получении уведомления о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="a332c-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="a332c-155">Это означает, что данные не передаются между контактами и что вызывающий объект может безопасно повторно подключить ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="a332c-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="a332c-156">Обратите внимание, что метод **играфконфиг:: Reconnect** автоматически обрабатывает предыдущие шаги.</span><span class="sxs-lookup"><span data-stu-id="a332c-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="a332c-157">Эти действия необходимо выполнить только при использовании метода **RECONFIGURE** .</span><span class="sxs-lookup"><span data-stu-id="a332c-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="a332c-158">После передачи данных через граф вызовите метод **RECONFIGURE** и передайте указатель на интерфейс обратного вызова **играфконфигкаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="a332c-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="a332c-159">Диспетчер графов фильтров будет вызывать указанный метод [**играфконфигкаллбакк:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) .</span><span class="sxs-lookup"><span data-stu-id="a332c-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="a332c-160">**Шаг 3. Разблокирование потока данных**</span><span class="sxs-lookup"><span data-stu-id="a332c-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="a332c-161">После повторного подключения ПИН-кода Разблокируйте поток данных, вызвав **ипинфловконтрол:: Block** со значением, равным нулю, для первого параметра.</span><span class="sxs-lookup"><span data-stu-id="a332c-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="a332c-162">Если динамическое повторное подключение выполняется фильтром, необходимо знать о некоторых проблемах с потоками.</span><span class="sxs-lookup"><span data-stu-id="a332c-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="a332c-163">Если диспетчер графов фильтров пытается отключить фильтр, это может привести к взаимоблокировке, так как граф ожидает завершения фильтра, в то время как фильтр может ожидать передачи данных через граф.</span><span class="sxs-lookup"><span data-stu-id="a332c-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="a332c-164">Чтобы предотвратить возможную взаимоблокировку, некоторые методы, описанные в этом разделе, принимают в качестве маркера событие Win32.</span><span class="sxs-lookup"><span data-stu-id="a332c-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="a332c-165">Фильтр должен сообщить о событии, если диспетчер графов фильтров пытается отключить фильтр.</span><span class="sxs-lookup"><span data-stu-id="a332c-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="a332c-166">Дополнительные сведения см. в разделе [**играфконфиг**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) и [**ипинконнектион**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span><span class="sxs-lookup"><span data-stu-id="a332c-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a332c-167">См. также</span><span class="sxs-lookup"><span data-stu-id="a332c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a332c-168">Построение динамического графа</span><span class="sxs-lookup"><span data-stu-id="a332c-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



