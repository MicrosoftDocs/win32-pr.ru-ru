---
title: RID-распределение — атрибут пула
description: Пул, который был предварительно выбран для использования диспетчером RID при использовании RID-Previous-распределения-пула.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "выделение RID — пул"
- Схема AD атрибута Ридаллокатионпул
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655067"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="333ae-105">RID-распределение — атрибут пула</span><span class="sxs-lookup"><span data-stu-id="333ae-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="333ae-106">Пул, который был предварительно выбран для использования диспетчером RID при использовании RID-Previous-распределения-пула.</span><span class="sxs-lookup"><span data-stu-id="333ae-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="333ae-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-107">Entry</span></span> | <span data-ttu-id="333ae-108">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="333ae-109">CN</span><span class="sxs-lookup"><span data-stu-id="333ae-109">CN</span></span>                | <span data-ttu-id="333ae-110">RID-распределение — пул</span><span class="sxs-lookup"><span data-stu-id="333ae-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="333ae-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="333ae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="333ae-112">ридаллокатионпул</span><span class="sxs-lookup"><span data-stu-id="333ae-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="333ae-113">Размер</span><span class="sxs-lookup"><span data-stu-id="333ae-113">Size</span></span>              | <span data-ttu-id="333ae-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="333ae-114">8 bytes</span></span>                              |
| <span data-ttu-id="333ae-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="333ae-115">Update Privilege</span></span>  | <span data-ttu-id="333ae-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="333ae-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="333ae-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="333ae-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="333ae-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-118">Attribute-Id</span></span>      | <span data-ttu-id="333ae-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="333ae-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="333ae-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="333ae-120">System-Id-Guid</span></span>    | <span data-ttu-id="333ae-121">66171889-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="333ae-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="333ae-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="333ae-122">Syntax</span></span>            | [<span data-ttu-id="333ae-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="333ae-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="333ae-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="333ae-124">Implementations</span></span>

-   [<span data-ttu-id="333ae-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="333ae-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="333ae-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="333ae-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="333ae-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="333ae-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="333ae-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="333ae-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="333ae-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="333ae-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="333ae-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="333ae-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="333ae-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="333ae-131">Windows 2000 Server</span></span>



| <span data-ttu-id="333ae-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-132">Entry</span></span> | <span data-ttu-id="333ae-133">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="333ae-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="333ae-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="333ae-136">System-Only</span></span>            | <span data-ttu-id="333ae-137">True</span><span class="sxs-lookup"><span data-stu-id="333ae-137">True</span></span>                                   |
| <span data-ttu-id="333ae-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="333ae-138">Is-Single-Valued</span></span>       | <span data-ttu-id="333ae-139">True</span><span class="sxs-lookup"><span data-stu-id="333ae-139">True</span></span>                                   |
| <span data-ttu-id="333ae-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="333ae-140">Is Indexed</span></span>             | <span data-ttu-id="333ae-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-141">False</span></span>                                  |
| <span data-ttu-id="333ae-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="333ae-142">In Global Catalog</span></span>      | <span data-ttu-id="333ae-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-143">False</span></span>                                  |
| <span data-ttu-id="333ae-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="333ae-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="333ae-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="333ae-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="333ae-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="333ae-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="333ae-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="333ae-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="333ae-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-148">Search-Flags</span></span>           | <span data-ttu-id="333ae-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="333ae-149">0x00000000</span></span>                             |
| <span data-ttu-id="333ae-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-150">System-Flags</span></span>           | <span data-ttu-id="333ae-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="333ae-151">0x00000010</span></span>                             |
| <span data-ttu-id="333ae-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="333ae-152">Classes used in</span></span>        | [<span data-ttu-id="333ae-153">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="333ae-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="333ae-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="333ae-154">Windows Server 2003</span></span>



| <span data-ttu-id="333ae-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-155">Entry</span></span> | <span data-ttu-id="333ae-156">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="333ae-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="333ae-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="333ae-159">System-Only</span></span>            | <span data-ttu-id="333ae-160">True</span><span class="sxs-lookup"><span data-stu-id="333ae-160">True</span></span>                                   |
| <span data-ttu-id="333ae-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="333ae-161">Is-Single-Valued</span></span>       | <span data-ttu-id="333ae-162">True</span><span class="sxs-lookup"><span data-stu-id="333ae-162">True</span></span>                                   |
| <span data-ttu-id="333ae-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="333ae-163">Is Indexed</span></span>             | <span data-ttu-id="333ae-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-164">False</span></span>                                  |
| <span data-ttu-id="333ae-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="333ae-165">In Global Catalog</span></span>      | <span data-ttu-id="333ae-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-166">False</span></span>                                  |
| <span data-ttu-id="333ae-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="333ae-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="333ae-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="333ae-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="333ae-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="333ae-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="333ae-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="333ae-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="333ae-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-171">Search-Flags</span></span>           | <span data-ttu-id="333ae-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="333ae-172">0x00000000</span></span>                             |
| <span data-ttu-id="333ae-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-173">System-Flags</span></span>           | <span data-ttu-id="333ae-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="333ae-174">0x00000010</span></span>                             |
| <span data-ttu-id="333ae-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="333ae-175">Classes used in</span></span>        | [<span data-ttu-id="333ae-176">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="333ae-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="333ae-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="333ae-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="333ae-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-178">Entry</span></span> | <span data-ttu-id="333ae-179">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="333ae-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="333ae-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="333ae-182">System-Only</span></span>            | <span data-ttu-id="333ae-183">True</span><span class="sxs-lookup"><span data-stu-id="333ae-183">True</span></span>                                   |
| <span data-ttu-id="333ae-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="333ae-184">Is-Single-Valued</span></span>       | <span data-ttu-id="333ae-185">True</span><span class="sxs-lookup"><span data-stu-id="333ae-185">True</span></span>                                   |
| <span data-ttu-id="333ae-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="333ae-186">Is Indexed</span></span>             | <span data-ttu-id="333ae-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-187">False</span></span>                                  |
| <span data-ttu-id="333ae-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="333ae-188">In Global Catalog</span></span>      | <span data-ttu-id="333ae-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-189">False</span></span>                                  |
| <span data-ttu-id="333ae-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="333ae-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="333ae-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="333ae-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="333ae-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="333ae-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="333ae-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="333ae-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="333ae-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-194">Search-Flags</span></span>           | <span data-ttu-id="333ae-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="333ae-195">0x00000000</span></span>                             |
| <span data-ttu-id="333ae-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-196">System-Flags</span></span>           | <span data-ttu-id="333ae-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="333ae-197">0x00000010</span></span>                             |
| <span data-ttu-id="333ae-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="333ae-198">Classes used in</span></span>        | [<span data-ttu-id="333ae-199">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="333ae-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="333ae-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="333ae-200">Windows Server 2008</span></span>



| <span data-ttu-id="333ae-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-201">Entry</span></span> | <span data-ttu-id="333ae-202">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="333ae-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="333ae-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="333ae-205">System-Only</span></span>            | <span data-ttu-id="333ae-206">True</span><span class="sxs-lookup"><span data-stu-id="333ae-206">True</span></span>                                   |
| <span data-ttu-id="333ae-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="333ae-207">Is-Single-Valued</span></span>       | <span data-ttu-id="333ae-208">True</span><span class="sxs-lookup"><span data-stu-id="333ae-208">True</span></span>                                   |
| <span data-ttu-id="333ae-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="333ae-209">Is Indexed</span></span>             | <span data-ttu-id="333ae-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-210">False</span></span>                                  |
| <span data-ttu-id="333ae-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="333ae-211">In Global Catalog</span></span>      | <span data-ttu-id="333ae-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-212">False</span></span>                                  |
| <span data-ttu-id="333ae-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="333ae-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="333ae-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="333ae-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="333ae-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="333ae-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="333ae-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="333ae-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="333ae-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-217">Search-Flags</span></span>           | <span data-ttu-id="333ae-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="333ae-218">0x00000000</span></span>                             |
| <span data-ttu-id="333ae-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-219">System-Flags</span></span>           | <span data-ttu-id="333ae-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="333ae-220">0x00000010</span></span>                             |
| <span data-ttu-id="333ae-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="333ae-221">Classes used in</span></span>        | [<span data-ttu-id="333ae-222">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="333ae-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="333ae-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="333ae-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="333ae-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-224">Entry</span></span> | <span data-ttu-id="333ae-225">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="333ae-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="333ae-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="333ae-228">System-Only</span></span>            | <span data-ttu-id="333ae-229">True</span><span class="sxs-lookup"><span data-stu-id="333ae-229">True</span></span>                                   |
| <span data-ttu-id="333ae-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="333ae-230">Is-Single-Valued</span></span>       | <span data-ttu-id="333ae-231">True</span><span class="sxs-lookup"><span data-stu-id="333ae-231">True</span></span>                                   |
| <span data-ttu-id="333ae-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="333ae-232">Is Indexed</span></span>             | <span data-ttu-id="333ae-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-233">False</span></span>                                  |
| <span data-ttu-id="333ae-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="333ae-234">In Global Catalog</span></span>      | <span data-ttu-id="333ae-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-235">False</span></span>                                  |
| <span data-ttu-id="333ae-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="333ae-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="333ae-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="333ae-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="333ae-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="333ae-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="333ae-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="333ae-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="333ae-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-240">Search-Flags</span></span>           | <span data-ttu-id="333ae-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="333ae-241">0x00000000</span></span>                             |
| <span data-ttu-id="333ae-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-242">System-Flags</span></span>           | <span data-ttu-id="333ae-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="333ae-243">0x00000010</span></span>                             |
| <span data-ttu-id="333ae-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="333ae-244">Classes used in</span></span>        | [<span data-ttu-id="333ae-245">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="333ae-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="333ae-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="333ae-246">Windows Server 2012</span></span>



| <span data-ttu-id="333ae-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="333ae-247">Entry</span></span> | <span data-ttu-id="333ae-248">Значение</span><span class="sxs-lookup"><span data-stu-id="333ae-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="333ae-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="333ae-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="333ae-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="333ae-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="333ae-251">System-Only</span></span>            | <span data-ttu-id="333ae-252">True</span><span class="sxs-lookup"><span data-stu-id="333ae-252">True</span></span>                                   |
| <span data-ttu-id="333ae-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="333ae-253">Is-Single-Valued</span></span>       | <span data-ttu-id="333ae-254">True</span><span class="sxs-lookup"><span data-stu-id="333ae-254">True</span></span>                                   |
| <span data-ttu-id="333ae-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="333ae-255">Is Indexed</span></span>             | <span data-ttu-id="333ae-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-256">False</span></span>                                  |
| <span data-ttu-id="333ae-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="333ae-257">In Global Catalog</span></span>      | <span data-ttu-id="333ae-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="333ae-258">False</span></span>                                  |
| <span data-ttu-id="333ae-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="333ae-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="333ae-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="333ae-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="333ae-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="333ae-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="333ae-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="333ae-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="333ae-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-263">Search-Flags</span></span>           | <span data-ttu-id="333ae-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="333ae-264">0x00000000</span></span>                             |
| <span data-ttu-id="333ae-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="333ae-265">System-Flags</span></span>           | <span data-ttu-id="333ae-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="333ae-266">0x00000010</span></span>                             |
| <span data-ttu-id="333ae-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="333ae-267">Classes used in</span></span>        | [<span data-ttu-id="333ae-268">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="333ae-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





