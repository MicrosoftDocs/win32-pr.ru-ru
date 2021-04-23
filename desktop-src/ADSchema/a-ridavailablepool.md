---
title: RID — атрибут пула доступности
description: Пространство, из которого выделяются пулы RID.
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- RID — схема AD атрибутов пула
- Схема AD атрибута Ридаваилаблепул
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59faf801b7f6f70e92c55a1d2a27857ed6ecb0c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262262"
---
# <a name="rid-available-pool-attribute"></a><span data-ttu-id="05602-105">RID — атрибут пула доступности</span><span class="sxs-lookup"><span data-stu-id="05602-105">RID-Available-Pool attribute</span></span>

<span data-ttu-id="05602-106">Пространство, из которого выделяются пулы RID.</span><span class="sxs-lookup"><span data-stu-id="05602-106">The space from which RID Pools are allocated.</span></span>



| <span data-ttu-id="05602-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-107">Entry</span></span> | <span data-ttu-id="05602-108">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="05602-109">CN</span><span class="sxs-lookup"><span data-stu-id="05602-109">CN</span></span>                | <span data-ttu-id="05602-110">RID — пул доступности</span><span class="sxs-lookup"><span data-stu-id="05602-110">RID-Available-Pool</span></span>                   |
| <span data-ttu-id="05602-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="05602-111">Ldap-Display-Name</span></span> | <span data-ttu-id="05602-112">ридаваилаблепул</span><span class="sxs-lookup"><span data-stu-id="05602-112">rIDAvailablePool</span></span>                     |
| <span data-ttu-id="05602-113">Размер</span><span class="sxs-lookup"><span data-stu-id="05602-113">Size</span></span>              | <span data-ttu-id="05602-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="05602-114">8 bytes</span></span>                              |
| <span data-ttu-id="05602-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="05602-115">Update Privilege</span></span>  | <span data-ttu-id="05602-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="05602-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="05602-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="05602-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="05602-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="05602-118">Attribute-Id</span></span>      | <span data-ttu-id="05602-119">1.2.840.113556.1.4.370</span><span class="sxs-lookup"><span data-stu-id="05602-119">1.2.840.113556.1.4.370</span></span>               |
| <span data-ttu-id="05602-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="05602-120">System-Id-Guid</span></span>    | <span data-ttu-id="05602-121">66171888-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="05602-121">66171888-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="05602-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05602-122">Syntax</span></span>            | [<span data-ttu-id="05602-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="05602-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="05602-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="05602-124">Implementations</span></span>

