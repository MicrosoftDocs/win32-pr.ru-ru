---
description: Ошибки Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Ошибки Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701185"
---
# <a name="client-side-errors"></a><span data-ttu-id="4d9bc-103">Ошибки Client-Side</span><span class="sxs-lookup"><span data-stu-id="4d9bc-103">Client-Side Errors</span></span>

<span data-ttu-id="4d9bc-104">Ошибки на стороне клиента обрабатываются способом, аналогичным сбоям на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="4d9bc-105">[Очередь сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) может переместить сообщение в очередь назначения, если, например, сообщение не может быть перемещено с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="4d9bc-106">В этом случае сообщение перемещается в очередь недоставленных сообщений на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="4d9bc-107">Служба COM+ очереди компонентов наблюдает за очередью недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="4d9bc-108">Если сообщения были перемещены, служба очередей компонентов создает экземпляр класса Exception и вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для запроса [**иплайбаккконтрол**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span><span class="sxs-lookup"><span data-stu-id="4d9bc-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="4d9bc-109">В случае успеха монитор очереди недоставленных сообщений вызывает [**иплайбаккконтрол:: финалклиентретри**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span><span class="sxs-lookup"><span data-stu-id="4d9bc-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="4d9bc-110">Объект может выполнить какое-либо действие, чтобы отменить результат предыдущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="4d9bc-111">Если воспроизведение завершается, сообщение удаляется из очереди недоставленных сообщений о транзакции.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="4d9bc-112">Если воспроизведение завершается ошибкой или требуемый CLSID и интерфейс недоступны, сообщение остается в очереди недоставленных сообщений активной транзакции.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="4d9bc-113">Если необходимо выполнить описанный выше процесс или переместить опасное сообщение из конечной очереди RESTful, используйте программу перемещения сообщений.</span><span class="sxs-lookup"><span data-stu-id="4d9bc-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="4d9bc-114">Дополнительные сведения о программе перемещения сообщений см. в разделе [Обработка ошибок](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="4d9bc-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d9bc-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4d9bc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d9bc-116">Постоянные сбои Client-Side</span><span class="sxs-lookup"><span data-stu-id="4d9bc-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="4d9bc-117">Ошибки на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="4d9bc-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
