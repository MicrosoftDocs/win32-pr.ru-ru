---
title: Атрибут MS-SQL-SortOrder
description: Порядок сортировки текущего экземпляра SQL Server.
ms.assetid: cd58cb56-19aa-4ee6-b241-1198b3e9e097
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "MS-SQL-SortOrder"
- Схема AD атрибута "mS-SQL-SortOrder"
topic_type:
- apiref
api_name:
- MS-SQL-SortOrder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940dafa4cc9bfce15ae1a5df472720e6e779f19e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654896"
---
# <a name="ms-sql-sortorder-attribute"></a><span data-ttu-id="e2fbb-105">Атрибут MS-SQL-SortOrder</span><span class="sxs-lookup"><span data-stu-id="e2fbb-105">MS-SQL-SortOrder attribute</span></span>

<span data-ttu-id="e2fbb-106">Порядок сортировки текущего экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-106">The sort order for the current instance of SQL Server.</span></span>



| <span data-ttu-id="e2fbb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-107">Entry</span></span> | <span data-ttu-id="e2fbb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e2fbb-109">CN</span><span class="sxs-lookup"><span data-stu-id="e2fbb-109">CN</span></span>                | <span data-ttu-id="e2fbb-110">MS-SQL-SortOrder</span><span class="sxs-lookup"><span data-stu-id="e2fbb-110">MS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="e2fbb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e2fbb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e2fbb-112">mS-SQL-SortOrder</span><span class="sxs-lookup"><span data-stu-id="e2fbb-112">mS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="e2fbb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e2fbb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e2fbb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e2fbb-114">Update Privilege</span></span>  | <span data-ttu-id="e2fbb-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="e2fbb-115">Domain administrator</span></span>                        |
| <span data-ttu-id="e2fbb-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e2fbb-116">Update Frequency</span></span>  | <span data-ttu-id="e2fbb-117">При установке системы.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-117">At system setup.</span></span>                            |
| <span data-ttu-id="e2fbb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-118">Attribute-Id</span></span>      | <span data-ttu-id="e2fbb-119">1.2.840.113556.1.4.1371</span><span class="sxs-lookup"><span data-stu-id="e2fbb-119">1.2.840.113556.1.4.1371</span></span>                     |
| <span data-ttu-id="e2fbb-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e2fbb-120">System-Id-Guid</span></span>    | <span data-ttu-id="e2fbb-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e2fbb-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="e2fbb-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2fbb-122">Syntax</span></span>            | [<span data-ttu-id="e2fbb-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e2fbb-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e2fbb-124">Implementations</span></span>

