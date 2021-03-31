---
title: Встроенный атрибут времени создания
description: Встроенный атрибут времени создания используется для поддержки репликации в домены Windows NT 4,0.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Встроенная схема AD атрибута времени создания
- Схема AD атрибута Буилтинкреатионтиме
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893973"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="f376d-105">Встроенный атрибут времени создания</span><span class="sxs-lookup"><span data-stu-id="f376d-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="f376d-106">**Встроенный атрибут времени создания** используется для поддержки репликации в домены Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="f376d-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="f376d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-107">Entry</span></span> | <span data-ttu-id="f376d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f376d-109">CN</span><span class="sxs-lookup"><span data-stu-id="f376d-109">CN</span></span>                | <span data-ttu-id="f376d-110">Встроенное время создания</span><span class="sxs-lookup"><span data-stu-id="f376d-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="f376d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f376d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f376d-112">буилтинкреатионтиме</span><span class="sxs-lookup"><span data-stu-id="f376d-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="f376d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f376d-113">Size</span></span>              | <span data-ttu-id="f376d-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="f376d-114">8 bytes</span></span>                              |
| <span data-ttu-id="f376d-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f376d-115">Update Privilege</span></span>  | <span data-ttu-id="f376d-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="f376d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="f376d-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f376d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f376d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-118">Attribute-Id</span></span>      | <span data-ttu-id="f376d-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="f376d-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="f376d-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f376d-120">System-Id-Guid</span></span>    | <span data-ttu-id="f376d-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f376d-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f376d-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f376d-122">Syntax</span></span>            | [<span data-ttu-id="f376d-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="f376d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f376d-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f376d-124">Implementations</span></span>

-   [<span data-ttu-id="f376d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f376d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f376d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f376d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f376d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f376d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f376d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f376d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f376d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f376d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f376d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f376d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f376d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f376d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f376d-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-132">Entry</span></span> | <span data-ttu-id="f376d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f376d-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f376d-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f376d-136">System-Only</span></span>            | <span data-ttu-id="f376d-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-137">False</span></span>                                        |
| <span data-ttu-id="f376d-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f376d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f376d-139">True</span><span class="sxs-lookup"><span data-stu-id="f376d-139">True</span></span>                                         |
| <span data-ttu-id="f376d-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f376d-140">Is Indexed</span></span>             | <span data-ttu-id="f376d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-141">False</span></span>                                        |
| <span data-ttu-id="f376d-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f376d-142">In Global Catalog</span></span>      | <span data-ttu-id="f376d-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-143">False</span></span>                                        |
| <span data-ttu-id="f376d-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f376d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f376d-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f376d-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f376d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f376d-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f376d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f376d-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f376d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-148">Search-Flags</span></span>           | <span data-ttu-id="f376d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f376d-149">0x00000000</span></span>                                   |
| <span data-ttu-id="f376d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-150">System-Flags</span></span>           | <span data-ttu-id="f376d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f376d-151">0x00000010</span></span>                                   |
| <span data-ttu-id="f376d-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f376d-152">Classes used in</span></span>        | [<span data-ttu-id="f376d-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="f376d-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f376d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f376d-154">Windows Server 2003</span></span>



| <span data-ttu-id="f376d-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-155">Entry</span></span> | <span data-ttu-id="f376d-156">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f376d-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f376d-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f376d-159">System-Only</span></span>            | <span data-ttu-id="f376d-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-160">False</span></span>                                        |
| <span data-ttu-id="f376d-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f376d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f376d-162">True</span><span class="sxs-lookup"><span data-stu-id="f376d-162">True</span></span>                                         |
| <span data-ttu-id="f376d-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f376d-163">Is Indexed</span></span>             | <span data-ttu-id="f376d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-164">False</span></span>                                        |
| <span data-ttu-id="f376d-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f376d-165">In Global Catalog</span></span>      | <span data-ttu-id="f376d-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-166">False</span></span>                                        |
| <span data-ttu-id="f376d-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f376d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f376d-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f376d-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f376d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f376d-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f376d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f376d-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f376d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-171">Search-Flags</span></span>           | <span data-ttu-id="f376d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f376d-172">0x00000000</span></span>                                   |
| <span data-ttu-id="f376d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-173">System-Flags</span></span>           | <span data-ttu-id="f376d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f376d-174">0x00000010</span></span>                                   |
| <span data-ttu-id="f376d-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f376d-175">Classes used in</span></span>        | [<span data-ttu-id="f376d-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="f376d-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f376d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f376d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f376d-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-178">Entry</span></span> | <span data-ttu-id="f376d-179">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f376d-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f376d-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f376d-182">System-Only</span></span>            | <span data-ttu-id="f376d-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-183">False</span></span>                                        |
| <span data-ttu-id="f376d-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f376d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f376d-185">True</span><span class="sxs-lookup"><span data-stu-id="f376d-185">True</span></span>                                         |
| <span data-ttu-id="f376d-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f376d-186">Is Indexed</span></span>             | <span data-ttu-id="f376d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-187">False</span></span>                                        |
| <span data-ttu-id="f376d-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f376d-188">In Global Catalog</span></span>      | <span data-ttu-id="f376d-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-189">False</span></span>                                        |
| <span data-ttu-id="f376d-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f376d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f376d-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f376d-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f376d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f376d-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f376d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f376d-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f376d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-194">Search-Flags</span></span>           | <span data-ttu-id="f376d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f376d-195">0x00000000</span></span>                                   |
| <span data-ttu-id="f376d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-196">System-Flags</span></span>           | <span data-ttu-id="f376d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f376d-197">0x00000010</span></span>                                   |
| <span data-ttu-id="f376d-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f376d-198">Classes used in</span></span>        | [<span data-ttu-id="f376d-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="f376d-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f376d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f376d-200">Windows Server 2008</span></span>



| <span data-ttu-id="f376d-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-201">Entry</span></span> | <span data-ttu-id="f376d-202">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f376d-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f376d-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f376d-205">System-Only</span></span>            | <span data-ttu-id="f376d-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-206">False</span></span>                                        |
| <span data-ttu-id="f376d-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f376d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f376d-208">True</span><span class="sxs-lookup"><span data-stu-id="f376d-208">True</span></span>                                         |
| <span data-ttu-id="f376d-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f376d-209">Is Indexed</span></span>             | <span data-ttu-id="f376d-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-210">False</span></span>                                        |
| <span data-ttu-id="f376d-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f376d-211">In Global Catalog</span></span>      | <span data-ttu-id="f376d-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-212">False</span></span>                                        |
| <span data-ttu-id="f376d-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f376d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f376d-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f376d-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f376d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f376d-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f376d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f376d-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f376d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-217">Search-Flags</span></span>           | <span data-ttu-id="f376d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f376d-218">0x00000000</span></span>                                   |
| <span data-ttu-id="f376d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-219">System-Flags</span></span>           | <span data-ttu-id="f376d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f376d-220">0x00000010</span></span>                                   |
| <span data-ttu-id="f376d-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f376d-221">Classes used in</span></span>        | [<span data-ttu-id="f376d-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="f376d-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f376d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f376d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f376d-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-224">Entry</span></span> | <span data-ttu-id="f376d-225">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f376d-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f376d-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f376d-228">System-Only</span></span>            | <span data-ttu-id="f376d-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-229">False</span></span>                                        |
| <span data-ttu-id="f376d-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f376d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f376d-231">True</span><span class="sxs-lookup"><span data-stu-id="f376d-231">True</span></span>                                         |
| <span data-ttu-id="f376d-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f376d-232">Is Indexed</span></span>             | <span data-ttu-id="f376d-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-233">False</span></span>                                        |
| <span data-ttu-id="f376d-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f376d-234">In Global Catalog</span></span>      | <span data-ttu-id="f376d-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-235">False</span></span>                                        |
| <span data-ttu-id="f376d-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f376d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f376d-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f376d-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f376d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f376d-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f376d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f376d-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f376d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-240">Search-Flags</span></span>           | <span data-ttu-id="f376d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f376d-241">0x00000000</span></span>                                   |
| <span data-ttu-id="f376d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-242">System-Flags</span></span>           | <span data-ttu-id="f376d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f376d-243">0x00000010</span></span>                                   |
| <span data-ttu-id="f376d-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f376d-244">Classes used in</span></span>        | [<span data-ttu-id="f376d-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="f376d-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f376d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f376d-246">Windows Server 2012</span></span>



| <span data-ttu-id="f376d-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="f376d-247">Entry</span></span> | <span data-ttu-id="f376d-248">Значение</span><span class="sxs-lookup"><span data-stu-id="f376d-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f376d-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f376d-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f376d-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f376d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f376d-251">System-Only</span></span>            | <span data-ttu-id="f376d-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-252">False</span></span>                                        |
| <span data-ttu-id="f376d-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f376d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f376d-254">True</span><span class="sxs-lookup"><span data-stu-id="f376d-254">True</span></span>                                         |
| <span data-ttu-id="f376d-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f376d-255">Is Indexed</span></span>             | <span data-ttu-id="f376d-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-256">False</span></span>                                        |
| <span data-ttu-id="f376d-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f376d-257">In Global Catalog</span></span>      | <span data-ttu-id="f376d-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="f376d-258">False</span></span>                                        |
| <span data-ttu-id="f376d-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f376d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f376d-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f376d-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f376d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f376d-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f376d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f376d-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f376d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-263">Search-Flags</span></span>           | <span data-ttu-id="f376d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f376d-264">0x00000000</span></span>                                   |
| <span data-ttu-id="f376d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f376d-265">System-Flags</span></span>           | <span data-ttu-id="f376d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f376d-266">0x00000010</span></span>                                   |
| <span data-ttu-id="f376d-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f376d-267">Classes used in</span></span>        | [<span data-ttu-id="f376d-268">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="f376d-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





