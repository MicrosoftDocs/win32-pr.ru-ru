---
title: Обновить-Group-Cache — расширенное право
description: Это происходит без входа в систему GC. Отсутствие входа в систему сборки мусора зависит от кэширования членства в группах, и это право доступа используется, чтобы предоставить администраторам и операторам права на обновление кэша, обратившись к доступной сборке мусора.
ms.assetid: 1db49a92-ccf8-4087-ac79-f4c1bcea6aa4
ms.tgt_platform: multiple
keywords:
- Обновление — Расширенная правая схема AD кэша группы
topic_type:
- apiref
api_name:
- Refresh-Group-Cache
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb576b5ef2310bceedb632a3b1ab8453b4d435e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103892973"
---
# <a name="refresh-group-cache-extended-right"></a><span data-ttu-id="9ca7d-105">Обновить-Group-Cache — расширенное право</span><span class="sxs-lookup"><span data-stu-id="9ca7d-105">Refresh-Group-Cache extended right</span></span>

<span data-ttu-id="9ca7d-106">Это происходит без входа в систему GC.</span><span class="sxs-lookup"><span data-stu-id="9ca7d-106">This is for no GC logon.</span></span> <span data-ttu-id="9ca7d-107">Отсутствие входа в систему сборки мусора зависит от кэширования членства в группах, и это право доступа используется, чтобы предоставить администраторам и операторам права на обновление кэша, обратившись к доступной сборке мусора.</span><span class="sxs-lookup"><span data-stu-id="9ca7d-107">No GC logon relies on caching group memberships, and this control access right is used to grant administrators and operators permission rights to cause an immediate refresh of the cache, contacting an available GC.</span></span>



| <span data-ttu-id="9ca7d-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca7d-108">Entry</span></span> | <span data-ttu-id="9ca7d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca7d-109">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="9ca7d-110">CN</span><span class="sxs-lookup"><span data-stu-id="9ca7d-110">CN</span></span>           | <span data-ttu-id="9ca7d-111">Обновление — кэш группы</span><span class="sxs-lookup"><span data-stu-id="9ca7d-111">Refresh-Group-Cache</span></span>                  |
| <span data-ttu-id="9ca7d-112">Display-Name</span><span class="sxs-lookup"><span data-stu-id="9ca7d-112">Display-Name</span></span> | <span data-ttu-id="9ca7d-113">Обновить кэш группы для входа</span><span class="sxs-lookup"><span data-stu-id="9ca7d-113">Refresh Group Cache for Logons</span></span>       |
| <span data-ttu-id="9ca7d-114">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="9ca7d-114">Rights-GUID</span></span>  | <span data-ttu-id="9ca7d-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span><span class="sxs-lookup"><span data-stu-id="9ca7d-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span></span> |



## <a name="implementations"></a><span data-ttu-id="9ca7d-116">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9ca7d-116">Implementations</span></span>

-   [<span data-ttu-id="9ca7d-117">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-117">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ca7d-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ca7d-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ca7d-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ca7d-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9ca7d-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ca7d-122">Windows Server 2003</span></span>



| <span data-ttu-id="9ca7d-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca7d-123">Entry</span></span> | <span data-ttu-id="9ca7d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca7d-124">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="9ca7d-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9ca7d-125">Applies-To</span></span>              | [<span data-ttu-id="9ca7d-126">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-126">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="9ca7d-127">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9ca7d-127">Localization-Display-ID</span></span> | <span data-ttu-id="9ca7d-128">56</span><span class="sxs-lookup"><span data-stu-id="9ca7d-128">56</span></span>                                       |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ca7d-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ca7d-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ca7d-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca7d-130">Entry</span></span> | <span data-ttu-id="9ca7d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca7d-131">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="9ca7d-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9ca7d-132">Applies-To</span></span>              | [<span data-ttu-id="9ca7d-133">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-133">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="9ca7d-134">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9ca7d-134">Localization-Display-ID</span></span> | <span data-ttu-id="9ca7d-135">56</span><span class="sxs-lookup"><span data-stu-id="9ca7d-135">56</span></span>                                       |



## <a name="windows-server-2008"></a><span data-ttu-id="9ca7d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ca7d-136">Windows Server 2008</span></span>



| <span data-ttu-id="9ca7d-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca7d-137">Entry</span></span> | <span data-ttu-id="9ca7d-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca7d-138">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="9ca7d-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9ca7d-139">Applies-To</span></span>              | [<span data-ttu-id="9ca7d-140">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-140">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="9ca7d-141">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9ca7d-141">Localization-Display-ID</span></span> | <span data-ttu-id="9ca7d-142">56</span><span class="sxs-lookup"><span data-stu-id="9ca7d-142">56</span></span>                                       |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ca7d-143">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ca7d-143">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ca7d-144">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca7d-144">Entry</span></span> | <span data-ttu-id="9ca7d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca7d-145">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="9ca7d-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9ca7d-146">Applies-To</span></span>              | [<span data-ttu-id="9ca7d-147">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-147">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="9ca7d-148">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9ca7d-148">Localization-Display-ID</span></span> | <span data-ttu-id="9ca7d-149">56</span><span class="sxs-lookup"><span data-stu-id="9ca7d-149">56</span></span>                                       |



## <a name="windows-server-2012"></a><span data-ttu-id="9ca7d-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ca7d-150">Windows Server 2012</span></span>



| <span data-ttu-id="9ca7d-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca7d-151">Entry</span></span> | <span data-ttu-id="9ca7d-152">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca7d-152">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="9ca7d-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9ca7d-153">Applies-To</span></span>              | [<span data-ttu-id="9ca7d-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ca7d-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="9ca7d-155">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9ca7d-155">Localization-Display-ID</span></span> | <span data-ttu-id="9ca7d-156">56</span><span class="sxs-lookup"><span data-stu-id="9ca7d-156">56</span></span>                                       |



 

 





