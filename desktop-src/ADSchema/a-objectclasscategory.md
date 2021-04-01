---
title: Атрибут "объект-класс-категория"
description: Этот атрибут содержит тип класса, например abstract, вспомогательный или структурированный.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута объекта-класса
- Схема AD атрибута objectClassCategory
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989643"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="4b8ef-105">Атрибут "объект-класс-категория"</span><span class="sxs-lookup"><span data-stu-id="4b8ef-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="4b8ef-106">Этот атрибут содержит тип класса, например abstract, вспомогательный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="4b8ef-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="4b8ef-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-107">Entry</span></span> | <span data-ttu-id="4b8ef-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4b8ef-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b8ef-109">CN</span></span>                | <span data-ttu-id="4b8ef-110">Объект-класс-категория</span><span class="sxs-lookup"><span data-stu-id="4b8ef-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="4b8ef-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4b8ef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b8ef-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="4b8ef-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="4b8ef-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4b8ef-113">Size</span></span>              | <span data-ttu-id="4b8ef-114">4 байта.</span><span class="sxs-lookup"><span data-stu-id="4b8ef-114">4 bytes.</span></span> <span data-ttu-id="4b8ef-115">Структур 1, абстрактно 2, дополнительный 3.</span><span class="sxs-lookup"><span data-stu-id="4b8ef-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="4b8ef-116">Класс 88, 0 не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="4b8ef-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="4b8ef-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4b8ef-117">Update Privilege</span></span>  | <span data-ttu-id="4b8ef-118">Это значение задается конструктором объекта.</span><span class="sxs-lookup"><span data-stu-id="4b8ef-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="4b8ef-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4b8ef-119">Update Frequency</span></span>  | <span data-ttu-id="4b8ef-120">Это значение никогда не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="4b8ef-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="4b8ef-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-121">Attribute-Id</span></span>      | <span data-ttu-id="4b8ef-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="4b8ef-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="4b8ef-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4b8ef-123">System-Id-Guid</span></span>    | <span data-ttu-id="4b8ef-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4b8ef-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="4b8ef-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b8ef-125">Syntax</span></span>            | [<span data-ttu-id="4b8ef-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="4b8ef-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4b8ef-127">Implementations</span></span>

