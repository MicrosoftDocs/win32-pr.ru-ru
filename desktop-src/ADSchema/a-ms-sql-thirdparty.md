---
title: Атрибут MS-SQL-сторонних
description: Этот атрибут указывает, относится ли данные публикации к источнику данных, отличному от SQL Server. Если это из другого источника, то ему присваивается значение TRUE.
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-сторонних
- Схема AD атрибута mS-SQL-сторонних
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804373"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="13ba1-106">Атрибут MS-SQL-сторонних</span><span class="sxs-lookup"><span data-stu-id="13ba1-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="13ba1-107">Этот атрибут указывает, относится ли данные публикации к источнику данных, отличному от SQL Server.</span><span class="sxs-lookup"><span data-stu-id="13ba1-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="13ba1-108">Если это из другого источника, то ему присваивается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="13ba1-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="13ba1-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-109">Entry</span></span> | <span data-ttu-id="13ba1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="13ba1-111">CN</span><span class="sxs-lookup"><span data-stu-id="13ba1-111">CN</span></span>                | <span data-ttu-id="13ba1-112">MS-SQL-сторонних</span><span class="sxs-lookup"><span data-stu-id="13ba1-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="13ba1-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="13ba1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="13ba1-114">mS-SQL-сторонних</span><span class="sxs-lookup"><span data-stu-id="13ba1-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="13ba1-115">Размер</span><span class="sxs-lookup"><span data-stu-id="13ba1-115">Size</span></span>              | <span data-ttu-id="13ba1-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="13ba1-116">4 bytes</span></span>                              |
| <span data-ttu-id="13ba1-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="13ba1-117">Update Privilege</span></span>  | <span data-ttu-id="13ba1-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="13ba1-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="13ba1-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="13ba1-119">Update Frequency</span></span>  | <span data-ttu-id="13ba1-120">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="13ba1-120">When replication is setup.</span></span>           |
| <span data-ttu-id="13ba1-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-121">Attribute-Id</span></span>      | <span data-ttu-id="13ba1-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="13ba1-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="13ba1-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="13ba1-123">System-Id-Guid</span></span>    | <span data-ttu-id="13ba1-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="13ba1-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="13ba1-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13ba1-125">Syntax</span></span>            | [<span data-ttu-id="13ba1-126">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="13ba1-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="13ba1-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="13ba1-127">Implementations</span></span>

