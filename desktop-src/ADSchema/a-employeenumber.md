---
title: Атрибут Employee-Number
description: Номер, назначенный сотруднику, отличному от идентификатора.
ms.assetid: 30ad1570-d833-48d0-b2aa-9447bcd33b92
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Employee-Number
- Схема AD атрибута Емплойинумбер
topic_type:
- apiref
api_name:
- Employee-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8eea803eb9ae0430d3c47c6b32f98216f83ca3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989569"
---
# <a name="employee-number-attribute"></a><span data-ttu-id="491f3-105">Атрибут Employee-Number</span><span class="sxs-lookup"><span data-stu-id="491f3-105">Employee-Number attribute</span></span>

<span data-ttu-id="491f3-106">Номер, назначенный сотруднику, отличному от идентификатора.</span><span class="sxs-lookup"><span data-stu-id="491f3-106">The number assigned to an employee other than the ID.</span></span>



| <span data-ttu-id="491f3-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-107">Entry</span></span> | <span data-ttu-id="491f3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="491f3-109">CN</span><span class="sxs-lookup"><span data-stu-id="491f3-109">CN</span></span>                | <span data-ttu-id="491f3-110">Employee-Number</span><span class="sxs-lookup"><span data-stu-id="491f3-110">Employee-Number</span></span>                             |
| <span data-ttu-id="491f3-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="491f3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="491f3-112">employeeNumber</span><span class="sxs-lookup"><span data-stu-id="491f3-112">employeeNumber</span></span>                              |
| <span data-ttu-id="491f3-113">Размер</span><span class="sxs-lookup"><span data-stu-id="491f3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="491f3-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="491f3-114">Update Privilege</span></span>  | <span data-ttu-id="491f3-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="491f3-115">Domain administrator</span></span>                        |
| <span data-ttu-id="491f3-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="491f3-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="491f3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-117">Attribute-Id</span></span>      | <span data-ttu-id="491f3-118">1.2.840.113556.1.2.610</span><span class="sxs-lookup"><span data-stu-id="491f3-118">1.2.840.113556.1.2.610</span></span>                      |
| <span data-ttu-id="491f3-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="491f3-119">System-Id-Guid</span></span>    | <span data-ttu-id="491f3-120">a8df73ef-c5ea-11d1-bbcb-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="491f3-120">a8df73ef-c5ea-11d1-bbcb-0080c76670c0</span></span>        |
| <span data-ttu-id="491f3-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="491f3-121">Syntax</span></span>            | [<span data-ttu-id="491f3-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="491f3-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="491f3-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="491f3-123">Implementations</span></span>