-   [<span data-ttu-id="e2fbb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e2fbb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e2fbb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e2fbb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e2fbb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e2fbb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e2fbb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2fbb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e2fbb-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-132">Entry</span></span> | <span data-ttu-id="e2fbb-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e2fbb-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2fbb-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2fbb-136">System-Only</span></span>            | <span data-ttu-id="e2fbb-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-137">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2fbb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e2fbb-139">True</span><span class="sxs-lookup"><span data-stu-id="e2fbb-139">True</span></span>                                                      |
| <span data-ttu-id="e2fbb-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2fbb-140">Is Indexed</span></span>             | <span data-ttu-id="e2fbb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-141">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2fbb-142">In Global Catalog</span></span>      | <span data-ttu-id="e2fbb-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-143">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2fbb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2fbb-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e2fbb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2fbb-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2fbb-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-148">Search-Flags</span></span>           | <span data-ttu-id="e2fbb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2fbb-149">0x00000000</span></span>                                                |
| <span data-ttu-id="e2fbb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-150">System-Flags</span></span>           | <span data-ttu-id="e2fbb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2fbb-151">0x00000010</span></span>                                                |
| <span data-ttu-id="e2fbb-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2fbb-152">Classes used in</span></span>        | [<span data-ttu-id="e2fbb-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e2fbb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2fbb-154">Windows Server 2003</span></span>



| <span data-ttu-id="e2fbb-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-155">Entry</span></span> | <span data-ttu-id="e2fbb-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e2fbb-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2fbb-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2fbb-159">System-Only</span></span>            | <span data-ttu-id="e2fbb-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-160">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2fbb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e2fbb-162">True</span><span class="sxs-lookup"><span data-stu-id="e2fbb-162">True</span></span>                                                      |
| <span data-ttu-id="e2fbb-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2fbb-163">Is Indexed</span></span>             | <span data-ttu-id="e2fbb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-164">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2fbb-165">In Global Catalog</span></span>      | <span data-ttu-id="e2fbb-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-166">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2fbb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2fbb-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e2fbb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2fbb-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2fbb-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-171">Search-Flags</span></span>           | <span data-ttu-id="e2fbb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2fbb-172">0x00000000</span></span>                                                |
| <span data-ttu-id="e2fbb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-173">System-Flags</span></span>           | <span data-ttu-id="e2fbb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2fbb-174">0x00000010</span></span>                                                |
| <span data-ttu-id="e2fbb-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2fbb-175">Classes used in</span></span>        | [<span data-ttu-id="e2fbb-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e2fbb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e2fbb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e2fbb-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-178">Entry</span></span> | <span data-ttu-id="e2fbb-179">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e2fbb-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2fbb-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2fbb-182">System-Only</span></span>            | <span data-ttu-id="e2fbb-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-183">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2fbb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e2fbb-185">True</span><span class="sxs-lookup"><span data-stu-id="e2fbb-185">True</span></span>                                                      |
| <span data-ttu-id="e2fbb-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2fbb-186">Is Indexed</span></span>             | <span data-ttu-id="e2fbb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-187">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2fbb-188">In Global Catalog</span></span>      | <span data-ttu-id="e2fbb-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-189">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2fbb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2fbb-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e2fbb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2fbb-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2fbb-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-194">Search-Flags</span></span>           | <span data-ttu-id="e2fbb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2fbb-195">0x00000000</span></span>                                                |
| <span data-ttu-id="e2fbb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-196">System-Flags</span></span>           | <span data-ttu-id="e2fbb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2fbb-197">0x00000010</span></span>                                                |
| <span data-ttu-id="e2fbb-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2fbb-198">Classes used in</span></span>        | [<span data-ttu-id="e2fbb-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e2fbb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2fbb-200">Windows Server 2008</span></span>



| <span data-ttu-id="e2fbb-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-201">Entry</span></span> | <span data-ttu-id="e2fbb-202">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e2fbb-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2fbb-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2fbb-205">System-Only</span></span>            | <span data-ttu-id="e2fbb-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-206">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2fbb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e2fbb-208">True</span><span class="sxs-lookup"><span data-stu-id="e2fbb-208">True</span></span>                                                      |
| <span data-ttu-id="e2fbb-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2fbb-209">Is Indexed</span></span>             | <span data-ttu-id="e2fbb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-210">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2fbb-211">In Global Catalog</span></span>      | <span data-ttu-id="e2fbb-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-212">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2fbb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2fbb-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e2fbb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2fbb-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2fbb-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-217">Search-Flags</span></span>           | <span data-ttu-id="e2fbb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2fbb-218">0x00000000</span></span>                                                |
| <span data-ttu-id="e2fbb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-219">System-Flags</span></span>           | <span data-ttu-id="e2fbb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2fbb-220">0x00000010</span></span>                                                |
| <span data-ttu-id="e2fbb-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2fbb-221">Classes used in</span></span>        | [<span data-ttu-id="e2fbb-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e2fbb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2fbb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e2fbb-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-224">Entry</span></span> | <span data-ttu-id="e2fbb-225">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e2fbb-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2fbb-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2fbb-228">System-Only</span></span>            | <span data-ttu-id="e2fbb-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-229">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2fbb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e2fbb-231">True</span><span class="sxs-lookup"><span data-stu-id="e2fbb-231">True</span></span>                                                      |
| <span data-ttu-id="e2fbb-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2fbb-232">Is Indexed</span></span>             | <span data-ttu-id="e2fbb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-233">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2fbb-234">In Global Catalog</span></span>      | <span data-ttu-id="e2fbb-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-235">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2fbb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2fbb-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e2fbb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2fbb-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2fbb-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-240">Search-Flags</span></span>           | <span data-ttu-id="e2fbb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2fbb-241">0x00000000</span></span>                                                |
| <span data-ttu-id="e2fbb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-242">System-Flags</span></span>           | <span data-ttu-id="e2fbb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2fbb-243">0x00000010</span></span>                                                |
| <span data-ttu-id="e2fbb-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2fbb-244">Classes used in</span></span>        | [<span data-ttu-id="e2fbb-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e2fbb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2fbb-246">Windows Server 2012</span></span>



| <span data-ttu-id="e2fbb-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2fbb-247">Entry</span></span> | <span data-ttu-id="e2fbb-248">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fbb-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e2fbb-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2fbb-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2fbb-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e2fbb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2fbb-251">System-Only</span></span>            | <span data-ttu-id="e2fbb-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-252">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2fbb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e2fbb-254">True</span><span class="sxs-lookup"><span data-stu-id="e2fbb-254">True</span></span>                                                      |
| <span data-ttu-id="e2fbb-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2fbb-255">Is Indexed</span></span>             | <span data-ttu-id="e2fbb-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-256">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2fbb-257">In Global Catalog</span></span>      | <span data-ttu-id="e2fbb-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2fbb-258">False</span></span>                                                     |
| <span data-ttu-id="e2fbb-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2fbb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2fbb-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e2fbb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2fbb-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2fbb-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e2fbb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-263">Search-Flags</span></span>           | <span data-ttu-id="e2fbb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2fbb-264">0x00000000</span></span>                                                |
| <span data-ttu-id="e2fbb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2fbb-265">System-Flags</span></span>           | <span data-ttu-id="e2fbb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2fbb-266">0x00000010</span></span>                                                |
| <span data-ttu-id="e2fbb-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2fbb-267">Classes used in</span></span>        | [<span data-ttu-id="e2fbb-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e2fbb-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





