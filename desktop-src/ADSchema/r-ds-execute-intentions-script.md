---
title: DS-Execute-намерения-скрипт расширенное право
description: Право на управление доступом, которое должно быть предоставлено контейнеру секций, что позволяет использовать Rendom.exe или подготовительную операцию в переименовании домена.
ms.assetid: 39e9e76c-55c5-4514-ad4d-102844bcbc5a
ms.tgt_platform: multiple
keywords:
- DS-Execute-намерения-создать скрипт для расширенной правой схемы AD
topic_type:
- apiref
api_name:
- DS-Execute-Intentions-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b34765db2063688ccc8fced0a1e25cac23b98ded
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139067"
---
# <a name="ds-execute-intentions-script-extended-right"></a><span data-ttu-id="9c716-104">DS-Execute-намерения-скрипт расширенное право</span><span class="sxs-lookup"><span data-stu-id="9c716-104">DS-Execute-Intentions-Script extended right</span></span>

<span data-ttu-id="9c716-105">Право на управление доступом, которое должно быть предоставлено контейнеру секций, что позволяет использовать Rendom.exe или подготовительную операцию в переименовании домена.</span><span class="sxs-lookup"><span data-stu-id="9c716-105">Control access right, which should be granted to the partitions container, that allows the Rendom.exe or prepare operation to be used in a domain rename.</span></span> <span data-ttu-id="9c716-106">Это право доступа к элементу управления также отображается как право аудита только при выполнении операции Rendom.exe или выполнения шага.</span><span class="sxs-lookup"><span data-stu-id="9c716-106">This control access right also appears as an audit-only right when the Rendom.exe or execute step operation is performed.</span></span>



| <span data-ttu-id="9c716-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-107">Entry</span></span> | <span data-ttu-id="9c716-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-108">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="9c716-109">CN</span><span class="sxs-lookup"><span data-stu-id="9c716-109">CN</span></span>           | <span data-ttu-id="9c716-110">DS-Execute-намерения-Скрипт</span><span class="sxs-lookup"><span data-stu-id="9c716-110">DS-Execute-Intentions-Script</span></span>         |
| <span data-ttu-id="9c716-111">Display-Name</span><span class="sxs-lookup"><span data-stu-id="9c716-111">Display-Name</span></span> | <span data-ttu-id="9c716-112">Выполнение скрипта обновления леса</span><span class="sxs-lookup"><span data-stu-id="9c716-112">Execute Forest Update Script</span></span>         |
| <span data-ttu-id="9c716-113">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="9c716-113">Rights-GUID</span></span>  | <span data-ttu-id="9c716-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span><span class="sxs-lookup"><span data-stu-id="9c716-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span></span> |



## <a name="implementations"></a><span data-ttu-id="9c716-115">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9c716-115">Implementations</span></span>

-   [<span data-ttu-id="9c716-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c716-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c716-117">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9c716-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9c716-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c716-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c716-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c716-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c716-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c716-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c716-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c716-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9c716-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c716-122">Windows Server 2003</span></span>



| <span data-ttu-id="9c716-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-123">Entry</span></span> | <span data-ttu-id="9c716-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c716-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9c716-125">Applies-To</span></span>              | [<span data-ttu-id="9c716-126">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="9c716-126">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="9c716-127">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9c716-127">Localization-Display-ID</span></span> | <span data-ttu-id="9c716-128">66</span><span class="sxs-lookup"><span data-stu-id="9c716-128">66</span></span>                                                            |



## <a name="adam"></a><span data-ttu-id="9c716-129">ADAM</span><span class="sxs-lookup"><span data-stu-id="9c716-129">ADAM</span></span>



| <span data-ttu-id="9c716-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-130">Entry</span></span> | <span data-ttu-id="9c716-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c716-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9c716-132">Applies-To</span></span>              | [<span data-ttu-id="9c716-133">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="9c716-133">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="9c716-134">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9c716-134">Localization-Display-ID</span></span> | <span data-ttu-id="9c716-135">66</span><span class="sxs-lookup"><span data-stu-id="9c716-135">66</span></span>                                                            |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c716-136">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c716-136">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c716-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-137">Entry</span></span> | <span data-ttu-id="9c716-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-138">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c716-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9c716-139">Applies-To</span></span>              | [<span data-ttu-id="9c716-140">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="9c716-140">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="9c716-141">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9c716-141">Localization-Display-ID</span></span> | <span data-ttu-id="9c716-142">66</span><span class="sxs-lookup"><span data-stu-id="9c716-142">66</span></span>                                                            |



## <a name="windows-server-2008"></a><span data-ttu-id="9c716-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c716-143">Windows Server 2008</span></span>



| <span data-ttu-id="9c716-144">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-144">Entry</span></span> | <span data-ttu-id="9c716-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-145">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c716-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9c716-146">Applies-To</span></span>              | [<span data-ttu-id="9c716-147">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="9c716-147">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="9c716-148">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9c716-148">Localization-Display-ID</span></span> | <span data-ttu-id="9c716-149">66</span><span class="sxs-lookup"><span data-stu-id="9c716-149">66</span></span>                                                            |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c716-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c716-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c716-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-151">Entry</span></span> | <span data-ttu-id="9c716-152">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-152">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c716-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9c716-153">Applies-To</span></span>              | [<span data-ttu-id="9c716-154">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="9c716-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="9c716-155">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9c716-155">Localization-Display-ID</span></span> | <span data-ttu-id="9c716-156">66</span><span class="sxs-lookup"><span data-stu-id="9c716-156">66</span></span>                                                            |



## <a name="windows-server-2012"></a><span data-ttu-id="9c716-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c716-157">Windows Server 2012</span></span>



| <span data-ttu-id="9c716-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="9c716-158">Entry</span></span> | <span data-ttu-id="9c716-159">Значение</span><span class="sxs-lookup"><span data-stu-id="9c716-159">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c716-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9c716-160">Applies-To</span></span>              | [<span data-ttu-id="9c716-161">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="9c716-161">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="9c716-162">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="9c716-162">Localization-Display-ID</span></span> | <span data-ttu-id="9c716-163">66</span><span class="sxs-lookup"><span data-stu-id="9c716-163">66</span></span>                                                            |



 

 





