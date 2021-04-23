---
title: MS-SQL-многопротокольный атрибут
description: Точка подключения RPC.
ms.assetid: 70cb9f80-7140-4c26-a1a4-f78a60de430f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута протокола MS-SQL-Multiprotocol
- Схема AD атрибута протокола mS-SQL-Multiprotocol
topic_type:
- apiref
api_name:
- MS-SQL-MultiProtocol
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cdfb8e42d8e3d533090b7b0bf49dcefc5492a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654901"
---
# <a name="ms-sql-multiprotocol-attribute"></a><span data-ttu-id="b5689-105">MS-SQL-многопротокольный атрибут</span><span class="sxs-lookup"><span data-stu-id="b5689-105">MS-SQL-MultiProtocol attribute</span></span>

<span data-ttu-id="b5689-106">Точка подключения RPC.</span><span class="sxs-lookup"><span data-stu-id="b5689-106">The RPC connection point.</span></span>



| <span data-ttu-id="b5689-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-107">Entry</span></span> | <span data-ttu-id="b5689-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b5689-109">CN</span><span class="sxs-lookup"><span data-stu-id="b5689-109">CN</span></span>                | <span data-ttu-id="b5689-110">Протокол MS-SQL-Multiprotocol</span><span class="sxs-lookup"><span data-stu-id="b5689-110">MS-SQL-MultiProtocol</span></span>                        |
| <span data-ttu-id="b5689-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b5689-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b5689-112">Протокол mS-SQL-Multiprotocol</span><span class="sxs-lookup"><span data-stu-id="b5689-112">mS-SQL-MultiProtocol</span></span>                        |
| <span data-ttu-id="b5689-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b5689-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b5689-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b5689-114">Update Privilege</span></span>  | <span data-ttu-id="b5689-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b5689-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="b5689-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b5689-116">Update Frequency</span></span>  | <span data-ttu-id="b5689-117">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="b5689-117">At system startup.</span></span>                          |
| <span data-ttu-id="b5689-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-118">Attribute-Id</span></span>      | <span data-ttu-id="b5689-119">1.2.840.113556.1.4.1375</span><span class="sxs-lookup"><span data-stu-id="b5689-119">1.2.840.113556.1.4.1375</span></span>                     |
| <span data-ttu-id="b5689-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b5689-120">System-Id-Guid</span></span>    | <span data-ttu-id="b5689-121">8157fa38-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b5689-121">8157fa38-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="b5689-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5689-122">Syntax</span></span>            | [<span data-ttu-id="b5689-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b5689-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b5689-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b5689-124">Implementations</span></span>

