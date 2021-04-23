---
title: Атрибут Attribute-Syntax
description: OID для синтаксиса этого атрибута.
ms.assetid: 7ae16381-c8e9-4f85-b3e6-86c82b487ca2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Attribute-Syntax
- Схема AD атрибута attributeSyntax
topic_type:
- apiref
api_name:
- Attribute-Syntax
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed69d6886d25f1d47f4340ecfaecd74cc1ae591e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893134"
---
# <a name="attribute-syntax-attribute"></a><span data-ttu-id="c0b17-105">Атрибут Attribute-Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b17-105">Attribute-Syntax attribute</span></span>

<span data-ttu-id="c0b17-106">OID для синтаксиса этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="c0b17-106">The OID for the syntax for this attribute.</span></span>



| <span data-ttu-id="c0b17-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-107">Entry</span></span> | <span data-ttu-id="c0b17-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c0b17-109">CN</span><span class="sxs-lookup"><span data-stu-id="c0b17-109">CN</span></span>                | <span data-ttu-id="c0b17-110">Attribute-Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b17-110">Attribute-Syntax</span></span>                                                |
| <span data-ttu-id="c0b17-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c0b17-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c0b17-112">attributeSyntax</span><span class="sxs-lookup"><span data-stu-id="c0b17-112">attributeSyntax</span></span>                                                 |
| <span data-ttu-id="c0b17-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c0b17-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="c0b17-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c0b17-114">Update Privilege</span></span>  | <span data-ttu-id="c0b17-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="c0b17-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="c0b17-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c0b17-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="c0b17-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-117">Attribute-Id</span></span>      | <span data-ttu-id="c0b17-118">1.2.840.113556.1.2.32</span><span class="sxs-lookup"><span data-stu-id="c0b17-118">1.2.840.113556.1.2.32</span></span>                                           |
| <span data-ttu-id="c0b17-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c0b17-119">System-Id-Guid</span></span>    | <span data-ttu-id="c0b17-120">bf967925-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c0b17-120">bf967925-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="c0b17-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0b17-121">Syntax</span></span>            | [<span data-ttu-id="c0b17-122">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="c0b17-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="c0b17-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c0b17-123">Implementations</span></span>

