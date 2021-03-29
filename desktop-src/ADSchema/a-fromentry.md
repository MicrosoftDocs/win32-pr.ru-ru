---
title: Атрибут From-Entry
description: Это сконструированный атрибут, который имеет значение TRUE, если объект доступен для записи, и значение FALSE, если он доступен только для чтения, например экземпляр реплики GC.
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута From-Entry
- Схема AD атрибута Фроментри
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654953"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="fdffe-105">Атрибут From-Entry</span><span class="sxs-lookup"><span data-stu-id="fdffe-105">From-Entry attribute</span></span>

<span data-ttu-id="fdffe-106">Это сконструированный атрибут, который имеет **значение true** , если объект доступен для записи, и **значение false** , если он доступен только для чтения, например экземпляр реплики GC.</span><span class="sxs-lookup"><span data-stu-id="fdffe-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="fdffe-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-107">Entry</span></span> | <span data-ttu-id="fdffe-108">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fdffe-109">CN</span><span class="sxs-lookup"><span data-stu-id="fdffe-109">CN</span></span>                | <span data-ttu-id="fdffe-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="fdffe-110">From-Entry</span></span>                           |
| <span data-ttu-id="fdffe-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fdffe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fdffe-112">фроментри</span><span class="sxs-lookup"><span data-stu-id="fdffe-112">fromEntry</span></span>                            |
| <span data-ttu-id="fdffe-113">Размер</span><span class="sxs-lookup"><span data-stu-id="fdffe-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="fdffe-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fdffe-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fdffe-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fdffe-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fdffe-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-116">Attribute-Id</span></span>      | <span data-ttu-id="fdffe-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="fdffe-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="fdffe-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fdffe-118">System-Id-Guid</span></span>    | <span data-ttu-id="fdffe-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="fdffe-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="fdffe-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdffe-120">Syntax</span></span>            | [<span data-ttu-id="fdffe-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="fdffe-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fdffe-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fdffe-122">Implementations</span></span>

