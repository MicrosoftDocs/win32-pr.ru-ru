---
title: Атрибут RID — предыдущий выделенный пул
description: Содержит пул относительных идентификаторов (RID), из которого выделяется контроллер домена.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута RID предыдущего уровня выделения ресурсов пула
- Схема AD атрибута Ридпревиаусаллокатионпул
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893290"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="9b9aa-105">Атрибут RID — предыдущий выделенный пул</span><span class="sxs-lookup"><span data-stu-id="9b9aa-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="9b9aa-106">Атрибут **RID-Previous-распределения-Pool** содержит пул относительных идентификаторов (RID), из которого выделяется контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="9b9aa-107">Этот атрибут представляет собой 8-байтовое значение, содержащее пару из четырех байтов, представляющих начальное и конечное значения пула RID.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="9b9aa-108">Начальное значение находится в младших четырех байтах, а конечное значение — в верхних четырех байтах.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="9b9aa-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-109">Entry</span></span> | <span data-ttu-id="9b9aa-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9b9aa-111">CN</span><span class="sxs-lookup"><span data-stu-id="9b9aa-111">CN</span></span>                | <span data-ttu-id="9b9aa-112">RID — предыдущий пул выделения ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b9aa-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="9b9aa-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9b9aa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9b9aa-114">ридпревиаусаллокатионпул</span><span class="sxs-lookup"><span data-stu-id="9b9aa-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="9b9aa-115">Размер</span><span class="sxs-lookup"><span data-stu-id="9b9aa-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="9b9aa-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9b9aa-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9b9aa-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9b9aa-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9b9aa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-118">Attribute-Id</span></span>      | <span data-ttu-id="9b9aa-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="9b9aa-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="9b9aa-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9b9aa-120">System-Id-Guid</span></span>    | <span data-ttu-id="9b9aa-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9b9aa-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="9b9aa-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b9aa-122">Syntax</span></span>            | [<span data-ttu-id="9b9aa-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="9b9aa-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9b9aa-124">Implementations</span></span>

