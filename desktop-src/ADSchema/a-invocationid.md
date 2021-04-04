---
title: Атрибут Invocation-Id
description: Используется для уникальной идентификации каждого каталога Microsoft Exchange Server в Организации.
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Invocation-Id
- Схема AD атрибута invocationId
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611589c466013ad46c0920a2da1e2250cf596214
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138131"
---
# <a name="invocation-id-attribute"></a><span data-ttu-id="bb40b-105">Атрибут Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-105">Invocation-Id attribute</span></span>

<span data-ttu-id="bb40b-106">Используется для уникальной идентификации каждого каталога Microsoft Exchange Server в Организации.</span><span class="sxs-lookup"><span data-stu-id="bb40b-106">Used to uniquely identify each Microsoft Exchange Server directory in the organization.</span></span>



| <span data-ttu-id="bb40b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-107">Entry</span></span> | <span data-ttu-id="bb40b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bb40b-109">CN</span><span class="sxs-lookup"><span data-stu-id="bb40b-109">CN</span></span>                | <span data-ttu-id="bb40b-110">Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-110">Invocation-Id</span></span>                                         |
| <span data-ttu-id="bb40b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bb40b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bb40b-112">invocationId</span><span class="sxs-lookup"><span data-stu-id="bb40b-112">invocationId</span></span>                                          |
| <span data-ttu-id="bb40b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="bb40b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bb40b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bb40b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="bb40b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bb40b-115">Update Frequency</span></span>  | <span data-ttu-id="bb40b-116">При установке Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bb40b-116">When the Exchange Server is installed.</span></span>                |
| <span data-ttu-id="bb40b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-117">Attribute-Id</span></span>      | <span data-ttu-id="bb40b-118">1.2.840.113556.1.2.115</span><span class="sxs-lookup"><span data-stu-id="bb40b-118">1.2.840.113556.1.2.115</span></span>                                |
| <span data-ttu-id="bb40b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bb40b-119">System-Id-Guid</span></span>    | <span data-ttu-id="bb40b-120">bf96798e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bb40b-120">bf96798e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="bb40b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb40b-121">Syntax</span></span>            | [<span data-ttu-id="bb40b-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="bb40b-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bb40b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bb40b-123">Implementations</span></span>

