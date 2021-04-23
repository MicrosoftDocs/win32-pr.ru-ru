---
description: Указывает дескриптор очереди завершения, используемый для уведомлений о завершении ввода-вывода с помощью запросов send и Receive с зарегистрированными расширениями ввода-вывода Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702093"
---
# <a name="rio_cq"></a><span data-ttu-id="8147c-103">Рио \_ КК</span><span class="sxs-lookup"><span data-stu-id="8147c-103">RIO\_CQ</span></span>

<span data-ttu-id="8147c-104">**Рио \_ КК** typedef указывает дескриптор очереди завершения, используемый для уведомлений о завершении ввода-вывода с помощью запросов send и Receive с зарегистрированными расширениями ввода-вывода Winsock.</span><span class="sxs-lookup"><span data-stu-id="8147c-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="8147c-105">**Рио \_ КК**</span><span class="sxs-lookup"><span data-stu-id="8147c-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="8147c-106">Тип данных, указывающий дескриптор очереди завершения, используемый для уведомлений о завершении ввода-вывода по запросам Send и Receive.</span><span class="sxs-lookup"><span data-stu-id="8147c-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8147c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8147c-107">Remarks</span></span>

<span data-ttu-id="8147c-108">Объект **Рио \_ КК** используется для уведомления о завершении ввода-вывода запросов send и Receive по сетевым запросам, зарегистрированным расширениями ввода-вывода Winsock.</span><span class="sxs-lookup"><span data-stu-id="8147c-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="8147c-109">Приложение может использовать функцию [**рионотифи**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) для запроса уведомления, если очередь завершения **Рио \_ КК** не пуста.</span><span class="sxs-lookup"><span data-stu-id="8147c-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="8147c-110">Приложение также может опрашивать состояние в любое время в очереди завершения **Рио \_ КК** без блокировки с помощью функции [**риодекуеуекомплетион**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="8147c-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="8147c-111">Объект **\_ КК Рио** создается с помощью функции [**риокреатекомплетионкуеуе**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="8147c-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="8147c-112">Во время создания приложение должно указать размер очереди, который определяет количество записей завершения, которое он может содержать.</span><span class="sxs-lookup"><span data-stu-id="8147c-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="8147c-113">Когда приложение вызывает функцию [**риокреатерекуесткуеуе**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) для получения маркера [**\_ РК Рио**](riorqueue.md) , приложение должно указать **Рио \_ КК** для отправки завершений и Рио **\_ КК** для получения завершений.</span><span class="sxs-lookup"><span data-stu-id="8147c-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="8147c-114">Эти дескрипторы могут быть идентичны, если одна и та же очередь должна использоваться для завершения отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="8147c-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="8147c-115">Функция **риокреатерекуесткуеуе** также требует максимального количества ожидающих операций отправки и получения, которые начисляются по емкости связанной очереди завершения или очередей.</span><span class="sxs-lookup"><span data-stu-id="8147c-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="8147c-116">Если в очередях недостаточно емкости, вызов **риокреатерекуесткуеуе** завершится с ошибкой [всаенобуфс](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="8147c-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="8147c-117">Поведение уведомлений для очереди завершения задается при создании **\_ КК Рио** .</span><span class="sxs-lookup"><span data-stu-id="8147c-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="8147c-118">Для очереди завершения, в которой используется событие, элементу **Type** структуры [**\_ \_ завершения уведомлений Рио**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) присваивается значение Рио для **\_ \_ завершения события**.</span><span class="sxs-lookup"><span data-stu-id="8147c-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="8147c-119">Элемент **Event. евенсандле** должен содержать маркер события, созданного функцией [**всакреативент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) или [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .</span><span class="sxs-lookup"><span data-stu-id="8147c-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="8147c-120">Чтобы получить завершение [**рионотифи**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , приложение должно ожидать указанного обработчика событий с помощью [**всаваитформултипливентс**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) или аналогичной процедуры Wait.</span><span class="sxs-lookup"><span data-stu-id="8147c-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="8147c-121">Если приложение планирует сбросить и повторно использовать событие, оно может снизить нагрузку, установив для элемента **Event. нотифиресет** ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8147c-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="8147c-122">Это приводит к тому, что событие автоматически сбрасывается функцией **рионотифи** при возникновении уведомления.</span><span class="sxs-lookup"><span data-stu-id="8147c-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="8147c-123">Это снижает потребность в вызове функции [**всаресетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) для сброса события между вызовами функции **рионотифи** .</span><span class="sxs-lookup"><span data-stu-id="8147c-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="8147c-124">Для очереди завершения, в которой используется порт завершения ввода-вывода, элементу **Type** структуры [**\_ \_ завершения уведомлений Рио**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) присваивается значение **Рио \_ IOCP \_ завершения**.</span><span class="sxs-lookup"><span data-stu-id="8147c-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="8147c-125">Элемент **IOCP. иокфандле** должен содержать маркер для порта завершения ввода-вывода, созданного функцией [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) .</span><span class="sxs-lookup"><span data-stu-id="8147c-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="8147c-126">Чтобы получить завершение [**рионотифи**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , приложение должно вызвать функцию [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) или [**жеткуеуедкомплетионстатусекс**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) .</span><span class="sxs-lookup"><span data-stu-id="8147c-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="8147c-127">Приложение должно предоставить выделенный объект [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) для очереди завершения, а также элемент **IOCP. комплетионкэй** , чтобы отличать запросы **рионотифи** к очереди завершения от других завершений ввода-вывода, включая **рионотифи** завершения для других очередей завершения.</span><span class="sxs-lookup"><span data-stu-id="8147c-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="8147c-128">В целях повышения эффективности доступ к очередям завершения (структурам **Рио \_ КК** ) и очередям запросов ([**Рио \_ РК**](riorqueue.md) структуры) не защищается примитивами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8147c-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="8147c-129">Если необходимо получить доступ к очереди завершения или запросов из нескольких потоков, доступ должен координироваться критическим разделом, упрощенной блокировкой записи чтения или аналогичным механизмом.</span><span class="sxs-lookup"><span data-stu-id="8147c-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="8147c-130">Эта блокировка не требуется для доступа в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="8147c-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="8147c-131">Различные потоки могут обращаться к отдельным запросам или очередям завершения без блокировок.</span><span class="sxs-lookup"><span data-stu-id="8147c-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="8147c-132">Необходимость в синхронизации происходит только в том случае, если несколько потоков пытаются получить доступ к одной и той же очереди.</span><span class="sxs-lookup"><span data-stu-id="8147c-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="8147c-133">Синхронизация также необходима, если несколько потоков отправляют и получают на одном сокете, так как операции отправки и получения используют очередь запросов сокета.</span><span class="sxs-lookup"><span data-stu-id="8147c-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="8147c-134">Если несколько потоков пытаются получить доступ к одному **Рио \_ КК** с помощью [**риодекуеуекомплетион**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), доступ должен координироваться критической секцией, упрощенной блокировкой записи чтения или аналогичным механизмом взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="8147c-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="8147c-135">Если очереди завершения не являются общими, взаимное исключение не требуется.</span><span class="sxs-lookup"><span data-stu-id="8147c-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="8147c-136">Если очередь завершения больше не нужна, приложение может закрыть его с помощью функции [**риоклосекомплетионкуеуе**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8147c-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="8147c-137">**Рио \_ КК** typedef определяется в файле заголовка *мсвсоккдеф. h* , который автоматически включается в заголовочный файл *мсвсокк. h* .</span><span class="sxs-lookup"><span data-stu-id="8147c-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="8147c-138">Файл заголовка *мсвсоккдеф. h* никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="8147c-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="8147c-139">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="8147c-139">Thread Safety</span></span>

<span data-ttu-id="8147c-140">Если несколько потоков пытаются получить доступ к одному **Рио \_ КК** с помощью [**риодекуеуекомплетион**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), доступ должен координироваться критической секцией, упрощенной блокировкой записи чтения или аналогичным механизмом взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="8147c-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="8147c-141">Если очереди завершения не являются общими, взаимное исключение не требуется.</span><span class="sxs-lookup"><span data-stu-id="8147c-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="8147c-142">Требования</span><span class="sxs-lookup"><span data-stu-id="8147c-142">Requirements</span></span>



| <span data-ttu-id="8147c-143">Требование</span><span class="sxs-lookup"><span data-stu-id="8147c-143">Requirement</span></span> | <span data-ttu-id="8147c-144">Значение</span><span class="sxs-lookup"><span data-stu-id="8147c-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8147c-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8147c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8147c-146">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8147c-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="8147c-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8147c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8147c-148">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8147c-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="8147c-149">Header</span><span class="sxs-lookup"><span data-stu-id="8147c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8147c-150"><dt>Мсвсоккдеф. h (включение Мсвсокк. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8147c-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8147c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8147c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8147c-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="8147c-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="8147c-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="8147c-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="8147c-154">**жеткуеуедкомплетионстатус**</span><span class="sxs-lookup"><span data-stu-id="8147c-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="8147c-155">**жеткуеуедкомплетионстатусекс**</span><span class="sxs-lookup"><span data-stu-id="8147c-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="8147c-156">**OVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="8147c-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="8147c-157">**\_Завершение уведомлений \_ Рио**</span><span class="sxs-lookup"><span data-stu-id="8147c-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="8147c-158">**\_ \_ тип завершения уведомления \_ Рио**</span><span class="sxs-lookup"><span data-stu-id="8147c-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="8147c-159">**Рио \_ РК**</span><span class="sxs-lookup"><span data-stu-id="8147c-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="8147c-160">[**риоклосекомплетионкуеуе**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8147c-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8147c-161">**риокреатекомплетионкуеуе**</span><span class="sxs-lookup"><span data-stu-id="8147c-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="8147c-162">**риокреатерекуесткуеуе**</span><span class="sxs-lookup"><span data-stu-id="8147c-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="8147c-163">**риодекуеуекомплетион**</span><span class="sxs-lookup"><span data-stu-id="8147c-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="8147c-164">**рионотифи**</span><span class="sxs-lookup"><span data-stu-id="8147c-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="8147c-165">**всакреативент**</span><span class="sxs-lookup"><span data-stu-id="8147c-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="8147c-166">**всаресетевент**</span><span class="sxs-lookup"><span data-stu-id="8147c-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="8147c-167">**всаваитформултипливентс**</span><span class="sxs-lookup"><span data-stu-id="8147c-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
