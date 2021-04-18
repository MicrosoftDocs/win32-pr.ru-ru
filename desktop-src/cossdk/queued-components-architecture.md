---
description: Служба COM+ в очереди компонентов расширяет модель программирования COM, предоставляя среду, в которой компонент может быть вызван синхронно (в режиме реального времени) или асинхронно (в очереди).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Архитектура очередей компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565344"
---
# <a name="queued-components-architecture"></a><span data-ttu-id="c4705-103">Архитектура очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="c4705-103">Queued Components Architecture</span></span>

<span data-ttu-id="c4705-104">Служба COM+ в очереди компонентов расширяет модель программирования COM, предоставляя среду, в которой компонент может быть вызван синхронно (в режиме реального времени) или асинхронно (в очереди).</span><span class="sxs-lookup"><span data-stu-id="c4705-104">The COM+ queued components service enhances the COM programming model by providing an environment in which a component can be invoked either synchronously (real-time) or asynchronously (queued).</span></span> <span data-ttu-id="c4705-105">Компоненту не нужно знать, используется ли он в режиме реального времени или в очереди.</span><span class="sxs-lookup"><span data-stu-id="c4705-105">A component need not be aware of whether it is employed in a real-time or a queued context.</span></span>

<span data-ttu-id="c4705-106">Приложения обмена сообщениями подобны транзакциям электронной почты между программами.</span><span class="sxs-lookup"><span data-stu-id="c4705-106">Messaging applications are like email transactions between programs.</span></span> <span data-ttu-id="c4705-107">Инициатор запроса отправляет сообщение на сервер; Когда сервер получает к нему, сообщение обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="c4705-107">The requester sends a message to the server; when the server gets to it, the message is processed.</span></span> <span data-ttu-id="c4705-108">Как и электронная почта, система обмена сообщениями должна выполнить обработку сведений о сети и убедиться, что сообщение перемещается с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="c4705-108">Like email, a messaging system must handle the network details and ensure that the message moves from the client to the server.</span></span> <span data-ttu-id="c4705-109">В инфраструктуре компонентов с очередями за это отвечает Служба очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="c4705-109">In the queued components framework, Message Queuing is responsible for this.</span></span>

<span data-ttu-id="c4705-110">Служба COM+ «очереди компонентов» состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="c4705-110">The COM+ queued components service consists of the following parts:</span></span>

-   <span data-ttu-id="c4705-111">Средство записи (для клиента или на стороне отправки)</span><span class="sxs-lookup"><span data-stu-id="c4705-111">Recorder (for the client or send side)</span></span>
-   <span data-ttu-id="c4705-112">Прослушиватель (для сервера или принимающей стороны)</span><span class="sxs-lookup"><span data-stu-id="c4705-112">Listener (for the server or receive side)</span></span>
-   <span data-ttu-id="c4705-113">Проигрыватель (для сервера или принимающей стороны)</span><span class="sxs-lookup"><span data-stu-id="c4705-113">Player (for the server or receive side)</span></span>

