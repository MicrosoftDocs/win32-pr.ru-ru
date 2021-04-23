---
title: Атрибут "согласование IPSec-политика-ссылка"
description: Атрибут IPSec-согласовать-Policy-Reference предназначен только для внутреннего использования.
ms.assetid: d30d8817-0661-430a-939d-f91072585807
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "согласование IPSec-политика-ссылка"
- Схема AD атрибута Ипсекнеготиатионполициреференце
topic_type:
- apiref
api_name:
- Ipsec-Negotiation-Policy-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b0fa5ca8d564b02e27aa5c9dfbcb7f3a90d78e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655256"
---
# <a name="ipsec-negotiation-policy-reference-attribute"></a><span data-ttu-id="3505d-105">Атрибут "согласование IPSec-политика-ссылка"</span><span class="sxs-lookup"><span data-stu-id="3505d-105">Ipsec-Negotiation-Policy-Reference attribute</span></span>

<span data-ttu-id="3505d-106">Атрибут **IPSec-согласовать-Policy-Reference** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="3505d-106">The **Ipsec-Negotiation-Policy-Reference** attribute is for internal use only.</span></span>



| <span data-ttu-id="3505d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-107">Entry</span></span> | <span data-ttu-id="3505d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3505d-109">CN</span><span class="sxs-lookup"><span data-stu-id="3505d-109">CN</span></span>                | <span data-ttu-id="3505d-110">IPSec-согласование — политика-Справочник</span><span class="sxs-lookup"><span data-stu-id="3505d-110">Ipsec-Negotiation-Policy-Reference</span></span>      |
| <span data-ttu-id="3505d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3505d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3505d-112">ипсекнеготиатионполициреференце</span><span class="sxs-lookup"><span data-stu-id="3505d-112">ipsecNegotiationPolicyReference</span></span>         |
| <span data-ttu-id="3505d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3505d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="3505d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3505d-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="3505d-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3505d-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="3505d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-116">Attribute-Id</span></span>      | <span data-ttu-id="3505d-117">1.2.840.113556.1.4.628</span><span class="sxs-lookup"><span data-stu-id="3505d-117">1.2.840.113556.1.4.628</span></span>                  |
| <span data-ttu-id="3505d-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3505d-118">System-Id-Guid</span></span>    | <span data-ttu-id="3505d-119">b40ff822-427a-11d1-a9c2-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3505d-119">b40ff822-427a-11d1-a9c2-0000f80367c1</span></span>    |
| <span data-ttu-id="3505d-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3505d-120">Syntax</span></span>            | [<span data-ttu-id="3505d-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3505d-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3505d-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3505d-122">Implementations</span></span>

-   [<span data-ttu-id="3505d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3505d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3505d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3505d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3505d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3505d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3505d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3505d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3505d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3505d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3505d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3505d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3505d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3505d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3505d-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-130">Entry</span></span> | <span data-ttu-id="3505d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3505d-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3505d-132">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-133">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3505d-134">System-Only</span></span>            | <span data-ttu-id="3505d-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-135">False</span></span>                                      |
| <span data-ttu-id="3505d-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3505d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3505d-137">True</span><span class="sxs-lookup"><span data-stu-id="3505d-137">True</span></span>                                       |
| <span data-ttu-id="3505d-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3505d-138">Is Indexed</span></span>             | <span data-ttu-id="3505d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-139">False</span></span>                                      |
| <span data-ttu-id="3505d-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3505d-140">In Global Catalog</span></span>      | <span data-ttu-id="3505d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-141">False</span></span>                                      |
| <span data-ttu-id="3505d-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3505d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3505d-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3505d-143">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3505d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3505d-144">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3505d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3505d-145">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3505d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-146">Search-Flags</span></span>           | <span data-ttu-id="3505d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3505d-147">0x00000000</span></span>                                 |
| <span data-ttu-id="3505d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-148">System-Flags</span></span>           | <span data-ttu-id="3505d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3505d-149">0x00000010</span></span>                                 |
| <span data-ttu-id="3505d-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3505d-150">Classes used in</span></span>        | [<span data-ttu-id="3505d-151">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="3505d-151">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3505d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3505d-152">Windows Server 2003</span></span>



| <span data-ttu-id="3505d-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-153">Entry</span></span> | <span data-ttu-id="3505d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-154">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3505d-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3505d-155">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-156">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="3505d-157">System-Only</span></span>            | <span data-ttu-id="3505d-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-158">False</span></span>                                      |
| <span data-ttu-id="3505d-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3505d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="3505d-160">True</span><span class="sxs-lookup"><span data-stu-id="3505d-160">True</span></span>                                       |
| <span data-ttu-id="3505d-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3505d-161">Is Indexed</span></span>             | <span data-ttu-id="3505d-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-162">False</span></span>                                      |
| <span data-ttu-id="3505d-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3505d-163">In Global Catalog</span></span>      | <span data-ttu-id="3505d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-164">False</span></span>                                      |
| <span data-ttu-id="3505d-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3505d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="3505d-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3505d-166">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3505d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3505d-167">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3505d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3505d-168">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3505d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-169">Search-Flags</span></span>           | <span data-ttu-id="3505d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3505d-170">0x00000000</span></span>                                 |
| <span data-ttu-id="3505d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-171">System-Flags</span></span>           | <span data-ttu-id="3505d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3505d-172">0x00000010</span></span>                                 |
| <span data-ttu-id="3505d-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3505d-173">Classes used in</span></span>        | [<span data-ttu-id="3505d-174">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="3505d-174">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3505d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3505d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3505d-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-176">Entry</span></span> | <span data-ttu-id="3505d-177">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-177">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3505d-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3505d-178">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-179">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="3505d-180">System-Only</span></span>            | <span data-ttu-id="3505d-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-181">False</span></span>                                      |
| <span data-ttu-id="3505d-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3505d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="3505d-183">True</span><span class="sxs-lookup"><span data-stu-id="3505d-183">True</span></span>                                       |
| <span data-ttu-id="3505d-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3505d-184">Is Indexed</span></span>             | <span data-ttu-id="3505d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-185">False</span></span>                                      |
| <span data-ttu-id="3505d-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3505d-186">In Global Catalog</span></span>      | <span data-ttu-id="3505d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-187">False</span></span>                                      |
| <span data-ttu-id="3505d-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3505d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="3505d-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3505d-189">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3505d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3505d-190">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3505d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3505d-191">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3505d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-192">Search-Flags</span></span>           | <span data-ttu-id="3505d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3505d-193">0x00000000</span></span>                                 |
| <span data-ttu-id="3505d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-194">System-Flags</span></span>           | <span data-ttu-id="3505d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3505d-195">0x00000010</span></span>                                 |
| <span data-ttu-id="3505d-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3505d-196">Classes used in</span></span>        | [<span data-ttu-id="3505d-197">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="3505d-197">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3505d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3505d-198">Windows Server 2008</span></span>



| <span data-ttu-id="3505d-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-199">Entry</span></span> | <span data-ttu-id="3505d-200">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-200">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3505d-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3505d-201">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-202">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="3505d-203">System-Only</span></span>            | <span data-ttu-id="3505d-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-204">False</span></span>                                      |
| <span data-ttu-id="3505d-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3505d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="3505d-206">True</span><span class="sxs-lookup"><span data-stu-id="3505d-206">True</span></span>                                       |
| <span data-ttu-id="3505d-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3505d-207">Is Indexed</span></span>             | <span data-ttu-id="3505d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-208">False</span></span>                                      |
| <span data-ttu-id="3505d-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3505d-209">In Global Catalog</span></span>      | <span data-ttu-id="3505d-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-210">False</span></span>                                      |
| <span data-ttu-id="3505d-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3505d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="3505d-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3505d-212">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3505d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3505d-213">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3505d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3505d-214">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3505d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-215">Search-Flags</span></span>           | <span data-ttu-id="3505d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3505d-216">0x00000000</span></span>                                 |
| <span data-ttu-id="3505d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-217">System-Flags</span></span>           | <span data-ttu-id="3505d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3505d-218">0x00000010</span></span>                                 |
| <span data-ttu-id="3505d-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3505d-219">Classes used in</span></span>        | [<span data-ttu-id="3505d-220">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="3505d-220">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3505d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3505d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3505d-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-222">Entry</span></span> | <span data-ttu-id="3505d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-223">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3505d-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3505d-224">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-225">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="3505d-226">System-Only</span></span>            | <span data-ttu-id="3505d-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-227">False</span></span>                                      |
| <span data-ttu-id="3505d-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3505d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="3505d-229">True</span><span class="sxs-lookup"><span data-stu-id="3505d-229">True</span></span>                                       |
| <span data-ttu-id="3505d-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3505d-230">Is Indexed</span></span>             | <span data-ttu-id="3505d-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-231">False</span></span>                                      |
| <span data-ttu-id="3505d-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3505d-232">In Global Catalog</span></span>      | <span data-ttu-id="3505d-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-233">False</span></span>                                      |
| <span data-ttu-id="3505d-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3505d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="3505d-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3505d-235">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3505d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3505d-236">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3505d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3505d-237">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3505d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-238">Search-Flags</span></span>           | <span data-ttu-id="3505d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3505d-239">0x00000000</span></span>                                 |
| <span data-ttu-id="3505d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-240">System-Flags</span></span>           | <span data-ttu-id="3505d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3505d-241">0x00000010</span></span>                                 |
| <span data-ttu-id="3505d-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3505d-242">Classes used in</span></span>        | [<span data-ttu-id="3505d-243">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="3505d-243">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3505d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3505d-244">Windows Server 2012</span></span>



| <span data-ttu-id="3505d-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="3505d-245">Entry</span></span> | <span data-ttu-id="3505d-246">Значение</span><span class="sxs-lookup"><span data-stu-id="3505d-246">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3505d-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3505d-247">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3505d-248">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3505d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="3505d-249">System-Only</span></span>            | <span data-ttu-id="3505d-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-250">False</span></span>                                      |
| <span data-ttu-id="3505d-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3505d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="3505d-252">True</span><span class="sxs-lookup"><span data-stu-id="3505d-252">True</span></span>                                       |
| <span data-ttu-id="3505d-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3505d-253">Is Indexed</span></span>             | <span data-ttu-id="3505d-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-254">False</span></span>                                      |
| <span data-ttu-id="3505d-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3505d-255">In Global Catalog</span></span>      | <span data-ttu-id="3505d-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="3505d-256">False</span></span>                                      |
| <span data-ttu-id="3505d-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3505d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="3505d-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3505d-258">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3505d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3505d-259">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3505d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3505d-260">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3505d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-261">Search-Flags</span></span>           | <span data-ttu-id="3505d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3505d-262">0x00000000</span></span>                                 |
| <span data-ttu-id="3505d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3505d-263">System-Flags</span></span>           | <span data-ttu-id="3505d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3505d-264">0x00000010</span></span>                                 |
| <span data-ttu-id="3505d-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3505d-265">Classes used in</span></span>        | [<span data-ttu-id="3505d-266">**IPSec-NFA**</span><span class="sxs-lookup"><span data-stu-id="3505d-266">**Ipsec-NFA**</span></span>](c-ipsecnfa.md)<br/> |



 

 





