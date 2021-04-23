---
title: Атрибут Object-Classes
description: Многозначное свойство, содержащее строки, представляющие каждый класс в схеме. Каждое значение содержит governsID, lDAPDisplayName, mustContain, mayContain и т. д.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Classes
- Схема AD атрибута Обжектклассес
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893730"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="14141-106">Атрибут Object-Classes</span><span class="sxs-lookup"><span data-stu-id="14141-106">Object-Classes attribute</span></span>

<span data-ttu-id="14141-107">Многозначное свойство, содержащее строки, представляющие каждый класс в схеме.</span><span class="sxs-lookup"><span data-stu-id="14141-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="14141-108">Каждое значение содержит governsID, lDAPDisplayName, mustContain, mayContain и т. д.</span><span class="sxs-lookup"><span data-stu-id="14141-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="14141-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-109">Entry</span></span> | <span data-ttu-id="14141-110">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="14141-111">CN</span><span class="sxs-lookup"><span data-stu-id="14141-111">CN</span></span>                | <span data-ttu-id="14141-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="14141-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="14141-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="14141-113">Ldap-Display-Name</span></span> | <span data-ttu-id="14141-114">обжектклассес</span><span class="sxs-lookup"><span data-stu-id="14141-114">objectClasses</span></span>                                    |
| <span data-ttu-id="14141-115">Размер</span><span class="sxs-lookup"><span data-stu-id="14141-115">Size</span></span>              | <span data-ttu-id="14141-116">Примерно 20 байт в среднем на имя класса.</span><span class="sxs-lookup"><span data-stu-id="14141-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="14141-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="14141-117">Update Privilege</span></span>  | <span data-ttu-id="14141-118">Это значение задается конструктором объекта.</span><span class="sxs-lookup"><span data-stu-id="14141-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="14141-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="14141-119">Update Frequency</span></span>  | <span data-ttu-id="14141-120">При изменении структуры класса.</span><span class="sxs-lookup"><span data-stu-id="14141-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="14141-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14141-121">Attribute-Id</span></span>      | <span data-ttu-id="14141-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="14141-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="14141-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="14141-123">System-Id-Guid</span></span>    | <span data-ttu-id="14141-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="14141-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="14141-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14141-125">Syntax</span></span>            | [<span data-ttu-id="14141-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="14141-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="14141-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="14141-127">Implementations</span></span>

-   [<span data-ttu-id="14141-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14141-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14141-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14141-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14141-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="14141-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="14141-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14141-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14141-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14141-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14141-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14141-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14141-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14141-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14141-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14141-135">Windows 2000 Server</span></span>



| <span data-ttu-id="14141-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-136">Entry</span></span> | <span data-ttu-id="14141-137">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-140">System-Only</span></span>            | <span data-ttu-id="14141-141">True</span><span class="sxs-lookup"><span data-stu-id="14141-141">True</span></span>                                        |
| <span data-ttu-id="14141-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-142">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-143">False</span></span>                                       |
| <span data-ttu-id="14141-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-144">Is Indexed</span></span>             | <span data-ttu-id="14141-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-145">False</span></span>                                       |
| <span data-ttu-id="14141-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-146">In Global Catalog</span></span>      | <span data-ttu-id="14141-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-147">False</span></span>                                       |
| <span data-ttu-id="14141-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-152">Search-Flags</span></span>           | <span data-ttu-id="14141-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-153">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-154">System-Flags</span></span>           | <span data-ttu-id="14141-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-155">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-156">Classes used in</span></span>        | [<span data-ttu-id="14141-157">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14141-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14141-158">Windows Server 2003</span></span>



| <span data-ttu-id="14141-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-159">Entry</span></span> | <span data-ttu-id="14141-160">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-163">System-Only</span></span>            | <span data-ttu-id="14141-164">True</span><span class="sxs-lookup"><span data-stu-id="14141-164">True</span></span>                                        |
| <span data-ttu-id="14141-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-165">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-166">False</span></span>                                       |
| <span data-ttu-id="14141-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-167">Is Indexed</span></span>             | <span data-ttu-id="14141-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-168">False</span></span>                                       |
| <span data-ttu-id="14141-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-169">In Global Catalog</span></span>      | <span data-ttu-id="14141-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-170">False</span></span>                                       |
| <span data-ttu-id="14141-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-175">Search-Flags</span></span>           | <span data-ttu-id="14141-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-176">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-177">System-Flags</span></span>           | <span data-ttu-id="14141-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-178">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-179">Classes used in</span></span>        | [<span data-ttu-id="14141-180">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="14141-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="14141-181">ADAM</span></span>



| <span data-ttu-id="14141-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-182">Entry</span></span> | <span data-ttu-id="14141-183">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-186">System-Only</span></span>            | <span data-ttu-id="14141-187">True</span><span class="sxs-lookup"><span data-stu-id="14141-187">True</span></span>                                        |
| <span data-ttu-id="14141-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-188">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-189">False</span></span>                                       |
| <span data-ttu-id="14141-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-190">Is Indexed</span></span>             | <span data-ttu-id="14141-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-191">False</span></span>                                       |
| <span data-ttu-id="14141-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-192">In Global Catalog</span></span>      | <span data-ttu-id="14141-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-193">False</span></span>                                       |
| <span data-ttu-id="14141-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-198">Search-Flags</span></span>           | <span data-ttu-id="14141-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-199">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-200">System-Flags</span></span>           | <span data-ttu-id="14141-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-201">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-202">Classes used in</span></span>        | [<span data-ttu-id="14141-203">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14141-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14141-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14141-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-205">Entry</span></span> | <span data-ttu-id="14141-206">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-209">System-Only</span></span>            | <span data-ttu-id="14141-210">True</span><span class="sxs-lookup"><span data-stu-id="14141-210">True</span></span>                                        |
| <span data-ttu-id="14141-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-211">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-212">False</span></span>                                       |
| <span data-ttu-id="14141-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-213">Is Indexed</span></span>             | <span data-ttu-id="14141-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-214">False</span></span>                                       |
| <span data-ttu-id="14141-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-215">In Global Catalog</span></span>      | <span data-ttu-id="14141-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-216">False</span></span>                                       |
| <span data-ttu-id="14141-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-221">Search-Flags</span></span>           | <span data-ttu-id="14141-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-222">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-223">System-Flags</span></span>           | <span data-ttu-id="14141-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-224">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-225">Classes used in</span></span>        | [<span data-ttu-id="14141-226">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14141-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14141-227">Windows Server 2008</span></span>



| <span data-ttu-id="14141-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-228">Entry</span></span> | <span data-ttu-id="14141-229">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-232">System-Only</span></span>            | <span data-ttu-id="14141-233">True</span><span class="sxs-lookup"><span data-stu-id="14141-233">True</span></span>                                        |
| <span data-ttu-id="14141-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-234">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-235">False</span></span>                                       |
| <span data-ttu-id="14141-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-236">Is Indexed</span></span>             | <span data-ttu-id="14141-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-237">False</span></span>                                       |
| <span data-ttu-id="14141-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-238">In Global Catalog</span></span>      | <span data-ttu-id="14141-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-239">False</span></span>                                       |
| <span data-ttu-id="14141-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-244">Search-Flags</span></span>           | <span data-ttu-id="14141-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-245">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-246">System-Flags</span></span>           | <span data-ttu-id="14141-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-247">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-248">Classes used in</span></span>        | [<span data-ttu-id="14141-249">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14141-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14141-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14141-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-251">Entry</span></span> | <span data-ttu-id="14141-252">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-255">System-Only</span></span>            | <span data-ttu-id="14141-256">True</span><span class="sxs-lookup"><span data-stu-id="14141-256">True</span></span>                                        |
| <span data-ttu-id="14141-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-257">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-258">False</span></span>                                       |
| <span data-ttu-id="14141-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-259">Is Indexed</span></span>             | <span data-ttu-id="14141-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-260">False</span></span>                                       |
| <span data-ttu-id="14141-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-261">In Global Catalog</span></span>      | <span data-ttu-id="14141-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-262">False</span></span>                                       |
| <span data-ttu-id="14141-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-267">Search-Flags</span></span>           | <span data-ttu-id="14141-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-268">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-269">System-Flags</span></span>           | <span data-ttu-id="14141-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-270">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-271">Classes used in</span></span>        | [<span data-ttu-id="14141-272">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14141-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14141-273">Windows Server 2012</span></span>



| <span data-ttu-id="14141-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="14141-274">Entry</span></span> | <span data-ttu-id="14141-275">Значение</span><span class="sxs-lookup"><span data-stu-id="14141-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14141-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14141-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14141-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="14141-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="14141-278">System-Only</span></span>            | <span data-ttu-id="14141-279">True</span><span class="sxs-lookup"><span data-stu-id="14141-279">True</span></span>                                        |
| <span data-ttu-id="14141-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14141-280">Is-Single-Valued</span></span>       | <span data-ttu-id="14141-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-281">False</span></span>                                       |
| <span data-ttu-id="14141-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14141-282">Is Indexed</span></span>             | <span data-ttu-id="14141-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-283">False</span></span>                                       |
| <span data-ttu-id="14141-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14141-284">In Global Catalog</span></span>      | <span data-ttu-id="14141-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="14141-285">False</span></span>                                       |
| <span data-ttu-id="14141-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14141-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="14141-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14141-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="14141-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14141-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="14141-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14141-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="14141-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-290">Search-Flags</span></span>           | <span data-ttu-id="14141-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14141-291">0x00000000</span></span>                                  |
| <span data-ttu-id="14141-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14141-292">System-Flags</span></span>           | <span data-ttu-id="14141-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="14141-293">0x08000014</span></span>                                  |
| <span data-ttu-id="14141-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14141-294">Classes used in</span></span>        | [<span data-ttu-id="14141-295">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="14141-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





