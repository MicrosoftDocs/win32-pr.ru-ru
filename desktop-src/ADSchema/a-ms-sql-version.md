---
title: Атрибут MS-SQL-Version
description: Версия текущего экземпляра SQL Server.
ms.assetid: 0003892c-906d-429b-bc98-bbc441b2d58b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута версии MS-SQL-Version
- Схема AD атрибута версии mS-SQL-Version
topic_type:
- apiref
api_name:
- MS-SQL-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a436a30311f5696d8ed63334b0cf796eb2767
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893894"
---
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="998e0-105">Атрибут MS-SQL-Version</span><span class="sxs-lookup"><span data-stu-id="998e0-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="998e0-106">Версия текущего экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="998e0-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="998e0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-107">Entry</span></span> | <span data-ttu-id="998e0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="998e0-109">CN</span><span class="sxs-lookup"><span data-stu-id="998e0-109">CN</span></span>                | <span data-ttu-id="998e0-110">MS-SQL-версия</span><span class="sxs-lookup"><span data-stu-id="998e0-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="998e0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="998e0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="998e0-112">mS-SQL-версия</span><span class="sxs-lookup"><span data-stu-id="998e0-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="998e0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="998e0-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="998e0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="998e0-114">Update Privilege</span></span>  | <span data-ttu-id="998e0-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="998e0-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="998e0-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="998e0-116">Update Frequency</span></span>  | <span data-ttu-id="998e0-117">При установке системы.</span><span class="sxs-lookup"><span data-stu-id="998e0-117">At system setup.</span></span>                            |
| <span data-ttu-id="998e0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-118">Attribute-Id</span></span>      | <span data-ttu-id="998e0-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="998e0-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="998e0-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="998e0-120">System-Id-Guid</span></span>    | <span data-ttu-id="998e0-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="998e0-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="998e0-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="998e0-122">Syntax</span></span>            | [<span data-ttu-id="998e0-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="998e0-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="998e0-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="998e0-124">Implementations</span></span>

-   [<span data-ttu-id="998e0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="998e0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="998e0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="998e0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="998e0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="998e0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="998e0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="998e0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="998e0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="998e0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="998e0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="998e0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="998e0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="998e0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="998e0-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-132">Entry</span></span> | <span data-ttu-id="998e0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e0-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="998e0-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="998e0-136">System-Only</span></span>            | <span data-ttu-id="998e0-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="998e0-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="998e0-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="998e0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="998e0-139">True</span><span class="sxs-lookup"><span data-stu-id="998e0-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="998e0-140">Is Indexed</span></span>             | <span data-ttu-id="998e0-141">True</span><span class="sxs-lookup"><span data-stu-id="998e0-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="998e0-142">In Global Catalog</span></span>      | <span data-ttu-id="998e0-143">True</span><span class="sxs-lookup"><span data-stu-id="998e0-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="998e0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="998e0-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="998e0-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="998e0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="998e0-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="998e0-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-148">Search-Flags</span></span>           | <span data-ttu-id="998e0-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="998e0-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-150">System-Flags</span></span>           | <span data-ttu-id="998e0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="998e0-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="998e0-152">Classes used in</span></span>        | [<span data-ttu-id="998e0-153">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="998e0-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="998e0-154">**MS-SQL-Склрепоситори**</span><span class="sxs-lookup"><span data-stu-id="998e0-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="998e0-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="998e0-155">Windows Server 2003</span></span>



| <span data-ttu-id="998e0-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-156">Entry</span></span> | <span data-ttu-id="998e0-157">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e0-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="998e0-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="998e0-160">System-Only</span></span>            | <span data-ttu-id="998e0-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="998e0-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="998e0-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="998e0-162">Is-Single-Valued</span></span>       | <span data-ttu-id="998e0-163">True</span><span class="sxs-lookup"><span data-stu-id="998e0-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="998e0-164">Is Indexed</span></span>             | <span data-ttu-id="998e0-165">True</span><span class="sxs-lookup"><span data-stu-id="998e0-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="998e0-166">In Global Catalog</span></span>      | <span data-ttu-id="998e0-167">True</span><span class="sxs-lookup"><span data-stu-id="998e0-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="998e0-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="998e0-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="998e0-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="998e0-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="998e0-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="998e0-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-172">Search-Flags</span></span>           | <span data-ttu-id="998e0-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="998e0-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-174">System-Flags</span></span>           | <span data-ttu-id="998e0-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="998e0-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="998e0-176">Classes used in</span></span>        | [<span data-ttu-id="998e0-177">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="998e0-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="998e0-178">**MS-SQL-Склрепоситори**</span><span class="sxs-lookup"><span data-stu-id="998e0-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="998e0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="998e0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="998e0-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-180">Entry</span></span> | <span data-ttu-id="998e0-181">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e0-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="998e0-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="998e0-184">System-Only</span></span>            | <span data-ttu-id="998e0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="998e0-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="998e0-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="998e0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="998e0-187">True</span><span class="sxs-lookup"><span data-stu-id="998e0-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="998e0-188">Is Indexed</span></span>             | <span data-ttu-id="998e0-189">True</span><span class="sxs-lookup"><span data-stu-id="998e0-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="998e0-190">In Global Catalog</span></span>      | <span data-ttu-id="998e0-191">True</span><span class="sxs-lookup"><span data-stu-id="998e0-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="998e0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="998e0-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="998e0-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="998e0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="998e0-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="998e0-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-196">Search-Flags</span></span>           | <span data-ttu-id="998e0-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="998e0-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-198">System-Flags</span></span>           | <span data-ttu-id="998e0-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="998e0-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="998e0-200">Classes used in</span></span>        | [<span data-ttu-id="998e0-201">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="998e0-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="998e0-202">**MS-SQL-Склрепоситори**</span><span class="sxs-lookup"><span data-stu-id="998e0-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="998e0-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="998e0-203">Windows Server 2008</span></span>



| <span data-ttu-id="998e0-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-204">Entry</span></span> | <span data-ttu-id="998e0-205">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e0-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="998e0-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="998e0-208">System-Only</span></span>            | <span data-ttu-id="998e0-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="998e0-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="998e0-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="998e0-210">Is-Single-Valued</span></span>       | <span data-ttu-id="998e0-211">True</span><span class="sxs-lookup"><span data-stu-id="998e0-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="998e0-212">Is Indexed</span></span>             | <span data-ttu-id="998e0-213">True</span><span class="sxs-lookup"><span data-stu-id="998e0-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="998e0-214">In Global Catalog</span></span>      | <span data-ttu-id="998e0-215">True</span><span class="sxs-lookup"><span data-stu-id="998e0-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="998e0-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="998e0-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="998e0-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="998e0-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="998e0-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="998e0-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-220">Search-Flags</span></span>           | <span data-ttu-id="998e0-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="998e0-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-222">System-Flags</span></span>           | <span data-ttu-id="998e0-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="998e0-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="998e0-224">Classes used in</span></span>        | [<span data-ttu-id="998e0-225">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="998e0-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="998e0-226">**MS-SQL-Склрепоситори**</span><span class="sxs-lookup"><span data-stu-id="998e0-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="998e0-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="998e0-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="998e0-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-228">Entry</span></span> | <span data-ttu-id="998e0-229">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e0-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="998e0-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="998e0-232">System-Only</span></span>            | <span data-ttu-id="998e0-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="998e0-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="998e0-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="998e0-234">Is-Single-Valued</span></span>       | <span data-ttu-id="998e0-235">True</span><span class="sxs-lookup"><span data-stu-id="998e0-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="998e0-236">Is Indexed</span></span>             | <span data-ttu-id="998e0-237">True</span><span class="sxs-lookup"><span data-stu-id="998e0-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="998e0-238">In Global Catalog</span></span>      | <span data-ttu-id="998e0-239">True</span><span class="sxs-lookup"><span data-stu-id="998e0-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="998e0-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="998e0-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="998e0-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="998e0-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="998e0-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="998e0-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-244">Search-Flags</span></span>           | <span data-ttu-id="998e0-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="998e0-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-246">System-Flags</span></span>           | <span data-ttu-id="998e0-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="998e0-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="998e0-248">Classes used in</span></span>        | [<span data-ttu-id="998e0-249">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="998e0-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="998e0-250">**MS-SQL-Склрепоситори**</span><span class="sxs-lookup"><span data-stu-id="998e0-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="998e0-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="998e0-251">Windows Server 2012</span></span>



| <span data-ttu-id="998e0-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="998e0-252">Entry</span></span> | <span data-ttu-id="998e0-253">Значение</span><span class="sxs-lookup"><span data-stu-id="998e0-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e0-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="998e0-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="998e0-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="998e0-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="998e0-256">System-Only</span></span>            | <span data-ttu-id="998e0-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="998e0-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="998e0-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="998e0-258">Is-Single-Valued</span></span>       | <span data-ttu-id="998e0-259">True</span><span class="sxs-lookup"><span data-stu-id="998e0-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="998e0-260">Is Indexed</span></span>             | <span data-ttu-id="998e0-261">True</span><span class="sxs-lookup"><span data-stu-id="998e0-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="998e0-262">In Global Catalog</span></span>      | <span data-ttu-id="998e0-263">True</span><span class="sxs-lookup"><span data-stu-id="998e0-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="998e0-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="998e0-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="998e0-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="998e0-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="998e0-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="998e0-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="998e0-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="998e0-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-268">Search-Flags</span></span>           | <span data-ttu-id="998e0-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="998e0-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="998e0-270">System-Flags</span></span>           | <span data-ttu-id="998e0-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="998e0-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="998e0-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="998e0-272">Classes used in</span></span>        | [<span data-ttu-id="998e0-273">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="998e0-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="998e0-274">**MS-SQL-Склрепоситори**</span><span class="sxs-lookup"><span data-stu-id="998e0-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





