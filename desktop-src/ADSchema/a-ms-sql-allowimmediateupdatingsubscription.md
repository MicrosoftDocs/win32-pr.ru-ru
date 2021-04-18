---
title: Атрибут MS-SQL-Алловиммедиатеупдатингсубскриптион
description: Значение true, если публикация разрешает синхронизированные транзакции обновляемые подписки.
ms.assetid: 7efa4b8f-77ad-4f68-9852-7dac9f922d95
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Алловиммедиатеупдатингсубскриптион
- Схема AD атрибута mS-SQL-Алловиммедиатеупдатингсубскриптион
topic_type:
- apiref
api_name:
- MS-SQL-AllowImmediateUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed7970aa4b4f26a7221ea9a0c3d4e279ddc5db1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535786"
---
# <a name="ms-sql-allowimmediateupdatingsubscription-attribute"></a><span data-ttu-id="fcb45-105">Атрибут MS-SQL-Алловиммедиатеупдатингсубскриптион</span><span class="sxs-lookup"><span data-stu-id="fcb45-105">MS-SQL-AllowImmediateUpdatingSubscription attribute</span></span>

<span data-ttu-id="fcb45-106">Значение true, если публикация разрешает синхронизированные транзакции обновляемые подписки.</span><span class="sxs-lookup"><span data-stu-id="fcb45-106">True if the publication allows synchronized transaction updating subscriptions.</span></span>



