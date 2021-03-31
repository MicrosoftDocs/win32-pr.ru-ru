---
title: Атрибут Schema-ID-GUID
description: Уникальный идентификатор атрибута.
ms.assetid: 50f0a4b6-dded-42db-9ac5-123f2885c658
ms.tgt_platform: multiple
keywords:
- Schema-ID-схема AD атрибута GUID
- Схема AD атрибута schemaIDGUID
topic_type:
- apiref
api_name:
- Schema-ID-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f0b16cc45ecfbcd03e2104cbc6c5b5b41bd813
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138475"
---
# <a name="schema-id-guid-attribute"></a><span data-ttu-id="31903-105">Атрибут Schema-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="31903-105">Schema-ID-GUID attribute</span></span>

<span data-ttu-id="31903-106">Уникальный идентификатор атрибута.</span><span class="sxs-lookup"><span data-stu-id="31903-106">The unique identifier for an attribute.</span></span>



| <span data-ttu-id="31903-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-107">Entry</span></span> | <span data-ttu-id="31903-108">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="31903-109">CN</span><span class="sxs-lookup"><span data-stu-id="31903-109">CN</span></span>                | <span data-ttu-id="31903-110">Schema-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="31903-110">Schema-ID-GUID</span></span>                                                      |
| <span data-ttu-id="31903-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="31903-111">Ldap-Display-Name</span></span> | <span data-ttu-id="31903-112">schemaIDGUID</span><span class="sxs-lookup"><span data-stu-id="31903-112">schemaIDGUID</span></span>                                                        |
| <span data-ttu-id="31903-113">Размер</span><span class="sxs-lookup"><span data-stu-id="31903-113">Size</span></span>              | <span data-ttu-id="31903-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="31903-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="31903-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="31903-115">Update Privilege</span></span>  | <span data-ttu-id="31903-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="31903-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="31903-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="31903-117">Update Frequency</span></span>  | <span data-ttu-id="31903-118">Это значение задается при создании объекта и не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="31903-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="31903-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="31903-119">Attribute-Id</span></span>      | <span data-ttu-id="31903-120">1.2.840.113556.1.4.148</span><span class="sxs-lookup"><span data-stu-id="31903-120">1.2.840.113556.1.4.148</span></span>                                              |
| <span data-ttu-id="31903-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="31903-121">System-Id-Guid</span></span>    | <span data-ttu-id="31903-122">bf967923-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="31903-122">bf967923-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="31903-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31903-123">Syntax</span></span>            | [<span data-ttu-id="31903-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="31903-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="31903-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="31903-125">Implementations</span></span>

