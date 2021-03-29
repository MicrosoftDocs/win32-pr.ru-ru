---
title: Атрибут кодировки MS-SQL
description: Кодировка для текущего экземпляра SQL Server.
ms.assetid: 5c45058f-e883-455c-8e18-415ddae149f8
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута кодировки MS-SQL
- Схема AD для атрибута кодировки mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-CharacterSet
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2f3718c9e47393498e42c4091283ea768d5072
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893910"
---
# <a name="ms-sql-characterset-attribute"></a><span data-ttu-id="df6fd-105">Атрибут кодировки MS-SQL</span><span class="sxs-lookup"><span data-stu-id="df6fd-105">MS-SQL-CharacterSet attribute</span></span>

<span data-ttu-id="df6fd-106">Кодировка для текущего экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="df6fd-106">The character set for the current instance of SQL Server.</span></span>



| <span data-ttu-id="df6fd-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-107">Entry</span></span> | <span data-ttu-id="df6fd-108">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="df6fd-109">CN</span><span class="sxs-lookup"><span data-stu-id="df6fd-109">CN</span></span>                | <span data-ttu-id="df6fd-110">Кодировка MS-SQL</span><span class="sxs-lookup"><span data-stu-id="df6fd-110">MS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="df6fd-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="df6fd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="df6fd-112">Кодировка mS-SQL</span><span class="sxs-lookup"><span data-stu-id="df6fd-112">mS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="df6fd-113">Размер</span><span class="sxs-lookup"><span data-stu-id="df6fd-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="df6fd-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="df6fd-114">Update Privilege</span></span>  | <span data-ttu-id="df6fd-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="df6fd-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="df6fd-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="df6fd-116">Update Frequency</span></span>  | <span data-ttu-id="df6fd-117">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="df6fd-117">At system startup.</span></span>                   |
| <span data-ttu-id="df6fd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-118">Attribute-Id</span></span>      | <span data-ttu-id="df6fd-119">1.2.840.113556.1.4.1370</span><span class="sxs-lookup"><span data-stu-id="df6fd-119">1.2.840.113556.1.4.1370</span></span>              |
| <span data-ttu-id="df6fd-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="df6fd-120">System-Id-Guid</span></span>    | <span data-ttu-id="df6fd-121">696177a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="df6fd-121">696177a6-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="df6fd-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df6fd-122">Syntax</span></span>            | [<span data-ttu-id="df6fd-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="df6fd-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="df6fd-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="df6fd-124">Implementations</span></span>

