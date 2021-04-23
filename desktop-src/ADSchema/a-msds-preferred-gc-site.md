---
title: Атрибут ms-DS-предпочтителен-GC-site
description: Атрибут ms-DS-предпочтителен-GC-site используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-предпочтителен-GC-site
- msDS-предпочтительный — GC — схема AD атрибута site
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262250"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="7449a-105">Атрибут ms-DS-предпочтителен-GC-site</span><span class="sxs-lookup"><span data-stu-id="7449a-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="7449a-106">Атрибут **MS-DS-предпочтителен-GC-site** используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.</span><span class="sxs-lookup"><span data-stu-id="7449a-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="7449a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-107">Entry</span></span> | <span data-ttu-id="7449a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7449a-109">CN</span><span class="sxs-lookup"><span data-stu-id="7449a-109">CN</span></span>                | <span data-ttu-id="7449a-110">MS-DS-предпочтительный — GC-site</span><span class="sxs-lookup"><span data-stu-id="7449a-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="7449a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7449a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7449a-112">msDS-предпочтителен — GC-site</span><span class="sxs-lookup"><span data-stu-id="7449a-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="7449a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7449a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7449a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7449a-114">Update Privilege</span></span>  | <span data-ttu-id="7449a-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="7449a-115">Domain administrator</span></span>                    |
| <span data-ttu-id="7449a-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7449a-116">Update Frequency</span></span>  | <span data-ttu-id="7449a-117">По усмотрению администратора.</span><span class="sxs-lookup"><span data-stu-id="7449a-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="7449a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-118">Attribute-Id</span></span>      | <span data-ttu-id="7449a-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="7449a-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="7449a-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7449a-120">System-Id-Guid</span></span>    | <span data-ttu-id="7449a-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="7449a-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="7449a-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7449a-122">Syntax</span></span>            | [<span data-ttu-id="7449a-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7449a-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7449a-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7449a-124">Implementations</span></span>

