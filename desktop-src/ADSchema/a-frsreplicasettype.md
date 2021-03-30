---
title: FRS-реплика-набор-тип атрибута
description: Это код, указывающий, является ли этот набор репликой SYSVOL, набором реплик DFS или другим набором реплик.
ms.assetid: 687a854f-ffa1-41f4-a515-5224759696ab
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута службы FRS-Set-Type
- Схема AD атрибута Фрсрепликасеттипе
topic_type:
- apiref
api_name:
- FRS-Replica-Set-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18046c9b4edb794687d275af52e35416419c7e2d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893013"
---
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="84f7b-105">FRS-реплика-набор-тип атрибута</span><span class="sxs-lookup"><span data-stu-id="84f7b-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="84f7b-106">Это код, указывающий, является ли этот набор репликой SYSVOL, набором реплик DFS или другим набором реплик.</span><span class="sxs-lookup"><span data-stu-id="84f7b-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="84f7b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-107">Entry</span></span> | <span data-ttu-id="84f7b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="84f7b-109">CN</span><span class="sxs-lookup"><span data-stu-id="84f7b-109">CN</span></span>                | <span data-ttu-id="84f7b-110">FRS-Replica-Set-Type</span><span class="sxs-lookup"><span data-stu-id="84f7b-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="84f7b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="84f7b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="84f7b-112">фрсрепликасеттипе</span><span class="sxs-lookup"><span data-stu-id="84f7b-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="84f7b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="84f7b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="84f7b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="84f7b-114">Update Privilege</span></span>  | <span data-ttu-id="84f7b-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="84f7b-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="84f7b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="84f7b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="84f7b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-117">Attribute-Id</span></span>      | <span data-ttu-id="84f7b-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="84f7b-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="84f7b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="84f7b-119">System-Id-Guid</span></span>    | <span data-ttu-id="84f7b-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="84f7b-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="84f7b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84f7b-121">Syntax</span></span>            | [<span data-ttu-id="84f7b-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="84f7b-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="84f7b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="84f7b-123">Implementations</span></span>

