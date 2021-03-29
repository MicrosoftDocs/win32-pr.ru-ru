---
title: MS-WMI-TargetPath, атрибут
description: Список пар "ключ-значение" для уникальной идентификации объекта WMI.
ms.assetid: b5d6c718-86f6-40a5-8fb1-e3ed4821ac62
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута TargetPath для MS-WMI
- Мсвми-схема AD атрибута TargetPath
topic_type:
- apiref
api_name:
- ms-WMI-TargetPath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9818125d757716970cff538167d5d737a8354555
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989653"
---
# <a name="ms-wmi-targetpath-attribute"></a><span data-ttu-id="cd6a3-105">MS-WMI-TargetPath, атрибут</span><span class="sxs-lookup"><span data-stu-id="cd6a3-105">ms-WMI-TargetPath attribute</span></span>

<span data-ttu-id="cd6a3-106">Список пар "ключ-значение" для уникальной идентификации объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-106">List of key/value pairs for uniquely identifying a WMI object.</span></span>



| <span data-ttu-id="cd6a3-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd6a3-107">Entry</span></span> | <span data-ttu-id="cd6a3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6a3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cd6a3-109">CN</span><span class="sxs-lookup"><span data-stu-id="cd6a3-109">CN</span></span>                | <span data-ttu-id="cd6a3-110">MS-WMI-TargetPath</span><span class="sxs-lookup"><span data-stu-id="cd6a3-110">ms-WMI-TargetPath</span></span>                           |
| <span data-ttu-id="cd6a3-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cd6a3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cd6a3-112">Мсвми-TargetPath</span><span class="sxs-lookup"><span data-stu-id="cd6a3-112">msWMI-TargetPath</span></span>                            |
| <span data-ttu-id="cd6a3-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cd6a3-113">Size</span></span>              | <span data-ttu-id="cd6a3-114">Менее 100 символов.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-114">Less than 100 characters.</span></span>                   |
| <span data-ttu-id="cd6a3-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cd6a3-115">Update Privilege</span></span>  | <span data-ttu-id="cd6a3-116">Администратор групповая политика</span><span class="sxs-lookup"><span data-stu-id="cd6a3-116">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="cd6a3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cd6a3-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cd6a3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd6a3-118">Attribute-Id</span></span>      | <span data-ttu-id="cd6a3-119">1.2.840.113556.1.4.1648</span><span class="sxs-lookup"><span data-stu-id="cd6a3-119">1.2.840.113556.1.4.1648</span></span>                     |
| <span data-ttu-id="cd6a3-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cd6a3-120">System-Id-Guid</span></span>    | <span data-ttu-id="cd6a3-121">5006a79a-6bfe-4561-9f52-13cf4dd3e560</span><span class="sxs-lookup"><span data-stu-id="cd6a3-121">5006a79a-6bfe-4561-9f52-13cf4dd3e560</span></span>        |
| <span data-ttu-id="cd6a3-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd6a3-122">Syntax</span></span>            | [<span data-ttu-id="cd6a3-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cd6a3-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cd6a3-124">Implementations</span></span>

-   [<span data-ttu-id="cd6a3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd6a3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd6a3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd6a3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd6a3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cd6a3-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd6a3-130">Windows Server 2003</span></span>



| <span data-ttu-id="cd6a3-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd6a3-131">Entry</span></span> | <span data-ttu-id="cd6a3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6a3-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd6a3-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd6a3-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd6a3-135">System-Only</span></span>            | <span data-ttu-id="cd6a3-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-136">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd6a3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cd6a3-138">True</span><span class="sxs-lookup"><span data-stu-id="cd6a3-138">True</span></span>                                                               |
| <span data-ttu-id="cd6a3-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd6a3-139">Is Indexed</span></span>             | <span data-ttu-id="cd6a3-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-140">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd6a3-141">In Global Catalog</span></span>      | <span data-ttu-id="cd6a3-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-142">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd6a3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd6a3-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd6a3-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd6a3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd6a3-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd6a3-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-147">Search-Flags</span></span>           | <span data-ttu-id="cd6a3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd6a3-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd6a3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-149">System-Flags</span></span>           | <span data-ttu-id="cd6a3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd6a3-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd6a3-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd6a3-151">Classes used in</span></span>        | [<span data-ttu-id="cd6a3-152">**MS-WMI-PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-152">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd6a3-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd6a3-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd6a3-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd6a3-154">Entry</span></span> | <span data-ttu-id="cd6a3-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6a3-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd6a3-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd6a3-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd6a3-158">System-Only</span></span>            | <span data-ttu-id="cd6a3-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-159">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd6a3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cd6a3-161">True</span><span class="sxs-lookup"><span data-stu-id="cd6a3-161">True</span></span>                                                               |
| <span data-ttu-id="cd6a3-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd6a3-162">Is Indexed</span></span>             | <span data-ttu-id="cd6a3-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-163">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd6a3-164">In Global Catalog</span></span>      | <span data-ttu-id="cd6a3-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-165">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd6a3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd6a3-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd6a3-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd6a3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd6a3-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd6a3-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-170">Search-Flags</span></span>           | <span data-ttu-id="cd6a3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd6a3-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd6a3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-172">System-Flags</span></span>           | <span data-ttu-id="cd6a3-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd6a3-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd6a3-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd6a3-174">Classes used in</span></span>        | [<span data-ttu-id="cd6a3-175">**MS-WMI-PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-175">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd6a3-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd6a3-176">Windows Server 2008</span></span>



| <span data-ttu-id="cd6a3-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd6a3-177">Entry</span></span> | <span data-ttu-id="cd6a3-178">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6a3-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd6a3-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd6a3-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd6a3-181">System-Only</span></span>            | <span data-ttu-id="cd6a3-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-182">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd6a3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cd6a3-184">True</span><span class="sxs-lookup"><span data-stu-id="cd6a3-184">True</span></span>                                                               |
| <span data-ttu-id="cd6a3-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd6a3-185">Is Indexed</span></span>             | <span data-ttu-id="cd6a3-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-186">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd6a3-187">In Global Catalog</span></span>      | <span data-ttu-id="cd6a3-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-188">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd6a3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd6a3-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd6a3-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd6a3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd6a3-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd6a3-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-193">Search-Flags</span></span>           | <span data-ttu-id="cd6a3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd6a3-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd6a3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-195">System-Flags</span></span>           | <span data-ttu-id="cd6a3-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd6a3-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd6a3-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd6a3-197">Classes used in</span></span>        | [<span data-ttu-id="cd6a3-198">**MS-WMI-PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-198">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd6a3-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd6a3-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd6a3-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd6a3-200">Entry</span></span> | <span data-ttu-id="cd6a3-201">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6a3-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd6a3-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd6a3-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd6a3-204">System-Only</span></span>            | <span data-ttu-id="cd6a3-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-205">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd6a3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cd6a3-207">True</span><span class="sxs-lookup"><span data-stu-id="cd6a3-207">True</span></span>                                                               |
| <span data-ttu-id="cd6a3-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd6a3-208">Is Indexed</span></span>             | <span data-ttu-id="cd6a3-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-209">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd6a3-210">In Global Catalog</span></span>      | <span data-ttu-id="cd6a3-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-211">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd6a3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd6a3-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd6a3-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd6a3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd6a3-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd6a3-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-216">Search-Flags</span></span>           | <span data-ttu-id="cd6a3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd6a3-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd6a3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-218">System-Flags</span></span>           | <span data-ttu-id="cd6a3-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd6a3-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd6a3-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd6a3-220">Classes used in</span></span>        | [<span data-ttu-id="cd6a3-221">**MS-WMI-PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-221">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd6a3-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd6a3-222">Windows Server 2012</span></span>



| <span data-ttu-id="cd6a3-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd6a3-223">Entry</span></span> | <span data-ttu-id="cd6a3-224">Значение</span><span class="sxs-lookup"><span data-stu-id="cd6a3-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd6a3-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd6a3-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cd6a3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd6a3-227">System-Only</span></span>            | <span data-ttu-id="cd6a3-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-228">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd6a3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cd6a3-230">True</span><span class="sxs-lookup"><span data-stu-id="cd6a3-230">True</span></span>                                                               |
| <span data-ttu-id="cd6a3-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd6a3-231">Is Indexed</span></span>             | <span data-ttu-id="cd6a3-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-232">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd6a3-233">In Global Catalog</span></span>      | <span data-ttu-id="cd6a3-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd6a3-234">False</span></span>                                                              |
| <span data-ttu-id="cd6a3-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd6a3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd6a3-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd6a3-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cd6a3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd6a3-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd6a3-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cd6a3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-239">Search-Flags</span></span>           | <span data-ttu-id="cd6a3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd6a3-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="cd6a3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd6a3-241">System-Flags</span></span>           | <span data-ttu-id="cd6a3-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd6a3-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="cd6a3-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd6a3-243">Classes used in</span></span>        | [<span data-ttu-id="cd6a3-244">**MS-WMI-PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-244">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> |



 

 





