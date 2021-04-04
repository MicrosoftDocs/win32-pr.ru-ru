---
title: Атрибут MS-SQL-Ластбаккупдате
description: Последняя Дата резервного копирования базы данных.
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Ластбаккупдате
- Схема AD атрибута mS-SQL-Ластбаккупдате
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989847"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="ca8c1-105">Атрибут MS-SQL-Ластбаккупдате</span><span class="sxs-lookup"><span data-stu-id="ca8c1-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="ca8c1-106">Последняя Дата резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="ca8c1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-107">Entry</span></span> | <span data-ttu-id="ca8c1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ca8c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="ca8c1-109">CN</span></span>                | <span data-ttu-id="ca8c1-110">MS-SQL-Ластбаккупдате</span><span class="sxs-lookup"><span data-stu-id="ca8c1-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="ca8c1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ca8c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ca8c1-112">mS-SQL-Ластбаккупдате</span><span class="sxs-lookup"><span data-stu-id="ca8c1-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="ca8c1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ca8c1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="ca8c1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ca8c1-114">Update Privilege</span></span>  | <span data-ttu-id="ca8c1-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="ca8c1-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ca8c1-116">Update Frequency</span></span>  | <span data-ttu-id="ca8c1-117">При резервном копировании базы данных.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="ca8c1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-118">Attribute-Id</span></span>      | <span data-ttu-id="ca8c1-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="ca8c1-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="ca8c1-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ca8c1-120">System-Id-Guid</span></span>    | <span data-ttu-id="ca8c1-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ca8c1-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="ca8c1-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca8c1-122">Syntax</span></span>            | [<span data-ttu-id="ca8c1-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ca8c1-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ca8c1-124">Implementations</span></span>

-   [<span data-ttu-id="ca8c1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ca8c1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ca8c1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ca8c1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ca8c1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ca8c1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ca8c1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca8c1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ca8c1-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-132">Entry</span></span> | <span data-ttu-id="ca8c1-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c1-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8c1-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8c1-136">System-Only</span></span>            | <span data-ttu-id="ca8c1-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8c1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8c1-139">True</span><span class="sxs-lookup"><span data-stu-id="ca8c1-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="ca8c1-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8c1-140">Is Indexed</span></span>             | <span data-ttu-id="ca8c1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8c1-142">In Global Catalog</span></span>      | <span data-ttu-id="ca8c1-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8c1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8c1-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8c1-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ca8c1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8c1-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8c1-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-148">Search-Flags</span></span>           | <span data-ttu-id="ca8c1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca8c1-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-150">System-Flags</span></span>           | <span data-ttu-id="ca8c1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8c1-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8c1-152">Classes used in</span></span>        | [<span data-ttu-id="ca8c1-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="ca8c1-154">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ca8c1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca8c1-155">Windows Server 2003</span></span>



| <span data-ttu-id="ca8c1-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-156">Entry</span></span> | <span data-ttu-id="ca8c1-157">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c1-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8c1-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8c1-160">System-Only</span></span>            | <span data-ttu-id="ca8c1-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8c1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8c1-163">True</span><span class="sxs-lookup"><span data-stu-id="ca8c1-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="ca8c1-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8c1-164">Is Indexed</span></span>             | <span data-ttu-id="ca8c1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8c1-166">In Global Catalog</span></span>      | <span data-ttu-id="ca8c1-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8c1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8c1-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8c1-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ca8c1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8c1-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8c1-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-172">Search-Flags</span></span>           | <span data-ttu-id="ca8c1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca8c1-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-174">System-Flags</span></span>           | <span data-ttu-id="ca8c1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8c1-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8c1-176">Classes used in</span></span>        | [<span data-ttu-id="ca8c1-177">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="ca8c1-178">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ca8c1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ca8c1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ca8c1-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-180">Entry</span></span> | <span data-ttu-id="ca8c1-181">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c1-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8c1-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8c1-184">System-Only</span></span>            | <span data-ttu-id="ca8c1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8c1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8c1-187">True</span><span class="sxs-lookup"><span data-stu-id="ca8c1-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="ca8c1-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8c1-188">Is Indexed</span></span>             | <span data-ttu-id="ca8c1-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8c1-190">In Global Catalog</span></span>      | <span data-ttu-id="ca8c1-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8c1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8c1-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8c1-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ca8c1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8c1-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8c1-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-196">Search-Flags</span></span>           | <span data-ttu-id="ca8c1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca8c1-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-198">System-Flags</span></span>           | <span data-ttu-id="ca8c1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8c1-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8c1-200">Classes used in</span></span>        | [<span data-ttu-id="ca8c1-201">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="ca8c1-202">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ca8c1-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca8c1-203">Windows Server 2008</span></span>



| <span data-ttu-id="ca8c1-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-204">Entry</span></span> | <span data-ttu-id="ca8c1-205">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c1-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8c1-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8c1-208">System-Only</span></span>            | <span data-ttu-id="ca8c1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8c1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8c1-211">True</span><span class="sxs-lookup"><span data-stu-id="ca8c1-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="ca8c1-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8c1-212">Is Indexed</span></span>             | <span data-ttu-id="ca8c1-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8c1-214">In Global Catalog</span></span>      | <span data-ttu-id="ca8c1-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8c1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8c1-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8c1-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ca8c1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8c1-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8c1-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-220">Search-Flags</span></span>           | <span data-ttu-id="ca8c1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca8c1-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-222">System-Flags</span></span>           | <span data-ttu-id="ca8c1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8c1-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8c1-224">Classes used in</span></span>        | [<span data-ttu-id="ca8c1-225">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="ca8c1-226">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ca8c1-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca8c1-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ca8c1-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-228">Entry</span></span> | <span data-ttu-id="ca8c1-229">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c1-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8c1-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8c1-232">System-Only</span></span>            | <span data-ttu-id="ca8c1-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8c1-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8c1-235">True</span><span class="sxs-lookup"><span data-stu-id="ca8c1-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="ca8c1-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8c1-236">Is Indexed</span></span>             | <span data-ttu-id="ca8c1-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8c1-238">In Global Catalog</span></span>      | <span data-ttu-id="ca8c1-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8c1-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8c1-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8c1-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ca8c1-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8c1-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8c1-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-244">Search-Flags</span></span>           | <span data-ttu-id="ca8c1-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca8c1-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-246">System-Flags</span></span>           | <span data-ttu-id="ca8c1-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8c1-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8c1-248">Classes used in</span></span>        | [<span data-ttu-id="ca8c1-249">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="ca8c1-250">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ca8c1-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca8c1-251">Windows Server 2012</span></span>



| <span data-ttu-id="ca8c1-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8c1-252">Entry</span></span> | <span data-ttu-id="ca8c1-253">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8c1-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c1-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8c1-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8c1-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8c1-256">System-Only</span></span>            | <span data-ttu-id="ca8c1-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8c1-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8c1-259">True</span><span class="sxs-lookup"><span data-stu-id="ca8c1-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="ca8c1-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8c1-260">Is Indexed</span></span>             | <span data-ttu-id="ca8c1-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8c1-262">In Global Catalog</span></span>      | <span data-ttu-id="ca8c1-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8c1-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="ca8c1-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8c1-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8c1-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8c1-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ca8c1-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8c1-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8c1-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ca8c1-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-268">Search-Flags</span></span>           | <span data-ttu-id="ca8c1-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca8c1-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8c1-270">System-Flags</span></span>           | <span data-ttu-id="ca8c1-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8c1-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ca8c1-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8c1-272">Classes used in</span></span>        | [<span data-ttu-id="ca8c1-273">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="ca8c1-274">**MS-SQL-Олапдатабасе**</span><span class="sxs-lookup"><span data-stu-id="ca8c1-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





