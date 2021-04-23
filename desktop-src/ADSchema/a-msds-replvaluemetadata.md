---
title: Атрибут ms-DS-REPL-value-Meta-Data
description: Список метаданных для каждого значения атрибута. Метаданные показывают, кто изменил значение последним.
ms.assetid: 79c01bda-ea1b-41ca-b4de-c16c5167b270
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-REPL-value-Meta-Data
- Схема AD атрибута msDS-Реплвалуеметадата
topic_type:
- apiref
api_name:
- ms-DS-Repl-Value-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e90cb5fd462fc75126b6ba80f10638826811d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655425"
---
# <a name="ms-ds-repl-value-meta-data-attribute"></a><span data-ttu-id="26742-106">Атрибут ms-DS-REPL-value-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="26742-106">ms-DS-Repl-Value-Meta-Data attribute</span></span>

<span data-ttu-id="26742-107">Список метаданных для каждого значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="26742-107">A list of metadata for each value of an attribute.</span></span> <span data-ttu-id="26742-108">Метаданные показывают, кто изменил значение последним.</span><span class="sxs-lookup"><span data-stu-id="26742-108">The metadata indicates who changed the value last.</span></span>



| <span data-ttu-id="26742-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-109">Entry</span></span> | <span data-ttu-id="26742-110">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="26742-111">CN</span><span class="sxs-lookup"><span data-stu-id="26742-111">CN</span></span>                | <span data-ttu-id="26742-112">MS-DS-REPL-value-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="26742-112">ms-DS-Repl-Value-Meta-Data</span></span>                  |
| <span data-ttu-id="26742-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="26742-113">Ldap-Display-Name</span></span> | <span data-ttu-id="26742-114">msDS-Реплвалуеметадата</span><span class="sxs-lookup"><span data-stu-id="26742-114">msDS-ReplValueMetaData</span></span>                      |
| <span data-ttu-id="26742-115">Размер</span><span class="sxs-lookup"><span data-stu-id="26742-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="26742-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="26742-116">Update Privilege</span></span>  | <span data-ttu-id="26742-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="26742-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="26742-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="26742-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="26742-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="26742-119">Attribute-Id</span></span>      | <span data-ttu-id="26742-120">1.2.840.113556.1.4.1708</span><span class="sxs-lookup"><span data-stu-id="26742-120">1.2.840.113556.1.4.1708</span></span>                     |
| <span data-ttu-id="26742-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="26742-121">System-Id-Guid</span></span>    | <span data-ttu-id="26742-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span><span class="sxs-lookup"><span data-stu-id="26742-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span></span>        |
| <span data-ttu-id="26742-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26742-123">Syntax</span></span>            | [<span data-ttu-id="26742-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="26742-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="26742-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="26742-125">Implementations</span></span>

-   [<span data-ttu-id="26742-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="26742-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="26742-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="26742-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="26742-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="26742-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="26742-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="26742-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="26742-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="26742-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="26742-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="26742-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="26742-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26742-132">Windows Server 2003</span></span>



| <span data-ttu-id="26742-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-133">Entry</span></span> | <span data-ttu-id="26742-134">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26742-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26742-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26742-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="26742-137">System-Only</span></span>            | <span data-ttu-id="26742-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-138">False</span></span>                           |
| <span data-ttu-id="26742-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26742-139">Is-Single-Valued</span></span>       | <span data-ttu-id="26742-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-140">False</span></span>                           |
| <span data-ttu-id="26742-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26742-141">Is Indexed</span></span>             | <span data-ttu-id="26742-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-142">False</span></span>                           |
| <span data-ttu-id="26742-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26742-143">In Global Catalog</span></span>      | <span data-ttu-id="26742-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-144">False</span></span>                           |
| <span data-ttu-id="26742-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26742-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="26742-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26742-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26742-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26742-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26742-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26742-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26742-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-149">Search-Flags</span></span>           | <span data-ttu-id="26742-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26742-150">0x00000000</span></span>                      |
| <span data-ttu-id="26742-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-151">System-Flags</span></span>           | <span data-ttu-id="26742-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="26742-152">0x00000014</span></span>                      |
| <span data-ttu-id="26742-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26742-153">Classes used in</span></span>        | [<span data-ttu-id="26742-154">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="26742-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="26742-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="26742-155">ADAM</span></span>



| <span data-ttu-id="26742-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-156">Entry</span></span> | <span data-ttu-id="26742-157">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26742-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26742-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26742-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="26742-160">System-Only</span></span>            | <span data-ttu-id="26742-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-161">False</span></span>                           |
| <span data-ttu-id="26742-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26742-162">Is-Single-Valued</span></span>       | <span data-ttu-id="26742-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-163">False</span></span>                           |
| <span data-ttu-id="26742-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26742-164">Is Indexed</span></span>             | <span data-ttu-id="26742-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-165">False</span></span>                           |
| <span data-ttu-id="26742-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26742-166">In Global Catalog</span></span>      | <span data-ttu-id="26742-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-167">False</span></span>                           |
| <span data-ttu-id="26742-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26742-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="26742-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26742-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26742-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26742-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26742-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26742-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26742-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-172">Search-Flags</span></span>           | <span data-ttu-id="26742-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26742-173">0x00000000</span></span>                      |
| <span data-ttu-id="26742-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-174">System-Flags</span></span>           | <span data-ttu-id="26742-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="26742-175">0x00000014</span></span>                      |
| <span data-ttu-id="26742-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26742-176">Classes used in</span></span>        | [<span data-ttu-id="26742-177">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="26742-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="26742-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="26742-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="26742-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-179">Entry</span></span> | <span data-ttu-id="26742-180">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26742-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26742-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26742-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="26742-183">System-Only</span></span>            | <span data-ttu-id="26742-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-184">False</span></span>                           |
| <span data-ttu-id="26742-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26742-185">Is-Single-Valued</span></span>       | <span data-ttu-id="26742-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-186">False</span></span>                           |
| <span data-ttu-id="26742-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26742-187">Is Indexed</span></span>             | <span data-ttu-id="26742-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-188">False</span></span>                           |
| <span data-ttu-id="26742-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26742-189">In Global Catalog</span></span>      | <span data-ttu-id="26742-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-190">False</span></span>                           |
| <span data-ttu-id="26742-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26742-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="26742-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26742-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26742-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26742-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26742-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26742-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26742-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-195">Search-Flags</span></span>           | <span data-ttu-id="26742-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26742-196">0x00000000</span></span>                      |
| <span data-ttu-id="26742-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-197">System-Flags</span></span>           | <span data-ttu-id="26742-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="26742-198">0x00000014</span></span>                      |
| <span data-ttu-id="26742-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26742-199">Classes used in</span></span>        | [<span data-ttu-id="26742-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="26742-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="26742-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26742-201">Windows Server 2008</span></span>



| <span data-ttu-id="26742-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-202">Entry</span></span> | <span data-ttu-id="26742-203">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26742-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26742-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26742-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="26742-206">System-Only</span></span>            | <span data-ttu-id="26742-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-207">False</span></span>                           |
| <span data-ttu-id="26742-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26742-208">Is-Single-Valued</span></span>       | <span data-ttu-id="26742-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-209">False</span></span>                           |
| <span data-ttu-id="26742-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26742-210">Is Indexed</span></span>             | <span data-ttu-id="26742-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-211">False</span></span>                           |
| <span data-ttu-id="26742-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26742-212">In Global Catalog</span></span>      | <span data-ttu-id="26742-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-213">False</span></span>                           |
| <span data-ttu-id="26742-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26742-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="26742-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26742-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26742-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26742-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26742-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26742-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26742-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-218">Search-Flags</span></span>           | <span data-ttu-id="26742-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26742-219">0x00000000</span></span>                      |
| <span data-ttu-id="26742-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-220">System-Flags</span></span>           | <span data-ttu-id="26742-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="26742-221">0x00000014</span></span>                      |
| <span data-ttu-id="26742-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26742-222">Classes used in</span></span>        | [<span data-ttu-id="26742-223">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="26742-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="26742-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26742-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="26742-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-225">Entry</span></span> | <span data-ttu-id="26742-226">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26742-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26742-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26742-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="26742-229">System-Only</span></span>            | <span data-ttu-id="26742-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-230">False</span></span>                           |
| <span data-ttu-id="26742-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26742-231">Is-Single-Valued</span></span>       | <span data-ttu-id="26742-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-232">False</span></span>                           |
| <span data-ttu-id="26742-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26742-233">Is Indexed</span></span>             | <span data-ttu-id="26742-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-234">False</span></span>                           |
| <span data-ttu-id="26742-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26742-235">In Global Catalog</span></span>      | <span data-ttu-id="26742-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-236">False</span></span>                           |
| <span data-ttu-id="26742-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26742-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="26742-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26742-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26742-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26742-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26742-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26742-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26742-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-241">Search-Flags</span></span>           | <span data-ttu-id="26742-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26742-242">0x00000000</span></span>                      |
| <span data-ttu-id="26742-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-243">System-Flags</span></span>           | <span data-ttu-id="26742-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="26742-244">0x00000014</span></span>                      |
| <span data-ttu-id="26742-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26742-245">Classes used in</span></span>        | [<span data-ttu-id="26742-246">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="26742-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="26742-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26742-247">Windows Server 2012</span></span>



| <span data-ttu-id="26742-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="26742-248">Entry</span></span> | <span data-ttu-id="26742-249">Значение</span><span class="sxs-lookup"><span data-stu-id="26742-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26742-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26742-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26742-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26742-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="26742-252">System-Only</span></span>            | <span data-ttu-id="26742-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-253">False</span></span>                           |
| <span data-ttu-id="26742-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26742-254">Is-Single-Valued</span></span>       | <span data-ttu-id="26742-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-255">False</span></span>                           |
| <span data-ttu-id="26742-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26742-256">Is Indexed</span></span>             | <span data-ttu-id="26742-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-257">False</span></span>                           |
| <span data-ttu-id="26742-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26742-258">In Global Catalog</span></span>      | <span data-ttu-id="26742-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="26742-259">False</span></span>                           |
| <span data-ttu-id="26742-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26742-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="26742-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26742-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26742-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26742-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26742-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26742-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26742-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-264">Search-Flags</span></span>           | <span data-ttu-id="26742-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26742-265">0x00000000</span></span>                      |
| <span data-ttu-id="26742-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26742-266">System-Flags</span></span>           | <span data-ttu-id="26742-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="26742-267">0x00000014</span></span>                      |
| <span data-ttu-id="26742-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26742-268">Classes used in</span></span>        | [<span data-ttu-id="26742-269">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="26742-269">**Top**</span></span>](c-top.md)<br/> |



 

 





