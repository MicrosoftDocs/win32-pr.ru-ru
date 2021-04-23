---
title: Атрибут ID атрибута
description: Уникальный идентификатор объекта класса, определенного данным объектом Class-Schema.
ms.assetid: d865966d-0130-4e99-8369-6c11e9f47a82
ms.tgt_platform: multiple
keywords:
- Схема Active Directory атрибута ID
- Схема AD атрибута governsID
topic_type:
- apiref
api_name:
- Governs-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f035a0bf1e432d17c335aebc7b72d401d3298c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989527"
---
# <a name="governs-id-attribute"></a><span data-ttu-id="5e6ec-105">Атрибут ID атрибута</span><span class="sxs-lookup"><span data-stu-id="5e6ec-105">Governs-ID attribute</span></span>

<span data-ttu-id="5e6ec-106">Уникальный идентификатор объекта класса, определенного данным объектом Class-Schema.</span><span class="sxs-lookup"><span data-stu-id="5e6ec-106">The unique object ID of the class defined by this Class-Schema object.</span></span>



| <span data-ttu-id="5e6ec-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-107">Entry</span></span> | <span data-ttu-id="5e6ec-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5e6ec-109">CN</span><span class="sxs-lookup"><span data-stu-id="5e6ec-109">CN</span></span>                | <span data-ttu-id="5e6ec-110">Идентификатор, управляющий</span><span class="sxs-lookup"><span data-stu-id="5e6ec-110">Governs-ID</span></span>                                                      |
| <span data-ttu-id="5e6ec-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5e6ec-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5e6ec-112">governsID</span><span class="sxs-lookup"><span data-stu-id="5e6ec-112">governsID</span></span>                                                       |
| <span data-ttu-id="5e6ec-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5e6ec-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="5e6ec-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5e6ec-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="5e6ec-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5e6ec-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="5e6ec-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-116">Attribute-Id</span></span>      | <span data-ttu-id="5e6ec-117">1.2.840.113556.1.2.22</span><span class="sxs-lookup"><span data-stu-id="5e6ec-117">1.2.840.113556.1.2.22</span></span>                                           |
| <span data-ttu-id="5e6ec-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5e6ec-118">System-Id-Guid</span></span>    | <span data-ttu-id="5e6ec-119">bf96797d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5e6ec-119">bf96797d-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="5e6ec-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e6ec-120">Syntax</span></span>            | [<span data-ttu-id="5e6ec-121">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="5e6ec-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5e6ec-122">Implementations</span></span>