-   [<span data-ttu-id="84f7b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="84f7b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="84f7b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="84f7b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="84f7b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="84f7b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="84f7b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="84f7b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="84f7b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="84f7b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="84f7b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="84f7b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="84f7b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84f7b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="84f7b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-131">Entry</span></span> | <span data-ttu-id="84f7b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84f7b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="84f7b-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f7b-135">System-Only</span></span>            | <span data-ttu-id="84f7b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-136">False</span></span>                                                     |
| <span data-ttu-id="84f7b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="84f7b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="84f7b-138">True</span><span class="sxs-lookup"><span data-stu-id="84f7b-138">True</span></span>                                                      |
| <span data-ttu-id="84f7b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="84f7b-139">Is Indexed</span></span>             | <span data-ttu-id="84f7b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-140">False</span></span>                                                     |
| <span data-ttu-id="84f7b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="84f7b-141">In Global Catalog</span></span>      | <span data-ttu-id="84f7b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-142">False</span></span>                                                     |
| <span data-ttu-id="84f7b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="84f7b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f7b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f7b-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84f7b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f7b-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f7b-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-147">Search-Flags</span></span>           | <span data-ttu-id="84f7b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f7b-148">0x00000000</span></span>                                                |
| <span data-ttu-id="84f7b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-149">System-Flags</span></span>           | <span data-ttu-id="84f7b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f7b-150">0x00000010</span></span>                                                |
| <span data-ttu-id="84f7b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="84f7b-151">Classes used in</span></span>        | [<span data-ttu-id="84f7b-152">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="84f7b-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="84f7b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84f7b-153">Windows Server 2003</span></span>



| <span data-ttu-id="84f7b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-154">Entry</span></span> | <span data-ttu-id="84f7b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84f7b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="84f7b-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f7b-158">System-Only</span></span>            | <span data-ttu-id="84f7b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-159">False</span></span>                                                     |
| <span data-ttu-id="84f7b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="84f7b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="84f7b-161">True</span><span class="sxs-lookup"><span data-stu-id="84f7b-161">True</span></span>                                                      |
| <span data-ttu-id="84f7b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="84f7b-162">Is Indexed</span></span>             | <span data-ttu-id="84f7b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-163">False</span></span>                                                     |
| <span data-ttu-id="84f7b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="84f7b-164">In Global Catalog</span></span>      | <span data-ttu-id="84f7b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-165">False</span></span>                                                     |
| <span data-ttu-id="84f7b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="84f7b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f7b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f7b-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84f7b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f7b-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f7b-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-170">Search-Flags</span></span>           | <span data-ttu-id="84f7b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f7b-171">0x00000000</span></span>                                                |
| <span data-ttu-id="84f7b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-172">System-Flags</span></span>           | <span data-ttu-id="84f7b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f7b-173">0x00000010</span></span>                                                |
| <span data-ttu-id="84f7b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="84f7b-174">Classes used in</span></span>        | [<span data-ttu-id="84f7b-175">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="84f7b-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="84f7b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="84f7b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="84f7b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-177">Entry</span></span> | <span data-ttu-id="84f7b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84f7b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="84f7b-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f7b-181">System-Only</span></span>            | <span data-ttu-id="84f7b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-182">False</span></span>                                                     |
| <span data-ttu-id="84f7b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="84f7b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="84f7b-184">True</span><span class="sxs-lookup"><span data-stu-id="84f7b-184">True</span></span>                                                      |
| <span data-ttu-id="84f7b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="84f7b-185">Is Indexed</span></span>             | <span data-ttu-id="84f7b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-186">False</span></span>                                                     |
| <span data-ttu-id="84f7b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="84f7b-187">In Global Catalog</span></span>      | <span data-ttu-id="84f7b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-188">False</span></span>                                                     |
| <span data-ttu-id="84f7b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="84f7b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f7b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f7b-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84f7b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f7b-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f7b-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-193">Search-Flags</span></span>           | <span data-ttu-id="84f7b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f7b-194">0x00000000</span></span>                                                |
| <span data-ttu-id="84f7b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-195">System-Flags</span></span>           | <span data-ttu-id="84f7b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f7b-196">0x00000010</span></span>                                                |
| <span data-ttu-id="84f7b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="84f7b-197">Classes used in</span></span>        | [<span data-ttu-id="84f7b-198">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="84f7b-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="84f7b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84f7b-199">Windows Server 2008</span></span>



| <span data-ttu-id="84f7b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-200">Entry</span></span> | <span data-ttu-id="84f7b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84f7b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="84f7b-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f7b-204">System-Only</span></span>            | <span data-ttu-id="84f7b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-205">False</span></span>                                                     |
| <span data-ttu-id="84f7b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="84f7b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="84f7b-207">True</span><span class="sxs-lookup"><span data-stu-id="84f7b-207">True</span></span>                                                      |
| <span data-ttu-id="84f7b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="84f7b-208">Is Indexed</span></span>             | <span data-ttu-id="84f7b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-209">False</span></span>                                                     |
| <span data-ttu-id="84f7b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="84f7b-210">In Global Catalog</span></span>      | <span data-ttu-id="84f7b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-211">False</span></span>                                                     |
| <span data-ttu-id="84f7b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="84f7b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f7b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f7b-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84f7b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f7b-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f7b-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-216">Search-Flags</span></span>           | <span data-ttu-id="84f7b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f7b-217">0x00000000</span></span>                                                |
| <span data-ttu-id="84f7b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-218">System-Flags</span></span>           | <span data-ttu-id="84f7b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f7b-219">0x00000010</span></span>                                                |
| <span data-ttu-id="84f7b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="84f7b-220">Classes used in</span></span>        | [<span data-ttu-id="84f7b-221">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="84f7b-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="84f7b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f7b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="84f7b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-223">Entry</span></span> | <span data-ttu-id="84f7b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84f7b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="84f7b-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f7b-227">System-Only</span></span>            | <span data-ttu-id="84f7b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-228">False</span></span>                                                     |
| <span data-ttu-id="84f7b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="84f7b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="84f7b-230">True</span><span class="sxs-lookup"><span data-stu-id="84f7b-230">True</span></span>                                                      |
| <span data-ttu-id="84f7b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="84f7b-231">Is Indexed</span></span>             | <span data-ttu-id="84f7b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-232">False</span></span>                                                     |
| <span data-ttu-id="84f7b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="84f7b-233">In Global Catalog</span></span>      | <span data-ttu-id="84f7b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-234">False</span></span>                                                     |
| <span data-ttu-id="84f7b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="84f7b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f7b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f7b-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84f7b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f7b-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f7b-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-239">Search-Flags</span></span>           | <span data-ttu-id="84f7b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f7b-240">0x00000000</span></span>                                                |
| <span data-ttu-id="84f7b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-241">System-Flags</span></span>           | <span data-ttu-id="84f7b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f7b-242">0x00000010</span></span>                                                |
| <span data-ttu-id="84f7b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="84f7b-243">Classes used in</span></span>        | [<span data-ttu-id="84f7b-244">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="84f7b-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="84f7b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84f7b-245">Windows Server 2012</span></span>



| <span data-ttu-id="84f7b-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="84f7b-246">Entry</span></span> | <span data-ttu-id="84f7b-247">Значение</span><span class="sxs-lookup"><span data-stu-id="84f7b-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84f7b-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="84f7b-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f7b-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84f7b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f7b-250">System-Only</span></span>            | <span data-ttu-id="84f7b-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-251">False</span></span>                                                     |
| <span data-ttu-id="84f7b-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="84f7b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="84f7b-253">True</span><span class="sxs-lookup"><span data-stu-id="84f7b-253">True</span></span>                                                      |
| <span data-ttu-id="84f7b-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="84f7b-254">Is Indexed</span></span>             | <span data-ttu-id="84f7b-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-255">False</span></span>                                                     |
| <span data-ttu-id="84f7b-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="84f7b-256">In Global Catalog</span></span>      | <span data-ttu-id="84f7b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="84f7b-257">False</span></span>                                                     |
| <span data-ttu-id="84f7b-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="84f7b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f7b-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f7b-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84f7b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f7b-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f7b-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84f7b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-262">Search-Flags</span></span>           | <span data-ttu-id="84f7b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f7b-263">0x00000000</span></span>                                                |
| <span data-ttu-id="84f7b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f7b-264">System-Flags</span></span>           | <span data-ttu-id="84f7b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f7b-265">0x00000010</span></span>                                                |
| <span data-ttu-id="84f7b-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="84f7b-266">Classes used in</span></span>        | [<span data-ttu-id="84f7b-267">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="84f7b-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





