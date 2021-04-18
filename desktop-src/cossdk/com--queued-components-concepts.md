---
description: Основные понятия COM+ в очереди компонентов
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Основные понятия COM+ в очереди компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701183"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="d3dca-103">Основные понятия COM+ в очереди компонентов</span><span class="sxs-lookup"><span data-stu-id="d3dca-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="d3dca-104">В зависимости от служб [очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) служба COM+ в очереди предоставляет простой способ асинхронного вызова и выполнения компонентов.</span><span class="sxs-lookup"><span data-stu-id="d3dca-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="d3dca-105">Обработка может выполняться без учета доступности или доступности отправителя или получателя.</span><span class="sxs-lookup"><span data-stu-id="d3dca-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="d3dca-106">В терминах COM *очередь* — это область хранения, которая сохраняет сообщения для последующего извлечения.</span><span class="sxs-lookup"><span data-stu-id="d3dca-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="d3dca-107">Служба очередей предоставляет механизм связи без подключения.</span><span class="sxs-lookup"><span data-stu-id="d3dca-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="d3dca-108">То есть отправитель и получатель не подключаются напрямую и обмениваются данными только через очереди.</span><span class="sxs-lookup"><span data-stu-id="d3dca-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="d3dca-109">Служба очереди предоставляет способ хранения информации до тех пор, пока получатель не будет готов к получению.</span><span class="sxs-lookup"><span data-stu-id="d3dca-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="d3dca-110">Отправитель и получатель косвенно взаимодействуют, чтобы каждый мог действовать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="d3dca-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="d3dca-111">В прошлом было необходимо глубокое знание упаковки для очередей, отправки и получения асинхронных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d3dca-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="d3dca-112">Теперь, используя вызовы методов, которые легко понятны и используются разработчиками компонентов, служба очередей компонентов COM+ автоматически маршалирует данные в виде сообщения очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="d3dca-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="d3dca-113">А поскольку служба очередей компонентов предлагает встроенную поддержку транзакций, непротиворечивое состояние не может нарушать данные в случае сбоя сервера.</span><span class="sxs-lookup"><span data-stu-id="d3dca-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="d3dca-114">В следующих подразделах этого раздела содержатся общие сведения о проектировании и написании очередей компонентов.</span><span class="sxs-lookup"><span data-stu-id="d3dca-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="d3dca-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="d3dca-115">Topic</span></span>                                                                           | <span data-ttu-id="d3dca-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d3dca-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3dca-117">Преимущества обработки в очереди</span><span class="sxs-lookup"><span data-stu-id="d3dca-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="d3dca-118">Описывает преимущества программирования с помощью компонентов, поставленных в очередь COM+.</span><span class="sxs-lookup"><span data-stu-id="d3dca-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="d3dca-119">Архитектура очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="d3dca-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="d3dca-120">Описывает архитектуру службы компонентов COM+ в очереди.</span><span class="sxs-lookup"><span data-stu-id="d3dca-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="d3dca-121">Транзакционная очередь сообщений</span><span class="sxs-lookup"><span data-stu-id="d3dca-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="d3dca-122">Описывает, как транзакции обрабатываются службой компонентов COM+ в очереди.</span><span class="sxs-lookup"><span data-stu-id="d3dca-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="d3dca-123">Безопасность очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="d3dca-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="d3dca-124">Описание параметров политики для проверки подлинности клиентских сообщений и их последствий.</span><span class="sxs-lookup"><span data-stu-id="d3dca-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="d3dca-125">Разработка компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="d3dca-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="d3dca-126">Описывает вопросы программирования при написании компонентов куеуабле.</span><span class="sxs-lookup"><span data-stu-id="d3dca-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="d3dca-127">Ошибки компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="d3dca-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="d3dca-128">Описание наиболее распространенных типов ошибок, которые могут возникнуть при использовании службы очередей компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="d3dca-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d3dca-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d3dca-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3dca-130">Задачи компонентов, поставленных в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="d3dca-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




