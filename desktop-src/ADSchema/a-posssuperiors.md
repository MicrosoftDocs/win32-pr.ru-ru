---
title: Атрибут Poss-Superiors
description: Список объектов, которые могут содержать этот класс.
ms.assetid: 7d16c0bd-e27c-4c4a-b6cc-bc59cc295559
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Poss-Superiors
- Схема AD атрибута possSuperiors
topic_type:
- apiref
api_name:
- Poss-Superiors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4a2610ff4ada2c433da6eb28c51d36798f5db9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655313"
---
# <a name="poss-superiors-attribute"></a><span data-ttu-id="68288-105">Атрибут Poss-Superiors</span><span class="sxs-lookup"><span data-stu-id="68288-105">Poss-Superiors attribute</span></span>

<span data-ttu-id="68288-106">Список объектов, которые могут содержать этот класс.</span><span class="sxs-lookup"><span data-stu-id="68288-106">The list of objects that can contain this class.</span></span>



| <span data-ttu-id="68288-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-107">Entry</span></span> | <span data-ttu-id="68288-108">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="68288-109">CN</span><span class="sxs-lookup"><span data-stu-id="68288-109">CN</span></span>                | <span data-ttu-id="68288-110">Poss-Superiors</span><span class="sxs-lookup"><span data-stu-id="68288-110">Poss-Superiors</span></span>                                                  |
| <span data-ttu-id="68288-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="68288-111">Ldap-Display-Name</span></span> | <span data-ttu-id="68288-112">possSuperiors</span><span class="sxs-lookup"><span data-stu-id="68288-112">possSuperiors</span></span>                                                   |
| <span data-ttu-id="68288-113">Размер</span><span class="sxs-lookup"><span data-stu-id="68288-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="68288-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="68288-114">Update Privilege</span></span>  | <span data-ttu-id="68288-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="68288-115">Domain administrator</span></span>                                            |
| <span data-ttu-id="68288-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="68288-116">Update Frequency</span></span>  | <span data-ttu-id="68288-117">При определении класса.</span><span class="sxs-lookup"><span data-stu-id="68288-117">When the class is defined.</span></span>                                      |
| <span data-ttu-id="68288-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="68288-118">Attribute-Id</span></span>      | <span data-ttu-id="68288-119">1.2.840.113556.1.2.8</span><span class="sxs-lookup"><span data-stu-id="68288-119">1.2.840.113556.1.2.8</span></span>                                            |
| <span data-ttu-id="68288-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="68288-120">System-Id-Guid</span></span>    | <span data-ttu-id="68288-121">bf9679fa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="68288-121">bf9679fa-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="68288-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68288-122">Syntax</span></span>            | [<span data-ttu-id="68288-123">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="68288-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="68288-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="68288-124">Implementations</span></span>

