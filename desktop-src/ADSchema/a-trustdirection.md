---
title: Атрибут Trust-Direction
description: Направление доверия.
ms.assetid: 29ee19c6-a6c5-40e6-ad70-bfa0a16e3a84
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Direction
- Схема AD атрибута Трустдиректион
topic_type:
- apiref
api_name:
- Trust-Direction
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54feb80079ea4ac8f1b68fee7d223275313b64b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493677"
---
# <a name="trust-direction-attribute"></a><span data-ttu-id="b01fc-105">Атрибут Trust-Direction</span><span class="sxs-lookup"><span data-stu-id="b01fc-105">Trust-Direction attribute</span></span>

<span data-ttu-id="b01fc-106">Направление доверия.</span><span class="sxs-lookup"><span data-stu-id="b01fc-106">The direction of a trust.</span></span>



| <span data-ttu-id="b01fc-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-107">Entry</span></span> | <span data-ttu-id="b01fc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b01fc-109">CN</span><span class="sxs-lookup"><span data-stu-id="b01fc-109">CN</span></span>                | <span data-ttu-id="b01fc-110">Trust-Direction</span><span class="sxs-lookup"><span data-stu-id="b01fc-110">Trust-Direction</span></span>                      |
| <span data-ttu-id="b01fc-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b01fc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b01fc-112">трустдиректион</span><span class="sxs-lookup"><span data-stu-id="b01fc-112">trustDirection</span></span>                       |
| <span data-ttu-id="b01fc-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b01fc-113">Size</span></span>              | <span data-ttu-id="b01fc-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="b01fc-114">4 bytes</span></span>                              |
| <span data-ttu-id="b01fc-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b01fc-115">Update Privilege</span></span>  | <span data-ttu-id="b01fc-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b01fc-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="b01fc-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b01fc-117">Update Frequency</span></span>  | <span data-ttu-id="b01fc-118">При создании нового доверия.</span><span class="sxs-lookup"><span data-stu-id="b01fc-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="b01fc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-119">Attribute-Id</span></span>      | <span data-ttu-id="b01fc-120">1.2.840.113556.1.4.132</span><span class="sxs-lookup"><span data-stu-id="b01fc-120">1.2.840.113556.1.4.132</span></span>               |
| <span data-ttu-id="b01fc-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b01fc-121">System-Id-Guid</span></span>    | <span data-ttu-id="b01fc-122">bf967a5c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b01fc-122">bf967a5c-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b01fc-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b01fc-123">Syntax</span></span>            | [<span data-ttu-id="b01fc-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b01fc-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b01fc-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b01fc-125">Implementations</span></span>

-   [<span data-ttu-id="b01fc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b01fc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b01fc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b01fc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b01fc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b01fc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b01fc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b01fc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b01fc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b01fc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b01fc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b01fc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b01fc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b01fc-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b01fc-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-133">Entry</span></span> | <span data-ttu-id="b01fc-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b01fc-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b01fc-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fc-137">System-Only</span></span>            | <span data-ttu-id="b01fc-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-138">False</span></span>                                                |
| <span data-ttu-id="b01fc-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b01fc-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fc-140">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-140">True</span></span>                                                 |
| <span data-ttu-id="b01fc-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b01fc-141">Is Indexed</span></span>             | <span data-ttu-id="b01fc-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-142">False</span></span>                                                |
| <span data-ttu-id="b01fc-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b01fc-143">In Global Catalog</span></span>      | <span data-ttu-id="b01fc-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-144">False</span></span>                                                |
| <span data-ttu-id="b01fc-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b01fc-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fc-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b01fc-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b01fc-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fc-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fc-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-149">Search-Flags</span></span>           | <span data-ttu-id="b01fc-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fc-150">0x00000000</span></span>                                           |
| <span data-ttu-id="b01fc-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-151">System-Flags</span></span>           | <span data-ttu-id="b01fc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fc-152">0x00000010</span></span>                                           |
| <span data-ttu-id="b01fc-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b01fc-153">Classes used in</span></span>        | [<span data-ttu-id="b01fc-154">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="b01fc-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b01fc-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b01fc-155">Windows Server 2003</span></span>



| <span data-ttu-id="b01fc-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-156">Entry</span></span> | <span data-ttu-id="b01fc-157">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b01fc-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b01fc-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fc-160">System-Only</span></span>            | <span data-ttu-id="b01fc-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-161">False</span></span>                                                |
| <span data-ttu-id="b01fc-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b01fc-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fc-163">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-163">True</span></span>                                                 |
| <span data-ttu-id="b01fc-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b01fc-164">Is Indexed</span></span>             | <span data-ttu-id="b01fc-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-165">False</span></span>                                                |
| <span data-ttu-id="b01fc-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b01fc-166">In Global Catalog</span></span>      | <span data-ttu-id="b01fc-167">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-167">True</span></span>                                                 |
| <span data-ttu-id="b01fc-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b01fc-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fc-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b01fc-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b01fc-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fc-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fc-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-172">Search-Flags</span></span>           | <span data-ttu-id="b01fc-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fc-173">0x00000000</span></span>                                           |
| <span data-ttu-id="b01fc-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-174">System-Flags</span></span>           | <span data-ttu-id="b01fc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fc-175">0x00000010</span></span>                                           |
| <span data-ttu-id="b01fc-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b01fc-176">Classes used in</span></span>        | [<span data-ttu-id="b01fc-177">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="b01fc-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b01fc-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b01fc-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b01fc-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-179">Entry</span></span> | <span data-ttu-id="b01fc-180">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b01fc-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b01fc-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fc-183">System-Only</span></span>            | <span data-ttu-id="b01fc-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-184">False</span></span>                                                |
| <span data-ttu-id="b01fc-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b01fc-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fc-186">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-186">True</span></span>                                                 |
| <span data-ttu-id="b01fc-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b01fc-187">Is Indexed</span></span>             | <span data-ttu-id="b01fc-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-188">False</span></span>                                                |
| <span data-ttu-id="b01fc-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b01fc-189">In Global Catalog</span></span>      | <span data-ttu-id="b01fc-190">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-190">True</span></span>                                                 |
| <span data-ttu-id="b01fc-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b01fc-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fc-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b01fc-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b01fc-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fc-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fc-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-195">Search-Flags</span></span>           | <span data-ttu-id="b01fc-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fc-196">0x00000000</span></span>                                           |
| <span data-ttu-id="b01fc-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-197">System-Flags</span></span>           | <span data-ttu-id="b01fc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fc-198">0x00000010</span></span>                                           |
| <span data-ttu-id="b01fc-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b01fc-199">Classes used in</span></span>        | [<span data-ttu-id="b01fc-200">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="b01fc-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b01fc-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b01fc-201">Windows Server 2008</span></span>



| <span data-ttu-id="b01fc-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-202">Entry</span></span> | <span data-ttu-id="b01fc-203">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b01fc-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b01fc-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fc-206">System-Only</span></span>            | <span data-ttu-id="b01fc-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-207">False</span></span>                                                |
| <span data-ttu-id="b01fc-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b01fc-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fc-209">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-209">True</span></span>                                                 |
| <span data-ttu-id="b01fc-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b01fc-210">Is Indexed</span></span>             | <span data-ttu-id="b01fc-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-211">False</span></span>                                                |
| <span data-ttu-id="b01fc-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b01fc-212">In Global Catalog</span></span>      | <span data-ttu-id="b01fc-213">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-213">True</span></span>                                                 |
| <span data-ttu-id="b01fc-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b01fc-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fc-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b01fc-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b01fc-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fc-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fc-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-218">Search-Flags</span></span>           | <span data-ttu-id="b01fc-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fc-219">0x00000000</span></span>                                           |
| <span data-ttu-id="b01fc-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-220">System-Flags</span></span>           | <span data-ttu-id="b01fc-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fc-221">0x00000010</span></span>                                           |
| <span data-ttu-id="b01fc-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b01fc-222">Classes used in</span></span>        | [<span data-ttu-id="b01fc-223">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="b01fc-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b01fc-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b01fc-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b01fc-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-225">Entry</span></span> | <span data-ttu-id="b01fc-226">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b01fc-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b01fc-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fc-229">System-Only</span></span>            | <span data-ttu-id="b01fc-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-230">False</span></span>                                                |
| <span data-ttu-id="b01fc-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b01fc-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fc-232">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-232">True</span></span>                                                 |
| <span data-ttu-id="b01fc-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b01fc-233">Is Indexed</span></span>             | <span data-ttu-id="b01fc-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-234">False</span></span>                                                |
| <span data-ttu-id="b01fc-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b01fc-235">In Global Catalog</span></span>      | <span data-ttu-id="b01fc-236">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-236">True</span></span>                                                 |
| <span data-ttu-id="b01fc-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b01fc-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fc-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b01fc-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b01fc-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fc-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fc-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-241">Search-Flags</span></span>           | <span data-ttu-id="b01fc-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fc-242">0x00000000</span></span>                                           |
| <span data-ttu-id="b01fc-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-243">System-Flags</span></span>           | <span data-ttu-id="b01fc-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fc-244">0x00000010</span></span>                                           |
| <span data-ttu-id="b01fc-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b01fc-245">Classes used in</span></span>        | [<span data-ttu-id="b01fc-246">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="b01fc-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b01fc-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b01fc-247">Windows Server 2012</span></span>



| <span data-ttu-id="b01fc-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="b01fc-248">Entry</span></span> | <span data-ttu-id="b01fc-249">Значение</span><span class="sxs-lookup"><span data-stu-id="b01fc-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b01fc-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b01fc-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01fc-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b01fc-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01fc-252">System-Only</span></span>            | <span data-ttu-id="b01fc-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-253">False</span></span>                                                |
| <span data-ttu-id="b01fc-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b01fc-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b01fc-255">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-255">True</span></span>                                                 |
| <span data-ttu-id="b01fc-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b01fc-256">Is Indexed</span></span>             | <span data-ttu-id="b01fc-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="b01fc-257">False</span></span>                                                |
| <span data-ttu-id="b01fc-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b01fc-258">In Global Catalog</span></span>      | <span data-ttu-id="b01fc-259">True</span><span class="sxs-lookup"><span data-stu-id="b01fc-259">True</span></span>                                                 |
| <span data-ttu-id="b01fc-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b01fc-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01fc-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b01fc-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b01fc-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01fc-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01fc-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b01fc-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-264">Search-Flags</span></span>           | <span data-ttu-id="b01fc-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01fc-265">0x00000000</span></span>                                           |
| <span data-ttu-id="b01fc-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01fc-266">System-Flags</span></span>           | <span data-ttu-id="b01fc-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01fc-267">0x00000010</span></span>                                           |
| <span data-ttu-id="b01fc-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b01fc-268">Classes used in</span></span>        | [<span data-ttu-id="b01fc-269">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="b01fc-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





