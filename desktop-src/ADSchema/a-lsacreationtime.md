---
title: LSA-атрибут времени создания
description: Атрибут времени создания LSA-Time используется для поддержки репликации в домены Windows NT 4,0.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- LSA-схема AD атрибута времени создания
- Схема AD атрибута Лсакреатионтиме
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416217"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="43957-105">LSA-атрибут времени создания</span><span class="sxs-lookup"><span data-stu-id="43957-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="43957-106">Атрибут **времени создания LSA-Time** используется для поддержки репликации в домены Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="43957-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="43957-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-107">Entry</span></span> | <span data-ttu-id="43957-108">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="43957-109">CN</span><span class="sxs-lookup"><span data-stu-id="43957-109">CN</span></span>                | <span data-ttu-id="43957-110">LSA-время создания</span><span class="sxs-lookup"><span data-stu-id="43957-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="43957-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="43957-111">Ldap-Display-Name</span></span> | <span data-ttu-id="43957-112">лсакреатионтиме</span><span class="sxs-lookup"><span data-stu-id="43957-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="43957-113">Размер</span><span class="sxs-lookup"><span data-stu-id="43957-113">Size</span></span>              | <span data-ttu-id="43957-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="43957-114">8 bytes</span></span>                              |
| <span data-ttu-id="43957-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="43957-115">Update Privilege</span></span>  | <span data-ttu-id="43957-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="43957-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="43957-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="43957-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="43957-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="43957-118">Attribute-Id</span></span>      | <span data-ttu-id="43957-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="43957-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="43957-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="43957-120">System-Id-Guid</span></span>    | <span data-ttu-id="43957-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="43957-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="43957-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43957-122">Syntax</span></span>            | [<span data-ttu-id="43957-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="43957-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="43957-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="43957-124">Implementations</span></span>

