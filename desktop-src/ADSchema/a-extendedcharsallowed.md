---
title: Расширенный атрибут-chars-Allowed
description: Указывает, разрешены ли расширенные символы в значении этого атрибута. Применяется только к атрибутам строковых атрибутов IA5, numeric, печатаемых и Teletex.
ms.assetid: aeacb5ef-9af2-498b-ae53-b3095de0d0c6
ms.tgt_platform: multiple
keywords:
- Расширенная кодировка — схема AD разрешенных атрибутов
- Схема AD атрибута Екстендедчарсалловед
topic_type:
- apiref
api_name:
- Extended-Chars-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e26194232387f27f3177f13edeab90efc97a4bb3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654855"
---
# <a name="extended-chars-allowed-attribute"></a><span data-ttu-id="48538-106">Расширенный атрибут-chars-Allowed</span><span class="sxs-lookup"><span data-stu-id="48538-106">Extended-Chars-Allowed attribute</span></span>

<span data-ttu-id="48538-107">Указывает, разрешены ли расширенные символы в значении этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="48538-107">Indicates whether extended characters are allowed in the value of this attribute.</span></span> <span data-ttu-id="48538-108">Применяется только к атрибутам строковых атрибутов IA5, numeric, печатаемых и Teletex.</span><span class="sxs-lookup"><span data-stu-id="48538-108">Only applies to IA5, Numeric, Printable, and Teletex string attributes.</span></span>



| <span data-ttu-id="48538-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-109">Entry</span></span> | <span data-ttu-id="48538-110">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="48538-111">CN</span><span class="sxs-lookup"><span data-stu-id="48538-111">CN</span></span>                | <span data-ttu-id="48538-112">Расширенные символы-разрешено</span><span class="sxs-lookup"><span data-stu-id="48538-112">Extended-Chars-Allowed</span></span>               |
| <span data-ttu-id="48538-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="48538-113">Ldap-Display-Name</span></span> | <span data-ttu-id="48538-114">екстендедчарсалловед</span><span class="sxs-lookup"><span data-stu-id="48538-114">extendedCharsAllowed</span></span>                 |
| <span data-ttu-id="48538-115">Размер</span><span class="sxs-lookup"><span data-stu-id="48538-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="48538-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="48538-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="48538-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="48538-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="48538-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48538-118">Attribute-Id</span></span>      | <span data-ttu-id="48538-119">1.2.840.113556.1.2.380</span><span class="sxs-lookup"><span data-stu-id="48538-119">1.2.840.113556.1.2.380</span></span>               |
| <span data-ttu-id="48538-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="48538-120">System-Id-Guid</span></span>    | <span data-ttu-id="48538-121">bf967966-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="48538-121">bf967966-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="48538-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48538-122">Syntax</span></span>            | [<span data-ttu-id="48538-123">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="48538-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="48538-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="48538-124">Implementations</span></span>

