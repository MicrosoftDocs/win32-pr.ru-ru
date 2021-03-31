---
title: Параметр запроса — атрибут объекта
description: Ссылка на Query-Policy по умолчанию для этого сервера.
ms.assetid: 5a492305-ac57-4331-b96b-bdd8107d4a4d
ms.tgt_platform: multiple
keywords:
- "\"Запрос — политика\" — схема AD атрибута объекта"
- Схема AD атрибута Куериполициобжект
topic_type:
- apiref
api_name:
- Query-Policy-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e33bc2840fb1ca8a936b417c4407f48fcdf7f46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804289"
---
# <a name="query-policy-object-attribute"></a><span data-ttu-id="8c03c-105">Параметр запроса — атрибут объекта</span><span class="sxs-lookup"><span data-stu-id="8c03c-105">Query-Policy-Object attribute</span></span>

<span data-ttu-id="8c03c-106">Ссылка на Query-Policy по умолчанию для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="8c03c-106">Reference to the default Query-Policy in force for this server.</span></span>



| <span data-ttu-id="8c03c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-107">Entry</span></span> | <span data-ttu-id="8c03c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8c03c-109">CN</span><span class="sxs-lookup"><span data-stu-id="8c03c-109">CN</span></span>                | <span data-ttu-id="8c03c-110">Запрос — политика — объект</span><span class="sxs-lookup"><span data-stu-id="8c03c-110">Query-Policy-Object</span></span>                     |
| <span data-ttu-id="8c03c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8c03c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8c03c-112">куериполициобжект</span><span class="sxs-lookup"><span data-stu-id="8c03c-112">queryPolicyObject</span></span>                       |
| <span data-ttu-id="8c03c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8c03c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="8c03c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8c03c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="8c03c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8c03c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="8c03c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-116">Attribute-Id</span></span>      | <span data-ttu-id="8c03c-117">1.2.840.113556.1.4.607</span><span class="sxs-lookup"><span data-stu-id="8c03c-117">1.2.840.113556.1.4.607</span></span>                  |
| <span data-ttu-id="8c03c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8c03c-118">System-Id-Guid</span></span>    | <span data-ttu-id="8c03c-119">e1aea403-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8c03c-119">e1aea403-cd5b-11d0-afff-0000f80367c1</span></span>    |
| <span data-ttu-id="8c03c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c03c-120">Syntax</span></span>            | [<span data-ttu-id="8c03c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8c03c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="8c03c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8c03c-122">Implementations</span></span>

-   [<span data-ttu-id="8c03c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8c03c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8c03c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8c03c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8c03c-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8c03c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8c03c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8c03c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8c03c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8c03c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8c03c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8c03c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8c03c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8c03c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8c03c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c03c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8c03c-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-131">Entry</span></span> | <span data-ttu-id="8c03c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-133">Link-Id</span></span>                | <span data-ttu-id="8c03c-134">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-134">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-135">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-136">System-Only</span></span>            | <span data-ttu-id="8c03c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-137">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-139">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-139">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-140">Is Indexed</span></span>             | <span data-ttu-id="8c03c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-141">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-142">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-143">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-145">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-146">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-147">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-148">Search-Flags</span></span>           | <span data-ttu-id="8c03c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-149">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-150">System-Flags</span></span>           | <span data-ttu-id="8c03c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-151">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-152">Classes used in</span></span>        | [<span data-ttu-id="8c03c-153">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-153">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-154">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-154">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8c03c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c03c-155">Windows Server 2003</span></span>



| <span data-ttu-id="8c03c-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-156">Entry</span></span> | <span data-ttu-id="8c03c-157">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-158">Link-Id</span></span>                | <span data-ttu-id="8c03c-159">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-159">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-161">System-Only</span></span>            | <span data-ttu-id="8c03c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-162">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-164">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-164">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-165">Is Indexed</span></span>             | <span data-ttu-id="8c03c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-166">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-167">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-168">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-173">Search-Flags</span></span>           | <span data-ttu-id="8c03c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-175">System-Flags</span></span>           | <span data-ttu-id="8c03c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-177">Classes used in</span></span>        | [<span data-ttu-id="8c03c-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-179">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-179">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8c03c-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="8c03c-180">ADAM</span></span>



| <span data-ttu-id="8c03c-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-181">Entry</span></span> | <span data-ttu-id="8c03c-182">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-183">Link-Id</span></span>                | <span data-ttu-id="8c03c-184">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-184">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-185">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-186">System-Only</span></span>            | <span data-ttu-id="8c03c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-187">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-189">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-189">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-190">Is Indexed</span></span>             | <span data-ttu-id="8c03c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-191">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-192">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-193">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-195">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-196">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-197">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-198">Search-Flags</span></span>           | <span data-ttu-id="8c03c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-199">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-200">System-Flags</span></span>           | <span data-ttu-id="8c03c-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-201">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-202">Classes used in</span></span>        | [<span data-ttu-id="8c03c-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-204">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-204">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8c03c-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8c03c-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8c03c-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-206">Entry</span></span> | <span data-ttu-id="8c03c-207">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-207">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-208">Link-Id</span></span>                | <span data-ttu-id="8c03c-209">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-209">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-210">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-211">System-Only</span></span>            | <span data-ttu-id="8c03c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-212">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-214">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-214">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-215">Is Indexed</span></span>             | <span data-ttu-id="8c03c-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-216">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-217">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-218">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-220">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-221">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-222">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-223">Search-Flags</span></span>           | <span data-ttu-id="8c03c-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-224">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-225">System-Flags</span></span>           | <span data-ttu-id="8c03c-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-226">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-227">Classes used in</span></span>        | [<span data-ttu-id="8c03c-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-229">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-229">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8c03c-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c03c-230">Windows Server 2008</span></span>



| <span data-ttu-id="8c03c-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-231">Entry</span></span> | <span data-ttu-id="8c03c-232">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-233">Link-Id</span></span>                | <span data-ttu-id="8c03c-234">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-234">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-235">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-236">System-Only</span></span>            | <span data-ttu-id="8c03c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-237">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-239">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-239">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-240">Is Indexed</span></span>             | <span data-ttu-id="8c03c-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-241">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-242">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-243">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-245">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-246">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-247">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-248">Search-Flags</span></span>           | <span data-ttu-id="8c03c-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-249">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-250">System-Flags</span></span>           | <span data-ttu-id="8c03c-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-251">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-252">Classes used in</span></span>        | [<span data-ttu-id="8c03c-253">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-253">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-254">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-254">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8c03c-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c03c-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8c03c-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-256">Entry</span></span> | <span data-ttu-id="8c03c-257">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-257">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-258">Link-Id</span></span>                | <span data-ttu-id="8c03c-259">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-259">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-260">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-261">System-Only</span></span>            | <span data-ttu-id="8c03c-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-262">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-263">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-264">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-264">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-265">Is Indexed</span></span>             | <span data-ttu-id="8c03c-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-266">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-267">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-268">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-270">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-271">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-272">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-273">Search-Flags</span></span>           | <span data-ttu-id="8c03c-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-274">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-275">System-Flags</span></span>           | <span data-ttu-id="8c03c-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-276">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-277">Classes used in</span></span>        | [<span data-ttu-id="8c03c-278">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-278">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-279">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-279">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8c03c-280">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c03c-280">Windows Server 2012</span></span>



| <span data-ttu-id="8c03c-281">Ввод</span><span class="sxs-lookup"><span data-stu-id="8c03c-281">Entry</span></span> | <span data-ttu-id="8c03c-282">Значение</span><span class="sxs-lookup"><span data-stu-id="8c03c-282">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03c-283">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8c03c-283">Link-Id</span></span>                | <span data-ttu-id="8c03c-284">68</span><span class="sxs-lookup"><span data-stu-id="8c03c-284">68</span></span>                                                                                                   |
| <span data-ttu-id="8c03c-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c03c-285">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8c03c-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c03c-286">System-Only</span></span>            | <span data-ttu-id="8c03c-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-287">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-288">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8c03c-288">Is-Single-Valued</span></span>       | <span data-ttu-id="8c03c-289">True</span><span class="sxs-lookup"><span data-stu-id="8c03c-289">True</span></span>                                                                                                 |
| <span data-ttu-id="8c03c-290">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8c03c-290">Is Indexed</span></span>             | <span data-ttu-id="8c03c-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-291">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-292">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8c03c-292">In Global Catalog</span></span>      | <span data-ttu-id="8c03c-293">Неверно</span><span class="sxs-lookup"><span data-stu-id="8c03c-293">False</span></span>                                                                                                |
| <span data-ttu-id="8c03c-294">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8c03c-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c03c-295">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8c03c-295">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8c03c-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c03c-296">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-297">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c03c-297">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8c03c-298">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-298">Search-Flags</span></span>           | <span data-ttu-id="8c03c-299">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c03c-299">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8c03c-300">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c03c-300">System-Flags</span></span>           | <span data-ttu-id="8c03c-301">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c03c-301">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8c03c-302">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8c03c-302">Classes used in</span></span>        | [<span data-ttu-id="8c03c-303">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8c03c-303">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="8c03c-304">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="8c03c-304">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