-   [<span data-ttu-id="13ba1-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13ba1-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13ba1-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13ba1-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13ba1-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13ba1-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13ba1-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13ba1-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13ba1-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13ba1-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13ba1-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13ba1-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13ba1-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13ba1-134">Windows 2000 Server</span></span>



| <span data-ttu-id="13ba1-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-135">Entry</span></span> | <span data-ttu-id="13ba1-136">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13ba1-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13ba1-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="13ba1-139">System-Only</span></span>            | <span data-ttu-id="13ba1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-140">False</span></span>                                                               |
| <span data-ttu-id="13ba1-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13ba1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="13ba1-142">True</span><span class="sxs-lookup"><span data-stu-id="13ba1-142">True</span></span>                                                                |
| <span data-ttu-id="13ba1-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13ba1-143">Is Indexed</span></span>             | <span data-ttu-id="13ba1-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-144">False</span></span>                                                               |
| <span data-ttu-id="13ba1-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13ba1-145">In Global Catalog</span></span>      | <span data-ttu-id="13ba1-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-146">False</span></span>                                                               |
| <span data-ttu-id="13ba1-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13ba1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="13ba1-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13ba1-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="13ba1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13ba1-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13ba1-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-151">Search-Flags</span></span>           | <span data-ttu-id="13ba1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13ba1-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="13ba1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-153">System-Flags</span></span>           | <span data-ttu-id="13ba1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13ba1-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="13ba1-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13ba1-155">Classes used in</span></span>        | [<span data-ttu-id="13ba1-156">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="13ba1-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13ba1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13ba1-157">Windows Server 2003</span></span>



| <span data-ttu-id="13ba1-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-158">Entry</span></span> | <span data-ttu-id="13ba1-159">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13ba1-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13ba1-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="13ba1-162">System-Only</span></span>            | <span data-ttu-id="13ba1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-163">False</span></span>                                                               |
| <span data-ttu-id="13ba1-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13ba1-164">Is-Single-Valued</span></span>       | <span data-ttu-id="13ba1-165">True</span><span class="sxs-lookup"><span data-stu-id="13ba1-165">True</span></span>                                                                |
| <span data-ttu-id="13ba1-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13ba1-166">Is Indexed</span></span>             | <span data-ttu-id="13ba1-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-167">False</span></span>                                                               |
| <span data-ttu-id="13ba1-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13ba1-168">In Global Catalog</span></span>      | <span data-ttu-id="13ba1-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-169">False</span></span>                                                               |
| <span data-ttu-id="13ba1-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13ba1-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="13ba1-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13ba1-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="13ba1-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13ba1-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13ba1-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-174">Search-Flags</span></span>           | <span data-ttu-id="13ba1-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13ba1-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="13ba1-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-176">System-Flags</span></span>           | <span data-ttu-id="13ba1-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13ba1-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="13ba1-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13ba1-178">Classes used in</span></span>        | [<span data-ttu-id="13ba1-179">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="13ba1-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13ba1-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13ba1-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13ba1-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-181">Entry</span></span> | <span data-ttu-id="13ba1-182">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13ba1-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13ba1-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="13ba1-185">System-Only</span></span>            | <span data-ttu-id="13ba1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-186">False</span></span>                                                               |
| <span data-ttu-id="13ba1-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13ba1-187">Is-Single-Valued</span></span>       | <span data-ttu-id="13ba1-188">True</span><span class="sxs-lookup"><span data-stu-id="13ba1-188">True</span></span>                                                                |
| <span data-ttu-id="13ba1-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13ba1-189">Is Indexed</span></span>             | <span data-ttu-id="13ba1-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-190">False</span></span>                                                               |
| <span data-ttu-id="13ba1-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13ba1-191">In Global Catalog</span></span>      | <span data-ttu-id="13ba1-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-192">False</span></span>                                                               |
| <span data-ttu-id="13ba1-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13ba1-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="13ba1-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13ba1-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="13ba1-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13ba1-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13ba1-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-197">Search-Flags</span></span>           | <span data-ttu-id="13ba1-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13ba1-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="13ba1-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-199">System-Flags</span></span>           | <span data-ttu-id="13ba1-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13ba1-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="13ba1-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13ba1-201">Classes used in</span></span>        | [<span data-ttu-id="13ba1-202">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="13ba1-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13ba1-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13ba1-203">Windows Server 2008</span></span>



| <span data-ttu-id="13ba1-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-204">Entry</span></span> | <span data-ttu-id="13ba1-205">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13ba1-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13ba1-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="13ba1-208">System-Only</span></span>            | <span data-ttu-id="13ba1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-209">False</span></span>                                                               |
| <span data-ttu-id="13ba1-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13ba1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="13ba1-211">True</span><span class="sxs-lookup"><span data-stu-id="13ba1-211">True</span></span>                                                                |
| <span data-ttu-id="13ba1-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13ba1-212">Is Indexed</span></span>             | <span data-ttu-id="13ba1-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-213">False</span></span>                                                               |
| <span data-ttu-id="13ba1-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13ba1-214">In Global Catalog</span></span>      | <span data-ttu-id="13ba1-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-215">False</span></span>                                                               |
| <span data-ttu-id="13ba1-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13ba1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="13ba1-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13ba1-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="13ba1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13ba1-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13ba1-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-220">Search-Flags</span></span>           | <span data-ttu-id="13ba1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13ba1-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="13ba1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-222">System-Flags</span></span>           | <span data-ttu-id="13ba1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13ba1-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="13ba1-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13ba1-224">Classes used in</span></span>        | [<span data-ttu-id="13ba1-225">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="13ba1-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13ba1-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13ba1-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13ba1-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-227">Entry</span></span> | <span data-ttu-id="13ba1-228">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13ba1-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13ba1-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="13ba1-231">System-Only</span></span>            | <span data-ttu-id="13ba1-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-232">False</span></span>                                                               |
| <span data-ttu-id="13ba1-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13ba1-233">Is-Single-Valued</span></span>       | <span data-ttu-id="13ba1-234">True</span><span class="sxs-lookup"><span data-stu-id="13ba1-234">True</span></span>                                                                |
| <span data-ttu-id="13ba1-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13ba1-235">Is Indexed</span></span>             | <span data-ttu-id="13ba1-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-236">False</span></span>                                                               |
| <span data-ttu-id="13ba1-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13ba1-237">In Global Catalog</span></span>      | <span data-ttu-id="13ba1-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-238">False</span></span>                                                               |
| <span data-ttu-id="13ba1-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13ba1-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="13ba1-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13ba1-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="13ba1-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13ba1-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13ba1-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-243">Search-Flags</span></span>           | <span data-ttu-id="13ba1-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13ba1-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="13ba1-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-245">System-Flags</span></span>           | <span data-ttu-id="13ba1-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13ba1-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="13ba1-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13ba1-247">Classes used in</span></span>        | [<span data-ttu-id="13ba1-248">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="13ba1-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13ba1-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13ba1-249">Windows Server 2012</span></span>



| <span data-ttu-id="13ba1-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="13ba1-250">Entry</span></span> | <span data-ttu-id="13ba1-251">Значение</span><span class="sxs-lookup"><span data-stu-id="13ba1-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13ba1-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13ba1-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13ba1-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="13ba1-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="13ba1-254">System-Only</span></span>            | <span data-ttu-id="13ba1-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-255">False</span></span>                                                               |
| <span data-ttu-id="13ba1-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13ba1-256">Is-Single-Valued</span></span>       | <span data-ttu-id="13ba1-257">True</span><span class="sxs-lookup"><span data-stu-id="13ba1-257">True</span></span>                                                                |
| <span data-ttu-id="13ba1-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13ba1-258">Is Indexed</span></span>             | <span data-ttu-id="13ba1-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-259">False</span></span>                                                               |
| <span data-ttu-id="13ba1-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13ba1-260">In Global Catalog</span></span>      | <span data-ttu-id="13ba1-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="13ba1-261">False</span></span>                                                               |
| <span data-ttu-id="13ba1-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13ba1-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="13ba1-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13ba1-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="13ba1-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13ba1-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13ba1-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="13ba1-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-266">Search-Flags</span></span>           | <span data-ttu-id="13ba1-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13ba1-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="13ba1-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13ba1-268">System-Flags</span></span>           | <span data-ttu-id="13ba1-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13ba1-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="13ba1-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13ba1-270">Classes used in</span></span>        | [<span data-ttu-id="13ba1-271">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="13ba1-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





