---
title: Атрибут ms-DS-Schema-Extensions
description: Двоичный BLOB-объект, используемый для хранения сведений о расширениях объектов схемы.
ms.assetid: a2ffc4c6-ec33-4265-9a1e-c07597d2af50
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-Schema-Extensions
- msDs-Schema-Extensions атрибут AD
topic_type:
- apiref
api_name:
- ms-ds-Schema-Extensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f524e28f2d45d03f7851fc46d32e986968f81bfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494013"
---
# <a name="ms-ds-schema-extensions-attribute"></a><span data-ttu-id="12761-105">Атрибут ms-DS-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="12761-105">ms-ds-Schema-Extensions attribute</span></span>

<span data-ttu-id="12761-106">Двоичный BLOB-объект, используемый для хранения сведений о расширениях объектов схемы.</span><span class="sxs-lookup"><span data-stu-id="12761-106">A binary BLOB used to store information about extensions to schema objects.</span></span>



| <span data-ttu-id="12761-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-107">Entry</span></span> | <span data-ttu-id="12761-108">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="12761-109">CN</span><span class="sxs-lookup"><span data-stu-id="12761-109">CN</span></span>                | <span data-ttu-id="12761-110">Расширения MS-DS-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="12761-110">ms-ds-Schema-Extensions</span></span>                               |
| <span data-ttu-id="12761-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="12761-111">Ldap-Display-Name</span></span> | <span data-ttu-id="12761-112">msDs-расширения схемы</span><span class="sxs-lookup"><span data-stu-id="12761-112">msDs-Schema-Extensions</span></span>                                |
| <span data-ttu-id="12761-113">Размер</span><span class="sxs-lookup"><span data-stu-id="12761-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="12761-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="12761-114">Update Privilege</span></span>  | <span data-ttu-id="12761-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="12761-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="12761-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="12761-116">Update Frequency</span></span>  | <span data-ttu-id="12761-117">При расширении схемы.</span><span class="sxs-lookup"><span data-stu-id="12761-117">When the schema is extended.</span></span>                          |
| <span data-ttu-id="12761-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="12761-118">Attribute-Id</span></span>      | <span data-ttu-id="12761-119">1.2.840.113556.1.4.1440</span><span class="sxs-lookup"><span data-stu-id="12761-119">1.2.840.113556.1.4.1440</span></span>                               |
| <span data-ttu-id="12761-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="12761-120">System-Id-Guid</span></span>    | <span data-ttu-id="12761-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span><span class="sxs-lookup"><span data-stu-id="12761-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span></span>                  |
| <span data-ttu-id="12761-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12761-122">Syntax</span></span>            | [<span data-ttu-id="12761-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="12761-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="12761-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="12761-124">Implementations</span></span>

-   [<span data-ttu-id="12761-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="12761-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="12761-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="12761-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="12761-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="12761-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="12761-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="12761-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="12761-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="12761-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="12761-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="12761-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="12761-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12761-131">Windows Server 2003</span></span>



| <span data-ttu-id="12761-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-132">Entry</span></span> | <span data-ttu-id="12761-133">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12761-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="12761-134">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12761-135">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="12761-136">System-Only</span></span>            | <span data-ttu-id="12761-137">True</span><span class="sxs-lookup"><span data-stu-id="12761-137">True</span></span>                                                                                                                                      |
| <span data-ttu-id="12761-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="12761-138">Is-Single-Valued</span></span>       | <span data-ttu-id="12761-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-139">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="12761-140">Is Indexed</span></span>             | <span data-ttu-id="12761-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-141">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="12761-142">In Global Catalog</span></span>      | <span data-ttu-id="12761-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-143">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="12761-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="12761-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12761-145">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="12761-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12761-146">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12761-147">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-148">Search-Flags</span></span>           | <span data-ttu-id="12761-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12761-149">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="12761-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-150">System-Flags</span></span>           | <span data-ttu-id="12761-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12761-151">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="12761-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="12761-152">Classes used in</span></span>        | [<span data-ttu-id="12761-153">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="12761-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="12761-154">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="12761-154">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="12761-155">**дмд**</span><span class="sxs-lookup"><span data-stu-id="12761-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="12761-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="12761-156">ADAM</span></span>



| <span data-ttu-id="12761-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-157">Entry</span></span> | <span data-ttu-id="12761-158">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12761-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="12761-159">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12761-160">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="12761-161">System-Only</span></span>            | <span data-ttu-id="12761-162">True</span><span class="sxs-lookup"><span data-stu-id="12761-162">True</span></span>                                                                                                                                      |
| <span data-ttu-id="12761-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="12761-163">Is-Single-Valued</span></span>       | <span data-ttu-id="12761-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-164">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="12761-165">Is Indexed</span></span>             | <span data-ttu-id="12761-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-166">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="12761-167">In Global Catalog</span></span>      | <span data-ttu-id="12761-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-168">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="12761-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="12761-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12761-170">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="12761-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12761-171">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12761-172">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-173">Search-Flags</span></span>           | <span data-ttu-id="12761-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12761-174">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="12761-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-175">System-Flags</span></span>           | <span data-ttu-id="12761-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12761-176">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="12761-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="12761-177">Classes used in</span></span>        | [<span data-ttu-id="12761-178">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="12761-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="12761-179">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="12761-179">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="12761-180">**дмд**</span><span class="sxs-lookup"><span data-stu-id="12761-180">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="12761-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="12761-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="12761-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-182">Entry</span></span> | <span data-ttu-id="12761-183">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12761-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="12761-184">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12761-185">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="12761-186">System-Only</span></span>            | <span data-ttu-id="12761-187">True</span><span class="sxs-lookup"><span data-stu-id="12761-187">True</span></span>                                                                                                                                      |
| <span data-ttu-id="12761-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="12761-188">Is-Single-Valued</span></span>       | <span data-ttu-id="12761-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-189">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="12761-190">Is Indexed</span></span>             | <span data-ttu-id="12761-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-191">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="12761-192">In Global Catalog</span></span>      | <span data-ttu-id="12761-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-193">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="12761-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="12761-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12761-195">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="12761-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12761-196">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12761-197">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-198">Search-Flags</span></span>           | <span data-ttu-id="12761-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12761-199">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="12761-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-200">System-Flags</span></span>           | <span data-ttu-id="12761-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12761-201">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="12761-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="12761-202">Classes used in</span></span>        | [<span data-ttu-id="12761-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="12761-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="12761-204">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="12761-204">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="12761-205">**дмд**</span><span class="sxs-lookup"><span data-stu-id="12761-205">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="12761-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12761-206">Windows Server 2008</span></span>



| <span data-ttu-id="12761-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-207">Entry</span></span> | <span data-ttu-id="12761-208">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12761-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="12761-209">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12761-210">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="12761-211">System-Only</span></span>            | <span data-ttu-id="12761-212">True</span><span class="sxs-lookup"><span data-stu-id="12761-212">True</span></span>                                                                                                                                      |
| <span data-ttu-id="12761-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="12761-213">Is-Single-Valued</span></span>       | <span data-ttu-id="12761-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-214">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="12761-215">Is Indexed</span></span>             | <span data-ttu-id="12761-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-216">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="12761-217">In Global Catalog</span></span>      | <span data-ttu-id="12761-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-218">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="12761-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="12761-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12761-220">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="12761-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12761-221">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12761-222">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-223">Search-Flags</span></span>           | <span data-ttu-id="12761-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12761-224">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="12761-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-225">System-Flags</span></span>           | <span data-ttu-id="12761-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12761-226">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="12761-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="12761-227">Classes used in</span></span>        | [<span data-ttu-id="12761-228">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="12761-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="12761-229">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="12761-229">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="12761-230">**дмд**</span><span class="sxs-lookup"><span data-stu-id="12761-230">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="12761-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12761-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="12761-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-232">Entry</span></span> | <span data-ttu-id="12761-233">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12761-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="12761-234">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12761-235">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="12761-236">System-Only</span></span>            | <span data-ttu-id="12761-237">True</span><span class="sxs-lookup"><span data-stu-id="12761-237">True</span></span>                                                                                                                                      |
| <span data-ttu-id="12761-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="12761-238">Is-Single-Valued</span></span>       | <span data-ttu-id="12761-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-239">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="12761-240">Is Indexed</span></span>             | <span data-ttu-id="12761-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-241">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="12761-242">In Global Catalog</span></span>      | <span data-ttu-id="12761-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-243">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="12761-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="12761-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12761-245">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="12761-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12761-246">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12761-247">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-248">Search-Flags</span></span>           | <span data-ttu-id="12761-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12761-249">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="12761-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-250">System-Flags</span></span>           | <span data-ttu-id="12761-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12761-251">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="12761-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="12761-252">Classes used in</span></span>        | [<span data-ttu-id="12761-253">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="12761-253">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="12761-254">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="12761-254">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="12761-255">**дмд**</span><span class="sxs-lookup"><span data-stu-id="12761-255">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="12761-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12761-256">Windows Server 2012</span></span>



| <span data-ttu-id="12761-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="12761-257">Entry</span></span> | <span data-ttu-id="12761-258">Значение</span><span class="sxs-lookup"><span data-stu-id="12761-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12761-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="12761-259">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12761-260">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="12761-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="12761-261">System-Only</span></span>            | <span data-ttu-id="12761-262">True</span><span class="sxs-lookup"><span data-stu-id="12761-262">True</span></span>                                                                                                                                      |
| <span data-ttu-id="12761-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="12761-263">Is-Single-Valued</span></span>       | <span data-ttu-id="12761-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-264">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="12761-265">Is Indexed</span></span>             | <span data-ttu-id="12761-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-266">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="12761-267">In Global Catalog</span></span>      | <span data-ttu-id="12761-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="12761-268">False</span></span>                                                                                                                                     |
| <span data-ttu-id="12761-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="12761-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="12761-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12761-270">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="12761-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12761-271">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12761-272">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="12761-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-273">Search-Flags</span></span>           | <span data-ttu-id="12761-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12761-274">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="12761-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12761-275">System-Flags</span></span>           | <span data-ttu-id="12761-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12761-276">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="12761-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="12761-277">Classes used in</span></span>        | [<span data-ttu-id="12761-278">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="12761-278">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="12761-279">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="12761-279">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="12761-280">**дмд**</span><span class="sxs-lookup"><span data-stu-id="12761-280">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





