---
title: Атрибут ms-DS-Quota-доверенного лица
description: Идентификатор безопасности субъекта безопасности, для которого назначается квота.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута доверенного лица MS-DS-Quota
- Схема AD атрибута msDS-Куотатрусти
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655172"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="e08c1-105">Атрибут ms-DS-Quota-доверенного лица</span><span class="sxs-lookup"><span data-stu-id="e08c1-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="e08c1-106">Идентификатор безопасности субъекта безопасности, для которого назначается квота.</span><span class="sxs-lookup"><span data-stu-id="e08c1-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="e08c1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-107">Entry</span></span> | <span data-ttu-id="e08c1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e08c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="e08c1-109">CN</span></span>                | <span data-ttu-id="e08c1-110">MS-DS-Quota-доверенное лицо</span><span class="sxs-lookup"><span data-stu-id="e08c1-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="e08c1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e08c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e08c1-112">msDS-Куотатрусти</span><span class="sxs-lookup"><span data-stu-id="e08c1-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="e08c1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e08c1-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="e08c1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e08c1-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e08c1-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e08c1-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e08c1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-116">Attribute-Id</span></span>      | <span data-ttu-id="e08c1-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="e08c1-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="e08c1-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e08c1-118">System-Id-Guid</span></span>    | <span data-ttu-id="e08c1-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="e08c1-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="e08c1-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e08c1-120">Syntax</span></span>            | [<span data-ttu-id="e08c1-121">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="e08c1-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="e08c1-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e08c1-122">Implementations</span></span>