-   [<span data-ttu-id="4b8ef-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b8ef-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b8ef-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4b8ef-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b8ef-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b8ef-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b8ef-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b8ef-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b8ef-135">Windows 2000 Server</span></span>



| <span data-ttu-id="4b8ef-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-136">Entry</span></span> | <span data-ttu-id="4b8ef-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-139">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-140">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-141">System-Only</span></span>            | <span data-ttu-id="4b8ef-142">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-142">True</span></span>                                             |
| <span data-ttu-id="4b8ef-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-143">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-144">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-144">True</span></span>                                             |
| <span data-ttu-id="4b8ef-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-145">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-146">False</span></span>                                            |
| <span data-ttu-id="4b8ef-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-147">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-148">False</span></span>                                            |
| <span data-ttu-id="4b8ef-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-151">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-152">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-152">0</span></span>                                                |
| <span data-ttu-id="4b8ef-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-153">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-154">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-154">3</span></span>                                                |
| <span data-ttu-id="4b8ef-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-155">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-156">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-157">System-Flags</span></span>           | <span data-ttu-id="4b8ef-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-158">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-159">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-159">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-160">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b8ef-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b8ef-161">Windows Server 2003</span></span>



| <span data-ttu-id="4b8ef-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-162">Entry</span></span> | <span data-ttu-id="4b8ef-163">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-165">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-166">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-167">System-Only</span></span>            | <span data-ttu-id="4b8ef-168">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-168">True</span></span>                                             |
| <span data-ttu-id="4b8ef-169">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-169">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-170">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-170">True</span></span>                                             |
| <span data-ttu-id="4b8ef-171">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-171">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-172">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-172">False</span></span>                                            |
| <span data-ttu-id="4b8ef-173">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-173">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-174">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-174">False</span></span>                                            |
| <span data-ttu-id="4b8ef-175">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-176">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-177">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-178">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-178">0</span></span>                                                |
| <span data-ttu-id="4b8ef-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-179">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-180">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-180">3</span></span>                                                |
| <span data-ttu-id="4b8ef-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-181">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-182">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-183">System-Flags</span></span>           | <span data-ttu-id="4b8ef-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-184">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-185">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-185">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-186">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4b8ef-187">ADAM</span><span class="sxs-lookup"><span data-stu-id="4b8ef-187">ADAM</span></span>



| <span data-ttu-id="4b8ef-188">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-188">Entry</span></span> | <span data-ttu-id="4b8ef-189">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-190">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-191">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-192">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-193">System-Only</span></span>            | <span data-ttu-id="4b8ef-194">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-194">True</span></span>                                             |
| <span data-ttu-id="4b8ef-195">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-195">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-196">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-196">True</span></span>                                             |
| <span data-ttu-id="4b8ef-197">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-197">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-198">False</span></span>                                            |
| <span data-ttu-id="4b8ef-199">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-199">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-200">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-200">False</span></span>                                            |
| <span data-ttu-id="4b8ef-201">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-202">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-203">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-204">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-204">0</span></span>                                                |
| <span data-ttu-id="4b8ef-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-205">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-206">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-206">3</span></span>                                                |
| <span data-ttu-id="4b8ef-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-207">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-208">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-209">System-Flags</span></span>           | <span data-ttu-id="4b8ef-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-210">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-211">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-211">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-212">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b8ef-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b8ef-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b8ef-214">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-214">Entry</span></span> | <span data-ttu-id="4b8ef-215">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-216">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-217">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-218">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-219">System-Only</span></span>            | <span data-ttu-id="4b8ef-220">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-220">True</span></span>                                             |
| <span data-ttu-id="4b8ef-221">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-221">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-222">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-222">True</span></span>                                             |
| <span data-ttu-id="4b8ef-223">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-223">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-224">False</span></span>                                            |
| <span data-ttu-id="4b8ef-225">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-225">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-226">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-226">False</span></span>                                            |
| <span data-ttu-id="4b8ef-227">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-228">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-229">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-230">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-230">0</span></span>                                                |
| <span data-ttu-id="4b8ef-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-231">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-232">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-232">3</span></span>                                                |
| <span data-ttu-id="4b8ef-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-233">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-234">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-235">System-Flags</span></span>           | <span data-ttu-id="4b8ef-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-236">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-237">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-237">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-238">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b8ef-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b8ef-239">Windows Server 2008</span></span>



| <span data-ttu-id="4b8ef-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-240">Entry</span></span> | <span data-ttu-id="4b8ef-241">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-243">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-244">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-245">System-Only</span></span>            | <span data-ttu-id="4b8ef-246">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-246">True</span></span>                                             |
| <span data-ttu-id="4b8ef-247">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-247">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-248">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-248">True</span></span>                                             |
| <span data-ttu-id="4b8ef-249">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-249">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-250">False</span></span>                                            |
| <span data-ttu-id="4b8ef-251">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-251">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-252">False</span></span>                                            |
| <span data-ttu-id="4b8ef-253">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-254">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-255">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-256">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-256">0</span></span>                                                |
| <span data-ttu-id="4b8ef-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-257">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-258">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-258">3</span></span>                                                |
| <span data-ttu-id="4b8ef-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-259">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-260">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-261">System-Flags</span></span>           | <span data-ttu-id="4b8ef-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-262">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-263">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-264">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b8ef-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b8ef-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b8ef-266">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-266">Entry</span></span> | <span data-ttu-id="4b8ef-267">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-268">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-269">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-270">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-271">System-Only</span></span>            | <span data-ttu-id="4b8ef-272">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-272">True</span></span>                                             |
| <span data-ttu-id="4b8ef-273">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-273">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-274">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-274">True</span></span>                                             |
| <span data-ttu-id="4b8ef-275">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-275">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-276">False</span></span>                                            |
| <span data-ttu-id="4b8ef-277">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-277">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-278">False</span></span>                                            |
| <span data-ttu-id="4b8ef-279">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-280">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-281">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-282">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-282">0</span></span>                                                |
| <span data-ttu-id="4b8ef-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-283">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-284">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-284">3</span></span>                                                |
| <span data-ttu-id="4b8ef-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-285">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-286">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-287">System-Flags</span></span>           | <span data-ttu-id="4b8ef-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-288">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-289">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-290">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b8ef-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b8ef-291">Windows Server 2012</span></span>



| <span data-ttu-id="4b8ef-292">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8ef-292">Entry</span></span> | <span data-ttu-id="4b8ef-293">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8ef-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4b8ef-294">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ef-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4b8ef-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8ef-295">MAPI-Id</span></span>                | <span data-ttu-id="4b8ef-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="4b8ef-296">0x80F6</span></span>                                           |
| <span data-ttu-id="4b8ef-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8ef-297">System-Only</span></span>            | <span data-ttu-id="4b8ef-298">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-298">True</span></span>                                             |
| <span data-ttu-id="4b8ef-299">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8ef-299">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8ef-300">True</span><span class="sxs-lookup"><span data-stu-id="4b8ef-300">True</span></span>                                             |
| <span data-ttu-id="4b8ef-301">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8ef-301">Is Indexed</span></span>             | <span data-ttu-id="4b8ef-302">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-302">False</span></span>                                            |
| <span data-ttu-id="4b8ef-303">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8ef-303">In Global Catalog</span></span>      | <span data-ttu-id="4b8ef-304">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8ef-304">False</span></span>                                            |
| <span data-ttu-id="4b8ef-305">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8ef-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8ef-306">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8ef-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4b8ef-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8ef-307">Range-Lower</span></span>            | <span data-ttu-id="4b8ef-308">0</span><span class="sxs-lookup"><span data-stu-id="4b8ef-308">0</span></span>                                                |
| <span data-ttu-id="4b8ef-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8ef-309">Range-Upper</span></span>            | <span data-ttu-id="4b8ef-310">3</span><span class="sxs-lookup"><span data-stu-id="4b8ef-310">3</span></span>                                                |
| <span data-ttu-id="4b8ef-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-311">Search-Flags</span></span>           | <span data-ttu-id="4b8ef-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8ef-312">0x00000000</span></span>                                       |
| <span data-ttu-id="4b8ef-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8ef-313">System-Flags</span></span>           | <span data-ttu-id="4b8ef-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8ef-314">0x00000010</span></span>                                       |
| <span data-ttu-id="4b8ef-315">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8ef-315">Classes used in</span></span>        | [<span data-ttu-id="4b8ef-316">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="4b8ef-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





