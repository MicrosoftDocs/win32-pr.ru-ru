---
title: Атрибут Trust-Type
description: Тип доверия, например Windows NT или MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Type
- Схема AD атрибута Трусттипе
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989624"
---
# <a name="trust-type-attribute"></a><span data-ttu-id="d4888-105">Атрибут Trust-Type</span><span class="sxs-lookup"><span data-stu-id="d4888-105">Trust-Type attribute</span></span>

<span data-ttu-id="d4888-106">Тип доверия, например Windows NT или MIT.</span><span class="sxs-lookup"><span data-stu-id="d4888-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="d4888-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-107">Entry</span></span> | <span data-ttu-id="d4888-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d4888-109">CN</span><span class="sxs-lookup"><span data-stu-id="d4888-109">CN</span></span>                | <span data-ttu-id="d4888-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="d4888-110">Trust-Type</span></span>                           |
| <span data-ttu-id="d4888-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d4888-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d4888-112">трусттипе</span><span class="sxs-lookup"><span data-stu-id="d4888-112">trustType</span></span>                            |
| <span data-ttu-id="d4888-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d4888-113">Size</span></span>              | <span data-ttu-id="d4888-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="d4888-114">4 bytes</span></span>                              |
| <span data-ttu-id="d4888-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d4888-115">Update Privilege</span></span>  | <span data-ttu-id="d4888-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="d4888-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d4888-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d4888-117">Update Frequency</span></span>  | <span data-ttu-id="d4888-118">При создании нового доверия.</span><span class="sxs-lookup"><span data-stu-id="d4888-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="d4888-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-119">Attribute-Id</span></span>      | <span data-ttu-id="d4888-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="d4888-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="d4888-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d4888-121">System-Id-Guid</span></span>    | <span data-ttu-id="d4888-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d4888-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d4888-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4888-123">Syntax</span></span>            | [<span data-ttu-id="d4888-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="d4888-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d4888-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d4888-125">Implementations</span></span>

-   [<span data-ttu-id="d4888-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d4888-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d4888-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4888-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4888-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4888-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4888-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4888-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4888-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4888-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4888-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4888-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d4888-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4888-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d4888-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-133">Entry</span></span> | <span data-ttu-id="d4888-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d4888-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d4888-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4888-137">System-Only</span></span>            | <span data-ttu-id="d4888-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-138">False</span></span>                                                |
| <span data-ttu-id="d4888-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d4888-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d4888-140">True</span><span class="sxs-lookup"><span data-stu-id="d4888-140">True</span></span>                                                 |
| <span data-ttu-id="d4888-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d4888-141">Is Indexed</span></span>             | <span data-ttu-id="d4888-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-142">False</span></span>                                                |
| <span data-ttu-id="d4888-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d4888-143">In Global Catalog</span></span>      | <span data-ttu-id="d4888-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-144">False</span></span>                                                |
| <span data-ttu-id="d4888-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d4888-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4888-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d4888-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d4888-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4888-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4888-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-149">Search-Flags</span></span>           | <span data-ttu-id="d4888-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4888-150">0x00000000</span></span>                                           |
| <span data-ttu-id="d4888-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-151">System-Flags</span></span>           | <span data-ttu-id="d4888-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4888-152">0x00000010</span></span>                                           |
| <span data-ttu-id="d4888-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d4888-153">Classes used in</span></span>        | [<span data-ttu-id="d4888-154">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="d4888-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d4888-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4888-155">Windows Server 2003</span></span>



| <span data-ttu-id="d4888-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-156">Entry</span></span> | <span data-ttu-id="d4888-157">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d4888-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d4888-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4888-160">System-Only</span></span>            | <span data-ttu-id="d4888-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-161">False</span></span>                                                |
| <span data-ttu-id="d4888-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d4888-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d4888-163">True</span><span class="sxs-lookup"><span data-stu-id="d4888-163">True</span></span>                                                 |
| <span data-ttu-id="d4888-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d4888-164">Is Indexed</span></span>             | <span data-ttu-id="d4888-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-165">False</span></span>                                                |
| <span data-ttu-id="d4888-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d4888-166">In Global Catalog</span></span>      | <span data-ttu-id="d4888-167">True</span><span class="sxs-lookup"><span data-stu-id="d4888-167">True</span></span>                                                 |
| <span data-ttu-id="d4888-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d4888-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4888-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d4888-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d4888-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4888-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4888-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-172">Search-Flags</span></span>           | <span data-ttu-id="d4888-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4888-173">0x00000000</span></span>                                           |
| <span data-ttu-id="d4888-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-174">System-Flags</span></span>           | <span data-ttu-id="d4888-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4888-175">0x00000010</span></span>                                           |
| <span data-ttu-id="d4888-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d4888-176">Classes used in</span></span>        | [<span data-ttu-id="d4888-177">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="d4888-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4888-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4888-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4888-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-179">Entry</span></span> | <span data-ttu-id="d4888-180">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d4888-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d4888-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4888-183">System-Only</span></span>            | <span data-ttu-id="d4888-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-184">False</span></span>                                                |
| <span data-ttu-id="d4888-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d4888-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d4888-186">True</span><span class="sxs-lookup"><span data-stu-id="d4888-186">True</span></span>                                                 |
| <span data-ttu-id="d4888-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d4888-187">Is Indexed</span></span>             | <span data-ttu-id="d4888-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-188">False</span></span>                                                |
| <span data-ttu-id="d4888-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d4888-189">In Global Catalog</span></span>      | <span data-ttu-id="d4888-190">True</span><span class="sxs-lookup"><span data-stu-id="d4888-190">True</span></span>                                                 |
| <span data-ttu-id="d4888-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d4888-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4888-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d4888-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d4888-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4888-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4888-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-195">Search-Flags</span></span>           | <span data-ttu-id="d4888-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4888-196">0x00000000</span></span>                                           |
| <span data-ttu-id="d4888-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-197">System-Flags</span></span>           | <span data-ttu-id="d4888-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4888-198">0x00000010</span></span>                                           |
| <span data-ttu-id="d4888-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d4888-199">Classes used in</span></span>        | [<span data-ttu-id="d4888-200">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="d4888-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d4888-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4888-201">Windows Server 2008</span></span>



| <span data-ttu-id="d4888-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-202">Entry</span></span> | <span data-ttu-id="d4888-203">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d4888-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d4888-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4888-206">System-Only</span></span>            | <span data-ttu-id="d4888-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-207">False</span></span>                                                |
| <span data-ttu-id="d4888-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d4888-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d4888-209">True</span><span class="sxs-lookup"><span data-stu-id="d4888-209">True</span></span>                                                 |
| <span data-ttu-id="d4888-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d4888-210">Is Indexed</span></span>             | <span data-ttu-id="d4888-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-211">False</span></span>                                                |
| <span data-ttu-id="d4888-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d4888-212">In Global Catalog</span></span>      | <span data-ttu-id="d4888-213">True</span><span class="sxs-lookup"><span data-stu-id="d4888-213">True</span></span>                                                 |
| <span data-ttu-id="d4888-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d4888-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4888-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d4888-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d4888-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4888-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4888-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-218">Search-Flags</span></span>           | <span data-ttu-id="d4888-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4888-219">0x00000000</span></span>                                           |
| <span data-ttu-id="d4888-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-220">System-Flags</span></span>           | <span data-ttu-id="d4888-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4888-221">0x00000010</span></span>                                           |
| <span data-ttu-id="d4888-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d4888-222">Classes used in</span></span>        | [<span data-ttu-id="d4888-223">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="d4888-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4888-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4888-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4888-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-225">Entry</span></span> | <span data-ttu-id="d4888-226">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d4888-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d4888-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4888-229">System-Only</span></span>            | <span data-ttu-id="d4888-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-230">False</span></span>                                                |
| <span data-ttu-id="d4888-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d4888-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d4888-232">True</span><span class="sxs-lookup"><span data-stu-id="d4888-232">True</span></span>                                                 |
| <span data-ttu-id="d4888-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d4888-233">Is Indexed</span></span>             | <span data-ttu-id="d4888-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-234">False</span></span>                                                |
| <span data-ttu-id="d4888-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d4888-235">In Global Catalog</span></span>      | <span data-ttu-id="d4888-236">True</span><span class="sxs-lookup"><span data-stu-id="d4888-236">True</span></span>                                                 |
| <span data-ttu-id="d4888-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d4888-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4888-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d4888-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d4888-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4888-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4888-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-241">Search-Flags</span></span>           | <span data-ttu-id="d4888-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4888-242">0x00000000</span></span>                                           |
| <span data-ttu-id="d4888-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-243">System-Flags</span></span>           | <span data-ttu-id="d4888-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4888-244">0x00000010</span></span>                                           |
| <span data-ttu-id="d4888-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d4888-245">Classes used in</span></span>        | [<span data-ttu-id="d4888-246">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="d4888-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d4888-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4888-247">Windows Server 2012</span></span>



| <span data-ttu-id="d4888-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="d4888-248">Entry</span></span> | <span data-ttu-id="d4888-249">Значение</span><span class="sxs-lookup"><span data-stu-id="d4888-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d4888-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d4888-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4888-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d4888-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4888-252">System-Only</span></span>            | <span data-ttu-id="d4888-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-253">False</span></span>                                                |
| <span data-ttu-id="d4888-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d4888-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d4888-255">True</span><span class="sxs-lookup"><span data-stu-id="d4888-255">True</span></span>                                                 |
| <span data-ttu-id="d4888-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d4888-256">Is Indexed</span></span>             | <span data-ttu-id="d4888-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="d4888-257">False</span></span>                                                |
| <span data-ttu-id="d4888-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d4888-258">In Global Catalog</span></span>      | <span data-ttu-id="d4888-259">True</span><span class="sxs-lookup"><span data-stu-id="d4888-259">True</span></span>                                                 |
| <span data-ttu-id="d4888-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d4888-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4888-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d4888-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d4888-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4888-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4888-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d4888-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-264">Search-Flags</span></span>           | <span data-ttu-id="d4888-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4888-265">0x00000000</span></span>                                           |
| <span data-ttu-id="d4888-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4888-266">System-Flags</span></span>           | <span data-ttu-id="d4888-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4888-267">0x00000010</span></span>                                           |
| <span data-ttu-id="d4888-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d4888-268">Classes used in</span></span>        | [<span data-ttu-id="d4888-269">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="d4888-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





