---
title: Атрибут Group-Type
description: Содержит набор флагов, определяющих тип и область объекта группы.
ms.assetid: cd37ed2f-8503-4227-b0d2-c8135605cb84
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Group-Type
- Схема AD атрибута groupType
topic_type:
- apiref
api_name:
- Group-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e1db8f102e7e56b38d15d74fedb7c5a5366ee47
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654824"
---
# <a name="group-type-attribute"></a><span data-ttu-id="aa335-105">Атрибут Group-Type</span><span class="sxs-lookup"><span data-stu-id="aa335-105">Group-Type attribute</span></span>

<span data-ttu-id="aa335-106">Содержит набор флагов, определяющих тип и область объекта группы.</span><span class="sxs-lookup"><span data-stu-id="aa335-106">Contains a set of flags that define the type and scope of a group object.</span></span> <span data-ttu-id="aa335-107">Возможные значения для этого атрибута см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="aa335-107">For the possible values for this attribute, see Remarks.</span></span>



| <span data-ttu-id="aa335-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-108">Entry</span></span> | <span data-ttu-id="aa335-109">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="aa335-110">CN</span><span class="sxs-lookup"><span data-stu-id="aa335-110">CN</span></span>                | <span data-ttu-id="aa335-111">Group-Type</span><span class="sxs-lookup"><span data-stu-id="aa335-111">Group-Type</span></span>                           |
| <span data-ttu-id="aa335-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="aa335-112">Ldap-Display-Name</span></span> | <span data-ttu-id="aa335-113">groupType</span><span class="sxs-lookup"><span data-stu-id="aa335-113">groupType</span></span>                            |
| <span data-ttu-id="aa335-114">Размер</span><span class="sxs-lookup"><span data-stu-id="aa335-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="aa335-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="aa335-115">Update Privilege</span></span>  | <span data-ttu-id="aa335-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="aa335-116">Domain administrator</span></span>                 |
| <span data-ttu-id="aa335-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="aa335-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="aa335-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-118">Attribute-Id</span></span>      | <span data-ttu-id="aa335-119">1.2.840.113556.1.4.750</span><span class="sxs-lookup"><span data-stu-id="aa335-119">1.2.840.113556.1.4.750</span></span>               |
| <span data-ttu-id="aa335-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="aa335-120">System-Id-Guid</span></span>    | <span data-ttu-id="aa335-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="aa335-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="aa335-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa335-122">Syntax</span></span>            | [<span data-ttu-id="aa335-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="aa335-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="aa335-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="aa335-124">Implementations</span></span>

