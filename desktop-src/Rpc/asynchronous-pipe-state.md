---
title: Состояние асинхронного канала
description: На этой странице описывается асинхронное состояние канала для вызовов RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069577"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="d085c-103">Состояние асинхронного канала</span><span class="sxs-lookup"><span data-stu-id="d085c-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="d085c-104">На этой странице описывается асинхронное состояние канала для вызовов RPC.</span><span class="sxs-lookup"><span data-stu-id="d085c-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="d085c-105">В канале</span><span class="sxs-lookup"><span data-stu-id="d085c-105">IN Pipe</span></span>

<span data-ttu-id="d085c-106">Поведение клиента</span><span class="sxs-lookup"><span data-stu-id="d085c-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d085c-107">Состояние</span><span class="sxs-lookup"><span data-stu-id="d085c-107">State</span></span></th>
<th><span data-ttu-id="d085c-108">State Name</span><span class="sxs-lookup"><span data-stu-id="d085c-108">State Name</span></span></th>
<th><span data-ttu-id="d085c-109">Действие</span><span class="sxs-lookup"><span data-stu-id="d085c-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d085c-110">C</span><span class="sxs-lookup"><span data-stu-id="d085c-110">C</span></span></td>
<td><span data-ttu-id="d085c-111">Сделать вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-111">Make the call</span></span></td>
<td><span data-ttu-id="d085c-112">Создание RPC</span><span class="sxs-lookup"><span data-stu-id="d085c-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="d085c-113">При успешном завершении переходит в состояние WS</span><span class="sxs-lookup"><span data-stu-id="d085c-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="d085c-114">При возникновении исключения перейдите в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="d085c-115">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-116">С</span><span class="sxs-lookup"><span data-stu-id="d085c-116">P</span></span></td>
<td><span data-ttu-id="d085c-117">push</span><span class="sxs-lookup"><span data-stu-id="d085c-117">Push</span></span></td>
<td><span data-ttu-id="d085c-118">Выполнить принудительную отправку</span><span class="sxs-lookup"><span data-stu-id="d085c-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="d085c-119">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-119">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-120">При успешном переходе в WS</span><span class="sxs-lookup"><span data-stu-id="d085c-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="d085c-121">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-122">WS</span><span class="sxs-lookup"><span data-stu-id="d085c-122">WS</span></span></td>
<td><span data-ttu-id="d085c-123">Ожидание отправки</span><span class="sxs-lookup"><span data-stu-id="d085c-123">Wait for Send</span></span></td>
<td><span data-ttu-id="d085c-124">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-125">При сбое получения уведомления может</span><span class="sxs-lookup"><span data-stu-id="d085c-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="d085c-126">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите на страницу P</span><span class="sxs-lookup"><span data-stu-id="d085c-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="d085c-127">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</span><span class="sxs-lookup"><span data-stu-id="d085c-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="d085c-128">Если сообщение о сбое <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпккаллкомплете</strong></a> получено Go</span><span class="sxs-lookup"><span data-stu-id="d085c-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-129">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-130">NP</span><span class="sxs-lookup"><span data-stu-id="d085c-130">NP</span></span></td>
<td><span data-ttu-id="d085c-131">Push-уведомления null</span><span class="sxs-lookup"><span data-stu-id="d085c-131">Null Push</span></span></td>
<td><span data-ttu-id="d085c-132">Отправить 0 байт (Push-уведомления null)</span><span class="sxs-lookup"><span data-stu-id="d085c-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="d085c-133">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-133">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-134">При успешном завершении переходит в Вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="d085c-135">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-136">Можно</span><span class="sxs-lookup"><span data-stu-id="d085c-136">Can</span></span></td>
<td><span data-ttu-id="d085c-137">Отменить вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="d085c-138">Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-139">вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-139">WComp</span></span></td>
<td><span data-ttu-id="d085c-140">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="d085c-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="d085c-141">Должно быть получено уведомление о Нотификатионкалл-завершении.</span><span class="sxs-lookup"><span data-stu-id="d085c-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="d085c-142">К Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-143">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="d085c-143">Comp</span></span></td>
<td><span data-ttu-id="d085c-144">Completion</span><span class="sxs-lookup"><span data-stu-id="d085c-144">Completion</span></span></td>
<td><span data-ttu-id="d085c-145">Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-146">Конец</span><span class="sxs-lookup"><span data-stu-id="d085c-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="d085c-147">Поведение сервера</span><span class="sxs-lookup"><span data-stu-id="d085c-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d085c-148">Состояние</span><span class="sxs-lookup"><span data-stu-id="d085c-148">State</span></span></th>
<th><span data-ttu-id="d085c-149">State Name</span><span class="sxs-lookup"><span data-stu-id="d085c-149">State Name</span></span></th>
<th><span data-ttu-id="d085c-150">Действие</span><span class="sxs-lookup"><span data-stu-id="d085c-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d085c-151">D</span><span class="sxs-lookup"><span data-stu-id="d085c-151">D</span></span></td>
<td><span data-ttu-id="d085c-152">Dispatch</span><span class="sxs-lookup"><span data-stu-id="d085c-152">Dispatch</span></span></td>
<td><span data-ttu-id="d085c-153">Вызов отправляется средой выполнения RPC к P</span><span class="sxs-lookup"><span data-stu-id="d085c-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="d085c-154">Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="d085c-155">Для корректного сбоя: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-156">С</span><span class="sxs-lookup"><span data-stu-id="d085c-156">P</span></span></td>
<td><span data-ttu-id="d085c-157">По запросу</span><span class="sxs-lookup"><span data-stu-id="d085c-157">Pull</span></span></td>
<td><span data-ttu-id="d085c-158">Сделать запрос на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="d085c-159">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-159">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-160">При успешном выполнении и синхронном завершении с чтением ненулевых байтов перейдите к P</span><span class="sxs-lookup"><span data-stu-id="d085c-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="d085c-161">При успешном выполнении и синхронном завершении с нулевым количеством считанных байтов (по запросу null) переход к Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="d085c-162">При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WP.</span><span class="sxs-lookup"><span data-stu-id="d085c-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="d085c-163">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-164">WP</span><span class="sxs-lookup"><span data-stu-id="d085c-164">WP</span></span></td>
<td><span data-ttu-id="d085c-165">Ожидание запроса на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="d085c-166">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-167">При сбое для получения завершения перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="d085c-168">Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="d085c-169">Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к P</span><span class="sxs-lookup"><span data-stu-id="d085c-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="d085c-170">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым количеством считанных байтов (по запросу null), перейдите в раздел "Comp"</span><span class="sxs-lookup"><span data-stu-id="d085c-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="d085c-171">При получении ошибки перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="d085c-172">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-173">Объект</span><span class="sxs-lookup"><span data-stu-id="d085c-173">A</span></span></td>
<td><span data-ttu-id="d085c-174">Прервать вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-174">Abort the Call</span></span></td>
<td><span data-ttu-id="d085c-175">Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>рпкасинкаборткалл</strong></a>к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-176">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="d085c-176">Comp</span></span></td>
<td><span data-ttu-id="d085c-177">Completion</span><span class="sxs-lookup"><span data-stu-id="d085c-177">Completion</span></span></td>
<td><span data-ttu-id="d085c-178">Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-179">Конец</span><span class="sxs-lookup"><span data-stu-id="d085c-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="d085c-180">ВЫХОДНОЙ канал</span><span class="sxs-lookup"><span data-stu-id="d085c-180">OUT Pipe</span></span>