-   [<span data-ttu-id="bb40b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bb40b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bb40b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb40b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb40b-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bb40b-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bb40b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb40b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb40b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb40b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb40b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb40b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb40b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb40b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bb40b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb40b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bb40b-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-132">Entry</span></span> | <span data-ttu-id="bb40b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-135">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-136">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-136">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-137">System-Only</span></span>            | <span data-ttu-id="bb40b-138">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-138">True</span></span>                                     |
| <span data-ttu-id="bb40b-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-140">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-140">True</span></span>                                     |
| <span data-ttu-id="bb40b-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-141">Is Indexed</span></span>             | <span data-ttu-id="bb40b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-142">False</span></span>                                    |
| <span data-ttu-id="bb40b-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-143">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-144">False</span></span>                                    |
| <span data-ttu-id="bb40b-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-149">Search-Flags</span></span>           | <span data-ttu-id="bb40b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb40b-150">0x00000000</span></span>                               |
| <span data-ttu-id="bb40b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-151">System-Flags</span></span>           | <span data-ttu-id="bb40b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-152">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-153">Classes used in</span></span>        | [<span data-ttu-id="bb40b-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bb40b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb40b-155">Windows Server 2003</span></span>



| <span data-ttu-id="bb40b-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-156">Entry</span></span> | <span data-ttu-id="bb40b-157">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-159">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-160">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-160">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-161">System-Only</span></span>            | <span data-ttu-id="bb40b-162">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-162">True</span></span>                                     |
| <span data-ttu-id="bb40b-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-164">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-164">True</span></span>                                     |
| <span data-ttu-id="bb40b-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-165">Is Indexed</span></span>             | <span data-ttu-id="bb40b-166">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-166">True</span></span>                                     |
| <span data-ttu-id="bb40b-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-167">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-168">False</span></span>                                    |
| <span data-ttu-id="bb40b-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-170">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-171">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-172">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-173">Search-Flags</span></span>           | <span data-ttu-id="bb40b-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb40b-174">0x00000001</span></span>                               |
| <span data-ttu-id="bb40b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-175">System-Flags</span></span>           | <span data-ttu-id="bb40b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-176">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-177">Classes used in</span></span>        | [<span data-ttu-id="bb40b-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bb40b-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="bb40b-179">ADAM</span></span>



| <span data-ttu-id="bb40b-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-180">Entry</span></span> | <span data-ttu-id="bb40b-181">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-181">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-182">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-183">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-184">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-184">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-185">System-Only</span></span>            | <span data-ttu-id="bb40b-186">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-186">True</span></span>                                     |
| <span data-ttu-id="bb40b-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-188">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-188">True</span></span>                                     |
| <span data-ttu-id="bb40b-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-189">Is Indexed</span></span>             | <span data-ttu-id="bb40b-190">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-190">True</span></span>                                     |
| <span data-ttu-id="bb40b-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-191">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-192">False</span></span>                                    |
| <span data-ttu-id="bb40b-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-194">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-195">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-196">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-197">Search-Flags</span></span>           | <span data-ttu-id="bb40b-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb40b-198">0x00000001</span></span>                               |
| <span data-ttu-id="bb40b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-199">System-Flags</span></span>           | <span data-ttu-id="bb40b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-200">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-201">Classes used in</span></span>        | [<span data-ttu-id="bb40b-202">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-202">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb40b-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb40b-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb40b-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-204">Entry</span></span> | <span data-ttu-id="bb40b-205">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-205">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-206">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-207">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-208">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-208">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-209">System-Only</span></span>            | <span data-ttu-id="bb40b-210">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-210">True</span></span>                                     |
| <span data-ttu-id="bb40b-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-212">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-212">True</span></span>                                     |
| <span data-ttu-id="bb40b-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-213">Is Indexed</span></span>             | <span data-ttu-id="bb40b-214">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-214">True</span></span>                                     |
| <span data-ttu-id="bb40b-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-215">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-216">False</span></span>                                    |
| <span data-ttu-id="bb40b-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-221">Search-Flags</span></span>           | <span data-ttu-id="bb40b-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb40b-222">0x00000001</span></span>                               |
| <span data-ttu-id="bb40b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-223">System-Flags</span></span>           | <span data-ttu-id="bb40b-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-224">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-225">Classes used in</span></span>        | [<span data-ttu-id="bb40b-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb40b-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb40b-227">Windows Server 2008</span></span>



| <span data-ttu-id="bb40b-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-228">Entry</span></span> | <span data-ttu-id="bb40b-229">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-231">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-232">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-232">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-233">System-Only</span></span>            | <span data-ttu-id="bb40b-234">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-234">True</span></span>                                     |
| <span data-ttu-id="bb40b-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-235">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-236">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-236">True</span></span>                                     |
| <span data-ttu-id="bb40b-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-237">Is Indexed</span></span>             | <span data-ttu-id="bb40b-238">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-238">True</span></span>                                     |
| <span data-ttu-id="bb40b-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-239">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-240">False</span></span>                                    |
| <span data-ttu-id="bb40b-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-245">Search-Flags</span></span>           | <span data-ttu-id="bb40b-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb40b-246">0x00000001</span></span>                               |
| <span data-ttu-id="bb40b-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-247">System-Flags</span></span>           | <span data-ttu-id="bb40b-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-248">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-249">Classes used in</span></span>        | [<span data-ttu-id="bb40b-250">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-250">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb40b-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb40b-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb40b-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-252">Entry</span></span> | <span data-ttu-id="bb40b-253">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-255">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-256">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-256">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-257">System-Only</span></span>            | <span data-ttu-id="bb40b-258">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-258">True</span></span>                                     |
| <span data-ttu-id="bb40b-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-259">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-260">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-260">True</span></span>                                     |
| <span data-ttu-id="bb40b-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-261">Is Indexed</span></span>             | <span data-ttu-id="bb40b-262">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-262">True</span></span>                                     |
| <span data-ttu-id="bb40b-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-263">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-264">False</span></span>                                    |
| <span data-ttu-id="bb40b-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-266">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-267">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-268">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-269">Search-Flags</span></span>           | <span data-ttu-id="bb40b-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb40b-270">0x00000001</span></span>                               |
| <span data-ttu-id="bb40b-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-271">System-Flags</span></span>           | <span data-ttu-id="bb40b-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-272">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-273">Classes used in</span></span>        | [<span data-ttu-id="bb40b-274">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-274">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb40b-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb40b-275">Windows Server 2012</span></span>



| <span data-ttu-id="bb40b-276">Ввод</span><span class="sxs-lookup"><span data-stu-id="bb40b-276">Entry</span></span> | <span data-ttu-id="bb40b-277">Значение</span><span class="sxs-lookup"><span data-stu-id="bb40b-277">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="bb40b-278">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bb40b-278">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="bb40b-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb40b-279">MAPI-Id</span></span>                | <span data-ttu-id="bb40b-280">0x80BF</span><span class="sxs-lookup"><span data-stu-id="bb40b-280">0x80BF</span></span>                                   |
| <span data-ttu-id="bb40b-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb40b-281">System-Only</span></span>            | <span data-ttu-id="bb40b-282">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-282">True</span></span>                                     |
| <span data-ttu-id="bb40b-283">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bb40b-283">Is-Single-Valued</span></span>       | <span data-ttu-id="bb40b-284">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-284">True</span></span>                                     |
| <span data-ttu-id="bb40b-285">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bb40b-285">Is Indexed</span></span>             | <span data-ttu-id="bb40b-286">True</span><span class="sxs-lookup"><span data-stu-id="bb40b-286">True</span></span>                                     |
| <span data-ttu-id="bb40b-287">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bb40b-287">In Global Catalog</span></span>      | <span data-ttu-id="bb40b-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="bb40b-288">False</span></span>                                    |
| <span data-ttu-id="bb40b-289">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bb40b-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb40b-290">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb40b-290">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="bb40b-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb40b-291">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb40b-292">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="bb40b-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-293">Search-Flags</span></span>           | <span data-ttu-id="bb40b-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb40b-294">0x00000001</span></span>                               |
| <span data-ttu-id="bb40b-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb40b-295">System-Flags</span></span>           | <span data-ttu-id="bb40b-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb40b-296">0x00000010</span></span>                               |
| <span data-ttu-id="bb40b-297">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bb40b-297">Classes used in</span></span>        | [<span data-ttu-id="bb40b-298">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bb40b-298">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





