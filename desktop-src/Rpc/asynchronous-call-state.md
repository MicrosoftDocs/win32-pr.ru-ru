---
title: Асинхронное состояние вызова
description: На этой странице описывается асинхронное состояние вызова для вызовов RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889207"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="49347-103">Асинхронное состояние вызова</span><span class="sxs-lookup"><span data-stu-id="49347-103">Asynchronous Call State</span></span>

<span data-ttu-id="49347-104">На этой странице описывается асинхронное состояние вызова для вызовов RPC.</span><span class="sxs-lookup"><span data-stu-id="49347-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="49347-105">Поведение клиента</span><span class="sxs-lookup"><span data-stu-id="49347-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49347-106">Состояние</span><span class="sxs-lookup"><span data-stu-id="49347-106">State</span></span></th>
<th><span data-ttu-id="49347-107">Имя состояния</span><span class="sxs-lookup"><span data-stu-id="49347-107">State name</span></span></th>
<th><span data-ttu-id="49347-108">Действие</span><span class="sxs-lookup"><span data-stu-id="49347-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49347-109">C</span><span class="sxs-lookup"><span data-stu-id="49347-109">C</span></span></td>
<td><span data-ttu-id="49347-110">Сделать вызов</span><span class="sxs-lookup"><span data-stu-id="49347-110">Make the call</span></span></td>
<td><span data-ttu-id="49347-111">Создание RPC</span><span class="sxs-lookup"><span data-stu-id="49347-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="49347-112">При успешном завершении переходит в состояние Вкомп</span><span class="sxs-lookup"><span data-stu-id="49347-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="49347-113">При возникновении исключения перейдите в конец</span><span class="sxs-lookup"><span data-stu-id="49347-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="49347-114">Сбой: перейдите на страницу Can</span><span class="sxs-lookup"><span data-stu-id="49347-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49347-115">Можно</span><span class="sxs-lookup"><span data-stu-id="49347-115">Can</span></span></td>
<td><span data-ttu-id="49347-116">Отменить вызов</span><span class="sxs-lookup"><span data-stu-id="49347-116">Cancel the call</span></span></td>
<td><span data-ttu-id="49347-117">Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп</span><span class="sxs-lookup"><span data-stu-id="49347-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49347-118">вкомп</span><span class="sxs-lookup"><span data-stu-id="49347-118">WComp</span></span></td>
<td><span data-ttu-id="49347-119">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="49347-119">Wait for completion</span></span></td>
<td><span data-ttu-id="49347-120">Ожидается получение уведомления Нотификатионкалл-Complete</span><span class="sxs-lookup"><span data-stu-id="49347-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="49347-121">К Comp</span><span class="sxs-lookup"><span data-stu-id="49347-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49347-122">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="49347-122">Comp</span></span></td>
<td><span data-ttu-id="49347-123">Completion</span><span class="sxs-lookup"><span data-stu-id="49347-123">Completion</span></span></td>
<td><span data-ttu-id="49347-124">Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу</span><span class="sxs-lookup"><span data-stu-id="49347-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49347-125">Конец</span><span class="sxs-lookup"><span data-stu-id="49347-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="49347-126">Поведение сервера</span><span class="sxs-lookup"><span data-stu-id="49347-126">Server Behavior</span></span>



| <span data-ttu-id="49347-127">Состояние</span><span class="sxs-lookup"><span data-stu-id="49347-127">State</span></span> | <span data-ttu-id="49347-128">Имя состояния</span><span class="sxs-lookup"><span data-stu-id="49347-128">State name</span></span>     | <span data-ttu-id="49347-129">Действие</span><span class="sxs-lookup"><span data-stu-id="49347-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49347-130">D</span><span class="sxs-lookup"><span data-stu-id="49347-130">D</span></span>     | <span data-ttu-id="49347-131">Dispatch</span><span class="sxs-lookup"><span data-stu-id="49347-131">Dispatch</span></span>       | <span data-ttu-id="49347-132">Вызов отправляется RPC Рунтимепроцесс</span><span class="sxs-lookup"><span data-stu-id="49347-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="49347-133">К Comp</span><span class="sxs-lookup"><span data-stu-id="49347-133">Go to Comp</span></span><br/> <span data-ttu-id="49347-134">Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу</span><span class="sxs-lookup"><span data-stu-id="49347-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="49347-135">Для корректного сбоя: перейдите на</span><span class="sxs-lookup"><span data-stu-id="49347-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="49347-136">Объект</span><span class="sxs-lookup"><span data-stu-id="49347-136">A</span></span>     | <span data-ttu-id="49347-137">Прервать вызов</span><span class="sxs-lookup"><span data-stu-id="49347-137">Abort the call</span></span> | <span data-ttu-id="49347-138">Вызов [**рпкасинкаборткалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)к концу</span><span class="sxs-lookup"><span data-stu-id="49347-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="49347-139">Соответствовал</span><span class="sxs-lookup"><span data-stu-id="49347-139">Comp</span></span>  | <span data-ttu-id="49347-140">Completion</span><span class="sxs-lookup"><span data-stu-id="49347-140">Completion</span></span>     | <span data-ttu-id="49347-141">Выдача [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)к концу</span><span class="sxs-lookup"><span data-stu-id="49347-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="49347-142">Конец</span><span class="sxs-lookup"><span data-stu-id="49347-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





