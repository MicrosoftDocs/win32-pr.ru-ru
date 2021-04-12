---
title: Атрибут расширенного класса info
description: Многозначное свойство, содержащее строки, представляющие дополнительные сведения для каждого класса. Каждое значение содержит governsID, lDAPDisplayName и schemaIDGUID класса.
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута расширенного класса info
- Схема AD атрибута Екстендедклассинфо
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416225"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="6d758-106">Атрибут расширенного класса info</span><span class="sxs-lookup"><span data-stu-id="6d758-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="6d758-107">Многозначное свойство, содержащее строки, представляющие дополнительные сведения для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="6d758-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="6d758-108">Каждое значение содержит governsID, lDAPDisplayName и schemaIDGUID класса.</span><span class="sxs-lookup"><span data-stu-id="6d758-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="6d758-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-109">Entry</span></span> | <span data-ttu-id="6d758-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6d758-111">CN</span><span class="sxs-lookup"><span data-stu-id="6d758-111">CN</span></span>                | <span data-ttu-id="6d758-112">Расширенные сведения о классе</span><span class="sxs-lookup"><span data-stu-id="6d758-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="6d758-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6d758-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6d758-114">екстендедклассинфо</span><span class="sxs-lookup"><span data-stu-id="6d758-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="6d758-115">Размер</span><span class="sxs-lookup"><span data-stu-id="6d758-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6d758-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6d758-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6d758-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6d758-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6d758-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-118">Attribute-Id</span></span>      | <span data-ttu-id="6d758-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="6d758-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="6d758-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6d758-120">System-Id-Guid</span></span>    | <span data-ttu-id="6d758-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6d758-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="6d758-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d758-122">Syntax</span></span>            | [<span data-ttu-id="6d758-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6d758-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6d758-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6d758-124">Implementations</span></span>

