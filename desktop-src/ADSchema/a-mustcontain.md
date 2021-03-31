---
title: Атрибут Must-Contain
description: Список обязательных атрибутов для класса. Эти атрибуты должны быть указаны при создании экземпляра класса.
ms.assetid: ad112640-0e99-453a-8eff-f964419d8631
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Must-Contain
- Схема AD атрибута mustContain
topic_type:
- apiref
api_name:
- Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791468691f438d01161f0d6252f7b995fc0f51e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804594"
---
# <a name="must-contain-attribute"></a><span data-ttu-id="6210c-106">Атрибут Must-Contain</span><span class="sxs-lookup"><span data-stu-id="6210c-106">Must-Contain attribute</span></span>

<span data-ttu-id="6210c-107">Список обязательных атрибутов для класса.</span><span class="sxs-lookup"><span data-stu-id="6210c-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="6210c-108">Эти атрибуты должны быть указаны при создании экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="6210c-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="6210c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-109">Entry</span></span> | <span data-ttu-id="6210c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6210c-111">CN</span><span class="sxs-lookup"><span data-stu-id="6210c-111">CN</span></span>                | <span data-ttu-id="6210c-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="6210c-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="6210c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6210c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6210c-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="6210c-114">mustContain</span></span>                                                     |
| <span data-ttu-id="6210c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="6210c-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="6210c-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6210c-116">Update Privilege</span></span>  | <span data-ttu-id="6210c-117">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="6210c-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="6210c-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6210c-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="6210c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-119">Attribute-Id</span></span>      | <span data-ttu-id="6210c-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="6210c-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="6210c-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6210c-121">System-Id-Guid</span></span>    | <span data-ttu-id="6210c-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6210c-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="6210c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6210c-123">Syntax</span></span>            | [<span data-ttu-id="6210c-124">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="6210c-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="6210c-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6210c-125">Implementations</span></span>

