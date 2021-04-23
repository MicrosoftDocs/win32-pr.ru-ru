---
title: Атрибут MS-SQL-Ластдиагностикдате
description: Последняя дата выполнения инструкции DBCC CHECKDB.
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Ластдиагностикдате
- Схема AD атрибута mS-SQL-Ластдиагностикдате
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804390"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="56035-105">Атрибут MS-SQL-Ластдиагностикдате</span><span class="sxs-lookup"><span data-stu-id="56035-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="56035-106">Последняя дата выполнения инструкции DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="56035-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="56035-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-107">Entry</span></span> | <span data-ttu-id="56035-108">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="56035-109">CN</span><span class="sxs-lookup"><span data-stu-id="56035-109">CN</span></span>                | <span data-ttu-id="56035-110">MS-SQL-Ластдиагностикдате</span><span class="sxs-lookup"><span data-stu-id="56035-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="56035-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="56035-111">Ldap-Display-Name</span></span> | <span data-ttu-id="56035-112">mS-SQL-Ластдиагностикдате</span><span class="sxs-lookup"><span data-stu-id="56035-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="56035-113">Размер</span><span class="sxs-lookup"><span data-stu-id="56035-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="56035-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="56035-114">Update Privilege</span></span>  | <span data-ttu-id="56035-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="56035-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="56035-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="56035-116">Update Frequency</span></span>  | <span data-ttu-id="56035-117">При выполнении инструкции DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="56035-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="56035-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56035-118">Attribute-Id</span></span>      | <span data-ttu-id="56035-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="56035-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="56035-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="56035-120">System-Id-Guid</span></span>    | <span data-ttu-id="56035-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="56035-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="56035-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56035-122">Syntax</span></span>            | [<span data-ttu-id="56035-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="56035-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="56035-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="56035-124">Implementations</span></span>

