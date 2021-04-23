---
title: Атрибут System-ПОСС-старший
description: Список классов, которые могут содержать этот класс. Этот список может быть изменен только системой.
ms.assetid: 8b98249a-fe9a-4a42-abb8-a8b042250a76
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута System-ПОСС-превосходно
- Схема AD атрибута Системпосссупериорс
topic_type:
- apiref
api_name:
- System-Poss-Superiors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2116dfb8d2ad21d8a52854b1eb98ef156eb46a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893641"
---
# <a name="system-poss-superiors-attribute"></a><span data-ttu-id="13d85-106">Атрибут System-ПОСС-старший</span><span class="sxs-lookup"><span data-stu-id="13d85-106">System-Poss-Superiors attribute</span></span>

<span data-ttu-id="13d85-107">Список классов, которые могут содержать этот класс.</span><span class="sxs-lookup"><span data-stu-id="13d85-107">The list of classes that can contain this class.</span></span> <span data-ttu-id="13d85-108">Этот список может быть изменен только системой.</span><span class="sxs-lookup"><span data-stu-id="13d85-108">This list can only be modified by the system.</span></span>



| <span data-ttu-id="13d85-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-109">Entry</span></span> | <span data-ttu-id="13d85-110">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="13d85-111">CN</span><span class="sxs-lookup"><span data-stu-id="13d85-111">CN</span></span>                | <span data-ttu-id="13d85-112">System-ПОСС-старший</span><span class="sxs-lookup"><span data-stu-id="13d85-112">System-Poss-Superiors</span></span>                                                       |
| <span data-ttu-id="13d85-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="13d85-113">Ldap-Display-Name</span></span> | <span data-ttu-id="13d85-114">системпосссупериорс</span><span class="sxs-lookup"><span data-stu-id="13d85-114">systemPossSuperiors</span></span>                                                         |
| <span data-ttu-id="13d85-115">Размер</span><span class="sxs-lookup"><span data-stu-id="13d85-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="13d85-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="13d85-116">Update Privilege</span></span>  | <span data-ttu-id="13d85-117">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="13d85-117">Schema administrator</span></span>                                                        |
| <span data-ttu-id="13d85-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="13d85-118">Update Frequency</span></span>  | <span data-ttu-id="13d85-119">При создании класса или добавлении к классу нового возможного старшего элемента.</span><span class="sxs-lookup"><span data-stu-id="13d85-119">When the class is created or a new possible superior is added to the class.</span></span> |
| <span data-ttu-id="13d85-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-120">Attribute-Id</span></span>      | <span data-ttu-id="13d85-121">1.2.840.113556.1.4.195</span><span class="sxs-lookup"><span data-stu-id="13d85-121">1.2.840.113556.1.4.195</span></span>                                                      |
| <span data-ttu-id="13d85-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="13d85-122">System-Id-Guid</span></span>    | <span data-ttu-id="13d85-123">bf967a47-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="13d85-123">bf967a47-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="13d85-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13d85-124">Syntax</span></span>            | [<span data-ttu-id="13d85-125">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="13d85-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)             |



## <a name="implementations"></a><span data-ttu-id="13d85-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="13d85-126">Implementations</span></span>

