---
title: Allowed-Child-classes-эффективный атрибут
description: Список классов, которые можно изменить.
ms.assetid: e7c30918-3aac-4c08-bd98-60ddc704769f
ms.tgt_platform: multiple
keywords:
- Allowed-Child-classes — эффективная схема AD атрибута
- Схема AD атрибута Алловедчилдклассесеффективе
topic_type:
- apiref
api_name:
- Allowed-Child-Classes-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ead0a7f8e03b545d28c5f4c3bf266c3acba54
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893989"
---
# <a name="allowed-child-classes-effective-attribute"></a><span data-ttu-id="cc4d1-105">Allowed-Child-classes-эффективный атрибут</span><span class="sxs-lookup"><span data-stu-id="cc4d1-105">Allowed-Child-Classes-Effective attribute</span></span>

<span data-ttu-id="cc4d1-106">Список классов, которые можно изменить.</span><span class="sxs-lookup"><span data-stu-id="cc4d1-106">A list of classes that can be modified.</span></span>



| <span data-ttu-id="cc4d1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-107">Entry</span></span> | <span data-ttu-id="cc4d1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cc4d1-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc4d1-109">CN</span></span>                | <span data-ttu-id="cc4d1-110">Allowed-Child-classes-эффективен</span><span class="sxs-lookup"><span data-stu-id="cc4d1-110">Allowed-Child-Classes-Effective</span></span>                                 |
| <span data-ttu-id="cc4d1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cc4d1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc4d1-112">алловедчилдклассесеффективе</span><span class="sxs-lookup"><span data-stu-id="cc4d1-112">allowedChildClassesEffective</span></span>                                    |
| <span data-ttu-id="cc4d1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cc4d1-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="cc4d1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cc4d1-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="cc4d1-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cc4d1-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="cc4d1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-116">Attribute-Id</span></span>      | <span data-ttu-id="cc4d1-117">1.2.840.113556.1.4.912</span><span class="sxs-lookup"><span data-stu-id="cc4d1-117">1.2.840.113556.1.4.912</span></span>                                          |
| <span data-ttu-id="cc4d1-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cc4d1-118">System-Id-Guid</span></span>    | <span data-ttu-id="cc4d1-119">9a7ad943-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="cc4d1-119">9a7ad943-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="cc4d1-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc4d1-120">Syntax</span></span>            | [<span data-ttu-id="cc4d1-121">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="cc4d1-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cc4d1-122">Implementations</span></span>

-   [<span data-ttu-id="cc4d1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc4d1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc4d1-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cc4d1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc4d1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc4d1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc4d1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc4d1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc4d1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="cc4d1-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-131">Entry</span></span> | <span data-ttu-id="cc4d1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-135">System-Only</span></span>            | <span data-ttu-id="cc4d1-136">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-136">True</span></span>                            |
| <span data-ttu-id="cc4d1-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-138">False</span></span>                           |
| <span data-ttu-id="cc4d1-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-139">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-140">False</span></span>                           |
| <span data-ttu-id="cc4d1-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-141">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-142">False</span></span>                           |
| <span data-ttu-id="cc4d1-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-147">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-148">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-149">System-Flags</span></span>           | <span data-ttu-id="cc4d1-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-150">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-151">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cc4d1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc4d1-153">Windows Server 2003</span></span>



| <span data-ttu-id="cc4d1-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-154">Entry</span></span> | <span data-ttu-id="cc4d1-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-158">System-Only</span></span>            | <span data-ttu-id="cc4d1-159">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-159">True</span></span>                            |
| <span data-ttu-id="cc4d1-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-161">False</span></span>                           |
| <span data-ttu-id="cc4d1-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-162">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-163">False</span></span>                           |
| <span data-ttu-id="cc4d1-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-164">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-165">False</span></span>                           |
| <span data-ttu-id="cc4d1-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-170">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-171">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-172">System-Flags</span></span>           | <span data-ttu-id="cc4d1-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-173">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-174">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cc4d1-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="cc4d1-176">ADAM</span></span>



| <span data-ttu-id="cc4d1-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-177">Entry</span></span> | <span data-ttu-id="cc4d1-178">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-181">System-Only</span></span>            | <span data-ttu-id="cc4d1-182">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-182">True</span></span>                            |
| <span data-ttu-id="cc4d1-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-184">False</span></span>                           |
| <span data-ttu-id="cc4d1-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-185">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-186">False</span></span>                           |
| <span data-ttu-id="cc4d1-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-187">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-188">False</span></span>                           |
| <span data-ttu-id="cc4d1-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-193">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-194">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-195">System-Flags</span></span>           | <span data-ttu-id="cc4d1-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-196">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-197">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc4d1-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc4d1-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc4d1-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-200">Entry</span></span> | <span data-ttu-id="cc4d1-201">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-204">System-Only</span></span>            | <span data-ttu-id="cc4d1-205">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-205">True</span></span>                            |
| <span data-ttu-id="cc4d1-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-207">False</span></span>                           |
| <span data-ttu-id="cc4d1-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-208">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-209">False</span></span>                           |
| <span data-ttu-id="cc4d1-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-210">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-211">False</span></span>                           |
| <span data-ttu-id="cc4d1-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-216">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-217">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-218">System-Flags</span></span>           | <span data-ttu-id="cc4d1-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-219">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-220">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc4d1-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc4d1-222">Windows Server 2008</span></span>



| <span data-ttu-id="cc4d1-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-223">Entry</span></span> | <span data-ttu-id="cc4d1-224">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-227">System-Only</span></span>            | <span data-ttu-id="cc4d1-228">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-228">True</span></span>                            |
| <span data-ttu-id="cc4d1-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-230">False</span></span>                           |
| <span data-ttu-id="cc4d1-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-231">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-232">False</span></span>                           |
| <span data-ttu-id="cc4d1-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-233">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-234">False</span></span>                           |
| <span data-ttu-id="cc4d1-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-239">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-240">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-241">System-Flags</span></span>           | <span data-ttu-id="cc4d1-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-242">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-243">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc4d1-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc4d1-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc4d1-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-246">Entry</span></span> | <span data-ttu-id="cc4d1-247">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-250">System-Only</span></span>            | <span data-ttu-id="cc4d1-251">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-251">True</span></span>                            |
| <span data-ttu-id="cc4d1-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-253">False</span></span>                           |
| <span data-ttu-id="cc4d1-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-254">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-255">False</span></span>                           |
| <span data-ttu-id="cc4d1-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-256">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-257">False</span></span>                           |
| <span data-ttu-id="cc4d1-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-262">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-263">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-264">System-Flags</span></span>           | <span data-ttu-id="cc4d1-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-265">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-266">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc4d1-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc4d1-268">Windows Server 2012</span></span>



| <span data-ttu-id="cc4d1-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc4d1-269">Entry</span></span> | <span data-ttu-id="cc4d1-270">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d1-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc4d1-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc4d1-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc4d1-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc4d1-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc4d1-273">System-Only</span></span>            | <span data-ttu-id="cc4d1-274">True</span><span class="sxs-lookup"><span data-stu-id="cc4d1-274">True</span></span>                            |
| <span data-ttu-id="cc4d1-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc4d1-275">Is-Single-Valued</span></span>       | <span data-ttu-id="cc4d1-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-276">False</span></span>                           |
| <span data-ttu-id="cc4d1-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc4d1-277">Is Indexed</span></span>             | <span data-ttu-id="cc4d1-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-278">False</span></span>                           |
| <span data-ttu-id="cc4d1-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc4d1-279">In Global Catalog</span></span>      | <span data-ttu-id="cc4d1-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc4d1-280">False</span></span>                           |
| <span data-ttu-id="cc4d1-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc4d1-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc4d1-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc4d1-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc4d1-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc4d1-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc4d1-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc4d1-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-285">Search-Flags</span></span>           | <span data-ttu-id="cc4d1-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc4d1-286">0x00000000</span></span>                      |
| <span data-ttu-id="cc4d1-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc4d1-287">System-Flags</span></span>           | <span data-ttu-id="cc4d1-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc4d1-288">0x08000014</span></span>                      |
| <span data-ttu-id="cc4d1-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc4d1-289">Classes used in</span></span>        | [<span data-ttu-id="cc4d1-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="cc4d1-290">**Top**</span></span>](c-top.md)<br/> |



 

 





