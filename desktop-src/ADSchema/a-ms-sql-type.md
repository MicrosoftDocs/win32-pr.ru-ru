---
title: Атрибут типа MS-SQL
description: Тип репликации, используемый этим сервером SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута типа MS-SQL
- Схема AD атрибута типа mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893897"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="cf0ae-105">Атрибут типа MS-SQL</span><span class="sxs-lookup"><span data-stu-id="cf0ae-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="cf0ae-106">Тип репликации, используемый этим сервером SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="cf0ae-107">Для этого атрибута возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="cf0ae-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-108">Value</span></span>        | <span data-ttu-id="cf0ae-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cf0ae-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="cf0ae-110">0</span><span class="sxs-lookup"><span data-stu-id="cf0ae-110">0</span></span><br/> | <span data-ttu-id="cf0ae-111">Репликация транзакций.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="cf0ae-112">1</span><span class="sxs-lookup"><span data-stu-id="cf0ae-112">1</span></span><br/> | <span data-ttu-id="cf0ae-113">Репликация моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="cf0ae-114">2</span><span class="sxs-lookup"><span data-stu-id="cf0ae-114">2</span></span><br/> | <span data-ttu-id="cf0ae-115">Репликация слиянием.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="cf0ae-116">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-116">Entry</span></span> | <span data-ttu-id="cf0ae-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cf0ae-118">CN</span><span class="sxs-lookup"><span data-stu-id="cf0ae-118">CN</span></span>                | <span data-ttu-id="cf0ae-119">Тип MS-SQL</span><span class="sxs-lookup"><span data-stu-id="cf0ae-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="cf0ae-120">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cf0ae-120">Ldap-Display-Name</span></span> | <span data-ttu-id="cf0ae-121">Тип mS-SQL</span><span class="sxs-lookup"><span data-stu-id="cf0ae-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="cf0ae-122">Размер</span><span class="sxs-lookup"><span data-stu-id="cf0ae-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="cf0ae-123">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cf0ae-123">Update Privilege</span></span>  | <span data-ttu-id="cf0ae-124">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="cf0ae-124">Domain administrator</span></span>                        |
| <span data-ttu-id="cf0ae-125">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cf0ae-125">Update Frequency</span></span>  | <span data-ttu-id="cf0ae-126">При настройке репликации.</span><span class="sxs-lookup"><span data-stu-id="cf0ae-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="cf0ae-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-127">Attribute-Id</span></span>      | <span data-ttu-id="cf0ae-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="cf0ae-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="cf0ae-129">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cf0ae-129">System-Id-Guid</span></span>    | <span data-ttu-id="cf0ae-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cf0ae-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="cf0ae-131">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf0ae-131">Syntax</span></span>            | [<span data-ttu-id="cf0ae-132">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cf0ae-133">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cf0ae-133">Implementations</span></span>

