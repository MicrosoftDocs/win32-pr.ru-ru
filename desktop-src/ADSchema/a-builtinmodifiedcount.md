---
title: Встроенный атрибут Count
description: Встроенный атрибут Count используется для поддержки репликации в домены Windows NT 4,0.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Встроенная схема AD атрибута count
- Схема AD атрибута Буилтинмодифиедкаунт
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139050"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="04aad-105">Встроенный атрибут Count</span><span class="sxs-lookup"><span data-stu-id="04aad-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="04aad-106">**Встроенный атрибут Count** используется для поддержки репликации в домены Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="04aad-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="04aad-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-107">Entry</span></span> | <span data-ttu-id="04aad-108">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="04aad-109">CN</span><span class="sxs-lookup"><span data-stu-id="04aad-109">CN</span></span>                | <span data-ttu-id="04aad-110">Builtin — изменено — количество</span><span class="sxs-lookup"><span data-stu-id="04aad-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="04aad-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="04aad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="04aad-112">буилтинмодифиедкаунт</span><span class="sxs-lookup"><span data-stu-id="04aad-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="04aad-113">Размер</span><span class="sxs-lookup"><span data-stu-id="04aad-113">Size</span></span>              | <span data-ttu-id="04aad-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="04aad-114">8 bytes</span></span>                              |
| <span data-ttu-id="04aad-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="04aad-115">Update Privilege</span></span>  | <span data-ttu-id="04aad-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="04aad-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="04aad-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="04aad-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="04aad-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-118">Attribute-Id</span></span>      | <span data-ttu-id="04aad-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="04aad-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="04aad-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="04aad-120">System-Id-Guid</span></span>    | <span data-ttu-id="04aad-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="04aad-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="04aad-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04aad-122">Syntax</span></span>            | [<span data-ttu-id="04aad-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="04aad-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="04aad-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="04aad-124">Implementations</span></span>

-   [<span data-ttu-id="04aad-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04aad-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04aad-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04aad-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04aad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04aad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04aad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04aad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04aad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04aad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04aad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04aad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04aad-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04aad-131">Windows 2000 Server</span></span>



| <span data-ttu-id="04aad-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-132">Entry</span></span> | <span data-ttu-id="04aad-133">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="04aad-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="04aad-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="04aad-136">System-Only</span></span>            | <span data-ttu-id="04aad-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-137">False</span></span>                                        |
| <span data-ttu-id="04aad-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="04aad-138">Is-Single-Valued</span></span>       | <span data-ttu-id="04aad-139">True</span><span class="sxs-lookup"><span data-stu-id="04aad-139">True</span></span>                                         |
| <span data-ttu-id="04aad-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="04aad-140">Is Indexed</span></span>             | <span data-ttu-id="04aad-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-141">False</span></span>                                        |
| <span data-ttu-id="04aad-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="04aad-142">In Global Catalog</span></span>      | <span data-ttu-id="04aad-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-143">False</span></span>                                        |
| <span data-ttu-id="04aad-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="04aad-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="04aad-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04aad-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="04aad-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04aad-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="04aad-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04aad-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="04aad-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-148">Search-Flags</span></span>           | <span data-ttu-id="04aad-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04aad-149">0x00000000</span></span>                                   |
| <span data-ttu-id="04aad-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-150">System-Flags</span></span>           | <span data-ttu-id="04aad-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04aad-151">0x00000010</span></span>                                   |
| <span data-ttu-id="04aad-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="04aad-152">Classes used in</span></span>        | [<span data-ttu-id="04aad-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="04aad-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04aad-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04aad-154">Windows Server 2003</span></span>



| <span data-ttu-id="04aad-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-155">Entry</span></span> | <span data-ttu-id="04aad-156">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="04aad-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="04aad-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="04aad-159">System-Only</span></span>            | <span data-ttu-id="04aad-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-160">False</span></span>                                        |
| <span data-ttu-id="04aad-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="04aad-161">Is-Single-Valued</span></span>       | <span data-ttu-id="04aad-162">True</span><span class="sxs-lookup"><span data-stu-id="04aad-162">True</span></span>                                         |
| <span data-ttu-id="04aad-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="04aad-163">Is Indexed</span></span>             | <span data-ttu-id="04aad-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-164">False</span></span>                                        |
| <span data-ttu-id="04aad-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="04aad-165">In Global Catalog</span></span>      | <span data-ttu-id="04aad-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-166">False</span></span>                                        |
| <span data-ttu-id="04aad-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="04aad-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="04aad-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04aad-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="04aad-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04aad-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="04aad-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04aad-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="04aad-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-171">Search-Flags</span></span>           | <span data-ttu-id="04aad-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04aad-172">0x00000000</span></span>                                   |
| <span data-ttu-id="04aad-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-173">System-Flags</span></span>           | <span data-ttu-id="04aad-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04aad-174">0x00000010</span></span>                                   |
| <span data-ttu-id="04aad-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="04aad-175">Classes used in</span></span>        | [<span data-ttu-id="04aad-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="04aad-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04aad-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04aad-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04aad-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-178">Entry</span></span> | <span data-ttu-id="04aad-179">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="04aad-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="04aad-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="04aad-182">System-Only</span></span>            | <span data-ttu-id="04aad-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-183">False</span></span>                                        |
| <span data-ttu-id="04aad-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="04aad-184">Is-Single-Valued</span></span>       | <span data-ttu-id="04aad-185">True</span><span class="sxs-lookup"><span data-stu-id="04aad-185">True</span></span>                                         |
| <span data-ttu-id="04aad-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="04aad-186">Is Indexed</span></span>             | <span data-ttu-id="04aad-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-187">False</span></span>                                        |
| <span data-ttu-id="04aad-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="04aad-188">In Global Catalog</span></span>      | <span data-ttu-id="04aad-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-189">False</span></span>                                        |
| <span data-ttu-id="04aad-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="04aad-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="04aad-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04aad-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="04aad-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04aad-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="04aad-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04aad-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="04aad-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-194">Search-Flags</span></span>           | <span data-ttu-id="04aad-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04aad-195">0x00000000</span></span>                                   |
| <span data-ttu-id="04aad-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-196">System-Flags</span></span>           | <span data-ttu-id="04aad-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04aad-197">0x00000010</span></span>                                   |
| <span data-ttu-id="04aad-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="04aad-198">Classes used in</span></span>        | [<span data-ttu-id="04aad-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="04aad-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04aad-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04aad-200">Windows Server 2008</span></span>



| <span data-ttu-id="04aad-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-201">Entry</span></span> | <span data-ttu-id="04aad-202">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="04aad-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="04aad-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="04aad-205">System-Only</span></span>            | <span data-ttu-id="04aad-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-206">False</span></span>                                        |
| <span data-ttu-id="04aad-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="04aad-207">Is-Single-Valued</span></span>       | <span data-ttu-id="04aad-208">True</span><span class="sxs-lookup"><span data-stu-id="04aad-208">True</span></span>                                         |
| <span data-ttu-id="04aad-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="04aad-209">Is Indexed</span></span>             | <span data-ttu-id="04aad-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-210">False</span></span>                                        |
| <span data-ttu-id="04aad-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="04aad-211">In Global Catalog</span></span>      | <span data-ttu-id="04aad-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-212">False</span></span>                                        |
| <span data-ttu-id="04aad-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="04aad-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="04aad-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04aad-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="04aad-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04aad-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="04aad-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04aad-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="04aad-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-217">Search-Flags</span></span>           | <span data-ttu-id="04aad-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04aad-218">0x00000000</span></span>                                   |
| <span data-ttu-id="04aad-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-219">System-Flags</span></span>           | <span data-ttu-id="04aad-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04aad-220">0x00000010</span></span>                                   |
| <span data-ttu-id="04aad-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="04aad-221">Classes used in</span></span>        | [<span data-ttu-id="04aad-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="04aad-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04aad-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04aad-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04aad-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-224">Entry</span></span> | <span data-ttu-id="04aad-225">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="04aad-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="04aad-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="04aad-228">System-Only</span></span>            | <span data-ttu-id="04aad-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-229">False</span></span>                                        |
| <span data-ttu-id="04aad-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="04aad-230">Is-Single-Valued</span></span>       | <span data-ttu-id="04aad-231">True</span><span class="sxs-lookup"><span data-stu-id="04aad-231">True</span></span>                                         |
| <span data-ttu-id="04aad-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="04aad-232">Is Indexed</span></span>             | <span data-ttu-id="04aad-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-233">False</span></span>                                        |
| <span data-ttu-id="04aad-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="04aad-234">In Global Catalog</span></span>      | <span data-ttu-id="04aad-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-235">False</span></span>                                        |
| <span data-ttu-id="04aad-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="04aad-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="04aad-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04aad-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="04aad-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04aad-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="04aad-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04aad-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="04aad-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-240">Search-Flags</span></span>           | <span data-ttu-id="04aad-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04aad-241">0x00000000</span></span>                                   |
| <span data-ttu-id="04aad-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-242">System-Flags</span></span>           | <span data-ttu-id="04aad-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04aad-243">0x00000010</span></span>                                   |
| <span data-ttu-id="04aad-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="04aad-244">Classes used in</span></span>        | [<span data-ttu-id="04aad-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="04aad-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04aad-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04aad-246">Windows Server 2012</span></span>



| <span data-ttu-id="04aad-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="04aad-247">Entry</span></span> | <span data-ttu-id="04aad-248">Значение</span><span class="sxs-lookup"><span data-stu-id="04aad-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="04aad-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="04aad-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04aad-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="04aad-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="04aad-251">System-Only</span></span>            | <span data-ttu-id="04aad-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-252">False</span></span>                                        |
| <span data-ttu-id="04aad-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="04aad-253">Is-Single-Valued</span></span>       | <span data-ttu-id="04aad-254">True</span><span class="sxs-lookup"><span data-stu-id="04aad-254">True</span></span>                                         |
| <span data-ttu-id="04aad-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="04aad-255">Is Indexed</span></span>             | <span data-ttu-id="04aad-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-256">False</span></span>                                        |
| <span data-ttu-id="04aad-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="04aad-257">In Global Catalog</span></span>      | <span data-ttu-id="04aad-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="04aad-258">False</span></span>                                        |
| <span data-ttu-id="04aad-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="04aad-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="04aad-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04aad-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="04aad-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04aad-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="04aad-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04aad-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="04aad-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-263">Search-Flags</span></span>           | <span data-ttu-id="04aad-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04aad-264">0x00000000</span></span>                                   |
| <span data-ttu-id="04aad-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04aad-265">System-Flags</span></span>           | <span data-ttu-id="04aad-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04aad-266">0x00000010</span></span>                                   |
| <span data-ttu-id="04aad-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="04aad-267">Classes used in</span></span>        | [<span data-ttu-id="04aad-268">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="04aad-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





