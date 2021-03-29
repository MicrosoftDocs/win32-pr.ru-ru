---
title: Получение состояния изменения и игнорирование изменений
description: Клиент может запросить диспетчер таблиц маршрутизации, чтобы выяснить, ожидает ли уведомление об изменении назначения, вызвав Ртмжетчанжестатус. Эта функция возвращает значение TRUE, пока вызывающий объект не извлечет это изменение, вызвав Ртмжетчанжеддестс.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774639"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="c537c-104">Получение состояния изменения и игнорирование изменений</span><span class="sxs-lookup"><span data-stu-id="c537c-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="c537c-105">Клиент может запросить диспетчер таблиц маршрутизации, чтобы выяснить, ожидает ли уведомление об изменении назначения, вызвав [**ртмжетчанжестатус**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span><span class="sxs-lookup"><span data-stu-id="c537c-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="c537c-106">Эта функция возвращает **значение true** , пока вызывающий объект не извлечет это изменение, вызвав [**ртмжетчанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span><span class="sxs-lookup"><span data-stu-id="c537c-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="c537c-107">Клиент может использовать этот запрос, чтобы избежать выполнения действия, которое должно быть отменено после получения и обработки уведомления об изменении.</span><span class="sxs-lookup"><span data-stu-id="c537c-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="c537c-108">Использование этой функции позволяет клиенту эффективно работать, откладывая некоторые операции на более позднее время.</span><span class="sxs-lookup"><span data-stu-id="c537c-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="c537c-109">Клиент также может игнорировать ожидающее уведомление об изменении для назначения, вызвав [**ртмигноречанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="c537c-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="c537c-110">Последующий вызов [**ртмжетчанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) не возвращает это назначение, если после вызова [**ртмигноречанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)не происходит другое изменение.</span><span class="sxs-lookup"><span data-stu-id="c537c-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