-   [<span data-ttu-id="fdffe-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fdffe-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fdffe-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fdffe-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fdffe-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="fdffe-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fdffe-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fdffe-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fdffe-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fdffe-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fdffe-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fdffe-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fdffe-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fdffe-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fdffe-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fdffe-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fdffe-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-131">Entry</span></span> | <span data-ttu-id="fdffe-132">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-135">System-Only</span></span>            | <span data-ttu-id="fdffe-136">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-136">True</span></span>                            |
| <span data-ttu-id="fdffe-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-138">False</span></span>                           |
| <span data-ttu-id="fdffe-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-139">Is Indexed</span></span>             | <span data-ttu-id="fdffe-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-140">False</span></span>                           |
| <span data-ttu-id="fdffe-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-141">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-142">False</span></span>                           |
| <span data-ttu-id="fdffe-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-147">Search-Flags</span></span>           | <span data-ttu-id="fdffe-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-148">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-149">System-Flags</span></span>           | <span data-ttu-id="fdffe-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-150">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-151">Classes used in</span></span>        | [<span data-ttu-id="fdffe-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fdffe-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fdffe-153">Windows Server 2003</span></span>



| <span data-ttu-id="fdffe-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-154">Entry</span></span> | <span data-ttu-id="fdffe-155">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-158">System-Only</span></span>            | <span data-ttu-id="fdffe-159">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-159">True</span></span>                            |
| <span data-ttu-id="fdffe-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-161">False</span></span>                           |
| <span data-ttu-id="fdffe-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-162">Is Indexed</span></span>             | <span data-ttu-id="fdffe-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-163">False</span></span>                           |
| <span data-ttu-id="fdffe-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-164">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-165">False</span></span>                           |
| <span data-ttu-id="fdffe-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-170">Search-Flags</span></span>           | <span data-ttu-id="fdffe-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-171">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-172">System-Flags</span></span>           | <span data-ttu-id="fdffe-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-173">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-174">Classes used in</span></span>        | [<span data-ttu-id="fdffe-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fdffe-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="fdffe-176">ADAM</span></span>



| <span data-ttu-id="fdffe-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-177">Entry</span></span> | <span data-ttu-id="fdffe-178">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-181">System-Only</span></span>            | <span data-ttu-id="fdffe-182">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-182">True</span></span>                            |
| <span data-ttu-id="fdffe-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-184">False</span></span>                           |
| <span data-ttu-id="fdffe-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-185">Is Indexed</span></span>             | <span data-ttu-id="fdffe-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-186">False</span></span>                           |
| <span data-ttu-id="fdffe-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-187">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-188">False</span></span>                           |
| <span data-ttu-id="fdffe-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-193">Search-Flags</span></span>           | <span data-ttu-id="fdffe-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-194">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-195">System-Flags</span></span>           | <span data-ttu-id="fdffe-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-196">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-197">Classes used in</span></span>        | [<span data-ttu-id="fdffe-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fdffe-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fdffe-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fdffe-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-200">Entry</span></span> | <span data-ttu-id="fdffe-201">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-204">System-Only</span></span>            | <span data-ttu-id="fdffe-205">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-205">True</span></span>                            |
| <span data-ttu-id="fdffe-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-207">False</span></span>                           |
| <span data-ttu-id="fdffe-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-208">Is Indexed</span></span>             | <span data-ttu-id="fdffe-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-209">False</span></span>                           |
| <span data-ttu-id="fdffe-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-210">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-211">False</span></span>                           |
| <span data-ttu-id="fdffe-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-216">Search-Flags</span></span>           | <span data-ttu-id="fdffe-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-217">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-218">System-Flags</span></span>           | <span data-ttu-id="fdffe-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-219">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-220">Classes used in</span></span>        | [<span data-ttu-id="fdffe-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fdffe-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdffe-222">Windows Server 2008</span></span>



| <span data-ttu-id="fdffe-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-223">Entry</span></span> | <span data-ttu-id="fdffe-224">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-227">System-Only</span></span>            | <span data-ttu-id="fdffe-228">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-228">True</span></span>                            |
| <span data-ttu-id="fdffe-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-230">False</span></span>                           |
| <span data-ttu-id="fdffe-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-231">Is Indexed</span></span>             | <span data-ttu-id="fdffe-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-232">False</span></span>                           |
| <span data-ttu-id="fdffe-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-233">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-234">False</span></span>                           |
| <span data-ttu-id="fdffe-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-239">Search-Flags</span></span>           | <span data-ttu-id="fdffe-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-240">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-241">System-Flags</span></span>           | <span data-ttu-id="fdffe-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-242">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-243">Classes used in</span></span>        | [<span data-ttu-id="fdffe-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fdffe-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fdffe-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fdffe-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-246">Entry</span></span> | <span data-ttu-id="fdffe-247">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-250">System-Only</span></span>            | <span data-ttu-id="fdffe-251">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-251">True</span></span>                            |
| <span data-ttu-id="fdffe-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-252">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-253">False</span></span>                           |
| <span data-ttu-id="fdffe-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-254">Is Indexed</span></span>             | <span data-ttu-id="fdffe-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-255">False</span></span>                           |
| <span data-ttu-id="fdffe-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-256">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-257">False</span></span>                           |
| <span data-ttu-id="fdffe-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-262">Search-Flags</span></span>           | <span data-ttu-id="fdffe-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-263">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-264">System-Flags</span></span>           | <span data-ttu-id="fdffe-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-265">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-266">Classes used in</span></span>        | [<span data-ttu-id="fdffe-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fdffe-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdffe-268">Windows Server 2012</span></span>



| <span data-ttu-id="fdffe-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdffe-269">Entry</span></span> | <span data-ttu-id="fdffe-270">Значение</span><span class="sxs-lookup"><span data-stu-id="fdffe-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fdffe-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdffe-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdffe-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fdffe-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdffe-273">System-Only</span></span>            | <span data-ttu-id="fdffe-274">True</span><span class="sxs-lookup"><span data-stu-id="fdffe-274">True</span></span>                            |
| <span data-ttu-id="fdffe-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdffe-275">Is-Single-Valued</span></span>       | <span data-ttu-id="fdffe-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-276">False</span></span>                           |
| <span data-ttu-id="fdffe-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdffe-277">Is Indexed</span></span>             | <span data-ttu-id="fdffe-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-278">False</span></span>                           |
| <span data-ttu-id="fdffe-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdffe-279">In Global Catalog</span></span>      | <span data-ttu-id="fdffe-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdffe-280">False</span></span>                           |
| <span data-ttu-id="fdffe-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdffe-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdffe-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdffe-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fdffe-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdffe-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fdffe-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdffe-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fdffe-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-285">Search-Flags</span></span>           | <span data-ttu-id="fdffe-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdffe-286">0x00000000</span></span>                      |
| <span data-ttu-id="fdffe-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdffe-287">System-Flags</span></span>           | <span data-ttu-id="fdffe-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdffe-288">0x08000014</span></span>                      |
| <span data-ttu-id="fdffe-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdffe-289">Classes used in</span></span>        | [<span data-ttu-id="fdffe-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="fdffe-290">**Top**</span></span>](c-top.md)<br/> |



 

 





