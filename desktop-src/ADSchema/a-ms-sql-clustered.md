---
title: MS-SQL-кластеризованный атрибут
description: Значение true, если сервер кластеризован.
ms.assetid: 066609a4-fdf1-422b-9b26-445f617c99d4
ms.tgt_platform: multiple
keywords:
- MS-SQL — схема AD атрибутов с группировкой
- mS-SQL — схема AD атрибутов с группировкой
topic_type:
- apiref
api_name:
- MS-SQL-Clustered
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ba701168f3dff5b3809818a6df987855a08e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654909"
---
# <a name="ms-sql-clustered-attribute"></a><span data-ttu-id="00c96-105">MS-SQL-кластеризованный атрибут</span><span class="sxs-lookup"><span data-stu-id="00c96-105">MS-SQL-Clustered attribute</span></span>

<span data-ttu-id="00c96-106">Значение true, если сервер кластеризован.</span><span class="sxs-lookup"><span data-stu-id="00c96-106">True if the server is clustered.</span></span>



| <span data-ttu-id="00c96-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-107">Entry</span></span> | <span data-ttu-id="00c96-108">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="00c96-109">CN</span><span class="sxs-lookup"><span data-stu-id="00c96-109">CN</span></span>                | <span data-ttu-id="00c96-110">MS-SQL-Clustered</span><span class="sxs-lookup"><span data-stu-id="00c96-110">MS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="00c96-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="00c96-111">Ldap-Display-Name</span></span> | <span data-ttu-id="00c96-112">mS-SQL-Clustered</span><span class="sxs-lookup"><span data-stu-id="00c96-112">mS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="00c96-113">Размер</span><span class="sxs-lookup"><span data-stu-id="00c96-113">Size</span></span>              | <span data-ttu-id="00c96-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="00c96-114">4 bytes</span></span>                              |
| <span data-ttu-id="00c96-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="00c96-115">Update Privilege</span></span>  | <span data-ttu-id="00c96-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="00c96-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="00c96-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="00c96-117">Update Frequency</span></span>  | <span data-ttu-id="00c96-118">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="00c96-118">At system startup.</span></span>                   |
| <span data-ttu-id="00c96-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-119">Attribute-Id</span></span>      | <span data-ttu-id="00c96-120">1.2.840.113556.1.4.1373</span><span class="sxs-lookup"><span data-stu-id="00c96-120">1.2.840.113556.1.4.1373</span></span>              |
| <span data-ttu-id="00c96-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="00c96-121">System-Id-Guid</span></span>    | <span data-ttu-id="00c96-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="00c96-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="00c96-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00c96-123">Syntax</span></span>            | [<span data-ttu-id="00c96-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="00c96-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="00c96-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="00c96-125">Implementations</span></span>

