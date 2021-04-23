---
title: Атрибут идентификатора MAPI
description: Целое число, по которому клиенты MAPI определяют этот атрибут.
ms.assetid: 581989f5-d979-4fe6-95d5-2c0651f40d78
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута идентификатора MAPI
- Схема AD атрибута mAPIID
topic_type:
- apiref
api_name:
- MAPI-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4a754d88d048abccd199c6ab20a6a00fcfdc036
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654929"
---
# <a name="mapi-id-attribute"></a><span data-ttu-id="cf951-105">Атрибут идентификатора MAPI</span><span class="sxs-lookup"><span data-stu-id="cf951-105">MAPI-ID attribute</span></span>

<span data-ttu-id="cf951-106">Целое число, по которому клиенты MAPI определяют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="cf951-106">An integer by which MAPI clients identify this attribute.</span></span>



| <span data-ttu-id="cf951-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-107">Entry</span></span> | <span data-ttu-id="cf951-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cf951-109">CN</span><span class="sxs-lookup"><span data-stu-id="cf951-109">CN</span></span>                | <span data-ttu-id="cf951-110">ИДЕНТИФИКАТОР MAPI</span><span class="sxs-lookup"><span data-stu-id="cf951-110">MAPI-ID</span></span>                              |
| <span data-ttu-id="cf951-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cf951-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cf951-112">mAPIID</span><span class="sxs-lookup"><span data-stu-id="cf951-112">mAPIID</span></span>                               |
| <span data-ttu-id="cf951-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cf951-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="cf951-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cf951-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cf951-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cf951-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cf951-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-116">Attribute-Id</span></span>      | <span data-ttu-id="cf951-117">1.2.840.113556.1.2.49</span><span class="sxs-lookup"><span data-stu-id="cf951-117">1.2.840.113556.1.2.49</span></span>                |
| <span data-ttu-id="cf951-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cf951-118">System-Id-Guid</span></span>    | <span data-ttu-id="cf951-119">bf9679b7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cf951-119">bf9679b7-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="cf951-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf951-120">Syntax</span></span>            | [<span data-ttu-id="cf951-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="cf951-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cf951-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cf951-122">Implementations</span></span>