-   [<span data-ttu-id="cf0ae-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf0ae-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf0ae-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf0ae-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf0ae-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf0ae-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf0ae-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf0ae-140">Windows 2000 Server</span></span>



| <span data-ttu-id="cf0ae-141">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-141">Entry</span></span> | <span data-ttu-id="cf0ae-142">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0ae-143">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0ae-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0ae-145">System-Only</span></span>            | <span data-ttu-id="cf0ae-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-147">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0ae-147">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0ae-148">True</span><span class="sxs-lookup"><span data-stu-id="cf0ae-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="cf0ae-149">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0ae-149">Is Indexed</span></span>             | <span data-ttu-id="cf0ae-150">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-151">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0ae-151">In Global Catalog</span></span>      | <span data-ttu-id="cf0ae-152">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-153">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0ae-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0ae-154">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0ae-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="cf0ae-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0ae-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0ae-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-157">Search-Flags</span></span>           | <span data-ttu-id="cf0ae-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0ae-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-159">System-Flags</span></span>           | <span data-ttu-id="cf0ae-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0ae-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-161">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0ae-161">Classes used in</span></span>        | [<span data-ttu-id="cf0ae-162">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="cf0ae-163">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf0ae-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf0ae-164">Windows Server 2003</span></span>



| <span data-ttu-id="cf0ae-165">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-165">Entry</span></span> | <span data-ttu-id="cf0ae-166">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0ae-167">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0ae-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0ae-169">System-Only</span></span>            | <span data-ttu-id="cf0ae-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-171">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0ae-171">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0ae-172">True</span><span class="sxs-lookup"><span data-stu-id="cf0ae-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="cf0ae-173">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0ae-173">Is Indexed</span></span>             | <span data-ttu-id="cf0ae-174">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-175">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0ae-175">In Global Catalog</span></span>      | <span data-ttu-id="cf0ae-176">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-177">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0ae-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0ae-178">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0ae-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="cf0ae-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0ae-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0ae-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-181">Search-Flags</span></span>           | <span data-ttu-id="cf0ae-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0ae-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-183">System-Flags</span></span>           | <span data-ttu-id="cf0ae-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0ae-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-185">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0ae-185">Classes used in</span></span>        | [<span data-ttu-id="cf0ae-186">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="cf0ae-187">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf0ae-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf0ae-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf0ae-189">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-189">Entry</span></span> | <span data-ttu-id="cf0ae-190">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0ae-191">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0ae-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0ae-193">System-Only</span></span>            | <span data-ttu-id="cf0ae-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-195">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0ae-195">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0ae-196">True</span><span class="sxs-lookup"><span data-stu-id="cf0ae-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="cf0ae-197">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0ae-197">Is Indexed</span></span>             | <span data-ttu-id="cf0ae-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-199">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0ae-199">In Global Catalog</span></span>      | <span data-ttu-id="cf0ae-200">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-201">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0ae-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0ae-202">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0ae-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="cf0ae-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0ae-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0ae-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-205">Search-Flags</span></span>           | <span data-ttu-id="cf0ae-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0ae-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-207">System-Flags</span></span>           | <span data-ttu-id="cf0ae-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0ae-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0ae-209">Classes used in</span></span>        | [<span data-ttu-id="cf0ae-210">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="cf0ae-211">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf0ae-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf0ae-212">Windows Server 2008</span></span>



| <span data-ttu-id="cf0ae-213">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-213">Entry</span></span> | <span data-ttu-id="cf0ae-214">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0ae-215">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0ae-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0ae-217">System-Only</span></span>            | <span data-ttu-id="cf0ae-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0ae-219">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0ae-220">True</span><span class="sxs-lookup"><span data-stu-id="cf0ae-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="cf0ae-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0ae-221">Is Indexed</span></span>             | <span data-ttu-id="cf0ae-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0ae-223">In Global Catalog</span></span>      | <span data-ttu-id="cf0ae-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0ae-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0ae-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0ae-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="cf0ae-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0ae-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0ae-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-229">Search-Flags</span></span>           | <span data-ttu-id="cf0ae-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0ae-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-231">System-Flags</span></span>           | <span data-ttu-id="cf0ae-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0ae-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0ae-233">Classes used in</span></span>        | [<span data-ttu-id="cf0ae-234">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="cf0ae-235">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf0ae-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf0ae-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf0ae-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-237">Entry</span></span> | <span data-ttu-id="cf0ae-238">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0ae-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0ae-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0ae-241">System-Only</span></span>            | <span data-ttu-id="cf0ae-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0ae-243">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0ae-244">True</span><span class="sxs-lookup"><span data-stu-id="cf0ae-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="cf0ae-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0ae-245">Is Indexed</span></span>             | <span data-ttu-id="cf0ae-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0ae-247">In Global Catalog</span></span>      | <span data-ttu-id="cf0ae-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0ae-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0ae-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0ae-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="cf0ae-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0ae-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0ae-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-253">Search-Flags</span></span>           | <span data-ttu-id="cf0ae-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0ae-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-255">System-Flags</span></span>           | <span data-ttu-id="cf0ae-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0ae-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0ae-257">Classes used in</span></span>        | [<span data-ttu-id="cf0ae-258">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="cf0ae-259">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf0ae-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf0ae-260">Windows Server 2012</span></span>



| <span data-ttu-id="cf0ae-261">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0ae-261">Entry</span></span> | <span data-ttu-id="cf0ae-262">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0ae-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0ae-263">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0ae-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0ae-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0ae-265">System-Only</span></span>            | <span data-ttu-id="cf0ae-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-267">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0ae-267">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0ae-268">True</span><span class="sxs-lookup"><span data-stu-id="cf0ae-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="cf0ae-269">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0ae-269">Is Indexed</span></span>             | <span data-ttu-id="cf0ae-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-271">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0ae-271">In Global Catalog</span></span>      | <span data-ttu-id="cf0ae-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0ae-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="cf0ae-273">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0ae-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0ae-274">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0ae-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="cf0ae-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0ae-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0ae-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="cf0ae-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-277">Search-Flags</span></span>           | <span data-ttu-id="cf0ae-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0ae-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0ae-279">System-Flags</span></span>           | <span data-ttu-id="cf0ae-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0ae-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="cf0ae-281">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0ae-281">Classes used in</span></span>        | [<span data-ttu-id="cf0ae-282">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="cf0ae-283">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="cf0ae-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





