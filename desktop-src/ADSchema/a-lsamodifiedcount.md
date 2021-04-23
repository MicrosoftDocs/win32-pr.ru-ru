---
title: LSA-Modified-Count, атрибут
description: Атрибут LSA-Modified-Count используется для поддержки репликации в домены Windows NT 4,0.
ms.assetid: 6af5931c-5d4f-4061-81a1-e8947d760abc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута LSA-Modified-Count
- Схема AD атрибута Лсамодифиедкаунт
topic_type:
- apiref
api_name:
- LSA-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042d4d52974457eb1853a3705adb87cc24a7dc3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655240"
---
# <a name="lsa-modified-count-attribute"></a><span data-ttu-id="ec4eb-105">LSA-Modified-Count, атрибут</span><span class="sxs-lookup"><span data-stu-id="ec4eb-105">LSA-Modified-Count attribute</span></span>

<span data-ttu-id="ec4eb-106">Атрибут **LSA-Modified-Count** используется для поддержки репликации в домены Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="ec4eb-106">The **LSA-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="ec4eb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-107">Entry</span></span> | <span data-ttu-id="ec4eb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ec4eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="ec4eb-109">CN</span></span>                | <span data-ttu-id="ec4eb-110">LSA-Modified-recount</span><span class="sxs-lookup"><span data-stu-id="ec4eb-110">LSA-Modified-Count</span></span>                   |
| <span data-ttu-id="ec4eb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ec4eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ec4eb-112">лсамодифиедкаунт</span><span class="sxs-lookup"><span data-stu-id="ec4eb-112">lSAModifiedCount</span></span>                     |
| <span data-ttu-id="ec4eb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ec4eb-113">Size</span></span>              | <span data-ttu-id="ec4eb-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="ec4eb-114">8 bytes</span></span>                              |
| <span data-ttu-id="ec4eb-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ec4eb-115">Update Privilege</span></span>  | <span data-ttu-id="ec4eb-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="ec4eb-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ec4eb-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ec4eb-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ec4eb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-118">Attribute-Id</span></span>      | <span data-ttu-id="ec4eb-119">1.2.840.113556.1.4.67</span><span class="sxs-lookup"><span data-stu-id="ec4eb-119">1.2.840.113556.1.4.67</span></span>                |
| <span data-ttu-id="ec4eb-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ec4eb-120">System-Id-Guid</span></span>    | <span data-ttu-id="ec4eb-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ec4eb-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ec4eb-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec4eb-122">Syntax</span></span>            | [<span data-ttu-id="ec4eb-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ec4eb-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ec4eb-124">Implementations</span></span>

-   [<span data-ttu-id="ec4eb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec4eb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec4eb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec4eb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec4eb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec4eb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec4eb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec4eb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ec4eb-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-132">Entry</span></span> | <span data-ttu-id="ec4eb-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec4eb-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec4eb-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4eb-136">System-Only</span></span>            | <span data-ttu-id="ec4eb-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-137">False</span></span>                                        |
| <span data-ttu-id="ec4eb-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec4eb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4eb-139">True</span><span class="sxs-lookup"><span data-stu-id="ec4eb-139">True</span></span>                                         |
| <span data-ttu-id="ec4eb-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec4eb-140">Is Indexed</span></span>             | <span data-ttu-id="ec4eb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-141">False</span></span>                                        |
| <span data-ttu-id="ec4eb-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec4eb-142">In Global Catalog</span></span>      | <span data-ttu-id="ec4eb-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-143">False</span></span>                                        |
| <span data-ttu-id="ec4eb-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec4eb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4eb-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec4eb-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec4eb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4eb-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4eb-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-148">Search-Flags</span></span>           | <span data-ttu-id="ec4eb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4eb-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ec4eb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-150">System-Flags</span></span>           | <span data-ttu-id="ec4eb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4eb-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ec4eb-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec4eb-152">Classes used in</span></span>        | [<span data-ttu-id="ec4eb-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec4eb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec4eb-154">Windows Server 2003</span></span>



| <span data-ttu-id="ec4eb-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-155">Entry</span></span> | <span data-ttu-id="ec4eb-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec4eb-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec4eb-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4eb-159">System-Only</span></span>            | <span data-ttu-id="ec4eb-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-160">False</span></span>                                        |
| <span data-ttu-id="ec4eb-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec4eb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4eb-162">True</span><span class="sxs-lookup"><span data-stu-id="ec4eb-162">True</span></span>                                         |
| <span data-ttu-id="ec4eb-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec4eb-163">Is Indexed</span></span>             | <span data-ttu-id="ec4eb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-164">False</span></span>                                        |
| <span data-ttu-id="ec4eb-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec4eb-165">In Global Catalog</span></span>      | <span data-ttu-id="ec4eb-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-166">False</span></span>                                        |
| <span data-ttu-id="ec4eb-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec4eb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4eb-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec4eb-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec4eb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4eb-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4eb-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-171">Search-Flags</span></span>           | <span data-ttu-id="ec4eb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4eb-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ec4eb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-173">System-Flags</span></span>           | <span data-ttu-id="ec4eb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4eb-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ec4eb-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec4eb-175">Classes used in</span></span>        | [<span data-ttu-id="ec4eb-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec4eb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec4eb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec4eb-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-178">Entry</span></span> | <span data-ttu-id="ec4eb-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec4eb-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec4eb-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4eb-182">System-Only</span></span>            | <span data-ttu-id="ec4eb-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-183">False</span></span>                                        |
| <span data-ttu-id="ec4eb-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec4eb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4eb-185">True</span><span class="sxs-lookup"><span data-stu-id="ec4eb-185">True</span></span>                                         |
| <span data-ttu-id="ec4eb-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec4eb-186">Is Indexed</span></span>             | <span data-ttu-id="ec4eb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-187">False</span></span>                                        |
| <span data-ttu-id="ec4eb-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec4eb-188">In Global Catalog</span></span>      | <span data-ttu-id="ec4eb-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-189">False</span></span>                                        |
| <span data-ttu-id="ec4eb-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec4eb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4eb-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec4eb-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec4eb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4eb-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4eb-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-194">Search-Flags</span></span>           | <span data-ttu-id="ec4eb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4eb-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ec4eb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-196">System-Flags</span></span>           | <span data-ttu-id="ec4eb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4eb-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ec4eb-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec4eb-198">Classes used in</span></span>        | [<span data-ttu-id="ec4eb-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec4eb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec4eb-200">Windows Server 2008</span></span>



| <span data-ttu-id="ec4eb-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-201">Entry</span></span> | <span data-ttu-id="ec4eb-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec4eb-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec4eb-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4eb-205">System-Only</span></span>            | <span data-ttu-id="ec4eb-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-206">False</span></span>                                        |
| <span data-ttu-id="ec4eb-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec4eb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4eb-208">True</span><span class="sxs-lookup"><span data-stu-id="ec4eb-208">True</span></span>                                         |
| <span data-ttu-id="ec4eb-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec4eb-209">Is Indexed</span></span>             | <span data-ttu-id="ec4eb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-210">False</span></span>                                        |
| <span data-ttu-id="ec4eb-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec4eb-211">In Global Catalog</span></span>      | <span data-ttu-id="ec4eb-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-212">False</span></span>                                        |
| <span data-ttu-id="ec4eb-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec4eb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4eb-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec4eb-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec4eb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4eb-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4eb-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-217">Search-Flags</span></span>           | <span data-ttu-id="ec4eb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4eb-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ec4eb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-219">System-Flags</span></span>           | <span data-ttu-id="ec4eb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4eb-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ec4eb-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec4eb-221">Classes used in</span></span>        | [<span data-ttu-id="ec4eb-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec4eb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec4eb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec4eb-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-224">Entry</span></span> | <span data-ttu-id="ec4eb-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec4eb-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec4eb-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4eb-228">System-Only</span></span>            | <span data-ttu-id="ec4eb-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-229">False</span></span>                                        |
| <span data-ttu-id="ec4eb-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec4eb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4eb-231">True</span><span class="sxs-lookup"><span data-stu-id="ec4eb-231">True</span></span>                                         |
| <span data-ttu-id="ec4eb-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec4eb-232">Is Indexed</span></span>             | <span data-ttu-id="ec4eb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-233">False</span></span>                                        |
| <span data-ttu-id="ec4eb-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec4eb-234">In Global Catalog</span></span>      | <span data-ttu-id="ec4eb-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-235">False</span></span>                                        |
| <span data-ttu-id="ec4eb-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec4eb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4eb-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec4eb-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec4eb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4eb-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4eb-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-240">Search-Flags</span></span>           | <span data-ttu-id="ec4eb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4eb-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ec4eb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-242">System-Flags</span></span>           | <span data-ttu-id="ec4eb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4eb-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ec4eb-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec4eb-244">Classes used in</span></span>        | [<span data-ttu-id="ec4eb-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec4eb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec4eb-246">Windows Server 2012</span></span>



| <span data-ttu-id="ec4eb-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec4eb-247">Entry</span></span> | <span data-ttu-id="ec4eb-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4eb-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec4eb-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec4eb-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4eb-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec4eb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4eb-251">System-Only</span></span>            | <span data-ttu-id="ec4eb-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-252">False</span></span>                                        |
| <span data-ttu-id="ec4eb-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec4eb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4eb-254">True</span><span class="sxs-lookup"><span data-stu-id="ec4eb-254">True</span></span>                                         |
| <span data-ttu-id="ec4eb-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec4eb-255">Is Indexed</span></span>             | <span data-ttu-id="ec4eb-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-256">False</span></span>                                        |
| <span data-ttu-id="ec4eb-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec4eb-257">In Global Catalog</span></span>      | <span data-ttu-id="ec4eb-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec4eb-258">False</span></span>                                        |
| <span data-ttu-id="ec4eb-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec4eb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4eb-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec4eb-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec4eb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4eb-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4eb-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec4eb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-263">Search-Flags</span></span>           | <span data-ttu-id="ec4eb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4eb-264">0x00000000</span></span>                                   |
| <span data-ttu-id="ec4eb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4eb-265">System-Flags</span></span>           | <span data-ttu-id="ec4eb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4eb-266">0x00000010</span></span>                                   |
| <span data-ttu-id="ec4eb-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec4eb-267">Classes used in</span></span>        | [<span data-ttu-id="ec4eb-268">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="ec4eb-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





