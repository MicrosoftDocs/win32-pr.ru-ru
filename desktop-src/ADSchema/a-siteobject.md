---
title: Атрибут Site-Object
description: Различающееся имя для сайта, к которому принадлежит эта подсеть.
ms.assetid: 4533c742-4276-48df-b0cd-7ba1641737a7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Site-Object
- Схема AD атрибута Ситеобжект
topic_type:
- apiref
api_name:
- Site-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac43fb4ee0718aec855de4b7eb251a5d67c1a5fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893646"
---
# <a name="site-object-attribute"></a><span data-ttu-id="69fb4-105">Атрибут Site-Object</span><span class="sxs-lookup"><span data-stu-id="69fb4-105">Site-Object attribute</span></span>

<span data-ttu-id="69fb4-106">Различающееся имя для сайта, к которому принадлежит эта подсеть.</span><span class="sxs-lookup"><span data-stu-id="69fb4-106">The distinguished name for the site to which this subnet belongs.</span></span>



| <span data-ttu-id="69fb4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-107">Entry</span></span> | <span data-ttu-id="69fb4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="69fb4-109">CN</span><span class="sxs-lookup"><span data-stu-id="69fb4-109">CN</span></span>                | <span data-ttu-id="69fb4-110">Site-Object</span><span class="sxs-lookup"><span data-stu-id="69fb4-110">Site-Object</span></span>                             |
| <span data-ttu-id="69fb4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="69fb4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69fb4-112">ситеобжект</span><span class="sxs-lookup"><span data-stu-id="69fb4-112">siteObject</span></span>                              |
| <span data-ttu-id="69fb4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="69fb4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="69fb4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="69fb4-114">Update Privilege</span></span>  | <span data-ttu-id="69fb4-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="69fb4-115">Domain administrator</span></span>                    |
| <span data-ttu-id="69fb4-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="69fb4-116">Update Frequency</span></span>  | <span data-ttu-id="69fb4-117">При создании сайта.</span><span class="sxs-lookup"><span data-stu-id="69fb4-117">Whenever a site is created.</span></span>             |
| <span data-ttu-id="69fb4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-118">Attribute-Id</span></span>      | <span data-ttu-id="69fb4-119">1.2.840.113556.1.4.512</span><span class="sxs-lookup"><span data-stu-id="69fb4-119">1.2.840.113556.1.4.512</span></span>                  |
| <span data-ttu-id="69fb4-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="69fb4-120">System-Id-Guid</span></span>    | <span data-ttu-id="69fb4-121">3e10944c-c354-11d0-aff8-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="69fb4-121">3e10944c-c354-11d0-aff8-0000f80367c1</span></span>    |
| <span data-ttu-id="69fb4-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69fb4-122">Syntax</span></span>            | [<span data-ttu-id="69fb4-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="69fb4-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="69fb4-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="69fb4-124">Implementations</span></span>

-   [<span data-ttu-id="69fb4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69fb4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69fb4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69fb4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69fb4-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="69fb4-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="69fb4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69fb4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69fb4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69fb4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69fb4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69fb4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69fb4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69fb4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69fb4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69fb4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="69fb4-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-133">Entry</span></span> | <span data-ttu-id="69fb4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-135">Link-Id</span></span>                | <span data-ttu-id="69fb4-136">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-136">46</span></span>                                    |
| <span data-ttu-id="69fb4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-138">System-Only</span></span>            | <span data-ttu-id="69fb4-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-139">False</span></span>                                 |
| <span data-ttu-id="69fb4-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-141">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-141">True</span></span>                                  |
| <span data-ttu-id="69fb4-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-142">Is Indexed</span></span>             | <span data-ttu-id="69fb4-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-143">False</span></span>                                 |
| <span data-ttu-id="69fb4-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-144">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-145">False</span></span>                                 |
| <span data-ttu-id="69fb4-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-150">Search-Flags</span></span>           | <span data-ttu-id="69fb4-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-151">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-152">System-Flags</span></span>           | <span data-ttu-id="69fb4-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-153">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-154">Classes used in</span></span>        | [<span data-ttu-id="69fb4-155">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-155">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69fb4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69fb4-156">Windows Server 2003</span></span>



| <span data-ttu-id="69fb4-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-157">Entry</span></span> | <span data-ttu-id="69fb4-158">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-159">Link-Id</span></span>                | <span data-ttu-id="69fb4-160">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-160">46</span></span>                                    |
| <span data-ttu-id="69fb4-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-162">System-Only</span></span>            | <span data-ttu-id="69fb4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-163">False</span></span>                                 |
| <span data-ttu-id="69fb4-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-164">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-165">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-165">True</span></span>                                  |
| <span data-ttu-id="69fb4-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-166">Is Indexed</span></span>             | <span data-ttu-id="69fb4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-167">False</span></span>                                 |
| <span data-ttu-id="69fb4-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-168">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-169">False</span></span>                                 |
| <span data-ttu-id="69fb4-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-174">Search-Flags</span></span>           | <span data-ttu-id="69fb4-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-175">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-176">System-Flags</span></span>           | <span data-ttu-id="69fb4-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-177">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-178">Classes used in</span></span>        | [<span data-ttu-id="69fb4-179">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-179">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="adam"></a><span data-ttu-id="69fb4-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="69fb4-180">ADAM</span></span>



| <span data-ttu-id="69fb4-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-181">Entry</span></span> | <span data-ttu-id="69fb4-182">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-183">Link-Id</span></span>                | <span data-ttu-id="69fb4-184">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-184">46</span></span>                                    |
| <span data-ttu-id="69fb4-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-186">System-Only</span></span>            | <span data-ttu-id="69fb4-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-187">False</span></span>                                 |
| <span data-ttu-id="69fb4-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-188">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-189">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-189">True</span></span>                                  |
| <span data-ttu-id="69fb4-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-190">Is Indexed</span></span>             | <span data-ttu-id="69fb4-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-191">False</span></span>                                 |
| <span data-ttu-id="69fb4-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-192">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-193">False</span></span>                                 |
| <span data-ttu-id="69fb4-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-198">Search-Flags</span></span>           | <span data-ttu-id="69fb4-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-199">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-200">System-Flags</span></span>           | <span data-ttu-id="69fb4-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-201">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-202">Classes used in</span></span>        | [<span data-ttu-id="69fb4-203">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-203">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69fb4-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69fb4-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69fb4-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-205">Entry</span></span> | <span data-ttu-id="69fb4-206">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-207">Link-Id</span></span>                | <span data-ttu-id="69fb4-208">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-208">46</span></span>                                    |
| <span data-ttu-id="69fb4-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-210">System-Only</span></span>            | <span data-ttu-id="69fb4-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-211">False</span></span>                                 |
| <span data-ttu-id="69fb4-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-212">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-213">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-213">True</span></span>                                  |
| <span data-ttu-id="69fb4-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-214">Is Indexed</span></span>             | <span data-ttu-id="69fb4-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-215">False</span></span>                                 |
| <span data-ttu-id="69fb4-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-216">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-217">False</span></span>                                 |
| <span data-ttu-id="69fb4-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-222">Search-Flags</span></span>           | <span data-ttu-id="69fb4-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-223">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-224">System-Flags</span></span>           | <span data-ttu-id="69fb4-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-225">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-226">Classes used in</span></span>        | [<span data-ttu-id="69fb4-227">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-227">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69fb4-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69fb4-228">Windows Server 2008</span></span>



| <span data-ttu-id="69fb4-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-229">Entry</span></span> | <span data-ttu-id="69fb4-230">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-231">Link-Id</span></span>                | <span data-ttu-id="69fb4-232">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-232">46</span></span>                                    |
| <span data-ttu-id="69fb4-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-234">System-Only</span></span>            | <span data-ttu-id="69fb4-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-235">False</span></span>                                 |
| <span data-ttu-id="69fb4-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-236">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-237">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-237">True</span></span>                                  |
| <span data-ttu-id="69fb4-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-238">Is Indexed</span></span>             | <span data-ttu-id="69fb4-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-239">False</span></span>                                 |
| <span data-ttu-id="69fb4-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-240">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-241">False</span></span>                                 |
| <span data-ttu-id="69fb4-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-246">Search-Flags</span></span>           | <span data-ttu-id="69fb4-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-247">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-248">System-Flags</span></span>           | <span data-ttu-id="69fb4-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-249">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-250">Classes used in</span></span>        | [<span data-ttu-id="69fb4-251">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-251">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69fb4-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69fb4-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69fb4-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-253">Entry</span></span> | <span data-ttu-id="69fb4-254">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-255">Link-Id</span></span>                | <span data-ttu-id="69fb4-256">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-256">46</span></span>                                    |
| <span data-ttu-id="69fb4-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-258">System-Only</span></span>            | <span data-ttu-id="69fb4-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-259">False</span></span>                                 |
| <span data-ttu-id="69fb4-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-260">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-261">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-261">True</span></span>                                  |
| <span data-ttu-id="69fb4-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-262">Is Indexed</span></span>             | <span data-ttu-id="69fb4-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-263">False</span></span>                                 |
| <span data-ttu-id="69fb4-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-264">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-265">False</span></span>                                 |
| <span data-ttu-id="69fb4-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-270">Search-Flags</span></span>           | <span data-ttu-id="69fb4-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-271">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-272">System-Flags</span></span>           | <span data-ttu-id="69fb4-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-273">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-274">Classes used in</span></span>        | [<span data-ttu-id="69fb4-275">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-275">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69fb4-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69fb4-276">Windows Server 2012</span></span>



| <span data-ttu-id="69fb4-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="69fb4-277">Entry</span></span> | <span data-ttu-id="69fb4-278">Значение</span><span class="sxs-lookup"><span data-stu-id="69fb4-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69fb4-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69fb4-279">Link-Id</span></span>                | <span data-ttu-id="69fb4-280">46</span><span class="sxs-lookup"><span data-stu-id="69fb4-280">46</span></span>                                    |
| <span data-ttu-id="69fb4-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69fb4-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69fb4-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="69fb4-282">System-Only</span></span>            | <span data-ttu-id="69fb4-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-283">False</span></span>                                 |
| <span data-ttu-id="69fb4-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69fb4-284">Is-Single-Valued</span></span>       | <span data-ttu-id="69fb4-285">True</span><span class="sxs-lookup"><span data-stu-id="69fb4-285">True</span></span>                                  |
| <span data-ttu-id="69fb4-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69fb4-286">Is Indexed</span></span>             | <span data-ttu-id="69fb4-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-287">False</span></span>                                 |
| <span data-ttu-id="69fb4-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69fb4-288">In Global Catalog</span></span>      | <span data-ttu-id="69fb4-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="69fb4-289">False</span></span>                                 |
| <span data-ttu-id="69fb4-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69fb4-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="69fb4-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69fb4-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69fb4-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69fb4-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69fb4-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69fb4-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-294">Search-Flags</span></span>           | <span data-ttu-id="69fb4-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69fb4-295">0x00000000</span></span>                            |
| <span data-ttu-id="69fb4-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69fb4-296">System-Flags</span></span>           | <span data-ttu-id="69fb4-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69fb4-297">0x00000010</span></span>                            |
| <span data-ttu-id="69fb4-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69fb4-298">Classes used in</span></span>        | [<span data-ttu-id="69fb4-299">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="69fb4-299">**Subnet**</span></span>](c-subnet.md)<br/> |



 

 





