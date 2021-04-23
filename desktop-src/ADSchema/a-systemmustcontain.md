---
title: System-должен-содержать атрибут
description: Список обязательных атрибутов для класса. Эти атрибуты должны быть указаны при создании экземпляра класса. Список атрибутов может быть изменен только системой.
ms.assetid: 5131bd16-1a8d-4d4a-98e4-6140438c6517
ms.tgt_platform: multiple
keywords:
- System-должен содержать схему AD атрибута
- Схема AD атрибута Системмустконтаин
topic_type:
- apiref
api_name:
- System-Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8d36419ca7e6cd24422645579fb7f9ecc69457
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536125"
---
# <a name="system-must-contain-attribute"></a><span data-ttu-id="37349-107">System-должен-содержать атрибут</span><span class="sxs-lookup"><span data-stu-id="37349-107">System-Must-Contain attribute</span></span>

<span data-ttu-id="37349-108">Список обязательных атрибутов для класса.</span><span class="sxs-lookup"><span data-stu-id="37349-108">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="37349-109">Эти атрибуты должны быть указаны при создании экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="37349-109">These attributes must be specified when an instance of the class is created.</span></span> <span data-ttu-id="37349-110">Список атрибутов может быть изменен только системой.</span><span class="sxs-lookup"><span data-stu-id="37349-110">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="37349-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-111">Entry</span></span> | <span data-ttu-id="37349-112">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-112">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="37349-113">CN</span><span class="sxs-lookup"><span data-stu-id="37349-113">CN</span></span>                | <span data-ttu-id="37349-114">System — должно содержать</span><span class="sxs-lookup"><span data-stu-id="37349-114">System-Must-Contain</span></span>                                                           |
| <span data-ttu-id="37349-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="37349-115">Ldap-Display-Name</span></span> | <span data-ttu-id="37349-116">системмустконтаин</span><span class="sxs-lookup"><span data-stu-id="37349-116">systemMustContain</span></span>                                                             |
| <span data-ttu-id="37349-117">Размер</span><span class="sxs-lookup"><span data-stu-id="37349-117">Size</span></span>              | \-                                                                            |
| <span data-ttu-id="37349-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="37349-118">Update Privilege</span></span>  | <span data-ttu-id="37349-119">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="37349-119">Schema administrator</span></span>                                                          |
| <span data-ttu-id="37349-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="37349-120">Update Frequency</span></span>  | <span data-ttu-id="37349-121">При создании класса или добавлении нового обязательного атрибута в класс.</span><span class="sxs-lookup"><span data-stu-id="37349-121">When the class is created or a new mandatory attribute is added to the class.</span></span> |
| <span data-ttu-id="37349-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37349-122">Attribute-Id</span></span>      | <span data-ttu-id="37349-123">1.2.840.113556.1.4.197</span><span class="sxs-lookup"><span data-stu-id="37349-123">1.2.840.113556.1.4.197</span></span>                                                        |
| <span data-ttu-id="37349-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="37349-124">System-Id-Guid</span></span>    | <span data-ttu-id="37349-125">bf967a45-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="37349-125">bf967a45-0de6-11d0-a285-00aa003049e2</span></span>                                          |
| <span data-ttu-id="37349-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37349-126">Syntax</span></span>            | [<span data-ttu-id="37349-127">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="37349-127">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)               |



## <a name="implementations"></a><span data-ttu-id="37349-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="37349-128">Implementations</span></span>

