---
title: Атрибут site-Object-BL
description: Список различающихся имен для подсетей, принадлежащих этому сайту.
ms.assetid: 70408711-7886-4a8e-9aeb-60354b418c2d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута site-Object-BL
- Схема AD атрибута Ситеобжектбл
topic_type:
- apiref
api_name:
- Site-Object-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba50b7a8f713cebfbbd1f19f5879cb46366128c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493689"
---
# <a name="site-object-bl-attribute"></a><span data-ttu-id="7edb9-105">Атрибут site-Object-BL</span><span class="sxs-lookup"><span data-stu-id="7edb9-105">Site-Object-BL attribute</span></span>

<span data-ttu-id="7edb9-106">Список различающихся имен для подсетей, принадлежащих этому сайту.</span><span class="sxs-lookup"><span data-stu-id="7edb9-106">The list of distinguished names for subnets that belong to this site.</span></span>



| <span data-ttu-id="7edb9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-107">Entry</span></span> | <span data-ttu-id="7edb9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7edb9-109">CN</span><span class="sxs-lookup"><span data-stu-id="7edb9-109">CN</span></span>                | <span data-ttu-id="7edb9-110">Site-Object-BL</span><span class="sxs-lookup"><span data-stu-id="7edb9-110">Site-Object-BL</span></span>                          |
| <span data-ttu-id="7edb9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7edb9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7edb9-112">ситеобжектбл</span><span class="sxs-lookup"><span data-stu-id="7edb9-112">siteObjectBL</span></span>                            |
| <span data-ttu-id="7edb9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7edb9-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7edb9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7edb9-114">Update Privilege</span></span>  | <span data-ttu-id="7edb9-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="7edb9-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="7edb9-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7edb9-116">Update Frequency</span></span>  | <span data-ttu-id="7edb9-117">При каждом создании или удалении сайта.</span><span class="sxs-lookup"><span data-stu-id="7edb9-117">Whenever a site is created or deleted.</span></span>  |
| <span data-ttu-id="7edb9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-118">Attribute-Id</span></span>      | <span data-ttu-id="7edb9-119">1.2.840.113556.1.4.513</span><span class="sxs-lookup"><span data-stu-id="7edb9-119">1.2.840.113556.1.4.513</span></span>                  |
| <span data-ttu-id="7edb9-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7edb9-120">System-Id-Guid</span></span>    | <span data-ttu-id="7edb9-121">3e10944d-c354-11d0-aff8-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7edb9-121">3e10944d-c354-11d0-aff8-0000f80367c1</span></span>    |
| <span data-ttu-id="7edb9-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7edb9-122">Syntax</span></span>            | [<span data-ttu-id="7edb9-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7edb9-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7edb9-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7edb9-124">Implementations</span></span>

-   [<span data-ttu-id="7edb9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7edb9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7edb9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7edb9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7edb9-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7edb9-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7edb9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7edb9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7edb9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7edb9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7edb9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7edb9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7edb9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7edb9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7edb9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7edb9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7edb9-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-133">Entry</span></span> | <span data-ttu-id="7edb9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-135">Link-Id</span></span>                | <span data-ttu-id="7edb9-136">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-136">47</span></span>                              |
| <span data-ttu-id="7edb9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-138">System-Only</span></span>            | <span data-ttu-id="7edb9-139">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-139">True</span></span>                            |
| <span data-ttu-id="7edb9-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-141">False</span></span>                           |
| <span data-ttu-id="7edb9-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-142">Is Indexed</span></span>             | <span data-ttu-id="7edb9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-143">False</span></span>                           |
| <span data-ttu-id="7edb9-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-144">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-145">False</span></span>                           |
| <span data-ttu-id="7edb9-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-150">Search-Flags</span></span>           | <span data-ttu-id="7edb9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-151">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-152">System-Flags</span></span>           | <span data-ttu-id="7edb9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-153">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-154">Classes used in</span></span>        | [<span data-ttu-id="7edb9-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7edb9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7edb9-156">Windows Server 2003</span></span>



| <span data-ttu-id="7edb9-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-157">Entry</span></span> | <span data-ttu-id="7edb9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-159">Link-Id</span></span>                | <span data-ttu-id="7edb9-160">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-160">47</span></span>                              |
| <span data-ttu-id="7edb9-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-162">System-Only</span></span>            | <span data-ttu-id="7edb9-163">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-163">True</span></span>                            |
| <span data-ttu-id="7edb9-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-165">False</span></span>                           |
| <span data-ttu-id="7edb9-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-166">Is Indexed</span></span>             | <span data-ttu-id="7edb9-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-167">False</span></span>                           |
| <span data-ttu-id="7edb9-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-168">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-169">False</span></span>                           |
| <span data-ttu-id="7edb9-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-174">Search-Flags</span></span>           | <span data-ttu-id="7edb9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-175">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-176">System-Flags</span></span>           | <span data-ttu-id="7edb9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-177">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-178">Classes used in</span></span>        | [<span data-ttu-id="7edb9-179">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7edb9-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="7edb9-180">ADAM</span></span>



| <span data-ttu-id="7edb9-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-181">Entry</span></span> | <span data-ttu-id="7edb9-182">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-183">Link-Id</span></span>                | <span data-ttu-id="7edb9-184">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-184">47</span></span>                              |
| <span data-ttu-id="7edb9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-186">System-Only</span></span>            | <span data-ttu-id="7edb9-187">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-187">True</span></span>                            |
| <span data-ttu-id="7edb9-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-189">False</span></span>                           |
| <span data-ttu-id="7edb9-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-190">Is Indexed</span></span>             | <span data-ttu-id="7edb9-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-191">False</span></span>                           |
| <span data-ttu-id="7edb9-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-192">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-193">False</span></span>                           |
| <span data-ttu-id="7edb9-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-198">Search-Flags</span></span>           | <span data-ttu-id="7edb9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-199">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-200">System-Flags</span></span>           | <span data-ttu-id="7edb9-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-201">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-202">Classes used in</span></span>        | [<span data-ttu-id="7edb9-203">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7edb9-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7edb9-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7edb9-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-205">Entry</span></span> | <span data-ttu-id="7edb9-206">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-207">Link-Id</span></span>                | <span data-ttu-id="7edb9-208">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-208">47</span></span>                              |
| <span data-ttu-id="7edb9-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-210">System-Only</span></span>            | <span data-ttu-id="7edb9-211">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-211">True</span></span>                            |
| <span data-ttu-id="7edb9-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-213">False</span></span>                           |
| <span data-ttu-id="7edb9-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-214">Is Indexed</span></span>             | <span data-ttu-id="7edb9-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-215">False</span></span>                           |
| <span data-ttu-id="7edb9-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-216">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-217">False</span></span>                           |
| <span data-ttu-id="7edb9-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-222">Search-Flags</span></span>           | <span data-ttu-id="7edb9-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-223">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-224">System-Flags</span></span>           | <span data-ttu-id="7edb9-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-225">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-226">Classes used in</span></span>        | [<span data-ttu-id="7edb9-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7edb9-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7edb9-228">Windows Server 2008</span></span>



| <span data-ttu-id="7edb9-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-229">Entry</span></span> | <span data-ttu-id="7edb9-230">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-231">Link-Id</span></span>                | <span data-ttu-id="7edb9-232">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-232">47</span></span>                              |
| <span data-ttu-id="7edb9-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-234">System-Only</span></span>            | <span data-ttu-id="7edb9-235">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-235">True</span></span>                            |
| <span data-ttu-id="7edb9-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-236">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-237">False</span></span>                           |
| <span data-ttu-id="7edb9-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-238">Is Indexed</span></span>             | <span data-ttu-id="7edb9-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-239">False</span></span>                           |
| <span data-ttu-id="7edb9-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-240">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-241">False</span></span>                           |
| <span data-ttu-id="7edb9-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-246">Search-Flags</span></span>           | <span data-ttu-id="7edb9-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-247">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-248">System-Flags</span></span>           | <span data-ttu-id="7edb9-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-249">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-250">Classes used in</span></span>        | [<span data-ttu-id="7edb9-251">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7edb9-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7edb9-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7edb9-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-253">Entry</span></span> | <span data-ttu-id="7edb9-254">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-255">Link-Id</span></span>                | <span data-ttu-id="7edb9-256">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-256">47</span></span>                              |
| <span data-ttu-id="7edb9-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-257">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-258">System-Only</span></span>            | <span data-ttu-id="7edb9-259">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-259">True</span></span>                            |
| <span data-ttu-id="7edb9-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-260">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-261">False</span></span>                           |
| <span data-ttu-id="7edb9-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-262">Is Indexed</span></span>             | <span data-ttu-id="7edb9-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-263">False</span></span>                           |
| <span data-ttu-id="7edb9-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-264">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-265">False</span></span>                           |
| <span data-ttu-id="7edb9-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-270">Search-Flags</span></span>           | <span data-ttu-id="7edb9-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-271">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-272">System-Flags</span></span>           | <span data-ttu-id="7edb9-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-273">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-274">Classes used in</span></span>        | [<span data-ttu-id="7edb9-275">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7edb9-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7edb9-276">Windows Server 2012</span></span>



| <span data-ttu-id="7edb9-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="7edb9-277">Entry</span></span> | <span data-ttu-id="7edb9-278">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7edb9-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7edb9-279">Link-Id</span></span>                | <span data-ttu-id="7edb9-280">47</span><span class="sxs-lookup"><span data-stu-id="7edb9-280">47</span></span>                              |
| <span data-ttu-id="7edb9-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7edb9-281">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7edb9-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="7edb9-282">System-Only</span></span>            | <span data-ttu-id="7edb9-283">True</span><span class="sxs-lookup"><span data-stu-id="7edb9-283">True</span></span>                            |
| <span data-ttu-id="7edb9-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7edb9-284">Is-Single-Valued</span></span>       | <span data-ttu-id="7edb9-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-285">False</span></span>                           |
| <span data-ttu-id="7edb9-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7edb9-286">Is Indexed</span></span>             | <span data-ttu-id="7edb9-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-287">False</span></span>                           |
| <span data-ttu-id="7edb9-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7edb9-288">In Global Catalog</span></span>      | <span data-ttu-id="7edb9-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="7edb9-289">False</span></span>                           |
| <span data-ttu-id="7edb9-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7edb9-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="7edb9-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7edb9-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7edb9-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7edb9-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7edb9-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7edb9-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7edb9-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-294">Search-Flags</span></span>           | <span data-ttu-id="7edb9-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7edb9-295">0x00000000</span></span>                      |
| <span data-ttu-id="7edb9-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7edb9-296">System-Flags</span></span>           | <span data-ttu-id="7edb9-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7edb9-297">0x00000010</span></span>                      |
| <span data-ttu-id="7edb9-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7edb9-298">Classes used in</span></span>        | [<span data-ttu-id="7edb9-299">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7edb9-299">**Top**</span></span>](c-top.md)<br/> |



 

 