-   [<span data-ttu-id="df6fd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df6fd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df6fd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df6fd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df6fd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df6fd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df6fd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df6fd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df6fd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df6fd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df6fd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df6fd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df6fd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df6fd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="df6fd-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-132">Entry</span></span> | <span data-ttu-id="df6fd-133">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df6fd-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="df6fd-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="df6fd-136">System-Only</span></span>            | <span data-ttu-id="df6fd-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-137">False</span></span>                                                     |
| <span data-ttu-id="df6fd-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="df6fd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="df6fd-139">True</span><span class="sxs-lookup"><span data-stu-id="df6fd-139">True</span></span>                                                      |
| <span data-ttu-id="df6fd-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="df6fd-140">Is Indexed</span></span>             | <span data-ttu-id="df6fd-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-141">False</span></span>                                                     |
| <span data-ttu-id="df6fd-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="df6fd-142">In Global Catalog</span></span>      | <span data-ttu-id="df6fd-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-143">False</span></span>                                                     |
| <span data-ttu-id="df6fd-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="df6fd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="df6fd-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df6fd-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="df6fd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df6fd-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df6fd-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-148">Search-Flags</span></span>           | <span data-ttu-id="df6fd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df6fd-149">0x00000000</span></span>                                                |
| <span data-ttu-id="df6fd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-150">System-Flags</span></span>           | <span data-ttu-id="df6fd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df6fd-151">0x00000010</span></span>                                                |
| <span data-ttu-id="df6fd-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="df6fd-152">Classes used in</span></span>        | [<span data-ttu-id="df6fd-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="df6fd-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df6fd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df6fd-154">Windows Server 2003</span></span>



| <span data-ttu-id="df6fd-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-155">Entry</span></span> | <span data-ttu-id="df6fd-156">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df6fd-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="df6fd-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="df6fd-159">System-Only</span></span>            | <span data-ttu-id="df6fd-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-160">False</span></span>                                                     |
| <span data-ttu-id="df6fd-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="df6fd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="df6fd-162">True</span><span class="sxs-lookup"><span data-stu-id="df6fd-162">True</span></span>                                                      |
| <span data-ttu-id="df6fd-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="df6fd-163">Is Indexed</span></span>             | <span data-ttu-id="df6fd-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-164">False</span></span>                                                     |
| <span data-ttu-id="df6fd-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="df6fd-165">In Global Catalog</span></span>      | <span data-ttu-id="df6fd-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-166">False</span></span>                                                     |
| <span data-ttu-id="df6fd-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="df6fd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="df6fd-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df6fd-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="df6fd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df6fd-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df6fd-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-171">Search-Flags</span></span>           | <span data-ttu-id="df6fd-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df6fd-172">0x00000000</span></span>                                                |
| <span data-ttu-id="df6fd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-173">System-Flags</span></span>           | <span data-ttu-id="df6fd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df6fd-174">0x00000010</span></span>                                                |
| <span data-ttu-id="df6fd-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="df6fd-175">Classes used in</span></span>        | [<span data-ttu-id="df6fd-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="df6fd-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df6fd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df6fd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df6fd-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-178">Entry</span></span> | <span data-ttu-id="df6fd-179">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df6fd-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="df6fd-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="df6fd-182">System-Only</span></span>            | <span data-ttu-id="df6fd-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-183">False</span></span>                                                     |
| <span data-ttu-id="df6fd-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="df6fd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="df6fd-185">True</span><span class="sxs-lookup"><span data-stu-id="df6fd-185">True</span></span>                                                      |
| <span data-ttu-id="df6fd-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="df6fd-186">Is Indexed</span></span>             | <span data-ttu-id="df6fd-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-187">False</span></span>                                                     |
| <span data-ttu-id="df6fd-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="df6fd-188">In Global Catalog</span></span>      | <span data-ttu-id="df6fd-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-189">False</span></span>                                                     |
| <span data-ttu-id="df6fd-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="df6fd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="df6fd-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df6fd-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="df6fd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df6fd-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df6fd-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-194">Search-Flags</span></span>           | <span data-ttu-id="df6fd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df6fd-195">0x00000000</span></span>                                                |
| <span data-ttu-id="df6fd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-196">System-Flags</span></span>           | <span data-ttu-id="df6fd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df6fd-197">0x00000010</span></span>                                                |
| <span data-ttu-id="df6fd-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="df6fd-198">Classes used in</span></span>        | [<span data-ttu-id="df6fd-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="df6fd-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df6fd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df6fd-200">Windows Server 2008</span></span>



| <span data-ttu-id="df6fd-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-201">Entry</span></span> | <span data-ttu-id="df6fd-202">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df6fd-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="df6fd-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="df6fd-205">System-Only</span></span>            | <span data-ttu-id="df6fd-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-206">False</span></span>                                                     |
| <span data-ttu-id="df6fd-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="df6fd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="df6fd-208">True</span><span class="sxs-lookup"><span data-stu-id="df6fd-208">True</span></span>                                                      |
| <span data-ttu-id="df6fd-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="df6fd-209">Is Indexed</span></span>             | <span data-ttu-id="df6fd-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-210">False</span></span>                                                     |
| <span data-ttu-id="df6fd-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="df6fd-211">In Global Catalog</span></span>      | <span data-ttu-id="df6fd-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-212">False</span></span>                                                     |
| <span data-ttu-id="df6fd-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="df6fd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="df6fd-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df6fd-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="df6fd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df6fd-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df6fd-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-217">Search-Flags</span></span>           | <span data-ttu-id="df6fd-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df6fd-218">0x00000000</span></span>                                                |
| <span data-ttu-id="df6fd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-219">System-Flags</span></span>           | <span data-ttu-id="df6fd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df6fd-220">0x00000010</span></span>                                                |
| <span data-ttu-id="df6fd-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="df6fd-221">Classes used in</span></span>        | [<span data-ttu-id="df6fd-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="df6fd-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df6fd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df6fd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df6fd-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-224">Entry</span></span> | <span data-ttu-id="df6fd-225">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df6fd-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="df6fd-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="df6fd-228">System-Only</span></span>            | <span data-ttu-id="df6fd-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-229">False</span></span>                                                     |
| <span data-ttu-id="df6fd-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="df6fd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="df6fd-231">True</span><span class="sxs-lookup"><span data-stu-id="df6fd-231">True</span></span>                                                      |
| <span data-ttu-id="df6fd-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="df6fd-232">Is Indexed</span></span>             | <span data-ttu-id="df6fd-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-233">False</span></span>                                                     |
| <span data-ttu-id="df6fd-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="df6fd-234">In Global Catalog</span></span>      | <span data-ttu-id="df6fd-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-235">False</span></span>                                                     |
| <span data-ttu-id="df6fd-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="df6fd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="df6fd-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df6fd-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="df6fd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df6fd-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df6fd-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-240">Search-Flags</span></span>           | <span data-ttu-id="df6fd-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df6fd-241">0x00000000</span></span>                                                |
| <span data-ttu-id="df6fd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-242">System-Flags</span></span>           | <span data-ttu-id="df6fd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df6fd-243">0x00000010</span></span>                                                |
| <span data-ttu-id="df6fd-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="df6fd-244">Classes used in</span></span>        | [<span data-ttu-id="df6fd-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="df6fd-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df6fd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df6fd-246">Windows Server 2012</span></span>



| <span data-ttu-id="df6fd-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="df6fd-247">Entry</span></span> | <span data-ttu-id="df6fd-248">Значение</span><span class="sxs-lookup"><span data-stu-id="df6fd-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df6fd-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="df6fd-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df6fd-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="df6fd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="df6fd-251">System-Only</span></span>            | <span data-ttu-id="df6fd-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-252">False</span></span>                                                     |
| <span data-ttu-id="df6fd-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="df6fd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="df6fd-254">True</span><span class="sxs-lookup"><span data-stu-id="df6fd-254">True</span></span>                                                      |
| <span data-ttu-id="df6fd-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="df6fd-255">Is Indexed</span></span>             | <span data-ttu-id="df6fd-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-256">False</span></span>                                                     |
| <span data-ttu-id="df6fd-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="df6fd-257">In Global Catalog</span></span>      | <span data-ttu-id="df6fd-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="df6fd-258">False</span></span>                                                     |
| <span data-ttu-id="df6fd-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="df6fd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="df6fd-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df6fd-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="df6fd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df6fd-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df6fd-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="df6fd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-263">Search-Flags</span></span>           | <span data-ttu-id="df6fd-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df6fd-264">0x00000000</span></span>                                                |
| <span data-ttu-id="df6fd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df6fd-265">System-Flags</span></span>           | <span data-ttu-id="df6fd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df6fd-266">0x00000010</span></span>                                                |
| <span data-ttu-id="df6fd-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="df6fd-267">Classes used in</span></span>        | [<span data-ttu-id="df6fd-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="df6fd-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





