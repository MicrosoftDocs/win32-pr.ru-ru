---
title: Политика-репликация — атрибут Flags
description: Определяет, какие свойства LSA реплицируются на клиенты.
ms.assetid: 2dadd659-c834-4105-ab3e-8ce0b8811212
ms.tgt_platform: multiple
keywords:
- Политика-репликация-схема AD атрибута
- Схема AD атрибута Полицирепликатионфлагс
topic_type:
- apiref
api_name:
- Policy-Replication-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42da6509662d11c4a069ba58dff5f648e7ab2261
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654803"
---
# <a name="policy-replication-flags-attribute"></a><span data-ttu-id="ae990-105">Политика-репликация — атрибут Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-105">Policy-Replication-Flags attribute</span></span>

<span data-ttu-id="ae990-106">Определяет, какие свойства LSA реплицируются на клиенты.</span><span class="sxs-lookup"><span data-stu-id="ae990-106">Determines which LSA properties are replicated to clients.</span></span>



| <span data-ttu-id="ae990-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-107">Entry</span></span> | <span data-ttu-id="ae990-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ae990-109">CN</span><span class="sxs-lookup"><span data-stu-id="ae990-109">CN</span></span>                | <span data-ttu-id="ae990-110">Политика-репликация-флаги</span><span class="sxs-lookup"><span data-stu-id="ae990-110">Policy-Replication-Flags</span></span>             |
| <span data-ttu-id="ae990-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ae990-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ae990-112">полицирепликатионфлагс</span><span class="sxs-lookup"><span data-stu-id="ae990-112">policyReplicationFlags</span></span>               |
| <span data-ttu-id="ae990-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ae990-113">Size</span></span>              | <span data-ttu-id="ae990-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="ae990-114">4 bytes</span></span>                              |
| <span data-ttu-id="ae990-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ae990-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ae990-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ae990-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ae990-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-117">Attribute-Id</span></span>      | <span data-ttu-id="ae990-118">1.2.840.113556.1.4.633</span><span class="sxs-lookup"><span data-stu-id="ae990-118">1.2.840.113556.1.4.633</span></span>               |
| <span data-ttu-id="ae990-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ae990-119">System-Id-Guid</span></span>    | <span data-ttu-id="ae990-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ae990-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span></span> |
| <span data-ttu-id="ae990-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae990-121">Syntax</span></span>            | [<span data-ttu-id="ae990-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ae990-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ae990-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ae990-123">Implementations</span></span>

-   [<span data-ttu-id="ae990-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ae990-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ae990-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ae990-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ae990-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ae990-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ae990-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ae990-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ae990-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ae990-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ae990-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae990-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ae990-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae990-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ae990-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-131">Entry</span></span> | <span data-ttu-id="ae990-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ae990-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae990-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae990-135">System-Only</span></span>            | <span data-ttu-id="ae990-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-136">False</span></span>                                     |
| <span data-ttu-id="ae990-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae990-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ae990-138">True</span><span class="sxs-lookup"><span data-stu-id="ae990-138">True</span></span>                                      |
| <span data-ttu-id="ae990-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae990-139">Is Indexed</span></span>             | <span data-ttu-id="ae990-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-140">False</span></span>                                     |
| <span data-ttu-id="ae990-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae990-141">In Global Catalog</span></span>      | <span data-ttu-id="ae990-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-142">False</span></span>                                     |
| <span data-ttu-id="ae990-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae990-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae990-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae990-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ae990-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae990-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ae990-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae990-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ae990-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-147">Search-Flags</span></span>           | <span data-ttu-id="ae990-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae990-148">0x00000000</span></span>                                |
| <span data-ttu-id="ae990-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-149">System-Flags</span></span>           | <span data-ttu-id="ae990-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae990-150">0x00000010</span></span>                                |
| <span data-ttu-id="ae990-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae990-151">Classes used in</span></span>        | [<span data-ttu-id="ae990-152">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ae990-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ae990-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae990-153">Windows Server 2003</span></span>



| <span data-ttu-id="ae990-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-154">Entry</span></span> | <span data-ttu-id="ae990-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ae990-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae990-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae990-158">System-Only</span></span>            | <span data-ttu-id="ae990-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-159">False</span></span>                                     |
| <span data-ttu-id="ae990-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae990-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ae990-161">True</span><span class="sxs-lookup"><span data-stu-id="ae990-161">True</span></span>                                      |
| <span data-ttu-id="ae990-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae990-162">Is Indexed</span></span>             | <span data-ttu-id="ae990-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-163">False</span></span>                                     |
| <span data-ttu-id="ae990-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae990-164">In Global Catalog</span></span>      | <span data-ttu-id="ae990-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-165">False</span></span>                                     |
| <span data-ttu-id="ae990-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae990-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae990-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae990-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ae990-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae990-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ae990-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae990-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ae990-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-170">Search-Flags</span></span>           | <span data-ttu-id="ae990-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae990-171">0x00000000</span></span>                                |
| <span data-ttu-id="ae990-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-172">System-Flags</span></span>           | <span data-ttu-id="ae990-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae990-173">0x00000010</span></span>                                |
| <span data-ttu-id="ae990-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae990-174">Classes used in</span></span>        | [<span data-ttu-id="ae990-175">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ae990-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ae990-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ae990-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ae990-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-177">Entry</span></span> | <span data-ttu-id="ae990-178">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ae990-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae990-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae990-181">System-Only</span></span>            | <span data-ttu-id="ae990-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-182">False</span></span>                                     |
| <span data-ttu-id="ae990-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae990-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ae990-184">True</span><span class="sxs-lookup"><span data-stu-id="ae990-184">True</span></span>                                      |
| <span data-ttu-id="ae990-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae990-185">Is Indexed</span></span>             | <span data-ttu-id="ae990-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-186">False</span></span>                                     |
| <span data-ttu-id="ae990-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae990-187">In Global Catalog</span></span>      | <span data-ttu-id="ae990-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-188">False</span></span>                                     |
| <span data-ttu-id="ae990-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae990-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae990-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae990-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ae990-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae990-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ae990-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae990-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ae990-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-193">Search-Flags</span></span>           | <span data-ttu-id="ae990-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae990-194">0x00000000</span></span>                                |
| <span data-ttu-id="ae990-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-195">System-Flags</span></span>           | <span data-ttu-id="ae990-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae990-196">0x00000010</span></span>                                |
| <span data-ttu-id="ae990-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae990-197">Classes used in</span></span>        | [<span data-ttu-id="ae990-198">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ae990-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ae990-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae990-199">Windows Server 2008</span></span>



| <span data-ttu-id="ae990-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-200">Entry</span></span> | <span data-ttu-id="ae990-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ae990-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae990-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae990-204">System-Only</span></span>            | <span data-ttu-id="ae990-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-205">False</span></span>                                     |
| <span data-ttu-id="ae990-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae990-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ae990-207">True</span><span class="sxs-lookup"><span data-stu-id="ae990-207">True</span></span>                                      |
| <span data-ttu-id="ae990-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae990-208">Is Indexed</span></span>             | <span data-ttu-id="ae990-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-209">False</span></span>                                     |
| <span data-ttu-id="ae990-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae990-210">In Global Catalog</span></span>      | <span data-ttu-id="ae990-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-211">False</span></span>                                     |
| <span data-ttu-id="ae990-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae990-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae990-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae990-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ae990-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae990-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ae990-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae990-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ae990-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-216">Search-Flags</span></span>           | <span data-ttu-id="ae990-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae990-217">0x00000000</span></span>                                |
| <span data-ttu-id="ae990-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-218">System-Flags</span></span>           | <span data-ttu-id="ae990-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae990-219">0x00000010</span></span>                                |
| <span data-ttu-id="ae990-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae990-220">Classes used in</span></span>        | [<span data-ttu-id="ae990-221">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ae990-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ae990-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae990-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ae990-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-223">Entry</span></span> | <span data-ttu-id="ae990-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ae990-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae990-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae990-227">System-Only</span></span>            | <span data-ttu-id="ae990-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-228">False</span></span>                                     |
| <span data-ttu-id="ae990-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae990-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ae990-230">True</span><span class="sxs-lookup"><span data-stu-id="ae990-230">True</span></span>                                      |
| <span data-ttu-id="ae990-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae990-231">Is Indexed</span></span>             | <span data-ttu-id="ae990-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-232">False</span></span>                                     |
| <span data-ttu-id="ae990-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae990-233">In Global Catalog</span></span>      | <span data-ttu-id="ae990-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-234">False</span></span>                                     |
| <span data-ttu-id="ae990-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae990-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae990-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae990-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ae990-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae990-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ae990-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae990-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ae990-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-239">Search-Flags</span></span>           | <span data-ttu-id="ae990-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae990-240">0x00000000</span></span>                                |
| <span data-ttu-id="ae990-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-241">System-Flags</span></span>           | <span data-ttu-id="ae990-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae990-242">0x00000010</span></span>                                |
| <span data-ttu-id="ae990-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae990-243">Classes used in</span></span>        | [<span data-ttu-id="ae990-244">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ae990-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ae990-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae990-245">Windows Server 2012</span></span>



| <span data-ttu-id="ae990-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae990-246">Entry</span></span> | <span data-ttu-id="ae990-247">Значение</span><span class="sxs-lookup"><span data-stu-id="ae990-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ae990-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae990-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae990-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ae990-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae990-250">System-Only</span></span>            | <span data-ttu-id="ae990-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-251">False</span></span>                                     |
| <span data-ttu-id="ae990-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae990-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ae990-253">True</span><span class="sxs-lookup"><span data-stu-id="ae990-253">True</span></span>                                      |
| <span data-ttu-id="ae990-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae990-254">Is Indexed</span></span>             | <span data-ttu-id="ae990-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-255">False</span></span>                                     |
| <span data-ttu-id="ae990-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae990-256">In Global Catalog</span></span>      | <span data-ttu-id="ae990-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae990-257">False</span></span>                                     |
| <span data-ttu-id="ae990-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae990-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae990-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae990-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ae990-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae990-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ae990-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae990-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ae990-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-262">Search-Flags</span></span>           | <span data-ttu-id="ae990-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae990-263">0x00000000</span></span>                                |
| <span data-ttu-id="ae990-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae990-264">System-Flags</span></span>           | <span data-ttu-id="ae990-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae990-265">0x00000010</span></span>                                |
| <span data-ttu-id="ae990-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae990-266">Classes used in</span></span>        | [<span data-ttu-id="ae990-267">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ae990-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





