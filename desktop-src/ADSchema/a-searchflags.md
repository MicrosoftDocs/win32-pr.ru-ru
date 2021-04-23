---
title: Атрибут Search-Flags
description: Содержит набор флагов, задающих сведения о поиске и индексировании для атрибута.
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Search-Flags
- Схема AD атрибута searchFlags
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f615464aa0aed69dd9590f668e37ec8c789c88
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655291"
---
# <a name="search-flags-attribute"></a><span data-ttu-id="60ea9-105">Атрибут Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-105">Search-Flags attribute</span></span>

<span data-ttu-id="60ea9-106">Содержит набор флагов, задающих сведения о поиске и индексировании для атрибута.</span><span class="sxs-lookup"><span data-stu-id="60ea9-106">Contains a set of flags that specify search and indexing information for an attribute.</span></span> <span data-ttu-id="60ea9-107">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="60ea9-107">See Remarks.</span></span>



| <span data-ttu-id="60ea9-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-108">Entry</span></span> | <span data-ttu-id="60ea9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="60ea9-110">CN</span><span class="sxs-lookup"><span data-stu-id="60ea9-110">CN</span></span>                | <span data-ttu-id="60ea9-111">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-111">Search-Flags</span></span>                         |
| <span data-ttu-id="60ea9-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="60ea9-112">Ldap-Display-Name</span></span> | <span data-ttu-id="60ea9-113">searchFlags</span><span class="sxs-lookup"><span data-stu-id="60ea9-113">searchFlags</span></span>                          |
| <span data-ttu-id="60ea9-114">Размер</span><span class="sxs-lookup"><span data-stu-id="60ea9-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="60ea9-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="60ea9-115">Update Privilege</span></span>  | <span data-ttu-id="60ea9-116">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="60ea9-116">Schema administrator</span></span>                 |
| <span data-ttu-id="60ea9-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="60ea9-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="60ea9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-118">Attribute-Id</span></span>      | <span data-ttu-id="60ea9-119">1.2.840.113556.1.2.334</span><span class="sxs-lookup"><span data-stu-id="60ea9-119">1.2.840.113556.1.2.334</span></span>               |
| <span data-ttu-id="60ea9-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="60ea9-120">System-Id-Guid</span></span>    | <span data-ttu-id="60ea9-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="60ea9-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="60ea9-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60ea9-122">Syntax</span></span>            | [<span data-ttu-id="60ea9-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="60ea9-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="60ea9-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="60ea9-124">Implementations</span></span>

