---
title: Обратные вызовы диспетчера групп многоадресной рассылки
description: Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления клиентов (обычно протоколы маршрутизации) о событиях и изменениях состояния.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890861"
---
# <a name="multicast-group-manager-callbacks"></a><span data-ttu-id="cbd6d-103">Обратные вызовы диспетчера групп многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="cbd6d-103">Multicast Group Manager Callbacks</span></span>

<span data-ttu-id="cbd6d-104">Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления клиентов (обычно это протоколы маршрутизации) о событиях и изменениях состояния:</span><span class="sxs-lookup"><span data-stu-id="cbd6d-104">The multicast group manager uses the following callbacks to notify clients (typically, routing protocols) of events and state changes:</span></span>

[<span data-ttu-id="cbd6d-105">**\_ \_ обратный вызов оповещения о создании пмгм \_**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-105">**PMGM\_CREATION\_ALERT\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[<span data-ttu-id="cbd6d-106">**\_обратный вызов пмгм для \_ оповещения о соединении \_**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-106">**PMGM\_JOIN\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[<span data-ttu-id="cbd6d-107">**\_ \_ обратный вызов оповещения пмгм \_**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-107">**PMGM\_PRUNE\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[<span data-ttu-id="cbd6d-108">**\_ \_ обратный вызов локального ПРИсоединение пмгм \_**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-108">**PMGM\_LOCAL\_JOIN\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[<span data-ttu-id="cbd6d-109">**\_обратный вызов пмгм для локального \_ выхода \_**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-109">**PMGM\_LOCAL\_LEAVE\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[<span data-ttu-id="cbd6d-110">**\_ \_ обратный вызов пмгм РПФ**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-110">**PMGM\_RPF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[<span data-ttu-id="cbd6d-111">**ПМГМ \_ неправильный \_ \_ обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-111">**PMGM\_WRONG\_IF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

<span data-ttu-id="cbd6d-112">Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления IGMP о событиях и изменениях состояния:</span><span class="sxs-lookup"><span data-stu-id="cbd6d-112">The multicast group manager uses the following callbacks to notify IGMP of events and state changes:</span></span>

[<span data-ttu-id="cbd6d-113">**ПМГМ \_ Отключить \_ \_ обратный вызов IGMP**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-113">**PMGM\_DISABLE\_IGMP\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[<span data-ttu-id="cbd6d-114">**ПМГМ \_ включить \_ \_ обратный вызов IGMP**</span><span class="sxs-lookup"><span data-stu-id="cbd6d-114">**PMGM\_ENABLE\_IGMP\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 