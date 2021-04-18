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
# <a name="client-side-errors"></a>Ошибки Client-Side

Ошибки на стороне клиента обрабатываются способом, аналогичным сбоям на стороне сервера. [Очередь сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) может переместить сообщение в очередь назначения, если, например, сообщение не может быть перемещено с клиента на сервер. В этом случае сообщение перемещается в очередь недоставленных сообщений на стороне клиента.

Служба COM+ очереди компонентов наблюдает за очередью недоставленных сообщений. Если сообщения были перемещены, служба очередей компонентов создает экземпляр класса Exception и вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для запроса [**иплайбаккконтрол**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). В случае успеха монитор очереди недоставленных сообщений вызывает [**иплайбаккконтрол:: финалклиентретри**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

Объект может выполнить какое-либо действие, чтобы отменить результат предыдущей транзакции. Если воспроизведение завершается, сообщение удаляется из очереди недоставленных сообщений о транзакции. Если воспроизведение завершается ошибкой или требуемый CLSID и интерфейс недоступны, сообщение остается в очереди недоставленных сообщений активной транзакции.

Если необходимо выполнить описанный выше процесс или переместить опасное сообщение из конечной очереди RESTful, используйте программу перемещения сообщений. Дополнительные сведения о программе перемещения сообщений см. в разделе [Обработка ошибок](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Постоянные сбои Client-Side](persistent-client-side-failures.md)
</dt> <dt>

[Ошибки на стороне сервера](server-side-errors.md)
</dt> </dl>

 

 
