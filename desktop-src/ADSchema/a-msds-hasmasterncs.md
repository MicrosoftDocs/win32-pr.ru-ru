---
title: Атрибут ms-DS-содержит-Master-NC
description: Содержит контексты именования, удерживаемые контроллером домена. Этот атрибут не является устаревшим с-Master-NC.
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов Active-DS-Schema-Master-NC
- Схема AD атрибута msDS-Хасмастернкс
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893842"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="8b941-106">Атрибут ms-DS-содержит-Master-NC</span><span class="sxs-lookup"><span data-stu-id="8b941-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="8b941-107">Содержит контексты именования, удерживаемые контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="8b941-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="8b941-108">Этот атрибут не является устаревшим с-Master-NC.</span><span class="sxs-lookup"><span data-stu-id="8b941-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="8b941-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-109">Entry</span></span> | <span data-ttu-id="8b941-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8b941-111">CN</span><span class="sxs-lookup"><span data-stu-id="8b941-111">CN</span></span>                | <span data-ttu-id="8b941-112">MS-DS-содержит-Master-NC</span><span class="sxs-lookup"><span data-stu-id="8b941-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="8b941-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8b941-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8b941-114">msDS-Хасмастернкс</span><span class="sxs-lookup"><span data-stu-id="8b941-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="8b941-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8b941-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="8b941-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8b941-116">Update Privilege</span></span>  | <span data-ttu-id="8b941-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="8b941-117">This value is set by the system</span></span>         |
| <span data-ttu-id="8b941-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8b941-118">Update Frequency</span></span>  | <span data-ttu-id="8b941-119">При каждом создании нового контекста именования.</span><span class="sxs-lookup"><span data-stu-id="8b941-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="8b941-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-120">Attribute-Id</span></span>      | <span data-ttu-id="8b941-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="8b941-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="8b941-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8b941-122">System-Id-Guid</span></span>    | <span data-ttu-id="8b941-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="8b941-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="8b941-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b941-124">Syntax</span></span>            | [<span data-ttu-id="8b941-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8b941-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="8b941-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8b941-126">Implementations</span></span>

