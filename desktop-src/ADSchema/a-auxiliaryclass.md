---
title: Атрибут Auxiliary-Class
description: Список вспомогательных классов, которые будут связаны с этим классом.
ms.assetid: 8c3bb822-222f-4ee2-9da7-820e29e33c9a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Auxiliary-Class
- Схема AD атрибута auxiliaryClass
topic_type:
- apiref
api_name:
- Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b3b633e343a0ca7d43deffee5bda7666a3d144
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654980"
---
# <a name="auxiliary-class-attribute"></a><span data-ttu-id="a8789-105">Атрибут Auxiliary-Class</span><span class="sxs-lookup"><span data-stu-id="a8789-105">Auxiliary-Class attribute</span></span>

<span data-ttu-id="a8789-106">Список вспомогательных классов, которые будут связаны с этим классом.</span><span class="sxs-lookup"><span data-stu-id="a8789-106">The list of auxiliary classes to be associated with this class.</span></span>



| <span data-ttu-id="a8789-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-107">Entry</span></span> | <span data-ttu-id="a8789-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="a8789-109">CN</span><span class="sxs-lookup"><span data-stu-id="a8789-109">CN</span></span>                | <span data-ttu-id="a8789-110">Auxiliary-Class</span><span class="sxs-lookup"><span data-stu-id="a8789-110">Auxiliary-Class</span></span>                                                 |
| <span data-ttu-id="a8789-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a8789-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a8789-112">auxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="a8789-112">auxiliaryClass</span></span>                                                  |
| <span data-ttu-id="a8789-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a8789-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="a8789-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a8789-114">Update Privilege</span></span>  | <span data-ttu-id="a8789-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="a8789-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="a8789-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a8789-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="a8789-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-117">Attribute-Id</span></span>      | <span data-ttu-id="a8789-118">1.2.840.113556.1.2.351</span><span class="sxs-lookup"><span data-stu-id="a8789-118">1.2.840.113556.1.2.351</span></span>                                          |
| <span data-ttu-id="a8789-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a8789-119">System-Id-Guid</span></span>    | <span data-ttu-id="a8789-120">bf96792c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a8789-120">bf96792c-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="a8789-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8789-121">Syntax</span></span>            | [<span data-ttu-id="a8789-122">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="a8789-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="a8789-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a8789-123">Implementations</span></span>