-   [<span data-ttu-id="68288-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="68288-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="68288-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="68288-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="68288-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="68288-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="68288-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="68288-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="68288-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="68288-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="68288-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="68288-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="68288-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="68288-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="68288-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68288-132">Windows 2000 Server</span></span>



| <span data-ttu-id="68288-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-133">Entry</span></span> | <span data-ttu-id="68288-134">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-137">System-Only</span></span>            | <span data-ttu-id="68288-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-138">False</span></span>                                            |
| <span data-ttu-id="68288-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-139">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-140">False</span></span>                                            |
| <span data-ttu-id="68288-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-141">Is Indexed</span></span>             | <span data-ttu-id="68288-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-142">False</span></span>                                            |
| <span data-ttu-id="68288-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-143">In Global Catalog</span></span>      | <span data-ttu-id="68288-144">True</span><span class="sxs-lookup"><span data-stu-id="68288-144">True</span></span>                                             |
| <span data-ttu-id="68288-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-149">Search-Flags</span></span>           | <span data-ttu-id="68288-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-150">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-151">System-Flags</span></span>           | <span data-ttu-id="68288-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-152">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-153">Classes used in</span></span>        | [<span data-ttu-id="68288-154">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="68288-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68288-155">Windows Server 2003</span></span>



| <span data-ttu-id="68288-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-156">Entry</span></span> | <span data-ttu-id="68288-157">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-160">System-Only</span></span>            | <span data-ttu-id="68288-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-161">False</span></span>                                            |
| <span data-ttu-id="68288-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-162">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-163">False</span></span>                                            |
| <span data-ttu-id="68288-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-164">Is Indexed</span></span>             | <span data-ttu-id="68288-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-165">False</span></span>                                            |
| <span data-ttu-id="68288-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-166">In Global Catalog</span></span>      | <span data-ttu-id="68288-167">True</span><span class="sxs-lookup"><span data-stu-id="68288-167">True</span></span>                                             |
| <span data-ttu-id="68288-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-172">Search-Flags</span></span>           | <span data-ttu-id="68288-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-173">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-174">System-Flags</span></span>           | <span data-ttu-id="68288-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-175">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-176">Classes used in</span></span>        | [<span data-ttu-id="68288-177">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="68288-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="68288-178">ADAM</span></span>



| <span data-ttu-id="68288-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-179">Entry</span></span> | <span data-ttu-id="68288-180">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-183">System-Only</span></span>            | <span data-ttu-id="68288-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-184">False</span></span>                                            |
| <span data-ttu-id="68288-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-185">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-186">False</span></span>                                            |
| <span data-ttu-id="68288-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-187">Is Indexed</span></span>             | <span data-ttu-id="68288-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-188">False</span></span>                                            |
| <span data-ttu-id="68288-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-189">In Global Catalog</span></span>      | <span data-ttu-id="68288-190">True</span><span class="sxs-lookup"><span data-stu-id="68288-190">True</span></span>                                             |
| <span data-ttu-id="68288-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-195">Search-Flags</span></span>           | <span data-ttu-id="68288-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-196">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-197">System-Flags</span></span>           | <span data-ttu-id="68288-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-198">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-199">Classes used in</span></span>        | [<span data-ttu-id="68288-200">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="68288-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="68288-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="68288-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-202">Entry</span></span> | <span data-ttu-id="68288-203">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-206">System-Only</span></span>            | <span data-ttu-id="68288-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-207">False</span></span>                                            |
| <span data-ttu-id="68288-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-208">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-209">False</span></span>                                            |
| <span data-ttu-id="68288-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-210">Is Indexed</span></span>             | <span data-ttu-id="68288-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-211">False</span></span>                                            |
| <span data-ttu-id="68288-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-212">In Global Catalog</span></span>      | <span data-ttu-id="68288-213">True</span><span class="sxs-lookup"><span data-stu-id="68288-213">True</span></span>                                             |
| <span data-ttu-id="68288-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-218">Search-Flags</span></span>           | <span data-ttu-id="68288-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-219">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-220">System-Flags</span></span>           | <span data-ttu-id="68288-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-221">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-222">Classes used in</span></span>        | [<span data-ttu-id="68288-223">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="68288-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68288-224">Windows Server 2008</span></span>



| <span data-ttu-id="68288-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-225">Entry</span></span> | <span data-ttu-id="68288-226">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-229">System-Only</span></span>            | <span data-ttu-id="68288-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-230">False</span></span>                                            |
| <span data-ttu-id="68288-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-231">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-232">False</span></span>                                            |
| <span data-ttu-id="68288-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-233">Is Indexed</span></span>             | <span data-ttu-id="68288-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-234">False</span></span>                                            |
| <span data-ttu-id="68288-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-235">In Global Catalog</span></span>      | <span data-ttu-id="68288-236">True</span><span class="sxs-lookup"><span data-stu-id="68288-236">True</span></span>                                             |
| <span data-ttu-id="68288-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-241">Search-Flags</span></span>           | <span data-ttu-id="68288-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-242">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-243">System-Flags</span></span>           | <span data-ttu-id="68288-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-244">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-245">Classes used in</span></span>        | [<span data-ttu-id="68288-246">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="68288-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68288-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="68288-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-248">Entry</span></span> | <span data-ttu-id="68288-249">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-252">System-Only</span></span>            | <span data-ttu-id="68288-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-253">False</span></span>                                            |
| <span data-ttu-id="68288-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-254">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-255">False</span></span>                                            |
| <span data-ttu-id="68288-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-256">Is Indexed</span></span>             | <span data-ttu-id="68288-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-257">False</span></span>                                            |
| <span data-ttu-id="68288-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-258">In Global Catalog</span></span>      | <span data-ttu-id="68288-259">True</span><span class="sxs-lookup"><span data-stu-id="68288-259">True</span></span>                                             |
| <span data-ttu-id="68288-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-264">Search-Flags</span></span>           | <span data-ttu-id="68288-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-265">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-266">System-Flags</span></span>           | <span data-ttu-id="68288-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-267">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-268">Classes used in</span></span>        | [<span data-ttu-id="68288-269">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="68288-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68288-270">Windows Server 2012</span></span>



| <span data-ttu-id="68288-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="68288-271">Entry</span></span> | <span data-ttu-id="68288-272">Значение</span><span class="sxs-lookup"><span data-stu-id="68288-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="68288-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="68288-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68288-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="68288-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="68288-275">System-Only</span></span>            | <span data-ttu-id="68288-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-276">False</span></span>                                            |
| <span data-ttu-id="68288-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="68288-277">Is-Single-Valued</span></span>       | <span data-ttu-id="68288-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-278">False</span></span>                                            |
| <span data-ttu-id="68288-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="68288-279">Is Indexed</span></span>             | <span data-ttu-id="68288-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="68288-280">False</span></span>                                            |
| <span data-ttu-id="68288-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="68288-281">In Global Catalog</span></span>      | <span data-ttu-id="68288-282">True</span><span class="sxs-lookup"><span data-stu-id="68288-282">True</span></span>                                             |
| <span data-ttu-id="68288-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="68288-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="68288-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="68288-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="68288-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68288-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="68288-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68288-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="68288-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-287">Search-Flags</span></span>           | <span data-ttu-id="68288-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68288-288">0x00000000</span></span>                                       |
| <span data-ttu-id="68288-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68288-289">System-Flags</span></span>           | <span data-ttu-id="68288-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68288-290">0x00000010</span></span>                                       |
| <span data-ttu-id="68288-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="68288-291">Classes used in</span></span>        | [<span data-ttu-id="68288-292">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="68288-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





