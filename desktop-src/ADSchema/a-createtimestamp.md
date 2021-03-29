---
title: Атрибут создания метки времени
description: Дата создания этого объекта. Это значение реплицируется.
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени создания
- Схема AD атрибута Креатетиместамп
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805099"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="79cd6-106">Атрибут создания метки времени</span><span class="sxs-lookup"><span data-stu-id="79cd6-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="79cd6-107">Дата создания этого объекта.</span><span class="sxs-lookup"><span data-stu-id="79cd6-107">The date when this object was created.</span></span> <span data-ttu-id="79cd6-108">Это значение реплицируется.</span><span class="sxs-lookup"><span data-stu-id="79cd6-108">This value is replicated.</span></span>



| <span data-ttu-id="79cd6-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-109">Entry</span></span> | <span data-ttu-id="79cd6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="79cd6-111">CN</span><span class="sxs-lookup"><span data-stu-id="79cd6-111">CN</span></span>                | <span data-ttu-id="79cd6-112">Метка времени создания</span><span class="sxs-lookup"><span data-stu-id="79cd6-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="79cd6-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="79cd6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="79cd6-114">креатетиместамп</span><span class="sxs-lookup"><span data-stu-id="79cd6-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="79cd6-115">Размер</span><span class="sxs-lookup"><span data-stu-id="79cd6-115">Size</span></span>              | <span data-ttu-id="79cd6-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="79cd6-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="79cd6-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="79cd6-117">Update Privilege</span></span>  | <span data-ttu-id="79cd6-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="79cd6-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="79cd6-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="79cd6-119">Update Frequency</span></span>  | <span data-ttu-id="79cd6-120">При создании объекта.</span><span class="sxs-lookup"><span data-stu-id="79cd6-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="79cd6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-121">Attribute-Id</span></span>      | <span data-ttu-id="79cd6-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="79cd6-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="79cd6-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="79cd6-123">System-Id-Guid</span></span>    | <span data-ttu-id="79cd6-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="79cd6-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="79cd6-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79cd6-125">Syntax</span></span>            | [<span data-ttu-id="79cd6-126">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="79cd6-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="79cd6-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="79cd6-127">Implementations</span></span>

