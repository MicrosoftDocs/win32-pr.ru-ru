---
title: Атрибут имеет значение, являющийся членом типа partial-Attribute
description: Если значение — TRUE, этот атрибут реплицируется в глобальный каталог.
ms.assetid: 9ffd85e8-da1a-4b39-9758-2dc049204ca0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута,-Member-of-Attribute-Set
- Схема AD атрибута Исмемберофпартиалаттрибутесет
topic_type:
- apiref
api_name:
- Is-Member-Of-Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbbd05f95a46ec4e42c139ddda157a4057bde60
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989520"
---
# <a name="is-member-of-partial-attribute-set-attribute"></a><span data-ttu-id="92916-105">Атрибут имеет значение, являющийся членом типа partial-Attribute</span><span class="sxs-lookup"><span data-stu-id="92916-105">Is-Member-Of-Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="92916-106">Если **значение — true**, этот атрибут реплицируется в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="92916-106">If **TRUE**, this attribute is replicated to the global catalog.</span></span>



| <span data-ttu-id="92916-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-107">Entry</span></span> | <span data-ttu-id="92916-108">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="92916-109">CN</span><span class="sxs-lookup"><span data-stu-id="92916-109">CN</span></span>                | <span data-ttu-id="92916-110">Параметр является членом типа partial-Attribute</span><span class="sxs-lookup"><span data-stu-id="92916-110">Is-Member-Of-Partial-Attribute-Set</span></span>   |
| <span data-ttu-id="92916-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="92916-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92916-112">isMemberOfPartialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="92916-112">isMemberOfPartialAttributeSet</span></span>        |
| <span data-ttu-id="92916-113">Размер</span><span class="sxs-lookup"><span data-stu-id="92916-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="92916-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="92916-114">Update Privilege</span></span>  | <span data-ttu-id="92916-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="92916-115">Schema administrator</span></span>                 |
| <span data-ttu-id="92916-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="92916-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="92916-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92916-117">Attribute-Id</span></span>      | <span data-ttu-id="92916-118">1.2.840.113556.1.4.639</span><span class="sxs-lookup"><span data-stu-id="92916-118">1.2.840.113556.1.4.639</span></span>               |
| <span data-ttu-id="92916-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="92916-119">System-Id-Guid</span></span>    | <span data-ttu-id="92916-120">19405b9d-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="92916-120">19405b9d-3cfa-11d1-a9c0-0000f80367c1</span></span> |
| <span data-ttu-id="92916-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92916-121">Syntax</span></span>            | [<span data-ttu-id="92916-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="92916-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="92916-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="92916-123">Implementations</span></span>

-   [<span data-ttu-id="92916-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92916-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92916-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92916-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92916-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="92916-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="92916-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92916-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92916-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92916-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92916-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92916-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92916-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92916-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92916-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92916-131">Windows 2000 Server</span></span>



| <span data-ttu-id="92916-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-132">Entry</span></span> | <span data-ttu-id="92916-133">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-136">System-Only</span></span>            | <span data-ttu-id="92916-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-137">False</span></span>                                                    |
| <span data-ttu-id="92916-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-138">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-139">True</span><span class="sxs-lookup"><span data-stu-id="92916-139">True</span></span>                                                     |
| <span data-ttu-id="92916-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-140">Is Indexed</span></span>             | <span data-ttu-id="92916-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-141">False</span></span>                                                    |
| <span data-ttu-id="92916-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-142">In Global Catalog</span></span>      | <span data-ttu-id="92916-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-143">False</span></span>                                                    |
| <span data-ttu-id="92916-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-146">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-147">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-148">Search-Flags</span></span>           | <span data-ttu-id="92916-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-149">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-150">System-Flags</span></span>           | <span data-ttu-id="92916-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-151">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-152">Classes used in</span></span>        | [<span data-ttu-id="92916-153">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92916-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92916-154">Windows Server 2003</span></span>



| <span data-ttu-id="92916-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-155">Entry</span></span> | <span data-ttu-id="92916-156">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-156">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-157">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-158">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-159">System-Only</span></span>            | <span data-ttu-id="92916-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-160">False</span></span>                                                    |
| <span data-ttu-id="92916-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-161">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-162">True</span><span class="sxs-lookup"><span data-stu-id="92916-162">True</span></span>                                                     |
| <span data-ttu-id="92916-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-163">Is Indexed</span></span>             | <span data-ttu-id="92916-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-164">False</span></span>                                                    |
| <span data-ttu-id="92916-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-165">In Global Catalog</span></span>      | <span data-ttu-id="92916-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-166">False</span></span>                                                    |
| <span data-ttu-id="92916-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-168">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-169">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-170">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-171">Search-Flags</span></span>           | <span data-ttu-id="92916-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-172">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-173">System-Flags</span></span>           | <span data-ttu-id="92916-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-174">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-175">Classes used in</span></span>        | [<span data-ttu-id="92916-176">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-176">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="92916-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="92916-177">ADAM</span></span>



| <span data-ttu-id="92916-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-178">Entry</span></span> | <span data-ttu-id="92916-179">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-179">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-180">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-181">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-182">System-Only</span></span>            | <span data-ttu-id="92916-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-183">False</span></span>                                                    |
| <span data-ttu-id="92916-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-184">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-185">True</span><span class="sxs-lookup"><span data-stu-id="92916-185">True</span></span>                                                     |
| <span data-ttu-id="92916-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-186">Is Indexed</span></span>             | <span data-ttu-id="92916-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-187">False</span></span>                                                    |
| <span data-ttu-id="92916-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-188">In Global Catalog</span></span>      | <span data-ttu-id="92916-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-189">False</span></span>                                                    |
| <span data-ttu-id="92916-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-191">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-192">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-193">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-194">Search-Flags</span></span>           | <span data-ttu-id="92916-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-195">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-196">System-Flags</span></span>           | <span data-ttu-id="92916-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-197">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-198">Classes used in</span></span>        | [<span data-ttu-id="92916-199">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-199">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92916-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92916-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92916-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-201">Entry</span></span> | <span data-ttu-id="92916-202">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-202">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-203">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-204">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-205">System-Only</span></span>            | <span data-ttu-id="92916-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-206">False</span></span>                                                    |
| <span data-ttu-id="92916-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-207">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-208">True</span><span class="sxs-lookup"><span data-stu-id="92916-208">True</span></span>                                                     |
| <span data-ttu-id="92916-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-209">Is Indexed</span></span>             | <span data-ttu-id="92916-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-210">False</span></span>                                                    |
| <span data-ttu-id="92916-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-211">In Global Catalog</span></span>      | <span data-ttu-id="92916-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-212">False</span></span>                                                    |
| <span data-ttu-id="92916-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-214">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-215">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-216">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-217">Search-Flags</span></span>           | <span data-ttu-id="92916-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-218">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-219">System-Flags</span></span>           | <span data-ttu-id="92916-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-220">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-221">Classes used in</span></span>        | [<span data-ttu-id="92916-222">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-222">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92916-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92916-223">Windows Server 2008</span></span>



| <span data-ttu-id="92916-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-224">Entry</span></span> | <span data-ttu-id="92916-225">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-225">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-226">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-227">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-228">System-Only</span></span>            | <span data-ttu-id="92916-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-229">False</span></span>                                                    |
| <span data-ttu-id="92916-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-230">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-231">True</span><span class="sxs-lookup"><span data-stu-id="92916-231">True</span></span>                                                     |
| <span data-ttu-id="92916-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-232">Is Indexed</span></span>             | <span data-ttu-id="92916-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-233">False</span></span>                                                    |
| <span data-ttu-id="92916-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-234">In Global Catalog</span></span>      | <span data-ttu-id="92916-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-235">False</span></span>                                                    |
| <span data-ttu-id="92916-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-237">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-238">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-239">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-240">Search-Flags</span></span>           | <span data-ttu-id="92916-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-241">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-242">System-Flags</span></span>           | <span data-ttu-id="92916-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-243">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-244">Classes used in</span></span>        | [<span data-ttu-id="92916-245">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-245">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92916-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92916-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92916-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-247">Entry</span></span> | <span data-ttu-id="92916-248">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-248">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-249">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-250">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-251">System-Only</span></span>            | <span data-ttu-id="92916-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-252">False</span></span>                                                    |
| <span data-ttu-id="92916-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-253">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-254">True</span><span class="sxs-lookup"><span data-stu-id="92916-254">True</span></span>                                                     |
| <span data-ttu-id="92916-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-255">Is Indexed</span></span>             | <span data-ttu-id="92916-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-256">False</span></span>                                                    |
| <span data-ttu-id="92916-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-257">In Global Catalog</span></span>      | <span data-ttu-id="92916-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-258">False</span></span>                                                    |
| <span data-ttu-id="92916-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-260">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-261">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-262">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-263">Search-Flags</span></span>           | <span data-ttu-id="92916-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-264">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-265">System-Flags</span></span>           | <span data-ttu-id="92916-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-266">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-267">Classes used in</span></span>        | [<span data-ttu-id="92916-268">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-268">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92916-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92916-269">Windows Server 2012</span></span>



| <span data-ttu-id="92916-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="92916-270">Entry</span></span> | <span data-ttu-id="92916-271">Значение</span><span class="sxs-lookup"><span data-stu-id="92916-271">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="92916-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="92916-272">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92916-273">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="92916-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="92916-274">System-Only</span></span>            | <span data-ttu-id="92916-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-275">False</span></span>                                                    |
| <span data-ttu-id="92916-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="92916-276">Is-Single-Valued</span></span>       | <span data-ttu-id="92916-277">True</span><span class="sxs-lookup"><span data-stu-id="92916-277">True</span></span>                                                     |
| <span data-ttu-id="92916-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="92916-278">Is Indexed</span></span>             | <span data-ttu-id="92916-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-279">False</span></span>                                                    |
| <span data-ttu-id="92916-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="92916-280">In Global Catalog</span></span>      | <span data-ttu-id="92916-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="92916-281">False</span></span>                                                    |
| <span data-ttu-id="92916-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="92916-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="92916-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92916-283">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="92916-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92916-284">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="92916-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92916-285">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="92916-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-286">Search-Flags</span></span>           | <span data-ttu-id="92916-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92916-287">0x00000000</span></span>                                               |
| <span data-ttu-id="92916-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92916-288">System-Flags</span></span>           | <span data-ttu-id="92916-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92916-289">0x00000010</span></span>                                               |
| <span data-ttu-id="92916-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="92916-290">Classes used in</span></span>        | [<span data-ttu-id="92916-291">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="92916-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