-   [<span data-ttu-id="13d85-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13d85-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13d85-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13d85-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13d85-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="13d85-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="13d85-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13d85-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13d85-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13d85-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13d85-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13d85-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13d85-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13d85-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13d85-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13d85-134">Windows 2000 Server</span></span>



| <span data-ttu-id="13d85-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-135">Entry</span></span> | <span data-ttu-id="13d85-136">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-139">System-Only</span></span>            | <span data-ttu-id="13d85-140">True</span><span class="sxs-lookup"><span data-stu-id="13d85-140">True</span></span>                                             |
| <span data-ttu-id="13d85-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-141">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-142">False</span></span>                                            |
| <span data-ttu-id="13d85-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-143">Is Indexed</span></span>             | <span data-ttu-id="13d85-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-144">False</span></span>                                            |
| <span data-ttu-id="13d85-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-145">In Global Catalog</span></span>      | <span data-ttu-id="13d85-146">True</span><span class="sxs-lookup"><span data-stu-id="13d85-146">True</span></span>                                             |
| <span data-ttu-id="13d85-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-151">Search-Flags</span></span>           | <span data-ttu-id="13d85-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-152">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-153">System-Flags</span></span>           | <span data-ttu-id="13d85-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d85-154">0x00000010</span></span>                                       |
| <span data-ttu-id="13d85-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-155">Classes used in</span></span>        | [<span data-ttu-id="13d85-156">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13d85-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13d85-157">Windows Server 2003</span></span>



| <span data-ttu-id="13d85-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-158">Entry</span></span> | <span data-ttu-id="13d85-159">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-162">System-Only</span></span>            | <span data-ttu-id="13d85-163">True</span><span class="sxs-lookup"><span data-stu-id="13d85-163">True</span></span>                                             |
| <span data-ttu-id="13d85-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-164">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-165">False</span></span>                                            |
| <span data-ttu-id="13d85-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-166">Is Indexed</span></span>             | <span data-ttu-id="13d85-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-167">False</span></span>                                            |
| <span data-ttu-id="13d85-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-168">In Global Catalog</span></span>      | <span data-ttu-id="13d85-169">True</span><span class="sxs-lookup"><span data-stu-id="13d85-169">True</span></span>                                             |
| <span data-ttu-id="13d85-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-174">Search-Flags</span></span>           | <span data-ttu-id="13d85-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-175">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-176">System-Flags</span></span>           | <span data-ttu-id="13d85-177">0x00000012</span><span class="sxs-lookup"><span data-stu-id="13d85-177">0x00000012</span></span>                                       |
| <span data-ttu-id="13d85-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-178">Classes used in</span></span>        | [<span data-ttu-id="13d85-179">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="13d85-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="13d85-180">ADAM</span></span>



| <span data-ttu-id="13d85-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-181">Entry</span></span> | <span data-ttu-id="13d85-182">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-185">System-Only</span></span>            | <span data-ttu-id="13d85-186">True</span><span class="sxs-lookup"><span data-stu-id="13d85-186">True</span></span>                                             |
| <span data-ttu-id="13d85-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-187">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-188">False</span></span>                                            |
| <span data-ttu-id="13d85-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-189">Is Indexed</span></span>             | <span data-ttu-id="13d85-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-190">False</span></span>                                            |
| <span data-ttu-id="13d85-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-191">In Global Catalog</span></span>      | <span data-ttu-id="13d85-192">True</span><span class="sxs-lookup"><span data-stu-id="13d85-192">True</span></span>                                             |
| <span data-ttu-id="13d85-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-197">Search-Flags</span></span>           | <span data-ttu-id="13d85-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-198">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-199">System-Flags</span></span>           | <span data-ttu-id="13d85-200">0x00000012</span><span class="sxs-lookup"><span data-stu-id="13d85-200">0x00000012</span></span>                                       |
| <span data-ttu-id="13d85-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-201">Classes used in</span></span>        | [<span data-ttu-id="13d85-202">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13d85-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13d85-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13d85-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-204">Entry</span></span> | <span data-ttu-id="13d85-205">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-208">System-Only</span></span>            | <span data-ttu-id="13d85-209">True</span><span class="sxs-lookup"><span data-stu-id="13d85-209">True</span></span>                                             |
| <span data-ttu-id="13d85-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-210">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-211">False</span></span>                                            |
| <span data-ttu-id="13d85-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-212">Is Indexed</span></span>             | <span data-ttu-id="13d85-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-213">False</span></span>                                            |
| <span data-ttu-id="13d85-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-214">In Global Catalog</span></span>      | <span data-ttu-id="13d85-215">True</span><span class="sxs-lookup"><span data-stu-id="13d85-215">True</span></span>                                             |
| <span data-ttu-id="13d85-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-220">Search-Flags</span></span>           | <span data-ttu-id="13d85-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-221">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-222">System-Flags</span></span>           | <span data-ttu-id="13d85-223">0x00000012</span><span class="sxs-lookup"><span data-stu-id="13d85-223">0x00000012</span></span>                                       |
| <span data-ttu-id="13d85-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-224">Classes used in</span></span>        | [<span data-ttu-id="13d85-225">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13d85-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13d85-226">Windows Server 2008</span></span>



| <span data-ttu-id="13d85-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-227">Entry</span></span> | <span data-ttu-id="13d85-228">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-231">System-Only</span></span>            | <span data-ttu-id="13d85-232">True</span><span class="sxs-lookup"><span data-stu-id="13d85-232">True</span></span>                                             |
| <span data-ttu-id="13d85-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-233">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-234">False</span></span>                                            |
| <span data-ttu-id="13d85-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-235">Is Indexed</span></span>             | <span data-ttu-id="13d85-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-236">False</span></span>                                            |
| <span data-ttu-id="13d85-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-237">In Global Catalog</span></span>      | <span data-ttu-id="13d85-238">True</span><span class="sxs-lookup"><span data-stu-id="13d85-238">True</span></span>                                             |
| <span data-ttu-id="13d85-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-243">Search-Flags</span></span>           | <span data-ttu-id="13d85-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-244">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-245">System-Flags</span></span>           | <span data-ttu-id="13d85-246">0x00000012</span><span class="sxs-lookup"><span data-stu-id="13d85-246">0x00000012</span></span>                                       |
| <span data-ttu-id="13d85-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-247">Classes used in</span></span>        | [<span data-ttu-id="13d85-248">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13d85-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13d85-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13d85-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-250">Entry</span></span> | <span data-ttu-id="13d85-251">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-254">System-Only</span></span>            | <span data-ttu-id="13d85-255">True</span><span class="sxs-lookup"><span data-stu-id="13d85-255">True</span></span>                                             |
| <span data-ttu-id="13d85-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-256">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-257">False</span></span>                                            |
| <span data-ttu-id="13d85-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-258">Is Indexed</span></span>             | <span data-ttu-id="13d85-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-259">False</span></span>                                            |
| <span data-ttu-id="13d85-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-260">In Global Catalog</span></span>      | <span data-ttu-id="13d85-261">True</span><span class="sxs-lookup"><span data-stu-id="13d85-261">True</span></span>                                             |
| <span data-ttu-id="13d85-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-266">Search-Flags</span></span>           | <span data-ttu-id="13d85-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-267">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-268">System-Flags</span></span>           | <span data-ttu-id="13d85-269">0x00000012</span><span class="sxs-lookup"><span data-stu-id="13d85-269">0x00000012</span></span>                                       |
| <span data-ttu-id="13d85-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-270">Classes used in</span></span>        | [<span data-ttu-id="13d85-271">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13d85-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13d85-272">Windows Server 2012</span></span>



| <span data-ttu-id="13d85-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="13d85-273">Entry</span></span> | <span data-ttu-id="13d85-274">Значение</span><span class="sxs-lookup"><span data-stu-id="13d85-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="13d85-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13d85-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d85-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="13d85-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d85-277">System-Only</span></span>            | <span data-ttu-id="13d85-278">True</span><span class="sxs-lookup"><span data-stu-id="13d85-278">True</span></span>                                             |
| <span data-ttu-id="13d85-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13d85-279">Is-Single-Valued</span></span>       | <span data-ttu-id="13d85-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-280">False</span></span>                                            |
| <span data-ttu-id="13d85-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13d85-281">Is Indexed</span></span>             | <span data-ttu-id="13d85-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="13d85-282">False</span></span>                                            |
| <span data-ttu-id="13d85-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13d85-283">In Global Catalog</span></span>      | <span data-ttu-id="13d85-284">True</span><span class="sxs-lookup"><span data-stu-id="13d85-284">True</span></span>                                             |
| <span data-ttu-id="13d85-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13d85-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d85-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13d85-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="13d85-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d85-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="13d85-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d85-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="13d85-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-289">Search-Flags</span></span>           | <span data-ttu-id="13d85-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d85-290">0x00000000</span></span>                                       |
| <span data-ttu-id="13d85-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d85-291">System-Flags</span></span>           | <span data-ttu-id="13d85-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="13d85-292">0x00000012</span></span>                                       |
| <span data-ttu-id="13d85-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13d85-293">Classes used in</span></span>        | [<span data-ttu-id="13d85-294">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="13d85-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





