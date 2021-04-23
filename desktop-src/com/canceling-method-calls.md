---
title: Отмена вызовов метода
description: С появлением распределенных и веб-приложений некоторые вызовы методов могут занимать неприемлемые длительное время.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105710375"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="7bef9-103">Отмена вызовов метода</span><span class="sxs-lookup"><span data-stu-id="7bef9-103">Canceling Method Calls</span></span>

<span data-ttu-id="7bef9-104">С появлением распределенных и веб-приложений некоторые вызовы методов могут занимать неприемлемые длительное время.</span><span class="sxs-lookup"><span data-stu-id="7bef9-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="7bef9-105">Задержка сетевого подключения может быть высокой, компьютер сервера может обслуживать много клиентов, или серверный компонент может передавать большой объем данных, например файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7bef9-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="7bef9-106">Пользователи должны иметь возможность отменить запрос, который занимает слишком много времени, и приложение должно иметь возможность обрабатывать запросы отмены и продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="7bef9-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="7bef9-107">В модели COM можно использовать интерфейс [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) для отмены ожидающего вызова, полученного из однопотокового подразделения.</span><span class="sxs-lookup"><span data-stu-id="7bef9-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="7bef9-108">При маршалировании вызова прокси-сервер создает объект Cancel, который реализует интерфейс [**иканцелмесодкаллс**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="7bef9-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="7bef9-109">Объект Cancel связан с вызовом и потоком, в котором ожидается вызов.</span><span class="sxs-lookup"><span data-stu-id="7bef9-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="7bef9-110">Чтобы отменить отложенный вызов, клиент передает запрос на отмену через объект Cancel, который обрабатывает сведения об уведомлении объекта сервера о том, что вызов был отменен.</span><span class="sxs-lookup"><span data-stu-id="7bef9-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="7bef9-111">Если вызванный метод не возвращает, объект сервера, при обнаружении запроса на отмену, очищает все выделенные ресурсы программы и уведомляет его клиента, возвращая соответствующее значение **HRESULT** , после чего выполнение вызова отменяется.</span><span class="sxs-lookup"><span data-stu-id="7bef9-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="7bef9-112">Если вызванный метод уже был возвращен, объект Cancel уведомляет клиента.</span><span class="sxs-lookup"><span data-stu-id="7bef9-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="7bef9-113">В любом случае клиентский поток разблокируется и может продолжать обработку.</span><span class="sxs-lookup"><span data-stu-id="7bef9-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="7bef9-114">Ответ серверного объекта на запрос отмены — это на усмотрение разработчиков сервера, но вызывающий поток на клиенте всегда будет разблокирован и будет игнорировать все результаты, которые сервер пытается передать в него.</span><span class="sxs-lookup"><span data-stu-id="7bef9-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="7bef9-115">Объекты Cancel предоставляют средства для запроса на отмену выполнения текущего метода, но нет никакой гарантии, что объект сервера прекратит обработку вызова.</span><span class="sxs-lookup"><span data-stu-id="7bef9-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="7bef9-116">Например, вызов может быть уже возвращен, или серверный объект не поддерживает отмену объектов.</span><span class="sxs-lookup"><span data-stu-id="7bef9-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="7bef9-117">COM автоматически предоставляет стандартную реализацию отмены объектов для клиентских объектов и интерфейсов, использующих стандартную упаковку.</span><span class="sxs-lookup"><span data-stu-id="7bef9-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="7bef9-118">Для объектов и интерфейсов, использующих настраиваемое маршалирование, необходимо реализовать собственный объект Cancel.</span><span class="sxs-lookup"><span data-stu-id="7bef9-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="7bef9-119">В настоящее время объекты отмены обрабатывают только синхронные вызовы.</span><span class="sxs-lookup"><span data-stu-id="7bef9-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bef9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7bef9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bef9-121">Отмена асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="7bef9-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="7bef9-122">**кожетканцелобжект**</span><span class="sxs-lookup"><span data-stu-id="7bef9-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="7bef9-123">**косетканцелобжект**</span><span class="sxs-lookup"><span data-stu-id="7bef9-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="7bef9-124">**котестканцел**</span><span class="sxs-lookup"><span data-stu-id="7bef9-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 