---
title: Атрибут Is-Defunct
description: Если значение — TRUE, класс или атрибут больше не может использоваться. Старые версии этого объекта могут существовать, но создать новые нельзя.
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Is-Defunct
- Схема AD атрибута "неуничтоженная"
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655251"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="845df-106">Атрибут Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="845df-106">Is-Defunct attribute</span></span>

<span data-ttu-id="845df-107">Если **значение — true**, класс или атрибут больше не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="845df-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="845df-108">Старые версии этого объекта могут существовать, но создать новые нельзя.</span><span class="sxs-lookup"><span data-stu-id="845df-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="845df-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-109">Entry</span></span> | <span data-ttu-id="845df-110">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="845df-111">CN</span><span class="sxs-lookup"><span data-stu-id="845df-111">CN</span></span>                | <span data-ttu-id="845df-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="845df-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="845df-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="845df-113">Ldap-Display-Name</span></span> | <span data-ttu-id="845df-114">Уничтоженный</span><span class="sxs-lookup"><span data-stu-id="845df-114">isDefunct</span></span>                            |
| <span data-ttu-id="845df-115">Размер</span><span class="sxs-lookup"><span data-stu-id="845df-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="845df-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="845df-116">Update Privilege</span></span>  | <span data-ttu-id="845df-117">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="845df-117">Schema administrator</span></span>                 |
| <span data-ttu-id="845df-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="845df-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="845df-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="845df-119">Attribute-Id</span></span>      | <span data-ttu-id="845df-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="845df-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="845df-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="845df-121">System-Id-Guid</span></span>    | <span data-ttu-id="845df-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="845df-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="845df-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="845df-123">Syntax</span></span>            | [<span data-ttu-id="845df-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="845df-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="845df-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="845df-125">Implementations</span></span>

-   [<span data-ttu-id="845df-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="845df-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="845df-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="845df-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="845df-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="845df-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="845df-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="845df-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="845df-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="845df-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="845df-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="845df-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="845df-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="845df-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="845df-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="845df-133">Windows 2000 Server</span></span>



| <span data-ttu-id="845df-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-134">Entry</span></span> | <span data-ttu-id="845df-135">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-138">System-Only</span></span>            | <span data-ttu-id="845df-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-139">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-140">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-141">True</span><span class="sxs-lookup"><span data-stu-id="845df-141">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-142">Is Indexed</span></span>             | <span data-ttu-id="845df-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-143">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-144">In Global Catalog</span></span>      | <span data-ttu-id="845df-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-145">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-150">Search-Flags</span></span>           | <span data-ttu-id="845df-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-152">System-Flags</span></span>           | <span data-ttu-id="845df-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-154">Classes used in</span></span>        | [<span data-ttu-id="845df-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-156">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="845df-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="845df-157">Windows Server 2003</span></span>



| <span data-ttu-id="845df-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-158">Entry</span></span> | <span data-ttu-id="845df-159">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-162">System-Only</span></span>            | <span data-ttu-id="845df-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-163">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-164">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-165">True</span><span class="sxs-lookup"><span data-stu-id="845df-165">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-166">Is Indexed</span></span>             | <span data-ttu-id="845df-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-167">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-168">In Global Catalog</span></span>      | <span data-ttu-id="845df-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-169">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-174">Search-Flags</span></span>           | <span data-ttu-id="845df-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-176">System-Flags</span></span>           | <span data-ttu-id="845df-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-178">Classes used in</span></span>        | [<span data-ttu-id="845df-179">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-180">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="845df-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="845df-181">ADAM</span></span>



| <span data-ttu-id="845df-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-182">Entry</span></span> | <span data-ttu-id="845df-183">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-186">System-Only</span></span>            | <span data-ttu-id="845df-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-187">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-188">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-189">True</span><span class="sxs-lookup"><span data-stu-id="845df-189">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-190">Is Indexed</span></span>             | <span data-ttu-id="845df-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-191">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-192">In Global Catalog</span></span>      | <span data-ttu-id="845df-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-193">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-198">Search-Flags</span></span>           | <span data-ttu-id="845df-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-200">System-Flags</span></span>           | <span data-ttu-id="845df-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-202">Classes used in</span></span>        | [<span data-ttu-id="845df-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-204">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="845df-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="845df-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="845df-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-206">Entry</span></span> | <span data-ttu-id="845df-207">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-210">System-Only</span></span>            | <span data-ttu-id="845df-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-211">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-212">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-213">True</span><span class="sxs-lookup"><span data-stu-id="845df-213">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-214">Is Indexed</span></span>             | <span data-ttu-id="845df-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-215">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-216">In Global Catalog</span></span>      | <span data-ttu-id="845df-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-217">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-222">Search-Flags</span></span>           | <span data-ttu-id="845df-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-224">System-Flags</span></span>           | <span data-ttu-id="845df-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-226">Classes used in</span></span>        | [<span data-ttu-id="845df-227">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-228">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="845df-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="845df-229">Windows Server 2008</span></span>



| <span data-ttu-id="845df-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-230">Entry</span></span> | <span data-ttu-id="845df-231">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-234">System-Only</span></span>            | <span data-ttu-id="845df-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-235">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-236">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-237">True</span><span class="sxs-lookup"><span data-stu-id="845df-237">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-238">Is Indexed</span></span>             | <span data-ttu-id="845df-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-239">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-240">In Global Catalog</span></span>      | <span data-ttu-id="845df-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-241">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-246">Search-Flags</span></span>           | <span data-ttu-id="845df-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-248">System-Flags</span></span>           | <span data-ttu-id="845df-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-250">Classes used in</span></span>        | [<span data-ttu-id="845df-251">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-252">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="845df-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="845df-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="845df-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-254">Entry</span></span> | <span data-ttu-id="845df-255">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-258">System-Only</span></span>            | <span data-ttu-id="845df-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-259">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-260">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-261">True</span><span class="sxs-lookup"><span data-stu-id="845df-261">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-262">Is Indexed</span></span>             | <span data-ttu-id="845df-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-263">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-264">In Global Catalog</span></span>      | <span data-ttu-id="845df-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-265">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-270">Search-Flags</span></span>           | <span data-ttu-id="845df-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-272">System-Flags</span></span>           | <span data-ttu-id="845df-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-274">Classes used in</span></span>        | [<span data-ttu-id="845df-275">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-276">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="845df-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="845df-277">Windows Server 2012</span></span>



| <span data-ttu-id="845df-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="845df-278">Entry</span></span> | <span data-ttu-id="845df-279">Значение</span><span class="sxs-lookup"><span data-stu-id="845df-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845df-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="845df-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="845df-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="845df-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="845df-282">System-Only</span></span>            | <span data-ttu-id="845df-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-283">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="845df-284">Is-Single-Valued</span></span>       | <span data-ttu-id="845df-285">True</span><span class="sxs-lookup"><span data-stu-id="845df-285">True</span></span>                                                                                                      |
| <span data-ttu-id="845df-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="845df-286">Is Indexed</span></span>             | <span data-ttu-id="845df-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-287">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="845df-288">In Global Catalog</span></span>      | <span data-ttu-id="845df-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="845df-289">False</span></span>                                                                                                     |
| <span data-ttu-id="845df-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="845df-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="845df-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="845df-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="845df-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="845df-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="845df-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="845df-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-294">Search-Flags</span></span>           | <span data-ttu-id="845df-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="845df-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="845df-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="845df-296">System-Flags</span></span>           | <span data-ttu-id="845df-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="845df-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="845df-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="845df-298">Classes used in</span></span>        | [<span data-ttu-id="845df-299">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="845df-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="845df-300">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="845df-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





