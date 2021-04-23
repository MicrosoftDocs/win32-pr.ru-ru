---
title: Атрибут содержит-Master-NC
description: Различающееся имя контекста именования для контроллера домена. Прямая ссылка на атрибут Mastered-By.
ms.assetid: 77a7e693-513f-4f76-8c4f-d2ef3240323b
ms.tgt_platform: multiple
keywords:
- Схема Active Directory с атрибутом NC
- Схема AD атрибута Хасмастернкс
topic_type:
- apiref
api_name:
- Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34756c491c5228c58da1b95d4fd7b838c691f38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989737"
---
# <a name="has-master-ncs-attribute"></a><span data-ttu-id="edf38-106">Атрибут содержит-Master-NC</span><span class="sxs-lookup"><span data-stu-id="edf38-106">Has-Master-NCs attribute</span></span>

<span data-ttu-id="edf38-107">Различающееся имя контекста именования для контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="edf38-107">The distinguished name for the naming contexts for the DC.</span></span> <span data-ttu-id="edf38-108">Прямая ссылка на атрибут Mastered-By.</span><span class="sxs-lookup"><span data-stu-id="edf38-108">Forward link for the Mastered-By attribute.</span></span>



| <span data-ttu-id="edf38-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-109">Entry</span></span> | <span data-ttu-id="edf38-110">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="edf38-111">CN</span><span class="sxs-lookup"><span data-stu-id="edf38-111">CN</span></span>                | <span data-ttu-id="edf38-112">Содержит-Master-NC</span><span class="sxs-lookup"><span data-stu-id="edf38-112">Has-Master-NCs</span></span>                          |
| <span data-ttu-id="edf38-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="edf38-113">Ldap-Display-Name</span></span> | <span data-ttu-id="edf38-114">хасмастернкс</span><span class="sxs-lookup"><span data-stu-id="edf38-114">hasMasterNCs</span></span>                            |
| <span data-ttu-id="edf38-115">Размер</span><span class="sxs-lookup"><span data-stu-id="edf38-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="edf38-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="edf38-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="edf38-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="edf38-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="edf38-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-118">Attribute-Id</span></span>      | <span data-ttu-id="edf38-119">1.2.840.113556.1.2.14</span><span class="sxs-lookup"><span data-stu-id="edf38-119">1.2.840.113556.1.2.14</span></span>                   |
| <span data-ttu-id="edf38-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="edf38-120">System-Id-Guid</span></span>    | <span data-ttu-id="edf38-121">bf967982-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="edf38-121">bf967982-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="edf38-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edf38-122">Syntax</span></span>            | [<span data-ttu-id="edf38-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="edf38-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="edf38-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="edf38-124">Implementations</span></span>