-   [<span data-ttu-id="43957-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="43957-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="43957-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="43957-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="43957-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="43957-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="43957-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="43957-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="43957-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="43957-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="43957-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="43957-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="43957-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="43957-131">Windows 2000 Server</span></span>



| <span data-ttu-id="43957-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-132">Entry</span></span> | <span data-ttu-id="43957-133">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="43957-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="43957-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43957-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="43957-136">System-Only</span></span>            | <span data-ttu-id="43957-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-137">False</span></span>                                        |
| <span data-ttu-id="43957-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="43957-138">Is-Single-Valued</span></span>       | <span data-ttu-id="43957-139">True</span><span class="sxs-lookup"><span data-stu-id="43957-139">True</span></span>                                         |
| <span data-ttu-id="43957-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="43957-140">Is Indexed</span></span>             | <span data-ttu-id="43957-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-141">False</span></span>                                        |
| <span data-ttu-id="43957-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="43957-142">In Global Catalog</span></span>      | <span data-ttu-id="43957-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-143">False</span></span>                                        |
| <span data-ttu-id="43957-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="43957-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="43957-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="43957-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="43957-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43957-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="43957-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43957-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="43957-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-148">Search-Flags</span></span>           | <span data-ttu-id="43957-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43957-149">0x00000000</span></span>                                   |
| <span data-ttu-id="43957-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-150">System-Flags</span></span>           | <span data-ttu-id="43957-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43957-151">0x00000010</span></span>                                   |
| <span data-ttu-id="43957-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="43957-152">Classes used in</span></span>        | [<span data-ttu-id="43957-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="43957-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="43957-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="43957-154">Windows Server 2003</span></span>



| <span data-ttu-id="43957-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-155">Entry</span></span> | <span data-ttu-id="43957-156">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="43957-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="43957-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43957-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="43957-159">System-Only</span></span>            | <span data-ttu-id="43957-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-160">False</span></span>                                        |
| <span data-ttu-id="43957-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="43957-161">Is-Single-Valued</span></span>       | <span data-ttu-id="43957-162">True</span><span class="sxs-lookup"><span data-stu-id="43957-162">True</span></span>                                         |
| <span data-ttu-id="43957-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="43957-163">Is Indexed</span></span>             | <span data-ttu-id="43957-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-164">False</span></span>                                        |
| <span data-ttu-id="43957-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="43957-165">In Global Catalog</span></span>      | <span data-ttu-id="43957-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-166">False</span></span>                                        |
| <span data-ttu-id="43957-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="43957-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="43957-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="43957-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="43957-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43957-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="43957-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43957-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="43957-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-171">Search-Flags</span></span>           | <span data-ttu-id="43957-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43957-172">0x00000000</span></span>                                   |
| <span data-ttu-id="43957-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-173">System-Flags</span></span>           | <span data-ttu-id="43957-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43957-174">0x00000010</span></span>                                   |
| <span data-ttu-id="43957-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="43957-175">Classes used in</span></span>        | [<span data-ttu-id="43957-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="43957-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="43957-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="43957-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="43957-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-178">Entry</span></span> | <span data-ttu-id="43957-179">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="43957-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="43957-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43957-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="43957-182">System-Only</span></span>            | <span data-ttu-id="43957-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-183">False</span></span>                                        |
| <span data-ttu-id="43957-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="43957-184">Is-Single-Valued</span></span>       | <span data-ttu-id="43957-185">True</span><span class="sxs-lookup"><span data-stu-id="43957-185">True</span></span>                                         |
| <span data-ttu-id="43957-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="43957-186">Is Indexed</span></span>             | <span data-ttu-id="43957-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-187">False</span></span>                                        |
| <span data-ttu-id="43957-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="43957-188">In Global Catalog</span></span>      | <span data-ttu-id="43957-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-189">False</span></span>                                        |
| <span data-ttu-id="43957-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="43957-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="43957-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="43957-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="43957-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43957-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="43957-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43957-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="43957-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-194">Search-Flags</span></span>           | <span data-ttu-id="43957-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43957-195">0x00000000</span></span>                                   |
| <span data-ttu-id="43957-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-196">System-Flags</span></span>           | <span data-ttu-id="43957-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43957-197">0x00000010</span></span>                                   |
| <span data-ttu-id="43957-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="43957-198">Classes used in</span></span>        | [<span data-ttu-id="43957-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="43957-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="43957-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43957-200">Windows Server 2008</span></span>



| <span data-ttu-id="43957-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-201">Entry</span></span> | <span data-ttu-id="43957-202">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="43957-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="43957-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43957-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="43957-205">System-Only</span></span>            | <span data-ttu-id="43957-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-206">False</span></span>                                        |
| <span data-ttu-id="43957-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="43957-207">Is-Single-Valued</span></span>       | <span data-ttu-id="43957-208">True</span><span class="sxs-lookup"><span data-stu-id="43957-208">True</span></span>                                         |
| <span data-ttu-id="43957-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="43957-209">Is Indexed</span></span>             | <span data-ttu-id="43957-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-210">False</span></span>                                        |
| <span data-ttu-id="43957-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="43957-211">In Global Catalog</span></span>      | <span data-ttu-id="43957-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-212">False</span></span>                                        |
| <span data-ttu-id="43957-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="43957-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="43957-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="43957-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="43957-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43957-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="43957-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43957-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="43957-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-217">Search-Flags</span></span>           | <span data-ttu-id="43957-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43957-218">0x00000000</span></span>                                   |
| <span data-ttu-id="43957-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-219">System-Flags</span></span>           | <span data-ttu-id="43957-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43957-220">0x00000010</span></span>                                   |
| <span data-ttu-id="43957-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="43957-221">Classes used in</span></span>        | [<span data-ttu-id="43957-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="43957-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="43957-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="43957-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="43957-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-224">Entry</span></span> | <span data-ttu-id="43957-225">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="43957-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="43957-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43957-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="43957-228">System-Only</span></span>            | <span data-ttu-id="43957-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-229">False</span></span>                                        |
| <span data-ttu-id="43957-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="43957-230">Is-Single-Valued</span></span>       | <span data-ttu-id="43957-231">True</span><span class="sxs-lookup"><span data-stu-id="43957-231">True</span></span>                                         |
| <span data-ttu-id="43957-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="43957-232">Is Indexed</span></span>             | <span data-ttu-id="43957-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-233">False</span></span>                                        |
| <span data-ttu-id="43957-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="43957-234">In Global Catalog</span></span>      | <span data-ttu-id="43957-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-235">False</span></span>                                        |
| <span data-ttu-id="43957-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="43957-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="43957-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="43957-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="43957-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43957-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="43957-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43957-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="43957-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-240">Search-Flags</span></span>           | <span data-ttu-id="43957-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43957-241">0x00000000</span></span>                                   |
| <span data-ttu-id="43957-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-242">System-Flags</span></span>           | <span data-ttu-id="43957-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43957-243">0x00000010</span></span>                                   |
| <span data-ttu-id="43957-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="43957-244">Classes used in</span></span>        | [<span data-ttu-id="43957-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="43957-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="43957-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="43957-246">Windows Server 2012</span></span>



| <span data-ttu-id="43957-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="43957-247">Entry</span></span> | <span data-ttu-id="43957-248">Значение</span><span class="sxs-lookup"><span data-stu-id="43957-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="43957-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="43957-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43957-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="43957-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="43957-251">System-Only</span></span>            | <span data-ttu-id="43957-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-252">False</span></span>                                        |
| <span data-ttu-id="43957-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="43957-253">Is-Single-Valued</span></span>       | <span data-ttu-id="43957-254">True</span><span class="sxs-lookup"><span data-stu-id="43957-254">True</span></span>                                         |
| <span data-ttu-id="43957-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="43957-255">Is Indexed</span></span>             | <span data-ttu-id="43957-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-256">False</span></span>                                        |
| <span data-ttu-id="43957-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="43957-257">In Global Catalog</span></span>      | <span data-ttu-id="43957-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="43957-258">False</span></span>                                        |
| <span data-ttu-id="43957-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="43957-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="43957-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="43957-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="43957-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43957-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="43957-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43957-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="43957-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-263">Search-Flags</span></span>           | <span data-ttu-id="43957-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43957-264">0x00000000</span></span>                                   |
| <span data-ttu-id="43957-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43957-265">System-Flags</span></span>           | <span data-ttu-id="43957-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43957-266">0x00000010</span></span>                                   |
| <span data-ttu-id="43957-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="43957-267">Classes used in</span></span>        | [<span data-ttu-id="43957-268">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="43957-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





