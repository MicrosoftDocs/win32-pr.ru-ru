---
title: Атрибут ANR
description: Неоднозначный атрибут разрешения имени, используемый при выборе между объектами.
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ANR
- Схема AD атрибута aNR
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494115"
---
# <a name="anr-attribute"></a><span data-ttu-id="2eae2-105">Атрибут ANR</span><span class="sxs-lookup"><span data-stu-id="2eae2-105">ANR attribute</span></span>

<span data-ttu-id="2eae2-106">Неоднозначный атрибут разрешения имени, используемый при выборе между объектами.</span><span class="sxs-lookup"><span data-stu-id="2eae2-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="2eae2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-107">Entry</span></span> | <span data-ttu-id="2eae2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2eae2-109">CN</span><span class="sxs-lookup"><span data-stu-id="2eae2-109">CN</span></span>                | <span data-ttu-id="2eae2-110">ANR</span><span class="sxs-lookup"><span data-stu-id="2eae2-110">ANR</span></span>                                                               |
| <span data-ttu-id="2eae2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2eae2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2eae2-112">aNR</span><span class="sxs-lookup"><span data-stu-id="2eae2-112">aNR</span></span>                                                               |
| <span data-ttu-id="2eae2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2eae2-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="2eae2-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2eae2-114">Update Privilege</span></span>  | <span data-ttu-id="2eae2-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="2eae2-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="2eae2-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2eae2-116">Update Frequency</span></span>  | <span data-ttu-id="2eae2-117">При необходимости добавления или удаления атрибута из списка ANR.</span><span class="sxs-lookup"><span data-stu-id="2eae2-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="2eae2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-118">Attribute-Id</span></span>      | <span data-ttu-id="2eae2-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="2eae2-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="2eae2-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2eae2-120">System-Id-Guid</span></span>    | <span data-ttu-id="2eae2-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2eae2-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="2eae2-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eae2-122">Syntax</span></span>            | [<span data-ttu-id="2eae2-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2eae2-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="2eae2-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2eae2-124">Implementations</span></span>

