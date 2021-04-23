---
title: ACS-разрешения — атрибут BITS
description: Разрешает исходящий трафик многоадресной рассылки для данного пользователя.
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- ACS-разрешения — схема AD атрибута BITS
- Схема AD атрибута Акспермиссионбитс
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a27370178dd46fd50df44b1226686db5a70a846
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138327"
---
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="69a33-105">ACS-разрешения — атрибут BITS</span><span class="sxs-lookup"><span data-stu-id="69a33-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="69a33-106">Разрешает исходящий трафик многоадресной рассылки для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="69a33-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="69a33-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-107">Entry</span></span> | <span data-ttu-id="69a33-108">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="69a33-109">CN</span><span class="sxs-lookup"><span data-stu-id="69a33-109">CN</span></span>                | <span data-ttu-id="69a33-110">ACS-разрешения — биты</span><span class="sxs-lookup"><span data-stu-id="69a33-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="69a33-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="69a33-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69a33-112">акспермиссионбитс</span><span class="sxs-lookup"><span data-stu-id="69a33-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="69a33-113">Размер</span><span class="sxs-lookup"><span data-stu-id="69a33-113">Size</span></span>              | <span data-ttu-id="69a33-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="69a33-114">8 bytes</span></span>                              |
| <span data-ttu-id="69a33-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="69a33-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="69a33-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="69a33-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="69a33-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-117">Attribute-Id</span></span>      | <span data-ttu-id="69a33-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="69a33-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="69a33-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="69a33-119">System-Id-Guid</span></span>    | <span data-ttu-id="69a33-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="69a33-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="69a33-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69a33-121">Syntax</span></span>            | [<span data-ttu-id="69a33-122">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="69a33-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="69a33-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="69a33-123">Implementations</span></span>