![Схема, показывающая путь от клиента к серверу: Клиент, устройство записи, очередь, прослушиватель, проигрыватель, сервер.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a><span data-ttu-id="c4705-115">Средство записи</span><span class="sxs-lookup"><span data-stu-id="c4705-115">The Recorder</span></span>

<span data-ttu-id="c4705-116">В типичном сценарии с очередями компонентов клиент вызывает компонент в очереди.</span><span class="sxs-lookup"><span data-stu-id="c4705-116">In a typical queued components scenario, the client calls a queued component.</span></span> <span data-ttu-id="c4705-117">Выполняется вызов средства записи очередей компонентов, которое упаковывает его как часть сообщения на сервер и помещает в очередь.</span><span class="sxs-lookup"><span data-stu-id="c4705-117">The call is made to the queued components recorder, which packages it as part of a message to the server and puts it in a queue.</span></span> <span data-ttu-id="c4705-118">Средство записи маршалирует в сообщение контекст безопасности клиента и записывает все вызовы метода клиента.</span><span class="sxs-lookup"><span data-stu-id="c4705-118">The recorder marshals the client's security context into the message and records all of the client's method calls.</span></span> <span data-ttu-id="c4705-119">В роли прокси-сервера для серверного компонента средство записи выбирает интерфейсы из интерфейсов куеуабле в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="c4705-119">In its role as proxy for the server component, the recorder selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

<span data-ttu-id="c4705-120">Представление записи отправляется в очередь сообщений в виде сообщения, отправляемого на сервер.</span><span class="sxs-lookup"><span data-stu-id="c4705-120">A representation of the recording is sent to Message Queuing as a message to be sent to a server.</span></span> <span data-ttu-id="c4705-121">Если для компонента в очереди задан атрибут транзакции Required или Supported, очередь сообщений принимает сообщение только в том случае, если транзакция на стороне клиента фиксируется и очередь очереди сообщений является транзакционной, то есть обычно установленной по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c4705-121">When the queued component has the transaction attribute setting of Required or Supported, Message Queuing accepts delivery of the message only if the client-side transaction commits and the Message Queuing queue is transactional, which is the default normally established.</span></span> <span data-ttu-id="c4705-122">Если для параметра атрибута транзакции требуется New, очередь сообщений может принять сообщение, даже если транзакция на стороне клиента прерывается.</span><span class="sxs-lookup"><span data-stu-id="c4705-122">When the transaction attribute setting is Requires New, Message Queuing can accept the message even if the client-side transaction aborts.</span></span> <span data-ttu-id="c4705-123">Дополнительные сведения о транзакциях см. в разделе [транзакционная очередь сообщений](transactional-message-queuing.md).</span><span class="sxs-lookup"><span data-stu-id="c4705-123">For more information on transactions, see [Transactional Message Queuing](transactional-message-queuing.md).</span></span>

## <a name="the-listener"></a><span data-ttu-id="c4705-124">Прослушиватель</span><span class="sxs-lookup"><span data-stu-id="c4705-124">The Listener</span></span>

<span data-ttu-id="c4705-125">Прослушиватель очередей компонентов извлекает сообщение из очереди и передает его в проигрыватель очередей компонентов.</span><span class="sxs-lookup"><span data-stu-id="c4705-125">The queued components listener retrieves the message from the queue and passes it to the queued components player.</span></span>

## <a name="the-player"></a><span data-ttu-id="c4705-126">Проигрыватель</span><span class="sxs-lookup"><span data-stu-id="c4705-126">The Player</span></span>

<span data-ttu-id="c4705-127">Проигрыватель отменяет упаковку контекста безопасности клиента на стороне сервера, а затем вызывает серверный компонент и выполняет те же вызовы метода.</span><span class="sxs-lookup"><span data-stu-id="c4705-127">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="c4705-128">Вызовы методов воспроизводятся проигрывателем до тех пор, пока не завершится клиентский компонент и транзакция, которая записала вызовы метода, фиксируется.</span><span class="sxs-lookup"><span data-stu-id="c4705-128">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

## <a name="the-message-mover"></a><span data-ttu-id="c4705-129">Перемещение сообщений</span><span class="sxs-lookup"><span data-stu-id="c4705-129">The Message Mover</span></span>

<span data-ttu-id="c4705-130">Средство перемещения сообщений о компонентах в очереди — это служебная программа, которая перемещает все сообщения об ошибках очереди сообщений из одной очереди в другую, чтобы их можно было повторить.</span><span class="sxs-lookup"><span data-stu-id="c4705-130">The queued components message mover is a utility that moves all failed Message Queuing messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="c4705-131">Служебная программа перемещения сообщений — это объект автоматизации, который можно вызывать с помощью VBScript; Дополнительные сведения см. в разделе [Обработка ошибок](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="c4705-131">The message mover utility is an Automation object that can be invoked with a VBScript; for more information, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

 

 