-   [<span data-ttu-id="2eae2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2eae2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2eae2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2eae2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2eae2-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2eae2-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2eae2-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2eae2-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2eae2-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2eae2-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2eae2-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2eae2-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2eae2-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2eae2-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2eae2-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2eae2-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2eae2-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-133">Entry</span></span> | <span data-ttu-id="2eae2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-137">System-Only</span></span>            | <span data-ttu-id="2eae2-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-138">False</span></span>        |
| <span data-ttu-id="2eae2-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-140">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-140">True</span></span>         |
| <span data-ttu-id="2eae2-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-141">Is Indexed</span></span>             | <span data-ttu-id="2eae2-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-142">False</span></span>        |
| <span data-ttu-id="2eae2-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-143">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-144">False</span></span>        |
| <span data-ttu-id="2eae2-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-149">Search-Flags</span></span>           | <span data-ttu-id="2eae2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-150">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-151">System-Flags</span></span>           | <span data-ttu-id="2eae2-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-152">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="2eae2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2eae2-154">Windows Server 2003</span></span>



| <span data-ttu-id="2eae2-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-155">Entry</span></span> | <span data-ttu-id="2eae2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-159">System-Only</span></span>            | <span data-ttu-id="2eae2-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-160">False</span></span>        |
| <span data-ttu-id="2eae2-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-162">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-162">True</span></span>         |
| <span data-ttu-id="2eae2-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-163">Is Indexed</span></span>             | <span data-ttu-id="2eae2-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-164">False</span></span>        |
| <span data-ttu-id="2eae2-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-165">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-166">False</span></span>        |
| <span data-ttu-id="2eae2-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-171">Search-Flags</span></span>           | <span data-ttu-id="2eae2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-172">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-173">System-Flags</span></span>           | <span data-ttu-id="2eae2-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-174">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="2eae2-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="2eae2-176">ADAM</span></span>



| <span data-ttu-id="2eae2-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-177">Entry</span></span> | <span data-ttu-id="2eae2-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-181">System-Only</span></span>            | <span data-ttu-id="2eae2-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-182">False</span></span>        |
| <span data-ttu-id="2eae2-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-184">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-184">True</span></span>         |
| <span data-ttu-id="2eae2-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-185">Is Indexed</span></span>             | <span data-ttu-id="2eae2-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-186">False</span></span>        |
| <span data-ttu-id="2eae2-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-187">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-188">False</span></span>        |
| <span data-ttu-id="2eae2-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-193">Search-Flags</span></span>           | <span data-ttu-id="2eae2-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-194">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-195">System-Flags</span></span>           | <span data-ttu-id="2eae2-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-196">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2eae2-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2eae2-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2eae2-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-199">Entry</span></span> | <span data-ttu-id="2eae2-200">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-203">System-Only</span></span>            | <span data-ttu-id="2eae2-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-204">False</span></span>        |
| <span data-ttu-id="2eae2-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-206">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-206">True</span></span>         |
| <span data-ttu-id="2eae2-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-207">Is Indexed</span></span>             | <span data-ttu-id="2eae2-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-208">False</span></span>        |
| <span data-ttu-id="2eae2-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-209">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-210">False</span></span>        |
| <span data-ttu-id="2eae2-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-215">Search-Flags</span></span>           | <span data-ttu-id="2eae2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-216">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-217">System-Flags</span></span>           | <span data-ttu-id="2eae2-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-218">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="2eae2-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eae2-220">Windows Server 2008</span></span>



| <span data-ttu-id="2eae2-221">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-221">Entry</span></span> | <span data-ttu-id="2eae2-222">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-223">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-225">System-Only</span></span>            | <span data-ttu-id="2eae2-226">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-226">False</span></span>        |
| <span data-ttu-id="2eae2-227">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-227">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-228">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-228">True</span></span>         |
| <span data-ttu-id="2eae2-229">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-229">Is Indexed</span></span>             | <span data-ttu-id="2eae2-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-230">False</span></span>        |
| <span data-ttu-id="2eae2-231">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-231">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-232">False</span></span>        |
| <span data-ttu-id="2eae2-233">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-234">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-237">Search-Flags</span></span>           | <span data-ttu-id="2eae2-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-238">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-239">System-Flags</span></span>           | <span data-ttu-id="2eae2-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-240">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-241">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2eae2-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2eae2-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2eae2-243">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-243">Entry</span></span> | <span data-ttu-id="2eae2-244">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-245">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-247">System-Only</span></span>            | <span data-ttu-id="2eae2-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-248">False</span></span>        |
| <span data-ttu-id="2eae2-249">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-249">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-250">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-250">True</span></span>         |
| <span data-ttu-id="2eae2-251">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-251">Is Indexed</span></span>             | <span data-ttu-id="2eae2-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-252">False</span></span>        |
| <span data-ttu-id="2eae2-253">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-253">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-254">False</span></span>        |
| <span data-ttu-id="2eae2-255">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-256">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-259">Search-Flags</span></span>           | <span data-ttu-id="2eae2-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-260">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-261">System-Flags</span></span>           | <span data-ttu-id="2eae2-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-262">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="2eae2-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2eae2-264">Windows Server 2012</span></span>



| <span data-ttu-id="2eae2-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eae2-265">Entry</span></span> | <span data-ttu-id="2eae2-266">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae2-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="2eae2-267">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eae2-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eae2-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="2eae2-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eae2-269">System-Only</span></span>            | <span data-ttu-id="2eae2-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-270">False</span></span>        |
| <span data-ttu-id="2eae2-271">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eae2-271">Is-Single-Valued</span></span>       | <span data-ttu-id="2eae2-272">True</span><span class="sxs-lookup"><span data-stu-id="2eae2-272">True</span></span>         |
| <span data-ttu-id="2eae2-273">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eae2-273">Is Indexed</span></span>             | <span data-ttu-id="2eae2-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-274">False</span></span>        |
| <span data-ttu-id="2eae2-275">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eae2-275">In Global Catalog</span></span>      | <span data-ttu-id="2eae2-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eae2-276">False</span></span>        |
| <span data-ttu-id="2eae2-277">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eae2-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eae2-278">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eae2-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="2eae2-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eae2-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="2eae2-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eae2-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="2eae2-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-281">Search-Flags</span></span>           | <span data-ttu-id="2eae2-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eae2-282">0x00000000</span></span>   |
| <span data-ttu-id="2eae2-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eae2-283">System-Flags</span></span>           | <span data-ttu-id="2eae2-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2eae2-284">0x08000014</span></span>   |
| <span data-ttu-id="2eae2-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eae2-285">Classes used in</span></span>        | \-           |



 

 




