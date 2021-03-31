---
title: Атрибут Privilege-Holder
description: Список различающихся имен участников, которым предоставлена эта привилегия.
ms.assetid: d7ae6de8-6725-436f-93e0-1dd966aa7c07
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Privilege-Holder
- Схема AD атрибута Привилежехолдер
topic_type:
- apiref
api_name:
- Privilege-Holder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f414e92f092eb6cb60f11807c9c5f3cdb20ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804846"
---
# <a name="privilege-holder-attribute"></a><span data-ttu-id="26018-105">Атрибут Privilege-Holder</span><span class="sxs-lookup"><span data-stu-id="26018-105">Privilege-Holder attribute</span></span>

<span data-ttu-id="26018-106">Список различающихся имен участников, которым предоставлена эта привилегия.</span><span class="sxs-lookup"><span data-stu-id="26018-106">List of Distinguished Names of principals granted this privilege.</span></span>



| <span data-ttu-id="26018-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-107">Entry</span></span> | <span data-ttu-id="26018-108">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="26018-109">CN</span><span class="sxs-lookup"><span data-stu-id="26018-109">CN</span></span>                | <span data-ttu-id="26018-110">Privilege-Holder</span><span class="sxs-lookup"><span data-stu-id="26018-110">Privilege-Holder</span></span>                        |
| <span data-ttu-id="26018-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="26018-111">Ldap-Display-Name</span></span> | <span data-ttu-id="26018-112">привилежехолдер</span><span class="sxs-lookup"><span data-stu-id="26018-112">privilegeHolder</span></span>                         |
| <span data-ttu-id="26018-113">Размер</span><span class="sxs-lookup"><span data-stu-id="26018-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="26018-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="26018-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="26018-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="26018-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="26018-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="26018-116">Attribute-Id</span></span>      | <span data-ttu-id="26018-117">1.2.840.113556.1.4.637</span><span class="sxs-lookup"><span data-stu-id="26018-117">1.2.840.113556.1.4.637</span></span>                  |
| <span data-ttu-id="26018-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="26018-118">System-Id-Guid</span></span>    | <span data-ttu-id="26018-119">19405b9b-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="26018-119">19405b9b-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="26018-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26018-120">Syntax</span></span>            | [<span data-ttu-id="26018-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="26018-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="26018-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="26018-122">Implementations</span></span>

