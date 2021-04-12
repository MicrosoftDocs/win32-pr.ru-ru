---
title: Атрибут времени последнего задания
description: Время последнего изменения секрета.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени последнего задания
- Схема AD атрибута Ластсеттиме
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416289"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="59b59-105">Атрибут времени последнего задания</span><span class="sxs-lookup"><span data-stu-id="59b59-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="59b59-106">Время последнего изменения секрета.</span><span class="sxs-lookup"><span data-stu-id="59b59-106">The last time the secret was changed.</span></span> <span data-ttu-id="59b59-107">Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="59b59-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="59b59-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-108">Entry</span></span> | <span data-ttu-id="59b59-109">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="59b59-110">CN</span><span class="sxs-lookup"><span data-stu-id="59b59-110">CN</span></span>                | <span data-ttu-id="59b59-111">Время последнего набора</span><span class="sxs-lookup"><span data-stu-id="59b59-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="59b59-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="59b59-112">Ldap-Display-Name</span></span> | <span data-ttu-id="59b59-113">ластсеттиме</span><span class="sxs-lookup"><span data-stu-id="59b59-113">lastSetTime</span></span>                          |
| <span data-ttu-id="59b59-114">Размер</span><span class="sxs-lookup"><span data-stu-id="59b59-114">Size</span></span>              | <span data-ttu-id="59b59-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="59b59-115">8 bytes</span></span>                              |
| <span data-ttu-id="59b59-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="59b59-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="59b59-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="59b59-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="59b59-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-118">Attribute-Id</span></span>      | <span data-ttu-id="59b59-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="59b59-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="59b59-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="59b59-120">System-Id-Guid</span></span>    | <span data-ttu-id="59b59-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="59b59-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="59b59-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59b59-122">Syntax</span></span>            | [<span data-ttu-id="59b59-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="59b59-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="59b59-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="59b59-124">Implementations</span></span>