-   [<span data-ttu-id="37349-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37349-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37349-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37349-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37349-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="37349-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="37349-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37349-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37349-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37349-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37349-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37349-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37349-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37349-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37349-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37349-136">Windows 2000 Server</span></span>



| <span data-ttu-id="37349-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-137">Entry</span></span> | <span data-ttu-id="37349-138">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-138">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-139">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-140">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-141">System-Only</span></span>            | <span data-ttu-id="37349-142">True</span><span class="sxs-lookup"><span data-stu-id="37349-142">True</span></span>                                             |
| <span data-ttu-id="37349-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-143">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-144">False</span></span>                                            |
| <span data-ttu-id="37349-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-145">Is Indexed</span></span>             | <span data-ttu-id="37349-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-146">False</span></span>                                            |
| <span data-ttu-id="37349-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-147">In Global Catalog</span></span>      | <span data-ttu-id="37349-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-148">False</span></span>                                            |
| <span data-ttu-id="37349-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-151">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-152">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-153">Search-Flags</span></span>           | <span data-ttu-id="37349-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-154">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-155">System-Flags</span></span>           | <span data-ttu-id="37349-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-156">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-157">Classes used in</span></span>        | [<span data-ttu-id="37349-158">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37349-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37349-159">Windows Server 2003</span></span>



| <span data-ttu-id="37349-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-160">Entry</span></span> | <span data-ttu-id="37349-161">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-161">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-162">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-163">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-164">System-Only</span></span>            | <span data-ttu-id="37349-165">True</span><span class="sxs-lookup"><span data-stu-id="37349-165">True</span></span>                                             |
| <span data-ttu-id="37349-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-166">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-167">False</span></span>                                            |
| <span data-ttu-id="37349-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-168">Is Indexed</span></span>             | <span data-ttu-id="37349-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-169">False</span></span>                                            |
| <span data-ttu-id="37349-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-170">In Global Catalog</span></span>      | <span data-ttu-id="37349-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-171">False</span></span>                                            |
| <span data-ttu-id="37349-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-176">Search-Flags</span></span>           | <span data-ttu-id="37349-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-177">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-178">System-Flags</span></span>           | <span data-ttu-id="37349-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-179">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-180">Classes used in</span></span>        | [<span data-ttu-id="37349-181">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-181">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="37349-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="37349-182">ADAM</span></span>



| <span data-ttu-id="37349-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-183">Entry</span></span> | <span data-ttu-id="37349-184">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-186">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-187">System-Only</span></span>            | <span data-ttu-id="37349-188">True</span><span class="sxs-lookup"><span data-stu-id="37349-188">True</span></span>                                             |
| <span data-ttu-id="37349-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-189">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-190">False</span></span>                                            |
| <span data-ttu-id="37349-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-191">Is Indexed</span></span>             | <span data-ttu-id="37349-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-192">False</span></span>                                            |
| <span data-ttu-id="37349-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-193">In Global Catalog</span></span>      | <span data-ttu-id="37349-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-194">False</span></span>                                            |
| <span data-ttu-id="37349-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-196">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-197">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-198">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-199">Search-Flags</span></span>           | <span data-ttu-id="37349-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-200">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-201">System-Flags</span></span>           | <span data-ttu-id="37349-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-202">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-203">Classes used in</span></span>        | [<span data-ttu-id="37349-204">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37349-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37349-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37349-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-206">Entry</span></span> | <span data-ttu-id="37349-207">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-207">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-208">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-209">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-210">System-Only</span></span>            | <span data-ttu-id="37349-211">True</span><span class="sxs-lookup"><span data-stu-id="37349-211">True</span></span>                                             |
| <span data-ttu-id="37349-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-212">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-213">False</span></span>                                            |
| <span data-ttu-id="37349-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-214">Is Indexed</span></span>             | <span data-ttu-id="37349-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-215">False</span></span>                                            |
| <span data-ttu-id="37349-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-216">In Global Catalog</span></span>      | <span data-ttu-id="37349-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-217">False</span></span>                                            |
| <span data-ttu-id="37349-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-219">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-220">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-221">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-222">Search-Flags</span></span>           | <span data-ttu-id="37349-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-223">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-224">System-Flags</span></span>           | <span data-ttu-id="37349-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-225">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-226">Classes used in</span></span>        | [<span data-ttu-id="37349-227">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-227">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37349-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37349-228">Windows Server 2008</span></span>



| <span data-ttu-id="37349-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-229">Entry</span></span> | <span data-ttu-id="37349-230">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-230">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-231">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-232">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-233">System-Only</span></span>            | <span data-ttu-id="37349-234">True</span><span class="sxs-lookup"><span data-stu-id="37349-234">True</span></span>                                             |
| <span data-ttu-id="37349-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-235">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-236">False</span></span>                                            |
| <span data-ttu-id="37349-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-237">Is Indexed</span></span>             | <span data-ttu-id="37349-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-238">False</span></span>                                            |
| <span data-ttu-id="37349-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-239">In Global Catalog</span></span>      | <span data-ttu-id="37349-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-240">False</span></span>                                            |
| <span data-ttu-id="37349-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-242">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-243">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-244">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-245">Search-Flags</span></span>           | <span data-ttu-id="37349-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-246">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-247">System-Flags</span></span>           | <span data-ttu-id="37349-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-248">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-249">Classes used in</span></span>        | [<span data-ttu-id="37349-250">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-250">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37349-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37349-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37349-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-252">Entry</span></span> | <span data-ttu-id="37349-253">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-253">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-254">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-255">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-256">System-Only</span></span>            | <span data-ttu-id="37349-257">True</span><span class="sxs-lookup"><span data-stu-id="37349-257">True</span></span>                                             |
| <span data-ttu-id="37349-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-258">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-259">False</span></span>                                            |
| <span data-ttu-id="37349-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-260">Is Indexed</span></span>             | <span data-ttu-id="37349-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-261">False</span></span>                                            |
| <span data-ttu-id="37349-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-262">In Global Catalog</span></span>      | <span data-ttu-id="37349-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-263">False</span></span>                                            |
| <span data-ttu-id="37349-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-265">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-266">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-267">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-268">Search-Flags</span></span>           | <span data-ttu-id="37349-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-269">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-270">System-Flags</span></span>           | <span data-ttu-id="37349-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-271">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-272">Classes used in</span></span>        | [<span data-ttu-id="37349-273">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-273">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37349-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37349-274">Windows Server 2012</span></span>



| <span data-ttu-id="37349-275">Ввод</span><span class="sxs-lookup"><span data-stu-id="37349-275">Entry</span></span> | <span data-ttu-id="37349-276">Значение</span><span class="sxs-lookup"><span data-stu-id="37349-276">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="37349-277">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="37349-277">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37349-278">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="37349-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="37349-279">System-Only</span></span>            | <span data-ttu-id="37349-280">True</span><span class="sxs-lookup"><span data-stu-id="37349-280">True</span></span>                                             |
| <span data-ttu-id="37349-281">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="37349-281">Is-Single-Valued</span></span>       | <span data-ttu-id="37349-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-282">False</span></span>                                            |
| <span data-ttu-id="37349-283">Индексируется</span><span class="sxs-lookup"><span data-stu-id="37349-283">Is Indexed</span></span>             | <span data-ttu-id="37349-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-284">False</span></span>                                            |
| <span data-ttu-id="37349-285">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="37349-285">In Global Catalog</span></span>      | <span data-ttu-id="37349-286">Неверно</span><span class="sxs-lookup"><span data-stu-id="37349-286">False</span></span>                                            |
| <span data-ttu-id="37349-287">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="37349-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="37349-288">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="37349-288">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="37349-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37349-289">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="37349-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37349-290">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="37349-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-291">Search-Flags</span></span>           | <span data-ttu-id="37349-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37349-292">0x00000000</span></span>                                       |
| <span data-ttu-id="37349-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37349-293">System-Flags</span></span>           | <span data-ttu-id="37349-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37349-294">0x00000010</span></span>                                       |
| <span data-ttu-id="37349-295">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="37349-295">Classes used in</span></span>        | [<span data-ttu-id="37349-296">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="37349-296">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