-   [<span data-ttu-id="edf38-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="edf38-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="edf38-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="edf38-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="edf38-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="edf38-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="edf38-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="edf38-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="edf38-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="edf38-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="edf38-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="edf38-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="edf38-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="edf38-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="edf38-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edf38-132">Windows 2000 Server</span></span>



| <span data-ttu-id="edf38-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-133">Entry</span></span> | <span data-ttu-id="edf38-134">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-135">Link-Id</span></span>                | <span data-ttu-id="edf38-136">76</span><span class="sxs-lookup"><span data-stu-id="edf38-136">76</span></span>                                       |
| <span data-ttu-id="edf38-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-137">MAPI-Id</span></span>                | <span data-ttu-id="edf38-138">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-138">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-139">System-Only</span></span>            | <span data-ttu-id="edf38-140">True</span><span class="sxs-lookup"><span data-stu-id="edf38-140">True</span></span>                                     |
| <span data-ttu-id="edf38-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-141">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-142">False</span></span>                                    |
| <span data-ttu-id="edf38-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-143">Is Indexed</span></span>             | <span data-ttu-id="edf38-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-144">False</span></span>                                    |
| <span data-ttu-id="edf38-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-145">In Global Catalog</span></span>      | <span data-ttu-id="edf38-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-146">False</span></span>                                    |
| <span data-ttu-id="edf38-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-151">Search-Flags</span></span>           | <span data-ttu-id="edf38-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-152">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-153">System-Flags</span></span>           | <span data-ttu-id="edf38-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-154">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-155">Classes used in</span></span>        | [<span data-ttu-id="edf38-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="edf38-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="edf38-157">Windows Server 2003</span></span>



| <span data-ttu-id="edf38-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-158">Entry</span></span> | <span data-ttu-id="edf38-159">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-160">Link-Id</span></span>                | <span data-ttu-id="edf38-161">76</span><span class="sxs-lookup"><span data-stu-id="edf38-161">76</span></span>                                       |
| <span data-ttu-id="edf38-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-162">MAPI-Id</span></span>                | <span data-ttu-id="edf38-163">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-163">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-164">System-Only</span></span>            | <span data-ttu-id="edf38-165">True</span><span class="sxs-lookup"><span data-stu-id="edf38-165">True</span></span>                                     |
| <span data-ttu-id="edf38-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-166">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-167">False</span></span>                                    |
| <span data-ttu-id="edf38-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-168">Is Indexed</span></span>             | <span data-ttu-id="edf38-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-169">False</span></span>                                    |
| <span data-ttu-id="edf38-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-170">In Global Catalog</span></span>      | <span data-ttu-id="edf38-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-171">False</span></span>                                    |
| <span data-ttu-id="edf38-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-176">Search-Flags</span></span>           | <span data-ttu-id="edf38-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-177">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-178">System-Flags</span></span>           | <span data-ttu-id="edf38-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-179">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-180">Classes used in</span></span>        | [<span data-ttu-id="edf38-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="edf38-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="edf38-182">ADAM</span></span>



| <span data-ttu-id="edf38-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-183">Entry</span></span> | <span data-ttu-id="edf38-184">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-185">Link-Id</span></span>                | <span data-ttu-id="edf38-186">76</span><span class="sxs-lookup"><span data-stu-id="edf38-186">76</span></span>                                       |
| <span data-ttu-id="edf38-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-187">MAPI-Id</span></span>                | <span data-ttu-id="edf38-188">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-188">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-189">System-Only</span></span>            | <span data-ttu-id="edf38-190">True</span><span class="sxs-lookup"><span data-stu-id="edf38-190">True</span></span>                                     |
| <span data-ttu-id="edf38-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-191">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-192">False</span></span>                                    |
| <span data-ttu-id="edf38-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-193">Is Indexed</span></span>             | <span data-ttu-id="edf38-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-194">False</span></span>                                    |
| <span data-ttu-id="edf38-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-195">In Global Catalog</span></span>      | <span data-ttu-id="edf38-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-196">False</span></span>                                    |
| <span data-ttu-id="edf38-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-201">Search-Flags</span></span>           | <span data-ttu-id="edf38-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-202">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-203">System-Flags</span></span>           | <span data-ttu-id="edf38-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-204">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-205">Classes used in</span></span>        | [<span data-ttu-id="edf38-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="edf38-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="edf38-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="edf38-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-208">Entry</span></span> | <span data-ttu-id="edf38-209">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-210">Link-Id</span></span>                | <span data-ttu-id="edf38-211">76</span><span class="sxs-lookup"><span data-stu-id="edf38-211">76</span></span>                                       |
| <span data-ttu-id="edf38-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-212">MAPI-Id</span></span>                | <span data-ttu-id="edf38-213">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-213">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-214">System-Only</span></span>            | <span data-ttu-id="edf38-215">True</span><span class="sxs-lookup"><span data-stu-id="edf38-215">True</span></span>                                     |
| <span data-ttu-id="edf38-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-216">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-217">False</span></span>                                    |
| <span data-ttu-id="edf38-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-218">Is Indexed</span></span>             | <span data-ttu-id="edf38-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-219">False</span></span>                                    |
| <span data-ttu-id="edf38-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-220">In Global Catalog</span></span>      | <span data-ttu-id="edf38-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-221">False</span></span>                                    |
| <span data-ttu-id="edf38-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-226">Search-Flags</span></span>           | <span data-ttu-id="edf38-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-227">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-228">System-Flags</span></span>           | <span data-ttu-id="edf38-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-229">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-230">Classes used in</span></span>        | [<span data-ttu-id="edf38-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="edf38-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edf38-232">Windows Server 2008</span></span>



| <span data-ttu-id="edf38-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-233">Entry</span></span> | <span data-ttu-id="edf38-234">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-235">Link-Id</span></span>                | <span data-ttu-id="edf38-236">76</span><span class="sxs-lookup"><span data-stu-id="edf38-236">76</span></span>                                       |
| <span data-ttu-id="edf38-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-237">MAPI-Id</span></span>                | <span data-ttu-id="edf38-238">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-238">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-239">System-Only</span></span>            | <span data-ttu-id="edf38-240">True</span><span class="sxs-lookup"><span data-stu-id="edf38-240">True</span></span>                                     |
| <span data-ttu-id="edf38-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-241">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-242">False</span></span>                                    |
| <span data-ttu-id="edf38-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-243">Is Indexed</span></span>             | <span data-ttu-id="edf38-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-244">False</span></span>                                    |
| <span data-ttu-id="edf38-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-245">In Global Catalog</span></span>      | <span data-ttu-id="edf38-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-246">False</span></span>                                    |
| <span data-ttu-id="edf38-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-251">Search-Flags</span></span>           | <span data-ttu-id="edf38-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-252">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-253">System-Flags</span></span>           | <span data-ttu-id="edf38-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-254">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-255">Classes used in</span></span>        | [<span data-ttu-id="edf38-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="edf38-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="edf38-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="edf38-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-258">Entry</span></span> | <span data-ttu-id="edf38-259">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-260">Link-Id</span></span>                | <span data-ttu-id="edf38-261">76</span><span class="sxs-lookup"><span data-stu-id="edf38-261">76</span></span>                                       |
| <span data-ttu-id="edf38-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-262">MAPI-Id</span></span>                | <span data-ttu-id="edf38-263">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-263">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-264">System-Only</span></span>            | <span data-ttu-id="edf38-265">True</span><span class="sxs-lookup"><span data-stu-id="edf38-265">True</span></span>                                     |
| <span data-ttu-id="edf38-266">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-266">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-267">False</span></span>                                    |
| <span data-ttu-id="edf38-268">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-268">Is Indexed</span></span>             | <span data-ttu-id="edf38-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-269">False</span></span>                                    |
| <span data-ttu-id="edf38-270">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-270">In Global Catalog</span></span>      | <span data-ttu-id="edf38-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-271">False</span></span>                                    |
| <span data-ttu-id="edf38-272">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-273">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-276">Search-Flags</span></span>           | <span data-ttu-id="edf38-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-277">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-278">System-Flags</span></span>           | <span data-ttu-id="edf38-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-279">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-280">Classes used in</span></span>        | [<span data-ttu-id="edf38-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="edf38-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edf38-282">Windows Server 2012</span></span>



| <span data-ttu-id="edf38-283">Ввод</span><span class="sxs-lookup"><span data-stu-id="edf38-283">Entry</span></span> | <span data-ttu-id="edf38-284">Значение</span><span class="sxs-lookup"><span data-stu-id="edf38-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="edf38-285">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="edf38-285">Link-Id</span></span>                | <span data-ttu-id="edf38-286">76</span><span class="sxs-lookup"><span data-stu-id="edf38-286">76</span></span>                                       |
| <span data-ttu-id="edf38-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edf38-287">MAPI-Id</span></span>                | <span data-ttu-id="edf38-288">0x80B6</span><span class="sxs-lookup"><span data-stu-id="edf38-288">0x80B6</span></span>                                   |
| <span data-ttu-id="edf38-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="edf38-289">System-Only</span></span>            | <span data-ttu-id="edf38-290">True</span><span class="sxs-lookup"><span data-stu-id="edf38-290">True</span></span>                                     |
| <span data-ttu-id="edf38-291">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="edf38-291">Is-Single-Valued</span></span>       | <span data-ttu-id="edf38-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-292">False</span></span>                                    |
| <span data-ttu-id="edf38-293">Индексируется</span><span class="sxs-lookup"><span data-stu-id="edf38-293">Is Indexed</span></span>             | <span data-ttu-id="edf38-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-294">False</span></span>                                    |
| <span data-ttu-id="edf38-295">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="edf38-295">In Global Catalog</span></span>      | <span data-ttu-id="edf38-296">Неверно</span><span class="sxs-lookup"><span data-stu-id="edf38-296">False</span></span>                                    |
| <span data-ttu-id="edf38-297">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="edf38-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="edf38-298">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="edf38-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="edf38-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edf38-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="edf38-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edf38-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="edf38-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-301">Search-Flags</span></span>           | <span data-ttu-id="edf38-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edf38-302">0x00000000</span></span>                               |
| <span data-ttu-id="edf38-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edf38-303">System-Flags</span></span>           | <span data-ttu-id="edf38-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edf38-304">0x00000010</span></span>                               |
| <span data-ttu-id="edf38-305">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="edf38-305">Classes used in</span></span>        | [<span data-ttu-id="edf38-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="edf38-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





