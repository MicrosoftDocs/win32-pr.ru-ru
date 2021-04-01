---
title: Атрибут ms-DS-NC-REPL-Cursors
description: Список прошлых и существующих партнеров по репликации, а также их текущее количество.
ms.assetid: febe8614-b68a-4001-b6ae-dae3fe6eb25f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-NC-REPL-Cursors
- Схема AD атрибута msDS-Нкреплкурсорс
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Cursors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555a09520079df624fffb2cb3cb3aa34b81502c2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138646"
---
# <a name="ms-ds-nc-repl-cursors-attribute"></a><span data-ttu-id="76f0b-105">Атрибут ms-DS-NC-REPL-Cursors</span><span class="sxs-lookup"><span data-stu-id="76f0b-105">ms-DS-NC-Repl-Cursors attribute</span></span>

<span data-ttu-id="76f0b-106">Список прошлых и существующих партнеров по репликации, а также их текущее количество.</span><span class="sxs-lookup"><span data-stu-id="76f0b-106">A list of past and present replication partners, and how current we are with each of them.</span></span>



| <span data-ttu-id="76f0b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-107">Entry</span></span> | <span data-ttu-id="76f0b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="76f0b-109">CN</span><span class="sxs-lookup"><span data-stu-id="76f0b-109">CN</span></span>                | <span data-ttu-id="76f0b-110">MS-DS-NC-REPL-курсоры</span><span class="sxs-lookup"><span data-stu-id="76f0b-110">ms-DS-NC-Repl-Cursors</span></span>                       |
| <span data-ttu-id="76f0b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="76f0b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="76f0b-112">msDS-Нкреплкурсорс</span><span class="sxs-lookup"><span data-stu-id="76f0b-112">msDS-NCReplCursors</span></span>                          |
| <span data-ttu-id="76f0b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="76f0b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="76f0b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="76f0b-114">Update Privilege</span></span>  | <span data-ttu-id="76f0b-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="76f0b-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="76f0b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="76f0b-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="76f0b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-117">Attribute-Id</span></span>      | <span data-ttu-id="76f0b-118">1.2.840.113556.1.4.1704</span><span class="sxs-lookup"><span data-stu-id="76f0b-118">1.2.840.113556.1.4.1704</span></span>                     |
| <span data-ttu-id="76f0b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="76f0b-119">System-Id-Guid</span></span>    | <span data-ttu-id="76f0b-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span><span class="sxs-lookup"><span data-stu-id="76f0b-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span></span>        |
| <span data-ttu-id="76f0b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76f0b-121">Syntax</span></span>            | [<span data-ttu-id="76f0b-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="76f0b-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="76f0b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="76f0b-123">Implementations</span></span>

-   [<span data-ttu-id="76f0b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76f0b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76f0b-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="76f0b-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="76f0b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76f0b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76f0b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76f0b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76f0b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76f0b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76f0b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76f0b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="76f0b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76f0b-130">Windows Server 2003</span></span>



| <span data-ttu-id="76f0b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-131">Entry</span></span> | <span data-ttu-id="76f0b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76f0b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76f0b-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="76f0b-135">System-Only</span></span>            | <span data-ttu-id="76f0b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-136">False</span></span>                           |
| <span data-ttu-id="76f0b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76f0b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="76f0b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-138">False</span></span>                           |
| <span data-ttu-id="76f0b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76f0b-139">Is Indexed</span></span>             | <span data-ttu-id="76f0b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-140">False</span></span>                           |
| <span data-ttu-id="76f0b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76f0b-141">In Global Catalog</span></span>      | <span data-ttu-id="76f0b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-142">False</span></span>                           |
| <span data-ttu-id="76f0b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76f0b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="76f0b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76f0b-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76f0b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76f0b-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76f0b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76f0b-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76f0b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-147">Search-Flags</span></span>           | <span data-ttu-id="76f0b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76f0b-148">0x00000000</span></span>                      |
| <span data-ttu-id="76f0b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-149">System-Flags</span></span>           | <span data-ttu-id="76f0b-150">0x00000014</span><span class="sxs-lookup"><span data-stu-id="76f0b-150">0x00000014</span></span>                      |
| <span data-ttu-id="76f0b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76f0b-151">Classes used in</span></span>        | [<span data-ttu-id="76f0b-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76f0b-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="76f0b-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="76f0b-153">ADAM</span></span>



| <span data-ttu-id="76f0b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-154">Entry</span></span> | <span data-ttu-id="76f0b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76f0b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76f0b-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="76f0b-158">System-Only</span></span>            | <span data-ttu-id="76f0b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-159">False</span></span>                           |
| <span data-ttu-id="76f0b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76f0b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="76f0b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-161">False</span></span>                           |
| <span data-ttu-id="76f0b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76f0b-162">Is Indexed</span></span>             | <span data-ttu-id="76f0b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-163">False</span></span>                           |
| <span data-ttu-id="76f0b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76f0b-164">In Global Catalog</span></span>      | <span data-ttu-id="76f0b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-165">False</span></span>                           |
| <span data-ttu-id="76f0b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76f0b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="76f0b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76f0b-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76f0b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76f0b-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76f0b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76f0b-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76f0b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-170">Search-Flags</span></span>           | <span data-ttu-id="76f0b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76f0b-171">0x00000000</span></span>                      |
| <span data-ttu-id="76f0b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-172">System-Flags</span></span>           | <span data-ttu-id="76f0b-173">0x00000014</span><span class="sxs-lookup"><span data-stu-id="76f0b-173">0x00000014</span></span>                      |
| <span data-ttu-id="76f0b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76f0b-174">Classes used in</span></span>        | [<span data-ttu-id="76f0b-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76f0b-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76f0b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76f0b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76f0b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-177">Entry</span></span> | <span data-ttu-id="76f0b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76f0b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76f0b-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="76f0b-181">System-Only</span></span>            | <span data-ttu-id="76f0b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-182">False</span></span>                           |
| <span data-ttu-id="76f0b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76f0b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="76f0b-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-184">False</span></span>                           |
| <span data-ttu-id="76f0b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76f0b-185">Is Indexed</span></span>             | <span data-ttu-id="76f0b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-186">False</span></span>                           |
| <span data-ttu-id="76f0b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76f0b-187">In Global Catalog</span></span>      | <span data-ttu-id="76f0b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-188">False</span></span>                           |
| <span data-ttu-id="76f0b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76f0b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="76f0b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76f0b-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76f0b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76f0b-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76f0b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76f0b-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76f0b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-193">Search-Flags</span></span>           | <span data-ttu-id="76f0b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76f0b-194">0x00000000</span></span>                      |
| <span data-ttu-id="76f0b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-195">System-Flags</span></span>           | <span data-ttu-id="76f0b-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="76f0b-196">0x00000014</span></span>                      |
| <span data-ttu-id="76f0b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76f0b-197">Classes used in</span></span>        | [<span data-ttu-id="76f0b-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76f0b-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76f0b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76f0b-199">Windows Server 2008</span></span>



| <span data-ttu-id="76f0b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-200">Entry</span></span> | <span data-ttu-id="76f0b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76f0b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76f0b-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="76f0b-204">System-Only</span></span>            | <span data-ttu-id="76f0b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-205">False</span></span>                           |
| <span data-ttu-id="76f0b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76f0b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="76f0b-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-207">False</span></span>                           |
| <span data-ttu-id="76f0b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76f0b-208">Is Indexed</span></span>             | <span data-ttu-id="76f0b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-209">False</span></span>                           |
| <span data-ttu-id="76f0b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76f0b-210">In Global Catalog</span></span>      | <span data-ttu-id="76f0b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-211">False</span></span>                           |
| <span data-ttu-id="76f0b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76f0b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="76f0b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76f0b-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76f0b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76f0b-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76f0b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76f0b-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76f0b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-216">Search-Flags</span></span>           | <span data-ttu-id="76f0b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76f0b-217">0x00000000</span></span>                      |
| <span data-ttu-id="76f0b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-218">System-Flags</span></span>           | <span data-ttu-id="76f0b-219">0x00000014</span><span class="sxs-lookup"><span data-stu-id="76f0b-219">0x00000014</span></span>                      |
| <span data-ttu-id="76f0b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76f0b-220">Classes used in</span></span>        | [<span data-ttu-id="76f0b-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76f0b-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76f0b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76f0b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76f0b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-223">Entry</span></span> | <span data-ttu-id="76f0b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76f0b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76f0b-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="76f0b-227">System-Only</span></span>            | <span data-ttu-id="76f0b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-228">False</span></span>                           |
| <span data-ttu-id="76f0b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76f0b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="76f0b-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-230">False</span></span>                           |
| <span data-ttu-id="76f0b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76f0b-231">Is Indexed</span></span>             | <span data-ttu-id="76f0b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-232">False</span></span>                           |
| <span data-ttu-id="76f0b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76f0b-233">In Global Catalog</span></span>      | <span data-ttu-id="76f0b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-234">False</span></span>                           |
| <span data-ttu-id="76f0b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76f0b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="76f0b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76f0b-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76f0b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76f0b-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76f0b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76f0b-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76f0b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-239">Search-Flags</span></span>           | <span data-ttu-id="76f0b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76f0b-240">0x00000000</span></span>                      |
| <span data-ttu-id="76f0b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-241">System-Flags</span></span>           | <span data-ttu-id="76f0b-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="76f0b-242">0x00000014</span></span>                      |
| <span data-ttu-id="76f0b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76f0b-243">Classes used in</span></span>        | [<span data-ttu-id="76f0b-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76f0b-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76f0b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76f0b-245">Windows Server 2012</span></span>



| <span data-ttu-id="76f0b-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="76f0b-246">Entry</span></span> | <span data-ttu-id="76f0b-247">Значение</span><span class="sxs-lookup"><span data-stu-id="76f0b-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76f0b-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76f0b-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76f0b-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76f0b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="76f0b-250">System-Only</span></span>            | <span data-ttu-id="76f0b-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-251">False</span></span>                           |
| <span data-ttu-id="76f0b-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76f0b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="76f0b-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-253">False</span></span>                           |
| <span data-ttu-id="76f0b-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76f0b-254">Is Indexed</span></span>             | <span data-ttu-id="76f0b-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-255">False</span></span>                           |
| <span data-ttu-id="76f0b-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76f0b-256">In Global Catalog</span></span>      | <span data-ttu-id="76f0b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="76f0b-257">False</span></span>                           |
| <span data-ttu-id="76f0b-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76f0b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="76f0b-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76f0b-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76f0b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76f0b-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76f0b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76f0b-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76f0b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-262">Search-Flags</span></span>           | <span data-ttu-id="76f0b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76f0b-263">0x00000000</span></span>                      |
| <span data-ttu-id="76f0b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76f0b-264">System-Flags</span></span>           | <span data-ttu-id="76f0b-265">0x00000014</span><span class="sxs-lookup"><span data-stu-id="76f0b-265">0x00000014</span></span>                      |
| <span data-ttu-id="76f0b-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76f0b-266">Classes used in</span></span>        | [<span data-ttu-id="76f0b-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76f0b-267">**Top**</span></span>](c-top.md)<br/> |



 

 