-   [<span data-ttu-id="5e6ec-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5e6ec-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5e6ec-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5e6ec-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5e6ec-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5e6ec-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5e6ec-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5e6ec-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5e6ec-130">Windows 2000 Server</span></span>



| <span data-ttu-id="5e6ec-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-131">Entry</span></span> | <span data-ttu-id="5e6ec-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-135">System-Only</span></span>            | <span data-ttu-id="5e6ec-136">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-136">True</span></span>                                             |
| <span data-ttu-id="5e6ec-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-138">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-138">True</span></span>                                             |
| <span data-ttu-id="5e6ec-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-139">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-140">False</span></span>                                            |
| <span data-ttu-id="5e6ec-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-141">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-142">False</span></span>                                            |
| <span data-ttu-id="5e6ec-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-147">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-148">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-149">System-Flags</span></span>           | <span data-ttu-id="5e6ec-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-150">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-151">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-152">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-152">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5e6ec-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e6ec-153">Windows Server 2003</span></span>



| <span data-ttu-id="5e6ec-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-154">Entry</span></span> | <span data-ttu-id="5e6ec-155">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-158">System-Only</span></span>            | <span data-ttu-id="5e6ec-159">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-159">True</span></span>                                             |
| <span data-ttu-id="5e6ec-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-161">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-161">True</span></span>                                             |
| <span data-ttu-id="5e6ec-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-162">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-163">False</span></span>                                            |
| <span data-ttu-id="5e6ec-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-164">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-165">False</span></span>                                            |
| <span data-ttu-id="5e6ec-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-170">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-171">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-172">System-Flags</span></span>           | <span data-ttu-id="5e6ec-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-173">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-174">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-175">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-175">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5e6ec-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="5e6ec-176">ADAM</span></span>



| <span data-ttu-id="5e6ec-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-177">Entry</span></span> | <span data-ttu-id="5e6ec-178">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-181">System-Only</span></span>            | <span data-ttu-id="5e6ec-182">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-182">True</span></span>                                             |
| <span data-ttu-id="5e6ec-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-184">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-184">True</span></span>                                             |
| <span data-ttu-id="5e6ec-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-185">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-186">False</span></span>                                            |
| <span data-ttu-id="5e6ec-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-187">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-188">False</span></span>                                            |
| <span data-ttu-id="5e6ec-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-193">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-194">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-195">System-Flags</span></span>           | <span data-ttu-id="5e6ec-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-196">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-197">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-198">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-198">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5e6ec-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5e6ec-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5e6ec-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-200">Entry</span></span> | <span data-ttu-id="5e6ec-201">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-204">System-Only</span></span>            | <span data-ttu-id="5e6ec-205">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-205">True</span></span>                                             |
| <span data-ttu-id="5e6ec-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-207">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-207">True</span></span>                                             |
| <span data-ttu-id="5e6ec-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-208">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-209">False</span></span>                                            |
| <span data-ttu-id="5e6ec-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-210">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-211">False</span></span>                                            |
| <span data-ttu-id="5e6ec-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-216">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-217">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-218">System-Flags</span></span>           | <span data-ttu-id="5e6ec-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-219">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-220">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-221">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-221">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5e6ec-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-222">Windows Server 2008</span></span>



| <span data-ttu-id="5e6ec-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-223">Entry</span></span> | <span data-ttu-id="5e6ec-224">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-227">System-Only</span></span>            | <span data-ttu-id="5e6ec-228">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-228">True</span></span>                                             |
| <span data-ttu-id="5e6ec-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-230">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-230">True</span></span>                                             |
| <span data-ttu-id="5e6ec-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-231">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-232">False</span></span>                                            |
| <span data-ttu-id="5e6ec-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-233">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-234">False</span></span>                                            |
| <span data-ttu-id="5e6ec-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-239">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-240">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-241">System-Flags</span></span>           | <span data-ttu-id="5e6ec-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-242">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-243">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-244">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-244">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5e6ec-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5e6ec-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5e6ec-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-246">Entry</span></span> | <span data-ttu-id="5e6ec-247">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-250">System-Only</span></span>            | <span data-ttu-id="5e6ec-251">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-251">True</span></span>                                             |
| <span data-ttu-id="5e6ec-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-252">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-253">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-253">True</span></span>                                             |
| <span data-ttu-id="5e6ec-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-254">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-255">False</span></span>                                            |
| <span data-ttu-id="5e6ec-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-256">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-257">False</span></span>                                            |
| <span data-ttu-id="5e6ec-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-262">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-263">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-264">System-Flags</span></span>           | <span data-ttu-id="5e6ec-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-265">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-266">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-267">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-267">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5e6ec-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5e6ec-268">Windows Server 2012</span></span>



| <span data-ttu-id="5e6ec-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="5e6ec-269">Entry</span></span> | <span data-ttu-id="5e6ec-270">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6ec-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5e6ec-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5e6ec-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e6ec-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5e6ec-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e6ec-273">System-Only</span></span>            | <span data-ttu-id="5e6ec-274">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-274">True</span></span>                                             |
| <span data-ttu-id="5e6ec-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5e6ec-275">Is-Single-Valued</span></span>       | <span data-ttu-id="5e6ec-276">True</span><span class="sxs-lookup"><span data-stu-id="5e6ec-276">True</span></span>                                             |
| <span data-ttu-id="5e6ec-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5e6ec-277">Is Indexed</span></span>             | <span data-ttu-id="5e6ec-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-278">False</span></span>                                            |
| <span data-ttu-id="5e6ec-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5e6ec-279">In Global Catalog</span></span>      | <span data-ttu-id="5e6ec-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="5e6ec-280">False</span></span>                                            |
| <span data-ttu-id="5e6ec-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5e6ec-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e6ec-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e6ec-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5e6ec-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e6ec-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e6ec-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5e6ec-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-285">Search-Flags</span></span>           | <span data-ttu-id="5e6ec-286">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5e6ec-286">0x00000008</span></span>                                       |
| <span data-ttu-id="5e6ec-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e6ec-287">System-Flags</span></span>           | <span data-ttu-id="5e6ec-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e6ec-288">0x00000010</span></span>                                       |
| <span data-ttu-id="5e6ec-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5e6ec-289">Classes used in</span></span>        | [<span data-ttu-id="5e6ec-290">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="5e6ec-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





