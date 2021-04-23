---
title: Атрибут MS-SQL-Алловкуеуедупдатингсубскриптион
description: Значение true, чтобы разрешить транзакции в очереди при обновлении подписок.
ms.assetid: 132c107f-8586-48db-b70c-027c619aadf7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Алловкуеуедупдатингсубскриптион
- Схема AD атрибута mS-SQL-Алловкуеуедупдатингсубскриптион
topic_type:
- apiref
api_name:
- MS-SQL-AllowQueuedUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2056a04b6e0f155c156cde06975e96eb13f61eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893061"
---
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="8f577-105">Атрибут MS-SQL-Алловкуеуедупдатингсубскриптион</span><span class="sxs-lookup"><span data-stu-id="8f577-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="8f577-106">Значение true, чтобы разрешить транзакции в очереди при обновлении подписок.</span><span class="sxs-lookup"><span data-stu-id="8f577-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="8f577-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-107">Entry</span></span> | <span data-ttu-id="8f577-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="8f577-109">CN</span><span class="sxs-lookup"><span data-stu-id="8f577-109">CN</span></span>                | <span data-ttu-id="8f577-110">MS-SQL-Алловкуеуедупдатингсубскриптион</span><span class="sxs-lookup"><span data-stu-id="8f577-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="8f577-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8f577-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8f577-112">mS-SQL-Алловкуеуедупдатингсубскриптион</span><span class="sxs-lookup"><span data-stu-id="8f577-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="8f577-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8f577-113">Size</span></span>              | <span data-ttu-id="8f577-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="8f577-114">4 bytes</span></span>                                |
| <span data-ttu-id="8f577-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8f577-115">Update Privilege</span></span>  | <span data-ttu-id="8f577-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="8f577-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="8f577-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8f577-117">Update Frequency</span></span>  | <span data-ttu-id="8f577-118">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="8f577-118">When replication is setup.</span></span>             |
| <span data-ttu-id="8f577-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-119">Attribute-Id</span></span>      | <span data-ttu-id="8f577-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="8f577-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="8f577-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8f577-121">System-Id-Guid</span></span>    | <span data-ttu-id="8f577-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="8f577-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="8f577-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f577-123">Syntax</span></span>            | [<span data-ttu-id="8f577-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="8f577-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="8f577-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8f577-125">Implementations</span></span>

-   [<span data-ttu-id="8f577-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f577-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f577-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f577-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f577-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f577-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f577-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f577-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f577-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f577-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f577-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f577-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f577-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f577-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8f577-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-133">Entry</span></span> | <span data-ttu-id="8f577-134">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8f577-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f577-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f577-137">System-Only</span></span>            | <span data-ttu-id="8f577-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-138">False</span></span>                                                               |
| <span data-ttu-id="8f577-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f577-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8f577-140">True</span><span class="sxs-lookup"><span data-stu-id="8f577-140">True</span></span>                                                                |
| <span data-ttu-id="8f577-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f577-141">Is Indexed</span></span>             | <span data-ttu-id="8f577-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-142">False</span></span>                                                               |
| <span data-ttu-id="8f577-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f577-143">In Global Catalog</span></span>      | <span data-ttu-id="8f577-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-144">False</span></span>                                                               |
| <span data-ttu-id="8f577-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f577-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f577-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f577-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8f577-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f577-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f577-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-149">Search-Flags</span></span>           | <span data-ttu-id="8f577-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f577-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="8f577-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-151">System-Flags</span></span>           | <span data-ttu-id="8f577-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f577-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="8f577-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f577-153">Classes used in</span></span>        | [<span data-ttu-id="8f577-154">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8f577-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8f577-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f577-155">Windows Server 2003</span></span>



| <span data-ttu-id="8f577-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-156">Entry</span></span> | <span data-ttu-id="8f577-157">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8f577-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f577-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f577-160">System-Only</span></span>            | <span data-ttu-id="8f577-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-161">False</span></span>                                                               |
| <span data-ttu-id="8f577-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f577-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8f577-163">True</span><span class="sxs-lookup"><span data-stu-id="8f577-163">True</span></span>                                                                |
| <span data-ttu-id="8f577-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f577-164">Is Indexed</span></span>             | <span data-ttu-id="8f577-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-165">False</span></span>                                                               |
| <span data-ttu-id="8f577-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f577-166">In Global Catalog</span></span>      | <span data-ttu-id="8f577-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-167">False</span></span>                                                               |
| <span data-ttu-id="8f577-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f577-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f577-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f577-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8f577-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f577-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f577-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-172">Search-Flags</span></span>           | <span data-ttu-id="8f577-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f577-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="8f577-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-174">System-Flags</span></span>           | <span data-ttu-id="8f577-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f577-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="8f577-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f577-176">Classes used in</span></span>        | [<span data-ttu-id="8f577-177">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8f577-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f577-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f577-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f577-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-179">Entry</span></span> | <span data-ttu-id="8f577-180">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8f577-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f577-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f577-183">System-Only</span></span>            | <span data-ttu-id="8f577-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-184">False</span></span>                                                               |
| <span data-ttu-id="8f577-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f577-185">Is-Single-Valued</span></span>       | <span data-ttu-id="8f577-186">True</span><span class="sxs-lookup"><span data-stu-id="8f577-186">True</span></span>                                                                |
| <span data-ttu-id="8f577-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f577-187">Is Indexed</span></span>             | <span data-ttu-id="8f577-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-188">False</span></span>                                                               |
| <span data-ttu-id="8f577-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f577-189">In Global Catalog</span></span>      | <span data-ttu-id="8f577-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-190">False</span></span>                                                               |
| <span data-ttu-id="8f577-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f577-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f577-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f577-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8f577-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f577-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f577-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-195">Search-Flags</span></span>           | <span data-ttu-id="8f577-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f577-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="8f577-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-197">System-Flags</span></span>           | <span data-ttu-id="8f577-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f577-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="8f577-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f577-199">Classes used in</span></span>        | [<span data-ttu-id="8f577-200">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8f577-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8f577-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f577-201">Windows Server 2008</span></span>



| <span data-ttu-id="8f577-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-202">Entry</span></span> | <span data-ttu-id="8f577-203">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8f577-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f577-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f577-206">System-Only</span></span>            | <span data-ttu-id="8f577-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-207">False</span></span>                                                               |
| <span data-ttu-id="8f577-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f577-208">Is-Single-Valued</span></span>       | <span data-ttu-id="8f577-209">True</span><span class="sxs-lookup"><span data-stu-id="8f577-209">True</span></span>                                                                |
| <span data-ttu-id="8f577-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f577-210">Is Indexed</span></span>             | <span data-ttu-id="8f577-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-211">False</span></span>                                                               |
| <span data-ttu-id="8f577-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f577-212">In Global Catalog</span></span>      | <span data-ttu-id="8f577-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-213">False</span></span>                                                               |
| <span data-ttu-id="8f577-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f577-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f577-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f577-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8f577-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f577-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f577-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-218">Search-Flags</span></span>           | <span data-ttu-id="8f577-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f577-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="8f577-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-220">System-Flags</span></span>           | <span data-ttu-id="8f577-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f577-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="8f577-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f577-222">Classes used in</span></span>        | [<span data-ttu-id="8f577-223">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8f577-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f577-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f577-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f577-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-225">Entry</span></span> | <span data-ttu-id="8f577-226">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8f577-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f577-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f577-229">System-Only</span></span>            | <span data-ttu-id="8f577-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-230">False</span></span>                                                               |
| <span data-ttu-id="8f577-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f577-231">Is-Single-Valued</span></span>       | <span data-ttu-id="8f577-232">True</span><span class="sxs-lookup"><span data-stu-id="8f577-232">True</span></span>                                                                |
| <span data-ttu-id="8f577-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f577-233">Is Indexed</span></span>             | <span data-ttu-id="8f577-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-234">False</span></span>                                                               |
| <span data-ttu-id="8f577-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f577-235">In Global Catalog</span></span>      | <span data-ttu-id="8f577-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-236">False</span></span>                                                               |
| <span data-ttu-id="8f577-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f577-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f577-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f577-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8f577-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f577-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f577-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-241">Search-Flags</span></span>           | <span data-ttu-id="8f577-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f577-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="8f577-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-243">System-Flags</span></span>           | <span data-ttu-id="8f577-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f577-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="8f577-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f577-245">Classes used in</span></span>        | [<span data-ttu-id="8f577-246">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8f577-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8f577-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f577-247">Windows Server 2012</span></span>



| <span data-ttu-id="8f577-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f577-248">Entry</span></span> | <span data-ttu-id="8f577-249">Значение</span><span class="sxs-lookup"><span data-stu-id="8f577-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8f577-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f577-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f577-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8f577-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f577-252">System-Only</span></span>            | <span data-ttu-id="8f577-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-253">False</span></span>                                                               |
| <span data-ttu-id="8f577-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f577-254">Is-Single-Valued</span></span>       | <span data-ttu-id="8f577-255">True</span><span class="sxs-lookup"><span data-stu-id="8f577-255">True</span></span>                                                                |
| <span data-ttu-id="8f577-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f577-256">Is Indexed</span></span>             | <span data-ttu-id="8f577-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-257">False</span></span>                                                               |
| <span data-ttu-id="8f577-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f577-258">In Global Catalog</span></span>      | <span data-ttu-id="8f577-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f577-259">False</span></span>                                                               |
| <span data-ttu-id="8f577-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f577-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f577-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f577-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8f577-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f577-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f577-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8f577-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-264">Search-Flags</span></span>           | <span data-ttu-id="8f577-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f577-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="8f577-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f577-266">System-Flags</span></span>           | <span data-ttu-id="8f577-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f577-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="8f577-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f577-268">Classes used in</span></span>        | [<span data-ttu-id="8f577-269">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8f577-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





