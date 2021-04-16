---
title: Атрибут RDN-Атри-ID
description: RDN для атрибута, который используется для именования класса.
ms.assetid: 793199c4-6c5e-481f-8f73-bd59375ab51b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута RDN-Атри-ID
- Схема AD атрибута Рднаттид
topic_type:
- apiref
api_name:
- RDN-Att-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b5fb573d289b71bb459cd8595b5df5115f42bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655074"
---
# <a name="rdn-att-id-attribute"></a><span data-ttu-id="6d715-105">Атрибут RDN-Атри-ID</span><span class="sxs-lookup"><span data-stu-id="6d715-105">RDN-Att-ID attribute</span></span>

<span data-ttu-id="6d715-106">RDN для атрибута, который используется для именования класса.</span><span class="sxs-lookup"><span data-stu-id="6d715-106">The RDN for the attribute that is used to name a class.</span></span>



| <span data-ttu-id="6d715-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-107">Entry</span></span> | <span data-ttu-id="6d715-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6d715-109">CN</span><span class="sxs-lookup"><span data-stu-id="6d715-109">CN</span></span>                | <span data-ttu-id="6d715-110">RDN-Атри-ID</span><span class="sxs-lookup"><span data-stu-id="6d715-110">RDN-Att-ID</span></span>                                                      |
| <span data-ttu-id="6d715-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6d715-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6d715-112">rDNAttID</span><span class="sxs-lookup"><span data-stu-id="6d715-112">rDNAttID</span></span>                                                        |
| <span data-ttu-id="6d715-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6d715-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="6d715-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6d715-114">Update Privilege</span></span>  | <span data-ttu-id="6d715-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="6d715-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="6d715-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6d715-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="6d715-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-117">Attribute-Id</span></span>      | <span data-ttu-id="6d715-118">1.2.840.113556.1.2.26</span><span class="sxs-lookup"><span data-stu-id="6d715-118">1.2.840.113556.1.2.26</span></span>                                           |
| <span data-ttu-id="6d715-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6d715-119">System-Id-Guid</span></span>    | <span data-ttu-id="6d715-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6d715-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="6d715-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d715-121">Syntax</span></span>            | [<span data-ttu-id="6d715-122">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="6d715-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="6d715-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6d715-123">Implementations</span></span>