-   [<span data-ttu-id="60ea9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="60ea9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="60ea9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="60ea9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="60ea9-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="60ea9-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="60ea9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="60ea9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="60ea9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="60ea9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="60ea9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="60ea9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="60ea9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="60ea9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="60ea9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60ea9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="60ea9-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-133">Entry</span></span> | <span data-ttu-id="60ea9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-136">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-137">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-137">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-138">System-Only</span></span>            | <span data-ttu-id="60ea9-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-139">False</span></span>                                                    |
| <span data-ttu-id="60ea9-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-141">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-141">True</span></span>                                                     |
| <span data-ttu-id="60ea9-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-142">Is Indexed</span></span>             | <span data-ttu-id="60ea9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-143">False</span></span>                                                    |
| <span data-ttu-id="60ea9-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-144">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-145">False</span></span>                                                    |
| <span data-ttu-id="60ea9-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-150">Search-Flags</span></span>           | <span data-ttu-id="60ea9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-151">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-152">System-Flags</span></span>           | <span data-ttu-id="60ea9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-153">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-154">Classes used in</span></span>        | [<span data-ttu-id="60ea9-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="60ea9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60ea9-156">Windows Server 2003</span></span>



| <span data-ttu-id="60ea9-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-157">Entry</span></span> | <span data-ttu-id="60ea9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-160">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-161">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-161">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-162">System-Only</span></span>            | <span data-ttu-id="60ea9-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-163">False</span></span>                                                    |
| <span data-ttu-id="60ea9-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-164">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-165">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-165">True</span></span>                                                     |
| <span data-ttu-id="60ea9-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-166">Is Indexed</span></span>             | <span data-ttu-id="60ea9-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-167">False</span></span>                                                    |
| <span data-ttu-id="60ea9-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-168">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-169">False</span></span>                                                    |
| <span data-ttu-id="60ea9-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-174">Search-Flags</span></span>           | <span data-ttu-id="60ea9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-175">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-176">System-Flags</span></span>           | <span data-ttu-id="60ea9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-177">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-178">Classes used in</span></span>        | [<span data-ttu-id="60ea9-179">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="60ea9-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="60ea9-180">ADAM</span></span>



| <span data-ttu-id="60ea9-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-181">Entry</span></span> | <span data-ttu-id="60ea9-182">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-184">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-185">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-185">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-186">System-Only</span></span>            | <span data-ttu-id="60ea9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-187">False</span></span>                                                    |
| <span data-ttu-id="60ea9-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-189">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-189">True</span></span>                                                     |
| <span data-ttu-id="60ea9-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-190">Is Indexed</span></span>             | <span data-ttu-id="60ea9-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-191">False</span></span>                                                    |
| <span data-ttu-id="60ea9-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-192">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-193">False</span></span>                                                    |
| <span data-ttu-id="60ea9-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-198">Search-Flags</span></span>           | <span data-ttu-id="60ea9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-199">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-200">System-Flags</span></span>           | <span data-ttu-id="60ea9-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-201">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-202">Classes used in</span></span>        | [<span data-ttu-id="60ea9-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="60ea9-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="60ea9-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="60ea9-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-205">Entry</span></span> | <span data-ttu-id="60ea9-206">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-208">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-209">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-209">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-210">System-Only</span></span>            | <span data-ttu-id="60ea9-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-211">False</span></span>                                                    |
| <span data-ttu-id="60ea9-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-213">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-213">True</span></span>                                                     |
| <span data-ttu-id="60ea9-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-214">Is Indexed</span></span>             | <span data-ttu-id="60ea9-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-215">False</span></span>                                                    |
| <span data-ttu-id="60ea9-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-216">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-217">False</span></span>                                                    |
| <span data-ttu-id="60ea9-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-222">Search-Flags</span></span>           | <span data-ttu-id="60ea9-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-223">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-224">System-Flags</span></span>           | <span data-ttu-id="60ea9-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-225">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-226">Classes used in</span></span>        | [<span data-ttu-id="60ea9-227">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="60ea9-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60ea9-228">Windows Server 2008</span></span>



| <span data-ttu-id="60ea9-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-229">Entry</span></span> | <span data-ttu-id="60ea9-230">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-232">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-233">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-233">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-234">System-Only</span></span>            | <span data-ttu-id="60ea9-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-235">False</span></span>                                                    |
| <span data-ttu-id="60ea9-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-236">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-237">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-237">True</span></span>                                                     |
| <span data-ttu-id="60ea9-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-238">Is Indexed</span></span>             | <span data-ttu-id="60ea9-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-239">False</span></span>                                                    |
| <span data-ttu-id="60ea9-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-240">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-241">False</span></span>                                                    |
| <span data-ttu-id="60ea9-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-246">Search-Flags</span></span>           | <span data-ttu-id="60ea9-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-247">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-248">System-Flags</span></span>           | <span data-ttu-id="60ea9-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-249">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-250">Classes used in</span></span>        | [<span data-ttu-id="60ea9-251">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="60ea9-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60ea9-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="60ea9-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-253">Entry</span></span> | <span data-ttu-id="60ea9-254">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-256">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-257">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-257">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-258">System-Only</span></span>            | <span data-ttu-id="60ea9-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-259">False</span></span>                                                    |
| <span data-ttu-id="60ea9-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-260">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-261">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-261">True</span></span>                                                     |
| <span data-ttu-id="60ea9-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-262">Is Indexed</span></span>             | <span data-ttu-id="60ea9-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-263">False</span></span>                                                    |
| <span data-ttu-id="60ea9-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-264">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-265">False</span></span>                                                    |
| <span data-ttu-id="60ea9-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-270">Search-Flags</span></span>           | <span data-ttu-id="60ea9-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-271">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-272">System-Flags</span></span>           | <span data-ttu-id="60ea9-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-273">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-274">Classes used in</span></span>        | [<span data-ttu-id="60ea9-275">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="60ea9-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60ea9-276">Windows Server 2012</span></span>



| <span data-ttu-id="60ea9-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="60ea9-277">Entry</span></span> | <span data-ttu-id="60ea9-278">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="60ea9-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="60ea9-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="60ea9-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60ea9-280">MAPI-Id</span></span>                | <span data-ttu-id="60ea9-281">0x812D</span><span class="sxs-lookup"><span data-stu-id="60ea9-281">0x812D</span></span>                                                   |
| <span data-ttu-id="60ea9-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="60ea9-282">System-Only</span></span>            | <span data-ttu-id="60ea9-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-283">False</span></span>                                                    |
| <span data-ttu-id="60ea9-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="60ea9-284">Is-Single-Valued</span></span>       | <span data-ttu-id="60ea9-285">True</span><span class="sxs-lookup"><span data-stu-id="60ea9-285">True</span></span>                                                     |
| <span data-ttu-id="60ea9-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="60ea9-286">Is Indexed</span></span>             | <span data-ttu-id="60ea9-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-287">False</span></span>                                                    |
| <span data-ttu-id="60ea9-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="60ea9-288">In Global Catalog</span></span>      | <span data-ttu-id="60ea9-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="60ea9-289">False</span></span>                                                    |
| <span data-ttu-id="60ea9-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="60ea9-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="60ea9-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60ea9-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="60ea9-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60ea9-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60ea9-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="60ea9-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-294">Search-Flags</span></span>           | <span data-ttu-id="60ea9-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60ea9-295">0x00000000</span></span>                                               |
| <span data-ttu-id="60ea9-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60ea9-296">System-Flags</span></span>           | <span data-ttu-id="60ea9-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="60ea9-297">0x00000010</span></span>                                               |
| <span data-ttu-id="60ea9-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="60ea9-298">Classes used in</span></span>        | [<span data-ttu-id="60ea9-299">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="60ea9-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="60ea9-300">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60ea9-300">Remarks</span></span>

<span data-ttu-id="60ea9-301">Этот атрибут может быть нулевым или сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="60ea9-301">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="60ea9-302">Значение</span><span class="sxs-lookup"><span data-stu-id="60ea9-302">Value</span></span>            | <span data-ttu-id="60ea9-303">Описание</span><span class="sxs-lookup"><span data-stu-id="60ea9-303">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ea9-304">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="60ea9-304">1 (0x00000001)</span></span>   | <span data-ttu-id="60ea9-305">Создайте индекс для атрибута.</span><span class="sxs-lookup"><span data-stu-id="60ea9-305">Create an index for the attribute.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="60ea9-306">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="60ea9-306">2 (0x00000002)</span></span>   | <span data-ttu-id="60ea9-307">Создайте индекс для атрибута в каждом контейнере.</span><span class="sxs-lookup"><span data-stu-id="60ea9-307">Create an index for the attribute in each container.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="60ea9-308">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="60ea9-308">4 (0x00000004)</span></span>   | <span data-ttu-id="60ea9-309">Добавьте этот атрибут в набор разрешения неоднозначных имен (ANR).</span><span class="sxs-lookup"><span data-stu-id="60ea9-309">Add this attribute to the Ambiguous Name Resolution (ANR) set.</span></span> <span data-ttu-id="60ea9-310">Используется для поиска объекта при наличии только частичной информации.</span><span class="sxs-lookup"><span data-stu-id="60ea9-310">This is used to assist in finding an object when only partial information is given.</span></span> <span data-ttu-id="60ea9-311">Например, если фильтр LDAP имеет значение (ANR = Джефф), поиск будет находить каждый объект, в котором имя, фамилия, адрес электронной почты или другой атрибут ANR равны ДЖЕФФу.</span><span class="sxs-lookup"><span data-stu-id="60ea9-311">For example, if the LDAP filter is (ANR=JEFF), the search will find each object where the first name, last name, email address, or other ANR attribute is equal to JEFF.</span></span> <span data-ttu-id="60ea9-312">Чтобы этот индекс вступил в силу, необходимо установить бит 0.</span><span class="sxs-lookup"><span data-stu-id="60ea9-312">Bit 0 must be set for this index take affect.</span></span> |
| <span data-ttu-id="60ea9-313">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="60ea9-313">8 (0x00000008)</span></span>   | <span data-ttu-id="60ea9-314">Сохраните этот атрибут в объекте захоронения для удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="60ea9-314">Preserve this attribute in the tombstone object for deleted objects.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="60ea9-315">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="60ea9-315">16 (0x00000010)</span></span>  | <span data-ttu-id="60ea9-316">Скопируйте значение этого атрибута при копировании объекта.</span><span class="sxs-lookup"><span data-stu-id="60ea9-316">Copy the value for this attribute when the object is copied.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="60ea9-317">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="60ea9-317">32 (0x00000020)</span></span>  | <span data-ttu-id="60ea9-318">Создайте индекс кортежа для атрибута.</span><span class="sxs-lookup"><span data-stu-id="60ea9-318">Create a tuple index for the attribute.</span></span> <span data-ttu-id="60ea9-319">Это улучшит Поиск, когда в начале строки поиска появится подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="60ea9-319">This will improve searches where the wildcard appears at the front of the search string.</span></span> <span data-ttu-id="60ea9-320">Например, (SN = \* МИС).</span><span class="sxs-lookup"><span data-stu-id="60ea9-320">For example, (sn=\*mith).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="60ea9-321">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="60ea9-321">64(0x00000040)</span></span>   | <span data-ttu-id="60ea9-322">Поддерживается начиная с ADAM.</span><span class="sxs-lookup"><span data-stu-id="60ea9-322">Supported beginning with ADAM.</span></span> <span data-ttu-id="60ea9-323">Создает индекс, значительно помогающий VLV производительность на произвольных атрибутах.</span><span class="sxs-lookup"><span data-stu-id="60ea9-323">Creates an index to greatly help VLV performance on arbitrary attributes.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="60ea9-324">128 (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="60ea9-324">128 (0x00000080)</span></span> | <span data-ttu-id="60ea9-325">Пометьте атрибут как конфиденциальный.</span><span class="sxs-lookup"><span data-stu-id="60ea9-325">Mark attribute as confidential.</span></span> <span data-ttu-id="60ea9-326">Игнорируется для атрибутов базовой схемы (systemFlags = 0x10).</span><span class="sxs-lookup"><span data-stu-id="60ea9-326">Ignored for base schema attributes (systemFlags=0x10).</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="60ea9-327">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="60ea9-327">64 (0x00000040)</span></span>  | <span data-ttu-id="60ea9-328">Поддерживается начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="60ea9-328">Supported beginning with Windows Server 2008.</span></span> <span data-ttu-id="60ea9-329">Создайте индекс, чтобы улучшить производительность поиска VLV для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="60ea9-329">Create an index to improve VLV search performance on this attribute.</span></span>                                                                                                                                                                                                                                                        |



 

 

 





