---
title: Обработка групп и обратных вызовов
description: В следующей таблице приведена последовательность действий в рабочем взаимодействии между протоколом маршрутизации и диспетчером групп многоадресной рассылки.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339476"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="deed5-103">Обработка групп и обратных вызовов</span><span class="sxs-lookup"><span data-stu-id="deed5-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="deed5-104">В следующей таблице приведена последовательность действий в рабочем взаимодействии между протоколом маршрутизации и диспетчером групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="deed5-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="deed5-105">В первом столбце описываются действия, выполняемые протоколом маршрутизации, а также ответы протокола маршрутизации к диспетчеру групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="deed5-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="deed5-106">Во втором столбце описаны ответы диспетчера групп многоадресной рассылки по протоколу маршрутизации и действия, выполняемые диспетчером групп многоадресной рассылки, такие как обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="deed5-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="deed5-107">В третьем столбце представлены дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="deed5-107">The third column presents any additional information.</span></span>

<span data-ttu-id="deed5-108">Каждая строка таблицы представляет один шаг.</span><span class="sxs-lookup"><span data-stu-id="deed5-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="deed5-109">Задачи, перечисленные в этой таблице, не выполняются в определенном порядке. Вместо этого они происходят в зависимости от состояния членства в группах многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="deed5-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="deed5-110">В таблице ниже показан пример порядка.</span><span class="sxs-lookup"><span data-stu-id="deed5-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="deed5-111">Действие протокола маршрутизации</span><span class="sxs-lookup"><span data-stu-id="deed5-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="deed5-112">Действие диспетчера групп многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="deed5-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="deed5-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="deed5-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="deed5-114">Управление членством в группах на основе сведений о протоколе, полученных в интерфейсах, которыми владеет протокол.</span><span class="sxs-lookup"><span data-stu-id="deed5-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="deed5-115">Управление выполняется с помощью следующих функций:</span><span class="sxs-lookup"><span data-stu-id="deed5-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="deed5-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>мгмаддграупмембершипентри</strong></a></span><span class="sxs-lookup"><span data-stu-id="deed5-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="deed5-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>мгмделетеграупмембершипентри</strong></a></span><span class="sxs-lookup"><span data-stu-id="deed5-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="deed5-118">Добавьте и удалите из списка исходящих интерфейсов для указанных записей (s, g), (*, g) и (*, \*).</span><span class="sxs-lookup"><span data-stu-id="deed5-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="deed5-119">Этот список представляет набор интерфейсов, на которые перенаправляются данные для этой группы.</span><span class="sxs-lookup"><span data-stu-id="deed5-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="deed5-120">Данные для этой группы находятся в указанном источнике.</span><span class="sxs-lookup"><span data-stu-id="deed5-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="deed5-121">Отправка предупреждений в протоколы маршрутизации в форме обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="deed5-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="deed5-122">Следующие события активируют Диспетчер групп многоадресной рассылки для вызова обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="deed5-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="deed5-123">Объединение или выход из групп ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="deed5-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="deed5-124">Членство в группе изменено IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="deed5-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="deed5-125">Данные получены на неправильном интерфейсе ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="deed5-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="deed5-126">Данные, полученные из новых источников или в новую группу ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> и <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="deed5-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="deed5-127">Используя эти обратные вызовы, Диспетчер групп многоадресной рассылки может координировать пересылку пакетов, если на маршрутизаторе есть несколько протоколов многоадресной маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="deed5-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="deed5-128">Перечислите записи многоадресной пересылки (мфес) с помощью функций <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>мгмжетфирстмфе</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>мгмжетнекстмфе</strong></a>и <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>мгмжетмфе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="deed5-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="deed5-129">Принимать решения о многоадресных данных на основе результатов перечисления.</span><span class="sxs-lookup"><span data-stu-id="deed5-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="deed5-130">Возврат запрошенной мфес.</span><span class="sxs-lookup"><span data-stu-id="deed5-130">Return the requested MFEs.</span></span> <span data-ttu-id="deed5-131">Возвращать ERROR_NO_MORE элементов, если больше нет возвращаемых мфес.</span><span class="sxs-lookup"><span data-stu-id="deed5-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="deed5-132">Используйте функции <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>мгмжетфирстмфестатс</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>мгмжетнекстмфестатс</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>мгмжетмфестатс</strong></a> для перечисления статистики мфе.</span><span class="sxs-lookup"><span data-stu-id="deed5-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="deed5-133">Полный пример использования этих функций см. в разделе <a href="administrative-application-scenario.md">сценарий административного приложения</a> .</span><span class="sxs-lookup"><span data-stu-id="deed5-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="deed5-134">Измените вышестоящего соседа в МФЕ с помощью функции <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>мгмсетмфе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="deed5-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="deed5-135">Клиенты используют эту функцию для изменения сведений о входящем интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="deed5-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