<span data-ttu-id="d085c-181">Поведение клиента</span><span class="sxs-lookup"><span data-stu-id="d085c-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d085c-182">Состояние</span><span class="sxs-lookup"><span data-stu-id="d085c-182">State</span></span></th>
<th><span data-ttu-id="d085c-183">State Name</span><span class="sxs-lookup"><span data-stu-id="d085c-183">State Name</span></span></th>
<th><span data-ttu-id="d085c-184">Действие</span><span class="sxs-lookup"><span data-stu-id="d085c-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d085c-185">C</span><span class="sxs-lookup"><span data-stu-id="d085c-185">C</span></span></td>
<td><span data-ttu-id="d085c-186">Сделать вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-186">Make the call</span></span></td>
<td><span data-ttu-id="d085c-187">Создание RPC</span><span class="sxs-lookup"><span data-stu-id="d085c-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="d085c-188">При успешном переходе на P</span><span class="sxs-lookup"><span data-stu-id="d085c-188">On success go to P</span></span></li>
<li><span data-ttu-id="d085c-189">При сбое перейдите в раздел Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-190">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-191">С</span><span class="sxs-lookup"><span data-stu-id="d085c-191">P</span></span></td>
<td><span data-ttu-id="d085c-192">По запросу</span><span class="sxs-lookup"><span data-stu-id="d085c-192">Pull</span></span></td>
<td><span data-ttu-id="d085c-193">Сделать запрос на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="d085c-194">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-194">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-195">При успешном выполнении и синхронном завершении с чтением ненулевых байтов перейдите к P</span><span class="sxs-lookup"><span data-stu-id="d085c-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="d085c-196">При успешном выполнении и синхронном завершении с нулевым количеством считанных байтов (по запросу null) перейдите в Вкомп.</span><span class="sxs-lookup"><span data-stu-id="d085c-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="d085c-197">При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WP.</span><span class="sxs-lookup"><span data-stu-id="d085c-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="d085c-198">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-199">WP</span><span class="sxs-lookup"><span data-stu-id="d085c-199">WP</span></span></td>
<td><span data-ttu-id="d085c-200">Ожидание запроса на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="d085c-201">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-202">При неудачном завершении переходит к CAN</span><span class="sxs-lookup"><span data-stu-id="d085c-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="d085c-203">Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, переходит к CAN</span><span class="sxs-lookup"><span data-stu-id="d085c-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="d085c-204">Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к P</span><span class="sxs-lookup"><span data-stu-id="d085c-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="d085c-205">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым количеством считанных байтов (по запросу null), перейдите в раздел "Comp"</span><span class="sxs-lookup"><span data-stu-id="d085c-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="d085c-206">Если ошибка получена, можно</span><span class="sxs-lookup"><span data-stu-id="d085c-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="d085c-207">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-208">Можно</span><span class="sxs-lookup"><span data-stu-id="d085c-208">Can</span></span></td>
<td><span data-ttu-id="d085c-209">Отменить вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="d085c-210">Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-211">вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-211">WComp</span></span></td>
<td><span data-ttu-id="d085c-212">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="d085c-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="d085c-213">Ожидание уведомления.</span><span class="sxs-lookup"><span data-stu-id="d085c-213">Wait for notification.</span></span> <span data-ttu-id="d085c-214">Должно быть получено уведомление о завершении вызова.</span><span class="sxs-lookup"><span data-stu-id="d085c-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="d085c-215">К Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-216">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="d085c-216">Comp</span></span></td>
<td><span data-ttu-id="d085c-217">Completion</span><span class="sxs-lookup"><span data-stu-id="d085c-217">Completion</span></span></td>
<td><span data-ttu-id="d085c-218">Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-219">Конец</span><span class="sxs-lookup"><span data-stu-id="d085c-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="d085c-220">Поведение сервера</span><span class="sxs-lookup"><span data-stu-id="d085c-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d085c-221">Состояние</span><span class="sxs-lookup"><span data-stu-id="d085c-221">State</span></span></th>
<th><span data-ttu-id="d085c-222">State Name</span><span class="sxs-lookup"><span data-stu-id="d085c-222">State Name</span></span></th>
<th><span data-ttu-id="d085c-223">Действие</span><span class="sxs-lookup"><span data-stu-id="d085c-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d085c-224">D</span><span class="sxs-lookup"><span data-stu-id="d085c-224">D</span></span></td>
<td><span data-ttu-id="d085c-225">Dispatch</span><span class="sxs-lookup"><span data-stu-id="d085c-225">Dispatch</span></span></td>
<td><span data-ttu-id="d085c-226">Вызов отправляется средой выполнения RPC к P</span><span class="sxs-lookup"><span data-stu-id="d085c-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="d085c-227">Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="d085c-228">Для корректного сбоя: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-229">С</span><span class="sxs-lookup"><span data-stu-id="d085c-229">P</span></span></td>
<td><span data-ttu-id="d085c-230">push</span><span class="sxs-lookup"><span data-stu-id="d085c-230">Push</span></span></td>
<td><span data-ttu-id="d085c-231">Выполнить принудительную отправку</span><span class="sxs-lookup"><span data-stu-id="d085c-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="d085c-232">При успешном переходе в WP</span><span class="sxs-lookup"><span data-stu-id="d085c-232">On success go to WP</span></span></li>
<li><span data-ttu-id="d085c-233">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="d085c-234">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-235">WP</span><span class="sxs-lookup"><span data-stu-id="d085c-235">WP</span></span></td>
<td><span data-ttu-id="d085c-236">Ожидание принудительной отправки</span><span class="sxs-lookup"><span data-stu-id="d085c-236">Wait for Push</span></span></td>
<td><span data-ttu-id="d085c-237">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-238">При сбое для получения завершения перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="d085c-239">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите на страницу P</span><span class="sxs-lookup"><span data-stu-id="d085c-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="d085c-240">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</span><span class="sxs-lookup"><span data-stu-id="d085c-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="d085c-241">Если ошибка получена, переходите к следующему.</span><span class="sxs-lookup"><span data-stu-id="d085c-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-242">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-243">NP</span><span class="sxs-lookup"><span data-stu-id="d085c-243">NP</span></span></td>
<td><span data-ttu-id="d085c-244">Push-уведомления null</span><span class="sxs-lookup"><span data-stu-id="d085c-244">Null Push</span></span></td>
<td><span data-ttu-id="d085c-245">Отправить 0 байт</span><span class="sxs-lookup"><span data-stu-id="d085c-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="d085c-246">При успешном переходе на WNP</span><span class="sxs-lookup"><span data-stu-id="d085c-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="d085c-247">при сбое перейдите в раздел Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-248">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-249">WNP</span><span class="sxs-lookup"><span data-stu-id="d085c-249">WNP</span></span></td>
<td><span data-ttu-id="d085c-250">Ожидание принудительной отправки null</span><span class="sxs-lookup"><span data-stu-id="d085c-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="d085c-251">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-252">При сбое для получения завершения перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="d085c-253">Если ошибка получена, переходите к следующему.</span><span class="sxs-lookup"><span data-stu-id="d085c-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="d085c-254">Если получено сообщение об успешном выполнении Go</span><span class="sxs-lookup"><span data-stu-id="d085c-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-255">Объект</span><span class="sxs-lookup"><span data-stu-id="d085c-255">A</span></span></td>
<td><span data-ttu-id="d085c-256">Прервать вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-256">Abort the Call</span></span></td>
<td><span data-ttu-id="d085c-257">Вызовите <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>рпкасинкаборткалл</strong></a>; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-258">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="d085c-258">Comp</span></span></td>
<td><span data-ttu-id="d085c-259">Completion</span><span class="sxs-lookup"><span data-stu-id="d085c-259">Completion</span></span></td>
<td><span data-ttu-id="d085c-260">Ошибка <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-261">Конец</span><span class="sxs-lookup"><span data-stu-id="d085c-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="d085c-262">Исходящий канал</span><span class="sxs-lookup"><span data-stu-id="d085c-262">IN-OUT Pipe</span></span>

