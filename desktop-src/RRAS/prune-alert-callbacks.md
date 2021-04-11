---
title: Удалять обратные вызовы оповещений
description: Когда диспетчер групп многоадресной рассылки получает уведомление о том, что получатели покидает группу в интерфейсе, Диспетчер групп многоадресной рассылки вызывает обратный вызов ПМГМ для \_ \_ оповещения об очистке \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068508"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="94767-103">Удалять обратные вызовы оповещений</span><span class="sxs-lookup"><span data-stu-id="94767-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="94767-104">Когда диспетчер групп многоадресной рассылки получает уведомление о том, что получатели покидает группу в интерфейсе, Диспетчер групп многоадресной рассылки вызывает обратный вызов [**пмгм для \_ \_ оповещения об \_ очистке**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="94767-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="94767-105">Этот обратный вызов уведомляет о протоколах маршрутизации, которые клиенты больше не входят в указанную группу.</span><span class="sxs-lookup"><span data-stu-id="94767-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="94767-106">Поэтому протоколы маршрутизации должны прерывать запрос данных многоадресной рассылки для указанных групп.</span><span class="sxs-lookup"><span data-stu-id="94767-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="94767-107">Диспетчер групп многоадресной рассылки имеет предопределенный набор правил, которые используются для определения того, когда вызывается этот обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="94767-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="94767-108">Эти правила основаны на типе запроса на очистку, отправленном клиентом, и порядке, в котором были получены запросы на очистку.</span><span class="sxs-lookup"><span data-stu-id="94767-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="94767-109">Запросы на удаление с использованием подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="94767-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="94767-110">Когда для группы (, g) получено удаление с подстановочным знаком, \* а окончательный интерфейс удаляется для второго клиента (т. е. когда остаются интерфейсы только для одного клиента), Диспетчер групп многоадресной рассылки вызывает обратный вызов [**\_ \_ \_ обратного вызова оповещения пмгм**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) для этого оставшегося клиента.</span><span class="sxs-lookup"><span data-stu-id="94767-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="94767-111">После удаления окончательного интерфейса для последнего клиента (т. е. Если другие интерфейсы не остаются) вызывается этот обратный вызов для всех остальных клиентов, зарегистрированных в диспетчере групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="94767-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="94767-112">Source-Specific запросов на очистку</span><span class="sxs-lookup"><span data-stu-id="94767-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="94767-113">При получении определенного для источника очистки для группы (s, g) Диспетчер групп многоадресной рассылки вызывает обратный вызов [**\_ \_ оповещения \_ пмгм для очистки**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) только для клиента, владеющего входящим интерфейсом к источнику s.</span><span class="sxs-lookup"><span data-stu-id="94767-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




