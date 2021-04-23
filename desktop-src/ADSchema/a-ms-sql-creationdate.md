---
title: Атрибут MS-SQL-CreationDate
description: Дата создания базы данных.
ms.assetid: c3b098f0-2575-4a7d-9a1d-a6189b9af2c8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута в MS-SQL-CreationDate
- Схема AD атрибута в mS-SQL-CreationDate
topic_type:
- apiref
api_name:
- MS-SQL-CreationDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c499a65ef8beee485bab647d8649559b74cfbd1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655497"
---
# <a name="ms-sql-creationdate-attribute"></a><span data-ttu-id="a5926-105">Атрибут MS-SQL-CreationDate</span><span class="sxs-lookup"><span data-stu-id="a5926-105">MS-SQL-CreationDate attribute</span></span>

<span data-ttu-id="a5926-106">Дата создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="a5926-106">The date the database was created.</span></span>



| <span data-ttu-id="a5926-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-107">Entry</span></span> | <span data-ttu-id="a5926-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a5926-109">CN</span><span class="sxs-lookup"><span data-stu-id="a5926-109">CN</span></span>                | <span data-ttu-id="a5926-110">MS-SQL-CreationDate</span><span class="sxs-lookup"><span data-stu-id="a5926-110">MS-SQL-CreationDate</span></span>                         |
| <span data-ttu-id="a5926-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a5926-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a5926-112">mS-SQL-CreationDate</span><span class="sxs-lookup"><span data-stu-id="a5926-112">mS-SQL-CreationDate</span></span>                         |
| <span data-ttu-id="a5926-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a5926-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a5926-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a5926-114">Update Privilege</span></span>  | <span data-ttu-id="a5926-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="a5926-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="a5926-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a5926-116">Update Frequency</span></span>  | <span data-ttu-id="a5926-117">При создании новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a5926-117">When a new database is created.</span></span>             |
| <span data-ttu-id="a5926-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-118">Attribute-Id</span></span>      | <span data-ttu-id="a5926-119">1.2.840.113556.1.4.1397</span><span class="sxs-lookup"><span data-stu-id="a5926-119">1.2.840.113556.1.4.1397</span></span>                     |
| <span data-ttu-id="a5926-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a5926-120">System-Id-Guid</span></span>    | <span data-ttu-id="a5926-121">ede14754-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a5926-121">ede14754-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="a5926-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5926-122">Syntax</span></span>            | [<span data-ttu-id="a5926-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="a5926-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a5926-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a5926-124">Implementations</span></span>