-   [<span data-ttu-id="00c96-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="00c96-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="00c96-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00c96-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00c96-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00c96-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00c96-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00c96-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00c96-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00c96-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00c96-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00c96-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="00c96-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00c96-132">Windows 2000 Server</span></span>



| <span data-ttu-id="00c96-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-133">Entry</span></span> | <span data-ttu-id="00c96-134">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00c96-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="00c96-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="00c96-137">System-Only</span></span>            | <span data-ttu-id="00c96-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-138">False</span></span>                                                     |
| <span data-ttu-id="00c96-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="00c96-139">Is-Single-Valued</span></span>       | <span data-ttu-id="00c96-140">True</span><span class="sxs-lookup"><span data-stu-id="00c96-140">True</span></span>                                                      |
| <span data-ttu-id="00c96-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="00c96-141">Is Indexed</span></span>             | <span data-ttu-id="00c96-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-142">False</span></span>                                                     |
| <span data-ttu-id="00c96-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="00c96-143">In Global Catalog</span></span>      | <span data-ttu-id="00c96-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-144">False</span></span>                                                     |
| <span data-ttu-id="00c96-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="00c96-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="00c96-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00c96-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="00c96-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00c96-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00c96-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-149">Search-Flags</span></span>           | <span data-ttu-id="00c96-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c96-150">0x00000000</span></span>                                                |
| <span data-ttu-id="00c96-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-151">System-Flags</span></span>           | <span data-ttu-id="00c96-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00c96-152">0x00000010</span></span>                                                |
| <span data-ttu-id="00c96-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="00c96-153">Classes used in</span></span>        | [<span data-ttu-id="00c96-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="00c96-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="00c96-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00c96-155">Windows Server 2003</span></span>



| <span data-ttu-id="00c96-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-156">Entry</span></span> | <span data-ttu-id="00c96-157">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00c96-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="00c96-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="00c96-160">System-Only</span></span>            | <span data-ttu-id="00c96-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-161">False</span></span>                                                     |
| <span data-ttu-id="00c96-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="00c96-162">Is-Single-Valued</span></span>       | <span data-ttu-id="00c96-163">True</span><span class="sxs-lookup"><span data-stu-id="00c96-163">True</span></span>                                                      |
| <span data-ttu-id="00c96-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="00c96-164">Is Indexed</span></span>             | <span data-ttu-id="00c96-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-165">False</span></span>                                                     |
| <span data-ttu-id="00c96-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="00c96-166">In Global Catalog</span></span>      | <span data-ttu-id="00c96-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-167">False</span></span>                                                     |
| <span data-ttu-id="00c96-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="00c96-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="00c96-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00c96-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="00c96-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00c96-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00c96-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-172">Search-Flags</span></span>           | <span data-ttu-id="00c96-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c96-173">0x00000000</span></span>                                                |
| <span data-ttu-id="00c96-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-174">System-Flags</span></span>           | <span data-ttu-id="00c96-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00c96-175">0x00000010</span></span>                                                |
| <span data-ttu-id="00c96-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="00c96-176">Classes used in</span></span>        | [<span data-ttu-id="00c96-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="00c96-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00c96-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00c96-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00c96-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-179">Entry</span></span> | <span data-ttu-id="00c96-180">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00c96-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="00c96-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="00c96-183">System-Only</span></span>            | <span data-ttu-id="00c96-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-184">False</span></span>                                                     |
| <span data-ttu-id="00c96-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="00c96-185">Is-Single-Valued</span></span>       | <span data-ttu-id="00c96-186">True</span><span class="sxs-lookup"><span data-stu-id="00c96-186">True</span></span>                                                      |
| <span data-ttu-id="00c96-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="00c96-187">Is Indexed</span></span>             | <span data-ttu-id="00c96-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-188">False</span></span>                                                     |
| <span data-ttu-id="00c96-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="00c96-189">In Global Catalog</span></span>      | <span data-ttu-id="00c96-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-190">False</span></span>                                                     |
| <span data-ttu-id="00c96-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="00c96-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="00c96-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00c96-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="00c96-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00c96-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00c96-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-195">Search-Flags</span></span>           | <span data-ttu-id="00c96-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c96-196">0x00000000</span></span>                                                |
| <span data-ttu-id="00c96-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-197">System-Flags</span></span>           | <span data-ttu-id="00c96-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00c96-198">0x00000010</span></span>                                                |
| <span data-ttu-id="00c96-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="00c96-199">Classes used in</span></span>        | [<span data-ttu-id="00c96-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="00c96-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00c96-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00c96-201">Windows Server 2008</span></span>



| <span data-ttu-id="00c96-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-202">Entry</span></span> | <span data-ttu-id="00c96-203">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00c96-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="00c96-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="00c96-206">System-Only</span></span>            | <span data-ttu-id="00c96-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-207">False</span></span>                                                     |
| <span data-ttu-id="00c96-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="00c96-208">Is-Single-Valued</span></span>       | <span data-ttu-id="00c96-209">True</span><span class="sxs-lookup"><span data-stu-id="00c96-209">True</span></span>                                                      |
| <span data-ttu-id="00c96-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="00c96-210">Is Indexed</span></span>             | <span data-ttu-id="00c96-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-211">False</span></span>                                                     |
| <span data-ttu-id="00c96-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="00c96-212">In Global Catalog</span></span>      | <span data-ttu-id="00c96-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-213">False</span></span>                                                     |
| <span data-ttu-id="00c96-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="00c96-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="00c96-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00c96-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="00c96-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00c96-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00c96-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-218">Search-Flags</span></span>           | <span data-ttu-id="00c96-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c96-219">0x00000000</span></span>                                                |
| <span data-ttu-id="00c96-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-220">System-Flags</span></span>           | <span data-ttu-id="00c96-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00c96-221">0x00000010</span></span>                                                |
| <span data-ttu-id="00c96-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="00c96-222">Classes used in</span></span>        | [<span data-ttu-id="00c96-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="00c96-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00c96-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00c96-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00c96-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-225">Entry</span></span> | <span data-ttu-id="00c96-226">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00c96-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="00c96-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="00c96-229">System-Only</span></span>            | <span data-ttu-id="00c96-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-230">False</span></span>                                                     |
| <span data-ttu-id="00c96-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="00c96-231">Is-Single-Valued</span></span>       | <span data-ttu-id="00c96-232">True</span><span class="sxs-lookup"><span data-stu-id="00c96-232">True</span></span>                                                      |
| <span data-ttu-id="00c96-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="00c96-233">Is Indexed</span></span>             | <span data-ttu-id="00c96-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-234">False</span></span>                                                     |
| <span data-ttu-id="00c96-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="00c96-235">In Global Catalog</span></span>      | <span data-ttu-id="00c96-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-236">False</span></span>                                                     |
| <span data-ttu-id="00c96-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="00c96-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="00c96-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00c96-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="00c96-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00c96-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00c96-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-241">Search-Flags</span></span>           | <span data-ttu-id="00c96-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c96-242">0x00000000</span></span>                                                |
| <span data-ttu-id="00c96-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-243">System-Flags</span></span>           | <span data-ttu-id="00c96-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00c96-244">0x00000010</span></span>                                                |
| <span data-ttu-id="00c96-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="00c96-245">Classes used in</span></span>        | [<span data-ttu-id="00c96-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="00c96-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00c96-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00c96-247">Windows Server 2012</span></span>



| <span data-ttu-id="00c96-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="00c96-248">Entry</span></span> | <span data-ttu-id="00c96-249">Значение</span><span class="sxs-lookup"><span data-stu-id="00c96-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00c96-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="00c96-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00c96-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="00c96-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="00c96-252">System-Only</span></span>            | <span data-ttu-id="00c96-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-253">False</span></span>                                                     |
| <span data-ttu-id="00c96-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="00c96-254">Is-Single-Valued</span></span>       | <span data-ttu-id="00c96-255">True</span><span class="sxs-lookup"><span data-stu-id="00c96-255">True</span></span>                                                      |
| <span data-ttu-id="00c96-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="00c96-256">Is Indexed</span></span>             | <span data-ttu-id="00c96-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-257">False</span></span>                                                     |
| <span data-ttu-id="00c96-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="00c96-258">In Global Catalog</span></span>      | <span data-ttu-id="00c96-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="00c96-259">False</span></span>                                                     |
| <span data-ttu-id="00c96-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="00c96-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="00c96-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00c96-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="00c96-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00c96-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00c96-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="00c96-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-264">Search-Flags</span></span>           | <span data-ttu-id="00c96-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c96-265">0x00000000</span></span>                                                |
| <span data-ttu-id="00c96-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00c96-266">System-Flags</span></span>           | <span data-ttu-id="00c96-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00c96-267">0x00000010</span></span>                                                |
| <span data-ttu-id="00c96-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="00c96-268">Classes used in</span></span>        | [<span data-ttu-id="00c96-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="00c96-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