<span data-ttu-id="d085c-263">Поведение клиента</span><span class="sxs-lookup"><span data-stu-id="d085c-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d085c-264">Состояние</span><span class="sxs-lookup"><span data-stu-id="d085c-264">State</span></span></th>
<th><span data-ttu-id="d085c-265">State Name</span><span class="sxs-lookup"><span data-stu-id="d085c-265">State Name</span></span></th>
<th><span data-ttu-id="d085c-266">Действие</span><span class="sxs-lookup"><span data-stu-id="d085c-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d085c-267">C</span><span class="sxs-lookup"><span data-stu-id="d085c-267">C</span></span></td>
<td><span data-ttu-id="d085c-268">Сделать вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-268">Make the call</span></span></td>
<td><span data-ttu-id="d085c-269">Создание RPC</span><span class="sxs-lookup"><span data-stu-id="d085c-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="d085c-270">При успешном переходе в WS</span><span class="sxs-lookup"><span data-stu-id="d085c-270">On success go to WS</span></span></li>
<li><span data-ttu-id="d085c-271">При возникновении исключения перейдите в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="d085c-272">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-273">PS</span><span class="sxs-lookup"><span data-stu-id="d085c-273">PS</span></span></td>
<td><span data-ttu-id="d085c-274">push</span><span class="sxs-lookup"><span data-stu-id="d085c-274">Push</span></span></td>
<td><span data-ttu-id="d085c-275">Выполнить принудительную отправку</span><span class="sxs-lookup"><span data-stu-id="d085c-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="d085c-276">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-276">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-277">При успешном переходе в WS</span><span class="sxs-lookup"><span data-stu-id="d085c-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="d085c-278">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-279">WS</span><span class="sxs-lookup"><span data-stu-id="d085c-279">WS</span></span></td>
<td><span data-ttu-id="d085c-280">Ожидание отправки</span><span class="sxs-lookup"><span data-stu-id="d085c-280">Wait for Send</span></span></td>
<td><span data-ttu-id="d085c-281">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-282">При сбое получения уведомления может</span><span class="sxs-lookup"><span data-stu-id="d085c-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="d085c-283">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите в PS</span><span class="sxs-lookup"><span data-stu-id="d085c-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="d085c-284">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</span><span class="sxs-lookup"><span data-stu-id="d085c-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="d085c-285">Если сообщение о сбое <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпккаллкомплете</strong></a> получено Go</span><span class="sxs-lookup"><span data-stu-id="d085c-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-286">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-287">NP</span><span class="sxs-lookup"><span data-stu-id="d085c-287">NP</span></span></td>
<td><span data-ttu-id="d085c-288">Push-уведомления null</span><span class="sxs-lookup"><span data-stu-id="d085c-288">Null Push</span></span></td>
<td><span data-ttu-id="d085c-289">Отправить 0 байт (Push-уведомления null)</span><span class="sxs-lookup"><span data-stu-id="d085c-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="d085c-290">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-290">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-291">При успешном переходе на PL</span><span class="sxs-lookup"><span data-stu-id="d085c-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="d085c-292">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-293">PL</span><span class="sxs-lookup"><span data-stu-id="d085c-293">PL</span></span></td>
<td><span data-ttu-id="d085c-294">По запросу</span><span class="sxs-lookup"><span data-stu-id="d085c-294">Pull</span></span></td>
<td><span data-ttu-id="d085c-295">Сделать запрос на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="d085c-296">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-296">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-297">При успешном выполнении и синхронном завершении с ненулевыми байтами чтение переходит к PL</span><span class="sxs-lookup"><span data-stu-id="d085c-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="d085c-298">При успешном выполнении и синхронном завершении с нулевым количеством считанных байтов (по запросу null) перейдите в Вкомп.</span><span class="sxs-lookup"><span data-stu-id="d085c-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="d085c-299">При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WPL.</span><span class="sxs-lookup"><span data-stu-id="d085c-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="d085c-300">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-301">WPL</span><span class="sxs-lookup"><span data-stu-id="d085c-301">WPL</span></span></td>
<td><span data-ttu-id="d085c-302">Ожидание запроса на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="d085c-303">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-304">При неудачном завершении переходит к CAN</span><span class="sxs-lookup"><span data-stu-id="d085c-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="d085c-305">Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, переходит к CAN</span><span class="sxs-lookup"><span data-stu-id="d085c-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="d085c-306">Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к PL</span><span class="sxs-lookup"><span data-stu-id="d085c-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="d085c-307">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым количеством байтов, перейдите к Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="d085c-308">Если ошибка получена, можно</span><span class="sxs-lookup"><span data-stu-id="d085c-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="d085c-309">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="d085c-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-310">Можно</span><span class="sxs-lookup"><span data-stu-id="d085c-310">Can</span></span></td>
<td><span data-ttu-id="d085c-311">Отменить вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="d085c-312">Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-313">вкомп</span><span class="sxs-lookup"><span data-stu-id="d085c-313">WComp</span></span></td>
<td><span data-ttu-id="d085c-314">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="d085c-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="d085c-315">Ожидание уведомления.</span><span class="sxs-lookup"><span data-stu-id="d085c-315">Wait for notification.</span></span> <span data-ttu-id="d085c-316">Должно быть получено уведомление Каллкомплете.</span><span class="sxs-lookup"><span data-stu-id="d085c-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="d085c-317">К Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-318">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="d085c-318">Comp</span></span></td>
<td><span data-ttu-id="d085c-319">Completion</span><span class="sxs-lookup"><span data-stu-id="d085c-319">Completion</span></span></td>
<td><span data-ttu-id="d085c-320">Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-321">Конец</span><span class="sxs-lookup"><span data-stu-id="d085c-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="d085c-322">Поведение сервера</span><span class="sxs-lookup"><span data-stu-id="d085c-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d085c-323">Состояние</span><span class="sxs-lookup"><span data-stu-id="d085c-323">State</span></span></th>
<th><span data-ttu-id="d085c-324">State Name</span><span class="sxs-lookup"><span data-stu-id="d085c-324">State Name</span></span></th>
<th><span data-ttu-id="d085c-325">Действие</span><span class="sxs-lookup"><span data-stu-id="d085c-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d085c-326">D</span><span class="sxs-lookup"><span data-stu-id="d085c-326">D</span></span></td>
<td><span data-ttu-id="d085c-327">Dispatch</span><span class="sxs-lookup"><span data-stu-id="d085c-327">Dispatch</span></span></td>
<td><span data-ttu-id="d085c-328">Вызов отправляется с помощью RPC Рунтимего в PL.</span><span class="sxs-lookup"><span data-stu-id="d085c-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="d085c-329">Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="d085c-330">Для корректного сбоя: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-331">PL</span><span class="sxs-lookup"><span data-stu-id="d085c-331">PL</span></span></td>
<td><span data-ttu-id="d085c-332">По запросу</span><span class="sxs-lookup"><span data-stu-id="d085c-332">Pull</span></span></td>
<td><span data-ttu-id="d085c-333">Сделать запрос на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="d085c-334">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-334">On failure go to End</span></span></li>
<li><span data-ttu-id="d085c-335">При успешном выполнении и синхронном завершении с ненулевыми байтами чтение переходит к PL</span><span class="sxs-lookup"><span data-stu-id="d085c-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="d085c-336">При успешном выполнении и синхронном завершении с нулевым количеством прочитанных байтов (по запросу null) переход к PS</span><span class="sxs-lookup"><span data-stu-id="d085c-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="d085c-337">При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WPL.</span><span class="sxs-lookup"><span data-stu-id="d085c-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="d085c-338">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-339">WPL</span><span class="sxs-lookup"><span data-stu-id="d085c-339">WPL</span></span></td>
<td><span data-ttu-id="d085c-340">Ожидание запроса на вытягивание</span><span class="sxs-lookup"><span data-stu-id="d085c-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="d085c-341">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-342">При сбое для получения завершения перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="d085c-343">Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="d085c-344">Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к PL</span><span class="sxs-lookup"><span data-stu-id="d085c-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="d085c-345">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым числом байтов Read, перейдите к PS</span><span class="sxs-lookup"><span data-stu-id="d085c-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="d085c-346">Если ошибка получена, перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="d085c-347">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-348">PS</span><span class="sxs-lookup"><span data-stu-id="d085c-348">PS</span></span></td>
<td><span data-ttu-id="d085c-349">push</span><span class="sxs-lookup"><span data-stu-id="d085c-349">Push</span></span></td>
<td><span data-ttu-id="d085c-350">Выполнить принудительную отправку</span><span class="sxs-lookup"><span data-stu-id="d085c-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="d085c-351">При успешном переходе в WPS</span><span class="sxs-lookup"><span data-stu-id="d085c-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="d085c-352">При сбое переходит в конец</span><span class="sxs-lookup"><span data-stu-id="d085c-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="d085c-353">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-354">Информационный</span><span class="sxs-lookup"><span data-stu-id="d085c-354">WPS</span></span></td>
<td><span data-ttu-id="d085c-355">Ожидание принудительной отправки</span><span class="sxs-lookup"><span data-stu-id="d085c-355">Wait for Push</span></span></td>
<td><span data-ttu-id="d085c-356">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-357">При сбое для получения завершения перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="d085c-358">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите в PS</span><span class="sxs-lookup"><span data-stu-id="d085c-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="d085c-359">Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</span><span class="sxs-lookup"><span data-stu-id="d085c-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="d085c-360">Если ошибка получена, переходите к следующему.</span><span class="sxs-lookup"><span data-stu-id="d085c-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-361">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-362">NP</span><span class="sxs-lookup"><span data-stu-id="d085c-362">NP</span></span></td>
<td><span data-ttu-id="d085c-363">Push-уведомления null</span><span class="sxs-lookup"><span data-stu-id="d085c-363">Null Push</span></span></td>
<td><span data-ttu-id="d085c-364">Отправить 0 байт</span><span class="sxs-lookup"><span data-stu-id="d085c-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="d085c-365">При успешном переходе на WNP</span><span class="sxs-lookup"><span data-stu-id="d085c-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="d085c-366">при сбое перейдите в раздел Comp</span><span class="sxs-lookup"><span data-stu-id="d085c-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="d085c-367">Сбой: перейдите на</span><span class="sxs-lookup"><span data-stu-id="d085c-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-368">WNP</span><span class="sxs-lookup"><span data-stu-id="d085c-368">WNP</span></span></td>
<td><span data-ttu-id="d085c-369">Ожидание принудительной отправки null</span><span class="sxs-lookup"><span data-stu-id="d085c-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="d085c-370">Ожидание уведомления</span><span class="sxs-lookup"><span data-stu-id="d085c-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="d085c-371">При сбое для получения завершения перейдите к</span><span class="sxs-lookup"><span data-stu-id="d085c-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="d085c-372">Если ошибка получена, переходите к следующему.</span><span class="sxs-lookup"><span data-stu-id="d085c-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="d085c-373">Если получено сообщение об успешном выполнении Go</span><span class="sxs-lookup"><span data-stu-id="d085c-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-374">Объект</span><span class="sxs-lookup"><span data-stu-id="d085c-374">A</span></span></td>
<td><span data-ttu-id="d085c-375">Прервать вызов</span><span class="sxs-lookup"><span data-stu-id="d085c-375">Abort the Call</span></span></td>
<td><span data-ttu-id="d085c-376">Вызовите <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>рпкасинкаборткалл</strong></a>; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d085c-377">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="d085c-377">Comp</span></span></td>
<td><span data-ttu-id="d085c-378">Completion</span><span class="sxs-lookup"><span data-stu-id="d085c-378">Completion</span></span></td>
<td><span data-ttu-id="d085c-379">Ошибка <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>; к концу</span><span class="sxs-lookup"><span data-stu-id="d085c-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d085c-380">Конец</span><span class="sxs-lookup"><span data-stu-id="d085c-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