-   [<span data-ttu-id="a8789-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a8789-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a8789-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8789-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8789-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a8789-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a8789-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8789-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8789-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8789-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8789-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8789-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8789-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8789-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a8789-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8789-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a8789-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-132">Entry</span></span> | <span data-ttu-id="a8789-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-136">System-Only</span></span>            | <span data-ttu-id="a8789-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-137">False</span></span>                                            |
| <span data-ttu-id="a8789-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-139">False</span></span>                                            |
| <span data-ttu-id="a8789-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-140">Is Indexed</span></span>             | <span data-ttu-id="a8789-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-141">False</span></span>                                            |
| <span data-ttu-id="a8789-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-142">In Global Catalog</span></span>      | <span data-ttu-id="a8789-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-143">False</span></span>                                            |
| <span data-ttu-id="a8789-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-148">Search-Flags</span></span>           | <span data-ttu-id="a8789-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-149">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-150">System-Flags</span></span>           | <span data-ttu-id="a8789-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-151">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-152">Classes used in</span></span>        | [<span data-ttu-id="a8789-153">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a8789-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8789-154">Windows Server 2003</span></span>



| <span data-ttu-id="a8789-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-155">Entry</span></span> | <span data-ttu-id="a8789-156">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-159">System-Only</span></span>            | <span data-ttu-id="a8789-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-160">False</span></span>                                            |
| <span data-ttu-id="a8789-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-162">False</span></span>                                            |
| <span data-ttu-id="a8789-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-163">Is Indexed</span></span>             | <span data-ttu-id="a8789-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-164">False</span></span>                                            |
| <span data-ttu-id="a8789-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-165">In Global Catalog</span></span>      | <span data-ttu-id="a8789-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-166">False</span></span>                                            |
| <span data-ttu-id="a8789-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-171">Search-Flags</span></span>           | <span data-ttu-id="a8789-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-172">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-173">System-Flags</span></span>           | <span data-ttu-id="a8789-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-174">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-175">Classes used in</span></span>        | [<span data-ttu-id="a8789-176">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a8789-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="a8789-177">ADAM</span></span>



| <span data-ttu-id="a8789-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-178">Entry</span></span> | <span data-ttu-id="a8789-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-182">System-Only</span></span>            | <span data-ttu-id="a8789-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-183">False</span></span>                                            |
| <span data-ttu-id="a8789-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-185">False</span></span>                                            |
| <span data-ttu-id="a8789-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-186">Is Indexed</span></span>             | <span data-ttu-id="a8789-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-187">False</span></span>                                            |
| <span data-ttu-id="a8789-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-188">In Global Catalog</span></span>      | <span data-ttu-id="a8789-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-189">False</span></span>                                            |
| <span data-ttu-id="a8789-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-194">Search-Flags</span></span>           | <span data-ttu-id="a8789-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-195">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-196">System-Flags</span></span>           | <span data-ttu-id="a8789-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-197">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-198">Classes used in</span></span>        | [<span data-ttu-id="a8789-199">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8789-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8789-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8789-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-201">Entry</span></span> | <span data-ttu-id="a8789-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-205">System-Only</span></span>            | <span data-ttu-id="a8789-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-206">False</span></span>                                            |
| <span data-ttu-id="a8789-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-208">False</span></span>                                            |
| <span data-ttu-id="a8789-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-209">Is Indexed</span></span>             | <span data-ttu-id="a8789-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-210">False</span></span>                                            |
| <span data-ttu-id="a8789-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-211">In Global Catalog</span></span>      | <span data-ttu-id="a8789-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-212">False</span></span>                                            |
| <span data-ttu-id="a8789-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-217">Search-Flags</span></span>           | <span data-ttu-id="a8789-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-218">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-219">System-Flags</span></span>           | <span data-ttu-id="a8789-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-220">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-221">Classes used in</span></span>        | [<span data-ttu-id="a8789-222">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8789-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8789-223">Windows Server 2008</span></span>



| <span data-ttu-id="a8789-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-224">Entry</span></span> | <span data-ttu-id="a8789-225">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-228">System-Only</span></span>            | <span data-ttu-id="a8789-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-229">False</span></span>                                            |
| <span data-ttu-id="a8789-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-231">False</span></span>                                            |
| <span data-ttu-id="a8789-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-232">Is Indexed</span></span>             | <span data-ttu-id="a8789-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-233">False</span></span>                                            |
| <span data-ttu-id="a8789-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-234">In Global Catalog</span></span>      | <span data-ttu-id="a8789-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-235">False</span></span>                                            |
| <span data-ttu-id="a8789-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-240">Search-Flags</span></span>           | <span data-ttu-id="a8789-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-241">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-242">System-Flags</span></span>           | <span data-ttu-id="a8789-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-243">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-244">Classes used in</span></span>        | [<span data-ttu-id="a8789-245">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8789-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8789-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8789-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-247">Entry</span></span> | <span data-ttu-id="a8789-248">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-251">System-Only</span></span>            | <span data-ttu-id="a8789-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-252">False</span></span>                                            |
| <span data-ttu-id="a8789-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-254">False</span></span>                                            |
| <span data-ttu-id="a8789-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-255">Is Indexed</span></span>             | <span data-ttu-id="a8789-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-256">False</span></span>                                            |
| <span data-ttu-id="a8789-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-257">In Global Catalog</span></span>      | <span data-ttu-id="a8789-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-258">False</span></span>                                            |
| <span data-ttu-id="a8789-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-263">Search-Flags</span></span>           | <span data-ttu-id="a8789-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-264">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-265">System-Flags</span></span>           | <span data-ttu-id="a8789-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-266">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-267">Classes used in</span></span>        | [<span data-ttu-id="a8789-268">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8789-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8789-269">Windows Server 2012</span></span>



| <span data-ttu-id="a8789-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8789-270">Entry</span></span> | <span data-ttu-id="a8789-271">Значение</span><span class="sxs-lookup"><span data-stu-id="a8789-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a8789-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a8789-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8789-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a8789-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8789-274">System-Only</span></span>            | <span data-ttu-id="a8789-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-275">False</span></span>                                            |
| <span data-ttu-id="a8789-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a8789-276">Is-Single-Valued</span></span>       | <span data-ttu-id="a8789-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-277">False</span></span>                                            |
| <span data-ttu-id="a8789-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a8789-278">Is Indexed</span></span>             | <span data-ttu-id="a8789-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-279">False</span></span>                                            |
| <span data-ttu-id="a8789-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a8789-280">In Global Catalog</span></span>      | <span data-ttu-id="a8789-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8789-281">False</span></span>                                            |
| <span data-ttu-id="a8789-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a8789-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8789-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a8789-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a8789-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8789-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a8789-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8789-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a8789-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-286">Search-Flags</span></span>           | <span data-ttu-id="a8789-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8789-287">0x00000000</span></span>                                       |
| <span data-ttu-id="a8789-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8789-288">System-Flags</span></span>           | <span data-ttu-id="a8789-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8789-289">0x00000010</span></span>                                       |
| <span data-ttu-id="a8789-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a8789-290">Classes used in</span></span>        | [<span data-ttu-id="a8789-291">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="a8789-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





