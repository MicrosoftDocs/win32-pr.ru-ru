---
title: Атрибут System-Only
description: Логическое значение, указывающее, может ли только Active Directory изменять класс. Только системные классы могут создаваться или удаляться только агентом системы каталогов.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута System-Only
- Схема AD атрибута Системонли
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893266"
---
# <a name="system-only-attribute"></a><span data-ttu-id="854bd-106">Атрибут System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-106">System-Only attribute</span></span>

<span data-ttu-id="854bd-107">Логическое значение, указывающее, может ли только Active Directory изменять класс.</span><span class="sxs-lookup"><span data-stu-id="854bd-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="854bd-108">Только системные классы могут создаваться или удаляться только агентом системы каталогов.</span><span class="sxs-lookup"><span data-stu-id="854bd-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="854bd-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-109">Entry</span></span> | <span data-ttu-id="854bd-110">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="854bd-111">CN</span><span class="sxs-lookup"><span data-stu-id="854bd-111">CN</span></span>                | <span data-ttu-id="854bd-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-112">System-Only</span></span>                          |
| <span data-ttu-id="854bd-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="854bd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="854bd-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="854bd-114">systemOnly</span></span>                           |
| <span data-ttu-id="854bd-115">Размер</span><span class="sxs-lookup"><span data-stu-id="854bd-115">Size</span></span>              | <span data-ttu-id="854bd-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="854bd-116">4 bytes</span></span>                              |
| <span data-ttu-id="854bd-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="854bd-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="854bd-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="854bd-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="854bd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-119">Attribute-Id</span></span>      | <span data-ttu-id="854bd-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="854bd-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="854bd-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="854bd-121">System-Id-Guid</span></span>    | <span data-ttu-id="854bd-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="854bd-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="854bd-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="854bd-123">Syntax</span></span>            | [<span data-ttu-id="854bd-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="854bd-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="854bd-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="854bd-125">Implementations</span></span>

-   [<span data-ttu-id="854bd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="854bd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="854bd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="854bd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="854bd-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="854bd-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="854bd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="854bd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="854bd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="854bd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="854bd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="854bd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="854bd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="854bd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="854bd-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="854bd-133">Windows 2000 Server</span></span>



| <span data-ttu-id="854bd-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-134">Entry</span></span> | <span data-ttu-id="854bd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-138">System-Only</span></span>            | <span data-ttu-id="854bd-139">True</span><span class="sxs-lookup"><span data-stu-id="854bd-139">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-141">True</span><span class="sxs-lookup"><span data-stu-id="854bd-141">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-142">Is Indexed</span></span>             | <span data-ttu-id="854bd-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-143">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-144">In Global Catalog</span></span>      | <span data-ttu-id="854bd-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-145">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-150">Search-Flags</span></span>           | <span data-ttu-id="854bd-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-152">System-Flags</span></span>           | <span data-ttu-id="854bd-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-154">Classes used in</span></span>        | [<span data-ttu-id="854bd-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-156">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="854bd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="854bd-157">Windows Server 2003</span></span>



| <span data-ttu-id="854bd-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-158">Entry</span></span> | <span data-ttu-id="854bd-159">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-162">System-Only</span></span>            | <span data-ttu-id="854bd-163">True</span><span class="sxs-lookup"><span data-stu-id="854bd-163">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-165">True</span><span class="sxs-lookup"><span data-stu-id="854bd-165">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-166">Is Indexed</span></span>             | <span data-ttu-id="854bd-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-167">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-168">In Global Catalog</span></span>      | <span data-ttu-id="854bd-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-169">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-174">Search-Flags</span></span>           | <span data-ttu-id="854bd-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-176">System-Flags</span></span>           | <span data-ttu-id="854bd-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-178">Classes used in</span></span>        | [<span data-ttu-id="854bd-179">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-180">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="854bd-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="854bd-181">ADAM</span></span>



| <span data-ttu-id="854bd-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-182">Entry</span></span> | <span data-ttu-id="854bd-183">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-186">System-Only</span></span>            | <span data-ttu-id="854bd-187">True</span><span class="sxs-lookup"><span data-stu-id="854bd-187">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-189">True</span><span class="sxs-lookup"><span data-stu-id="854bd-189">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-190">Is Indexed</span></span>             | <span data-ttu-id="854bd-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-191">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-192">In Global Catalog</span></span>      | <span data-ttu-id="854bd-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-193">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-198">Search-Flags</span></span>           | <span data-ttu-id="854bd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-200">System-Flags</span></span>           | <span data-ttu-id="854bd-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-202">Classes used in</span></span>        | [<span data-ttu-id="854bd-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-204">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="854bd-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="854bd-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="854bd-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-206">Entry</span></span> | <span data-ttu-id="854bd-207">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-210">System-Only</span></span>            | <span data-ttu-id="854bd-211">True</span><span class="sxs-lookup"><span data-stu-id="854bd-211">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-212">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-213">True</span><span class="sxs-lookup"><span data-stu-id="854bd-213">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-214">Is Indexed</span></span>             | <span data-ttu-id="854bd-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-215">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-216">In Global Catalog</span></span>      | <span data-ttu-id="854bd-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-217">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-222">Search-Flags</span></span>           | <span data-ttu-id="854bd-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-224">System-Flags</span></span>           | <span data-ttu-id="854bd-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-226">Classes used in</span></span>        | [<span data-ttu-id="854bd-227">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-228">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="854bd-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="854bd-229">Windows Server 2008</span></span>



| <span data-ttu-id="854bd-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-230">Entry</span></span> | <span data-ttu-id="854bd-231">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-234">System-Only</span></span>            | <span data-ttu-id="854bd-235">True</span><span class="sxs-lookup"><span data-stu-id="854bd-235">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-236">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-237">True</span><span class="sxs-lookup"><span data-stu-id="854bd-237">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-238">Is Indexed</span></span>             | <span data-ttu-id="854bd-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-239">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-240">In Global Catalog</span></span>      | <span data-ttu-id="854bd-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-241">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-246">Search-Flags</span></span>           | <span data-ttu-id="854bd-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-248">System-Flags</span></span>           | <span data-ttu-id="854bd-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-250">Classes used in</span></span>        | [<span data-ttu-id="854bd-251">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-252">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="854bd-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="854bd-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="854bd-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-254">Entry</span></span> | <span data-ttu-id="854bd-255">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-258">System-Only</span></span>            | <span data-ttu-id="854bd-259">True</span><span class="sxs-lookup"><span data-stu-id="854bd-259">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-260">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-261">True</span><span class="sxs-lookup"><span data-stu-id="854bd-261">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-262">Is Indexed</span></span>             | <span data-ttu-id="854bd-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-263">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-264">In Global Catalog</span></span>      | <span data-ttu-id="854bd-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-265">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-270">Search-Flags</span></span>           | <span data-ttu-id="854bd-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-272">System-Flags</span></span>           | <span data-ttu-id="854bd-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-274">Classes used in</span></span>        | [<span data-ttu-id="854bd-275">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-276">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="854bd-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="854bd-277">Windows Server 2012</span></span>



| <span data-ttu-id="854bd-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="854bd-278">Entry</span></span> | <span data-ttu-id="854bd-279">Значение</span><span class="sxs-lookup"><span data-stu-id="854bd-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854bd-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="854bd-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="854bd-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="854bd-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="854bd-282">System-Only</span></span>            | <span data-ttu-id="854bd-283">True</span><span class="sxs-lookup"><span data-stu-id="854bd-283">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="854bd-284">Is-Single-Valued</span></span>       | <span data-ttu-id="854bd-285">True</span><span class="sxs-lookup"><span data-stu-id="854bd-285">True</span></span>                                                                                                      |
| <span data-ttu-id="854bd-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="854bd-286">Is Indexed</span></span>             | <span data-ttu-id="854bd-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-287">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="854bd-288">In Global Catalog</span></span>      | <span data-ttu-id="854bd-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="854bd-289">False</span></span>                                                                                                     |
| <span data-ttu-id="854bd-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="854bd-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="854bd-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="854bd-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="854bd-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="854bd-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="854bd-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="854bd-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-294">Search-Flags</span></span>           | <span data-ttu-id="854bd-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="854bd-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="854bd-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="854bd-296">System-Flags</span></span>           | <span data-ttu-id="854bd-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="854bd-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="854bd-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="854bd-298">Classes used in</span></span>        | [<span data-ttu-id="854bd-299">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="854bd-300">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="854bd-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





