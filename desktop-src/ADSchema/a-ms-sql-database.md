---
title: MS-SQL-атрибут базы данных
description: Имя базы данных SQL Server, участвующей в репликации.
ms.assetid: 624705d9-df3f-458e-98f4-fb8da073efd6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута базы данных MS-SQL
- Схема AD атрибута базы данных mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Database
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6c448213bee18fede3cc8a77cabf607c3b2ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893054"
---
# <a name="ms-sql-database-attribute"></a><span data-ttu-id="7c6a2-105">MS-SQL-атрибут базы данных</span><span class="sxs-lookup"><span data-stu-id="7c6a2-105">MS-SQL-Database attribute</span></span>

<span data-ttu-id="7c6a2-106">Имя базы данных SQL Server, участвующей в репликации.</span><span class="sxs-lookup"><span data-stu-id="7c6a2-106">The name of the SQL Server database involved in replication.</span></span>



| <span data-ttu-id="7c6a2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-107">Entry</span></span> | <span data-ttu-id="7c6a2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7c6a2-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c6a2-109">CN</span></span>                | <span data-ttu-id="7c6a2-110">База данных MS-SQL</span><span class="sxs-lookup"><span data-stu-id="7c6a2-110">MS-SQL-Database</span></span>                             |
| <span data-ttu-id="7c6a2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7c6a2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7c6a2-112">База данных mS-SQL</span><span class="sxs-lookup"><span data-stu-id="7c6a2-112">mS-SQL-Database</span></span>                             |
| <span data-ttu-id="7c6a2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7c6a2-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7c6a2-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7c6a2-114">Update Privilege</span></span>  | <span data-ttu-id="7c6a2-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="7c6a2-115">Domain administrator</span></span>                        |
| <span data-ttu-id="7c6a2-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7c6a2-116">Update Frequency</span></span>  | <span data-ttu-id="7c6a2-117">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="7c6a2-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="7c6a2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-118">Attribute-Id</span></span>      | <span data-ttu-id="7c6a2-119">1.2.840.113556.1.4.1393</span><span class="sxs-lookup"><span data-stu-id="7c6a2-119">1.2.840.113556.1.4.1393</span></span>                     |
| <span data-ttu-id="7c6a2-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7c6a2-120">System-Id-Guid</span></span>    | <span data-ttu-id="7c6a2-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7c6a2-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="7c6a2-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c6a2-122">Syntax</span></span>            | [<span data-ttu-id="7c6a2-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7c6a2-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7c6a2-124">Implementations</span></span>