-   [<span data-ttu-id="9b9aa-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9b9aa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b9aa-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b9aa-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b9aa-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b9aa-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9b9aa-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b9aa-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9b9aa-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-132">Entry</span></span> | <span data-ttu-id="9b9aa-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="9b9aa-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9b9aa-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b9aa-136">System-Only</span></span>            | <span data-ttu-id="9b9aa-137">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-137">True</span></span>                                   |
| <span data-ttu-id="9b9aa-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9b9aa-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9b9aa-139">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-139">True</span></span>                                   |
| <span data-ttu-id="9b9aa-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9b9aa-140">Is Indexed</span></span>             | <span data-ttu-id="9b9aa-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-141">False</span></span>                                  |
| <span data-ttu-id="9b9aa-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9b9aa-142">In Global Catalog</span></span>      | <span data-ttu-id="9b9aa-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-143">False</span></span>                                  |
| <span data-ttu-id="9b9aa-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9b9aa-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b9aa-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="9b9aa-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b9aa-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b9aa-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-148">Search-Flags</span></span>           | <span data-ttu-id="9b9aa-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b9aa-149">0x00000000</span></span>                             |
| <span data-ttu-id="9b9aa-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-150">System-Flags</span></span>           | <span data-ttu-id="9b9aa-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9b9aa-151">0x00000011</span></span>                             |
| <span data-ttu-id="9b9aa-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9b9aa-152">Classes used in</span></span>        | [<span data-ttu-id="9b9aa-153">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9b9aa-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b9aa-154">Windows Server 2003</span></span>



| <span data-ttu-id="9b9aa-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-155">Entry</span></span> | <span data-ttu-id="9b9aa-156">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="9b9aa-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9b9aa-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b9aa-159">System-Only</span></span>            | <span data-ttu-id="9b9aa-160">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-160">True</span></span>                                   |
| <span data-ttu-id="9b9aa-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9b9aa-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9b9aa-162">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-162">True</span></span>                                   |
| <span data-ttu-id="9b9aa-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9b9aa-163">Is Indexed</span></span>             | <span data-ttu-id="9b9aa-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-164">False</span></span>                                  |
| <span data-ttu-id="9b9aa-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9b9aa-165">In Global Catalog</span></span>      | <span data-ttu-id="9b9aa-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-166">False</span></span>                                  |
| <span data-ttu-id="9b9aa-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9b9aa-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b9aa-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="9b9aa-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b9aa-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b9aa-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-171">Search-Flags</span></span>           | <span data-ttu-id="9b9aa-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b9aa-172">0x00000000</span></span>                             |
| <span data-ttu-id="9b9aa-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-173">System-Flags</span></span>           | <span data-ttu-id="9b9aa-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9b9aa-174">0x00000011</span></span>                             |
| <span data-ttu-id="9b9aa-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9b9aa-175">Classes used in</span></span>        | [<span data-ttu-id="9b9aa-176">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b9aa-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b9aa-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b9aa-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-178">Entry</span></span> | <span data-ttu-id="9b9aa-179">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="9b9aa-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9b9aa-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b9aa-182">System-Only</span></span>            | <span data-ttu-id="9b9aa-183">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-183">True</span></span>                                   |
| <span data-ttu-id="9b9aa-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9b9aa-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9b9aa-185">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-185">True</span></span>                                   |
| <span data-ttu-id="9b9aa-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9b9aa-186">Is Indexed</span></span>             | <span data-ttu-id="9b9aa-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-187">False</span></span>                                  |
| <span data-ttu-id="9b9aa-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9b9aa-188">In Global Catalog</span></span>      | <span data-ttu-id="9b9aa-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-189">False</span></span>                                  |
| <span data-ttu-id="9b9aa-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9b9aa-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b9aa-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="9b9aa-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b9aa-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b9aa-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-194">Search-Flags</span></span>           | <span data-ttu-id="9b9aa-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b9aa-195">0x00000000</span></span>                             |
| <span data-ttu-id="9b9aa-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-196">System-Flags</span></span>           | <span data-ttu-id="9b9aa-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9b9aa-197">0x00000011</span></span>                             |
| <span data-ttu-id="9b9aa-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9b9aa-198">Classes used in</span></span>        | [<span data-ttu-id="9b9aa-199">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b9aa-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b9aa-200">Windows Server 2008</span></span>



| <span data-ttu-id="9b9aa-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-201">Entry</span></span> | <span data-ttu-id="9b9aa-202">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="9b9aa-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9b9aa-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b9aa-205">System-Only</span></span>            | <span data-ttu-id="9b9aa-206">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-206">True</span></span>                                   |
| <span data-ttu-id="9b9aa-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9b9aa-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9b9aa-208">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-208">True</span></span>                                   |
| <span data-ttu-id="9b9aa-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9b9aa-209">Is Indexed</span></span>             | <span data-ttu-id="9b9aa-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-210">False</span></span>                                  |
| <span data-ttu-id="9b9aa-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9b9aa-211">In Global Catalog</span></span>      | <span data-ttu-id="9b9aa-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-212">False</span></span>                                  |
| <span data-ttu-id="9b9aa-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9b9aa-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b9aa-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="9b9aa-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b9aa-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b9aa-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-217">Search-Flags</span></span>           | <span data-ttu-id="9b9aa-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b9aa-218">0x00000000</span></span>                             |
| <span data-ttu-id="9b9aa-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-219">System-Flags</span></span>           | <span data-ttu-id="9b9aa-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9b9aa-220">0x00000011</span></span>                             |
| <span data-ttu-id="9b9aa-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9b9aa-221">Classes used in</span></span>        | [<span data-ttu-id="9b9aa-222">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b9aa-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b9aa-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b9aa-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-224">Entry</span></span> | <span data-ttu-id="9b9aa-225">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="9b9aa-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9b9aa-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b9aa-228">System-Only</span></span>            | <span data-ttu-id="9b9aa-229">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-229">True</span></span>                                   |
| <span data-ttu-id="9b9aa-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9b9aa-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9b9aa-231">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-231">True</span></span>                                   |
| <span data-ttu-id="9b9aa-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9b9aa-232">Is Indexed</span></span>             | <span data-ttu-id="9b9aa-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-233">False</span></span>                                  |
| <span data-ttu-id="9b9aa-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9b9aa-234">In Global Catalog</span></span>      | <span data-ttu-id="9b9aa-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-235">False</span></span>                                  |
| <span data-ttu-id="9b9aa-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9b9aa-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b9aa-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="9b9aa-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b9aa-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b9aa-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-240">Search-Flags</span></span>           | <span data-ttu-id="9b9aa-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b9aa-241">0x00000000</span></span>                             |
| <span data-ttu-id="9b9aa-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-242">System-Flags</span></span>           | <span data-ttu-id="9b9aa-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9b9aa-243">0x00000011</span></span>                             |
| <span data-ttu-id="9b9aa-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9b9aa-244">Classes used in</span></span>        | [<span data-ttu-id="9b9aa-245">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b9aa-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b9aa-246">Windows Server 2012</span></span>



| <span data-ttu-id="9b9aa-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="9b9aa-247">Entry</span></span> | <span data-ttu-id="9b9aa-248">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9aa-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="9b9aa-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9b9aa-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b9aa-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="9b9aa-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b9aa-251">System-Only</span></span>            | <span data-ttu-id="9b9aa-252">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-252">True</span></span>                                   |
| <span data-ttu-id="9b9aa-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9b9aa-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9b9aa-254">True</span><span class="sxs-lookup"><span data-stu-id="9b9aa-254">True</span></span>                                   |
| <span data-ttu-id="9b9aa-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9b9aa-255">Is Indexed</span></span>             | <span data-ttu-id="9b9aa-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-256">False</span></span>                                  |
| <span data-ttu-id="9b9aa-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9b9aa-257">In Global Catalog</span></span>      | <span data-ttu-id="9b9aa-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="9b9aa-258">False</span></span>                                  |
| <span data-ttu-id="9b9aa-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9b9aa-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b9aa-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="9b9aa-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b9aa-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b9aa-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="9b9aa-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-263">Search-Flags</span></span>           | <span data-ttu-id="9b9aa-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b9aa-264">0x00000000</span></span>                             |
| <span data-ttu-id="9b9aa-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b9aa-265">System-Flags</span></span>           | <span data-ttu-id="9b9aa-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9b9aa-266">0x00000011</span></span>                             |
| <span data-ttu-id="9b9aa-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9b9aa-267">Classes used in</span></span>        | [<span data-ttu-id="9b9aa-268">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="9b9aa-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





