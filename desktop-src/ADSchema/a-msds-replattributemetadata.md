---
title: Атрибут ms-DS-REPL-Attribute-Meta-Data
description: Список метаданных для каждого реплицированного атрибута. Метаданные показывают, кто изменил атрибут в последний раз.
ms.assetid: 07cfd323-eb90-4715-9307-583cf7e9f63e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-REPL-Attribute-Meta-Data
- Схема AD атрибута msDS-Реплаттрибутеметадата
topic_type:
- apiref
api_name:
- ms-DS-Repl-Attribute-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc991ead7104d8b9b4c023882d39adf1d53446
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655171"
---
# <a name="ms-ds-repl-attribute-meta-data-attribute"></a><span data-ttu-id="c6804-106">Атрибут ms-DS-REPL-Attribute-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="c6804-106">ms-DS-Repl-Attribute-Meta-Data attribute</span></span>

<span data-ttu-id="c6804-107">Список метаданных для каждого реплицированного атрибута.</span><span class="sxs-lookup"><span data-stu-id="c6804-107">A list of metadata for each replicated attribute.</span></span> <span data-ttu-id="c6804-108">Метаданные показывают, кто изменил атрибут в последний раз.</span><span class="sxs-lookup"><span data-stu-id="c6804-108">The metadata indicates who changed the attribute last.</span></span>