-   [<span data-ttu-id="7c6a2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7c6a2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c6a2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c6a2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c6a2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c6a2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7c6a2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c6a2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7c6a2-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-132">Entry</span></span> | <span data-ttu-id="7c6a2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c6a2-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6a2-136">System-Only</span></span>            | <span data-ttu-id="7c6a2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c6a2-137">False</span></span>                                                               |
| <span data-ttu-id="7c6a2-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c6a2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6a2-139">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-139">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c6a2-140">Is Indexed</span></span>             | <span data-ttu-id="7c6a2-141">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-141">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c6a2-142">In Global Catalog</span></span>      | <span data-ttu-id="7c6a2-143">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-143">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c6a2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6a2-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c6a2-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7c6a2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6a2-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6a2-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-148">Search-Flags</span></span>           | <span data-ttu-id="7c6a2-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6a2-149">0x00000001</span></span>                                                          |
| <span data-ttu-id="7c6a2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-150">System-Flags</span></span>           | <span data-ttu-id="7c6a2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6a2-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="7c6a2-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c6a2-152">Classes used in</span></span>        | [<span data-ttu-id="7c6a2-153">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7c6a2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c6a2-154">Windows Server 2003</span></span>



| <span data-ttu-id="7c6a2-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-155">Entry</span></span> | <span data-ttu-id="7c6a2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c6a2-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6a2-159">System-Only</span></span>            | <span data-ttu-id="7c6a2-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c6a2-160">False</span></span>                                                               |
| <span data-ttu-id="7c6a2-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c6a2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6a2-162">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-162">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c6a2-163">Is Indexed</span></span>             | <span data-ttu-id="7c6a2-164">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-164">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c6a2-165">In Global Catalog</span></span>      | <span data-ttu-id="7c6a2-166">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-166">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c6a2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6a2-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c6a2-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7c6a2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6a2-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6a2-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-171">Search-Flags</span></span>           | <span data-ttu-id="7c6a2-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6a2-172">0x00000001</span></span>                                                          |
| <span data-ttu-id="7c6a2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-173">System-Flags</span></span>           | <span data-ttu-id="7c6a2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6a2-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="7c6a2-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c6a2-175">Classes used in</span></span>        | [<span data-ttu-id="7c6a2-176">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c6a2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c6a2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c6a2-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-178">Entry</span></span> | <span data-ttu-id="7c6a2-179">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c6a2-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6a2-182">System-Only</span></span>            | <span data-ttu-id="7c6a2-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c6a2-183">False</span></span>                                                               |
| <span data-ttu-id="7c6a2-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c6a2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6a2-185">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-185">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c6a2-186">Is Indexed</span></span>             | <span data-ttu-id="7c6a2-187">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-187">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c6a2-188">In Global Catalog</span></span>      | <span data-ttu-id="7c6a2-189">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-189">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c6a2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6a2-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c6a2-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7c6a2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6a2-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6a2-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-194">Search-Flags</span></span>           | <span data-ttu-id="7c6a2-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6a2-195">0x00000001</span></span>                                                          |
| <span data-ttu-id="7c6a2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-196">System-Flags</span></span>           | <span data-ttu-id="7c6a2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6a2-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="7c6a2-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c6a2-198">Classes used in</span></span>        | [<span data-ttu-id="7c6a2-199">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c6a2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c6a2-200">Windows Server 2008</span></span>



| <span data-ttu-id="7c6a2-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-201">Entry</span></span> | <span data-ttu-id="7c6a2-202">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c6a2-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6a2-205">System-Only</span></span>            | <span data-ttu-id="7c6a2-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c6a2-206">False</span></span>                                                               |
| <span data-ttu-id="7c6a2-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c6a2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6a2-208">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-208">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c6a2-209">Is Indexed</span></span>             | <span data-ttu-id="7c6a2-210">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-210">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c6a2-211">In Global Catalog</span></span>      | <span data-ttu-id="7c6a2-212">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-212">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c6a2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6a2-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c6a2-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7c6a2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6a2-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6a2-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-217">Search-Flags</span></span>           | <span data-ttu-id="7c6a2-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6a2-218">0x00000001</span></span>                                                          |
| <span data-ttu-id="7c6a2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-219">System-Flags</span></span>           | <span data-ttu-id="7c6a2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6a2-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="7c6a2-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c6a2-221">Classes used in</span></span>        | [<span data-ttu-id="7c6a2-222">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c6a2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c6a2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c6a2-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-224">Entry</span></span> | <span data-ttu-id="7c6a2-225">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c6a2-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6a2-228">System-Only</span></span>            | <span data-ttu-id="7c6a2-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c6a2-229">False</span></span>                                                               |
| <span data-ttu-id="7c6a2-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c6a2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6a2-231">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-231">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c6a2-232">Is Indexed</span></span>             | <span data-ttu-id="7c6a2-233">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-233">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c6a2-234">In Global Catalog</span></span>      | <span data-ttu-id="7c6a2-235">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-235">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c6a2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6a2-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c6a2-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7c6a2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6a2-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6a2-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-240">Search-Flags</span></span>           | <span data-ttu-id="7c6a2-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6a2-241">0x00000001</span></span>                                                          |
| <span data-ttu-id="7c6a2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-242">System-Flags</span></span>           | <span data-ttu-id="7c6a2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6a2-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="7c6a2-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c6a2-244">Classes used in</span></span>        | [<span data-ttu-id="7c6a2-245">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c6a2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c6a2-246">Windows Server 2012</span></span>



| <span data-ttu-id="7c6a2-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c6a2-247">Entry</span></span> | <span data-ttu-id="7c6a2-248">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c6a2-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6a2-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7c6a2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6a2-251">System-Only</span></span>            | <span data-ttu-id="7c6a2-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c6a2-252">False</span></span>                                                               |
| <span data-ttu-id="7c6a2-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c6a2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6a2-254">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-254">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c6a2-255">Is Indexed</span></span>             | <span data-ttu-id="7c6a2-256">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-256">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c6a2-257">In Global Catalog</span></span>      | <span data-ttu-id="7c6a2-258">True</span><span class="sxs-lookup"><span data-stu-id="7c6a2-258">True</span></span>                                                                |
| <span data-ttu-id="7c6a2-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c6a2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6a2-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c6a2-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7c6a2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6a2-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6a2-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7c6a2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-263">Search-Flags</span></span>           | <span data-ttu-id="7c6a2-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6a2-264">0x00000001</span></span>                                                          |
| <span data-ttu-id="7c6a2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6a2-265">System-Flags</span></span>           | <span data-ttu-id="7c6a2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6a2-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="7c6a2-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c6a2-267">Classes used in</span></span>        | [<span data-ttu-id="7c6a2-268">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="7c6a2-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