-   [<span data-ttu-id="6210c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6210c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6210c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6210c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6210c-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6210c-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6210c-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6210c-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6210c-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6210c-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6210c-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6210c-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6210c-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6210c-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6210c-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6210c-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6210c-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-134">Entry</span></span> | <span data-ttu-id="6210c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-138">System-Only</span></span>            | <span data-ttu-id="6210c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-139">False</span></span>                                            |
| <span data-ttu-id="6210c-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-141">False</span></span>                                            |
| <span data-ttu-id="6210c-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-142">Is Indexed</span></span>             | <span data-ttu-id="6210c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-143">False</span></span>                                            |
| <span data-ttu-id="6210c-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-144">In Global Catalog</span></span>      | <span data-ttu-id="6210c-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-145">False</span></span>                                            |
| <span data-ttu-id="6210c-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-150">Search-Flags</span></span>           | <span data-ttu-id="6210c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-151">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-152">System-Flags</span></span>           | <span data-ttu-id="6210c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-153">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-154">Classes used in</span></span>        | [<span data-ttu-id="6210c-155">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6210c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6210c-156">Windows Server 2003</span></span>



| <span data-ttu-id="6210c-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-157">Entry</span></span> | <span data-ttu-id="6210c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-161">System-Only</span></span>            | <span data-ttu-id="6210c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-162">False</span></span>                                            |
| <span data-ttu-id="6210c-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-164">False</span></span>                                            |
| <span data-ttu-id="6210c-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-165">Is Indexed</span></span>             | <span data-ttu-id="6210c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-166">False</span></span>                                            |
| <span data-ttu-id="6210c-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-167">In Global Catalog</span></span>      | <span data-ttu-id="6210c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-168">False</span></span>                                            |
| <span data-ttu-id="6210c-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-173">Search-Flags</span></span>           | <span data-ttu-id="6210c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-174">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-175">System-Flags</span></span>           | <span data-ttu-id="6210c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-176">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-177">Classes used in</span></span>        | [<span data-ttu-id="6210c-178">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6210c-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="6210c-179">ADAM</span></span>



| <span data-ttu-id="6210c-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-180">Entry</span></span> | <span data-ttu-id="6210c-181">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-184">System-Only</span></span>            | <span data-ttu-id="6210c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-185">False</span></span>                                            |
| <span data-ttu-id="6210c-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-187">False</span></span>                                            |
| <span data-ttu-id="6210c-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-188">Is Indexed</span></span>             | <span data-ttu-id="6210c-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-189">False</span></span>                                            |
| <span data-ttu-id="6210c-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-190">In Global Catalog</span></span>      | <span data-ttu-id="6210c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-191">False</span></span>                                            |
| <span data-ttu-id="6210c-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-196">Search-Flags</span></span>           | <span data-ttu-id="6210c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-197">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-198">System-Flags</span></span>           | <span data-ttu-id="6210c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-199">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-200">Classes used in</span></span>        | [<span data-ttu-id="6210c-201">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6210c-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6210c-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6210c-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-203">Entry</span></span> | <span data-ttu-id="6210c-204">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-207">System-Only</span></span>            | <span data-ttu-id="6210c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-208">False</span></span>                                            |
| <span data-ttu-id="6210c-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-210">False</span></span>                                            |
| <span data-ttu-id="6210c-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-211">Is Indexed</span></span>             | <span data-ttu-id="6210c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-212">False</span></span>                                            |
| <span data-ttu-id="6210c-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-213">In Global Catalog</span></span>      | <span data-ttu-id="6210c-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-214">False</span></span>                                            |
| <span data-ttu-id="6210c-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-219">Search-Flags</span></span>           | <span data-ttu-id="6210c-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-220">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-221">System-Flags</span></span>           | <span data-ttu-id="6210c-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-222">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-223">Classes used in</span></span>        | [<span data-ttu-id="6210c-224">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6210c-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6210c-225">Windows Server 2008</span></span>



| <span data-ttu-id="6210c-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-226">Entry</span></span> | <span data-ttu-id="6210c-227">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-230">System-Only</span></span>            | <span data-ttu-id="6210c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-231">False</span></span>                                            |
| <span data-ttu-id="6210c-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-233">False</span></span>                                            |
| <span data-ttu-id="6210c-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-234">Is Indexed</span></span>             | <span data-ttu-id="6210c-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-235">False</span></span>                                            |
| <span data-ttu-id="6210c-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-236">In Global Catalog</span></span>      | <span data-ttu-id="6210c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-237">False</span></span>                                            |
| <span data-ttu-id="6210c-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-242">Search-Flags</span></span>           | <span data-ttu-id="6210c-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-243">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-244">System-Flags</span></span>           | <span data-ttu-id="6210c-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-245">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-246">Classes used in</span></span>        | [<span data-ttu-id="6210c-247">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6210c-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6210c-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6210c-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-249">Entry</span></span> | <span data-ttu-id="6210c-250">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-253">System-Only</span></span>            | <span data-ttu-id="6210c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-254">False</span></span>                                            |
| <span data-ttu-id="6210c-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-256">False</span></span>                                            |
| <span data-ttu-id="6210c-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-257">Is Indexed</span></span>             | <span data-ttu-id="6210c-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-258">False</span></span>                                            |
| <span data-ttu-id="6210c-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-259">In Global Catalog</span></span>      | <span data-ttu-id="6210c-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-260">False</span></span>                                            |
| <span data-ttu-id="6210c-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-265">Search-Flags</span></span>           | <span data-ttu-id="6210c-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-266">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-267">System-Flags</span></span>           | <span data-ttu-id="6210c-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-268">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-269">Classes used in</span></span>        | [<span data-ttu-id="6210c-270">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6210c-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6210c-271">Windows Server 2012</span></span>



| <span data-ttu-id="6210c-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="6210c-272">Entry</span></span> | <span data-ttu-id="6210c-273">Значение</span><span class="sxs-lookup"><span data-stu-id="6210c-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6210c-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6210c-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6210c-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6210c-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="6210c-276">System-Only</span></span>            | <span data-ttu-id="6210c-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-277">False</span></span>                                            |
| <span data-ttu-id="6210c-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6210c-278">Is-Single-Valued</span></span>       | <span data-ttu-id="6210c-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-279">False</span></span>                                            |
| <span data-ttu-id="6210c-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6210c-280">Is Indexed</span></span>             | <span data-ttu-id="6210c-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-281">False</span></span>                                            |
| <span data-ttu-id="6210c-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6210c-282">In Global Catalog</span></span>      | <span data-ttu-id="6210c-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="6210c-283">False</span></span>                                            |
| <span data-ttu-id="6210c-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6210c-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="6210c-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6210c-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6210c-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6210c-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6210c-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6210c-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6210c-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-288">Search-Flags</span></span>           | <span data-ttu-id="6210c-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6210c-289">0x00000000</span></span>                                       |
| <span data-ttu-id="6210c-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6210c-290">System-Flags</span></span>           | <span data-ttu-id="6210c-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6210c-291">0x00000010</span></span>                                       |
| <span data-ttu-id="6210c-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6210c-292">Classes used in</span></span>        | [<span data-ttu-id="6210c-293">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6210c-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