-   [<span data-ttu-id="e08c1-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e08c1-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e08c1-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e08c1-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e08c1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e08c1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e08c1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e08c1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e08c1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e08c1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e08c1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e08c1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e08c1-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e08c1-129">Windows Server 2003</span></span>



| <span data-ttu-id="e08c1-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-130">Entry</span></span> | <span data-ttu-id="e08c1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e08c1-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e08c1-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e08c1-134">System-Only</span></span>            | <span data-ttu-id="e08c1-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-135">False</span></span>                                                         |
| <span data-ttu-id="e08c1-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e08c1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e08c1-137">True</span><span class="sxs-lookup"><span data-stu-id="e08c1-137">True</span></span>                                                          |
| <span data-ttu-id="e08c1-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e08c1-138">Is Indexed</span></span>             | <span data-ttu-id="e08c1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-139">False</span></span>                                                         |
| <span data-ttu-id="e08c1-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e08c1-140">In Global Catalog</span></span>      | <span data-ttu-id="e08c1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-141">False</span></span>                                                         |
| <span data-ttu-id="e08c1-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e08c1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e08c1-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e08c1-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e08c1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e08c1-144">Range-Lower</span></span>            | <span data-ttu-id="e08c1-145">0</span><span class="sxs-lookup"><span data-stu-id="e08c1-145">0</span></span>                                                             |
| <span data-ttu-id="e08c1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e08c1-146">Range-Upper</span></span>            | <span data-ttu-id="e08c1-147">28</span><span class="sxs-lookup"><span data-stu-id="e08c1-147">28</span></span>                                                            |
| <span data-ttu-id="e08c1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-148">Search-Flags</span></span>           | <span data-ttu-id="e08c1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e08c1-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="e08c1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-150">System-Flags</span></span>           | <span data-ttu-id="e08c1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e08c1-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="e08c1-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e08c1-152">Classes used in</span></span>        | [<span data-ttu-id="e08c1-153">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="e08c1-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e08c1-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="e08c1-154">ADAM</span></span>



| <span data-ttu-id="e08c1-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-155">Entry</span></span> | <span data-ttu-id="e08c1-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e08c1-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e08c1-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e08c1-159">System-Only</span></span>            | <span data-ttu-id="e08c1-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-160">False</span></span>                                                         |
| <span data-ttu-id="e08c1-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e08c1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e08c1-162">True</span><span class="sxs-lookup"><span data-stu-id="e08c1-162">True</span></span>                                                          |
| <span data-ttu-id="e08c1-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e08c1-163">Is Indexed</span></span>             | <span data-ttu-id="e08c1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-164">False</span></span>                                                         |
| <span data-ttu-id="e08c1-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e08c1-165">In Global Catalog</span></span>      | <span data-ttu-id="e08c1-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-166">False</span></span>                                                         |
| <span data-ttu-id="e08c1-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e08c1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e08c1-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e08c1-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e08c1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e08c1-169">Range-Lower</span></span>            | <span data-ttu-id="e08c1-170">0</span><span class="sxs-lookup"><span data-stu-id="e08c1-170">0</span></span>                                                             |
| <span data-ttu-id="e08c1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e08c1-171">Range-Upper</span></span>            | <span data-ttu-id="e08c1-172">28</span><span class="sxs-lookup"><span data-stu-id="e08c1-172">28</span></span>                                                            |
| <span data-ttu-id="e08c1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-173">Search-Flags</span></span>           | <span data-ttu-id="e08c1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e08c1-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="e08c1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-175">System-Flags</span></span>           | <span data-ttu-id="e08c1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e08c1-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="e08c1-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e08c1-177">Classes used in</span></span>        | [<span data-ttu-id="e08c1-178">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="e08c1-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e08c1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e08c1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e08c1-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-180">Entry</span></span> | <span data-ttu-id="e08c1-181">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e08c1-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e08c1-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e08c1-184">System-Only</span></span>            | <span data-ttu-id="e08c1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-185">False</span></span>                                                         |
| <span data-ttu-id="e08c1-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e08c1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e08c1-187">True</span><span class="sxs-lookup"><span data-stu-id="e08c1-187">True</span></span>                                                          |
| <span data-ttu-id="e08c1-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e08c1-188">Is Indexed</span></span>             | <span data-ttu-id="e08c1-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-189">False</span></span>                                                         |
| <span data-ttu-id="e08c1-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e08c1-190">In Global Catalog</span></span>      | <span data-ttu-id="e08c1-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-191">False</span></span>                                                         |
| <span data-ttu-id="e08c1-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e08c1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e08c1-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e08c1-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e08c1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e08c1-194">Range-Lower</span></span>            | <span data-ttu-id="e08c1-195">0</span><span class="sxs-lookup"><span data-stu-id="e08c1-195">0</span></span>                                                             |
| <span data-ttu-id="e08c1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e08c1-196">Range-Upper</span></span>            | <span data-ttu-id="e08c1-197">28</span><span class="sxs-lookup"><span data-stu-id="e08c1-197">28</span></span>                                                            |
| <span data-ttu-id="e08c1-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-198">Search-Flags</span></span>           | <span data-ttu-id="e08c1-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e08c1-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="e08c1-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-200">System-Flags</span></span>           | <span data-ttu-id="e08c1-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e08c1-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="e08c1-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e08c1-202">Classes used in</span></span>        | [<span data-ttu-id="e08c1-203">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="e08c1-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e08c1-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e08c1-204">Windows Server 2008</span></span>



| <span data-ttu-id="e08c1-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-205">Entry</span></span> | <span data-ttu-id="e08c1-206">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e08c1-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e08c1-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e08c1-209">System-Only</span></span>            | <span data-ttu-id="e08c1-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-210">False</span></span>                                                         |
| <span data-ttu-id="e08c1-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e08c1-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e08c1-212">True</span><span class="sxs-lookup"><span data-stu-id="e08c1-212">True</span></span>                                                          |
| <span data-ttu-id="e08c1-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e08c1-213">Is Indexed</span></span>             | <span data-ttu-id="e08c1-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-214">False</span></span>                                                         |
| <span data-ttu-id="e08c1-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e08c1-215">In Global Catalog</span></span>      | <span data-ttu-id="e08c1-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-216">False</span></span>                                                         |
| <span data-ttu-id="e08c1-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e08c1-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e08c1-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e08c1-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e08c1-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e08c1-219">Range-Lower</span></span>            | <span data-ttu-id="e08c1-220">0</span><span class="sxs-lookup"><span data-stu-id="e08c1-220">0</span></span>                                                             |
| <span data-ttu-id="e08c1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e08c1-221">Range-Upper</span></span>            | <span data-ttu-id="e08c1-222">28</span><span class="sxs-lookup"><span data-stu-id="e08c1-222">28</span></span>                                                            |
| <span data-ttu-id="e08c1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-223">Search-Flags</span></span>           | <span data-ttu-id="e08c1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e08c1-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="e08c1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-225">System-Flags</span></span>           | <span data-ttu-id="e08c1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e08c1-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="e08c1-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e08c1-227">Classes used in</span></span>        | [<span data-ttu-id="e08c1-228">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="e08c1-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e08c1-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e08c1-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e08c1-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-230">Entry</span></span> | <span data-ttu-id="e08c1-231">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e08c1-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e08c1-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e08c1-234">System-Only</span></span>            | <span data-ttu-id="e08c1-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-235">False</span></span>                                                         |
| <span data-ttu-id="e08c1-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e08c1-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e08c1-237">True</span><span class="sxs-lookup"><span data-stu-id="e08c1-237">True</span></span>                                                          |
| <span data-ttu-id="e08c1-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e08c1-238">Is Indexed</span></span>             | <span data-ttu-id="e08c1-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-239">False</span></span>                                                         |
| <span data-ttu-id="e08c1-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e08c1-240">In Global Catalog</span></span>      | <span data-ttu-id="e08c1-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-241">False</span></span>                                                         |
| <span data-ttu-id="e08c1-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e08c1-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e08c1-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e08c1-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e08c1-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e08c1-244">Range-Lower</span></span>            | <span data-ttu-id="e08c1-245">0</span><span class="sxs-lookup"><span data-stu-id="e08c1-245">0</span></span>                                                             |
| <span data-ttu-id="e08c1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e08c1-246">Range-Upper</span></span>            | <span data-ttu-id="e08c1-247">28</span><span class="sxs-lookup"><span data-stu-id="e08c1-247">28</span></span>                                                            |
| <span data-ttu-id="e08c1-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-248">Search-Flags</span></span>           | <span data-ttu-id="e08c1-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e08c1-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="e08c1-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-250">System-Flags</span></span>           | <span data-ttu-id="e08c1-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e08c1-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="e08c1-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e08c1-252">Classes used in</span></span>        | [<span data-ttu-id="e08c1-253">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="e08c1-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e08c1-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e08c1-254">Windows Server 2012</span></span>



| <span data-ttu-id="e08c1-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="e08c1-255">Entry</span></span> | <span data-ttu-id="e08c1-256">Значение</span><span class="sxs-lookup"><span data-stu-id="e08c1-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e08c1-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e08c1-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e08c1-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e08c1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e08c1-259">System-Only</span></span>            | <span data-ttu-id="e08c1-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-260">False</span></span>                                                         |
| <span data-ttu-id="e08c1-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e08c1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e08c1-262">True</span><span class="sxs-lookup"><span data-stu-id="e08c1-262">True</span></span>                                                          |
| <span data-ttu-id="e08c1-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e08c1-263">Is Indexed</span></span>             | <span data-ttu-id="e08c1-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-264">False</span></span>                                                         |
| <span data-ttu-id="e08c1-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e08c1-265">In Global Catalog</span></span>      | <span data-ttu-id="e08c1-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="e08c1-266">False</span></span>                                                         |
| <span data-ttu-id="e08c1-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e08c1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e08c1-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e08c1-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e08c1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e08c1-269">Range-Lower</span></span>            | <span data-ttu-id="e08c1-270">0</span><span class="sxs-lookup"><span data-stu-id="e08c1-270">0</span></span>                                                             |
| <span data-ttu-id="e08c1-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e08c1-271">Range-Upper</span></span>            | <span data-ttu-id="e08c1-272">28</span><span class="sxs-lookup"><span data-stu-id="e08c1-272">28</span></span>                                                            |
| <span data-ttu-id="e08c1-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-273">Search-Flags</span></span>           | <span data-ttu-id="e08c1-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e08c1-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="e08c1-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e08c1-275">System-Flags</span></span>           | <span data-ttu-id="e08c1-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e08c1-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="e08c1-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e08c1-277">Classes used in</span></span>        | [<span data-ttu-id="e08c1-278">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="e08c1-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





