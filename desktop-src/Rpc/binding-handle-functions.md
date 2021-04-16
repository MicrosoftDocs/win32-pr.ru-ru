---
title: Функции обработчика привязки
description: В следующей таблице содержится список исполняемых процедур среды выполнения RPC, которые работают с дескрипторами привязки и указывают тип разрешенного дескриптора привязки.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672015"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="3ba26-103">Функции обработчика привязки</span><span class="sxs-lookup"><span data-stu-id="3ba26-103">Binding Handle Functions</span></span>

<span data-ttu-id="3ba26-104">В следующей таблице содержится список исполняемых процедур среды выполнения RPC, которые работают с дескрипторами привязки и указывают тип разрешенного дескриптора привязки.</span><span class="sxs-lookup"><span data-stu-id="3ba26-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="3ba26-105">Подпрограмма</span><span class="sxs-lookup"><span data-stu-id="3ba26-105">Routine</span></span>                                                            | <span data-ttu-id="3ba26-106">Входной аргумент</span><span class="sxs-lookup"><span data-stu-id="3ba26-106">Input argument</span></span>   | <span data-ttu-id="3ba26-107">Выходной аргумент</span><span class="sxs-lookup"><span data-stu-id="3ba26-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="3ba26-108">**рпкбиндингкопи**</span><span class="sxs-lookup"><span data-stu-id="3ba26-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="3ba26-109">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-109">Server</span></span>           | <span data-ttu-id="3ba26-110">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-110">Server</span></span>          |
| [<span data-ttu-id="3ba26-111">**рпкбиндингфри**</span><span class="sxs-lookup"><span data-stu-id="3ba26-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="3ba26-112">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-112">Server</span></span>           | <span data-ttu-id="3ba26-113">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-113">None</span></span>            |
| [<span data-ttu-id="3ba26-114">**рпкбиндингфромстрингбиндинг**</span><span class="sxs-lookup"><span data-stu-id="3ba26-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="3ba26-115">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-115">None</span></span>             | <span data-ttu-id="3ba26-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-116">Server</span></span>          |
| [<span data-ttu-id="3ba26-117">**рпкбиндингинкаусклиент**</span><span class="sxs-lookup"><span data-stu-id="3ba26-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="3ba26-118">Клиент</span><span class="sxs-lookup"><span data-stu-id="3ba26-118">Client</span></span>           | <span data-ttu-id="3ba26-119">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-119">None</span></span>            |
| [<span data-ttu-id="3ba26-120">**рпкбиндингинкаусинфо**</span><span class="sxs-lookup"><span data-stu-id="3ba26-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="3ba26-121">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-121">Server</span></span>           | <span data-ttu-id="3ba26-122">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-122">None</span></span>            |
| [<span data-ttu-id="3ba26-123">**рпкбиндингинкобжект**</span><span class="sxs-lookup"><span data-stu-id="3ba26-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="3ba26-124">Сервер или клиент</span><span class="sxs-lookup"><span data-stu-id="3ba26-124">Server or client</span></span> | <span data-ttu-id="3ba26-125">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-125">None</span></span>            |
| [<span data-ttu-id="3ba26-126">**рпкбиндингресет**</span><span class="sxs-lookup"><span data-stu-id="3ba26-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="3ba26-127">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-127">Server</span></span>           | <span data-ttu-id="3ba26-128">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-128">None</span></span>            |
| [<span data-ttu-id="3ba26-129">**рпкбиндингсетаусинфо**</span><span class="sxs-lookup"><span data-stu-id="3ba26-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="3ba26-130">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-130">Server</span></span>           | <span data-ttu-id="3ba26-131">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-131">None</span></span>            |
| [<span data-ttu-id="3ba26-132">**рпкбиндингсетобжект**</span><span class="sxs-lookup"><span data-stu-id="3ba26-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="3ba26-133">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-133">Server</span></span>           | <span data-ttu-id="3ba26-134">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-134">None</span></span>            |
| [<span data-ttu-id="3ba26-135">**рпкбиндингтострингбиндинг**</span><span class="sxs-lookup"><span data-stu-id="3ba26-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="3ba26-136">Сервер или клиент</span><span class="sxs-lookup"><span data-stu-id="3ba26-136">Server or client</span></span> | <span data-ttu-id="3ba26-137">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-137">None</span></span>            |
| [<span data-ttu-id="3ba26-138">**рпкбиндингвекторфри**</span><span class="sxs-lookup"><span data-stu-id="3ba26-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="3ba26-139">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-139">Server</span></span>           | <span data-ttu-id="3ba26-140">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-140">None</span></span>            |
| [<span data-ttu-id="3ba26-141">**рпкнсбиндинжекспорт**</span><span class="sxs-lookup"><span data-stu-id="3ba26-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="3ba26-142">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-142">Server</span></span>           | <span data-ttu-id="3ba26-143">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-143">None</span></span>            |
| [<span data-ttu-id="3ba26-144">**рпкнсбиндингимпортнекст**</span><span class="sxs-lookup"><span data-stu-id="3ba26-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="3ba26-145">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-145">None</span></span>             | <span data-ttu-id="3ba26-146">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-146">Server</span></span>          |
| [<span data-ttu-id="3ba26-147">**рпкнсбиндинглукупнекст**</span><span class="sxs-lookup"><span data-stu-id="3ba26-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="3ba26-148">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-148">None</span></span>             | <span data-ttu-id="3ba26-149">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-149">Server</span></span>          |
| [<span data-ttu-id="3ba26-150">**рпкнсбиндингселект**</span><span class="sxs-lookup"><span data-stu-id="3ba26-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="3ba26-151">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-151">Server</span></span>           | <span data-ttu-id="3ba26-152">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-152">Server</span></span>          |
| [<span data-ttu-id="3ba26-153">**рпксерверинкбиндингс**</span><span class="sxs-lookup"><span data-stu-id="3ba26-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="3ba26-154">Нет</span><span class="sxs-lookup"><span data-stu-id="3ba26-154">None</span></span>             | <span data-ttu-id="3ba26-155">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ba26-155">Server</span></span>          |



 

 

 




