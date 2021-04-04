---
title: Generate-RSoP — ведение журнала расширено справа
description: Пользователь, имеющий права в подразделении или домене, сможет создавать данные RSoP в режиме ведения журнала для пользователей или компьютеров в подразделении.
ms.assetid: 557be624-a58d-417c-bb20-43a9baa751b5
ms.tgt_platform: multiple
keywords:
- Generate-RSoP — ведение журнала расширенной правой схемы AD
topic_type:
- apiref
api_name:
- Generate-RSoP-Logging
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd2798cdba03cd5ad362acb8720f75153437c28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139058"
---
# <a name="generate-rsop-logging-extended-right"></a><span data-ttu-id="3d7e7-104">Generate-RSoP — ведение журнала расширено справа</span><span class="sxs-lookup"><span data-stu-id="3d7e7-104">Generate-RSoP-Logging extended right</span></span>

<span data-ttu-id="3d7e7-105">Пользователь, имеющий права в подразделении или домене, сможет создавать данные RSoP в режиме ведения журнала для пользователей или компьютеров в подразделении.</span><span class="sxs-lookup"><span data-stu-id="3d7e7-105">The user who has the rights on an OU or Domain will be able to generate logging mode RSoP data for the users or computers within the OU.</span></span>



| <span data-ttu-id="3d7e7-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d7e7-106">Entry</span></span> | <span data-ttu-id="3d7e7-107">Значение</span><span class="sxs-lookup"><span data-stu-id="3d7e7-107">Value</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="3d7e7-108">CN</span><span class="sxs-lookup"><span data-stu-id="3d7e7-108">CN</span></span>           | <span data-ttu-id="3d7e7-109">Generate-RSoP — ведение журнала</span><span class="sxs-lookup"><span data-stu-id="3d7e7-109">Generate-RSoP-Logging</span></span>                      |
| <span data-ttu-id="3d7e7-110">Display-Name</span><span class="sxs-lookup"><span data-stu-id="3d7e7-110">Display-Name</span></span> | <span data-ttu-id="3d7e7-111">Генерация RSoP (Протоколирование)</span><span class="sxs-lookup"><span data-stu-id="3d7e7-111">Generate Resultant Set of Policy (Logging)</span></span> |
| <span data-ttu-id="3d7e7-112">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="3d7e7-112">Rights-GUID</span></span>  | <span data-ttu-id="3d7e7-113">b7b1b3de-ab09-4242-9e30-9980e5d322f7</span><span class="sxs-lookup"><span data-stu-id="3d7e7-113">b7b1b3de-ab09-4242-9e30-9980e5d322f7</span></span>       |



## <a name="implementations"></a><span data-ttu-id="3d7e7-114">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3d7e7-114">Implementations</span></span>

-   [<span data-ttu-id="3d7e7-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d7e7-116">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-116">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d7e7-117">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-117">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d7e7-118">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-118">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d7e7-119">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-119">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3d7e7-120">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d7e7-120">Windows Server 2003</span></span>



| <span data-ttu-id="3d7e7-121">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d7e7-121">Entry</span></span> | <span data-ttu-id="3d7e7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3d7e7-122">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7e7-123">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3d7e7-123">Applies-To</span></span>              | [<span data-ttu-id="3d7e7-124">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-124">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="3d7e7-125">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-125">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="3d7e7-126">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="3d7e7-126">Localization-Display-ID</span></span> | <span data-ttu-id="3d7e7-127">58</span><span class="sxs-lookup"><span data-stu-id="3d7e7-127">58</span></span>                                                                                                          |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d7e7-128">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d7e7-128">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d7e7-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d7e7-129">Entry</span></span> | <span data-ttu-id="3d7e7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3d7e7-130">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7e7-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3d7e7-131">Applies-To</span></span>              | [<span data-ttu-id="3d7e7-132">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-132">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="3d7e7-133">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-133">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="3d7e7-134">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="3d7e7-134">Localization-Display-ID</span></span> | <span data-ttu-id="3d7e7-135">58</span><span class="sxs-lookup"><span data-stu-id="3d7e7-135">58</span></span>                                                                                                          |



## <a name="windows-server-2008"></a><span data-ttu-id="3d7e7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d7e7-136">Windows Server 2008</span></span>



| <span data-ttu-id="3d7e7-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d7e7-137">Entry</span></span> | <span data-ttu-id="3d7e7-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3d7e7-138">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7e7-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3d7e7-139">Applies-To</span></span>              | [<span data-ttu-id="3d7e7-140">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-140">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="3d7e7-141">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-141">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="3d7e7-142">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="3d7e7-142">Localization-Display-ID</span></span> | <span data-ttu-id="3d7e7-143">58</span><span class="sxs-lookup"><span data-stu-id="3d7e7-143">58</span></span>                                                                                                          |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d7e7-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d7e7-144">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d7e7-145">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d7e7-145">Entry</span></span> | <span data-ttu-id="3d7e7-146">Значение</span><span class="sxs-lookup"><span data-stu-id="3d7e7-146">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7e7-147">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3d7e7-147">Applies-To</span></span>              | [<span data-ttu-id="3d7e7-148">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-148">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="3d7e7-149">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-149">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="3d7e7-150">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="3d7e7-150">Localization-Display-ID</span></span> | <span data-ttu-id="3d7e7-151">58</span><span class="sxs-lookup"><span data-stu-id="3d7e7-151">58</span></span>                                                                                                          |



## <a name="windows-server-2012"></a><span data-ttu-id="3d7e7-152">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d7e7-152">Windows Server 2012</span></span>



| <span data-ttu-id="3d7e7-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d7e7-153">Entry</span></span> | <span data-ttu-id="3d7e7-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3d7e7-154">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7e7-155">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3d7e7-155">Applies-To</span></span>              | [<span data-ttu-id="3d7e7-156">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-156">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="3d7e7-157">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="3d7e7-157">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="3d7e7-158">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="3d7e7-158">Localization-Display-ID</span></span> | <span data-ttu-id="3d7e7-159">58</span><span class="sxs-lookup"><span data-stu-id="3d7e7-159">58</span></span>                                                                                                          |



 

 