-   [<span data-ttu-id="59b59-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="59b59-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="59b59-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="59b59-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="59b59-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="59b59-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="59b59-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="59b59-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="59b59-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="59b59-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="59b59-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="59b59-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="59b59-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59b59-131">Windows 2000 Server</span></span>



| <span data-ttu-id="59b59-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-132">Entry</span></span> | <span data-ttu-id="59b59-133">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="59b59-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59b59-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="59b59-136">System-Only</span></span>            | <span data-ttu-id="59b59-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-137">False</span></span>                                 |
| <span data-ttu-id="59b59-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59b59-138">Is-Single-Valued</span></span>       | <span data-ttu-id="59b59-139">True</span><span class="sxs-lookup"><span data-stu-id="59b59-139">True</span></span>                                  |
| <span data-ttu-id="59b59-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59b59-140">Is Indexed</span></span>             | <span data-ttu-id="59b59-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-141">False</span></span>                                 |
| <span data-ttu-id="59b59-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59b59-142">In Global Catalog</span></span>      | <span data-ttu-id="59b59-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-143">False</span></span>                                 |
| <span data-ttu-id="59b59-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59b59-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="59b59-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59b59-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="59b59-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59b59-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="59b59-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59b59-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="59b59-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-148">Search-Flags</span></span>           | <span data-ttu-id="59b59-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59b59-149">0x00000000</span></span>                            |
| <span data-ttu-id="59b59-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-150">System-Flags</span></span>           | <span data-ttu-id="59b59-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59b59-151">0x00000010</span></span>                            |
| <span data-ttu-id="59b59-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59b59-152">Classes used in</span></span>        | [<span data-ttu-id="59b59-153">**Владел**</span><span class="sxs-lookup"><span data-stu-id="59b59-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="59b59-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59b59-154">Windows Server 2003</span></span>



| <span data-ttu-id="59b59-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-155">Entry</span></span> | <span data-ttu-id="59b59-156">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="59b59-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59b59-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="59b59-159">System-Only</span></span>            | <span data-ttu-id="59b59-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-160">False</span></span>                                 |
| <span data-ttu-id="59b59-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59b59-161">Is-Single-Valued</span></span>       | <span data-ttu-id="59b59-162">True</span><span class="sxs-lookup"><span data-stu-id="59b59-162">True</span></span>                                  |
| <span data-ttu-id="59b59-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59b59-163">Is Indexed</span></span>             | <span data-ttu-id="59b59-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-164">False</span></span>                                 |
| <span data-ttu-id="59b59-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59b59-165">In Global Catalog</span></span>      | <span data-ttu-id="59b59-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-166">False</span></span>                                 |
| <span data-ttu-id="59b59-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59b59-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="59b59-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59b59-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="59b59-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59b59-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="59b59-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59b59-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="59b59-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-171">Search-Flags</span></span>           | <span data-ttu-id="59b59-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59b59-172">0x00000000</span></span>                            |
| <span data-ttu-id="59b59-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-173">System-Flags</span></span>           | <span data-ttu-id="59b59-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59b59-174">0x00000010</span></span>                            |
| <span data-ttu-id="59b59-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59b59-175">Classes used in</span></span>        | [<span data-ttu-id="59b59-176">**Владел**</span><span class="sxs-lookup"><span data-stu-id="59b59-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="59b59-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="59b59-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="59b59-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-178">Entry</span></span> | <span data-ttu-id="59b59-179">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="59b59-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59b59-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="59b59-182">System-Only</span></span>            | <span data-ttu-id="59b59-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-183">False</span></span>                                 |
| <span data-ttu-id="59b59-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59b59-184">Is-Single-Valued</span></span>       | <span data-ttu-id="59b59-185">True</span><span class="sxs-lookup"><span data-stu-id="59b59-185">True</span></span>                                  |
| <span data-ttu-id="59b59-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59b59-186">Is Indexed</span></span>             | <span data-ttu-id="59b59-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-187">False</span></span>                                 |
| <span data-ttu-id="59b59-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59b59-188">In Global Catalog</span></span>      | <span data-ttu-id="59b59-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-189">False</span></span>                                 |
| <span data-ttu-id="59b59-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59b59-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="59b59-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59b59-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="59b59-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59b59-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="59b59-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59b59-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="59b59-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-194">Search-Flags</span></span>           | <span data-ttu-id="59b59-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59b59-195">0x00000000</span></span>                            |
| <span data-ttu-id="59b59-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-196">System-Flags</span></span>           | <span data-ttu-id="59b59-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59b59-197">0x00000010</span></span>                            |
| <span data-ttu-id="59b59-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59b59-198">Classes used in</span></span>        | [<span data-ttu-id="59b59-199">**Владел**</span><span class="sxs-lookup"><span data-stu-id="59b59-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="59b59-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59b59-200">Windows Server 2008</span></span>



| <span data-ttu-id="59b59-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-201">Entry</span></span> | <span data-ttu-id="59b59-202">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="59b59-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59b59-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="59b59-205">System-Only</span></span>            | <span data-ttu-id="59b59-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-206">False</span></span>                                 |
| <span data-ttu-id="59b59-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59b59-207">Is-Single-Valued</span></span>       | <span data-ttu-id="59b59-208">True</span><span class="sxs-lookup"><span data-stu-id="59b59-208">True</span></span>                                  |
| <span data-ttu-id="59b59-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59b59-209">Is Indexed</span></span>             | <span data-ttu-id="59b59-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-210">False</span></span>                                 |
| <span data-ttu-id="59b59-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59b59-211">In Global Catalog</span></span>      | <span data-ttu-id="59b59-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-212">False</span></span>                                 |
| <span data-ttu-id="59b59-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59b59-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="59b59-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59b59-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="59b59-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59b59-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="59b59-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59b59-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="59b59-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-217">Search-Flags</span></span>           | <span data-ttu-id="59b59-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59b59-218">0x00000000</span></span>                            |
| <span data-ttu-id="59b59-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-219">System-Flags</span></span>           | <span data-ttu-id="59b59-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59b59-220">0x00000010</span></span>                            |
| <span data-ttu-id="59b59-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59b59-221">Classes used in</span></span>        | [<span data-ttu-id="59b59-222">**Владел**</span><span class="sxs-lookup"><span data-stu-id="59b59-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="59b59-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59b59-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="59b59-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-224">Entry</span></span> | <span data-ttu-id="59b59-225">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="59b59-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59b59-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="59b59-228">System-Only</span></span>            | <span data-ttu-id="59b59-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-229">False</span></span>                                 |
| <span data-ttu-id="59b59-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59b59-230">Is-Single-Valued</span></span>       | <span data-ttu-id="59b59-231">True</span><span class="sxs-lookup"><span data-stu-id="59b59-231">True</span></span>                                  |
| <span data-ttu-id="59b59-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59b59-232">Is Indexed</span></span>             | <span data-ttu-id="59b59-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-233">False</span></span>                                 |
| <span data-ttu-id="59b59-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59b59-234">In Global Catalog</span></span>      | <span data-ttu-id="59b59-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-235">False</span></span>                                 |
| <span data-ttu-id="59b59-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59b59-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="59b59-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59b59-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="59b59-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59b59-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="59b59-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59b59-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="59b59-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-240">Search-Flags</span></span>           | <span data-ttu-id="59b59-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59b59-241">0x00000000</span></span>                            |
| <span data-ttu-id="59b59-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-242">System-Flags</span></span>           | <span data-ttu-id="59b59-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59b59-243">0x00000010</span></span>                            |
| <span data-ttu-id="59b59-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59b59-244">Classes used in</span></span>        | [<span data-ttu-id="59b59-245">**Владел**</span><span class="sxs-lookup"><span data-stu-id="59b59-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="59b59-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59b59-246">Windows Server 2012</span></span>



| <span data-ttu-id="59b59-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="59b59-247">Entry</span></span> | <span data-ttu-id="59b59-248">Значение</span><span class="sxs-lookup"><span data-stu-id="59b59-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="59b59-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59b59-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59b59-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="59b59-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="59b59-251">System-Only</span></span>            | <span data-ttu-id="59b59-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-252">False</span></span>                                 |
| <span data-ttu-id="59b59-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59b59-253">Is-Single-Valued</span></span>       | <span data-ttu-id="59b59-254">True</span><span class="sxs-lookup"><span data-stu-id="59b59-254">True</span></span>                                  |
| <span data-ttu-id="59b59-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59b59-255">Is Indexed</span></span>             | <span data-ttu-id="59b59-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-256">False</span></span>                                 |
| <span data-ttu-id="59b59-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59b59-257">In Global Catalog</span></span>      | <span data-ttu-id="59b59-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="59b59-258">False</span></span>                                 |
| <span data-ttu-id="59b59-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59b59-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="59b59-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59b59-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="59b59-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59b59-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="59b59-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59b59-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="59b59-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-263">Search-Flags</span></span>           | <span data-ttu-id="59b59-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59b59-264">0x00000000</span></span>                            |
| <span data-ttu-id="59b59-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59b59-265">System-Flags</span></span>           | <span data-ttu-id="59b59-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59b59-266">0x00000010</span></span>                            |
| <span data-ttu-id="59b59-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59b59-267">Classes used in</span></span>        | [<span data-ttu-id="59b59-268">**Владел**</span><span class="sxs-lookup"><span data-stu-id="59b59-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 