-   [<span data-ttu-id="aa335-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aa335-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aa335-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aa335-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aa335-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="aa335-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="aa335-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aa335-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aa335-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aa335-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aa335-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aa335-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aa335-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aa335-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aa335-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa335-132">Windows 2000 Server</span></span>



| <span data-ttu-id="aa335-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-133">Entry</span></span> | <span data-ttu-id="aa335-134">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-134">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-135">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-136">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-137">System-Only</span></span>            | <span data-ttu-id="aa335-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-138">False</span></span>                               |
| <span data-ttu-id="aa335-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-139">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-140">True</span><span class="sxs-lookup"><span data-stu-id="aa335-140">True</span></span>                                |
| <span data-ttu-id="aa335-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-141">Is Indexed</span></span>             | <span data-ttu-id="aa335-142">True</span><span class="sxs-lookup"><span data-stu-id="aa335-142">True</span></span>                                |
| <span data-ttu-id="aa335-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-143">In Global Catalog</span></span>      | <span data-ttu-id="aa335-144">True</span><span class="sxs-lookup"><span data-stu-id="aa335-144">True</span></span>                                |
| <span data-ttu-id="aa335-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-146">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-147">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-148">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-149">Search-Flags</span></span>           | <span data-ttu-id="aa335-150">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-150">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-151">System-Flags</span></span>           | <span data-ttu-id="aa335-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-152">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-153">Classes used in</span></span>        | [<span data-ttu-id="aa335-154">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-154">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aa335-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa335-155">Windows Server 2003</span></span>



| <span data-ttu-id="aa335-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-156">Entry</span></span> | <span data-ttu-id="aa335-157">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-157">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-158">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-160">System-Only</span></span>            | <span data-ttu-id="aa335-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-161">False</span></span>                               |
| <span data-ttu-id="aa335-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-162">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-163">True</span><span class="sxs-lookup"><span data-stu-id="aa335-163">True</span></span>                                |
| <span data-ttu-id="aa335-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-164">Is Indexed</span></span>             | <span data-ttu-id="aa335-165">True</span><span class="sxs-lookup"><span data-stu-id="aa335-165">True</span></span>                                |
| <span data-ttu-id="aa335-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-166">In Global Catalog</span></span>      | <span data-ttu-id="aa335-167">True</span><span class="sxs-lookup"><span data-stu-id="aa335-167">True</span></span>                                |
| <span data-ttu-id="aa335-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-172">Search-Flags</span></span>           | <span data-ttu-id="aa335-173">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-173">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-174">System-Flags</span></span>           | <span data-ttu-id="aa335-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-175">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-176">Classes used in</span></span>        | [<span data-ttu-id="aa335-177">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="aa335-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="aa335-178">ADAM</span></span>



| <span data-ttu-id="aa335-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-179">Entry</span></span> | <span data-ttu-id="aa335-180">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-181">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-182">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-183">System-Only</span></span>            | <span data-ttu-id="aa335-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-184">False</span></span>                               |
| <span data-ttu-id="aa335-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-185">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-186">True</span><span class="sxs-lookup"><span data-stu-id="aa335-186">True</span></span>                                |
| <span data-ttu-id="aa335-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-187">Is Indexed</span></span>             | <span data-ttu-id="aa335-188">True</span><span class="sxs-lookup"><span data-stu-id="aa335-188">True</span></span>                                |
| <span data-ttu-id="aa335-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-189">In Global Catalog</span></span>      | <span data-ttu-id="aa335-190">True</span><span class="sxs-lookup"><span data-stu-id="aa335-190">True</span></span>                                |
| <span data-ttu-id="aa335-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-192">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-193">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-194">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-195">Search-Flags</span></span>           | <span data-ttu-id="aa335-196">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-196">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-197">System-Flags</span></span>           | <span data-ttu-id="aa335-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-198">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-199">Classes used in</span></span>        | [<span data-ttu-id="aa335-200">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-200">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aa335-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aa335-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aa335-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-202">Entry</span></span> | <span data-ttu-id="aa335-203">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-203">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-204">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-205">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-206">System-Only</span></span>            | <span data-ttu-id="aa335-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-207">False</span></span>                               |
| <span data-ttu-id="aa335-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-208">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-209">True</span><span class="sxs-lookup"><span data-stu-id="aa335-209">True</span></span>                                |
| <span data-ttu-id="aa335-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-210">Is Indexed</span></span>             | <span data-ttu-id="aa335-211">True</span><span class="sxs-lookup"><span data-stu-id="aa335-211">True</span></span>                                |
| <span data-ttu-id="aa335-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-212">In Global Catalog</span></span>      | <span data-ttu-id="aa335-213">True</span><span class="sxs-lookup"><span data-stu-id="aa335-213">True</span></span>                                |
| <span data-ttu-id="aa335-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-215">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-216">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-217">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-218">Search-Flags</span></span>           | <span data-ttu-id="aa335-219">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-219">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-220">System-Flags</span></span>           | <span data-ttu-id="aa335-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-221">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-222">Classes used in</span></span>        | [<span data-ttu-id="aa335-223">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-223">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aa335-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa335-224">Windows Server 2008</span></span>



| <span data-ttu-id="aa335-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-225">Entry</span></span> | <span data-ttu-id="aa335-226">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-226">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-227">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-228">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-229">System-Only</span></span>            | <span data-ttu-id="aa335-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-230">False</span></span>                               |
| <span data-ttu-id="aa335-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-231">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-232">True</span><span class="sxs-lookup"><span data-stu-id="aa335-232">True</span></span>                                |
| <span data-ttu-id="aa335-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-233">Is Indexed</span></span>             | <span data-ttu-id="aa335-234">True</span><span class="sxs-lookup"><span data-stu-id="aa335-234">True</span></span>                                |
| <span data-ttu-id="aa335-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-235">In Global Catalog</span></span>      | <span data-ttu-id="aa335-236">True</span><span class="sxs-lookup"><span data-stu-id="aa335-236">True</span></span>                                |
| <span data-ttu-id="aa335-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-238">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-239">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-240">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-241">Search-Flags</span></span>           | <span data-ttu-id="aa335-242">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-242">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-243">System-Flags</span></span>           | <span data-ttu-id="aa335-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-244">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-245">Classes used in</span></span>        | [<span data-ttu-id="aa335-246">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-246">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aa335-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa335-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aa335-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-248">Entry</span></span> | <span data-ttu-id="aa335-249">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-249">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-250">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-251">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-252">System-Only</span></span>            | <span data-ttu-id="aa335-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-253">False</span></span>                               |
| <span data-ttu-id="aa335-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-254">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-255">True</span><span class="sxs-lookup"><span data-stu-id="aa335-255">True</span></span>                                |
| <span data-ttu-id="aa335-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-256">Is Indexed</span></span>             | <span data-ttu-id="aa335-257">True</span><span class="sxs-lookup"><span data-stu-id="aa335-257">True</span></span>                                |
| <span data-ttu-id="aa335-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-258">In Global Catalog</span></span>      | <span data-ttu-id="aa335-259">True</span><span class="sxs-lookup"><span data-stu-id="aa335-259">True</span></span>                                |
| <span data-ttu-id="aa335-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-261">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-262">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-263">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-264">Search-Flags</span></span>           | <span data-ttu-id="aa335-265">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-265">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-266">System-Flags</span></span>           | <span data-ttu-id="aa335-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-267">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-268">Classes used in</span></span>        | [<span data-ttu-id="aa335-269">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-269">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aa335-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa335-270">Windows Server 2012</span></span>



| <span data-ttu-id="aa335-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="aa335-271">Entry</span></span> | <span data-ttu-id="aa335-272">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-272">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="aa335-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="aa335-273">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa335-274">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="aa335-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa335-275">System-Only</span></span>            | <span data-ttu-id="aa335-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="aa335-276">False</span></span>                               |
| <span data-ttu-id="aa335-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="aa335-277">Is-Single-Valued</span></span>       | <span data-ttu-id="aa335-278">True</span><span class="sxs-lookup"><span data-stu-id="aa335-278">True</span></span>                                |
| <span data-ttu-id="aa335-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="aa335-279">Is Indexed</span></span>             | <span data-ttu-id="aa335-280">True</span><span class="sxs-lookup"><span data-stu-id="aa335-280">True</span></span>                                |
| <span data-ttu-id="aa335-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="aa335-281">In Global Catalog</span></span>      | <span data-ttu-id="aa335-282">True</span><span class="sxs-lookup"><span data-stu-id="aa335-282">True</span></span>                                |
| <span data-ttu-id="aa335-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="aa335-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa335-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aa335-284">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="aa335-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa335-285">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="aa335-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa335-286">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="aa335-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-287">Search-Flags</span></span>           | <span data-ttu-id="aa335-288">0x00000009</span><span class="sxs-lookup"><span data-stu-id="aa335-288">0x00000009</span></span>                          |
| <span data-ttu-id="aa335-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa335-289">System-Flags</span></span>           | <span data-ttu-id="aa335-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aa335-290">0x00000012</span></span>                          |
| <span data-ttu-id="aa335-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="aa335-291">Classes used in</span></span>        | [<span data-ttu-id="aa335-292">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa335-292">**Group**</span></span>](c-group.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="aa335-293">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa335-293">Remarks</span></span>

<span data-ttu-id="aa335-294">Этот атрибут может быть нулевым или сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="aa335-294">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="aa335-295">Значение</span><span class="sxs-lookup"><span data-stu-id="aa335-295">Value</span></span>                   | <span data-ttu-id="aa335-296">Описание</span><span class="sxs-lookup"><span data-stu-id="aa335-296">Description</span></span>                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa335-297">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="aa335-297">1 (0x00000001)</span></span>          | <span data-ttu-id="aa335-298">Указывает группу, созданную системой.</span><span class="sxs-lookup"><span data-stu-id="aa335-298">Specifies a group that is created by the system.</span></span>                                             |
| <span data-ttu-id="aa335-299">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="aa335-299">2 (0x00000002)</span></span>          | <span data-ttu-id="aa335-300">Указывает группу с глобальной областью.</span><span class="sxs-lookup"><span data-stu-id="aa335-300">Specifies a group with global scope.</span></span>                                                         |
| <span data-ttu-id="aa335-301">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="aa335-301">4 (0x00000004)</span></span>          | <span data-ttu-id="aa335-302">Указывает группу с локальной областью действия домена.</span><span class="sxs-lookup"><span data-stu-id="aa335-302">Specifies a group with domain local scope.</span></span>                                                   |
| <span data-ttu-id="aa335-303">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="aa335-303">8 (0x00000008)</span></span>          | <span data-ttu-id="aa335-304">Задает группу с универсальной областью действия.</span><span class="sxs-lookup"><span data-stu-id="aa335-304">Specifies a group with universal scope.</span></span>                                                      |
| <span data-ttu-id="aa335-305">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="aa335-305">16 (0x00000010)</span></span>         | <span data-ttu-id="aa335-306">Указывает \_ группу Basic для приложения для диспетчера авторизации Windows Server.</span><span class="sxs-lookup"><span data-stu-id="aa335-306">Specifies an APP\_BASIC group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="aa335-307">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="aa335-307">32 (0x00000020)</span></span>         | <span data-ttu-id="aa335-308">Указывает \_ группу запросов приложений для диспетчера авторизации Windows Server.</span><span class="sxs-lookup"><span data-stu-id="aa335-308">Specifies an APP\_QUERY group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="aa335-309">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="aa335-309">2147483648 (0x80000000)</span></span> | <span data-ttu-id="aa335-310">Указывает группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aa335-310">Specifies a security group.</span></span> <span data-ttu-id="aa335-311">Если этот флаг не установлен, группа является группой рассылки.</span><span class="sxs-lookup"><span data-stu-id="aa335-311">If this flag is not set, then the group is a distribution group.</span></span> |



 

<span data-ttu-id="aa335-312">Дополнительные сведения о типе и области группы см. в разделах [типы групп](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) и [область групп](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) в Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="aa335-312">For more information about group type and scope, see the [Group types](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) and [Group scope](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) topics on Microsoft TechNet.</span></span>

 

