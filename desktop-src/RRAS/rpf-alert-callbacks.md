---
title: Обратные вызовы оповещений РПФ
description: После того как диспетчер групп многоадресной рассылки получает уведомление пакета от нового источника или пакета, предназначенного для новой группы, Диспетчер групп многоадресной рассылки находит маршрут к источнику в представлении многоадресной рассылки таблицы маршрутизации.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780201"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="6ca53-103">Обратные вызовы оповещений РПФ</span><span class="sxs-lookup"><span data-stu-id="6ca53-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="6ca53-104">После того как диспетчер групп многоадресной рассылки получает уведомление пакета от нового источника или пакета, предназначенного для новой группы, Диспетчер групп многоадресной рассылки находит маршрут к источнику в представлении многоадресной рассылки таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="6ca53-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="6ca53-105">Затем Диспетчер групп многоадресной рассылки вызывает обратный вызов [**\_ \_ обратного вызова пмгм РПФ**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) к протоколу, владеющему интерфейсом, в котором были получены данные.</span><span class="sxs-lookup"><span data-stu-id="6ca53-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="6ca53-106">После вызова этого обратного вызова протокол маршрутизации может изменить входящий интерфейс, если протокол маршрутизации должен получить данные для группы в другом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="6ca53-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