| <span data-ttu-id="c6804-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-109">Entry</span></span> | <span data-ttu-id="c6804-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c6804-111">CN</span><span class="sxs-lookup"><span data-stu-id="c6804-111">CN</span></span>                | <span data-ttu-id="c6804-112">MS-DS-REPL-Attribute-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="c6804-112">ms-DS-Repl-Attribute-Meta-Data</span></span>              |
| <span data-ttu-id="c6804-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c6804-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c6804-114">msDS-Реплаттрибутеметадата</span><span class="sxs-lookup"><span data-stu-id="c6804-114">msDS-ReplAttributeMetaData</span></span>                  |
| <span data-ttu-id="c6804-115">Размер</span><span class="sxs-lookup"><span data-stu-id="c6804-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="c6804-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c6804-116">Update Privilege</span></span>  | <span data-ttu-id="c6804-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c6804-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="c6804-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c6804-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c6804-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-119">Attribute-Id</span></span>      | <span data-ttu-id="c6804-120">1.2.840.113556.1.4.1707</span><span class="sxs-lookup"><span data-stu-id="c6804-120">1.2.840.113556.1.4.1707</span></span>                     |
| <span data-ttu-id="c6804-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c6804-121">System-Id-Guid</span></span>    | <span data-ttu-id="c6804-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span><span class="sxs-lookup"><span data-stu-id="c6804-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span></span>        |
| <span data-ttu-id="c6804-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6804-123">Syntax</span></span>            | [<span data-ttu-id="c6804-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c6804-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c6804-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c6804-125">Implementations</span></span>

-   [<span data-ttu-id="c6804-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c6804-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c6804-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c6804-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c6804-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c6804-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c6804-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c6804-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c6804-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c6804-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c6804-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c6804-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c6804-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6804-132">Windows Server 2003</span></span>



| <span data-ttu-id="c6804-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-133">Entry</span></span> | <span data-ttu-id="c6804-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6804-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6804-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6804-137">System-Only</span></span>            | <span data-ttu-id="c6804-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-138">False</span></span>                           |
| <span data-ttu-id="c6804-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6804-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c6804-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-140">False</span></span>                           |
| <span data-ttu-id="c6804-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6804-141">Is Indexed</span></span>             | <span data-ttu-id="c6804-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-142">False</span></span>                           |
| <span data-ttu-id="c6804-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6804-143">In Global Catalog</span></span>      | <span data-ttu-id="c6804-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-144">False</span></span>                           |
| <span data-ttu-id="c6804-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6804-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6804-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6804-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6804-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6804-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6804-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6804-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6804-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-149">Search-Flags</span></span>           | <span data-ttu-id="c6804-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6804-150">0x00000000</span></span>                      |
| <span data-ttu-id="c6804-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-151">System-Flags</span></span>           | <span data-ttu-id="c6804-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c6804-152">0x00000014</span></span>                      |
| <span data-ttu-id="c6804-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6804-153">Classes used in</span></span>        | [<span data-ttu-id="c6804-154">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6804-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c6804-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="c6804-155">ADAM</span></span>



| <span data-ttu-id="c6804-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-156">Entry</span></span> | <span data-ttu-id="c6804-157">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6804-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6804-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6804-160">System-Only</span></span>            | <span data-ttu-id="c6804-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-161">False</span></span>                           |
| <span data-ttu-id="c6804-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6804-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c6804-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-163">False</span></span>                           |
| <span data-ttu-id="c6804-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6804-164">Is Indexed</span></span>             | <span data-ttu-id="c6804-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-165">False</span></span>                           |
| <span data-ttu-id="c6804-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6804-166">In Global Catalog</span></span>      | <span data-ttu-id="c6804-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-167">False</span></span>                           |
| <span data-ttu-id="c6804-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6804-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6804-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6804-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6804-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6804-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6804-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6804-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6804-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-172">Search-Flags</span></span>           | <span data-ttu-id="c6804-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6804-173">0x00000000</span></span>                      |
| <span data-ttu-id="c6804-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-174">System-Flags</span></span>           | <span data-ttu-id="c6804-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c6804-175">0x00000014</span></span>                      |
| <span data-ttu-id="c6804-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6804-176">Classes used in</span></span>        | [<span data-ttu-id="c6804-177">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6804-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c6804-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c6804-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c6804-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-179">Entry</span></span> | <span data-ttu-id="c6804-180">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6804-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6804-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6804-183">System-Only</span></span>            | <span data-ttu-id="c6804-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-184">False</span></span>                           |
| <span data-ttu-id="c6804-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6804-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c6804-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-186">False</span></span>                           |
| <span data-ttu-id="c6804-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6804-187">Is Indexed</span></span>             | <span data-ttu-id="c6804-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-188">False</span></span>                           |
| <span data-ttu-id="c6804-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6804-189">In Global Catalog</span></span>      | <span data-ttu-id="c6804-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-190">False</span></span>                           |
| <span data-ttu-id="c6804-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6804-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6804-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6804-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6804-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6804-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6804-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6804-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6804-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-195">Search-Flags</span></span>           | <span data-ttu-id="c6804-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6804-196">0x00000000</span></span>                      |
| <span data-ttu-id="c6804-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-197">System-Flags</span></span>           | <span data-ttu-id="c6804-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c6804-198">0x00000014</span></span>                      |
| <span data-ttu-id="c6804-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6804-199">Classes used in</span></span>        | [<span data-ttu-id="c6804-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6804-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c6804-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6804-201">Windows Server 2008</span></span>



| <span data-ttu-id="c6804-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-202">Entry</span></span> | <span data-ttu-id="c6804-203">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6804-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6804-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6804-206">System-Only</span></span>            | <span data-ttu-id="c6804-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-207">False</span></span>                           |
| <span data-ttu-id="c6804-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6804-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c6804-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-209">False</span></span>                           |
| <span data-ttu-id="c6804-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6804-210">Is Indexed</span></span>             | <span data-ttu-id="c6804-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-211">False</span></span>                           |
| <span data-ttu-id="c6804-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6804-212">In Global Catalog</span></span>      | <span data-ttu-id="c6804-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-213">False</span></span>                           |
| <span data-ttu-id="c6804-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6804-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6804-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6804-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6804-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6804-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6804-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6804-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6804-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-218">Search-Flags</span></span>           | <span data-ttu-id="c6804-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6804-219">0x00000000</span></span>                      |
| <span data-ttu-id="c6804-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-220">System-Flags</span></span>           | <span data-ttu-id="c6804-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c6804-221">0x00000014</span></span>                      |
| <span data-ttu-id="c6804-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6804-222">Classes used in</span></span>        | [<span data-ttu-id="c6804-223">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6804-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c6804-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6804-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c6804-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-225">Entry</span></span> | <span data-ttu-id="c6804-226">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6804-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6804-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6804-229">System-Only</span></span>            | <span data-ttu-id="c6804-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-230">False</span></span>                           |
| <span data-ttu-id="c6804-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6804-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c6804-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-232">False</span></span>                           |
| <span data-ttu-id="c6804-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6804-233">Is Indexed</span></span>             | <span data-ttu-id="c6804-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-234">False</span></span>                           |
| <span data-ttu-id="c6804-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6804-235">In Global Catalog</span></span>      | <span data-ttu-id="c6804-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-236">False</span></span>                           |
| <span data-ttu-id="c6804-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6804-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6804-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6804-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6804-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6804-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6804-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6804-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6804-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-241">Search-Flags</span></span>           | <span data-ttu-id="c6804-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6804-242">0x00000000</span></span>                      |
| <span data-ttu-id="c6804-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-243">System-Flags</span></span>           | <span data-ttu-id="c6804-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c6804-244">0x00000014</span></span>                      |
| <span data-ttu-id="c6804-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6804-245">Classes used in</span></span>        | [<span data-ttu-id="c6804-246">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6804-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c6804-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6804-247">Windows Server 2012</span></span>



| <span data-ttu-id="c6804-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6804-248">Entry</span></span> | <span data-ttu-id="c6804-249">Значение</span><span class="sxs-lookup"><span data-stu-id="c6804-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6804-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6804-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6804-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6804-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6804-252">System-Only</span></span>            | <span data-ttu-id="c6804-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-253">False</span></span>                           |
| <span data-ttu-id="c6804-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6804-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c6804-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-255">False</span></span>                           |
| <span data-ttu-id="c6804-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6804-256">Is Indexed</span></span>             | <span data-ttu-id="c6804-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-257">False</span></span>                           |
| <span data-ttu-id="c6804-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6804-258">In Global Catalog</span></span>      | <span data-ttu-id="c6804-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6804-259">False</span></span>                           |
| <span data-ttu-id="c6804-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6804-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6804-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6804-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6804-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6804-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6804-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6804-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6804-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-264">Search-Flags</span></span>           | <span data-ttu-id="c6804-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6804-265">0x00000000</span></span>                      |
| <span data-ttu-id="c6804-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6804-266">System-Flags</span></span>           | <span data-ttu-id="c6804-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c6804-267">0x00000014</span></span>                      |
| <span data-ttu-id="c6804-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6804-268">Classes used in</span></span>        | [<span data-ttu-id="c6804-269">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6804-269">**Top**</span></span>](c-top.md)<br/> |



 

 