-   [<span data-ttu-id="7449a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7449a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7449a-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7449a-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7449a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7449a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7449a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7449a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7449a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7449a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7449a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7449a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7449a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7449a-131">Windows Server 2003</span></span>



| <span data-ttu-id="7449a-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-132">Entry</span></span> | <span data-ttu-id="7449a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7449a-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7449a-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7449a-136">System-Only</span></span>            | <span data-ttu-id="7449a-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-137">False</span></span>                                                       |
| <span data-ttu-id="7449a-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7449a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7449a-139">True</span><span class="sxs-lookup"><span data-stu-id="7449a-139">True</span></span>                                                        |
| <span data-ttu-id="7449a-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7449a-140">Is Indexed</span></span>             | <span data-ttu-id="7449a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-141">False</span></span>                                                       |
| <span data-ttu-id="7449a-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7449a-142">In Global Catalog</span></span>      | <span data-ttu-id="7449a-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-143">False</span></span>                                                       |
| <span data-ttu-id="7449a-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7449a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7449a-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7449a-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7449a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7449a-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7449a-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-148">Search-Flags</span></span>           | <span data-ttu-id="7449a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7449a-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="7449a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-150">System-Flags</span></span>           | <span data-ttu-id="7449a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7449a-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="7449a-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7449a-152">Classes used in</span></span>        | [<span data-ttu-id="7449a-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7449a-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7449a-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="7449a-154">ADAM</span></span>



| <span data-ttu-id="7449a-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-155">Entry</span></span> | <span data-ttu-id="7449a-156">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7449a-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7449a-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7449a-159">System-Only</span></span>            | <span data-ttu-id="7449a-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-160">False</span></span>                                                       |
| <span data-ttu-id="7449a-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7449a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7449a-162">True</span><span class="sxs-lookup"><span data-stu-id="7449a-162">True</span></span>                                                        |
| <span data-ttu-id="7449a-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7449a-163">Is Indexed</span></span>             | <span data-ttu-id="7449a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-164">False</span></span>                                                       |
| <span data-ttu-id="7449a-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7449a-165">In Global Catalog</span></span>      | <span data-ttu-id="7449a-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-166">False</span></span>                                                       |
| <span data-ttu-id="7449a-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7449a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7449a-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7449a-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7449a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7449a-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7449a-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-171">Search-Flags</span></span>           | <span data-ttu-id="7449a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7449a-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="7449a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-173">System-Flags</span></span>           | <span data-ttu-id="7449a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7449a-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="7449a-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7449a-175">Classes used in</span></span>        | [<span data-ttu-id="7449a-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7449a-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7449a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7449a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7449a-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-178">Entry</span></span> | <span data-ttu-id="7449a-179">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7449a-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7449a-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7449a-182">System-Only</span></span>            | <span data-ttu-id="7449a-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-183">False</span></span>                                                       |
| <span data-ttu-id="7449a-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7449a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7449a-185">True</span><span class="sxs-lookup"><span data-stu-id="7449a-185">True</span></span>                                                        |
| <span data-ttu-id="7449a-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7449a-186">Is Indexed</span></span>             | <span data-ttu-id="7449a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-187">False</span></span>                                                       |
| <span data-ttu-id="7449a-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7449a-188">In Global Catalog</span></span>      | <span data-ttu-id="7449a-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-189">False</span></span>                                                       |
| <span data-ttu-id="7449a-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7449a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7449a-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7449a-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7449a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7449a-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7449a-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-194">Search-Flags</span></span>           | <span data-ttu-id="7449a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7449a-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="7449a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-196">System-Flags</span></span>           | <span data-ttu-id="7449a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7449a-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="7449a-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7449a-198">Classes used in</span></span>        | [<span data-ttu-id="7449a-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7449a-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7449a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7449a-200">Windows Server 2008</span></span>



| <span data-ttu-id="7449a-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-201">Entry</span></span> | <span data-ttu-id="7449a-202">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7449a-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7449a-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7449a-205">System-Only</span></span>            | <span data-ttu-id="7449a-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-206">False</span></span>                                                       |
| <span data-ttu-id="7449a-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7449a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7449a-208">True</span><span class="sxs-lookup"><span data-stu-id="7449a-208">True</span></span>                                                        |
| <span data-ttu-id="7449a-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7449a-209">Is Indexed</span></span>             | <span data-ttu-id="7449a-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-210">False</span></span>                                                       |
| <span data-ttu-id="7449a-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7449a-211">In Global Catalog</span></span>      | <span data-ttu-id="7449a-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-212">False</span></span>                                                       |
| <span data-ttu-id="7449a-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7449a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7449a-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7449a-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7449a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7449a-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7449a-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-217">Search-Flags</span></span>           | <span data-ttu-id="7449a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7449a-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="7449a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-219">System-Flags</span></span>           | <span data-ttu-id="7449a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7449a-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="7449a-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7449a-221">Classes used in</span></span>        | [<span data-ttu-id="7449a-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7449a-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7449a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7449a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7449a-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-224">Entry</span></span> | <span data-ttu-id="7449a-225">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7449a-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7449a-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7449a-228">System-Only</span></span>            | <span data-ttu-id="7449a-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-229">False</span></span>                                                       |
| <span data-ttu-id="7449a-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7449a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7449a-231">True</span><span class="sxs-lookup"><span data-stu-id="7449a-231">True</span></span>                                                        |
| <span data-ttu-id="7449a-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7449a-232">Is Indexed</span></span>             | <span data-ttu-id="7449a-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-233">False</span></span>                                                       |
| <span data-ttu-id="7449a-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7449a-234">In Global Catalog</span></span>      | <span data-ttu-id="7449a-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-235">False</span></span>                                                       |
| <span data-ttu-id="7449a-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7449a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7449a-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7449a-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7449a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7449a-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7449a-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-240">Search-Flags</span></span>           | <span data-ttu-id="7449a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7449a-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="7449a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-242">System-Flags</span></span>           | <span data-ttu-id="7449a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7449a-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="7449a-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7449a-244">Classes used in</span></span>        | [<span data-ttu-id="7449a-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7449a-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7449a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7449a-246">Windows Server 2012</span></span>



| <span data-ttu-id="7449a-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="7449a-247">Entry</span></span> | <span data-ttu-id="7449a-248">Значение</span><span class="sxs-lookup"><span data-stu-id="7449a-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7449a-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7449a-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7449a-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7449a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7449a-251">System-Only</span></span>            | <span data-ttu-id="7449a-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-252">False</span></span>                                                       |
| <span data-ttu-id="7449a-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7449a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7449a-254">True</span><span class="sxs-lookup"><span data-stu-id="7449a-254">True</span></span>                                                        |
| <span data-ttu-id="7449a-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7449a-255">Is Indexed</span></span>             | <span data-ttu-id="7449a-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-256">False</span></span>                                                       |
| <span data-ttu-id="7449a-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7449a-257">In Global Catalog</span></span>      | <span data-ttu-id="7449a-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="7449a-258">False</span></span>                                                       |
| <span data-ttu-id="7449a-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7449a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7449a-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7449a-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7449a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7449a-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7449a-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7449a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-263">Search-Flags</span></span>           | <span data-ttu-id="7449a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7449a-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="7449a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7449a-265">System-Flags</span></span>           | <span data-ttu-id="7449a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7449a-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="7449a-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7449a-267">Classes used in</span></span>        | [<span data-ttu-id="7449a-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7449a-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





