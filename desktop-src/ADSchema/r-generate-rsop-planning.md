---
title: Создание-RSoP-планирование расширенного права
description: Пользователь, имеющий права в подразделении или домене, сможет создавать данные RSoP в режиме планирования для пользователей или компьютеров в подразделении.
ms.assetid: 4a874e47-c88b-4945-912b-7d4a2dd799df
ms.tgt_platform: multiple
keywords:
- Создание-RSoP-планирование расширенной правой схемы AD
topic_type:
- apiref
api_name:
- Generate-RSoP-Planning
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20b7d3a6431dcc19e83f95c594fd0332e35eb2b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105650408"
---
# <a name="generate-rsop-planning-extended-right"></a><span data-ttu-id="ea120-104">Создание-RSoP-планирование расширенного права</span><span class="sxs-lookup"><span data-stu-id="ea120-104">Generate-RSoP-Planning extended right</span></span>

<span data-ttu-id="ea120-105">Пользователь, имеющий права в подразделении или домене, сможет создавать данные RSoP в режиме планирования для пользователей или компьютеров в подразделении.</span><span class="sxs-lookup"><span data-stu-id="ea120-105">The user who has the rights on an OU or Domain will be able to generate planning mode RSoP data for the users or computers within the OU.</span></span>



| <span data-ttu-id="ea120-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="ea120-106">Entry</span></span> | <span data-ttu-id="ea120-107">Значение</span><span class="sxs-lookup"><span data-stu-id="ea120-107">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="ea120-108">CN</span><span class="sxs-lookup"><span data-stu-id="ea120-108">CN</span></span>           | <span data-ttu-id="ea120-109">Создание-RSoP-планирование</span><span class="sxs-lookup"><span data-stu-id="ea120-109">Generate-RSoP-Planning</span></span>                      |
| <span data-ttu-id="ea120-110">Display-Name</span><span class="sxs-lookup"><span data-stu-id="ea120-110">Display-Name</span></span> | <span data-ttu-id="ea120-111">Генерация RSoP (Планирование)</span><span class="sxs-lookup"><span data-stu-id="ea120-111">Generate Resultant Set of Policy (Planning)</span></span> |
| <span data-ttu-id="ea120-112">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="ea120-112">Rights-GUID</span></span>  | <span data-ttu-id="ea120-113">b7b1b3dd-ab09-4242-9e30-9980e5d322f7</span><span class="sxs-lookup"><span data-stu-id="ea120-113">b7b1b3dd-ab09-4242-9e30-9980e5d322f7</span></span>        |



## <a name="implementations"></a><span data-ttu-id="ea120-114">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ea120-114">Implementations</span></span>

-   [<span data-ttu-id="ea120-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ea120-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ea120-116">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ea120-116">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ea120-117">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ea120-117">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ea120-118">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ea120-118">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ea120-119">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ea120-119">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ea120-120">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea120-120">Windows Server 2003</span></span>



| <span data-ttu-id="ea120-121">Ввод</span><span class="sxs-lookup"><span data-stu-id="ea120-121">Entry</span></span> | <span data-ttu-id="ea120-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ea120-122">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea120-123">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ea120-123">Applies-To</span></span>              | [<span data-ttu-id="ea120-124">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="ea120-124">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="ea120-125">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="ea120-125">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="ea120-126">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="ea120-126">Localization-Display-ID</span></span> | <span data-ttu-id="ea120-127">55</span><span class="sxs-lookup"><span data-stu-id="ea120-127">55</span></span>                                                                                                          |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ea120-128">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ea120-128">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ea120-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="ea120-129">Entry</span></span> | <span data-ttu-id="ea120-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ea120-130">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea120-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ea120-131">Applies-To</span></span>              | [<span data-ttu-id="ea120-132">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="ea120-132">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="ea120-133">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="ea120-133">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="ea120-134">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="ea120-134">Localization-Display-ID</span></span> | <span data-ttu-id="ea120-135">55</span><span class="sxs-lookup"><span data-stu-id="ea120-135">55</span></span>                                                                                                          |



## <a name="windows-server-2008"></a><span data-ttu-id="ea120-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea120-136">Windows Server 2008</span></span>



| <span data-ttu-id="ea120-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="ea120-137">Entry</span></span> | <span data-ttu-id="ea120-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ea120-138">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea120-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ea120-139">Applies-To</span></span>              | [<span data-ttu-id="ea120-140">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="ea120-140">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="ea120-141">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="ea120-141">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="ea120-142">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="ea120-142">Localization-Display-ID</span></span> | <span data-ttu-id="ea120-143">55</span><span class="sxs-lookup"><span data-stu-id="ea120-143">55</span></span>                                                                                                          |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ea120-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea120-144">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ea120-145">Ввод</span><span class="sxs-lookup"><span data-stu-id="ea120-145">Entry</span></span> | <span data-ttu-id="ea120-146">Значение</span><span class="sxs-lookup"><span data-stu-id="ea120-146">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea120-147">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ea120-147">Applies-To</span></span>              | [<span data-ttu-id="ea120-148">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="ea120-148">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="ea120-149">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="ea120-149">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="ea120-150">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="ea120-150">Localization-Display-ID</span></span> | <span data-ttu-id="ea120-151">55</span><span class="sxs-lookup"><span data-stu-id="ea120-151">55</span></span>                                                                                                          |



## <a name="windows-server-2012"></a><span data-ttu-id="ea120-152">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea120-152">Windows Server 2012</span></span>



| <span data-ttu-id="ea120-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="ea120-153">Entry</span></span> | <span data-ttu-id="ea120-154">Значение</span><span class="sxs-lookup"><span data-stu-id="ea120-154">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea120-155">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ea120-155">Applies-To</span></span>              | [<span data-ttu-id="ea120-156">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="ea120-156">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="ea120-157">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="ea120-157">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="ea120-158">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="ea120-158">Localization-Display-ID</span></span> | <span data-ttu-id="ea120-159">55</span><span class="sxs-lookup"><span data-stu-id="ea120-159">55</span></span>                                                                                                          |



 

 