-   [<span data-ttu-id="56035-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="56035-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="56035-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56035-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56035-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56035-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56035-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56035-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56035-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56035-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56035-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56035-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="56035-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56035-131">Windows 2000 Server</span></span>



| <span data-ttu-id="56035-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-132">Entry</span></span> | <span data-ttu-id="56035-133">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="56035-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56035-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56035-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="56035-136">System-Only</span></span>            | <span data-ttu-id="56035-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-137">False</span></span>                                                         |
| <span data-ttu-id="56035-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56035-138">Is-Single-Valued</span></span>       | <span data-ttu-id="56035-139">True</span><span class="sxs-lookup"><span data-stu-id="56035-139">True</span></span>                                                          |
| <span data-ttu-id="56035-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56035-140">Is Indexed</span></span>             | <span data-ttu-id="56035-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-141">False</span></span>                                                         |
| <span data-ttu-id="56035-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56035-142">In Global Catalog</span></span>      | <span data-ttu-id="56035-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-143">False</span></span>                                                         |
| <span data-ttu-id="56035-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56035-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="56035-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56035-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="56035-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56035-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="56035-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56035-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="56035-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-148">Search-Flags</span></span>           | <span data-ttu-id="56035-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56035-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="56035-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-150">System-Flags</span></span>           | <span data-ttu-id="56035-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56035-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="56035-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56035-152">Classes used in</span></span>        | [<span data-ttu-id="56035-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="56035-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="56035-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56035-154">Windows Server 2003</span></span>



| <span data-ttu-id="56035-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-155">Entry</span></span> | <span data-ttu-id="56035-156">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="56035-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56035-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56035-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="56035-159">System-Only</span></span>            | <span data-ttu-id="56035-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-160">False</span></span>                                                         |
| <span data-ttu-id="56035-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56035-161">Is-Single-Valued</span></span>       | <span data-ttu-id="56035-162">True</span><span class="sxs-lookup"><span data-stu-id="56035-162">True</span></span>                                                          |
| <span data-ttu-id="56035-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56035-163">Is Indexed</span></span>             | <span data-ttu-id="56035-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-164">False</span></span>                                                         |
| <span data-ttu-id="56035-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56035-165">In Global Catalog</span></span>      | <span data-ttu-id="56035-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-166">False</span></span>                                                         |
| <span data-ttu-id="56035-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56035-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="56035-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56035-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="56035-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56035-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="56035-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56035-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="56035-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-171">Search-Flags</span></span>           | <span data-ttu-id="56035-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56035-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="56035-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-173">System-Flags</span></span>           | <span data-ttu-id="56035-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56035-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="56035-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56035-175">Classes used in</span></span>        | [<span data-ttu-id="56035-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="56035-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56035-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56035-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56035-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-178">Entry</span></span> | <span data-ttu-id="56035-179">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="56035-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56035-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56035-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="56035-182">System-Only</span></span>            | <span data-ttu-id="56035-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-183">False</span></span>                                                         |
| <span data-ttu-id="56035-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56035-184">Is-Single-Valued</span></span>       | <span data-ttu-id="56035-185">True</span><span class="sxs-lookup"><span data-stu-id="56035-185">True</span></span>                                                          |
| <span data-ttu-id="56035-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56035-186">Is Indexed</span></span>             | <span data-ttu-id="56035-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-187">False</span></span>                                                         |
| <span data-ttu-id="56035-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56035-188">In Global Catalog</span></span>      | <span data-ttu-id="56035-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-189">False</span></span>                                                         |
| <span data-ttu-id="56035-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56035-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="56035-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56035-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="56035-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56035-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="56035-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56035-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="56035-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-194">Search-Flags</span></span>           | <span data-ttu-id="56035-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56035-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="56035-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-196">System-Flags</span></span>           | <span data-ttu-id="56035-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56035-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="56035-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56035-198">Classes used in</span></span>        | [<span data-ttu-id="56035-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="56035-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56035-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56035-200">Windows Server 2008</span></span>



| <span data-ttu-id="56035-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-201">Entry</span></span> | <span data-ttu-id="56035-202">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="56035-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56035-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56035-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="56035-205">System-Only</span></span>            | <span data-ttu-id="56035-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-206">False</span></span>                                                         |
| <span data-ttu-id="56035-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56035-207">Is-Single-Valued</span></span>       | <span data-ttu-id="56035-208">True</span><span class="sxs-lookup"><span data-stu-id="56035-208">True</span></span>                                                          |
| <span data-ttu-id="56035-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56035-209">Is Indexed</span></span>             | <span data-ttu-id="56035-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-210">False</span></span>                                                         |
| <span data-ttu-id="56035-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56035-211">In Global Catalog</span></span>      | <span data-ttu-id="56035-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-212">False</span></span>                                                         |
| <span data-ttu-id="56035-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56035-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="56035-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56035-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="56035-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56035-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="56035-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56035-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="56035-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-217">Search-Flags</span></span>           | <span data-ttu-id="56035-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56035-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="56035-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-219">System-Flags</span></span>           | <span data-ttu-id="56035-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56035-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="56035-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56035-221">Classes used in</span></span>        | [<span data-ttu-id="56035-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="56035-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56035-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56035-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56035-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-224">Entry</span></span> | <span data-ttu-id="56035-225">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="56035-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56035-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56035-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="56035-228">System-Only</span></span>            | <span data-ttu-id="56035-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-229">False</span></span>                                                         |
| <span data-ttu-id="56035-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56035-230">Is-Single-Valued</span></span>       | <span data-ttu-id="56035-231">True</span><span class="sxs-lookup"><span data-stu-id="56035-231">True</span></span>                                                          |
| <span data-ttu-id="56035-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56035-232">Is Indexed</span></span>             | <span data-ttu-id="56035-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-233">False</span></span>                                                         |
| <span data-ttu-id="56035-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56035-234">In Global Catalog</span></span>      | <span data-ttu-id="56035-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-235">False</span></span>                                                         |
| <span data-ttu-id="56035-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56035-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="56035-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56035-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="56035-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56035-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="56035-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56035-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="56035-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-240">Search-Flags</span></span>           | <span data-ttu-id="56035-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56035-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="56035-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-242">System-Flags</span></span>           | <span data-ttu-id="56035-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56035-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="56035-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56035-244">Classes used in</span></span>        | [<span data-ttu-id="56035-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="56035-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56035-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56035-246">Windows Server 2012</span></span>



| <span data-ttu-id="56035-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="56035-247">Entry</span></span> | <span data-ttu-id="56035-248">Значение</span><span class="sxs-lookup"><span data-stu-id="56035-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="56035-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56035-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56035-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="56035-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="56035-251">System-Only</span></span>            | <span data-ttu-id="56035-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-252">False</span></span>                                                         |
| <span data-ttu-id="56035-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56035-253">Is-Single-Valued</span></span>       | <span data-ttu-id="56035-254">True</span><span class="sxs-lookup"><span data-stu-id="56035-254">True</span></span>                                                          |
| <span data-ttu-id="56035-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56035-255">Is Indexed</span></span>             | <span data-ttu-id="56035-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-256">False</span></span>                                                         |
| <span data-ttu-id="56035-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56035-257">In Global Catalog</span></span>      | <span data-ttu-id="56035-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="56035-258">False</span></span>                                                         |
| <span data-ttu-id="56035-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56035-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="56035-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56035-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="56035-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56035-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="56035-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56035-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="56035-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-263">Search-Flags</span></span>           | <span data-ttu-id="56035-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56035-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="56035-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56035-265">System-Flags</span></span>           | <span data-ttu-id="56035-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56035-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="56035-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56035-267">Classes used in</span></span>        | [<span data-ttu-id="56035-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="56035-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





