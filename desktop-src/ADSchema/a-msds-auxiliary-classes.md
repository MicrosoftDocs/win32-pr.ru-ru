---
title: Атрибут ms-DS-вспомогательных классов
description: Этот атрибут перечисляет вспомогательные классы, которые были динамически присоединены к объекту. Этот атрибут не связан с классом. Он заполняется системой автоматически.
ms.assetid: bf41f15d-9af9-43de-8425-33d50880c3fa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-вспомогательных классов
- msDS — схема AD атрибута для вспомогательных классов
topic_type:
- apiref
api_name:
- ms-DS-Auxiliary-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24608d0626ae4bcd6adb70a646d95121615c29e5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893534"
---
# <a name="ms-ds-auxiliary-classes-attribute"></a><span data-ttu-id="270b3-107">Атрибут ms-DS-вспомогательных классов</span><span class="sxs-lookup"><span data-stu-id="270b3-107">ms-DS-Auxiliary-Classes attribute</span></span>

<span data-ttu-id="270b3-108">Этот атрибут перечисляет вспомогательные классы, которые были динамически присоединены к объекту.</span><span class="sxs-lookup"><span data-stu-id="270b3-108">This attribute lists the auxiliary classes that have been dynamically attached to an object.</span></span> <span data-ttu-id="270b3-109">Этот атрибут не связан с классом.</span><span class="sxs-lookup"><span data-stu-id="270b3-109">This attribute is not associated with a class.</span></span> <span data-ttu-id="270b3-110">Он заполняется системой автоматически.</span><span class="sxs-lookup"><span data-stu-id="270b3-110">It is automatically populated by the system.</span></span>



| <span data-ttu-id="270b3-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-111">Entry</span></span> | <span data-ttu-id="270b3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="270b3-113">CN</span><span class="sxs-lookup"><span data-stu-id="270b3-113">CN</span></span>                | <span data-ttu-id="270b3-114">MS-DS-вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="270b3-114">ms-DS-Auxiliary-Classes</span></span>                                         |
| <span data-ttu-id="270b3-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="270b3-115">Ldap-Display-Name</span></span> | <span data-ttu-id="270b3-116">msDS-вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="270b3-116">msDS-Auxiliary-Classes</span></span>                                          |
| <span data-ttu-id="270b3-117">Размер</span><span class="sxs-lookup"><span data-stu-id="270b3-117">Size</span></span>              | \-                                                              |
| <span data-ttu-id="270b3-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="270b3-118">Update Privilege</span></span>  | <span data-ttu-id="270b3-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="270b3-119">This value is set by the system.</span></span>                                |
| <span data-ttu-id="270b3-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="270b3-120">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="270b3-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-121">Attribute-Id</span></span>      | <span data-ttu-id="270b3-122">1.2.840.113556.1.4.1458</span><span class="sxs-lookup"><span data-stu-id="270b3-122">1.2.840.113556.1.4.1458</span></span>                                         |
| <span data-ttu-id="270b3-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="270b3-123">System-Id-Guid</span></span>    | <span data-ttu-id="270b3-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span><span class="sxs-lookup"><span data-stu-id="270b3-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span></span>                            |
| <span data-ttu-id="270b3-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="270b3-125">Syntax</span></span>            | [<span data-ttu-id="270b3-126">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="270b3-126">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="270b3-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="270b3-127">Implementations</span></span>