-   [<span data-ttu-id="a5926-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a5926-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a5926-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5926-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5926-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5926-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5926-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5926-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5926-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5926-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5926-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5926-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a5926-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5926-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a5926-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-132">Entry</span></span> | <span data-ttu-id="a5926-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5926-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5926-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5926-136">System-Only</span></span>            | <span data-ttu-id="a5926-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-137">False</span></span>                                                         |
| <span data-ttu-id="a5926-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5926-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a5926-139">True</span><span class="sxs-lookup"><span data-stu-id="a5926-139">True</span></span>                                                          |
| <span data-ttu-id="a5926-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5926-140">Is Indexed</span></span>             | <span data-ttu-id="a5926-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-141">False</span></span>                                                         |
| <span data-ttu-id="a5926-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5926-142">In Global Catalog</span></span>      | <span data-ttu-id="a5926-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-143">False</span></span>                                                         |
| <span data-ttu-id="a5926-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5926-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5926-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5926-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="a5926-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5926-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5926-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-148">Search-Flags</span></span>           | <span data-ttu-id="a5926-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5926-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="a5926-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-150">System-Flags</span></span>           | <span data-ttu-id="a5926-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5926-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="a5926-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5926-152">Classes used in</span></span>        | [<span data-ttu-id="a5926-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="a5926-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a5926-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5926-154">Windows Server 2003</span></span>



| <span data-ttu-id="a5926-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-155">Entry</span></span> | <span data-ttu-id="a5926-156">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5926-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5926-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5926-159">System-Only</span></span>            | <span data-ttu-id="a5926-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-160">False</span></span>                                                         |
| <span data-ttu-id="a5926-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5926-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a5926-162">True</span><span class="sxs-lookup"><span data-stu-id="a5926-162">True</span></span>                                                          |
| <span data-ttu-id="a5926-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5926-163">Is Indexed</span></span>             | <span data-ttu-id="a5926-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-164">False</span></span>                                                         |
| <span data-ttu-id="a5926-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5926-165">In Global Catalog</span></span>      | <span data-ttu-id="a5926-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-166">False</span></span>                                                         |
| <span data-ttu-id="a5926-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5926-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5926-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5926-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="a5926-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5926-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5926-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-171">Search-Flags</span></span>           | <span data-ttu-id="a5926-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5926-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="a5926-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-173">System-Flags</span></span>           | <span data-ttu-id="a5926-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5926-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="a5926-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5926-175">Classes used in</span></span>        | [<span data-ttu-id="a5926-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="a5926-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5926-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5926-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5926-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-178">Entry</span></span> | <span data-ttu-id="a5926-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5926-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5926-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5926-182">System-Only</span></span>            | <span data-ttu-id="a5926-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-183">False</span></span>                                                         |
| <span data-ttu-id="a5926-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5926-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a5926-185">True</span><span class="sxs-lookup"><span data-stu-id="a5926-185">True</span></span>                                                          |
| <span data-ttu-id="a5926-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5926-186">Is Indexed</span></span>             | <span data-ttu-id="a5926-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-187">False</span></span>                                                         |
| <span data-ttu-id="a5926-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5926-188">In Global Catalog</span></span>      | <span data-ttu-id="a5926-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-189">False</span></span>                                                         |
| <span data-ttu-id="a5926-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5926-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5926-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5926-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="a5926-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5926-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5926-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-194">Search-Flags</span></span>           | <span data-ttu-id="a5926-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5926-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="a5926-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-196">System-Flags</span></span>           | <span data-ttu-id="a5926-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5926-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="a5926-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5926-198">Classes used in</span></span>        | [<span data-ttu-id="a5926-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="a5926-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5926-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5926-200">Windows Server 2008</span></span>



| <span data-ttu-id="a5926-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-201">Entry</span></span> | <span data-ttu-id="a5926-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5926-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5926-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5926-205">System-Only</span></span>            | <span data-ttu-id="a5926-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-206">False</span></span>                                                         |
| <span data-ttu-id="a5926-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5926-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a5926-208">True</span><span class="sxs-lookup"><span data-stu-id="a5926-208">True</span></span>                                                          |
| <span data-ttu-id="a5926-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5926-209">Is Indexed</span></span>             | <span data-ttu-id="a5926-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-210">False</span></span>                                                         |
| <span data-ttu-id="a5926-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5926-211">In Global Catalog</span></span>      | <span data-ttu-id="a5926-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-212">False</span></span>                                                         |
| <span data-ttu-id="a5926-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5926-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5926-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5926-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="a5926-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5926-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5926-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-217">Search-Flags</span></span>           | <span data-ttu-id="a5926-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5926-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="a5926-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-219">System-Flags</span></span>           | <span data-ttu-id="a5926-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5926-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="a5926-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5926-221">Classes used in</span></span>        | [<span data-ttu-id="a5926-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="a5926-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5926-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5926-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5926-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-224">Entry</span></span> | <span data-ttu-id="a5926-225">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5926-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5926-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5926-228">System-Only</span></span>            | <span data-ttu-id="a5926-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-229">False</span></span>                                                         |
| <span data-ttu-id="a5926-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5926-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a5926-231">True</span><span class="sxs-lookup"><span data-stu-id="a5926-231">True</span></span>                                                          |
| <span data-ttu-id="a5926-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5926-232">Is Indexed</span></span>             | <span data-ttu-id="a5926-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-233">False</span></span>                                                         |
| <span data-ttu-id="a5926-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5926-234">In Global Catalog</span></span>      | <span data-ttu-id="a5926-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-235">False</span></span>                                                         |
| <span data-ttu-id="a5926-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5926-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5926-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5926-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="a5926-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5926-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5926-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-240">Search-Flags</span></span>           | <span data-ttu-id="a5926-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5926-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="a5926-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-242">System-Flags</span></span>           | <span data-ttu-id="a5926-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5926-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="a5926-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5926-244">Classes used in</span></span>        | [<span data-ttu-id="a5926-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="a5926-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5926-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5926-246">Windows Server 2012</span></span>



| <span data-ttu-id="a5926-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5926-247">Entry</span></span> | <span data-ttu-id="a5926-248">Значение</span><span class="sxs-lookup"><span data-stu-id="a5926-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5926-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5926-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5926-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="a5926-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5926-251">System-Only</span></span>            | <span data-ttu-id="a5926-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-252">False</span></span>                                                         |
| <span data-ttu-id="a5926-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5926-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a5926-254">True</span><span class="sxs-lookup"><span data-stu-id="a5926-254">True</span></span>                                                          |
| <span data-ttu-id="a5926-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5926-255">Is Indexed</span></span>             | <span data-ttu-id="a5926-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-256">False</span></span>                                                         |
| <span data-ttu-id="a5926-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5926-257">In Global Catalog</span></span>      | <span data-ttu-id="a5926-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5926-258">False</span></span>                                                         |
| <span data-ttu-id="a5926-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5926-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5926-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5926-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="a5926-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5926-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5926-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="a5926-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-263">Search-Flags</span></span>           | <span data-ttu-id="a5926-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5926-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="a5926-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5926-265">System-Flags</span></span>           | <span data-ttu-id="a5926-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5926-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="a5926-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5926-267">Classes used in</span></span>        | [<span data-ttu-id="a5926-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="a5926-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