-   [<span data-ttu-id="05602-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="05602-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="05602-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="05602-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="05602-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="05602-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="05602-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="05602-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="05602-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="05602-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="05602-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="05602-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="05602-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05602-131">Windows 2000 Server</span></span>



| <span data-ttu-id="05602-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-132">Entry</span></span> | <span data-ttu-id="05602-133">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="05602-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05602-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05602-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="05602-136">System-Only</span></span>            | <span data-ttu-id="05602-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-137">False</span></span>                                          |
| <span data-ttu-id="05602-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05602-138">Is-Single-Valued</span></span>       | <span data-ttu-id="05602-139">True</span><span class="sxs-lookup"><span data-stu-id="05602-139">True</span></span>                                           |
| <span data-ttu-id="05602-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05602-140">Is Indexed</span></span>             | <span data-ttu-id="05602-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-141">False</span></span>                                          |
| <span data-ttu-id="05602-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05602-142">In Global Catalog</span></span>      | <span data-ttu-id="05602-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-143">False</span></span>                                          |
| <span data-ttu-id="05602-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05602-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="05602-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05602-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="05602-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05602-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="05602-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05602-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="05602-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-148">Search-Flags</span></span>           | <span data-ttu-id="05602-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05602-149">0x00000000</span></span>                                     |
| <span data-ttu-id="05602-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-150">System-Flags</span></span>           | <span data-ttu-id="05602-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05602-151">0x00000010</span></span>                                     |
| <span data-ttu-id="05602-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05602-152">Classes used in</span></span>        | [<span data-ttu-id="05602-153">**Диспетчер RID**</span><span class="sxs-lookup"><span data-stu-id="05602-153">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="05602-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05602-154">Windows Server 2003</span></span>



| <span data-ttu-id="05602-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-155">Entry</span></span> | <span data-ttu-id="05602-156">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="05602-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05602-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05602-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="05602-159">System-Only</span></span>            | <span data-ttu-id="05602-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-160">False</span></span>                                          |
| <span data-ttu-id="05602-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05602-161">Is-Single-Valued</span></span>       | <span data-ttu-id="05602-162">True</span><span class="sxs-lookup"><span data-stu-id="05602-162">True</span></span>                                           |
| <span data-ttu-id="05602-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05602-163">Is Indexed</span></span>             | <span data-ttu-id="05602-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-164">False</span></span>                                          |
| <span data-ttu-id="05602-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05602-165">In Global Catalog</span></span>      | <span data-ttu-id="05602-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-166">False</span></span>                                          |
| <span data-ttu-id="05602-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05602-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="05602-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05602-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="05602-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05602-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="05602-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05602-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="05602-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-171">Search-Flags</span></span>           | <span data-ttu-id="05602-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05602-172">0x00000000</span></span>                                     |
| <span data-ttu-id="05602-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-173">System-Flags</span></span>           | <span data-ttu-id="05602-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05602-174">0x00000010</span></span>                                     |
| <span data-ttu-id="05602-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05602-175">Classes used in</span></span>        | [<span data-ttu-id="05602-176">**Диспетчер RID**</span><span class="sxs-lookup"><span data-stu-id="05602-176">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="05602-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="05602-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="05602-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-178">Entry</span></span> | <span data-ttu-id="05602-179">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="05602-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05602-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05602-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="05602-182">System-Only</span></span>            | <span data-ttu-id="05602-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-183">False</span></span>                                          |
| <span data-ttu-id="05602-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05602-184">Is-Single-Valued</span></span>       | <span data-ttu-id="05602-185">True</span><span class="sxs-lookup"><span data-stu-id="05602-185">True</span></span>                                           |
| <span data-ttu-id="05602-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05602-186">Is Indexed</span></span>             | <span data-ttu-id="05602-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-187">False</span></span>                                          |
| <span data-ttu-id="05602-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05602-188">In Global Catalog</span></span>      | <span data-ttu-id="05602-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-189">False</span></span>                                          |
| <span data-ttu-id="05602-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05602-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="05602-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05602-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="05602-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05602-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="05602-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05602-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="05602-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-194">Search-Flags</span></span>           | <span data-ttu-id="05602-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05602-195">0x00000000</span></span>                                     |
| <span data-ttu-id="05602-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-196">System-Flags</span></span>           | <span data-ttu-id="05602-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05602-197">0x00000010</span></span>                                     |
| <span data-ttu-id="05602-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05602-198">Classes used in</span></span>        | [<span data-ttu-id="05602-199">**Диспетчер RID**</span><span class="sxs-lookup"><span data-stu-id="05602-199">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="05602-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05602-200">Windows Server 2008</span></span>



| <span data-ttu-id="05602-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-201">Entry</span></span> | <span data-ttu-id="05602-202">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="05602-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05602-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05602-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="05602-205">System-Only</span></span>            | <span data-ttu-id="05602-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-206">False</span></span>                                          |
| <span data-ttu-id="05602-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05602-207">Is-Single-Valued</span></span>       | <span data-ttu-id="05602-208">True</span><span class="sxs-lookup"><span data-stu-id="05602-208">True</span></span>                                           |
| <span data-ttu-id="05602-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05602-209">Is Indexed</span></span>             | <span data-ttu-id="05602-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-210">False</span></span>                                          |
| <span data-ttu-id="05602-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05602-211">In Global Catalog</span></span>      | <span data-ttu-id="05602-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-212">False</span></span>                                          |
| <span data-ttu-id="05602-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05602-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="05602-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05602-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="05602-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05602-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="05602-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05602-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="05602-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-217">Search-Flags</span></span>           | <span data-ttu-id="05602-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05602-218">0x00000000</span></span>                                     |
| <span data-ttu-id="05602-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-219">System-Flags</span></span>           | <span data-ttu-id="05602-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05602-220">0x00000010</span></span>                                     |
| <span data-ttu-id="05602-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05602-221">Classes used in</span></span>        | [<span data-ttu-id="05602-222">**Диспетчер RID**</span><span class="sxs-lookup"><span data-stu-id="05602-222">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="05602-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05602-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="05602-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-224">Entry</span></span> | <span data-ttu-id="05602-225">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="05602-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05602-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05602-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="05602-228">System-Only</span></span>            | <span data-ttu-id="05602-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-229">False</span></span>                                          |
| <span data-ttu-id="05602-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05602-230">Is-Single-Valued</span></span>       | <span data-ttu-id="05602-231">True</span><span class="sxs-lookup"><span data-stu-id="05602-231">True</span></span>                                           |
| <span data-ttu-id="05602-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05602-232">Is Indexed</span></span>             | <span data-ttu-id="05602-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-233">False</span></span>                                          |
| <span data-ttu-id="05602-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05602-234">In Global Catalog</span></span>      | <span data-ttu-id="05602-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-235">False</span></span>                                          |
| <span data-ttu-id="05602-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05602-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="05602-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05602-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="05602-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05602-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="05602-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05602-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="05602-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-240">Search-Flags</span></span>           | <span data-ttu-id="05602-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05602-241">0x00000000</span></span>                                     |
| <span data-ttu-id="05602-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-242">System-Flags</span></span>           | <span data-ttu-id="05602-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05602-243">0x00000010</span></span>                                     |
| <span data-ttu-id="05602-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05602-244">Classes used in</span></span>        | [<span data-ttu-id="05602-245">**Диспетчер RID**</span><span class="sxs-lookup"><span data-stu-id="05602-245">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="05602-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05602-246">Windows Server 2012</span></span>



| <span data-ttu-id="05602-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="05602-247">Entry</span></span> | <span data-ttu-id="05602-248">Значение</span><span class="sxs-lookup"><span data-stu-id="05602-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="05602-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05602-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05602-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="05602-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="05602-251">System-Only</span></span>            | <span data-ttu-id="05602-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-252">False</span></span>                                          |
| <span data-ttu-id="05602-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05602-253">Is-Single-Valued</span></span>       | <span data-ttu-id="05602-254">True</span><span class="sxs-lookup"><span data-stu-id="05602-254">True</span></span>                                           |
| <span data-ttu-id="05602-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05602-255">Is Indexed</span></span>             | <span data-ttu-id="05602-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-256">False</span></span>                                          |
| <span data-ttu-id="05602-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05602-257">In Global Catalog</span></span>      | <span data-ttu-id="05602-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="05602-258">False</span></span>                                          |
| <span data-ttu-id="05602-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05602-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="05602-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05602-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="05602-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05602-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="05602-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05602-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="05602-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-263">Search-Flags</span></span>           | <span data-ttu-id="05602-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05602-264">0x00000000</span></span>                                     |
| <span data-ttu-id="05602-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05602-265">System-Flags</span></span>           | <span data-ttu-id="05602-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05602-266">0x00000010</span></span>                                     |
| <span data-ttu-id="05602-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05602-267">Classes used in</span></span>        | [<span data-ttu-id="05602-268">**Диспетчер RID**</span><span class="sxs-lookup"><span data-stu-id="05602-268">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



 

 