-   [<span data-ttu-id="31903-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="31903-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="31903-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="31903-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="31903-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="31903-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="31903-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="31903-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="31903-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="31903-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="31903-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="31903-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="31903-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="31903-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="31903-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31903-133">Windows 2000 Server</span></span>



| <span data-ttu-id="31903-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-134">Entry</span></span> | <span data-ttu-id="31903-135">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-138">System-Only</span></span>            | <span data-ttu-id="31903-139">True</span><span class="sxs-lookup"><span data-stu-id="31903-139">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-140">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-141">True</span><span class="sxs-lookup"><span data-stu-id="31903-141">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-142">Is Indexed</span></span>             | <span data-ttu-id="31903-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-143">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-144">In Global Catalog</span></span>      | <span data-ttu-id="31903-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-145">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-148">Range-Lower</span></span>            | <span data-ttu-id="31903-149">16</span><span class="sxs-lookup"><span data-stu-id="31903-149">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-150">Range-Upper</span></span>            | <span data-ttu-id="31903-151">16</span><span class="sxs-lookup"><span data-stu-id="31903-151">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-152">Search-Flags</span></span>           | <span data-ttu-id="31903-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-153">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-154">System-Flags</span></span>           | <span data-ttu-id="31903-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-155">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-156">Classes used in</span></span>        | [<span data-ttu-id="31903-157">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-157">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-158">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="31903-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31903-159">Windows Server 2003</span></span>



| <span data-ttu-id="31903-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-160">Entry</span></span> | <span data-ttu-id="31903-161">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-162">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-163">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-164">System-Only</span></span>            | <span data-ttu-id="31903-165">True</span><span class="sxs-lookup"><span data-stu-id="31903-165">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-166">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-167">True</span><span class="sxs-lookup"><span data-stu-id="31903-167">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-168">Is Indexed</span></span>             | <span data-ttu-id="31903-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-169">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-170">In Global Catalog</span></span>      | <span data-ttu-id="31903-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-171">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-174">Range-Lower</span></span>            | <span data-ttu-id="31903-175">16</span><span class="sxs-lookup"><span data-stu-id="31903-175">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-176">Range-Upper</span></span>            | <span data-ttu-id="31903-177">16</span><span class="sxs-lookup"><span data-stu-id="31903-177">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-178">Search-Flags</span></span>           | <span data-ttu-id="31903-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-179">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-180">System-Flags</span></span>           | <span data-ttu-id="31903-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-182">Classes used in</span></span>        | [<span data-ttu-id="31903-183">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-184">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="31903-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="31903-185">ADAM</span></span>



| <span data-ttu-id="31903-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-186">Entry</span></span> | <span data-ttu-id="31903-187">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-189">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-190">System-Only</span></span>            | <span data-ttu-id="31903-191">True</span><span class="sxs-lookup"><span data-stu-id="31903-191">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-192">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-193">True</span><span class="sxs-lookup"><span data-stu-id="31903-193">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-194">Is Indexed</span></span>             | <span data-ttu-id="31903-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-195">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-196">In Global Catalog</span></span>      | <span data-ttu-id="31903-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-197">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-199">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-200">Range-Lower</span></span>            | <span data-ttu-id="31903-201">16</span><span class="sxs-lookup"><span data-stu-id="31903-201">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-202">Range-Upper</span></span>            | <span data-ttu-id="31903-203">16</span><span class="sxs-lookup"><span data-stu-id="31903-203">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-204">Search-Flags</span></span>           | <span data-ttu-id="31903-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-205">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-206">System-Flags</span></span>           | <span data-ttu-id="31903-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-207">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-208">Classes used in</span></span>        | [<span data-ttu-id="31903-209">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-209">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-210">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-210">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="31903-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="31903-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="31903-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-212">Entry</span></span> | <span data-ttu-id="31903-213">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-213">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-214">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-215">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-216">System-Only</span></span>            | <span data-ttu-id="31903-217">True</span><span class="sxs-lookup"><span data-stu-id="31903-217">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-218">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-219">True</span><span class="sxs-lookup"><span data-stu-id="31903-219">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-220">Is Indexed</span></span>             | <span data-ttu-id="31903-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-221">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-222">In Global Catalog</span></span>      | <span data-ttu-id="31903-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-223">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-225">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-226">Range-Lower</span></span>            | <span data-ttu-id="31903-227">16</span><span class="sxs-lookup"><span data-stu-id="31903-227">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-228">Range-Upper</span></span>            | <span data-ttu-id="31903-229">16</span><span class="sxs-lookup"><span data-stu-id="31903-229">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-230">Search-Flags</span></span>           | <span data-ttu-id="31903-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-231">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-232">System-Flags</span></span>           | <span data-ttu-id="31903-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-233">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-234">Classes used in</span></span>        | [<span data-ttu-id="31903-235">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-235">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-236">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-236">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="31903-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31903-237">Windows Server 2008</span></span>



| <span data-ttu-id="31903-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-238">Entry</span></span> | <span data-ttu-id="31903-239">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-240">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-241">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-242">System-Only</span></span>            | <span data-ttu-id="31903-243">True</span><span class="sxs-lookup"><span data-stu-id="31903-243">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-244">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-245">True</span><span class="sxs-lookup"><span data-stu-id="31903-245">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-246">Is Indexed</span></span>             | <span data-ttu-id="31903-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-247">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-248">In Global Catalog</span></span>      | <span data-ttu-id="31903-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-249">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-251">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-252">Range-Lower</span></span>            | <span data-ttu-id="31903-253">16</span><span class="sxs-lookup"><span data-stu-id="31903-253">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-254">Range-Upper</span></span>            | <span data-ttu-id="31903-255">16</span><span class="sxs-lookup"><span data-stu-id="31903-255">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-256">Search-Flags</span></span>           | <span data-ttu-id="31903-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-257">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-258">System-Flags</span></span>           | <span data-ttu-id="31903-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-259">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-260">Classes used in</span></span>        | [<span data-ttu-id="31903-261">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-261">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-262">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-262">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="31903-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31903-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="31903-264">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-264">Entry</span></span> | <span data-ttu-id="31903-265">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-265">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-266">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-266">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-267">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-268">System-Only</span></span>            | <span data-ttu-id="31903-269">True</span><span class="sxs-lookup"><span data-stu-id="31903-269">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-270">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-270">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-271">True</span><span class="sxs-lookup"><span data-stu-id="31903-271">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-272">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-272">Is Indexed</span></span>             | <span data-ttu-id="31903-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-273">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-274">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-274">In Global Catalog</span></span>      | <span data-ttu-id="31903-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-275">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-276">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-277">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-277">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-278">Range-Lower</span></span>            | <span data-ttu-id="31903-279">16</span><span class="sxs-lookup"><span data-stu-id="31903-279">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-280">Range-Upper</span></span>            | <span data-ttu-id="31903-281">16</span><span class="sxs-lookup"><span data-stu-id="31903-281">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-282">Search-Flags</span></span>           | <span data-ttu-id="31903-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-283">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-284">System-Flags</span></span>           | <span data-ttu-id="31903-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-285">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-286">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-286">Classes used in</span></span>        | [<span data-ttu-id="31903-287">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-287">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-288">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-288">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="31903-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="31903-289">Windows Server 2012</span></span>



| <span data-ttu-id="31903-290">Ввод</span><span class="sxs-lookup"><span data-stu-id="31903-290">Entry</span></span> | <span data-ttu-id="31903-291">Значение</span><span class="sxs-lookup"><span data-stu-id="31903-291">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31903-292">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31903-292">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31903-293">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="31903-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="31903-294">System-Only</span></span>            | <span data-ttu-id="31903-295">True</span><span class="sxs-lookup"><span data-stu-id="31903-295">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-296">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31903-296">Is-Single-Valued</span></span>       | <span data-ttu-id="31903-297">True</span><span class="sxs-lookup"><span data-stu-id="31903-297">True</span></span>                                                                                                      |
| <span data-ttu-id="31903-298">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31903-298">Is Indexed</span></span>             | <span data-ttu-id="31903-299">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-299">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-300">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31903-300">In Global Catalog</span></span>      | <span data-ttu-id="31903-301">Неверно</span><span class="sxs-lookup"><span data-stu-id="31903-301">False</span></span>                                                                                                     |
| <span data-ttu-id="31903-302">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31903-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="31903-303">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31903-303">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="31903-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31903-304">Range-Lower</span></span>            | <span data-ttu-id="31903-305">16</span><span class="sxs-lookup"><span data-stu-id="31903-305">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31903-306">Range-Upper</span></span>            | <span data-ttu-id="31903-307">16</span><span class="sxs-lookup"><span data-stu-id="31903-307">16</span></span>                                                                                                        |
| <span data-ttu-id="31903-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-308">Search-Flags</span></span>           | <span data-ttu-id="31903-309">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31903-309">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="31903-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31903-310">System-Flags</span></span>           | <span data-ttu-id="31903-311">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31903-311">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="31903-312">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31903-312">Classes used in</span></span>        | [<span data-ttu-id="31903-313">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="31903-313">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="31903-314">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="31903-314">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





