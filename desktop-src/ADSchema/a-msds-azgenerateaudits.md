---
title: Атрибут ms-DS-AZ-Generate-audits
description: Логическое поле, указывающее, нужно ли включать аудит времени выполнения (включить аудит для проверок доступа и т. д.).
ms.assetid: 23578f6a-7e7f-4871-9503-73f2ce598173
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-AZ-Generate-audits
- Схема AD атрибута msDS-Азженератеаудитс
topic_type:
- apiref
api_name:
- ms-DS-Az-Generate-Audits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645bdfd2f822139072391d401ecedfedee8680b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893853"
---
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="e8a36-105">Атрибут ms-DS-AZ-Generate-audits</span><span class="sxs-lookup"><span data-stu-id="e8a36-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="e8a36-106">Логическое поле, указывающее, нужно ли включать аудит времени выполнения (включить аудит для проверок доступа и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e8a36-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="e8a36-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e8a36-107">Entry</span></span> | <span data-ttu-id="e8a36-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e8a36-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e8a36-109">CN</span><span class="sxs-lookup"><span data-stu-id="e8a36-109">CN</span></span>                | <span data-ttu-id="e8a36-110">MS-DS-AZ-Generate-аудиты</span><span class="sxs-lookup"><span data-stu-id="e8a36-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="e8a36-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e8a36-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e8a36-112">msDS-Азженератеаудитс</span><span class="sxs-lookup"><span data-stu-id="e8a36-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="e8a36-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e8a36-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e8a36-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e8a36-114">Update Privilege</span></span>  | <span data-ttu-id="e8a36-115">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="e8a36-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="e8a36-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e8a36-116">Update Frequency</span></span>  | <span data-ttu-id="e8a36-117">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="e8a36-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="e8a36-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8a36-118">Attribute-Id</span></span>      | <span data-ttu-id="e8a36-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="e8a36-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="e8a36-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e8a36-120">System-Id-Guid</span></span>    | <span data-ttu-id="e8a36-121">f90abab0-186c-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="e8a36-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="e8a36-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8a36-122">Syntax</span></span>            | [<span data-ttu-id="e8a36-123">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="e8a36-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="e8a36-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e8a36-124">Implementations</span></span>

-   [<span data-ttu-id="e8a36-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8a36-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8a36-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8a36-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8a36-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8a36-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8a36-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8a36-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8a36-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8a36-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e8a36-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8a36-130">Windows Server 2003</span></span>



| <span data-ttu-id="e8a36-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e8a36-131">Entry</span></span> | <span data-ttu-id="e8a36-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e8a36-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a36-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e8a36-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8a36-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8a36-135">System-Only</span></span>            | <span data-ttu-id="e8a36-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e8a36-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e8a36-138">True</span><span class="sxs-lookup"><span data-stu-id="e8a36-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="e8a36-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e8a36-139">Is Indexed</span></span>             | <span data-ttu-id="e8a36-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e8a36-141">In Global Catalog</span></span>      | <span data-ttu-id="e8a36-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e8a36-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8a36-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8a36-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="e8a36-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8a36-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8a36-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-147">Search-Flags</span></span>           | <span data-ttu-id="e8a36-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8a36-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-149">System-Flags</span></span>           | <span data-ttu-id="e8a36-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8a36-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e8a36-151">Classes used in</span></span>        | [<span data-ttu-id="e8a36-152">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e8a36-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="e8a36-153">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="e8a36-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8a36-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8a36-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8a36-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e8a36-155">Entry</span></span> | <span data-ttu-id="e8a36-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e8a36-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a36-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e8a36-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8a36-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8a36-159">System-Only</span></span>            | <span data-ttu-id="e8a36-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e8a36-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e8a36-162">True</span><span class="sxs-lookup"><span data-stu-id="e8a36-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="e8a36-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e8a36-163">Is Indexed</span></span>             | <span data-ttu-id="e8a36-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e8a36-165">In Global Catalog</span></span>      | <span data-ttu-id="e8a36-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e8a36-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8a36-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8a36-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="e8a36-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8a36-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8a36-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-171">Search-Flags</span></span>           | <span data-ttu-id="e8a36-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8a36-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-173">System-Flags</span></span>           | <span data-ttu-id="e8a36-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8a36-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e8a36-175">Classes used in</span></span>        | [<span data-ttu-id="e8a36-176">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e8a36-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="e8a36-177">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="e8a36-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8a36-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8a36-178">Windows Server 2008</span></span>



| <span data-ttu-id="e8a36-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="e8a36-179">Entry</span></span> | <span data-ttu-id="e8a36-180">Значение</span><span class="sxs-lookup"><span data-stu-id="e8a36-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a36-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e8a36-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8a36-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8a36-183">System-Only</span></span>            | <span data-ttu-id="e8a36-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e8a36-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e8a36-186">True</span><span class="sxs-lookup"><span data-stu-id="e8a36-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="e8a36-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e8a36-187">Is Indexed</span></span>             | <span data-ttu-id="e8a36-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e8a36-189">In Global Catalog</span></span>      | <span data-ttu-id="e8a36-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e8a36-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8a36-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8a36-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="e8a36-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8a36-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8a36-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-195">Search-Flags</span></span>           | <span data-ttu-id="e8a36-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8a36-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-197">System-Flags</span></span>           | <span data-ttu-id="e8a36-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8a36-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e8a36-199">Classes used in</span></span>        | [<span data-ttu-id="e8a36-200">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e8a36-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="e8a36-201">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="e8a36-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8a36-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8a36-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8a36-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="e8a36-203">Entry</span></span> | <span data-ttu-id="e8a36-204">Значение</span><span class="sxs-lookup"><span data-stu-id="e8a36-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a36-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e8a36-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8a36-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8a36-207">System-Only</span></span>            | <span data-ttu-id="e8a36-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e8a36-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e8a36-210">True</span><span class="sxs-lookup"><span data-stu-id="e8a36-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="e8a36-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e8a36-211">Is Indexed</span></span>             | <span data-ttu-id="e8a36-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e8a36-213">In Global Catalog</span></span>      | <span data-ttu-id="e8a36-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e8a36-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8a36-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8a36-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="e8a36-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8a36-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8a36-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-219">Search-Flags</span></span>           | <span data-ttu-id="e8a36-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8a36-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-221">System-Flags</span></span>           | <span data-ttu-id="e8a36-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8a36-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e8a36-223">Classes used in</span></span>        | [<span data-ttu-id="e8a36-224">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e8a36-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="e8a36-225">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="e8a36-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8a36-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8a36-226">Windows Server 2012</span></span>



| <span data-ttu-id="e8a36-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="e8a36-227">Entry</span></span> | <span data-ttu-id="e8a36-228">Значение</span><span class="sxs-lookup"><span data-stu-id="e8a36-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a36-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e8a36-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8a36-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8a36-231">System-Only</span></span>            | <span data-ttu-id="e8a36-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e8a36-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e8a36-234">True</span><span class="sxs-lookup"><span data-stu-id="e8a36-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="e8a36-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e8a36-235">Is Indexed</span></span>             | <span data-ttu-id="e8a36-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e8a36-237">In Global Catalog</span></span>      | <span data-ttu-id="e8a36-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="e8a36-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="e8a36-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e8a36-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8a36-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8a36-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="e8a36-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8a36-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8a36-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="e8a36-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-243">Search-Flags</span></span>           | <span data-ttu-id="e8a36-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8a36-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8a36-245">System-Flags</span></span>           | <span data-ttu-id="e8a36-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8a36-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="e8a36-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e8a36-247">Classes used in</span></span>        | [<span data-ttu-id="e8a36-248">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="e8a36-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="e8a36-249">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="e8a36-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