-   [<span data-ttu-id="79cd6-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="79cd6-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="79cd6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79cd6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79cd6-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="79cd6-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="79cd6-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79cd6-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79cd6-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79cd6-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79cd6-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79cd6-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79cd6-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79cd6-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="79cd6-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79cd6-135">Windows 2000 Server</span></span>



| <span data-ttu-id="79cd6-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-136">Entry</span></span> | <span data-ttu-id="79cd6-137">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-140">System-Only</span></span>            | <span data-ttu-id="79cd6-141">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-141">True</span></span>                            |
| <span data-ttu-id="79cd6-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-142">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-143">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-143">True</span></span>                            |
| <span data-ttu-id="79cd6-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-144">Is Indexed</span></span>             | <span data-ttu-id="79cd6-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-145">False</span></span>                           |
| <span data-ttu-id="79cd6-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-146">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-147">False</span></span>                           |
| <span data-ttu-id="79cd6-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-152">Search-Flags</span></span>           | <span data-ttu-id="79cd6-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-153">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-154">System-Flags</span></span>           | <span data-ttu-id="79cd6-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-155">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-156">Classes used in</span></span>        | [<span data-ttu-id="79cd6-157">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="79cd6-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79cd6-158">Windows Server 2003</span></span>



| <span data-ttu-id="79cd6-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-159">Entry</span></span> | <span data-ttu-id="79cd6-160">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-163">System-Only</span></span>            | <span data-ttu-id="79cd6-164">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-164">True</span></span>                            |
| <span data-ttu-id="79cd6-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-165">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-166">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-166">True</span></span>                            |
| <span data-ttu-id="79cd6-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-167">Is Indexed</span></span>             | <span data-ttu-id="79cd6-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-168">False</span></span>                           |
| <span data-ttu-id="79cd6-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-169">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-170">False</span></span>                           |
| <span data-ttu-id="79cd6-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-175">Search-Flags</span></span>           | <span data-ttu-id="79cd6-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-176">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-177">System-Flags</span></span>           | <span data-ttu-id="79cd6-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-178">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-179">Classes used in</span></span>        | [<span data-ttu-id="79cd6-180">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="79cd6-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="79cd6-181">ADAM</span></span>



| <span data-ttu-id="79cd6-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-182">Entry</span></span> | <span data-ttu-id="79cd6-183">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-186">System-Only</span></span>            | <span data-ttu-id="79cd6-187">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-187">True</span></span>                            |
| <span data-ttu-id="79cd6-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-189">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-189">True</span></span>                            |
| <span data-ttu-id="79cd6-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-190">Is Indexed</span></span>             | <span data-ttu-id="79cd6-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-191">False</span></span>                           |
| <span data-ttu-id="79cd6-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-192">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-193">False</span></span>                           |
| <span data-ttu-id="79cd6-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-198">Search-Flags</span></span>           | <span data-ttu-id="79cd6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-199">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-200">System-Flags</span></span>           | <span data-ttu-id="79cd6-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-201">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-202">Classes used in</span></span>        | [<span data-ttu-id="79cd6-203">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79cd6-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79cd6-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79cd6-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-205">Entry</span></span> | <span data-ttu-id="79cd6-206">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-209">System-Only</span></span>            | <span data-ttu-id="79cd6-210">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-210">True</span></span>                            |
| <span data-ttu-id="79cd6-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-212">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-212">True</span></span>                            |
| <span data-ttu-id="79cd6-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-213">Is Indexed</span></span>             | <span data-ttu-id="79cd6-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-214">False</span></span>                           |
| <span data-ttu-id="79cd6-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-215">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-216">False</span></span>                           |
| <span data-ttu-id="79cd6-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-221">Search-Flags</span></span>           | <span data-ttu-id="79cd6-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-222">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-223">System-Flags</span></span>           | <span data-ttu-id="79cd6-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-224">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-225">Classes used in</span></span>        | [<span data-ttu-id="79cd6-226">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79cd6-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79cd6-227">Windows Server 2008</span></span>



| <span data-ttu-id="79cd6-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-228">Entry</span></span> | <span data-ttu-id="79cd6-229">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-232">System-Only</span></span>            | <span data-ttu-id="79cd6-233">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-233">True</span></span>                            |
| <span data-ttu-id="79cd6-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-235">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-235">True</span></span>                            |
| <span data-ttu-id="79cd6-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-236">Is Indexed</span></span>             | <span data-ttu-id="79cd6-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-237">False</span></span>                           |
| <span data-ttu-id="79cd6-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-238">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-239">False</span></span>                           |
| <span data-ttu-id="79cd6-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-244">Search-Flags</span></span>           | <span data-ttu-id="79cd6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-245">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-246">System-Flags</span></span>           | <span data-ttu-id="79cd6-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-247">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-248">Classes used in</span></span>        | [<span data-ttu-id="79cd6-249">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79cd6-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79cd6-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79cd6-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-251">Entry</span></span> | <span data-ttu-id="79cd6-252">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-255">System-Only</span></span>            | <span data-ttu-id="79cd6-256">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-256">True</span></span>                            |
| <span data-ttu-id="79cd6-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-257">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-258">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-258">True</span></span>                            |
| <span data-ttu-id="79cd6-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-259">Is Indexed</span></span>             | <span data-ttu-id="79cd6-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-260">False</span></span>                           |
| <span data-ttu-id="79cd6-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-261">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-262">False</span></span>                           |
| <span data-ttu-id="79cd6-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-267">Search-Flags</span></span>           | <span data-ttu-id="79cd6-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-268">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-269">System-Flags</span></span>           | <span data-ttu-id="79cd6-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-270">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-271">Classes used in</span></span>        | [<span data-ttu-id="79cd6-272">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79cd6-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79cd6-273">Windows Server 2012</span></span>



| <span data-ttu-id="79cd6-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="79cd6-274">Entry</span></span> | <span data-ttu-id="79cd6-275">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd6-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79cd6-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="79cd6-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79cd6-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="79cd6-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="79cd6-278">System-Only</span></span>            | <span data-ttu-id="79cd6-279">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-279">True</span></span>                            |
| <span data-ttu-id="79cd6-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="79cd6-280">Is-Single-Valued</span></span>       | <span data-ttu-id="79cd6-281">True</span><span class="sxs-lookup"><span data-stu-id="79cd6-281">True</span></span>                            |
| <span data-ttu-id="79cd6-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="79cd6-282">Is Indexed</span></span>             | <span data-ttu-id="79cd6-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-283">False</span></span>                           |
| <span data-ttu-id="79cd6-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="79cd6-284">In Global Catalog</span></span>      | <span data-ttu-id="79cd6-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="79cd6-285">False</span></span>                           |
| <span data-ttu-id="79cd6-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="79cd6-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="79cd6-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="79cd6-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79cd6-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79cd6-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="79cd6-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79cd6-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="79cd6-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-290">Search-Flags</span></span>           | <span data-ttu-id="79cd6-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79cd6-291">0x00000000</span></span>                      |
| <span data-ttu-id="79cd6-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79cd6-292">System-Flags</span></span>           | <span data-ttu-id="79cd6-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79cd6-293">0x08000014</span></span>                      |
| <span data-ttu-id="79cd6-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="79cd6-294">Classes used in</span></span>        | [<span data-ttu-id="79cd6-295">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="79cd6-295">**Top**</span></span>](c-top.md)<br/> |



 

 