-   [<span data-ttu-id="270b3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="270b3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="270b3-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="270b3-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="270b3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="270b3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="270b3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="270b3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="270b3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="270b3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="270b3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="270b3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="270b3-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="270b3-134">Windows Server 2003</span></span>



| <span data-ttu-id="270b3-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-135">Entry</span></span> | <span data-ttu-id="270b3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-136">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="270b3-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="270b3-137">Link-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-138">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="270b3-139">System-Only</span></span>            | <span data-ttu-id="270b3-140">True</span><span class="sxs-lookup"><span data-stu-id="270b3-140">True</span></span>         |
| <span data-ttu-id="270b3-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="270b3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="270b3-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-142">False</span></span>        |
| <span data-ttu-id="270b3-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="270b3-143">Is Indexed</span></span>             | <span data-ttu-id="270b3-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-144">False</span></span>        |
| <span data-ttu-id="270b3-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="270b3-145">In Global Catalog</span></span>      | <span data-ttu-id="270b3-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-146">False</span></span>        |
| <span data-ttu-id="270b3-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="270b3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="270b3-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="270b3-148">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="270b3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="270b3-149">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="270b3-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="270b3-150">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="270b3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-151">Search-Flags</span></span>           | <span data-ttu-id="270b3-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="270b3-152">0x00000008</span></span>   |
| <span data-ttu-id="270b3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-153">System-Flags</span></span>           | <span data-ttu-id="270b3-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="270b3-154">0x00000014</span></span>   |
| <span data-ttu-id="270b3-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="270b3-155">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="270b3-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="270b3-156">ADAM</span></span>



| <span data-ttu-id="270b3-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-157">Entry</span></span> | <span data-ttu-id="270b3-158">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-158">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="270b3-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="270b3-159">Link-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-160">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="270b3-161">System-Only</span></span>            | <span data-ttu-id="270b3-162">True</span><span class="sxs-lookup"><span data-stu-id="270b3-162">True</span></span>         |
| <span data-ttu-id="270b3-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="270b3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="270b3-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-164">False</span></span>        |
| <span data-ttu-id="270b3-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="270b3-165">Is Indexed</span></span>             | <span data-ttu-id="270b3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-166">False</span></span>        |
| <span data-ttu-id="270b3-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="270b3-167">In Global Catalog</span></span>      | <span data-ttu-id="270b3-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-168">False</span></span>        |
| <span data-ttu-id="270b3-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="270b3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="270b3-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="270b3-170">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="270b3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="270b3-171">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="270b3-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="270b3-172">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="270b3-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-173">Search-Flags</span></span>           | <span data-ttu-id="270b3-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="270b3-174">0x00000008</span></span>   |
| <span data-ttu-id="270b3-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-175">System-Flags</span></span>           | <span data-ttu-id="270b3-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="270b3-176">0x00000014</span></span>   |
| <span data-ttu-id="270b3-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="270b3-177">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="270b3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="270b3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="270b3-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-179">Entry</span></span> | <span data-ttu-id="270b3-180">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="270b3-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="270b3-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="270b3-183">System-Only</span></span>            | <span data-ttu-id="270b3-184">True</span><span class="sxs-lookup"><span data-stu-id="270b3-184">True</span></span>         |
| <span data-ttu-id="270b3-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="270b3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="270b3-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-186">False</span></span>        |
| <span data-ttu-id="270b3-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="270b3-187">Is Indexed</span></span>             | <span data-ttu-id="270b3-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-188">False</span></span>        |
| <span data-ttu-id="270b3-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="270b3-189">In Global Catalog</span></span>      | <span data-ttu-id="270b3-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-190">False</span></span>        |
| <span data-ttu-id="270b3-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="270b3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="270b3-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="270b3-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="270b3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="270b3-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="270b3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="270b3-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="270b3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-195">Search-Flags</span></span>           | <span data-ttu-id="270b3-196">0x00000008</span><span class="sxs-lookup"><span data-stu-id="270b3-196">0x00000008</span></span>   |
| <span data-ttu-id="270b3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-197">System-Flags</span></span>           | <span data-ttu-id="270b3-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="270b3-198">0x00000014</span></span>   |
| <span data-ttu-id="270b3-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="270b3-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="270b3-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="270b3-200">Windows Server 2008</span></span>



| <span data-ttu-id="270b3-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-201">Entry</span></span> | <span data-ttu-id="270b3-202">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-202">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="270b3-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="270b3-203">Link-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-204">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="270b3-205">System-Only</span></span>            | <span data-ttu-id="270b3-206">True</span><span class="sxs-lookup"><span data-stu-id="270b3-206">True</span></span>         |
| <span data-ttu-id="270b3-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="270b3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="270b3-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-208">False</span></span>        |
| <span data-ttu-id="270b3-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="270b3-209">Is Indexed</span></span>             | <span data-ttu-id="270b3-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-210">False</span></span>        |
| <span data-ttu-id="270b3-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="270b3-211">In Global Catalog</span></span>      | <span data-ttu-id="270b3-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-212">False</span></span>        |
| <span data-ttu-id="270b3-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="270b3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="270b3-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="270b3-214">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="270b3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="270b3-215">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="270b3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="270b3-216">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="270b3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-217">Search-Flags</span></span>           | <span data-ttu-id="270b3-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="270b3-218">0x00000008</span></span>   |
| <span data-ttu-id="270b3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-219">System-Flags</span></span>           | <span data-ttu-id="270b3-220">0x00000014</span><span class="sxs-lookup"><span data-stu-id="270b3-220">0x00000014</span></span>   |
| <span data-ttu-id="270b3-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="270b3-221">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="270b3-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="270b3-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="270b3-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-223">Entry</span></span> | <span data-ttu-id="270b3-224">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-224">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="270b3-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="270b3-225">Link-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="270b3-227">System-Only</span></span>            | <span data-ttu-id="270b3-228">True</span><span class="sxs-lookup"><span data-stu-id="270b3-228">True</span></span>         |
| <span data-ttu-id="270b3-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="270b3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="270b3-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-230">False</span></span>        |
| <span data-ttu-id="270b3-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="270b3-231">Is Indexed</span></span>             | <span data-ttu-id="270b3-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-232">False</span></span>        |
| <span data-ttu-id="270b3-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="270b3-233">In Global Catalog</span></span>      | <span data-ttu-id="270b3-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-234">False</span></span>        |
| <span data-ttu-id="270b3-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="270b3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="270b3-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="270b3-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="270b3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="270b3-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="270b3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="270b3-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="270b3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-239">Search-Flags</span></span>           | <span data-ttu-id="270b3-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="270b3-240">0x00000008</span></span>   |
| <span data-ttu-id="270b3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-241">System-Flags</span></span>           | <span data-ttu-id="270b3-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="270b3-242">0x00000014</span></span>   |
| <span data-ttu-id="270b3-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="270b3-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="270b3-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="270b3-244">Windows Server 2012</span></span>



| <span data-ttu-id="270b3-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="270b3-245">Entry</span></span> | <span data-ttu-id="270b3-246">Значение</span><span class="sxs-lookup"><span data-stu-id="270b3-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="270b3-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="270b3-247">Link-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="270b3-248">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="270b3-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="270b3-249">System-Only</span></span>            | <span data-ttu-id="270b3-250">True</span><span class="sxs-lookup"><span data-stu-id="270b3-250">True</span></span>         |
| <span data-ttu-id="270b3-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="270b3-251">Is-Single-Valued</span></span>       | <span data-ttu-id="270b3-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-252">False</span></span>        |
| <span data-ttu-id="270b3-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="270b3-253">Is Indexed</span></span>             | <span data-ttu-id="270b3-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-254">False</span></span>        |
| <span data-ttu-id="270b3-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="270b3-255">In Global Catalog</span></span>      | <span data-ttu-id="270b3-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="270b3-256">False</span></span>        |
| <span data-ttu-id="270b3-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="270b3-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="270b3-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="270b3-258">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="270b3-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="270b3-259">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="270b3-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="270b3-260">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="270b3-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-261">Search-Flags</span></span>           | <span data-ttu-id="270b3-262">0x00000008</span><span class="sxs-lookup"><span data-stu-id="270b3-262">0x00000008</span></span>   |
| <span data-ttu-id="270b3-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="270b3-263">System-Flags</span></span>           | <span data-ttu-id="270b3-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="270b3-264">0x00000014</span></span>   |
| <span data-ttu-id="270b3-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="270b3-265">Classes used in</span></span>        | \-           |



 

 