-   [<span data-ttu-id="48538-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48538-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48538-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48538-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48538-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="48538-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="48538-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48538-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48538-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48538-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48538-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48538-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48538-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48538-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48538-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48538-132">Windows 2000 Server</span></span>



| <span data-ttu-id="48538-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-133">Entry</span></span> | <span data-ttu-id="48538-134">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-136">MAPI-Id</span></span>                | <span data-ttu-id="48538-137">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-137">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-138">System-Only</span></span>            | <span data-ttu-id="48538-139">True</span><span class="sxs-lookup"><span data-stu-id="48538-139">True</span></span>                                                     |
| <span data-ttu-id="48538-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-140">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-141">True</span><span class="sxs-lookup"><span data-stu-id="48538-141">True</span></span>                                                     |
| <span data-ttu-id="48538-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-142">Is Indexed</span></span>             | <span data-ttu-id="48538-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-143">False</span></span>                                                    |
| <span data-ttu-id="48538-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-144">In Global Catalog</span></span>      | <span data-ttu-id="48538-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-145">False</span></span>                                                    |
| <span data-ttu-id="48538-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-150">Search-Flags</span></span>           | <span data-ttu-id="48538-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-151">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-152">System-Flags</span></span>           | <span data-ttu-id="48538-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-153">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-154">Classes used in</span></span>        | [<span data-ttu-id="48538-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48538-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48538-156">Windows Server 2003</span></span>



| <span data-ttu-id="48538-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-157">Entry</span></span> | <span data-ttu-id="48538-158">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-160">MAPI-Id</span></span>                | <span data-ttu-id="48538-161">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-161">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-162">System-Only</span></span>            | <span data-ttu-id="48538-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-163">False</span></span>                                                    |
| <span data-ttu-id="48538-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-164">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-165">True</span><span class="sxs-lookup"><span data-stu-id="48538-165">True</span></span>                                                     |
| <span data-ttu-id="48538-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-166">Is Indexed</span></span>             | <span data-ttu-id="48538-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-167">False</span></span>                                                    |
| <span data-ttu-id="48538-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-168">In Global Catalog</span></span>      | <span data-ttu-id="48538-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-169">False</span></span>                                                    |
| <span data-ttu-id="48538-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-174">Search-Flags</span></span>           | <span data-ttu-id="48538-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-175">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-176">System-Flags</span></span>           | <span data-ttu-id="48538-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-177">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-178">Classes used in</span></span>        | [<span data-ttu-id="48538-179">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="48538-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="48538-180">ADAM</span></span>



| <span data-ttu-id="48538-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-181">Entry</span></span> | <span data-ttu-id="48538-182">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-184">MAPI-Id</span></span>                | <span data-ttu-id="48538-185">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-185">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-186">System-Only</span></span>            | <span data-ttu-id="48538-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-187">False</span></span>                                                    |
| <span data-ttu-id="48538-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-188">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-189">True</span><span class="sxs-lookup"><span data-stu-id="48538-189">True</span></span>                                                     |
| <span data-ttu-id="48538-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-190">Is Indexed</span></span>             | <span data-ttu-id="48538-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-191">False</span></span>                                                    |
| <span data-ttu-id="48538-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-192">In Global Catalog</span></span>      | <span data-ttu-id="48538-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-193">False</span></span>                                                    |
| <span data-ttu-id="48538-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-198">Search-Flags</span></span>           | <span data-ttu-id="48538-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-199">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-200">System-Flags</span></span>           | <span data-ttu-id="48538-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-201">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-202">Classes used in</span></span>        | [<span data-ttu-id="48538-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48538-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48538-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48538-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-205">Entry</span></span> | <span data-ttu-id="48538-206">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-208">MAPI-Id</span></span>                | <span data-ttu-id="48538-209">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-209">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-210">System-Only</span></span>            | <span data-ttu-id="48538-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-211">False</span></span>                                                    |
| <span data-ttu-id="48538-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-212">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-213">True</span><span class="sxs-lookup"><span data-stu-id="48538-213">True</span></span>                                                     |
| <span data-ttu-id="48538-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-214">Is Indexed</span></span>             | <span data-ttu-id="48538-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-215">False</span></span>                                                    |
| <span data-ttu-id="48538-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-216">In Global Catalog</span></span>      | <span data-ttu-id="48538-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-217">False</span></span>                                                    |
| <span data-ttu-id="48538-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-222">Search-Flags</span></span>           | <span data-ttu-id="48538-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-223">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-224">System-Flags</span></span>           | <span data-ttu-id="48538-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-225">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-226">Classes used in</span></span>        | [<span data-ttu-id="48538-227">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48538-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48538-228">Windows Server 2008</span></span>



| <span data-ttu-id="48538-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-229">Entry</span></span> | <span data-ttu-id="48538-230">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-232">MAPI-Id</span></span>                | <span data-ttu-id="48538-233">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-233">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-234">System-Only</span></span>            | <span data-ttu-id="48538-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-235">False</span></span>                                                    |
| <span data-ttu-id="48538-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-236">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-237">True</span><span class="sxs-lookup"><span data-stu-id="48538-237">True</span></span>                                                     |
| <span data-ttu-id="48538-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-238">Is Indexed</span></span>             | <span data-ttu-id="48538-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-239">False</span></span>                                                    |
| <span data-ttu-id="48538-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-240">In Global Catalog</span></span>      | <span data-ttu-id="48538-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-241">False</span></span>                                                    |
| <span data-ttu-id="48538-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-246">Search-Flags</span></span>           | <span data-ttu-id="48538-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-247">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-248">System-Flags</span></span>           | <span data-ttu-id="48538-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-249">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-250">Classes used in</span></span>        | [<span data-ttu-id="48538-251">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48538-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48538-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48538-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-253">Entry</span></span> | <span data-ttu-id="48538-254">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-256">MAPI-Id</span></span>                | <span data-ttu-id="48538-257">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-257">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-258">System-Only</span></span>            | <span data-ttu-id="48538-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-259">False</span></span>                                                    |
| <span data-ttu-id="48538-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-260">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-261">True</span><span class="sxs-lookup"><span data-stu-id="48538-261">True</span></span>                                                     |
| <span data-ttu-id="48538-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-262">Is Indexed</span></span>             | <span data-ttu-id="48538-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-263">False</span></span>                                                    |
| <span data-ttu-id="48538-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-264">In Global Catalog</span></span>      | <span data-ttu-id="48538-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-265">False</span></span>                                                    |
| <span data-ttu-id="48538-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-270">Search-Flags</span></span>           | <span data-ttu-id="48538-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-271">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-272">System-Flags</span></span>           | <span data-ttu-id="48538-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-273">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-274">Classes used in</span></span>        | [<span data-ttu-id="48538-275">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48538-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48538-276">Windows Server 2012</span></span>



| <span data-ttu-id="48538-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="48538-277">Entry</span></span> | <span data-ttu-id="48538-278">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48538-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="48538-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48538-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48538-280">MAPI-Id</span></span>                | <span data-ttu-id="48538-281">0x80A7</span><span class="sxs-lookup"><span data-stu-id="48538-281">0x80A7</span></span>                                                   |
| <span data-ttu-id="48538-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="48538-282">System-Only</span></span>            | <span data-ttu-id="48538-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-283">False</span></span>                                                    |
| <span data-ttu-id="48538-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="48538-284">Is-Single-Valued</span></span>       | <span data-ttu-id="48538-285">True</span><span class="sxs-lookup"><span data-stu-id="48538-285">True</span></span>                                                     |
| <span data-ttu-id="48538-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="48538-286">Is Indexed</span></span>             | <span data-ttu-id="48538-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-287">False</span></span>                                                    |
| <span data-ttu-id="48538-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="48538-288">In Global Catalog</span></span>      | <span data-ttu-id="48538-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="48538-289">False</span></span>                                                    |
| <span data-ttu-id="48538-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="48538-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="48538-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48538-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48538-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48538-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48538-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48538-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48538-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-294">Search-Flags</span></span>           | <span data-ttu-id="48538-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48538-295">0x00000000</span></span>                                               |
| <span data-ttu-id="48538-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48538-296">System-Flags</span></span>           | <span data-ttu-id="48538-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48538-297">0x00000010</span></span>                                               |
| <span data-ttu-id="48538-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="48538-298">Classes used in</span></span>        | [<span data-ttu-id="48538-299">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="48538-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