-   [<span data-ttu-id="cf951-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf951-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf951-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf951-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf951-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf951-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf951-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf951-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf951-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf951-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf951-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf951-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf951-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf951-129">Windows 2000 Server</span></span>



| <span data-ttu-id="cf951-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-130">Entry</span></span> | <span data-ttu-id="cf951-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-131">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf951-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf951-132">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="cf951-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-133">MAPI-Id</span></span>                | <span data-ttu-id="cf951-134">0x80CE</span><span class="sxs-lookup"><span data-stu-id="cf951-134">0x80CE</span></span>                                                   |
| <span data-ttu-id="cf951-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf951-135">System-Only</span></span>            | <span data-ttu-id="cf951-136">True</span><span class="sxs-lookup"><span data-stu-id="cf951-136">True</span></span>                                                     |
| <span data-ttu-id="cf951-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf951-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cf951-138">True</span><span class="sxs-lookup"><span data-stu-id="cf951-138">True</span></span>                                                     |
| <span data-ttu-id="cf951-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf951-139">Is Indexed</span></span>             | <span data-ttu-id="cf951-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-140">False</span></span>                                                    |
| <span data-ttu-id="cf951-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf951-141">In Global Catalog</span></span>      | <span data-ttu-id="cf951-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-142">False</span></span>                                                    |
| <span data-ttu-id="cf951-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf951-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf951-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf951-144">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="cf951-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf951-145">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf951-146">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-147">Search-Flags</span></span>           | <span data-ttu-id="cf951-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf951-148">0x00000000</span></span>                                               |
| <span data-ttu-id="cf951-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-149">System-Flags</span></span>           | <span data-ttu-id="cf951-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf951-150">0x00000010</span></span>                                               |
| <span data-ttu-id="cf951-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf951-151">Classes used in</span></span>        | [<span data-ttu-id="cf951-152">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="cf951-152">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf951-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf951-153">Windows Server 2003</span></span>



| <span data-ttu-id="cf951-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-154">Entry</span></span> | <span data-ttu-id="cf951-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-155">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf951-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf951-156">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="cf951-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-157">MAPI-Id</span></span>                | <span data-ttu-id="cf951-158">0x80CE</span><span class="sxs-lookup"><span data-stu-id="cf951-158">0x80CE</span></span>                                                   |
| <span data-ttu-id="cf951-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf951-159">System-Only</span></span>            | <span data-ttu-id="cf951-160">True</span><span class="sxs-lookup"><span data-stu-id="cf951-160">True</span></span>                                                     |
| <span data-ttu-id="cf951-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf951-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cf951-162">True</span><span class="sxs-lookup"><span data-stu-id="cf951-162">True</span></span>                                                     |
| <span data-ttu-id="cf951-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf951-163">Is Indexed</span></span>             | <span data-ttu-id="cf951-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-164">False</span></span>                                                    |
| <span data-ttu-id="cf951-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf951-165">In Global Catalog</span></span>      | <span data-ttu-id="cf951-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-166">False</span></span>                                                    |
| <span data-ttu-id="cf951-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf951-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf951-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf951-168">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="cf951-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf951-169">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf951-170">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-171">Search-Flags</span></span>           | <span data-ttu-id="cf951-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf951-172">0x00000000</span></span>                                               |
| <span data-ttu-id="cf951-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-173">System-Flags</span></span>           | <span data-ttu-id="cf951-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf951-174">0x00000010</span></span>                                               |
| <span data-ttu-id="cf951-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf951-175">Classes used in</span></span>        | [<span data-ttu-id="cf951-176">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="cf951-176">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf951-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf951-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf951-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-178">Entry</span></span> | <span data-ttu-id="cf951-179">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-179">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf951-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf951-180">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="cf951-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-181">MAPI-Id</span></span>                | <span data-ttu-id="cf951-182">0x80CE</span><span class="sxs-lookup"><span data-stu-id="cf951-182">0x80CE</span></span>                                                   |
| <span data-ttu-id="cf951-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf951-183">System-Only</span></span>            | <span data-ttu-id="cf951-184">True</span><span class="sxs-lookup"><span data-stu-id="cf951-184">True</span></span>                                                     |
| <span data-ttu-id="cf951-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf951-185">Is-Single-Valued</span></span>       | <span data-ttu-id="cf951-186">True</span><span class="sxs-lookup"><span data-stu-id="cf951-186">True</span></span>                                                     |
| <span data-ttu-id="cf951-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf951-187">Is Indexed</span></span>             | <span data-ttu-id="cf951-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-188">False</span></span>                                                    |
| <span data-ttu-id="cf951-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf951-189">In Global Catalog</span></span>      | <span data-ttu-id="cf951-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-190">False</span></span>                                                    |
| <span data-ttu-id="cf951-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf951-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf951-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf951-192">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="cf951-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf951-193">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf951-194">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-195">Search-Flags</span></span>           | <span data-ttu-id="cf951-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf951-196">0x00000000</span></span>                                               |
| <span data-ttu-id="cf951-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-197">System-Flags</span></span>           | <span data-ttu-id="cf951-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf951-198">0x00000010</span></span>                                               |
| <span data-ttu-id="cf951-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf951-199">Classes used in</span></span>        | [<span data-ttu-id="cf951-200">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="cf951-200">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf951-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf951-201">Windows Server 2008</span></span>



| <span data-ttu-id="cf951-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-202">Entry</span></span> | <span data-ttu-id="cf951-203">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-203">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf951-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf951-204">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="cf951-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-205">MAPI-Id</span></span>                | <span data-ttu-id="cf951-206">0x80CE</span><span class="sxs-lookup"><span data-stu-id="cf951-206">0x80CE</span></span>                                                   |
| <span data-ttu-id="cf951-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf951-207">System-Only</span></span>            | <span data-ttu-id="cf951-208">True</span><span class="sxs-lookup"><span data-stu-id="cf951-208">True</span></span>                                                     |
| <span data-ttu-id="cf951-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf951-209">Is-Single-Valued</span></span>       | <span data-ttu-id="cf951-210">True</span><span class="sxs-lookup"><span data-stu-id="cf951-210">True</span></span>                                                     |
| <span data-ttu-id="cf951-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf951-211">Is Indexed</span></span>             | <span data-ttu-id="cf951-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-212">False</span></span>                                                    |
| <span data-ttu-id="cf951-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf951-213">In Global Catalog</span></span>      | <span data-ttu-id="cf951-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-214">False</span></span>                                                    |
| <span data-ttu-id="cf951-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf951-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf951-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf951-216">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="cf951-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf951-217">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf951-218">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-219">Search-Flags</span></span>           | <span data-ttu-id="cf951-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf951-220">0x00000000</span></span>                                               |
| <span data-ttu-id="cf951-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-221">System-Flags</span></span>           | <span data-ttu-id="cf951-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf951-222">0x00000010</span></span>                                               |
| <span data-ttu-id="cf951-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf951-223">Classes used in</span></span>        | [<span data-ttu-id="cf951-224">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="cf951-224">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf951-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf951-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf951-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-226">Entry</span></span> | <span data-ttu-id="cf951-227">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-227">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf951-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf951-228">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="cf951-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-229">MAPI-Id</span></span>                | <span data-ttu-id="cf951-230">0x80CE</span><span class="sxs-lookup"><span data-stu-id="cf951-230">0x80CE</span></span>                                                   |
| <span data-ttu-id="cf951-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf951-231">System-Only</span></span>            | <span data-ttu-id="cf951-232">True</span><span class="sxs-lookup"><span data-stu-id="cf951-232">True</span></span>                                                     |
| <span data-ttu-id="cf951-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf951-233">Is-Single-Valued</span></span>       | <span data-ttu-id="cf951-234">True</span><span class="sxs-lookup"><span data-stu-id="cf951-234">True</span></span>                                                     |
| <span data-ttu-id="cf951-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf951-235">Is Indexed</span></span>             | <span data-ttu-id="cf951-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-236">False</span></span>                                                    |
| <span data-ttu-id="cf951-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf951-237">In Global Catalog</span></span>      | <span data-ttu-id="cf951-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-238">False</span></span>                                                    |
| <span data-ttu-id="cf951-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf951-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf951-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf951-240">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="cf951-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf951-241">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf951-242">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-243">Search-Flags</span></span>           | <span data-ttu-id="cf951-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf951-244">0x00000000</span></span>                                               |
| <span data-ttu-id="cf951-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-245">System-Flags</span></span>           | <span data-ttu-id="cf951-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf951-246">0x00000010</span></span>                                               |
| <span data-ttu-id="cf951-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf951-247">Classes used in</span></span>        | [<span data-ttu-id="cf951-248">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="cf951-248">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf951-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf951-249">Windows Server 2012</span></span>



| <span data-ttu-id="cf951-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf951-250">Entry</span></span> | <span data-ttu-id="cf951-251">Значение</span><span class="sxs-lookup"><span data-stu-id="cf951-251">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf951-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf951-252">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="cf951-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf951-253">MAPI-Id</span></span>                | <span data-ttu-id="cf951-254">0x80CE</span><span class="sxs-lookup"><span data-stu-id="cf951-254">0x80CE</span></span>                                                   |
| <span data-ttu-id="cf951-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf951-255">System-Only</span></span>            | <span data-ttu-id="cf951-256">True</span><span class="sxs-lookup"><span data-stu-id="cf951-256">True</span></span>                                                     |
| <span data-ttu-id="cf951-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf951-257">Is-Single-Valued</span></span>       | <span data-ttu-id="cf951-258">True</span><span class="sxs-lookup"><span data-stu-id="cf951-258">True</span></span>                                                     |
| <span data-ttu-id="cf951-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf951-259">Is Indexed</span></span>             | <span data-ttu-id="cf951-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-260">False</span></span>                                                    |
| <span data-ttu-id="cf951-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf951-261">In Global Catalog</span></span>      | <span data-ttu-id="cf951-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf951-262">False</span></span>                                                    |
| <span data-ttu-id="cf951-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf951-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf951-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf951-264">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="cf951-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf951-265">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf951-266">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="cf951-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-267">Search-Flags</span></span>           | <span data-ttu-id="cf951-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf951-268">0x00000000</span></span>                                               |
| <span data-ttu-id="cf951-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf951-269">System-Flags</span></span>           | <span data-ttu-id="cf951-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf951-270">0x00000010</span></span>                                               |
| <span data-ttu-id="cf951-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf951-271">Classes used in</span></span>        | [<span data-ttu-id="cf951-272">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="cf951-272">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





