---
description: На этой странице описывается поведение параметров сокета многоадресной рассылки в зависимости от различных состояний параметров сокета.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Поведение параметра сокета многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072742"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="b2148-103">Поведение параметра сокета многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="b2148-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="b2148-104">На этой странице описывается поведение параметров сокета многоадресной рассылки в зависимости от различных состояний параметров сокета.</span><span class="sxs-lookup"><span data-stu-id="b2148-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="b2148-105">Например, на этой странице описывается поведение, когда \_ \_ параметр сокета членства в источнике для IP-адреса \_ установлен на сокете, для которого параметр IP-адрес \_ добавления \_ \_ членства уже установлен с указанной парой Group/Source в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="b2148-106">Ему разрешается вызывать членство в IP-адресе для \_ \_ \_ одной и той же группы в другом сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="b2148-107">Эта страница помогает правильно разрабатывать и устранять неполадки многоадресных приложений сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="b2148-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b2148-108">Начальный параметр сокета</span><span class="sxs-lookup"><span data-stu-id="b2148-108">Initial socket option</span></span></th>
<th><span data-ttu-id="b2148-109">Конфликт последующего параметра сокета</span><span class="sxs-lookup"><span data-stu-id="b2148-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="b2148-110">Возвращена ошибка</span><span class="sxs-lookup"><span data-stu-id="b2148-110">Error returned</span></span></th>
<th><span data-ttu-id="b2148-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2148-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="b2148-112">IP_ADD_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2148-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2148-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-115">Не вызывайте IP_ADD_MEMBERSHIP с одной и той же группой более одного раза в одном сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2148-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-118">Не вызывайте IP_ADD_SOURCE_MEMBERSHIP с той же группой, которая ранее вызывалась с IP_ADD_MEMBERSHIP в одном сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2148-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-120">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-121">Вместо этого используйте IP_BLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="b2148-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2148-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b2148-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="b2148-123">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-124">Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая ранее не была заблокирована в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2148-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-126">Любой последующий вызов в той же группе или группе, либо к исходной паре</span><span class="sxs-lookup"><span data-stu-id="b2148-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="b2148-127">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-128">Выполнение вызовов параметра сокета для группы или группы или исходной пары, не находящихся в списке включения (из-за удаления членства или других), приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b2148-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="b2148-129">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2148-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2148-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-132">Не вызывайте IP_ADD_MEMBERSHIP с той же группой, которая ранее вызывалась с IP_ADD_SOURCE_MEMBERSHIP в одном сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2148-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-135">Не вызывайте IP_ADD_SOURCE_MEMBERSHIP с той же группой или исходной парой, которая ранее вызывалась с IP_ADD_SOURCE_MEMBERSHIP в одном сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2148-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b2148-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="b2148-137">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-138">Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая ранее не была заблокирована в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b2148-139">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2148-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2148-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b2148-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="b2148-141">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-142">Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая ранее не была заблокирована в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2148-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-145">Возвращает ошибку при попытке удалить пару "Группа-источник", которая не находится в списке включения в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="b2148-146">IP_BLOCK_SOURCE $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2148-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2148-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b2148-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="b2148-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-149">Возвращает ошибку при попытке заблокировать пару "Группа-источник", которая уже заблокирована в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2148-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-151">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-152">Вместо этого используйте IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="b2148-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2148-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="b2148-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="b2148-154">всаеинвал</span><span class="sxs-lookup"><span data-stu-id="b2148-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="b2148-155">Вместо этого используйте IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="b2148-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2148-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b2148-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="b2148-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b2148-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="b2148-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="b2148-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="b2148-159">Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая не находится в списке заблокированных в том же сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2148-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



