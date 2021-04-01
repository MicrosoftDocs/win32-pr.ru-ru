---
title: MS-SQL-атрибут Memory
description: Объем памяти компьютера.
ms.assetid: 36d69b8a-669b-4488-a75e-3b0af7f9845a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута памяти MS-SQL
- Схема AD атрибута памяти mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Memory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7f6b96f2a591e05df8bf325b028172ef713dc5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139015"
---
# <a name="ms-sql-memory-attribute"></a><span data-ttu-id="afe4c-105">MS-SQL-атрибут Memory</span><span class="sxs-lookup"><span data-stu-id="afe4c-105">MS-SQL-Memory attribute</span></span>

<span data-ttu-id="afe4c-106">Объем памяти компьютера.</span><span class="sxs-lookup"><span data-stu-id="afe4c-106">The amount of memory on the computer.</span></span>



| <span data-ttu-id="afe4c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-107">Entry</span></span> | <span data-ttu-id="afe4c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="afe4c-109">CN</span><span class="sxs-lookup"><span data-stu-id="afe4c-109">CN</span></span>                | <span data-ttu-id="afe4c-110">MS-SQL-память</span><span class="sxs-lookup"><span data-stu-id="afe4c-110">MS-SQL-Memory</span></span>                        |
| <span data-ttu-id="afe4c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="afe4c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="afe4c-112">mS-SQL-память</span><span class="sxs-lookup"><span data-stu-id="afe4c-112">mS-SQL-Memory</span></span>                        |
| <span data-ttu-id="afe4c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="afe4c-113">Size</span></span>              | <span data-ttu-id="afe4c-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="afe4c-114">8 bytes</span></span>                              |
| <span data-ttu-id="afe4c-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="afe4c-115">Update Privilege</span></span>  | <span data-ttu-id="afe4c-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="afe4c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="afe4c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="afe4c-117">Update Frequency</span></span>  | <span data-ttu-id="afe4c-118">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="afe4c-118">At system startup.</span></span>                   |
| <span data-ttu-id="afe4c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-119">Attribute-Id</span></span>      | <span data-ttu-id="afe4c-120">1.2.840.113556.1.4.1367</span><span class="sxs-lookup"><span data-stu-id="afe4c-120">1.2.840.113556.1.4.1367</span></span>              |
| <span data-ttu-id="afe4c-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="afe4c-121">System-Id-Guid</span></span>    | <span data-ttu-id="afe4c-122">5b5d448c-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="afe4c-122">5b5d448c-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="afe4c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afe4c-123">Syntax</span></span>            | [<span data-ttu-id="afe4c-124">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="afe4c-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="afe4c-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="afe4c-125">Implementations</span></span>

