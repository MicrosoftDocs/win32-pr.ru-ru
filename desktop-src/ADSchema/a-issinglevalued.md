---
title: Атрибут имеет значение с одним значением
description: Если значение — TRUE, этот атрибут может хранить только одно значение.
ms.assetid: 53dd8dfe-2123-4a61-a346-12abe340ea11
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута с одним значением
- Схема AD атрибута Иссинглевалуед
topic_type:
- apiref
api_name:
- Is-Single-Valued
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a1fafd047afa47b874fb0385a690e2c0d13161
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893093"
---
# <a name="is-single-valued-attribute"></a><span data-ttu-id="af083-105">Атрибут имеет значение с одним значением</span><span class="sxs-lookup"><span data-stu-id="af083-105">Is-Single-Valued attribute</span></span>

<span data-ttu-id="af083-106">Если **значение — true**, этот атрибут может хранить только одно значение.</span><span class="sxs-lookup"><span data-stu-id="af083-106">If **TRUE**, this attribute can only store one value.</span></span>



| <span data-ttu-id="af083-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-107">Entry</span></span> | <span data-ttu-id="af083-108">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="af083-109">CN</span><span class="sxs-lookup"><span data-stu-id="af083-109">CN</span></span>                | <span data-ttu-id="af083-110">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-110">Is-Single-Valued</span></span>                     |
| <span data-ttu-id="af083-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="af083-111">Ldap-Display-Name</span></span> | <span data-ttu-id="af083-112">isSingleValued</span><span class="sxs-lookup"><span data-stu-id="af083-112">isSingleValued</span></span>                       |
| <span data-ttu-id="af083-113">Размер</span><span class="sxs-lookup"><span data-stu-id="af083-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="af083-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="af083-114">Update Privilege</span></span>  | <span data-ttu-id="af083-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="af083-115">Schema administrator</span></span>                 |
| <span data-ttu-id="af083-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="af083-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="af083-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af083-117">Attribute-Id</span></span>      | <span data-ttu-id="af083-118">1.2.840.113556.1.2.33</span><span class="sxs-lookup"><span data-stu-id="af083-118">1.2.840.113556.1.2.33</span></span>                |
| <span data-ttu-id="af083-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="af083-119">System-Id-Guid</span></span>    | <span data-ttu-id="af083-120">bf967992-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="af083-120">bf967992-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="af083-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af083-121">Syntax</span></span>            | [<span data-ttu-id="af083-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="af083-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="af083-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="af083-123">Implementations</span></span>