-   [<span data-ttu-id="491f3-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="491f3-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="491f3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="491f3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="491f3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="491f3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="491f3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="491f3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="491f3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="491f3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="491f3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="491f3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="491f3-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="491f3-130">Windows 2000 Server</span></span>



| <span data-ttu-id="491f3-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-131">Entry</span></span> | <span data-ttu-id="491f3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-132">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="491f3-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="491f3-133">Link-Id</span></span>                | \-           |
| <span data-ttu-id="491f3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-134">MAPI-Id</span></span>                | <span data-ttu-id="491f3-135">0x8C67</span><span class="sxs-lookup"><span data-stu-id="491f3-135">0x8C67</span></span>       |
| <span data-ttu-id="491f3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="491f3-136">System-Only</span></span>            | <span data-ttu-id="491f3-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-137">False</span></span>        |
| <span data-ttu-id="491f3-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="491f3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="491f3-139">True</span><span class="sxs-lookup"><span data-stu-id="491f3-139">True</span></span>         |
| <span data-ttu-id="491f3-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="491f3-140">Is Indexed</span></span>             | <span data-ttu-id="491f3-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-141">False</span></span>        |
| <span data-ttu-id="491f3-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="491f3-142">In Global Catalog</span></span>      | <span data-ttu-id="491f3-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-143">False</span></span>        |
| <span data-ttu-id="491f3-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="491f3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="491f3-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="491f3-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="491f3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="491f3-146">Range-Lower</span></span>            | <span data-ttu-id="491f3-147">1</span><span class="sxs-lookup"><span data-stu-id="491f3-147">1</span></span>            |
| <span data-ttu-id="491f3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="491f3-148">Range-Upper</span></span>            | <span data-ttu-id="491f3-149">512</span><span class="sxs-lookup"><span data-stu-id="491f3-149">512</span></span>          |
| <span data-ttu-id="491f3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-150">Search-Flags</span></span>           | <span data-ttu-id="491f3-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-151">0x00000000</span></span>   |
| <span data-ttu-id="491f3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-152">System-Flags</span></span>           | <span data-ttu-id="491f3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="491f3-153">0x00000010</span></span>   |
| <span data-ttu-id="491f3-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="491f3-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="491f3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="491f3-155">Windows Server 2003</span></span>



| <span data-ttu-id="491f3-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-156">Entry</span></span> | <span data-ttu-id="491f3-157">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="491f3-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="491f3-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="491f3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-159">MAPI-Id</span></span>                | <span data-ttu-id="491f3-160">0x8C67</span><span class="sxs-lookup"><span data-stu-id="491f3-160">0x8C67</span></span>       |
| <span data-ttu-id="491f3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="491f3-161">System-Only</span></span>            | <span data-ttu-id="491f3-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-162">False</span></span>        |
| <span data-ttu-id="491f3-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="491f3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="491f3-164">True</span><span class="sxs-lookup"><span data-stu-id="491f3-164">True</span></span>         |
| <span data-ttu-id="491f3-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="491f3-165">Is Indexed</span></span>             | <span data-ttu-id="491f3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-166">False</span></span>        |
| <span data-ttu-id="491f3-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="491f3-167">In Global Catalog</span></span>      | <span data-ttu-id="491f3-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-168">False</span></span>        |
| <span data-ttu-id="491f3-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="491f3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="491f3-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="491f3-170">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="491f3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="491f3-171">Range-Lower</span></span>            | <span data-ttu-id="491f3-172">1</span><span class="sxs-lookup"><span data-stu-id="491f3-172">1</span></span>            |
| <span data-ttu-id="491f3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="491f3-173">Range-Upper</span></span>            | <span data-ttu-id="491f3-174">512</span><span class="sxs-lookup"><span data-stu-id="491f3-174">512</span></span>          |
| <span data-ttu-id="491f3-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-175">Search-Flags</span></span>           | <span data-ttu-id="491f3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-176">0x00000000</span></span>   |
| <span data-ttu-id="491f3-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-177">System-Flags</span></span>           | <span data-ttu-id="491f3-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-178">0x00000000</span></span>   |
| <span data-ttu-id="491f3-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="491f3-179">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="491f3-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="491f3-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="491f3-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-181">Entry</span></span> | <span data-ttu-id="491f3-182">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-182">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="491f3-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="491f3-183">Link-Id</span></span>                | \-           |
| <span data-ttu-id="491f3-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-184">MAPI-Id</span></span>                | <span data-ttu-id="491f3-185">0x8C67</span><span class="sxs-lookup"><span data-stu-id="491f3-185">0x8C67</span></span>       |
| <span data-ttu-id="491f3-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="491f3-186">System-Only</span></span>            | <span data-ttu-id="491f3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-187">False</span></span>        |
| <span data-ttu-id="491f3-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="491f3-188">Is-Single-Valued</span></span>       | <span data-ttu-id="491f3-189">True</span><span class="sxs-lookup"><span data-stu-id="491f3-189">True</span></span>         |
| <span data-ttu-id="491f3-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="491f3-190">Is Indexed</span></span>             | <span data-ttu-id="491f3-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-191">False</span></span>        |
| <span data-ttu-id="491f3-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="491f3-192">In Global Catalog</span></span>      | <span data-ttu-id="491f3-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-193">False</span></span>        |
| <span data-ttu-id="491f3-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="491f3-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="491f3-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="491f3-195">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="491f3-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="491f3-196">Range-Lower</span></span>            | <span data-ttu-id="491f3-197">1</span><span class="sxs-lookup"><span data-stu-id="491f3-197">1</span></span>            |
| <span data-ttu-id="491f3-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="491f3-198">Range-Upper</span></span>            | <span data-ttu-id="491f3-199">512</span><span class="sxs-lookup"><span data-stu-id="491f3-199">512</span></span>          |
| <span data-ttu-id="491f3-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-200">Search-Flags</span></span>           | <span data-ttu-id="491f3-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-201">0x00000000</span></span>   |
| <span data-ttu-id="491f3-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-202">System-Flags</span></span>           | <span data-ttu-id="491f3-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-203">0x00000000</span></span>   |
| <span data-ttu-id="491f3-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="491f3-204">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="491f3-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="491f3-205">Windows Server 2008</span></span>



| <span data-ttu-id="491f3-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-206">Entry</span></span> | <span data-ttu-id="491f3-207">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-207">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="491f3-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="491f3-208">Link-Id</span></span>                | \-           |
| <span data-ttu-id="491f3-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-209">MAPI-Id</span></span>                | <span data-ttu-id="491f3-210">0x8C67</span><span class="sxs-lookup"><span data-stu-id="491f3-210">0x8C67</span></span>       |
| <span data-ttu-id="491f3-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="491f3-211">System-Only</span></span>            | <span data-ttu-id="491f3-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-212">False</span></span>        |
| <span data-ttu-id="491f3-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="491f3-213">Is-Single-Valued</span></span>       | <span data-ttu-id="491f3-214">True</span><span class="sxs-lookup"><span data-stu-id="491f3-214">True</span></span>         |
| <span data-ttu-id="491f3-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="491f3-215">Is Indexed</span></span>             | <span data-ttu-id="491f3-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-216">False</span></span>        |
| <span data-ttu-id="491f3-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="491f3-217">In Global Catalog</span></span>      | <span data-ttu-id="491f3-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-218">False</span></span>        |
| <span data-ttu-id="491f3-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="491f3-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="491f3-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="491f3-220">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="491f3-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="491f3-221">Range-Lower</span></span>            | <span data-ttu-id="491f3-222">1</span><span class="sxs-lookup"><span data-stu-id="491f3-222">1</span></span>            |
| <span data-ttu-id="491f3-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="491f3-223">Range-Upper</span></span>            | <span data-ttu-id="491f3-224">512</span><span class="sxs-lookup"><span data-stu-id="491f3-224">512</span></span>          |
| <span data-ttu-id="491f3-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-225">Search-Flags</span></span>           | <span data-ttu-id="491f3-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-226">0x00000000</span></span>   |
| <span data-ttu-id="491f3-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-227">System-Flags</span></span>           | <span data-ttu-id="491f3-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-228">0x00000000</span></span>   |
| <span data-ttu-id="491f3-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="491f3-229">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="491f3-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="491f3-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="491f3-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-231">Entry</span></span> | <span data-ttu-id="491f3-232">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-232">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="491f3-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="491f3-233">Link-Id</span></span>                | \-           |
| <span data-ttu-id="491f3-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-234">MAPI-Id</span></span>                | <span data-ttu-id="491f3-235">0x8C67</span><span class="sxs-lookup"><span data-stu-id="491f3-235">0x8C67</span></span>       |
| <span data-ttu-id="491f3-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="491f3-236">System-Only</span></span>            | <span data-ttu-id="491f3-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-237">False</span></span>        |
| <span data-ttu-id="491f3-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="491f3-238">Is-Single-Valued</span></span>       | <span data-ttu-id="491f3-239">True</span><span class="sxs-lookup"><span data-stu-id="491f3-239">True</span></span>         |
| <span data-ttu-id="491f3-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="491f3-240">Is Indexed</span></span>             | <span data-ttu-id="491f3-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-241">False</span></span>        |
| <span data-ttu-id="491f3-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="491f3-242">In Global Catalog</span></span>      | <span data-ttu-id="491f3-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-243">False</span></span>        |
| <span data-ttu-id="491f3-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="491f3-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="491f3-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="491f3-245">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="491f3-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="491f3-246">Range-Lower</span></span>            | <span data-ttu-id="491f3-247">1</span><span class="sxs-lookup"><span data-stu-id="491f3-247">1</span></span>            |
| <span data-ttu-id="491f3-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="491f3-248">Range-Upper</span></span>            | <span data-ttu-id="491f3-249">512</span><span class="sxs-lookup"><span data-stu-id="491f3-249">512</span></span>          |
| <span data-ttu-id="491f3-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-250">Search-Flags</span></span>           | <span data-ttu-id="491f3-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-251">0x00000000</span></span>   |
| <span data-ttu-id="491f3-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-252">System-Flags</span></span>           | <span data-ttu-id="491f3-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-253">0x00000000</span></span>   |
| <span data-ttu-id="491f3-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="491f3-254">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="491f3-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="491f3-255">Windows Server 2012</span></span>



| <span data-ttu-id="491f3-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="491f3-256">Entry</span></span> | <span data-ttu-id="491f3-257">Значение</span><span class="sxs-lookup"><span data-stu-id="491f3-257">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="491f3-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="491f3-258">Link-Id</span></span>                | \-           |
| <span data-ttu-id="491f3-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="491f3-259">MAPI-Id</span></span>                | <span data-ttu-id="491f3-260">0x8C67</span><span class="sxs-lookup"><span data-stu-id="491f3-260">0x8C67</span></span>       |
| <span data-ttu-id="491f3-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="491f3-261">System-Only</span></span>            | <span data-ttu-id="491f3-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-262">False</span></span>        |
| <span data-ttu-id="491f3-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="491f3-263">Is-Single-Valued</span></span>       | <span data-ttu-id="491f3-264">True</span><span class="sxs-lookup"><span data-stu-id="491f3-264">True</span></span>         |
| <span data-ttu-id="491f3-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="491f3-265">Is Indexed</span></span>             | <span data-ttu-id="491f3-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-266">False</span></span>        |
| <span data-ttu-id="491f3-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="491f3-267">In Global Catalog</span></span>      | <span data-ttu-id="491f3-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="491f3-268">False</span></span>        |
| <span data-ttu-id="491f3-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="491f3-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="491f3-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="491f3-270">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="491f3-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="491f3-271">Range-Lower</span></span>            | <span data-ttu-id="491f3-272">1</span><span class="sxs-lookup"><span data-stu-id="491f3-272">1</span></span>            |
| <span data-ttu-id="491f3-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="491f3-273">Range-Upper</span></span>            | <span data-ttu-id="491f3-274">512</span><span class="sxs-lookup"><span data-stu-id="491f3-274">512</span></span>          |
| <span data-ttu-id="491f3-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-275">Search-Flags</span></span>           | <span data-ttu-id="491f3-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-276">0x00000000</span></span>   |
| <span data-ttu-id="491f3-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="491f3-277">System-Flags</span></span>           | <span data-ttu-id="491f3-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="491f3-278">0x00000000</span></span>   |
| <span data-ttu-id="491f3-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="491f3-279">Classes used in</span></span>        | \-           |



 

 




