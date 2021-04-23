---
title: Атрибут ms-DS-NC-Replica-Locations
description: Список серверов, являющихся наборами реплик для соответствующего контекста именования, не являющегося доменом.
ms.assetid: b0379bb6-feee-432a-b484-1a6c8100d027
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Locations в MS-DS-NC-Replica
- Схема AD атрибута msDS-NC-Replica-Locations
topic_type:
- apiref
api_name:
- ms-DS-NC-Replica-Locations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4adc3d3ca3553c8e57cdc114eb045206c1501060
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989821"
---
# <a name="ms-ds-nc-replica-locations-attribute"></a><span data-ttu-id="a8495-105">Атрибут ms-DS-NC-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="a8495-105">ms-DS-NC-Replica-Locations attribute</span></span>

<span data-ttu-id="a8495-106">Список серверов, являющихся наборами реплик для соответствующего контекста именования, не являющегося доменом.</span><span class="sxs-lookup"><span data-stu-id="a8495-106">A list of servers that are the replica set for the corresponding Non-Domain Naming Context.</span></span>



| <span data-ttu-id="a8495-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-107">Entry</span></span> | <span data-ttu-id="a8495-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a8495-109">CN</span><span class="sxs-lookup"><span data-stu-id="a8495-109">CN</span></span>                | <span data-ttu-id="a8495-110">MS-DS-NC-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="a8495-110">ms-DS-NC-Replica-Locations</span></span>              |
| <span data-ttu-id="a8495-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a8495-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a8495-112">msDS-NC-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="a8495-112">msDS-NC-Replica-Locations</span></span>               |
| <span data-ttu-id="a8495-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a8495-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a8495-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a8495-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="a8495-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a8495-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a8495-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-116">Attribute-Id</span></span>      | <span data-ttu-id="a8495-117">1.2.840.113556.1.4.1661</span><span class="sxs-lookup"><span data-stu-id="a8495-117">1.2.840.113556.1.4.1661</span></span>                 |
| <span data-ttu-id="a8495-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a8495-118">System-Id-Guid</span></span>    | <span data-ttu-id="a8495-119">97de9615-b537-46bc-ac0f-10720f3909f3</span><span class="sxs-lookup"><span data-stu-id="a8495-119">97de9615-b537-46bc-ac0f-10720f3909f3</span></span>    |
| <span data-ttu-id="a8495-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8495-120">Syntax</span></span>            | [<span data-ttu-id="a8495-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a8495-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a8495-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a8495-122">Implementations</span></span>

-   [<span data-ttu-id="a8495-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8495-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8495-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a8495-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a8495-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8495-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8495-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8495-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8495-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8495-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8495-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8495-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a8495-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8495-129">Windows Server 2003</span></span>



| <span data-ttu-id="a8495-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-130">Entry</span></span> | <span data-ttu-id="a8495-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a8495-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8495-132">Link-Id</span></span>                | <span data-ttu-id="a8495-133">1044</span><span class="sxs-lookup"><span data-stu-id="a8495-133">1044</span></span>                                       |
| <span data-ttu-id="a8495-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a8495-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8495-135">System-Only</span></span>            | <span data-ttu-id="a8495-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-136">False</span></span>                                      |
| <span data-ttu-id="a8495-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8495-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a8495-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-138">False</span></span>                                      |
| <span data-ttu-id="a8495-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8495-139">Is Indexed</span></span>             | <span data-ttu-id="a8495-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-140">False</span></span>                                      |
| <span data-ttu-id="a8495-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8495-141">In Global Catalog</span></span>      | <span data-ttu-id="a8495-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-142">False</span></span>                                      |
| <span data-ttu-id="a8495-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8495-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8495-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8495-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a8495-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8495-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a8495-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8495-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a8495-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-147">Search-Flags</span></span>           | <span data-ttu-id="a8495-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8495-148">0x00000000</span></span>                                 |
| <span data-ttu-id="a8495-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-149">System-Flags</span></span>           | <span data-ttu-id="a8495-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8495-150">0x00000010</span></span>                                 |
| <span data-ttu-id="a8495-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8495-151">Classes used in</span></span>        | [<span data-ttu-id="a8495-152">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a8495-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a8495-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="a8495-153">ADAM</span></span>



| <span data-ttu-id="a8495-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-154">Entry</span></span> | <span data-ttu-id="a8495-155">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a8495-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8495-156">Link-Id</span></span>                | <span data-ttu-id="a8495-157">1044</span><span class="sxs-lookup"><span data-stu-id="a8495-157">1044</span></span>                                       |
| <span data-ttu-id="a8495-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a8495-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8495-159">System-Only</span></span>            | <span data-ttu-id="a8495-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-160">False</span></span>                                      |
| <span data-ttu-id="a8495-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8495-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a8495-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-162">False</span></span>                                      |
| <span data-ttu-id="a8495-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8495-163">Is Indexed</span></span>             | <span data-ttu-id="a8495-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-164">False</span></span>                                      |
| <span data-ttu-id="a8495-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8495-165">In Global Catalog</span></span>      | <span data-ttu-id="a8495-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-166">False</span></span>                                      |
| <span data-ttu-id="a8495-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8495-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8495-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8495-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a8495-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8495-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a8495-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8495-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a8495-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-171">Search-Flags</span></span>           | <span data-ttu-id="a8495-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8495-172">0x00000000</span></span>                                 |
| <span data-ttu-id="a8495-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-173">System-Flags</span></span>           | <span data-ttu-id="a8495-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8495-174">0x00000010</span></span>                                 |
| <span data-ttu-id="a8495-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8495-175">Classes used in</span></span>        | [<span data-ttu-id="a8495-176">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a8495-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8495-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8495-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8495-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-178">Entry</span></span> | <span data-ttu-id="a8495-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a8495-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8495-180">Link-Id</span></span>                | <span data-ttu-id="a8495-181">1044</span><span class="sxs-lookup"><span data-stu-id="a8495-181">1044</span></span>                                       |
| <span data-ttu-id="a8495-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a8495-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8495-183">System-Only</span></span>            | <span data-ttu-id="a8495-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-184">False</span></span>                                      |
| <span data-ttu-id="a8495-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8495-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a8495-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-186">False</span></span>                                      |
| <span data-ttu-id="a8495-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8495-187">Is Indexed</span></span>             | <span data-ttu-id="a8495-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-188">False</span></span>                                      |
| <span data-ttu-id="a8495-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8495-189">In Global Catalog</span></span>      | <span data-ttu-id="a8495-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-190">False</span></span>                                      |
| <span data-ttu-id="a8495-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8495-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8495-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8495-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a8495-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8495-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a8495-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8495-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a8495-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-195">Search-Flags</span></span>           | <span data-ttu-id="a8495-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8495-196">0x00000000</span></span>                                 |
| <span data-ttu-id="a8495-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-197">System-Flags</span></span>           | <span data-ttu-id="a8495-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8495-198">0x00000010</span></span>                                 |
| <span data-ttu-id="a8495-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8495-199">Classes used in</span></span>        | [<span data-ttu-id="a8495-200">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a8495-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8495-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8495-201">Windows Server 2008</span></span>



| <span data-ttu-id="a8495-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-202">Entry</span></span> | <span data-ttu-id="a8495-203">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a8495-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8495-204">Link-Id</span></span>                | <span data-ttu-id="a8495-205">1044</span><span class="sxs-lookup"><span data-stu-id="a8495-205">1044</span></span>                                       |
| <span data-ttu-id="a8495-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-206">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a8495-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8495-207">System-Only</span></span>            | <span data-ttu-id="a8495-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-208">False</span></span>                                      |
| <span data-ttu-id="a8495-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8495-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a8495-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-210">False</span></span>                                      |
| <span data-ttu-id="a8495-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8495-211">Is Indexed</span></span>             | <span data-ttu-id="a8495-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-212">False</span></span>                                      |
| <span data-ttu-id="a8495-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8495-213">In Global Catalog</span></span>      | <span data-ttu-id="a8495-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-214">False</span></span>                                      |
| <span data-ttu-id="a8495-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8495-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8495-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8495-216">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a8495-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8495-217">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a8495-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8495-218">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a8495-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-219">Search-Flags</span></span>           | <span data-ttu-id="a8495-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8495-220">0x00000000</span></span>                                 |
| <span data-ttu-id="a8495-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-221">System-Flags</span></span>           | <span data-ttu-id="a8495-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8495-222">0x00000010</span></span>                                 |
| <span data-ttu-id="a8495-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8495-223">Classes used in</span></span>        | [<span data-ttu-id="a8495-224">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a8495-224">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8495-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8495-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8495-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-226">Entry</span></span> | <span data-ttu-id="a8495-227">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-227">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a8495-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8495-228">Link-Id</span></span>                | <span data-ttu-id="a8495-229">1044</span><span class="sxs-lookup"><span data-stu-id="a8495-229">1044</span></span>                                       |
| <span data-ttu-id="a8495-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-230">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a8495-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8495-231">System-Only</span></span>            | <span data-ttu-id="a8495-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-232">False</span></span>                                      |
| <span data-ttu-id="a8495-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8495-233">Is-Single-Valued</span></span>       | <span data-ttu-id="a8495-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-234">False</span></span>                                      |
| <span data-ttu-id="a8495-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8495-235">Is Indexed</span></span>             | <span data-ttu-id="a8495-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-236">False</span></span>                                      |
| <span data-ttu-id="a8495-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8495-237">In Global Catalog</span></span>      | <span data-ttu-id="a8495-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-238">False</span></span>                                      |
| <span data-ttu-id="a8495-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8495-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8495-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8495-240">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a8495-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8495-241">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a8495-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8495-242">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a8495-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-243">Search-Flags</span></span>           | <span data-ttu-id="a8495-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8495-244">0x00000000</span></span>                                 |
| <span data-ttu-id="a8495-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-245">System-Flags</span></span>           | <span data-ttu-id="a8495-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8495-246">0x00000010</span></span>                                 |
| <span data-ttu-id="a8495-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8495-247">Classes used in</span></span>        | [<span data-ttu-id="a8495-248">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a8495-248">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8495-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8495-249">Windows Server 2012</span></span>



| <span data-ttu-id="a8495-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8495-250">Entry</span></span> | <span data-ttu-id="a8495-251">Значение</span><span class="sxs-lookup"><span data-stu-id="a8495-251">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a8495-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8495-252">Link-Id</span></span>                | <span data-ttu-id="a8495-253">1044</span><span class="sxs-lookup"><span data-stu-id="a8495-253">1044</span></span>                                       |
| <span data-ttu-id="a8495-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8495-254">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a8495-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8495-255">System-Only</span></span>            | <span data-ttu-id="a8495-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-256">False</span></span>                                      |
| <span data-ttu-id="a8495-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8495-257">Is-Single-Valued</span></span>       | <span data-ttu-id="a8495-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-258">False</span></span>                                      |
| <span data-ttu-id="a8495-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8495-259">Is Indexed</span></span>             | <span data-ttu-id="a8495-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-260">False</span></span>                                      |
| <span data-ttu-id="a8495-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8495-261">In Global Catalog</span></span>      | <span data-ttu-id="a8495-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8495-262">False</span></span>                                      |
| <span data-ttu-id="a8495-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8495-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8495-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8495-264">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a8495-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8495-265">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a8495-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8495-266">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a8495-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-267">Search-Flags</span></span>           | <span data-ttu-id="a8495-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8495-268">0x00000000</span></span>                                 |
| <span data-ttu-id="a8495-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8495-269">System-Flags</span></span>           | <span data-ttu-id="a8495-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8495-270">0x00000010</span></span>                                 |
| <span data-ttu-id="a8495-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8495-271">Classes used in</span></span>        | [<span data-ttu-id="a8495-272">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a8495-272">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