-   [<span data-ttu-id="6d758-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d758-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d758-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d758-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d758-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6d758-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6d758-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d758-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d758-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d758-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d758-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d758-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d758-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d758-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d758-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d758-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6d758-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-133">Entry</span></span> | <span data-ttu-id="6d758-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-137">System-Only</span></span>            | <span data-ttu-id="6d758-138">True</span><span class="sxs-lookup"><span data-stu-id="6d758-138">True</span></span>                                        |
| <span data-ttu-id="6d758-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-140">False</span></span>                                       |
| <span data-ttu-id="6d758-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-141">Is Indexed</span></span>             | <span data-ttu-id="6d758-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-142">False</span></span>                                       |
| <span data-ttu-id="6d758-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-143">In Global Catalog</span></span>      | <span data-ttu-id="6d758-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-144">False</span></span>                                       |
| <span data-ttu-id="6d758-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-149">Search-Flags</span></span>           | <span data-ttu-id="6d758-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-150">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-151">System-Flags</span></span>           | <span data-ttu-id="6d758-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-152">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-153">Classes used in</span></span>        | [<span data-ttu-id="6d758-154">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d758-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d758-155">Windows Server 2003</span></span>



| <span data-ttu-id="6d758-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-156">Entry</span></span> | <span data-ttu-id="6d758-157">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-160">System-Only</span></span>            | <span data-ttu-id="6d758-161">True</span><span class="sxs-lookup"><span data-stu-id="6d758-161">True</span></span>                                        |
| <span data-ttu-id="6d758-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-163">False</span></span>                                       |
| <span data-ttu-id="6d758-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-164">Is Indexed</span></span>             | <span data-ttu-id="6d758-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-165">False</span></span>                                       |
| <span data-ttu-id="6d758-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-166">In Global Catalog</span></span>      | <span data-ttu-id="6d758-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-167">False</span></span>                                       |
| <span data-ttu-id="6d758-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-172">Search-Flags</span></span>           | <span data-ttu-id="6d758-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-173">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-174">System-Flags</span></span>           | <span data-ttu-id="6d758-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-175">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-176">Classes used in</span></span>        | [<span data-ttu-id="6d758-177">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6d758-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="6d758-178">ADAM</span></span>



| <span data-ttu-id="6d758-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-179">Entry</span></span> | <span data-ttu-id="6d758-180">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-183">System-Only</span></span>            | <span data-ttu-id="6d758-184">True</span><span class="sxs-lookup"><span data-stu-id="6d758-184">True</span></span>                                        |
| <span data-ttu-id="6d758-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-186">False</span></span>                                       |
| <span data-ttu-id="6d758-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-187">Is Indexed</span></span>             | <span data-ttu-id="6d758-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-188">False</span></span>                                       |
| <span data-ttu-id="6d758-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-189">In Global Catalog</span></span>      | <span data-ttu-id="6d758-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-190">False</span></span>                                       |
| <span data-ttu-id="6d758-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-195">Search-Flags</span></span>           | <span data-ttu-id="6d758-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-196">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-197">System-Flags</span></span>           | <span data-ttu-id="6d758-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-198">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-199">Classes used in</span></span>        | [<span data-ttu-id="6d758-200">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d758-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d758-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d758-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-202">Entry</span></span> | <span data-ttu-id="6d758-203">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-206">System-Only</span></span>            | <span data-ttu-id="6d758-207">True</span><span class="sxs-lookup"><span data-stu-id="6d758-207">True</span></span>                                        |
| <span data-ttu-id="6d758-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-209">False</span></span>                                       |
| <span data-ttu-id="6d758-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-210">Is Indexed</span></span>             | <span data-ttu-id="6d758-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-211">False</span></span>                                       |
| <span data-ttu-id="6d758-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-212">In Global Catalog</span></span>      | <span data-ttu-id="6d758-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-213">False</span></span>                                       |
| <span data-ttu-id="6d758-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-218">Search-Flags</span></span>           | <span data-ttu-id="6d758-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-219">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-220">System-Flags</span></span>           | <span data-ttu-id="6d758-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-221">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-222">Classes used in</span></span>        | [<span data-ttu-id="6d758-223">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d758-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d758-224">Windows Server 2008</span></span>



| <span data-ttu-id="6d758-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-225">Entry</span></span> | <span data-ttu-id="6d758-226">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-229">System-Only</span></span>            | <span data-ttu-id="6d758-230">True</span><span class="sxs-lookup"><span data-stu-id="6d758-230">True</span></span>                                        |
| <span data-ttu-id="6d758-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-231">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-232">False</span></span>                                       |
| <span data-ttu-id="6d758-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-233">Is Indexed</span></span>             | <span data-ttu-id="6d758-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-234">False</span></span>                                       |
| <span data-ttu-id="6d758-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-235">In Global Catalog</span></span>      | <span data-ttu-id="6d758-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-236">False</span></span>                                       |
| <span data-ttu-id="6d758-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-241">Search-Flags</span></span>           | <span data-ttu-id="6d758-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-242">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-243">System-Flags</span></span>           | <span data-ttu-id="6d758-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-244">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-245">Classes used in</span></span>        | [<span data-ttu-id="6d758-246">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d758-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d758-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d758-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-248">Entry</span></span> | <span data-ttu-id="6d758-249">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-252">System-Only</span></span>            | <span data-ttu-id="6d758-253">True</span><span class="sxs-lookup"><span data-stu-id="6d758-253">True</span></span>                                        |
| <span data-ttu-id="6d758-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-254">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-255">False</span></span>                                       |
| <span data-ttu-id="6d758-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-256">Is Indexed</span></span>             | <span data-ttu-id="6d758-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-257">False</span></span>                                       |
| <span data-ttu-id="6d758-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-258">In Global Catalog</span></span>      | <span data-ttu-id="6d758-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-259">False</span></span>                                       |
| <span data-ttu-id="6d758-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-264">Search-Flags</span></span>           | <span data-ttu-id="6d758-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-265">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-266">System-Flags</span></span>           | <span data-ttu-id="6d758-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-267">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-268">Classes used in</span></span>        | [<span data-ttu-id="6d758-269">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d758-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d758-270">Windows Server 2012</span></span>



| <span data-ttu-id="6d758-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d758-271">Entry</span></span> | <span data-ttu-id="6d758-272">Значение</span><span class="sxs-lookup"><span data-stu-id="6d758-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6d758-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d758-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d758-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="6d758-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d758-275">System-Only</span></span>            | <span data-ttu-id="6d758-276">True</span><span class="sxs-lookup"><span data-stu-id="6d758-276">True</span></span>                                        |
| <span data-ttu-id="6d758-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d758-277">Is-Single-Valued</span></span>       | <span data-ttu-id="6d758-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-278">False</span></span>                                       |
| <span data-ttu-id="6d758-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d758-279">Is Indexed</span></span>             | <span data-ttu-id="6d758-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-280">False</span></span>                                       |
| <span data-ttu-id="6d758-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d758-281">In Global Catalog</span></span>      | <span data-ttu-id="6d758-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d758-282">False</span></span>                                       |
| <span data-ttu-id="6d758-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d758-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d758-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d758-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6d758-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d758-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6d758-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d758-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6d758-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-287">Search-Flags</span></span>           | <span data-ttu-id="6d758-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d758-288">0x00000000</span></span>                                  |
| <span data-ttu-id="6d758-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d758-289">System-Flags</span></span>           | <span data-ttu-id="6d758-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6d758-290">0x08000014</span></span>                                  |
| <span data-ttu-id="6d758-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d758-291">Classes used in</span></span>        | [<span data-ttu-id="6d758-292">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="6d758-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





