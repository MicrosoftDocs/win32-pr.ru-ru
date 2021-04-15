---
title: Атрибут Attribute-Types
description: Многозначное свойство, содержащее строки, представляющие каждый атрибут в схеме.
ms.assetid: 37d48944-b573-4067-982c-2e57db040b54
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Attribute-Types
- Схема AD атрибута Аттрибутетипес
topic_type:
- apiref
api_name:
- Attribute-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99f587f1704f7e2ea393279a8dbf0a20be10ef02
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655541"
---
# <a name="attribute-types-attribute"></a><span data-ttu-id="90f55-105">Атрибут Attribute-Types</span><span class="sxs-lookup"><span data-stu-id="90f55-105">Attribute-Types attribute</span></span>

<span data-ttu-id="90f55-106">Многозначное свойство, содержащее строки, представляющие каждый атрибут в схеме.</span><span class="sxs-lookup"><span data-stu-id="90f55-106">A multi-valued property that contains strings that represent each attribute in the schema.</span></span>



| <span data-ttu-id="90f55-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-107">Entry</span></span> | <span data-ttu-id="90f55-108">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="90f55-109">CN</span><span class="sxs-lookup"><span data-stu-id="90f55-109">CN</span></span>                | <span data-ttu-id="90f55-110">Attribute-Types</span><span class="sxs-lookup"><span data-stu-id="90f55-110">Attribute-Types</span></span>                             |
| <span data-ttu-id="90f55-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="90f55-111">Ldap-Display-Name</span></span> | <span data-ttu-id="90f55-112">аттрибутетипес</span><span class="sxs-lookup"><span data-stu-id="90f55-112">attributeTypes</span></span>                              |
| <span data-ttu-id="90f55-113">Размер</span><span class="sxs-lookup"><span data-stu-id="90f55-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="90f55-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="90f55-114">Update Privilege</span></span>  | <span data-ttu-id="90f55-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="90f55-115">Schema administrator</span></span>                        |
| <span data-ttu-id="90f55-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="90f55-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="90f55-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-117">Attribute-Id</span></span>      | <span data-ttu-id="90f55-118">2.5.21.5</span><span class="sxs-lookup"><span data-stu-id="90f55-118">2.5.21.5</span></span>                                    |
| <span data-ttu-id="90f55-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="90f55-119">System-Id-Guid</span></span>    | <span data-ttu-id="90f55-120">9a7ad944-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="90f55-120">9a7ad944-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="90f55-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90f55-121">Syntax</span></span>            | [<span data-ttu-id="90f55-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="90f55-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="90f55-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="90f55-123">Implementations</span></span>