-   [<span data-ttu-id="b5689-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b5689-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b5689-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5689-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5689-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5689-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5689-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5689-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5689-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5689-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5689-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5689-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b5689-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5689-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b5689-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-132">Entry</span></span> | <span data-ttu-id="b5689-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b5689-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b5689-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5689-136">System-Only</span></span>            | <span data-ttu-id="b5689-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-137">False</span></span>                                                     |
| <span data-ttu-id="b5689-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b5689-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b5689-139">True</span><span class="sxs-lookup"><span data-stu-id="b5689-139">True</span></span>                                                      |
| <span data-ttu-id="b5689-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b5689-140">Is Indexed</span></span>             | <span data-ttu-id="b5689-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-141">False</span></span>                                                     |
| <span data-ttu-id="b5689-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b5689-142">In Global Catalog</span></span>      | <span data-ttu-id="b5689-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-143">False</span></span>                                                     |
| <span data-ttu-id="b5689-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b5689-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5689-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5689-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b5689-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5689-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5689-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-148">Search-Flags</span></span>           | <span data-ttu-id="b5689-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5689-149">0x00000000</span></span>                                                |
| <span data-ttu-id="b5689-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-150">System-Flags</span></span>           | <span data-ttu-id="b5689-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5689-151">0x00000010</span></span>                                                |
| <span data-ttu-id="b5689-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b5689-152">Classes used in</span></span>        | [<span data-ttu-id="b5689-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b5689-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b5689-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5689-154">Windows Server 2003</span></span>



| <span data-ttu-id="b5689-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-155">Entry</span></span> | <span data-ttu-id="b5689-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b5689-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b5689-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5689-159">System-Only</span></span>            | <span data-ttu-id="b5689-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-160">False</span></span>                                                     |
| <span data-ttu-id="b5689-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b5689-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b5689-162">True</span><span class="sxs-lookup"><span data-stu-id="b5689-162">True</span></span>                                                      |
| <span data-ttu-id="b5689-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b5689-163">Is Indexed</span></span>             | <span data-ttu-id="b5689-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-164">False</span></span>                                                     |
| <span data-ttu-id="b5689-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b5689-165">In Global Catalog</span></span>      | <span data-ttu-id="b5689-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-166">False</span></span>                                                     |
| <span data-ttu-id="b5689-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b5689-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5689-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5689-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b5689-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5689-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5689-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-171">Search-Flags</span></span>           | <span data-ttu-id="b5689-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5689-172">0x00000000</span></span>                                                |
| <span data-ttu-id="b5689-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-173">System-Flags</span></span>           | <span data-ttu-id="b5689-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5689-174">0x00000010</span></span>                                                |
| <span data-ttu-id="b5689-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b5689-175">Classes used in</span></span>        | [<span data-ttu-id="b5689-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b5689-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5689-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5689-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5689-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-178">Entry</span></span> | <span data-ttu-id="b5689-179">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b5689-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b5689-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5689-182">System-Only</span></span>            | <span data-ttu-id="b5689-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-183">False</span></span>                                                     |
| <span data-ttu-id="b5689-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b5689-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b5689-185">True</span><span class="sxs-lookup"><span data-stu-id="b5689-185">True</span></span>                                                      |
| <span data-ttu-id="b5689-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b5689-186">Is Indexed</span></span>             | <span data-ttu-id="b5689-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-187">False</span></span>                                                     |
| <span data-ttu-id="b5689-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b5689-188">In Global Catalog</span></span>      | <span data-ttu-id="b5689-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-189">False</span></span>                                                     |
| <span data-ttu-id="b5689-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b5689-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5689-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5689-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b5689-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5689-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5689-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-194">Search-Flags</span></span>           | <span data-ttu-id="b5689-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5689-195">0x00000000</span></span>                                                |
| <span data-ttu-id="b5689-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-196">System-Flags</span></span>           | <span data-ttu-id="b5689-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5689-197">0x00000010</span></span>                                                |
| <span data-ttu-id="b5689-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b5689-198">Classes used in</span></span>        | [<span data-ttu-id="b5689-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b5689-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5689-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5689-200">Windows Server 2008</span></span>



| <span data-ttu-id="b5689-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-201">Entry</span></span> | <span data-ttu-id="b5689-202">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b5689-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b5689-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5689-205">System-Only</span></span>            | <span data-ttu-id="b5689-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-206">False</span></span>                                                     |
| <span data-ttu-id="b5689-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b5689-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b5689-208">True</span><span class="sxs-lookup"><span data-stu-id="b5689-208">True</span></span>                                                      |
| <span data-ttu-id="b5689-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b5689-209">Is Indexed</span></span>             | <span data-ttu-id="b5689-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-210">False</span></span>                                                     |
| <span data-ttu-id="b5689-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b5689-211">In Global Catalog</span></span>      | <span data-ttu-id="b5689-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-212">False</span></span>                                                     |
| <span data-ttu-id="b5689-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b5689-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5689-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5689-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b5689-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5689-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5689-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-217">Search-Flags</span></span>           | <span data-ttu-id="b5689-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5689-218">0x00000000</span></span>                                                |
| <span data-ttu-id="b5689-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-219">System-Flags</span></span>           | <span data-ttu-id="b5689-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5689-220">0x00000010</span></span>                                                |
| <span data-ttu-id="b5689-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b5689-221">Classes used in</span></span>        | [<span data-ttu-id="b5689-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b5689-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5689-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5689-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5689-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-224">Entry</span></span> | <span data-ttu-id="b5689-225">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b5689-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b5689-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5689-228">System-Only</span></span>            | <span data-ttu-id="b5689-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-229">False</span></span>                                                     |
| <span data-ttu-id="b5689-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b5689-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b5689-231">True</span><span class="sxs-lookup"><span data-stu-id="b5689-231">True</span></span>                                                      |
| <span data-ttu-id="b5689-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b5689-232">Is Indexed</span></span>             | <span data-ttu-id="b5689-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-233">False</span></span>                                                     |
| <span data-ttu-id="b5689-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b5689-234">In Global Catalog</span></span>      | <span data-ttu-id="b5689-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-235">False</span></span>                                                     |
| <span data-ttu-id="b5689-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b5689-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5689-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5689-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b5689-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5689-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5689-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-240">Search-Flags</span></span>           | <span data-ttu-id="b5689-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5689-241">0x00000000</span></span>                                                |
| <span data-ttu-id="b5689-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-242">System-Flags</span></span>           | <span data-ttu-id="b5689-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5689-243">0x00000010</span></span>                                                |
| <span data-ttu-id="b5689-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b5689-244">Classes used in</span></span>        | [<span data-ttu-id="b5689-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b5689-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5689-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5689-246">Windows Server 2012</span></span>



| <span data-ttu-id="b5689-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="b5689-247">Entry</span></span> | <span data-ttu-id="b5689-248">Значение</span><span class="sxs-lookup"><span data-stu-id="b5689-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b5689-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b5689-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5689-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b5689-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5689-251">System-Only</span></span>            | <span data-ttu-id="b5689-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-252">False</span></span>                                                     |
| <span data-ttu-id="b5689-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b5689-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b5689-254">True</span><span class="sxs-lookup"><span data-stu-id="b5689-254">True</span></span>                                                      |
| <span data-ttu-id="b5689-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b5689-255">Is Indexed</span></span>             | <span data-ttu-id="b5689-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-256">False</span></span>                                                     |
| <span data-ttu-id="b5689-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b5689-257">In Global Catalog</span></span>      | <span data-ttu-id="b5689-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="b5689-258">False</span></span>                                                     |
| <span data-ttu-id="b5689-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b5689-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5689-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5689-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b5689-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5689-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5689-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b5689-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-263">Search-Flags</span></span>           | <span data-ttu-id="b5689-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5689-264">0x00000000</span></span>                                                |
| <span data-ttu-id="b5689-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5689-265">System-Flags</span></span>           | <span data-ttu-id="b5689-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5689-266">0x00000010</span></span>                                                |
| <span data-ttu-id="b5689-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b5689-267">Classes used in</span></span>        | [<span data-ttu-id="b5689-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b5689-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