-   [<span data-ttu-id="af083-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af083-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af083-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af083-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af083-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="af083-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="af083-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af083-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af083-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af083-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af083-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af083-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af083-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af083-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af083-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af083-131">Windows 2000 Server</span></span>



| <span data-ttu-id="af083-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-132">Entry</span></span> | <span data-ttu-id="af083-133">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-135">MAPI-Id</span></span>                | <span data-ttu-id="af083-136">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-136">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-137">System-Only</span></span>            | <span data-ttu-id="af083-138">True</span><span class="sxs-lookup"><span data-stu-id="af083-138">True</span></span>                                                     |
| <span data-ttu-id="af083-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-139">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-140">True</span><span class="sxs-lookup"><span data-stu-id="af083-140">True</span></span>                                                     |
| <span data-ttu-id="af083-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-141">Is Indexed</span></span>             | <span data-ttu-id="af083-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-142">False</span></span>                                                    |
| <span data-ttu-id="af083-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-143">In Global Catalog</span></span>      | <span data-ttu-id="af083-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-144">False</span></span>                                                    |
| <span data-ttu-id="af083-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-146">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-147">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-148">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-149">Search-Flags</span></span>           | <span data-ttu-id="af083-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-150">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-151">System-Flags</span></span>           | <span data-ttu-id="af083-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-152">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-153">Classes used in</span></span>        | [<span data-ttu-id="af083-154">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-154">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af083-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af083-155">Windows Server 2003</span></span>



| <span data-ttu-id="af083-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-156">Entry</span></span> | <span data-ttu-id="af083-157">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-159">MAPI-Id</span></span>                | <span data-ttu-id="af083-160">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-160">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-161">System-Only</span></span>            | <span data-ttu-id="af083-162">True</span><span class="sxs-lookup"><span data-stu-id="af083-162">True</span></span>                                                     |
| <span data-ttu-id="af083-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-163">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-164">True</span><span class="sxs-lookup"><span data-stu-id="af083-164">True</span></span>                                                     |
| <span data-ttu-id="af083-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-165">Is Indexed</span></span>             | <span data-ttu-id="af083-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-166">False</span></span>                                                    |
| <span data-ttu-id="af083-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-167">In Global Catalog</span></span>      | <span data-ttu-id="af083-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-168">False</span></span>                                                    |
| <span data-ttu-id="af083-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-171">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-172">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-173">Search-Flags</span></span>           | <span data-ttu-id="af083-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-174">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-175">System-Flags</span></span>           | <span data-ttu-id="af083-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-176">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-177">Classes used in</span></span>        | [<span data-ttu-id="af083-178">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="af083-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="af083-179">ADAM</span></span>



| <span data-ttu-id="af083-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-180">Entry</span></span> | <span data-ttu-id="af083-181">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-183">MAPI-Id</span></span>                | <span data-ttu-id="af083-184">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-184">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-185">System-Only</span></span>            | <span data-ttu-id="af083-186">True</span><span class="sxs-lookup"><span data-stu-id="af083-186">True</span></span>                                                     |
| <span data-ttu-id="af083-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-187">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-188">True</span><span class="sxs-lookup"><span data-stu-id="af083-188">True</span></span>                                                     |
| <span data-ttu-id="af083-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-189">Is Indexed</span></span>             | <span data-ttu-id="af083-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-190">False</span></span>                                                    |
| <span data-ttu-id="af083-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-191">In Global Catalog</span></span>      | <span data-ttu-id="af083-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-192">False</span></span>                                                    |
| <span data-ttu-id="af083-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-194">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-195">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-196">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-197">Search-Flags</span></span>           | <span data-ttu-id="af083-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-198">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-199">System-Flags</span></span>           | <span data-ttu-id="af083-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-200">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-201">Classes used in</span></span>        | [<span data-ttu-id="af083-202">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-202">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af083-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af083-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af083-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-204">Entry</span></span> | <span data-ttu-id="af083-205">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-205">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-206">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-207">MAPI-Id</span></span>                | <span data-ttu-id="af083-208">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-208">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-209">System-Only</span></span>            | <span data-ttu-id="af083-210">True</span><span class="sxs-lookup"><span data-stu-id="af083-210">True</span></span>                                                     |
| <span data-ttu-id="af083-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-211">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-212">True</span><span class="sxs-lookup"><span data-stu-id="af083-212">True</span></span>                                                     |
| <span data-ttu-id="af083-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-213">Is Indexed</span></span>             | <span data-ttu-id="af083-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-214">False</span></span>                                                    |
| <span data-ttu-id="af083-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-215">In Global Catalog</span></span>      | <span data-ttu-id="af083-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-216">False</span></span>                                                    |
| <span data-ttu-id="af083-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-219">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-220">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-221">Search-Flags</span></span>           | <span data-ttu-id="af083-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-222">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-223">System-Flags</span></span>           | <span data-ttu-id="af083-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-224">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-225">Classes used in</span></span>        | [<span data-ttu-id="af083-226">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-226">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af083-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af083-227">Windows Server 2008</span></span>



| <span data-ttu-id="af083-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-228">Entry</span></span> | <span data-ttu-id="af083-229">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-229">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-230">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-231">MAPI-Id</span></span>                | <span data-ttu-id="af083-232">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-232">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-233">System-Only</span></span>            | <span data-ttu-id="af083-234">True</span><span class="sxs-lookup"><span data-stu-id="af083-234">True</span></span>                                                     |
| <span data-ttu-id="af083-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-235">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-236">True</span><span class="sxs-lookup"><span data-stu-id="af083-236">True</span></span>                                                     |
| <span data-ttu-id="af083-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-237">Is Indexed</span></span>             | <span data-ttu-id="af083-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-238">False</span></span>                                                    |
| <span data-ttu-id="af083-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-239">In Global Catalog</span></span>      | <span data-ttu-id="af083-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-240">False</span></span>                                                    |
| <span data-ttu-id="af083-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-242">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-243">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-244">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-245">Search-Flags</span></span>           | <span data-ttu-id="af083-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-246">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-247">System-Flags</span></span>           | <span data-ttu-id="af083-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-248">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-249">Classes used in</span></span>        | [<span data-ttu-id="af083-250">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-250">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af083-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af083-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af083-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-252">Entry</span></span> | <span data-ttu-id="af083-253">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-253">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-254">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-255">MAPI-Id</span></span>                | <span data-ttu-id="af083-256">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-256">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-257">System-Only</span></span>            | <span data-ttu-id="af083-258">True</span><span class="sxs-lookup"><span data-stu-id="af083-258">True</span></span>                                                     |
| <span data-ttu-id="af083-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-259">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-260">True</span><span class="sxs-lookup"><span data-stu-id="af083-260">True</span></span>                                                     |
| <span data-ttu-id="af083-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-261">Is Indexed</span></span>             | <span data-ttu-id="af083-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-262">False</span></span>                                                    |
| <span data-ttu-id="af083-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-263">In Global Catalog</span></span>      | <span data-ttu-id="af083-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-264">False</span></span>                                                    |
| <span data-ttu-id="af083-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-266">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-267">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-268">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-269">Search-Flags</span></span>           | <span data-ttu-id="af083-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-270">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-271">System-Flags</span></span>           | <span data-ttu-id="af083-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-272">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-273">Classes used in</span></span>        | [<span data-ttu-id="af083-274">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-274">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af083-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af083-275">Windows Server 2012</span></span>



| <span data-ttu-id="af083-276">Ввод</span><span class="sxs-lookup"><span data-stu-id="af083-276">Entry</span></span> | <span data-ttu-id="af083-277">Значение</span><span class="sxs-lookup"><span data-stu-id="af083-277">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="af083-278">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af083-278">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="af083-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af083-279">MAPI-Id</span></span>                | <span data-ttu-id="af083-280">0x80C1</span><span class="sxs-lookup"><span data-stu-id="af083-280">0x80C1</span></span>                                                   |
| <span data-ttu-id="af083-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="af083-281">System-Only</span></span>            | <span data-ttu-id="af083-282">True</span><span class="sxs-lookup"><span data-stu-id="af083-282">True</span></span>                                                     |
| <span data-ttu-id="af083-283">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af083-283">Is-Single-Valued</span></span>       | <span data-ttu-id="af083-284">True</span><span class="sxs-lookup"><span data-stu-id="af083-284">True</span></span>                                                     |
| <span data-ttu-id="af083-285">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af083-285">Is Indexed</span></span>             | <span data-ttu-id="af083-286">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-286">False</span></span>                                                    |
| <span data-ttu-id="af083-287">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af083-287">In Global Catalog</span></span>      | <span data-ttu-id="af083-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="af083-288">False</span></span>                                                    |
| <span data-ttu-id="af083-289">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af083-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="af083-290">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af083-290">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="af083-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af083-291">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="af083-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af083-292">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="af083-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-293">Search-Flags</span></span>           | <span data-ttu-id="af083-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af083-294">0x00000000</span></span>                                               |
| <span data-ttu-id="af083-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af083-295">System-Flags</span></span>           | <span data-ttu-id="af083-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af083-296">0x00000010</span></span>                                               |
| <span data-ttu-id="af083-297">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af083-297">Classes used in</span></span>        | [<span data-ttu-id="af083-298">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="af083-298">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





