---
title: MS-WMI-запрос атрибута
description: Один WQL-запрос.
ms.assetid: 3fb594fc-d160-4807-a019-3dec56d2262b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута запроса MS-WMI
- Мсвми — схема AD атрибута запроса
topic_type:
- apiref
api_name:
- ms-WMI-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5bb5376cf957d46894c6fa2c59016564d28dfb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893742"
---
# <a name="ms-wmi-query-attribute"></a><span data-ttu-id="91eaa-105">MS-WMI-запрос атрибута</span><span class="sxs-lookup"><span data-stu-id="91eaa-105">ms-WMI-Query attribute</span></span>

<span data-ttu-id="91eaa-106">Один WQL-запрос.</span><span class="sxs-lookup"><span data-stu-id="91eaa-106">A single WQL query.</span></span>



| <span data-ttu-id="91eaa-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="91eaa-107">Entry</span></span> | <span data-ttu-id="91eaa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="91eaa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="91eaa-109">CN</span><span class="sxs-lookup"><span data-stu-id="91eaa-109">CN</span></span>                | <span data-ttu-id="91eaa-110">MS-WMI-Query</span><span class="sxs-lookup"><span data-stu-id="91eaa-110">ms-WMI-Query</span></span>                                |
| <span data-ttu-id="91eaa-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="91eaa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="91eaa-112">Мсвми — запрос</span><span class="sxs-lookup"><span data-stu-id="91eaa-112">msWMI-Query</span></span>                                 |
| <span data-ttu-id="91eaa-113">Размер</span><span class="sxs-lookup"><span data-stu-id="91eaa-113">Size</span></span>              | <span data-ttu-id="91eaa-114">Менее 250 символов.</span><span class="sxs-lookup"><span data-stu-id="91eaa-114">Less than 250 characters.</span></span>                   |
| <span data-ttu-id="91eaa-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="91eaa-115">Update Privilege</span></span>  | <span data-ttu-id="91eaa-116">Администратор групповая политика</span><span class="sxs-lookup"><span data-stu-id="91eaa-116">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="91eaa-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="91eaa-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="91eaa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91eaa-118">Attribute-Id</span></span>      | <span data-ttu-id="91eaa-119">1.2.840.113556.1.4.1642</span><span class="sxs-lookup"><span data-stu-id="91eaa-119">1.2.840.113556.1.4.1642</span></span>                     |
| <span data-ttu-id="91eaa-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="91eaa-120">System-Id-Guid</span></span>    | <span data-ttu-id="91eaa-121">65fff93e-35e3-45a3-85ae-876c6718297f</span><span class="sxs-lookup"><span data-stu-id="91eaa-121">65fff93e-35e3-45a3-85ae-876c6718297f</span></span>        |
| <span data-ttu-id="91eaa-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91eaa-122">Syntax</span></span>            | [<span data-ttu-id="91eaa-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="91eaa-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="91eaa-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="91eaa-124">Implementations</span></span>

-   [<span data-ttu-id="91eaa-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91eaa-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91eaa-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91eaa-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91eaa-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91eaa-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91eaa-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91eaa-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91eaa-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91eaa-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="91eaa-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91eaa-130">Windows Server 2003</span></span>



| <span data-ttu-id="91eaa-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="91eaa-131">Entry</span></span> | <span data-ttu-id="91eaa-132">Значение</span><span class="sxs-lookup"><span data-stu-id="91eaa-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="91eaa-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91eaa-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91eaa-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="91eaa-135">System-Only</span></span>            | <span data-ttu-id="91eaa-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-136">False</span></span>                                          |
| <span data-ttu-id="91eaa-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91eaa-137">Is-Single-Valued</span></span>       | <span data-ttu-id="91eaa-138">True</span><span class="sxs-lookup"><span data-stu-id="91eaa-138">True</span></span>                                           |
| <span data-ttu-id="91eaa-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91eaa-139">Is Indexed</span></span>             | <span data-ttu-id="91eaa-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-140">False</span></span>                                          |
| <span data-ttu-id="91eaa-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91eaa-141">In Global Catalog</span></span>      | <span data-ttu-id="91eaa-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-142">False</span></span>                                          |
| <span data-ttu-id="91eaa-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91eaa-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="91eaa-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91eaa-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="91eaa-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91eaa-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91eaa-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-147">Search-Flags</span></span>           | <span data-ttu-id="91eaa-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91eaa-148">0x00000000</span></span>                                     |
| <span data-ttu-id="91eaa-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-149">System-Flags</span></span>           | <span data-ttu-id="91eaa-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91eaa-150">0x00000010</span></span>                                     |
| <span data-ttu-id="91eaa-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91eaa-151">Classes used in</span></span>        | [<span data-ttu-id="91eaa-152">**MS-WMI-правило**</span><span class="sxs-lookup"><span data-stu-id="91eaa-152">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91eaa-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91eaa-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91eaa-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="91eaa-154">Entry</span></span> | <span data-ttu-id="91eaa-155">Значение</span><span class="sxs-lookup"><span data-stu-id="91eaa-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="91eaa-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91eaa-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91eaa-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="91eaa-158">System-Only</span></span>            | <span data-ttu-id="91eaa-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-159">False</span></span>                                          |
| <span data-ttu-id="91eaa-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91eaa-160">Is-Single-Valued</span></span>       | <span data-ttu-id="91eaa-161">True</span><span class="sxs-lookup"><span data-stu-id="91eaa-161">True</span></span>                                           |
| <span data-ttu-id="91eaa-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91eaa-162">Is Indexed</span></span>             | <span data-ttu-id="91eaa-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-163">False</span></span>                                          |
| <span data-ttu-id="91eaa-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91eaa-164">In Global Catalog</span></span>      | <span data-ttu-id="91eaa-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-165">False</span></span>                                          |
| <span data-ttu-id="91eaa-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91eaa-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="91eaa-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91eaa-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="91eaa-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91eaa-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91eaa-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-170">Search-Flags</span></span>           | <span data-ttu-id="91eaa-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91eaa-171">0x00000000</span></span>                                     |
| <span data-ttu-id="91eaa-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-172">System-Flags</span></span>           | <span data-ttu-id="91eaa-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91eaa-173">0x00000010</span></span>                                     |
| <span data-ttu-id="91eaa-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91eaa-174">Classes used in</span></span>        | [<span data-ttu-id="91eaa-175">**MS-WMI-правило**</span><span class="sxs-lookup"><span data-stu-id="91eaa-175">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91eaa-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91eaa-176">Windows Server 2008</span></span>



| <span data-ttu-id="91eaa-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="91eaa-177">Entry</span></span> | <span data-ttu-id="91eaa-178">Значение</span><span class="sxs-lookup"><span data-stu-id="91eaa-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="91eaa-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91eaa-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91eaa-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="91eaa-181">System-Only</span></span>            | <span data-ttu-id="91eaa-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-182">False</span></span>                                          |
| <span data-ttu-id="91eaa-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91eaa-183">Is-Single-Valued</span></span>       | <span data-ttu-id="91eaa-184">True</span><span class="sxs-lookup"><span data-stu-id="91eaa-184">True</span></span>                                           |
| <span data-ttu-id="91eaa-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91eaa-185">Is Indexed</span></span>             | <span data-ttu-id="91eaa-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-186">False</span></span>                                          |
| <span data-ttu-id="91eaa-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91eaa-187">In Global Catalog</span></span>      | <span data-ttu-id="91eaa-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-188">False</span></span>                                          |
| <span data-ttu-id="91eaa-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91eaa-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="91eaa-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91eaa-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="91eaa-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91eaa-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91eaa-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-193">Search-Flags</span></span>           | <span data-ttu-id="91eaa-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91eaa-194">0x00000000</span></span>                                     |
| <span data-ttu-id="91eaa-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-195">System-Flags</span></span>           | <span data-ttu-id="91eaa-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91eaa-196">0x00000010</span></span>                                     |
| <span data-ttu-id="91eaa-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91eaa-197">Classes used in</span></span>        | [<span data-ttu-id="91eaa-198">**MS-WMI-правило**</span><span class="sxs-lookup"><span data-stu-id="91eaa-198">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91eaa-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91eaa-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91eaa-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="91eaa-200">Entry</span></span> | <span data-ttu-id="91eaa-201">Значение</span><span class="sxs-lookup"><span data-stu-id="91eaa-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="91eaa-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91eaa-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91eaa-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="91eaa-204">System-Only</span></span>            | <span data-ttu-id="91eaa-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-205">False</span></span>                                          |
| <span data-ttu-id="91eaa-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91eaa-206">Is-Single-Valued</span></span>       | <span data-ttu-id="91eaa-207">True</span><span class="sxs-lookup"><span data-stu-id="91eaa-207">True</span></span>                                           |
| <span data-ttu-id="91eaa-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91eaa-208">Is Indexed</span></span>             | <span data-ttu-id="91eaa-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-209">False</span></span>                                          |
| <span data-ttu-id="91eaa-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91eaa-210">In Global Catalog</span></span>      | <span data-ttu-id="91eaa-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-211">False</span></span>                                          |
| <span data-ttu-id="91eaa-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91eaa-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="91eaa-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91eaa-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="91eaa-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91eaa-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91eaa-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-216">Search-Flags</span></span>           | <span data-ttu-id="91eaa-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91eaa-217">0x00000000</span></span>                                     |
| <span data-ttu-id="91eaa-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-218">System-Flags</span></span>           | <span data-ttu-id="91eaa-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91eaa-219">0x00000010</span></span>                                     |
| <span data-ttu-id="91eaa-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91eaa-220">Classes used in</span></span>        | [<span data-ttu-id="91eaa-221">**MS-WMI-правило**</span><span class="sxs-lookup"><span data-stu-id="91eaa-221">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91eaa-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91eaa-222">Windows Server 2012</span></span>



| <span data-ttu-id="91eaa-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="91eaa-223">Entry</span></span> | <span data-ttu-id="91eaa-224">Значение</span><span class="sxs-lookup"><span data-stu-id="91eaa-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="91eaa-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91eaa-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91eaa-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="91eaa-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="91eaa-227">System-Only</span></span>            | <span data-ttu-id="91eaa-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-228">False</span></span>                                          |
| <span data-ttu-id="91eaa-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91eaa-229">Is-Single-Valued</span></span>       | <span data-ttu-id="91eaa-230">True</span><span class="sxs-lookup"><span data-stu-id="91eaa-230">True</span></span>                                           |
| <span data-ttu-id="91eaa-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91eaa-231">Is Indexed</span></span>             | <span data-ttu-id="91eaa-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-232">False</span></span>                                          |
| <span data-ttu-id="91eaa-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91eaa-233">In Global Catalog</span></span>      | <span data-ttu-id="91eaa-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="91eaa-234">False</span></span>                                          |
| <span data-ttu-id="91eaa-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91eaa-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="91eaa-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91eaa-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="91eaa-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91eaa-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91eaa-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="91eaa-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-239">Search-Flags</span></span>           | <span data-ttu-id="91eaa-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91eaa-240">0x00000000</span></span>                                     |
| <span data-ttu-id="91eaa-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91eaa-241">System-Flags</span></span>           | <span data-ttu-id="91eaa-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91eaa-242">0x00000010</span></span>                                     |
| <span data-ttu-id="91eaa-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91eaa-243">Classes used in</span></span>        | [<span data-ttu-id="91eaa-244">**MS-WMI-правило**</span><span class="sxs-lookup"><span data-stu-id="91eaa-244">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



 

 





