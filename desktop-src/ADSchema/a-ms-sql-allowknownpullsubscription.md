---
title: Атрибут MS-SQL-Алловкновнпуллсубскриптион
description: Значение true, если публикация позволяет зарегистрированным подписчикам подписываться.
ms.assetid: be3b618e-bdf5-4bb4-ac4d-51dc97e73408
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Алловкновнпуллсубскриптион
- Схема AD атрибута mS-SQL-Алловкновнпуллсубскриптион
topic_type:
- apiref
api_name:
- MS-SQL-AllowKnownPullSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07789bf68f470db69219765628ebc82b2014428
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893913"
---
# <a name="ms-sql-allowknownpullsubscription-attribute"></a><span data-ttu-id="087a3-105">Атрибут MS-SQL-Алловкновнпуллсубскриптион</span><span class="sxs-lookup"><span data-stu-id="087a3-105">MS-SQL-AllowKnownPullSubscription attribute</span></span>

<span data-ttu-id="087a3-106">Значение true, если публикация позволяет зарегистрированным подписчикам подписываться.</span><span class="sxs-lookup"><span data-stu-id="087a3-106">True if the publication allows registered subscribers to subscribe.</span></span>



| <span data-ttu-id="087a3-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-107">Entry</span></span> | <span data-ttu-id="087a3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="087a3-109">CN</span><span class="sxs-lookup"><span data-stu-id="087a3-109">CN</span></span>                | <span data-ttu-id="087a3-110">MS-SQL-Алловкновнпуллсубскриптион</span><span class="sxs-lookup"><span data-stu-id="087a3-110">MS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="087a3-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="087a3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="087a3-112">mS-SQL-Алловкновнпуллсубскриптион</span><span class="sxs-lookup"><span data-stu-id="087a3-112">mS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="087a3-113">Размер</span><span class="sxs-lookup"><span data-stu-id="087a3-113">Size</span></span>              | <span data-ttu-id="087a3-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="087a3-114">4 bytes</span></span>                              |
| <span data-ttu-id="087a3-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="087a3-115">Update Privilege</span></span>  | <span data-ttu-id="087a3-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="087a3-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="087a3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="087a3-117">Update Frequency</span></span>  | <span data-ttu-id="087a3-118">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="087a3-118">When replication is setup.</span></span>           |
| <span data-ttu-id="087a3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-119">Attribute-Id</span></span>      | <span data-ttu-id="087a3-120">1.2.840.113556.1.4.1403</span><span class="sxs-lookup"><span data-stu-id="087a3-120">1.2.840.113556.1.4.1403</span></span>              |
| <span data-ttu-id="087a3-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="087a3-121">System-Id-Guid</span></span>    | <span data-ttu-id="087a3-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="087a3-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="087a3-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="087a3-123">Syntax</span></span>            | [<span data-ttu-id="087a3-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="087a3-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="087a3-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="087a3-125">Implementations</span></span>

-   [<span data-ttu-id="087a3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="087a3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="087a3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="087a3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="087a3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="087a3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="087a3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="087a3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="087a3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="087a3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="087a3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="087a3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="087a3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="087a3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="087a3-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-133">Entry</span></span> | <span data-ttu-id="087a3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="087a3-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="087a3-137">System-Only</span></span>            | <span data-ttu-id="087a3-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-138">False</span></span>                                                               |
| <span data-ttu-id="087a3-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="087a3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="087a3-140">True</span><span class="sxs-lookup"><span data-stu-id="087a3-140">True</span></span>                                                                |
| <span data-ttu-id="087a3-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="087a3-141">Is Indexed</span></span>             | <span data-ttu-id="087a3-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-142">False</span></span>                                                               |
| <span data-ttu-id="087a3-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="087a3-143">In Global Catalog</span></span>      | <span data-ttu-id="087a3-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-144">False</span></span>                                                               |
| <span data-ttu-id="087a3-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="087a3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="087a3-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="087a3-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="087a3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="087a3-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="087a3-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-149">Search-Flags</span></span>           | <span data-ttu-id="087a3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="087a3-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="087a3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-151">System-Flags</span></span>           | <span data-ttu-id="087a3-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="087a3-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="087a3-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="087a3-153">Classes used in</span></span>        | [<span data-ttu-id="087a3-154">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="087a3-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="087a3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="087a3-155">Windows Server 2003</span></span>



| <span data-ttu-id="087a3-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-156">Entry</span></span> | <span data-ttu-id="087a3-157">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="087a3-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="087a3-160">System-Only</span></span>            | <span data-ttu-id="087a3-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-161">False</span></span>                                                               |
| <span data-ttu-id="087a3-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="087a3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="087a3-163">True</span><span class="sxs-lookup"><span data-stu-id="087a3-163">True</span></span>                                                                |
| <span data-ttu-id="087a3-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="087a3-164">Is Indexed</span></span>             | <span data-ttu-id="087a3-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-165">False</span></span>                                                               |
| <span data-ttu-id="087a3-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="087a3-166">In Global Catalog</span></span>      | <span data-ttu-id="087a3-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-167">False</span></span>                                                               |
| <span data-ttu-id="087a3-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="087a3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="087a3-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="087a3-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="087a3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="087a3-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="087a3-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-172">Search-Flags</span></span>           | <span data-ttu-id="087a3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="087a3-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="087a3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-174">System-Flags</span></span>           | <span data-ttu-id="087a3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="087a3-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="087a3-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="087a3-176">Classes used in</span></span>        | [<span data-ttu-id="087a3-177">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="087a3-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="087a3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="087a3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="087a3-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-179">Entry</span></span> | <span data-ttu-id="087a3-180">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="087a3-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="087a3-183">System-Only</span></span>            | <span data-ttu-id="087a3-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-184">False</span></span>                                                               |
| <span data-ttu-id="087a3-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="087a3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="087a3-186">True</span><span class="sxs-lookup"><span data-stu-id="087a3-186">True</span></span>                                                                |
| <span data-ttu-id="087a3-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="087a3-187">Is Indexed</span></span>             | <span data-ttu-id="087a3-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-188">False</span></span>                                                               |
| <span data-ttu-id="087a3-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="087a3-189">In Global Catalog</span></span>      | <span data-ttu-id="087a3-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-190">False</span></span>                                                               |
| <span data-ttu-id="087a3-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="087a3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="087a3-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="087a3-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="087a3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="087a3-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="087a3-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-195">Search-Flags</span></span>           | <span data-ttu-id="087a3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="087a3-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="087a3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-197">System-Flags</span></span>           | <span data-ttu-id="087a3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="087a3-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="087a3-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="087a3-199">Classes used in</span></span>        | [<span data-ttu-id="087a3-200">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="087a3-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="087a3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="087a3-201">Windows Server 2008</span></span>



| <span data-ttu-id="087a3-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-202">Entry</span></span> | <span data-ttu-id="087a3-203">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="087a3-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="087a3-206">System-Only</span></span>            | <span data-ttu-id="087a3-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-207">False</span></span>                                                               |
| <span data-ttu-id="087a3-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="087a3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="087a3-209">True</span><span class="sxs-lookup"><span data-stu-id="087a3-209">True</span></span>                                                                |
| <span data-ttu-id="087a3-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="087a3-210">Is Indexed</span></span>             | <span data-ttu-id="087a3-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-211">False</span></span>                                                               |
| <span data-ttu-id="087a3-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="087a3-212">In Global Catalog</span></span>      | <span data-ttu-id="087a3-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-213">False</span></span>                                                               |
| <span data-ttu-id="087a3-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="087a3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="087a3-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="087a3-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="087a3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="087a3-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="087a3-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-218">Search-Flags</span></span>           | <span data-ttu-id="087a3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="087a3-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="087a3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-220">System-Flags</span></span>           | <span data-ttu-id="087a3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="087a3-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="087a3-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="087a3-222">Classes used in</span></span>        | [<span data-ttu-id="087a3-223">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="087a3-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="087a3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="087a3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="087a3-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-225">Entry</span></span> | <span data-ttu-id="087a3-226">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="087a3-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="087a3-229">System-Only</span></span>            | <span data-ttu-id="087a3-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-230">False</span></span>                                                               |
| <span data-ttu-id="087a3-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="087a3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="087a3-232">True</span><span class="sxs-lookup"><span data-stu-id="087a3-232">True</span></span>                                                                |
| <span data-ttu-id="087a3-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="087a3-233">Is Indexed</span></span>             | <span data-ttu-id="087a3-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-234">False</span></span>                                                               |
| <span data-ttu-id="087a3-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="087a3-235">In Global Catalog</span></span>      | <span data-ttu-id="087a3-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-236">False</span></span>                                                               |
| <span data-ttu-id="087a3-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="087a3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="087a3-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="087a3-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="087a3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="087a3-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="087a3-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-241">Search-Flags</span></span>           | <span data-ttu-id="087a3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="087a3-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="087a3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-243">System-Flags</span></span>           | <span data-ttu-id="087a3-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="087a3-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="087a3-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="087a3-245">Classes used in</span></span>        | [<span data-ttu-id="087a3-246">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="087a3-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="087a3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="087a3-247">Windows Server 2012</span></span>



| <span data-ttu-id="087a3-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="087a3-248">Entry</span></span> | <span data-ttu-id="087a3-249">Значение</span><span class="sxs-lookup"><span data-stu-id="087a3-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="087a3-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="087a3-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="087a3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="087a3-252">System-Only</span></span>            | <span data-ttu-id="087a3-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-253">False</span></span>                                                               |
| <span data-ttu-id="087a3-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="087a3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="087a3-255">True</span><span class="sxs-lookup"><span data-stu-id="087a3-255">True</span></span>                                                                |
| <span data-ttu-id="087a3-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="087a3-256">Is Indexed</span></span>             | <span data-ttu-id="087a3-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-257">False</span></span>                                                               |
| <span data-ttu-id="087a3-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="087a3-258">In Global Catalog</span></span>      | <span data-ttu-id="087a3-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="087a3-259">False</span></span>                                                               |
| <span data-ttu-id="087a3-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="087a3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="087a3-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="087a3-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="087a3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="087a3-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="087a3-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="087a3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-264">Search-Flags</span></span>           | <span data-ttu-id="087a3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="087a3-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="087a3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="087a3-266">System-Flags</span></span>           | <span data-ttu-id="087a3-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="087a3-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="087a3-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="087a3-268">Classes used in</span></span>        | [<span data-ttu-id="087a3-269">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="087a3-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





