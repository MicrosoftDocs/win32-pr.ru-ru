---
title: Print — атрибут времени запуска
description: Время начала обслуживания заданий в очереди печати.
ms.assetid: 748d98a7-cef8-4a6d-9310-1f14667b2912
ms.tgt_platform: multiple
keywords:
- Печать — схема AD атрибута времени запуска
- Схема AD атрибута Принтстарттиме
topic_type:
- apiref
api_name:
- Print-Start-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1898bace41a795231585505da3f15d208bde264
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804852"
---
# <a name="print-start-time-attribute"></a><span data-ttu-id="9eb61-105">Print — атрибут времени запуска</span><span class="sxs-lookup"><span data-stu-id="9eb61-105">Print-Start-Time attribute</span></span>

<span data-ttu-id="9eb61-106">Время начала обслуживания заданий в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="9eb61-106">The time a print queue begins servicing jobs.</span></span>



| <span data-ttu-id="9eb61-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-107">Entry</span></span> | <span data-ttu-id="9eb61-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9eb61-109">CN</span><span class="sxs-lookup"><span data-stu-id="9eb61-109">CN</span></span>                | <span data-ttu-id="9eb61-110">Печать — время запуска</span><span class="sxs-lookup"><span data-stu-id="9eb61-110">Print-Start-Time</span></span>                     |
| <span data-ttu-id="9eb61-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9eb61-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9eb61-112">принтстарттиме</span><span class="sxs-lookup"><span data-stu-id="9eb61-112">printStartTime</span></span>                       |
| <span data-ttu-id="9eb61-113">Размер</span><span class="sxs-lookup"><span data-stu-id="9eb61-113">Size</span></span>              | <span data-ttu-id="9eb61-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="9eb61-114">4 bytes</span></span>                              |
| <span data-ttu-id="9eb61-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9eb61-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9eb61-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9eb61-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9eb61-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-117">Attribute-Id</span></span>      | <span data-ttu-id="9eb61-118">1.2.840.113556.1.4.233</span><span class="sxs-lookup"><span data-stu-id="9eb61-118">1.2.840.113556.1.4.233</span></span>               |
| <span data-ttu-id="9eb61-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9eb61-119">System-Id-Guid</span></span>    | <span data-ttu-id="9eb61-120">281416c9-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9eb61-120">281416c9-1968-11d0-a28f-00aa003049e2</span></span> |
| <span data-ttu-id="9eb61-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9eb61-121">Syntax</span></span>            | [<span data-ttu-id="9eb61-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="9eb61-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9eb61-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9eb61-123">Implementations</span></span>

-   [<span data-ttu-id="9eb61-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9eb61-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9eb61-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9eb61-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9eb61-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9eb61-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9eb61-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9eb61-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9eb61-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9eb61-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9eb61-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9eb61-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9eb61-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9eb61-130">Windows 2000 Server</span></span>



| <span data-ttu-id="9eb61-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-131">Entry</span></span> | <span data-ttu-id="9eb61-132">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="9eb61-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9eb61-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb61-135">System-Only</span></span>            | <span data-ttu-id="9eb61-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-136">False</span></span>                                          |
| <span data-ttu-id="9eb61-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9eb61-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb61-138">True</span><span class="sxs-lookup"><span data-stu-id="9eb61-138">True</span></span>                                           |
| <span data-ttu-id="9eb61-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9eb61-139">Is Indexed</span></span>             | <span data-ttu-id="9eb61-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-140">False</span></span>                                          |
| <span data-ttu-id="9eb61-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9eb61-141">In Global Catalog</span></span>      | <span data-ttu-id="9eb61-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-142">False</span></span>                                          |
| <span data-ttu-id="9eb61-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9eb61-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb61-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9eb61-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="9eb61-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb61-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb61-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-147">Search-Flags</span></span>           | <span data-ttu-id="9eb61-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb61-148">0x00000000</span></span>                                     |
| <span data-ttu-id="9eb61-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-149">System-Flags</span></span>           | <span data-ttu-id="9eb61-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb61-150">0x00000010</span></span>                                     |
| <span data-ttu-id="9eb61-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9eb61-151">Classes used in</span></span>        | [<span data-ttu-id="9eb61-152">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="9eb61-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9eb61-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9eb61-153">Windows Server 2003</span></span>



| <span data-ttu-id="9eb61-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-154">Entry</span></span> | <span data-ttu-id="9eb61-155">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="9eb61-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9eb61-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb61-158">System-Only</span></span>            | <span data-ttu-id="9eb61-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-159">False</span></span>                                          |
| <span data-ttu-id="9eb61-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9eb61-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb61-161">True</span><span class="sxs-lookup"><span data-stu-id="9eb61-161">True</span></span>                                           |
| <span data-ttu-id="9eb61-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9eb61-162">Is Indexed</span></span>             | <span data-ttu-id="9eb61-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-163">False</span></span>                                          |
| <span data-ttu-id="9eb61-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9eb61-164">In Global Catalog</span></span>      | <span data-ttu-id="9eb61-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-165">False</span></span>                                          |
| <span data-ttu-id="9eb61-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9eb61-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb61-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9eb61-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="9eb61-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb61-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb61-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-170">Search-Flags</span></span>           | <span data-ttu-id="9eb61-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb61-171">0x00000000</span></span>                                     |
| <span data-ttu-id="9eb61-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-172">System-Flags</span></span>           | <span data-ttu-id="9eb61-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb61-173">0x00000010</span></span>                                     |
| <span data-ttu-id="9eb61-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9eb61-174">Classes used in</span></span>        | [<span data-ttu-id="9eb61-175">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="9eb61-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9eb61-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9eb61-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9eb61-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-177">Entry</span></span> | <span data-ttu-id="9eb61-178">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="9eb61-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9eb61-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb61-181">System-Only</span></span>            | <span data-ttu-id="9eb61-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-182">False</span></span>                                          |
| <span data-ttu-id="9eb61-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9eb61-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb61-184">True</span><span class="sxs-lookup"><span data-stu-id="9eb61-184">True</span></span>                                           |
| <span data-ttu-id="9eb61-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9eb61-185">Is Indexed</span></span>             | <span data-ttu-id="9eb61-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-186">False</span></span>                                          |
| <span data-ttu-id="9eb61-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9eb61-187">In Global Catalog</span></span>      | <span data-ttu-id="9eb61-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-188">False</span></span>                                          |
| <span data-ttu-id="9eb61-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9eb61-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb61-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9eb61-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="9eb61-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb61-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb61-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-193">Search-Flags</span></span>           | <span data-ttu-id="9eb61-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb61-194">0x00000000</span></span>                                     |
| <span data-ttu-id="9eb61-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-195">System-Flags</span></span>           | <span data-ttu-id="9eb61-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb61-196">0x00000010</span></span>                                     |
| <span data-ttu-id="9eb61-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9eb61-197">Classes used in</span></span>        | [<span data-ttu-id="9eb61-198">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="9eb61-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9eb61-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eb61-199">Windows Server 2008</span></span>



| <span data-ttu-id="9eb61-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-200">Entry</span></span> | <span data-ttu-id="9eb61-201">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="9eb61-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9eb61-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb61-204">System-Only</span></span>            | <span data-ttu-id="9eb61-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-205">False</span></span>                                          |
| <span data-ttu-id="9eb61-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9eb61-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb61-207">True</span><span class="sxs-lookup"><span data-stu-id="9eb61-207">True</span></span>                                           |
| <span data-ttu-id="9eb61-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9eb61-208">Is Indexed</span></span>             | <span data-ttu-id="9eb61-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-209">False</span></span>                                          |
| <span data-ttu-id="9eb61-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9eb61-210">In Global Catalog</span></span>      | <span data-ttu-id="9eb61-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-211">False</span></span>                                          |
| <span data-ttu-id="9eb61-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9eb61-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb61-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9eb61-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="9eb61-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb61-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb61-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-216">Search-Flags</span></span>           | <span data-ttu-id="9eb61-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb61-217">0x00000000</span></span>                                     |
| <span data-ttu-id="9eb61-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-218">System-Flags</span></span>           | <span data-ttu-id="9eb61-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb61-219">0x00000010</span></span>                                     |
| <span data-ttu-id="9eb61-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9eb61-220">Classes used in</span></span>        | [<span data-ttu-id="9eb61-221">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="9eb61-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9eb61-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9eb61-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9eb61-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-223">Entry</span></span> | <span data-ttu-id="9eb61-224">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="9eb61-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9eb61-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb61-227">System-Only</span></span>            | <span data-ttu-id="9eb61-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-228">False</span></span>                                          |
| <span data-ttu-id="9eb61-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9eb61-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb61-230">True</span><span class="sxs-lookup"><span data-stu-id="9eb61-230">True</span></span>                                           |
| <span data-ttu-id="9eb61-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9eb61-231">Is Indexed</span></span>             | <span data-ttu-id="9eb61-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-232">False</span></span>                                          |
| <span data-ttu-id="9eb61-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9eb61-233">In Global Catalog</span></span>      | <span data-ttu-id="9eb61-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-234">False</span></span>                                          |
| <span data-ttu-id="9eb61-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9eb61-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb61-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9eb61-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="9eb61-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb61-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb61-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-239">Search-Flags</span></span>           | <span data-ttu-id="9eb61-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb61-240">0x00000000</span></span>                                     |
| <span data-ttu-id="9eb61-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-241">System-Flags</span></span>           | <span data-ttu-id="9eb61-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb61-242">0x00000010</span></span>                                     |
| <span data-ttu-id="9eb61-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9eb61-243">Classes used in</span></span>        | [<span data-ttu-id="9eb61-244">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="9eb61-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9eb61-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9eb61-245">Windows Server 2012</span></span>



| <span data-ttu-id="9eb61-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="9eb61-246">Entry</span></span> | <span data-ttu-id="9eb61-247">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb61-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="9eb61-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9eb61-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb61-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="9eb61-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb61-250">System-Only</span></span>            | <span data-ttu-id="9eb61-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-251">False</span></span>                                          |
| <span data-ttu-id="9eb61-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9eb61-252">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb61-253">True</span><span class="sxs-lookup"><span data-stu-id="9eb61-253">True</span></span>                                           |
| <span data-ttu-id="9eb61-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9eb61-254">Is Indexed</span></span>             | <span data-ttu-id="9eb61-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-255">False</span></span>                                          |
| <span data-ttu-id="9eb61-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9eb61-256">In Global Catalog</span></span>      | <span data-ttu-id="9eb61-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="9eb61-257">False</span></span>                                          |
| <span data-ttu-id="9eb61-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9eb61-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb61-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9eb61-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="9eb61-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb61-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb61-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="9eb61-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-262">Search-Flags</span></span>           | <span data-ttu-id="9eb61-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb61-263">0x00000000</span></span>                                     |
| <span data-ttu-id="9eb61-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb61-264">System-Flags</span></span>           | <span data-ttu-id="9eb61-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb61-265">0x00000010</span></span>                                     |
| <span data-ttu-id="9eb61-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9eb61-266">Classes used in</span></span>        | [<span data-ttu-id="9eb61-267">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="9eb61-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