-   [<span data-ttu-id="90f55-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90f55-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90f55-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90f55-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90f55-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="90f55-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="90f55-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90f55-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90f55-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90f55-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90f55-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90f55-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90f55-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90f55-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90f55-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90f55-131">Windows 2000 Server</span></span>



| <span data-ttu-id="90f55-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-132">Entry</span></span> | <span data-ttu-id="90f55-133">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-133">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-134">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-135">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-136">System-Only</span></span>            | <span data-ttu-id="90f55-137">True</span><span class="sxs-lookup"><span data-stu-id="90f55-137">True</span></span>                                        |
| <span data-ttu-id="90f55-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-138">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-139">False</span></span>                                       |
| <span data-ttu-id="90f55-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-140">Is Indexed</span></span>             | <span data-ttu-id="90f55-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-141">False</span></span>                                       |
| <span data-ttu-id="90f55-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-142">In Global Catalog</span></span>      | <span data-ttu-id="90f55-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-143">False</span></span>                                       |
| <span data-ttu-id="90f55-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-145">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-146">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-147">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-148">Search-Flags</span></span>           | <span data-ttu-id="90f55-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-149">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-150">System-Flags</span></span>           | <span data-ttu-id="90f55-151">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-151">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-152">Classes used in</span></span>        | [<span data-ttu-id="90f55-153">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-153">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90f55-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90f55-154">Windows Server 2003</span></span>



| <span data-ttu-id="90f55-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-155">Entry</span></span> | <span data-ttu-id="90f55-156">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-156">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-157">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-158">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-159">System-Only</span></span>            | <span data-ttu-id="90f55-160">True</span><span class="sxs-lookup"><span data-stu-id="90f55-160">True</span></span>                                        |
| <span data-ttu-id="90f55-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-161">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-162">False</span></span>                                       |
| <span data-ttu-id="90f55-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-163">Is Indexed</span></span>             | <span data-ttu-id="90f55-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-164">False</span></span>                                       |
| <span data-ttu-id="90f55-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-165">In Global Catalog</span></span>      | <span data-ttu-id="90f55-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-166">False</span></span>                                       |
| <span data-ttu-id="90f55-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-168">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-169">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-170">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-171">Search-Flags</span></span>           | <span data-ttu-id="90f55-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-172">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-173">System-Flags</span></span>           | <span data-ttu-id="90f55-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-174">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-175">Classes used in</span></span>        | [<span data-ttu-id="90f55-176">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-176">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="90f55-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="90f55-177">ADAM</span></span>



| <span data-ttu-id="90f55-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-178">Entry</span></span> | <span data-ttu-id="90f55-179">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-179">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-180">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-181">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-182">System-Only</span></span>            | <span data-ttu-id="90f55-183">True</span><span class="sxs-lookup"><span data-stu-id="90f55-183">True</span></span>                                        |
| <span data-ttu-id="90f55-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-184">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-185">False</span></span>                                       |
| <span data-ttu-id="90f55-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-186">Is Indexed</span></span>             | <span data-ttu-id="90f55-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-187">False</span></span>                                       |
| <span data-ttu-id="90f55-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-188">In Global Catalog</span></span>      | <span data-ttu-id="90f55-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-189">False</span></span>                                       |
| <span data-ttu-id="90f55-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-191">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-192">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-193">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-194">Search-Flags</span></span>           | <span data-ttu-id="90f55-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-195">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-196">System-Flags</span></span>           | <span data-ttu-id="90f55-197">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-197">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-198">Classes used in</span></span>        | [<span data-ttu-id="90f55-199">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-199">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90f55-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90f55-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90f55-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-201">Entry</span></span> | <span data-ttu-id="90f55-202">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-202">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-203">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-204">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-205">System-Only</span></span>            | <span data-ttu-id="90f55-206">True</span><span class="sxs-lookup"><span data-stu-id="90f55-206">True</span></span>                                        |
| <span data-ttu-id="90f55-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-207">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-208">False</span></span>                                       |
| <span data-ttu-id="90f55-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-209">Is Indexed</span></span>             | <span data-ttu-id="90f55-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-210">False</span></span>                                       |
| <span data-ttu-id="90f55-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-211">In Global Catalog</span></span>      | <span data-ttu-id="90f55-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-212">False</span></span>                                       |
| <span data-ttu-id="90f55-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-214">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-215">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-216">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-217">Search-Flags</span></span>           | <span data-ttu-id="90f55-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-218">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-219">System-Flags</span></span>           | <span data-ttu-id="90f55-220">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-220">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-221">Classes used in</span></span>        | [<span data-ttu-id="90f55-222">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-222">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90f55-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90f55-223">Windows Server 2008</span></span>



| <span data-ttu-id="90f55-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-224">Entry</span></span> | <span data-ttu-id="90f55-225">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-225">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-226">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-227">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-228">System-Only</span></span>            | <span data-ttu-id="90f55-229">True</span><span class="sxs-lookup"><span data-stu-id="90f55-229">True</span></span>                                        |
| <span data-ttu-id="90f55-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-230">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-231">False</span></span>                                       |
| <span data-ttu-id="90f55-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-232">Is Indexed</span></span>             | <span data-ttu-id="90f55-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-233">False</span></span>                                       |
| <span data-ttu-id="90f55-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-234">In Global Catalog</span></span>      | <span data-ttu-id="90f55-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-235">False</span></span>                                       |
| <span data-ttu-id="90f55-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-237">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-238">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-239">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-240">Search-Flags</span></span>           | <span data-ttu-id="90f55-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-241">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-242">System-Flags</span></span>           | <span data-ttu-id="90f55-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-243">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-244">Classes used in</span></span>        | [<span data-ttu-id="90f55-245">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-245">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90f55-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90f55-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90f55-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-247">Entry</span></span> | <span data-ttu-id="90f55-248">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-248">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-249">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-250">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-251">System-Only</span></span>            | <span data-ttu-id="90f55-252">True</span><span class="sxs-lookup"><span data-stu-id="90f55-252">True</span></span>                                        |
| <span data-ttu-id="90f55-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-253">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-254">False</span></span>                                       |
| <span data-ttu-id="90f55-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-255">Is Indexed</span></span>             | <span data-ttu-id="90f55-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-256">False</span></span>                                       |
| <span data-ttu-id="90f55-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-257">In Global Catalog</span></span>      | <span data-ttu-id="90f55-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-258">False</span></span>                                       |
| <span data-ttu-id="90f55-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-260">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-261">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-262">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-263">Search-Flags</span></span>           | <span data-ttu-id="90f55-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-264">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-265">System-Flags</span></span>           | <span data-ttu-id="90f55-266">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-266">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-267">Classes used in</span></span>        | [<span data-ttu-id="90f55-268">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-268">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90f55-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90f55-269">Windows Server 2012</span></span>



| <span data-ttu-id="90f55-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="90f55-270">Entry</span></span> | <span data-ttu-id="90f55-271">Значение</span><span class="sxs-lookup"><span data-stu-id="90f55-271">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="90f55-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90f55-272">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90f55-273">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="90f55-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="90f55-274">System-Only</span></span>            | <span data-ttu-id="90f55-275">True</span><span class="sxs-lookup"><span data-stu-id="90f55-275">True</span></span>                                        |
| <span data-ttu-id="90f55-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90f55-276">Is-Single-Valued</span></span>       | <span data-ttu-id="90f55-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-277">False</span></span>                                       |
| <span data-ttu-id="90f55-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90f55-278">Is Indexed</span></span>             | <span data-ttu-id="90f55-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-279">False</span></span>                                       |
| <span data-ttu-id="90f55-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90f55-280">In Global Catalog</span></span>      | <span data-ttu-id="90f55-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="90f55-281">False</span></span>                                       |
| <span data-ttu-id="90f55-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90f55-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="90f55-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90f55-283">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="90f55-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90f55-284">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="90f55-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90f55-285">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="90f55-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-286">Search-Flags</span></span>           | <span data-ttu-id="90f55-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90f55-287">0x00000000</span></span>                                  |
| <span data-ttu-id="90f55-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90f55-288">System-Flags</span></span>           | <span data-ttu-id="90f55-289">0x08000014</span><span class="sxs-lookup"><span data-stu-id="90f55-289">0x08000014</span></span>                                  |
| <span data-ttu-id="90f55-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90f55-290">Classes used in</span></span>        | [<span data-ttu-id="90f55-291">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="90f55-291">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