-   [<span data-ttu-id="69a33-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69a33-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69a33-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69a33-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69a33-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69a33-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69a33-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69a33-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69a33-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69a33-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69a33-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69a33-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69a33-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69a33-130">Windows 2000 Server</span></span>



| <span data-ttu-id="69a33-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-131">Entry</span></span> | <span data-ttu-id="69a33-132">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69a33-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69a33-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="69a33-135">System-Only</span></span>            | <span data-ttu-id="69a33-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-136">False</span></span>                                        |
| <span data-ttu-id="69a33-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69a33-137">Is-Single-Valued</span></span>       | <span data-ttu-id="69a33-138">True</span><span class="sxs-lookup"><span data-stu-id="69a33-138">True</span></span>                                         |
| <span data-ttu-id="69a33-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69a33-139">Is Indexed</span></span>             | <span data-ttu-id="69a33-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-140">False</span></span>                                        |
| <span data-ttu-id="69a33-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69a33-141">In Global Catalog</span></span>      | <span data-ttu-id="69a33-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-142">False</span></span>                                        |
| <span data-ttu-id="69a33-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69a33-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="69a33-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69a33-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69a33-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69a33-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69a33-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69a33-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69a33-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-147">Search-Flags</span></span>           | <span data-ttu-id="69a33-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69a33-148">0x00000000</span></span>                                   |
| <span data-ttu-id="69a33-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-149">System-Flags</span></span>           | <span data-ttu-id="69a33-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69a33-150">0x00000010</span></span>                                   |
| <span data-ttu-id="69a33-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69a33-151">Classes used in</span></span>        | [<span data-ttu-id="69a33-152">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="69a33-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69a33-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69a33-153">Windows Server 2003</span></span>



| <span data-ttu-id="69a33-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-154">Entry</span></span> | <span data-ttu-id="69a33-155">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69a33-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69a33-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="69a33-158">System-Only</span></span>            | <span data-ttu-id="69a33-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-159">False</span></span>                                        |
| <span data-ttu-id="69a33-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69a33-160">Is-Single-Valued</span></span>       | <span data-ttu-id="69a33-161">True</span><span class="sxs-lookup"><span data-stu-id="69a33-161">True</span></span>                                         |
| <span data-ttu-id="69a33-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69a33-162">Is Indexed</span></span>             | <span data-ttu-id="69a33-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-163">False</span></span>                                        |
| <span data-ttu-id="69a33-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69a33-164">In Global Catalog</span></span>      | <span data-ttu-id="69a33-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-165">False</span></span>                                        |
| <span data-ttu-id="69a33-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69a33-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="69a33-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69a33-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69a33-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69a33-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69a33-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69a33-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69a33-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-170">Search-Flags</span></span>           | <span data-ttu-id="69a33-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69a33-171">0x00000000</span></span>                                   |
| <span data-ttu-id="69a33-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-172">System-Flags</span></span>           | <span data-ttu-id="69a33-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69a33-173">0x00000010</span></span>                                   |
| <span data-ttu-id="69a33-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69a33-174">Classes used in</span></span>        | [<span data-ttu-id="69a33-175">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="69a33-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69a33-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69a33-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69a33-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-177">Entry</span></span> | <span data-ttu-id="69a33-178">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69a33-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69a33-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="69a33-181">System-Only</span></span>            | <span data-ttu-id="69a33-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-182">False</span></span>                                        |
| <span data-ttu-id="69a33-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69a33-183">Is-Single-Valued</span></span>       | <span data-ttu-id="69a33-184">True</span><span class="sxs-lookup"><span data-stu-id="69a33-184">True</span></span>                                         |
| <span data-ttu-id="69a33-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69a33-185">Is Indexed</span></span>             | <span data-ttu-id="69a33-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-186">False</span></span>                                        |
| <span data-ttu-id="69a33-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69a33-187">In Global Catalog</span></span>      | <span data-ttu-id="69a33-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-188">False</span></span>                                        |
| <span data-ttu-id="69a33-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69a33-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="69a33-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69a33-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69a33-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69a33-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69a33-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69a33-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69a33-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-193">Search-Flags</span></span>           | <span data-ttu-id="69a33-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69a33-194">0x00000000</span></span>                                   |
| <span data-ttu-id="69a33-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-195">System-Flags</span></span>           | <span data-ttu-id="69a33-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69a33-196">0x00000010</span></span>                                   |
| <span data-ttu-id="69a33-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69a33-197">Classes used in</span></span>        | [<span data-ttu-id="69a33-198">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="69a33-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69a33-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69a33-199">Windows Server 2008</span></span>



| <span data-ttu-id="69a33-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-200">Entry</span></span> | <span data-ttu-id="69a33-201">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69a33-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69a33-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="69a33-204">System-Only</span></span>            | <span data-ttu-id="69a33-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-205">False</span></span>                                        |
| <span data-ttu-id="69a33-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69a33-206">Is-Single-Valued</span></span>       | <span data-ttu-id="69a33-207">True</span><span class="sxs-lookup"><span data-stu-id="69a33-207">True</span></span>                                         |
| <span data-ttu-id="69a33-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69a33-208">Is Indexed</span></span>             | <span data-ttu-id="69a33-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-209">False</span></span>                                        |
| <span data-ttu-id="69a33-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69a33-210">In Global Catalog</span></span>      | <span data-ttu-id="69a33-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-211">False</span></span>                                        |
| <span data-ttu-id="69a33-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69a33-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="69a33-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69a33-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69a33-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69a33-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69a33-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69a33-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69a33-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-216">Search-Flags</span></span>           | <span data-ttu-id="69a33-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69a33-217">0x00000000</span></span>                                   |
| <span data-ttu-id="69a33-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-218">System-Flags</span></span>           | <span data-ttu-id="69a33-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69a33-219">0x00000010</span></span>                                   |
| <span data-ttu-id="69a33-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69a33-220">Classes used in</span></span>        | [<span data-ttu-id="69a33-221">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="69a33-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69a33-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69a33-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69a33-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-223">Entry</span></span> | <span data-ttu-id="69a33-224">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69a33-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69a33-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="69a33-227">System-Only</span></span>            | <span data-ttu-id="69a33-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-228">False</span></span>                                        |
| <span data-ttu-id="69a33-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69a33-229">Is-Single-Valued</span></span>       | <span data-ttu-id="69a33-230">True</span><span class="sxs-lookup"><span data-stu-id="69a33-230">True</span></span>                                         |
| <span data-ttu-id="69a33-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69a33-231">Is Indexed</span></span>             | <span data-ttu-id="69a33-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-232">False</span></span>                                        |
| <span data-ttu-id="69a33-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69a33-233">In Global Catalog</span></span>      | <span data-ttu-id="69a33-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-234">False</span></span>                                        |
| <span data-ttu-id="69a33-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69a33-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="69a33-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69a33-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69a33-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69a33-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69a33-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69a33-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69a33-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-239">Search-Flags</span></span>           | <span data-ttu-id="69a33-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69a33-240">0x00000000</span></span>                                   |
| <span data-ttu-id="69a33-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-241">System-Flags</span></span>           | <span data-ttu-id="69a33-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69a33-242">0x00000010</span></span>                                   |
| <span data-ttu-id="69a33-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69a33-243">Classes used in</span></span>        | [<span data-ttu-id="69a33-244">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="69a33-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69a33-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69a33-245">Windows Server 2012</span></span>



| <span data-ttu-id="69a33-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="69a33-246">Entry</span></span> | <span data-ttu-id="69a33-247">Значение</span><span class="sxs-lookup"><span data-stu-id="69a33-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69a33-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69a33-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69a33-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69a33-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="69a33-250">System-Only</span></span>            | <span data-ttu-id="69a33-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-251">False</span></span>                                        |
| <span data-ttu-id="69a33-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69a33-252">Is-Single-Valued</span></span>       | <span data-ttu-id="69a33-253">True</span><span class="sxs-lookup"><span data-stu-id="69a33-253">True</span></span>                                         |
| <span data-ttu-id="69a33-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69a33-254">Is Indexed</span></span>             | <span data-ttu-id="69a33-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-255">False</span></span>                                        |
| <span data-ttu-id="69a33-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69a33-256">In Global Catalog</span></span>      | <span data-ttu-id="69a33-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="69a33-257">False</span></span>                                        |
| <span data-ttu-id="69a33-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69a33-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="69a33-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69a33-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69a33-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69a33-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69a33-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69a33-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69a33-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-262">Search-Flags</span></span>           | <span data-ttu-id="69a33-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69a33-263">0x00000000</span></span>                                   |
| <span data-ttu-id="69a33-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69a33-264">System-Flags</span></span>           | <span data-ttu-id="69a33-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69a33-265">0x00000010</span></span>                                   |
| <span data-ttu-id="69a33-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69a33-266">Classes used in</span></span>        | [<span data-ttu-id="69a33-267">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="69a33-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