| <span data-ttu-id="fcb45-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-107">Entry</span></span> | <span data-ttu-id="fcb45-108">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="fcb45-109">CN</span><span class="sxs-lookup"><span data-stu-id="fcb45-109">CN</span></span>                | <span data-ttu-id="fcb45-110">MS-SQL-Алловиммедиатеупдатингсубскриптион</span><span class="sxs-lookup"><span data-stu-id="fcb45-110">MS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="fcb45-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fcb45-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fcb45-112">mS-SQL-Алловиммедиатеупдатингсубскриптион</span><span class="sxs-lookup"><span data-stu-id="fcb45-112">mS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="fcb45-113">Размер</span><span class="sxs-lookup"><span data-stu-id="fcb45-113">Size</span></span>              | <span data-ttu-id="fcb45-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="fcb45-114">4 bytes</span></span>                                   |
| <span data-ttu-id="fcb45-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fcb45-115">Update Privilege</span></span>  | <span data-ttu-id="fcb45-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="fcb45-116">This value is set by the system.</span></span>          |
| <span data-ttu-id="fcb45-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fcb45-117">Update Frequency</span></span>  | <span data-ttu-id="fcb45-118">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="fcb45-118">When replication is setup.</span></span>                |
| <span data-ttu-id="fcb45-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-119">Attribute-Id</span></span>      | <span data-ttu-id="fcb45-120">1.2.840.113556.1.4.1404</span><span class="sxs-lookup"><span data-stu-id="fcb45-120">1.2.840.113556.1.4.1404</span></span>                   |
| <span data-ttu-id="fcb45-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fcb45-121">System-Id-Guid</span></span>    | <span data-ttu-id="fcb45-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="fcb45-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span></span>      |
| <span data-ttu-id="fcb45-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcb45-123">Syntax</span></span>            | [<span data-ttu-id="fcb45-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="fcb45-124">**Boolean**</span></span>](s-boolean.md)              |



## <a name="implementations"></a><span data-ttu-id="fcb45-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fcb45-125">Implementations</span></span>

-   [<span data-ttu-id="fcb45-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fcb45-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fcb45-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fcb45-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fcb45-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fcb45-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fcb45-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fcb45-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fcb45-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fcb45-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fcb45-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fcb45-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fcb45-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fcb45-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fcb45-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-133">Entry</span></span> | <span data-ttu-id="fcb45-134">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcb45-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fcb45-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcb45-137">System-Only</span></span>            | <span data-ttu-id="fcb45-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-138">False</span></span>                                                               |
| <span data-ttu-id="fcb45-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fcb45-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fcb45-140">True</span><span class="sxs-lookup"><span data-stu-id="fcb45-140">True</span></span>                                                                |
| <span data-ttu-id="fcb45-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fcb45-141">Is Indexed</span></span>             | <span data-ttu-id="fcb45-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-142">False</span></span>                                                               |
| <span data-ttu-id="fcb45-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fcb45-143">In Global Catalog</span></span>      | <span data-ttu-id="fcb45-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-144">False</span></span>                                                               |
| <span data-ttu-id="fcb45-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fcb45-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcb45-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcb45-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fcb45-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcb45-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcb45-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-149">Search-Flags</span></span>           | <span data-ttu-id="fcb45-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcb45-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="fcb45-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-151">System-Flags</span></span>           | <span data-ttu-id="fcb45-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcb45-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="fcb45-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fcb45-153">Classes used in</span></span>        | [<span data-ttu-id="fcb45-154">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="fcb45-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fcb45-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fcb45-155">Windows Server 2003</span></span>



| <span data-ttu-id="fcb45-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-156">Entry</span></span> | <span data-ttu-id="fcb45-157">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcb45-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fcb45-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcb45-160">System-Only</span></span>            | <span data-ttu-id="fcb45-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-161">False</span></span>                                                               |
| <span data-ttu-id="fcb45-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fcb45-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fcb45-163">True</span><span class="sxs-lookup"><span data-stu-id="fcb45-163">True</span></span>                                                                |
| <span data-ttu-id="fcb45-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fcb45-164">Is Indexed</span></span>             | <span data-ttu-id="fcb45-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-165">False</span></span>                                                               |
| <span data-ttu-id="fcb45-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fcb45-166">In Global Catalog</span></span>      | <span data-ttu-id="fcb45-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-167">False</span></span>                                                               |
| <span data-ttu-id="fcb45-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fcb45-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcb45-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcb45-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fcb45-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcb45-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcb45-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-172">Search-Flags</span></span>           | <span data-ttu-id="fcb45-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcb45-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="fcb45-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-174">System-Flags</span></span>           | <span data-ttu-id="fcb45-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcb45-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="fcb45-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fcb45-176">Classes used in</span></span>        | [<span data-ttu-id="fcb45-177">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="fcb45-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fcb45-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fcb45-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fcb45-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-179">Entry</span></span> | <span data-ttu-id="fcb45-180">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcb45-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fcb45-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcb45-183">System-Only</span></span>            | <span data-ttu-id="fcb45-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-184">False</span></span>                                                               |
| <span data-ttu-id="fcb45-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fcb45-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fcb45-186">True</span><span class="sxs-lookup"><span data-stu-id="fcb45-186">True</span></span>                                                                |
| <span data-ttu-id="fcb45-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fcb45-187">Is Indexed</span></span>             | <span data-ttu-id="fcb45-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-188">False</span></span>                                                               |
| <span data-ttu-id="fcb45-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fcb45-189">In Global Catalog</span></span>      | <span data-ttu-id="fcb45-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-190">False</span></span>                                                               |
| <span data-ttu-id="fcb45-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fcb45-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcb45-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcb45-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fcb45-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcb45-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcb45-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-195">Search-Flags</span></span>           | <span data-ttu-id="fcb45-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcb45-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="fcb45-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-197">System-Flags</span></span>           | <span data-ttu-id="fcb45-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcb45-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="fcb45-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fcb45-199">Classes used in</span></span>        | [<span data-ttu-id="fcb45-200">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="fcb45-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fcb45-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcb45-201">Windows Server 2008</span></span>



| <span data-ttu-id="fcb45-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-202">Entry</span></span> | <span data-ttu-id="fcb45-203">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcb45-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fcb45-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcb45-206">System-Only</span></span>            | <span data-ttu-id="fcb45-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-207">False</span></span>                                                               |
| <span data-ttu-id="fcb45-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fcb45-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fcb45-209">True</span><span class="sxs-lookup"><span data-stu-id="fcb45-209">True</span></span>                                                                |
| <span data-ttu-id="fcb45-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fcb45-210">Is Indexed</span></span>             | <span data-ttu-id="fcb45-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-211">False</span></span>                                                               |
| <span data-ttu-id="fcb45-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fcb45-212">In Global Catalog</span></span>      | <span data-ttu-id="fcb45-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-213">False</span></span>                                                               |
| <span data-ttu-id="fcb45-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fcb45-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcb45-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcb45-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fcb45-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcb45-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcb45-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-218">Search-Flags</span></span>           | <span data-ttu-id="fcb45-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcb45-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="fcb45-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-220">System-Flags</span></span>           | <span data-ttu-id="fcb45-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcb45-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="fcb45-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fcb45-222">Classes used in</span></span>        | [<span data-ttu-id="fcb45-223">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="fcb45-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fcb45-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fcb45-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fcb45-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-225">Entry</span></span> | <span data-ttu-id="fcb45-226">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcb45-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fcb45-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcb45-229">System-Only</span></span>            | <span data-ttu-id="fcb45-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-230">False</span></span>                                                               |
| <span data-ttu-id="fcb45-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fcb45-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fcb45-232">True</span><span class="sxs-lookup"><span data-stu-id="fcb45-232">True</span></span>                                                                |
| <span data-ttu-id="fcb45-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fcb45-233">Is Indexed</span></span>             | <span data-ttu-id="fcb45-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-234">False</span></span>                                                               |
| <span data-ttu-id="fcb45-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fcb45-235">In Global Catalog</span></span>      | <span data-ttu-id="fcb45-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-236">False</span></span>                                                               |
| <span data-ttu-id="fcb45-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fcb45-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcb45-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcb45-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fcb45-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcb45-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcb45-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-241">Search-Flags</span></span>           | <span data-ttu-id="fcb45-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcb45-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="fcb45-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-243">System-Flags</span></span>           | <span data-ttu-id="fcb45-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcb45-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="fcb45-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fcb45-245">Classes used in</span></span>        | [<span data-ttu-id="fcb45-246">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="fcb45-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fcb45-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcb45-247">Windows Server 2012</span></span>



| <span data-ttu-id="fcb45-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="fcb45-248">Entry</span></span> | <span data-ttu-id="fcb45-249">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb45-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcb45-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fcb45-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcb45-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fcb45-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcb45-252">System-Only</span></span>            | <span data-ttu-id="fcb45-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-253">False</span></span>                                                               |
| <span data-ttu-id="fcb45-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fcb45-254">Is-Single-Valued</span></span>       | <span data-ttu-id="fcb45-255">True</span><span class="sxs-lookup"><span data-stu-id="fcb45-255">True</span></span>                                                                |
| <span data-ttu-id="fcb45-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fcb45-256">Is Indexed</span></span>             | <span data-ttu-id="fcb45-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-257">False</span></span>                                                               |
| <span data-ttu-id="fcb45-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fcb45-258">In Global Catalog</span></span>      | <span data-ttu-id="fcb45-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="fcb45-259">False</span></span>                                                               |
| <span data-ttu-id="fcb45-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fcb45-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcb45-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcb45-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fcb45-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcb45-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcb45-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fcb45-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-264">Search-Flags</span></span>           | <span data-ttu-id="fcb45-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcb45-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="fcb45-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcb45-266">System-Flags</span></span>           | <span data-ttu-id="fcb45-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcb45-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="fcb45-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fcb45-268">Classes used in</span></span>        | [<span data-ttu-id="fcb45-269">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="fcb45-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