-   [<span data-ttu-id="8b941-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b941-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b941-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8b941-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8b941-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b941-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b941-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b941-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b941-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b941-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b941-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b941-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8b941-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b941-133">Windows Server 2003</span></span>



| <span data-ttu-id="8b941-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-134">Entry</span></span> | <span data-ttu-id="8b941-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b941-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b941-136">Link-Id</span></span>                | <span data-ttu-id="8b941-137">2036</span><span class="sxs-lookup"><span data-stu-id="8b941-137">2036</span></span>                                     |
| <span data-ttu-id="8b941-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b941-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b941-139">System-Only</span></span>            | <span data-ttu-id="8b941-140">True</span><span class="sxs-lookup"><span data-stu-id="8b941-140">True</span></span>                                     |
| <span data-ttu-id="8b941-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b941-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8b941-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-142">False</span></span>                                    |
| <span data-ttu-id="8b941-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b941-143">Is Indexed</span></span>             | <span data-ttu-id="8b941-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-144">False</span></span>                                    |
| <span data-ttu-id="8b941-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b941-145">In Global Catalog</span></span>      | <span data-ttu-id="8b941-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-146">False</span></span>                                    |
| <span data-ttu-id="8b941-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b941-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b941-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b941-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b941-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b941-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b941-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b941-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b941-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-151">Search-Flags</span></span>           | <span data-ttu-id="8b941-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b941-152">0x00000000</span></span>                               |
| <span data-ttu-id="8b941-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-153">System-Flags</span></span>           | <span data-ttu-id="8b941-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b941-154">0x00000010</span></span>                               |
| <span data-ttu-id="8b941-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b941-155">Classes used in</span></span>        | [<span data-ttu-id="8b941-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b941-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8b941-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="8b941-157">ADAM</span></span>



| <span data-ttu-id="8b941-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-158">Entry</span></span> | <span data-ttu-id="8b941-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b941-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b941-160">Link-Id</span></span>                | <span data-ttu-id="8b941-161">2036</span><span class="sxs-lookup"><span data-stu-id="8b941-161">2036</span></span>                                     |
| <span data-ttu-id="8b941-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b941-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b941-163">System-Only</span></span>            | <span data-ttu-id="8b941-164">True</span><span class="sxs-lookup"><span data-stu-id="8b941-164">True</span></span>                                     |
| <span data-ttu-id="8b941-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b941-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8b941-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-166">False</span></span>                                    |
| <span data-ttu-id="8b941-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b941-167">Is Indexed</span></span>             | <span data-ttu-id="8b941-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-168">False</span></span>                                    |
| <span data-ttu-id="8b941-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b941-169">In Global Catalog</span></span>      | <span data-ttu-id="8b941-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-170">False</span></span>                                    |
| <span data-ttu-id="8b941-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b941-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b941-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b941-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b941-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b941-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b941-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b941-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b941-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-175">Search-Flags</span></span>           | <span data-ttu-id="8b941-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b941-176">0x00000000</span></span>                               |
| <span data-ttu-id="8b941-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-177">System-Flags</span></span>           | <span data-ttu-id="8b941-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b941-178">0x00000010</span></span>                               |
| <span data-ttu-id="8b941-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b941-179">Classes used in</span></span>        | [<span data-ttu-id="8b941-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b941-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b941-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b941-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b941-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-182">Entry</span></span> | <span data-ttu-id="8b941-183">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b941-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b941-184">Link-Id</span></span>                | <span data-ttu-id="8b941-185">2036</span><span class="sxs-lookup"><span data-stu-id="8b941-185">2036</span></span>                                     |
| <span data-ttu-id="8b941-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b941-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b941-187">System-Only</span></span>            | <span data-ttu-id="8b941-188">True</span><span class="sxs-lookup"><span data-stu-id="8b941-188">True</span></span>                                     |
| <span data-ttu-id="8b941-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b941-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8b941-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-190">False</span></span>                                    |
| <span data-ttu-id="8b941-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b941-191">Is Indexed</span></span>             | <span data-ttu-id="8b941-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-192">False</span></span>                                    |
| <span data-ttu-id="8b941-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b941-193">In Global Catalog</span></span>      | <span data-ttu-id="8b941-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-194">False</span></span>                                    |
| <span data-ttu-id="8b941-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b941-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b941-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b941-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b941-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b941-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b941-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b941-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b941-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-199">Search-Flags</span></span>           | <span data-ttu-id="8b941-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b941-200">0x00000000</span></span>                               |
| <span data-ttu-id="8b941-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-201">System-Flags</span></span>           | <span data-ttu-id="8b941-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b941-202">0x00000010</span></span>                               |
| <span data-ttu-id="8b941-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b941-203">Classes used in</span></span>        | [<span data-ttu-id="8b941-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b941-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b941-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b941-205">Windows Server 2008</span></span>



| <span data-ttu-id="8b941-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-206">Entry</span></span> | <span data-ttu-id="8b941-207">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b941-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b941-208">Link-Id</span></span>                | <span data-ttu-id="8b941-209">2036</span><span class="sxs-lookup"><span data-stu-id="8b941-209">2036</span></span>                                     |
| <span data-ttu-id="8b941-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b941-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b941-211">System-Only</span></span>            | <span data-ttu-id="8b941-212">True</span><span class="sxs-lookup"><span data-stu-id="8b941-212">True</span></span>                                     |
| <span data-ttu-id="8b941-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b941-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8b941-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-214">False</span></span>                                    |
| <span data-ttu-id="8b941-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b941-215">Is Indexed</span></span>             | <span data-ttu-id="8b941-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-216">False</span></span>                                    |
| <span data-ttu-id="8b941-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b941-217">In Global Catalog</span></span>      | <span data-ttu-id="8b941-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-218">False</span></span>                                    |
| <span data-ttu-id="8b941-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b941-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b941-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b941-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b941-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b941-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b941-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b941-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b941-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-223">Search-Flags</span></span>           | <span data-ttu-id="8b941-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b941-224">0x00000000</span></span>                               |
| <span data-ttu-id="8b941-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-225">System-Flags</span></span>           | <span data-ttu-id="8b941-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b941-226">0x00000010</span></span>                               |
| <span data-ttu-id="8b941-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b941-227">Classes used in</span></span>        | [<span data-ttu-id="8b941-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b941-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b941-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b941-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b941-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-230">Entry</span></span> | <span data-ttu-id="8b941-231">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b941-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b941-232">Link-Id</span></span>                | <span data-ttu-id="8b941-233">2036</span><span class="sxs-lookup"><span data-stu-id="8b941-233">2036</span></span>                                     |
| <span data-ttu-id="8b941-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b941-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b941-235">System-Only</span></span>            | <span data-ttu-id="8b941-236">True</span><span class="sxs-lookup"><span data-stu-id="8b941-236">True</span></span>                                     |
| <span data-ttu-id="8b941-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b941-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8b941-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-238">False</span></span>                                    |
| <span data-ttu-id="8b941-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b941-239">Is Indexed</span></span>             | <span data-ttu-id="8b941-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-240">False</span></span>                                    |
| <span data-ttu-id="8b941-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b941-241">In Global Catalog</span></span>      | <span data-ttu-id="8b941-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-242">False</span></span>                                    |
| <span data-ttu-id="8b941-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b941-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b941-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b941-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b941-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b941-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b941-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b941-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b941-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-247">Search-Flags</span></span>           | <span data-ttu-id="8b941-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b941-248">0x00000000</span></span>                               |
| <span data-ttu-id="8b941-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-249">System-Flags</span></span>           | <span data-ttu-id="8b941-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b941-250">0x00000010</span></span>                               |
| <span data-ttu-id="8b941-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b941-251">Classes used in</span></span>        | [<span data-ttu-id="8b941-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b941-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b941-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b941-253">Windows Server 2012</span></span>



| <span data-ttu-id="8b941-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b941-254">Entry</span></span> | <span data-ttu-id="8b941-255">Значение</span><span class="sxs-lookup"><span data-stu-id="8b941-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8b941-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b941-256">Link-Id</span></span>                | <span data-ttu-id="8b941-257">2036</span><span class="sxs-lookup"><span data-stu-id="8b941-257">2036</span></span>                                     |
| <span data-ttu-id="8b941-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b941-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8b941-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b941-259">System-Only</span></span>            | <span data-ttu-id="8b941-260">True</span><span class="sxs-lookup"><span data-stu-id="8b941-260">True</span></span>                                     |
| <span data-ttu-id="8b941-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b941-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8b941-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-262">False</span></span>                                    |
| <span data-ttu-id="8b941-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b941-263">Is Indexed</span></span>             | <span data-ttu-id="8b941-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-264">False</span></span>                                    |
| <span data-ttu-id="8b941-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b941-265">In Global Catalog</span></span>      | <span data-ttu-id="8b941-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b941-266">False</span></span>                                    |
| <span data-ttu-id="8b941-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b941-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b941-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b941-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8b941-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b941-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8b941-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b941-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8b941-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-271">Search-Flags</span></span>           | <span data-ttu-id="8b941-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b941-272">0x00000000</span></span>                               |
| <span data-ttu-id="8b941-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b941-273">System-Flags</span></span>           | <span data-ttu-id="8b941-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b941-274">0x00000010</span></span>                               |
| <span data-ttu-id="8b941-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b941-275">Classes used in</span></span>        | [<span data-ttu-id="8b941-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8b941-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





