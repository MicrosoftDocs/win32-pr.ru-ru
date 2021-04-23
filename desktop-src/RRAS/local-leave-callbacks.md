---
title: Обратные вызовы локального выхода
description: Когда диспетчер групп многоадресной рассылки получает сообщение IGMP о том, что для группы в интерфейсе нет получателей, Диспетчер групп многоадресной рассылки вызывает \_ \_ обратный вызов обратного вызова пмгм локального выхода \_ на протокол маршрутизации в этом интерфейсе, если он существует. Этот обратный вызов уведомляет протокол маршрутизации изменения.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068188"
---
# <a name="local-leave-callbacks"></a><span data-ttu-id="a8362-104">Обратные вызовы локального выхода</span><span class="sxs-lookup"><span data-stu-id="a8362-104">Local Leave Callbacks</span></span>

<span data-ttu-id="a8362-105">Когда диспетчер групп многоадресной рассылки получает сообщение IGMP о том, что для группы в интерфейсе нет получателей, Диспетчер групп многоадресной рассылки вызывает обратный вызов [**\_ \_ \_ обратного вызова пмгм локального выхода**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) на протокол маршрутизации в этом интерфейсе, если он существует.</span><span class="sxs-lookup"><span data-stu-id="a8362-105">After the multicast group manager is notified by IGMP that there are no more receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback to the routing protocol on that interface if one exists.</span></span> <span data-ttu-id="a8362-106">Этот обратный вызов уведомляет протокол маршрутизации изменения.</span><span class="sxs-lookup"><span data-stu-id="a8362-106">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="a8362-107">Этот обратный вызов и обратный вызов [**\_ \_ \_ обратного вызова пмгм локального Join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) используются для синхронизации перенаправления между протоколами IGMP и маршрутизацией.</span><span class="sxs-lookup"><span data-stu-id="a8362-107">This callback and the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




