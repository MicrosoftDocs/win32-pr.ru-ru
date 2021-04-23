---
title: RID — используется атрибут пула
description: Пулы RID, которые использовались контроллером домена.
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута, используемая идентификатором RID
- Схема AD атрибута Ридуседпул
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138494"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="f7827-105">RID — используется атрибут пула</span><span class="sxs-lookup"><span data-stu-id="f7827-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="f7827-106">Пулы RID, которые использовались контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="f7827-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="f7827-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-107">Entry</span></span> | <span data-ttu-id="f7827-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f7827-109">CN</span><span class="sxs-lookup"><span data-stu-id="f7827-109">CN</span></span>                | <span data-ttu-id="f7827-110">RID — используется для пула</span><span class="sxs-lookup"><span data-stu-id="f7827-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="f7827-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f7827-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f7827-112">ридуседпул</span><span class="sxs-lookup"><span data-stu-id="f7827-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="f7827-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f7827-113">Size</span></span>              | <span data-ttu-id="f7827-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="f7827-114">8 bytes</span></span>                              |
| <span data-ttu-id="f7827-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f7827-115">Update Privilege</span></span>  | <span data-ttu-id="f7827-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="f7827-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="f7827-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f7827-117">Update Frequency</span></span>  | <span data-ttu-id="f7827-118">При очистке пула RID.</span><span class="sxs-lookup"><span data-stu-id="f7827-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="f7827-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-119">Attribute-Id</span></span>      | <span data-ttu-id="f7827-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="f7827-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="f7827-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f7827-121">System-Id-Guid</span></span>    | <span data-ttu-id="f7827-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f7827-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="f7827-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7827-123">Syntax</span></span>            | [<span data-ttu-id="f7827-124">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="f7827-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f7827-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f7827-125">Implementations</span></span>

-   [<span data-ttu-id="f7827-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7827-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7827-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7827-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7827-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7827-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7827-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7827-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7827-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7827-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7827-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7827-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7827-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7827-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f7827-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-133">Entry</span></span> | <span data-ttu-id="f7827-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="f7827-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7827-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7827-137">System-Only</span></span>            | <span data-ttu-id="f7827-138">True</span><span class="sxs-lookup"><span data-stu-id="f7827-138">True</span></span>                                   |
| <span data-ttu-id="f7827-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7827-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f7827-140">True</span><span class="sxs-lookup"><span data-stu-id="f7827-140">True</span></span>                                   |
| <span data-ttu-id="f7827-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7827-141">Is Indexed</span></span>             | <span data-ttu-id="f7827-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-142">False</span></span>                                  |
| <span data-ttu-id="f7827-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7827-143">In Global Catalog</span></span>      | <span data-ttu-id="f7827-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-144">False</span></span>                                  |
| <span data-ttu-id="f7827-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7827-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7827-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7827-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="f7827-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7827-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="f7827-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7827-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="f7827-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-149">Search-Flags</span></span>           | <span data-ttu-id="f7827-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7827-150">0x00000000</span></span>                             |
| <span data-ttu-id="f7827-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-151">System-Flags</span></span>           | <span data-ttu-id="f7827-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7827-152">0x00000010</span></span>                             |
| <span data-ttu-id="f7827-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7827-153">Classes used in</span></span>        | [<span data-ttu-id="f7827-154">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="f7827-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7827-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7827-155">Windows Server 2003</span></span>



| <span data-ttu-id="f7827-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-156">Entry</span></span> | <span data-ttu-id="f7827-157">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="f7827-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7827-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7827-160">System-Only</span></span>            | <span data-ttu-id="f7827-161">True</span><span class="sxs-lookup"><span data-stu-id="f7827-161">True</span></span>                                   |
| <span data-ttu-id="f7827-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7827-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f7827-163">True</span><span class="sxs-lookup"><span data-stu-id="f7827-163">True</span></span>                                   |
| <span data-ttu-id="f7827-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7827-164">Is Indexed</span></span>             | <span data-ttu-id="f7827-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-165">False</span></span>                                  |
| <span data-ttu-id="f7827-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7827-166">In Global Catalog</span></span>      | <span data-ttu-id="f7827-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-167">False</span></span>                                  |
| <span data-ttu-id="f7827-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7827-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7827-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7827-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="f7827-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7827-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="f7827-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7827-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="f7827-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-172">Search-Flags</span></span>           | <span data-ttu-id="f7827-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7827-173">0x00000000</span></span>                             |
| <span data-ttu-id="f7827-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-174">System-Flags</span></span>           | <span data-ttu-id="f7827-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7827-175">0x00000010</span></span>                             |
| <span data-ttu-id="f7827-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7827-176">Classes used in</span></span>        | [<span data-ttu-id="f7827-177">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="f7827-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7827-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7827-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7827-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-179">Entry</span></span> | <span data-ttu-id="f7827-180">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="f7827-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7827-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7827-183">System-Only</span></span>            | <span data-ttu-id="f7827-184">True</span><span class="sxs-lookup"><span data-stu-id="f7827-184">True</span></span>                                   |
| <span data-ttu-id="f7827-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7827-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f7827-186">True</span><span class="sxs-lookup"><span data-stu-id="f7827-186">True</span></span>                                   |
| <span data-ttu-id="f7827-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7827-187">Is Indexed</span></span>             | <span data-ttu-id="f7827-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-188">False</span></span>                                  |
| <span data-ttu-id="f7827-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7827-189">In Global Catalog</span></span>      | <span data-ttu-id="f7827-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-190">False</span></span>                                  |
| <span data-ttu-id="f7827-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7827-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7827-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7827-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="f7827-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7827-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="f7827-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7827-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="f7827-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-195">Search-Flags</span></span>           | <span data-ttu-id="f7827-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7827-196">0x00000000</span></span>                             |
| <span data-ttu-id="f7827-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-197">System-Flags</span></span>           | <span data-ttu-id="f7827-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7827-198">0x00000010</span></span>                             |
| <span data-ttu-id="f7827-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7827-199">Classes used in</span></span>        | [<span data-ttu-id="f7827-200">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="f7827-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7827-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7827-201">Windows Server 2008</span></span>



| <span data-ttu-id="f7827-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-202">Entry</span></span> | <span data-ttu-id="f7827-203">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="f7827-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7827-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7827-206">System-Only</span></span>            | <span data-ttu-id="f7827-207">True</span><span class="sxs-lookup"><span data-stu-id="f7827-207">True</span></span>                                   |
| <span data-ttu-id="f7827-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7827-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f7827-209">True</span><span class="sxs-lookup"><span data-stu-id="f7827-209">True</span></span>                                   |
| <span data-ttu-id="f7827-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7827-210">Is Indexed</span></span>             | <span data-ttu-id="f7827-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-211">False</span></span>                                  |
| <span data-ttu-id="f7827-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7827-212">In Global Catalog</span></span>      | <span data-ttu-id="f7827-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-213">False</span></span>                                  |
| <span data-ttu-id="f7827-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7827-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7827-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7827-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="f7827-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7827-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="f7827-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7827-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="f7827-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-218">Search-Flags</span></span>           | <span data-ttu-id="f7827-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7827-219">0x00000000</span></span>                             |
| <span data-ttu-id="f7827-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-220">System-Flags</span></span>           | <span data-ttu-id="f7827-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7827-221">0x00000010</span></span>                             |
| <span data-ttu-id="f7827-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7827-222">Classes used in</span></span>        | [<span data-ttu-id="f7827-223">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="f7827-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7827-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7827-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7827-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-225">Entry</span></span> | <span data-ttu-id="f7827-226">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="f7827-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7827-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7827-229">System-Only</span></span>            | <span data-ttu-id="f7827-230">True</span><span class="sxs-lookup"><span data-stu-id="f7827-230">True</span></span>                                   |
| <span data-ttu-id="f7827-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7827-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f7827-232">True</span><span class="sxs-lookup"><span data-stu-id="f7827-232">True</span></span>                                   |
| <span data-ttu-id="f7827-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7827-233">Is Indexed</span></span>             | <span data-ttu-id="f7827-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-234">False</span></span>                                  |
| <span data-ttu-id="f7827-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7827-235">In Global Catalog</span></span>      | <span data-ttu-id="f7827-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-236">False</span></span>                                  |
| <span data-ttu-id="f7827-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7827-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7827-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7827-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="f7827-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7827-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="f7827-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7827-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="f7827-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-241">Search-Flags</span></span>           | <span data-ttu-id="f7827-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7827-242">0x00000000</span></span>                             |
| <span data-ttu-id="f7827-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-243">System-Flags</span></span>           | <span data-ttu-id="f7827-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7827-244">0x00000010</span></span>                             |
| <span data-ttu-id="f7827-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7827-245">Classes used in</span></span>        | [<span data-ttu-id="f7827-246">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="f7827-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7827-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7827-247">Windows Server 2012</span></span>



| <span data-ttu-id="f7827-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7827-248">Entry</span></span> | <span data-ttu-id="f7827-249">Значение</span><span class="sxs-lookup"><span data-stu-id="f7827-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="f7827-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7827-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7827-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="f7827-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7827-252">System-Only</span></span>            | <span data-ttu-id="f7827-253">True</span><span class="sxs-lookup"><span data-stu-id="f7827-253">True</span></span>                                   |
| <span data-ttu-id="f7827-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7827-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f7827-255">True</span><span class="sxs-lookup"><span data-stu-id="f7827-255">True</span></span>                                   |
| <span data-ttu-id="f7827-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7827-256">Is Indexed</span></span>             | <span data-ttu-id="f7827-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-257">False</span></span>                                  |
| <span data-ttu-id="f7827-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7827-258">In Global Catalog</span></span>      | <span data-ttu-id="f7827-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7827-259">False</span></span>                                  |
| <span data-ttu-id="f7827-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7827-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7827-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7827-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="f7827-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7827-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="f7827-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7827-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="f7827-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-264">Search-Flags</span></span>           | <span data-ttu-id="f7827-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7827-265">0x00000000</span></span>                             |
| <span data-ttu-id="f7827-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7827-266">System-Flags</span></span>           | <span data-ttu-id="f7827-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7827-267">0x00000010</span></span>                             |
| <span data-ttu-id="f7827-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7827-268">Classes used in</span></span>        | [<span data-ttu-id="f7827-269">**RID-Set**</span><span class="sxs-lookup"><span data-stu-id="f7827-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