-   [<span data-ttu-id="afe4c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="afe4c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="afe4c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afe4c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afe4c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afe4c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afe4c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afe4c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afe4c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afe4c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afe4c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afe4c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="afe4c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afe4c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="afe4c-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-133">Entry</span></span> | <span data-ttu-id="afe4c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afe4c-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afe4c-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="afe4c-137">System-Only</span></span>            | <span data-ttu-id="afe4c-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-138">False</span></span>                                                     |
| <span data-ttu-id="afe4c-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afe4c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="afe4c-140">True</span><span class="sxs-lookup"><span data-stu-id="afe4c-140">True</span></span>                                                      |
| <span data-ttu-id="afe4c-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afe4c-141">Is Indexed</span></span>             | <span data-ttu-id="afe4c-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-142">False</span></span>                                                     |
| <span data-ttu-id="afe4c-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afe4c-143">In Global Catalog</span></span>      | <span data-ttu-id="afe4c-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-144">False</span></span>                                                     |
| <span data-ttu-id="afe4c-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afe4c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="afe4c-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afe4c-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="afe4c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afe4c-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afe4c-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-149">Search-Flags</span></span>           | <span data-ttu-id="afe4c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afe4c-150">0x00000000</span></span>                                                |
| <span data-ttu-id="afe4c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-151">System-Flags</span></span>           | <span data-ttu-id="afe4c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afe4c-152">0x00000010</span></span>                                                |
| <span data-ttu-id="afe4c-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afe4c-153">Classes used in</span></span>        | [<span data-ttu-id="afe4c-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="afe4c-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="afe4c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afe4c-155">Windows Server 2003</span></span>



| <span data-ttu-id="afe4c-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-156">Entry</span></span> | <span data-ttu-id="afe4c-157">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afe4c-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afe4c-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="afe4c-160">System-Only</span></span>            | <span data-ttu-id="afe4c-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-161">False</span></span>                                                     |
| <span data-ttu-id="afe4c-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afe4c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="afe4c-163">True</span><span class="sxs-lookup"><span data-stu-id="afe4c-163">True</span></span>                                                      |
| <span data-ttu-id="afe4c-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afe4c-164">Is Indexed</span></span>             | <span data-ttu-id="afe4c-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-165">False</span></span>                                                     |
| <span data-ttu-id="afe4c-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afe4c-166">In Global Catalog</span></span>      | <span data-ttu-id="afe4c-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-167">False</span></span>                                                     |
| <span data-ttu-id="afe4c-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afe4c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="afe4c-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afe4c-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="afe4c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afe4c-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afe4c-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-172">Search-Flags</span></span>           | <span data-ttu-id="afe4c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afe4c-173">0x00000000</span></span>                                                |
| <span data-ttu-id="afe4c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-174">System-Flags</span></span>           | <span data-ttu-id="afe4c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afe4c-175">0x00000010</span></span>                                                |
| <span data-ttu-id="afe4c-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afe4c-176">Classes used in</span></span>        | [<span data-ttu-id="afe4c-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="afe4c-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afe4c-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afe4c-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afe4c-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-179">Entry</span></span> | <span data-ttu-id="afe4c-180">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afe4c-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afe4c-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="afe4c-183">System-Only</span></span>            | <span data-ttu-id="afe4c-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-184">False</span></span>                                                     |
| <span data-ttu-id="afe4c-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afe4c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="afe4c-186">True</span><span class="sxs-lookup"><span data-stu-id="afe4c-186">True</span></span>                                                      |
| <span data-ttu-id="afe4c-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afe4c-187">Is Indexed</span></span>             | <span data-ttu-id="afe4c-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-188">False</span></span>                                                     |
| <span data-ttu-id="afe4c-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afe4c-189">In Global Catalog</span></span>      | <span data-ttu-id="afe4c-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-190">False</span></span>                                                     |
| <span data-ttu-id="afe4c-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afe4c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="afe4c-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afe4c-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="afe4c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afe4c-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afe4c-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-195">Search-Flags</span></span>           | <span data-ttu-id="afe4c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afe4c-196">0x00000000</span></span>                                                |
| <span data-ttu-id="afe4c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-197">System-Flags</span></span>           | <span data-ttu-id="afe4c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afe4c-198">0x00000010</span></span>                                                |
| <span data-ttu-id="afe4c-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afe4c-199">Classes used in</span></span>        | [<span data-ttu-id="afe4c-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="afe4c-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afe4c-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afe4c-201">Windows Server 2008</span></span>



| <span data-ttu-id="afe4c-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-202">Entry</span></span> | <span data-ttu-id="afe4c-203">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afe4c-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afe4c-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="afe4c-206">System-Only</span></span>            | <span data-ttu-id="afe4c-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-207">False</span></span>                                                     |
| <span data-ttu-id="afe4c-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afe4c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="afe4c-209">True</span><span class="sxs-lookup"><span data-stu-id="afe4c-209">True</span></span>                                                      |
| <span data-ttu-id="afe4c-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afe4c-210">Is Indexed</span></span>             | <span data-ttu-id="afe4c-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-211">False</span></span>                                                     |
| <span data-ttu-id="afe4c-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afe4c-212">In Global Catalog</span></span>      | <span data-ttu-id="afe4c-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-213">False</span></span>                                                     |
| <span data-ttu-id="afe4c-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afe4c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="afe4c-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afe4c-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="afe4c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afe4c-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afe4c-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-218">Search-Flags</span></span>           | <span data-ttu-id="afe4c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afe4c-219">0x00000000</span></span>                                                |
| <span data-ttu-id="afe4c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-220">System-Flags</span></span>           | <span data-ttu-id="afe4c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afe4c-221">0x00000010</span></span>                                                |
| <span data-ttu-id="afe4c-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afe4c-222">Classes used in</span></span>        | [<span data-ttu-id="afe4c-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="afe4c-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afe4c-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afe4c-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afe4c-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-225">Entry</span></span> | <span data-ttu-id="afe4c-226">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afe4c-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afe4c-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="afe4c-229">System-Only</span></span>            | <span data-ttu-id="afe4c-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-230">False</span></span>                                                     |
| <span data-ttu-id="afe4c-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afe4c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="afe4c-232">True</span><span class="sxs-lookup"><span data-stu-id="afe4c-232">True</span></span>                                                      |
| <span data-ttu-id="afe4c-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afe4c-233">Is Indexed</span></span>             | <span data-ttu-id="afe4c-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-234">False</span></span>                                                     |
| <span data-ttu-id="afe4c-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afe4c-235">In Global Catalog</span></span>      | <span data-ttu-id="afe4c-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-236">False</span></span>                                                     |
| <span data-ttu-id="afe4c-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afe4c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="afe4c-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afe4c-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="afe4c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afe4c-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afe4c-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-241">Search-Flags</span></span>           | <span data-ttu-id="afe4c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afe4c-242">0x00000000</span></span>                                                |
| <span data-ttu-id="afe4c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-243">System-Flags</span></span>           | <span data-ttu-id="afe4c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afe4c-244">0x00000010</span></span>                                                |
| <span data-ttu-id="afe4c-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afe4c-245">Classes used in</span></span>        | [<span data-ttu-id="afe4c-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="afe4c-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afe4c-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afe4c-247">Windows Server 2012</span></span>



| <span data-ttu-id="afe4c-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="afe4c-248">Entry</span></span> | <span data-ttu-id="afe4c-249">Значение</span><span class="sxs-lookup"><span data-stu-id="afe4c-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afe4c-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afe4c-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afe4c-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="afe4c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="afe4c-252">System-Only</span></span>            | <span data-ttu-id="afe4c-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-253">False</span></span>                                                     |
| <span data-ttu-id="afe4c-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afe4c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="afe4c-255">True</span><span class="sxs-lookup"><span data-stu-id="afe4c-255">True</span></span>                                                      |
| <span data-ttu-id="afe4c-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afe4c-256">Is Indexed</span></span>             | <span data-ttu-id="afe4c-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-257">False</span></span>                                                     |
| <span data-ttu-id="afe4c-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afe4c-258">In Global Catalog</span></span>      | <span data-ttu-id="afe4c-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="afe4c-259">False</span></span>                                                     |
| <span data-ttu-id="afe4c-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afe4c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="afe4c-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afe4c-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="afe4c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afe4c-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afe4c-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="afe4c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-264">Search-Flags</span></span>           | <span data-ttu-id="afe4c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afe4c-265">0x00000000</span></span>                                                |
| <span data-ttu-id="afe4c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afe4c-266">System-Flags</span></span>           | <span data-ttu-id="afe4c-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afe4c-267">0x00000010</span></span>                                                |
| <span data-ttu-id="afe4c-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afe4c-268">Classes used in</span></span>        | [<span data-ttu-id="afe4c-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="afe4c-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





