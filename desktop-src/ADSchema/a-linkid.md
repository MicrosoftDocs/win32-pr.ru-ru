---
title: Атрибут Link-ID
description: Целое число, указывающее, что атрибут является связанным атрибутом. Четное целое число — это прямая ссылка, а нечетное целое — обратная.
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ID ссылки
- Схема AD атрибута linkID
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536077"
---
# <a name="link-id-attribute"></a><span data-ttu-id="0ac8f-106">Атрибут Link-ID</span><span class="sxs-lookup"><span data-stu-id="0ac8f-106">Link-ID attribute</span></span>

<span data-ttu-id="0ac8f-107">Целое число, указывающее, что атрибут является связанным атрибутом.</span><span class="sxs-lookup"><span data-stu-id="0ac8f-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="0ac8f-108">Четное целое число — это прямая ссылка, а нечетное целое — обратная.</span><span class="sxs-lookup"><span data-stu-id="0ac8f-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="0ac8f-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-109">Entry</span></span> | <span data-ttu-id="0ac8f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0ac8f-111">CN</span><span class="sxs-lookup"><span data-stu-id="0ac8f-111">CN</span></span>                | <span data-ttu-id="0ac8f-112">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-112">Link-ID</span></span>                              |
| <span data-ttu-id="0ac8f-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0ac8f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0ac8f-114">Параметра</span><span class="sxs-lookup"><span data-stu-id="0ac8f-114">linkID</span></span>                               |
| <span data-ttu-id="0ac8f-115">Размер</span><span class="sxs-lookup"><span data-stu-id="0ac8f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="0ac8f-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0ac8f-116">Update Privilege</span></span>  | <span data-ttu-id="0ac8f-117">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="0ac8f-117">Schema administrator</span></span>                 |
| <span data-ttu-id="0ac8f-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0ac8f-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0ac8f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-119">Attribute-Id</span></span>      | <span data-ttu-id="0ac8f-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="0ac8f-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="0ac8f-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0ac8f-121">System-Id-Guid</span></span>    | <span data-ttu-id="0ac8f-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0ac8f-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0ac8f-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ac8f-123">Syntax</span></span>            | [<span data-ttu-id="0ac8f-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="0ac8f-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0ac8f-125">Implementations</span></span>

-   [<span data-ttu-id="0ac8f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0ac8f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0ac8f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0ac8f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0ac8f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0ac8f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0ac8f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0ac8f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ac8f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="0ac8f-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-134">Entry</span></span> | <span data-ttu-id="0ac8f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-137">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-138">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-139">System-Only</span></span>            | <span data-ttu-id="0ac8f-140">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-140">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-142">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-142">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-143">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-144">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-145">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-146">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-151">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-152">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-153">System-Flags</span></span>           | <span data-ttu-id="0ac8f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-154">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-155">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-156">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0ac8f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0ac8f-157">Windows Server 2003</span></span>



| <span data-ttu-id="0ac8f-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-158">Entry</span></span> | <span data-ttu-id="0ac8f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-161">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-162">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-163">System-Only</span></span>            | <span data-ttu-id="0ac8f-164">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-164">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-166">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-166">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-167">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-168">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-169">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-170">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-175">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-176">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-177">System-Flags</span></span>           | <span data-ttu-id="0ac8f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-178">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-179">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-180">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0ac8f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="0ac8f-181">ADAM</span></span>



| <span data-ttu-id="0ac8f-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-182">Entry</span></span> | <span data-ttu-id="0ac8f-183">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-185">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-186">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-187">System-Only</span></span>            | <span data-ttu-id="0ac8f-188">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-188">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-190">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-190">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-191">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-192">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-193">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-194">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-199">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-200">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-201">System-Flags</span></span>           | <span data-ttu-id="0ac8f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-202">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-203">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-204">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0ac8f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0ac8f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0ac8f-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-206">Entry</span></span> | <span data-ttu-id="0ac8f-207">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-209">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-210">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-211">System-Only</span></span>            | <span data-ttu-id="0ac8f-212">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-212">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-214">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-214">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-215">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-216">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-217">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-218">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-223">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-224">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-225">System-Flags</span></span>           | <span data-ttu-id="0ac8f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-226">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-227">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-228">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0ac8f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ac8f-229">Windows Server 2008</span></span>



| <span data-ttu-id="0ac8f-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-230">Entry</span></span> | <span data-ttu-id="0ac8f-231">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-233">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-234">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-235">System-Only</span></span>            | <span data-ttu-id="0ac8f-236">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-236">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-238">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-238">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-239">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-240">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-241">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-242">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-247">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-248">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-249">System-Flags</span></span>           | <span data-ttu-id="0ac8f-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-250">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-251">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-252">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0ac8f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0ac8f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0ac8f-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-254">Entry</span></span> | <span data-ttu-id="0ac8f-255">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-257">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-258">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-259">System-Only</span></span>            | <span data-ttu-id="0ac8f-260">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-260">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-262">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-262">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-263">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-264">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-265">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-266">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-271">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-272">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-273">System-Flags</span></span>           | <span data-ttu-id="0ac8f-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-274">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-275">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-276">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0ac8f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ac8f-277">Windows Server 2012</span></span>



| <span data-ttu-id="0ac8f-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ac8f-278">Entry</span></span> | <span data-ttu-id="0ac8f-279">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac8f-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ac8f-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ac8f-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ac8f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ac8f-281">MAPI-Id</span></span>                | <span data-ttu-id="0ac8f-282">0x80C5</span><span class="sxs-lookup"><span data-stu-id="0ac8f-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="0ac8f-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ac8f-283">System-Only</span></span>            | <span data-ttu-id="0ac8f-284">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-284">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ac8f-285">Is-Single-Valued</span></span>       | <span data-ttu-id="0ac8f-286">True</span><span class="sxs-lookup"><span data-stu-id="0ac8f-286">True</span></span>                                                     |
| <span data-ttu-id="0ac8f-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ac8f-287">Is Indexed</span></span>             | <span data-ttu-id="0ac8f-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-288">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ac8f-289">In Global Catalog</span></span>      | <span data-ttu-id="0ac8f-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ac8f-290">False</span></span>                                                    |
| <span data-ttu-id="0ac8f-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ac8f-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ac8f-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ac8f-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ac8f-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ac8f-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ac8f-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="0ac8f-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-295">Search-Flags</span></span>           | <span data-ttu-id="0ac8f-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ac8f-296">0x00000000</span></span>                                               |
| <span data-ttu-id="0ac8f-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ac8f-297">System-Flags</span></span>           | <span data-ttu-id="0ac8f-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ac8f-298">0x00000010</span></span>                                               |
| <span data-ttu-id="0ac8f-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ac8f-299">Classes used in</span></span>        | [<span data-ttu-id="0ac8f-300">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="0ac8f-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