-   [<span data-ttu-id="26018-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="26018-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="26018-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="26018-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="26018-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="26018-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="26018-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="26018-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="26018-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="26018-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="26018-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="26018-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="26018-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26018-129">Windows 2000 Server</span></span>



| <span data-ttu-id="26018-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-130">Entry</span></span> | <span data-ttu-id="26018-131">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="26018-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26018-132">Link-Id</span></span>                | <span data-ttu-id="26018-133">70</span><span class="sxs-lookup"><span data-stu-id="26018-133">70</span></span>           |
| <span data-ttu-id="26018-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26018-134">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="26018-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="26018-135">System-Only</span></span>            | <span data-ttu-id="26018-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-136">False</span></span>        |
| <span data-ttu-id="26018-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26018-137">Is-Single-Valued</span></span>       | <span data-ttu-id="26018-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-138">False</span></span>        |
| <span data-ttu-id="26018-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26018-139">Is Indexed</span></span>             | <span data-ttu-id="26018-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-140">False</span></span>        |
| <span data-ttu-id="26018-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26018-141">In Global Catalog</span></span>      | <span data-ttu-id="26018-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-142">False</span></span>        |
| <span data-ttu-id="26018-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26018-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="26018-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26018-144">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="26018-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26018-145">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="26018-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26018-146">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="26018-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-147">Search-Flags</span></span>           | <span data-ttu-id="26018-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26018-148">0x00000000</span></span>   |
| <span data-ttu-id="26018-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-149">System-Flags</span></span>           | <span data-ttu-id="26018-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26018-150">0x00000010</span></span>   |
| <span data-ttu-id="26018-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26018-151">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="26018-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26018-152">Windows Server 2003</span></span>



| <span data-ttu-id="26018-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-153">Entry</span></span> | <span data-ttu-id="26018-154">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-154">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="26018-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26018-155">Link-Id</span></span>                | <span data-ttu-id="26018-156">70</span><span class="sxs-lookup"><span data-stu-id="26018-156">70</span></span>           |
| <span data-ttu-id="26018-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26018-157">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="26018-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="26018-158">System-Only</span></span>            | <span data-ttu-id="26018-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-159">False</span></span>        |
| <span data-ttu-id="26018-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26018-160">Is-Single-Valued</span></span>       | <span data-ttu-id="26018-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-161">False</span></span>        |
| <span data-ttu-id="26018-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26018-162">Is Indexed</span></span>             | <span data-ttu-id="26018-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-163">False</span></span>        |
| <span data-ttu-id="26018-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26018-164">In Global Catalog</span></span>      | <span data-ttu-id="26018-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-165">False</span></span>        |
| <span data-ttu-id="26018-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26018-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="26018-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26018-167">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="26018-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26018-168">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="26018-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26018-169">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="26018-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-170">Search-Flags</span></span>           | <span data-ttu-id="26018-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26018-171">0x00000000</span></span>   |
| <span data-ttu-id="26018-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-172">System-Flags</span></span>           | <span data-ttu-id="26018-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26018-173">0x00000010</span></span>   |
| <span data-ttu-id="26018-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26018-174">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="26018-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="26018-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="26018-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-176">Entry</span></span> | <span data-ttu-id="26018-177">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-177">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="26018-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26018-178">Link-Id</span></span>                | <span data-ttu-id="26018-179">70</span><span class="sxs-lookup"><span data-stu-id="26018-179">70</span></span>           |
| <span data-ttu-id="26018-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26018-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="26018-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="26018-181">System-Only</span></span>            | <span data-ttu-id="26018-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-182">False</span></span>        |
| <span data-ttu-id="26018-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26018-183">Is-Single-Valued</span></span>       | <span data-ttu-id="26018-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-184">False</span></span>        |
| <span data-ttu-id="26018-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26018-185">Is Indexed</span></span>             | <span data-ttu-id="26018-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-186">False</span></span>        |
| <span data-ttu-id="26018-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26018-187">In Global Catalog</span></span>      | <span data-ttu-id="26018-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-188">False</span></span>        |
| <span data-ttu-id="26018-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26018-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="26018-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26018-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="26018-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26018-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="26018-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26018-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="26018-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-193">Search-Flags</span></span>           | <span data-ttu-id="26018-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26018-194">0x00000000</span></span>   |
| <span data-ttu-id="26018-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-195">System-Flags</span></span>           | <span data-ttu-id="26018-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26018-196">0x00000010</span></span>   |
| <span data-ttu-id="26018-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26018-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="26018-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26018-198">Windows Server 2008</span></span>



| <span data-ttu-id="26018-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-199">Entry</span></span> | <span data-ttu-id="26018-200">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="26018-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26018-201">Link-Id</span></span>                | <span data-ttu-id="26018-202">70</span><span class="sxs-lookup"><span data-stu-id="26018-202">70</span></span>           |
| <span data-ttu-id="26018-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26018-203">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="26018-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="26018-204">System-Only</span></span>            | <span data-ttu-id="26018-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-205">False</span></span>        |
| <span data-ttu-id="26018-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26018-206">Is-Single-Valued</span></span>       | <span data-ttu-id="26018-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-207">False</span></span>        |
| <span data-ttu-id="26018-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26018-208">Is Indexed</span></span>             | <span data-ttu-id="26018-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-209">False</span></span>        |
| <span data-ttu-id="26018-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26018-210">In Global Catalog</span></span>      | <span data-ttu-id="26018-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-211">False</span></span>        |
| <span data-ttu-id="26018-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26018-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="26018-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26018-213">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="26018-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26018-214">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="26018-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26018-215">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="26018-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-216">Search-Flags</span></span>           | <span data-ttu-id="26018-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26018-217">0x00000000</span></span>   |
| <span data-ttu-id="26018-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-218">System-Flags</span></span>           | <span data-ttu-id="26018-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26018-219">0x00000010</span></span>   |
| <span data-ttu-id="26018-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26018-220">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="26018-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26018-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="26018-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-222">Entry</span></span> | <span data-ttu-id="26018-223">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-223">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="26018-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26018-224">Link-Id</span></span>                | <span data-ttu-id="26018-225">70</span><span class="sxs-lookup"><span data-stu-id="26018-225">70</span></span>           |
| <span data-ttu-id="26018-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26018-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="26018-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="26018-227">System-Only</span></span>            | <span data-ttu-id="26018-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-228">False</span></span>        |
| <span data-ttu-id="26018-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26018-229">Is-Single-Valued</span></span>       | <span data-ttu-id="26018-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-230">False</span></span>        |
| <span data-ttu-id="26018-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26018-231">Is Indexed</span></span>             | <span data-ttu-id="26018-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-232">False</span></span>        |
| <span data-ttu-id="26018-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26018-233">In Global Catalog</span></span>      | <span data-ttu-id="26018-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-234">False</span></span>        |
| <span data-ttu-id="26018-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26018-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="26018-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26018-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="26018-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26018-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="26018-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26018-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="26018-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-239">Search-Flags</span></span>           | <span data-ttu-id="26018-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26018-240">0x00000000</span></span>   |
| <span data-ttu-id="26018-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-241">System-Flags</span></span>           | <span data-ttu-id="26018-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26018-242">0x00000010</span></span>   |
| <span data-ttu-id="26018-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26018-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="26018-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26018-244">Windows Server 2012</span></span>



| <span data-ttu-id="26018-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="26018-245">Entry</span></span> | <span data-ttu-id="26018-246">Значение</span><span class="sxs-lookup"><span data-stu-id="26018-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="26018-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="26018-247">Link-Id</span></span>                | <span data-ttu-id="26018-248">70</span><span class="sxs-lookup"><span data-stu-id="26018-248">70</span></span>           |
| <span data-ttu-id="26018-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26018-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="26018-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="26018-250">System-Only</span></span>            | <span data-ttu-id="26018-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-251">False</span></span>        |
| <span data-ttu-id="26018-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="26018-252">Is-Single-Valued</span></span>       | <span data-ttu-id="26018-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-253">False</span></span>        |
| <span data-ttu-id="26018-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="26018-254">Is Indexed</span></span>             | <span data-ttu-id="26018-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-255">False</span></span>        |
| <span data-ttu-id="26018-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="26018-256">In Global Catalog</span></span>      | <span data-ttu-id="26018-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="26018-257">False</span></span>        |
| <span data-ttu-id="26018-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="26018-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="26018-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26018-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="26018-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26018-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="26018-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26018-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="26018-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-262">Search-Flags</span></span>           | <span data-ttu-id="26018-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26018-263">0x00000000</span></span>   |
| <span data-ttu-id="26018-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26018-264">System-Flags</span></span>           | <span data-ttu-id="26018-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26018-265">0x00000010</span></span>   |
| <span data-ttu-id="26018-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="26018-266">Classes used in</span></span>        | \-           |



 

 