-   [<span data-ttu-id="6d715-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d715-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d715-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d715-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d715-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6d715-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6d715-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d715-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d715-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d715-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d715-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d715-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d715-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d715-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d715-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d715-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6d715-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-132">Entry</span></span> | <span data-ttu-id="6d715-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-136">System-Only</span></span>            | <span data-ttu-id="6d715-137">True</span><span class="sxs-lookup"><span data-stu-id="6d715-137">True</span></span>                                             |
| <span data-ttu-id="6d715-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-139">True</span><span class="sxs-lookup"><span data-stu-id="6d715-139">True</span></span>                                             |
| <span data-ttu-id="6d715-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-140">Is Indexed</span></span>             | <span data-ttu-id="6d715-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-141">False</span></span>                                            |
| <span data-ttu-id="6d715-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-142">In Global Catalog</span></span>      | <span data-ttu-id="6d715-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-143">False</span></span>                                            |
| <span data-ttu-id="6d715-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-148">Search-Flags</span></span>           | <span data-ttu-id="6d715-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-149">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-150">System-Flags</span></span>           | <span data-ttu-id="6d715-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-151">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-152">Classes used in</span></span>        | [<span data-ttu-id="6d715-153">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d715-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d715-154">Windows Server 2003</span></span>



| <span data-ttu-id="6d715-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-155">Entry</span></span> | <span data-ttu-id="6d715-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-159">System-Only</span></span>            | <span data-ttu-id="6d715-160">True</span><span class="sxs-lookup"><span data-stu-id="6d715-160">True</span></span>                                             |
| <span data-ttu-id="6d715-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-162">True</span><span class="sxs-lookup"><span data-stu-id="6d715-162">True</span></span>                                             |
| <span data-ttu-id="6d715-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-163">Is Indexed</span></span>             | <span data-ttu-id="6d715-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-164">False</span></span>                                            |
| <span data-ttu-id="6d715-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-165">In Global Catalog</span></span>      | <span data-ttu-id="6d715-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-166">False</span></span>                                            |
| <span data-ttu-id="6d715-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-171">Search-Flags</span></span>           | <span data-ttu-id="6d715-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-172">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-173">System-Flags</span></span>           | <span data-ttu-id="6d715-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-174">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-175">Classes used in</span></span>        | [<span data-ttu-id="6d715-176">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6d715-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="6d715-177">ADAM</span></span>



| <span data-ttu-id="6d715-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-178">Entry</span></span> | <span data-ttu-id="6d715-179">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-182">System-Only</span></span>            | <span data-ttu-id="6d715-183">True</span><span class="sxs-lookup"><span data-stu-id="6d715-183">True</span></span>                                             |
| <span data-ttu-id="6d715-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-185">True</span><span class="sxs-lookup"><span data-stu-id="6d715-185">True</span></span>                                             |
| <span data-ttu-id="6d715-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-186">Is Indexed</span></span>             | <span data-ttu-id="6d715-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-187">False</span></span>                                            |
| <span data-ttu-id="6d715-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-188">In Global Catalog</span></span>      | <span data-ttu-id="6d715-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-189">False</span></span>                                            |
| <span data-ttu-id="6d715-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-194">Search-Flags</span></span>           | <span data-ttu-id="6d715-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-195">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-196">System-Flags</span></span>           | <span data-ttu-id="6d715-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-197">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-198">Classes used in</span></span>        | [<span data-ttu-id="6d715-199">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d715-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d715-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d715-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-201">Entry</span></span> | <span data-ttu-id="6d715-202">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-205">System-Only</span></span>            | <span data-ttu-id="6d715-206">True</span><span class="sxs-lookup"><span data-stu-id="6d715-206">True</span></span>                                             |
| <span data-ttu-id="6d715-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-208">True</span><span class="sxs-lookup"><span data-stu-id="6d715-208">True</span></span>                                             |
| <span data-ttu-id="6d715-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-209">Is Indexed</span></span>             | <span data-ttu-id="6d715-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-210">False</span></span>                                            |
| <span data-ttu-id="6d715-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-211">In Global Catalog</span></span>      | <span data-ttu-id="6d715-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-212">False</span></span>                                            |
| <span data-ttu-id="6d715-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-217">Search-Flags</span></span>           | <span data-ttu-id="6d715-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-218">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-219">System-Flags</span></span>           | <span data-ttu-id="6d715-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-220">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-221">Classes used in</span></span>        | [<span data-ttu-id="6d715-222">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d715-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d715-223">Windows Server 2008</span></span>



| <span data-ttu-id="6d715-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-224">Entry</span></span> | <span data-ttu-id="6d715-225">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-228">System-Only</span></span>            | <span data-ttu-id="6d715-229">True</span><span class="sxs-lookup"><span data-stu-id="6d715-229">True</span></span>                                             |
| <span data-ttu-id="6d715-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-231">True</span><span class="sxs-lookup"><span data-stu-id="6d715-231">True</span></span>                                             |
| <span data-ttu-id="6d715-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-232">Is Indexed</span></span>             | <span data-ttu-id="6d715-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-233">False</span></span>                                            |
| <span data-ttu-id="6d715-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-234">In Global Catalog</span></span>      | <span data-ttu-id="6d715-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-235">False</span></span>                                            |
| <span data-ttu-id="6d715-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-240">Search-Flags</span></span>           | <span data-ttu-id="6d715-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-241">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-242">System-Flags</span></span>           | <span data-ttu-id="6d715-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-243">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-244">Classes used in</span></span>        | [<span data-ttu-id="6d715-245">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d715-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d715-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d715-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-247">Entry</span></span> | <span data-ttu-id="6d715-248">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-251">System-Only</span></span>            | <span data-ttu-id="6d715-252">True</span><span class="sxs-lookup"><span data-stu-id="6d715-252">True</span></span>                                             |
| <span data-ttu-id="6d715-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-254">True</span><span class="sxs-lookup"><span data-stu-id="6d715-254">True</span></span>                                             |
| <span data-ttu-id="6d715-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-255">Is Indexed</span></span>             | <span data-ttu-id="6d715-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-256">False</span></span>                                            |
| <span data-ttu-id="6d715-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-257">In Global Catalog</span></span>      | <span data-ttu-id="6d715-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-258">False</span></span>                                            |
| <span data-ttu-id="6d715-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-263">Search-Flags</span></span>           | <span data-ttu-id="6d715-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-264">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-265">System-Flags</span></span>           | <span data-ttu-id="6d715-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-266">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-267">Classes used in</span></span>        | [<span data-ttu-id="6d715-268">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d715-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d715-269">Windows Server 2012</span></span>



| <span data-ttu-id="6d715-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d715-270">Entry</span></span> | <span data-ttu-id="6d715-271">Значение</span><span class="sxs-lookup"><span data-stu-id="6d715-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6d715-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d715-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d715-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6d715-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d715-274">System-Only</span></span>            | <span data-ttu-id="6d715-275">True</span><span class="sxs-lookup"><span data-stu-id="6d715-275">True</span></span>                                             |
| <span data-ttu-id="6d715-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d715-276">Is-Single-Valued</span></span>       | <span data-ttu-id="6d715-277">True</span><span class="sxs-lookup"><span data-stu-id="6d715-277">True</span></span>                                             |
| <span data-ttu-id="6d715-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d715-278">Is Indexed</span></span>             | <span data-ttu-id="6d715-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-279">False</span></span>                                            |
| <span data-ttu-id="6d715-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d715-280">In Global Catalog</span></span>      | <span data-ttu-id="6d715-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d715-281">False</span></span>                                            |
| <span data-ttu-id="6d715-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d715-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d715-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d715-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6d715-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d715-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6d715-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d715-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6d715-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-286">Search-Flags</span></span>           | <span data-ttu-id="6d715-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d715-287">0x00000000</span></span>                                       |
| <span data-ttu-id="6d715-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d715-288">System-Flags</span></span>           | <span data-ttu-id="6d715-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d715-289">0x00000010</span></span>                                       |
| <span data-ttu-id="6d715-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d715-290">Classes used in</span></span>        | [<span data-ttu-id="6d715-291">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6d715-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





