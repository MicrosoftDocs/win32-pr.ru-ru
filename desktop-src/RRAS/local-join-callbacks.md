---
title: Обратные вызовы локального объединения
description: Когда диспетчер групп многоадресной рассылки получает уведомления IGMP о наличии новых получателей для группы в интерфейсе, Диспетчер групп многоадресной рассылки вызывает \_ обратный вызов пмгм локального \_ Присоединение \_ к протоколу маршрутизации, владеющему интерфейсом, если он существует.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486937"
---
# <a name="local-join-callbacks"></a><span data-ttu-id="79b40-103">Обратные вызовы локального объединения</span><span class="sxs-lookup"><span data-stu-id="79b40-103">Local Join Callbacks</span></span>

<span data-ttu-id="79b40-104">Когда диспетчер групп многоадресной рассылки получает уведомления IGMP о наличии новых получателей для группы в интерфейсе, Диспетчер групп многоадресной рассылки вызывает обратный вызов [**пмгм \_ локального \_ Присоединение \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) к протоколу маршрутизации, владеющему интерфейсом, если он существует.</span><span class="sxs-lookup"><span data-stu-id="79b40-104">After the multicast group manager is notified by IGMP that new receivers are present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback to the routing protocol that owns the interface if one exists.</span></span> <span data-ttu-id="79b40-105">Этот обратный вызов уведомляет протокол маршрутизации изменения.</span><span class="sxs-lookup"><span data-stu-id="79b40-105">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="79b40-106">Этот обратный вызов и обратный вызов [**\_ \_ \_ обратного вызова пмгм локального выхода**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) используются для синхронизации перенаправления между протоколами IGMP и маршрутизацией.</span><span class="sxs-lookup"><span data-stu-id="79b40-106">This callback and the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




