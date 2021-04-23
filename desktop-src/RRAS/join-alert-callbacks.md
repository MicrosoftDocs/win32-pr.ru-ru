---
title: Обратные вызовы оповещений о соединении
description: Когда диспетчер групп многоадресной рассылки получает уведомление о наличии новых получателей для группы в интерфейсе, Диспетчер групп многоадресной рассылки вызывает \_ обратный вызов пмгм для \_ оповещения о соединении \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068190"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="f3aeb-103">Обратные вызовы оповещений о соединении</span><span class="sxs-lookup"><span data-stu-id="f3aeb-103">Join Alert Callbacks</span></span>

<span data-ttu-id="f3aeb-104">Когда диспетчер групп многоадресной рассылки получает уведомление о наличии новых получателей для группы в интерфейсе, Диспетчер групп многоадресной рассылки вызывает обратный вызов [**пмгм \_ для \_ оповещения \_ о соединении**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="f3aeb-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="f3aeb-105">Этот обратный вызов уведомляет протоколы маршрутизации, которые новые узлы присоединяются к указанным группам.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="f3aeb-106">Поэтому протоколы маршрутизации должны запрашивать данные многоадресной рассылки для групп, указанных в обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="f3aeb-107">Диспетчер групп многоадресной рассылки использует предопределенный набор правил, которые используются для определения того, когда вызывается этот обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="f3aeb-108">Этот набор правил основан на типе запроса на соединение, отправленном клиентом, и порядке, в котором были получены запросы на соединение.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="f3aeb-109">Запросы на соединение с подстановочными знаками</span><span class="sxs-lookup"><span data-stu-id="f3aeb-109">Wildcard Join Requests</span></span>

<span data-ttu-id="f3aeb-110">При получении подстановочного знака для группы ( \* , g) от первого клиента Диспетчер групп многоадресной рассылки вызывает обратный вызов пмгм для [**\_ \_ оповещения о \_ соединении**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) с другими зарегистрированными клиентами.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="f3aeb-111">При получении подстановочного знака для группы от второго клиента Диспетчер групп многоадресной рассылки вызывает этот обратный вызов для первого клиента, чтобы присоединиться к группе.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="f3aeb-112">Запросы на присоединение Source-Specific</span><span class="sxs-lookup"><span data-stu-id="f3aeb-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="f3aeb-113">Диспетчер групп многоадресной рассылки не вызывает этот обратный вызов для всех последующих соединений с группой.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="f3aeb-114">При получении присоединение к определенному источнику для группы (s, g) Диспетчер групп многоадресной рассылки вызывает обратный вызов [**пмгм для \_ \_ оповещения о \_ соединении**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) , только для клиента, владеющего входящим интерфейсом к источнику s.</span><span class="sxs-lookup"><span data-stu-id="f3aeb-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