-   [<span data-ttu-id="c0b17-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c0b17-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c0b17-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c0b17-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c0b17-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c0b17-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c0b17-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c0b17-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c0b17-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c0b17-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c0b17-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c0b17-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c0b17-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c0b17-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c0b17-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0b17-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c0b17-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-132">Entry</span></span> | <span data-ttu-id="c0b17-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-136">System-Only</span></span>            | <span data-ttu-id="c0b17-137">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-137">True</span></span>                                                     |
| <span data-ttu-id="c0b17-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-139">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-139">True</span></span>                                                     |
| <span data-ttu-id="c0b17-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-140">Is Indexed</span></span>             | <span data-ttu-id="c0b17-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-141">False</span></span>                                                    |
| <span data-ttu-id="c0b17-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-142">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-143">False</span></span>                                                    |
| <span data-ttu-id="c0b17-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-146">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-147">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-148">Search-Flags</span></span>           | <span data-ttu-id="c0b17-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-149">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-150">System-Flags</span></span>           | <span data-ttu-id="c0b17-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-151">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-152">Classes used in</span></span>        | [<span data-ttu-id="c0b17-153">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c0b17-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0b17-154">Windows Server 2003</span></span>



| <span data-ttu-id="c0b17-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-155">Entry</span></span> | <span data-ttu-id="c0b17-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-156">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-157">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-158">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-159">System-Only</span></span>            | <span data-ttu-id="c0b17-160">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-160">True</span></span>                                                     |
| <span data-ttu-id="c0b17-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-162">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-162">True</span></span>                                                     |
| <span data-ttu-id="c0b17-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-163">Is Indexed</span></span>             | <span data-ttu-id="c0b17-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-164">False</span></span>                                                    |
| <span data-ttu-id="c0b17-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-165">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-166">False</span></span>                                                    |
| <span data-ttu-id="c0b17-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-168">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-169">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-170">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-171">Search-Flags</span></span>           | <span data-ttu-id="c0b17-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-172">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-173">System-Flags</span></span>           | <span data-ttu-id="c0b17-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-174">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-175">Classes used in</span></span>        | [<span data-ttu-id="c0b17-176">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-176">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c0b17-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="c0b17-177">ADAM</span></span>



| <span data-ttu-id="c0b17-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-178">Entry</span></span> | <span data-ttu-id="c0b17-179">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-179">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-180">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-181">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-182">System-Only</span></span>            | <span data-ttu-id="c0b17-183">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-183">True</span></span>                                                     |
| <span data-ttu-id="c0b17-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-185">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-185">True</span></span>                                                     |
| <span data-ttu-id="c0b17-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-186">Is Indexed</span></span>             | <span data-ttu-id="c0b17-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-187">False</span></span>                                                    |
| <span data-ttu-id="c0b17-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-188">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-189">False</span></span>                                                    |
| <span data-ttu-id="c0b17-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-191">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-192">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-193">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-194">Search-Flags</span></span>           | <span data-ttu-id="c0b17-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-195">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-196">System-Flags</span></span>           | <span data-ttu-id="c0b17-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-197">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-198">Classes used in</span></span>        | [<span data-ttu-id="c0b17-199">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-199">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c0b17-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c0b17-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c0b17-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-201">Entry</span></span> | <span data-ttu-id="c0b17-202">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-202">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-203">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-204">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-205">System-Only</span></span>            | <span data-ttu-id="c0b17-206">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-206">True</span></span>                                                     |
| <span data-ttu-id="c0b17-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-208">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-208">True</span></span>                                                     |
| <span data-ttu-id="c0b17-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-209">Is Indexed</span></span>             | <span data-ttu-id="c0b17-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-210">False</span></span>                                                    |
| <span data-ttu-id="c0b17-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-211">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-212">False</span></span>                                                    |
| <span data-ttu-id="c0b17-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-214">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-215">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-216">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-217">Search-Flags</span></span>           | <span data-ttu-id="c0b17-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-218">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-219">System-Flags</span></span>           | <span data-ttu-id="c0b17-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-220">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-221">Classes used in</span></span>        | [<span data-ttu-id="c0b17-222">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-222">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c0b17-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0b17-223">Windows Server 2008</span></span>



| <span data-ttu-id="c0b17-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-224">Entry</span></span> | <span data-ttu-id="c0b17-225">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-225">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-226">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-227">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-228">System-Only</span></span>            | <span data-ttu-id="c0b17-229">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-229">True</span></span>                                                     |
| <span data-ttu-id="c0b17-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-231">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-231">True</span></span>                                                     |
| <span data-ttu-id="c0b17-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-232">Is Indexed</span></span>             | <span data-ttu-id="c0b17-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-233">False</span></span>                                                    |
| <span data-ttu-id="c0b17-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-234">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-235">False</span></span>                                                    |
| <span data-ttu-id="c0b17-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-237">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-238">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-239">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-240">Search-Flags</span></span>           | <span data-ttu-id="c0b17-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-241">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-242">System-Flags</span></span>           | <span data-ttu-id="c0b17-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-243">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-244">Classes used in</span></span>        | [<span data-ttu-id="c0b17-245">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-245">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c0b17-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0b17-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c0b17-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-247">Entry</span></span> | <span data-ttu-id="c0b17-248">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-248">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-249">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-250">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-251">System-Only</span></span>            | <span data-ttu-id="c0b17-252">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-252">True</span></span>                                                     |
| <span data-ttu-id="c0b17-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-254">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-254">True</span></span>                                                     |
| <span data-ttu-id="c0b17-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-255">Is Indexed</span></span>             | <span data-ttu-id="c0b17-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-256">False</span></span>                                                    |
| <span data-ttu-id="c0b17-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-257">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-258">False</span></span>                                                    |
| <span data-ttu-id="c0b17-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-260">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-261">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-262">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-263">Search-Flags</span></span>           | <span data-ttu-id="c0b17-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-264">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-265">System-Flags</span></span>           | <span data-ttu-id="c0b17-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-266">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-267">Classes used in</span></span>        | [<span data-ttu-id="c0b17-268">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-268">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c0b17-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0b17-269">Windows Server 2012</span></span>



| <span data-ttu-id="c0b17-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0b17-270">Entry</span></span> | <span data-ttu-id="c0b17-271">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b17-271">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0b17-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0b17-272">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b17-273">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c0b17-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b17-274">System-Only</span></span>            | <span data-ttu-id="c0b17-275">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-275">True</span></span>                                                     |
| <span data-ttu-id="c0b17-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0b17-276">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b17-277">True</span><span class="sxs-lookup"><span data-stu-id="c0b17-277">True</span></span>                                                     |
| <span data-ttu-id="c0b17-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0b17-278">Is Indexed</span></span>             | <span data-ttu-id="c0b17-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-279">False</span></span>                                                    |
| <span data-ttu-id="c0b17-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0b17-280">In Global Catalog</span></span>      | <span data-ttu-id="c0b17-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0b17-281">False</span></span>                                                    |
| <span data-ttu-id="c0b17-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0b17-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b17-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b17-283">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c0b17-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b17-284">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b17-285">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c0b17-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-286">Search-Flags</span></span>           | <span data-ttu-id="c0b17-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c0b17-287">0x00000008</span></span>                                               |
| <span data-ttu-id="c0b17-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b17-288">System-Flags</span></span>           | <span data-ttu-id="c0b17-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b17-289">0x00000010</span></span>                                               |
| <span data-ttu-id="c0b17-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0b17-290">Classes used in</span></span>        | [<span data-ttu-id="c0b17-291">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="c0b17-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





