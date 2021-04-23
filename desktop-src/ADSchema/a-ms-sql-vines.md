---
title: Атрибут MS-SQL-Vines
description: Точка подключения Vines.
ms.assetid: edb3ac70-6275-40e1-a91e-acf791c5cf23
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-SQL-Vines
- Схема AD атрибутов mS-SQL-Vines
topic_type:
- apiref
api_name:
- MS-SQL-Vines
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313b47714dbd8431a7552abc5ed7962e0c0a708a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654894"
---
# <a name="ms-sql-vines-attribute"></a><span data-ttu-id="2ae1f-105">Атрибут MS-SQL-Vines</span><span class="sxs-lookup"><span data-stu-id="2ae1f-105">MS-SQL-Vines attribute</span></span>

<span data-ttu-id="2ae1f-106">Точка подключения Vines.</span><span class="sxs-lookup"><span data-stu-id="2ae1f-106">The Vines connection point.</span></span>



| <span data-ttu-id="2ae1f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-107">Entry</span></span> | <span data-ttu-id="2ae1f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2ae1f-109">CN</span><span class="sxs-lookup"><span data-stu-id="2ae1f-109">CN</span></span>                | <span data-ttu-id="2ae1f-110">MS-SQL-Vines</span><span class="sxs-lookup"><span data-stu-id="2ae1f-110">MS-SQL-Vines</span></span>                                |
| <span data-ttu-id="2ae1f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2ae1f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2ae1f-112">mS-SQL-Vines</span><span class="sxs-lookup"><span data-stu-id="2ae1f-112">mS-SQL-Vines</span></span>                                |
| <span data-ttu-id="2ae1f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2ae1f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2ae1f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2ae1f-114">Update Privilege</span></span>  | <span data-ttu-id="2ae1f-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="2ae1f-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="2ae1f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2ae1f-116">Update Frequency</span></span>  | <span data-ttu-id="2ae1f-117">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="2ae1f-117">At system startup.</span></span>                          |
| <span data-ttu-id="2ae1f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-118">Attribute-Id</span></span>      | <span data-ttu-id="2ae1f-119">1.2.840.113556.1.4.1379</span><span class="sxs-lookup"><span data-stu-id="2ae1f-119">1.2.840.113556.1.4.1379</span></span>                     |
| <span data-ttu-id="2ae1f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2ae1f-120">System-Id-Guid</span></span>    | <span data-ttu-id="2ae1f-121">94c56394-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2ae1f-121">94c56394-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="2ae1f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ae1f-122">Syntax</span></span>            | [<span data-ttu-id="2ae1f-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2ae1f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2ae1f-124">Implementations</span></span>

-   [<span data-ttu-id="2ae1f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2ae1f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ae1f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ae1f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ae1f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ae1f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2ae1f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ae1f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2ae1f-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-132">Entry</span></span> | <span data-ttu-id="2ae1f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2ae1f-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ae1f-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ae1f-136">System-Only</span></span>            | <span data-ttu-id="2ae1f-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-137">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ae1f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2ae1f-139">True</span><span class="sxs-lookup"><span data-stu-id="2ae1f-139">True</span></span>                                                      |
| <span data-ttu-id="2ae1f-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ae1f-140">Is Indexed</span></span>             | <span data-ttu-id="2ae1f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-141">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ae1f-142">In Global Catalog</span></span>      | <span data-ttu-id="2ae1f-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-143">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ae1f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ae1f-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ae1f-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2ae1f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ae1f-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ae1f-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-148">Search-Flags</span></span>           | <span data-ttu-id="2ae1f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ae1f-149">0x00000000</span></span>                                                |
| <span data-ttu-id="2ae1f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-150">System-Flags</span></span>           | <span data-ttu-id="2ae1f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ae1f-151">0x00000010</span></span>                                                |
| <span data-ttu-id="2ae1f-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ae1f-152">Classes used in</span></span>        | [<span data-ttu-id="2ae1f-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2ae1f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ae1f-154">Windows Server 2003</span></span>



| <span data-ttu-id="2ae1f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-155">Entry</span></span> | <span data-ttu-id="2ae1f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2ae1f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ae1f-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ae1f-159">System-Only</span></span>            | <span data-ttu-id="2ae1f-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-160">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ae1f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2ae1f-162">True</span><span class="sxs-lookup"><span data-stu-id="2ae1f-162">True</span></span>                                                      |
| <span data-ttu-id="2ae1f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ae1f-163">Is Indexed</span></span>             | <span data-ttu-id="2ae1f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-164">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ae1f-165">In Global Catalog</span></span>      | <span data-ttu-id="2ae1f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-166">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ae1f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ae1f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ae1f-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2ae1f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ae1f-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ae1f-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-171">Search-Flags</span></span>           | <span data-ttu-id="2ae1f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ae1f-172">0x00000000</span></span>                                                |
| <span data-ttu-id="2ae1f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-173">System-Flags</span></span>           | <span data-ttu-id="2ae1f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ae1f-174">0x00000010</span></span>                                                |
| <span data-ttu-id="2ae1f-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ae1f-175">Classes used in</span></span>        | [<span data-ttu-id="2ae1f-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ae1f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ae1f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ae1f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-178">Entry</span></span> | <span data-ttu-id="2ae1f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2ae1f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ae1f-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ae1f-182">System-Only</span></span>            | <span data-ttu-id="2ae1f-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-183">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ae1f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2ae1f-185">True</span><span class="sxs-lookup"><span data-stu-id="2ae1f-185">True</span></span>                                                      |
| <span data-ttu-id="2ae1f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ae1f-186">Is Indexed</span></span>             | <span data-ttu-id="2ae1f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-187">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ae1f-188">In Global Catalog</span></span>      | <span data-ttu-id="2ae1f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-189">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ae1f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ae1f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ae1f-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2ae1f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ae1f-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ae1f-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-194">Search-Flags</span></span>           | <span data-ttu-id="2ae1f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ae1f-195">0x00000000</span></span>                                                |
| <span data-ttu-id="2ae1f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-196">System-Flags</span></span>           | <span data-ttu-id="2ae1f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ae1f-197">0x00000010</span></span>                                                |
| <span data-ttu-id="2ae1f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ae1f-198">Classes used in</span></span>        | [<span data-ttu-id="2ae1f-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ae1f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ae1f-200">Windows Server 2008</span></span>



| <span data-ttu-id="2ae1f-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-201">Entry</span></span> | <span data-ttu-id="2ae1f-202">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2ae1f-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ae1f-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ae1f-205">System-Only</span></span>            | <span data-ttu-id="2ae1f-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-206">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ae1f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2ae1f-208">True</span><span class="sxs-lookup"><span data-stu-id="2ae1f-208">True</span></span>                                                      |
| <span data-ttu-id="2ae1f-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ae1f-209">Is Indexed</span></span>             | <span data-ttu-id="2ae1f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-210">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ae1f-211">In Global Catalog</span></span>      | <span data-ttu-id="2ae1f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-212">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ae1f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ae1f-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ae1f-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2ae1f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ae1f-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ae1f-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-217">Search-Flags</span></span>           | <span data-ttu-id="2ae1f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ae1f-218">0x00000000</span></span>                                                |
| <span data-ttu-id="2ae1f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-219">System-Flags</span></span>           | <span data-ttu-id="2ae1f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ae1f-220">0x00000010</span></span>                                                |
| <span data-ttu-id="2ae1f-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ae1f-221">Classes used in</span></span>        | [<span data-ttu-id="2ae1f-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ae1f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ae1f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ae1f-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-224">Entry</span></span> | <span data-ttu-id="2ae1f-225">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2ae1f-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ae1f-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ae1f-228">System-Only</span></span>            | <span data-ttu-id="2ae1f-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-229">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ae1f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2ae1f-231">True</span><span class="sxs-lookup"><span data-stu-id="2ae1f-231">True</span></span>                                                      |
| <span data-ttu-id="2ae1f-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ae1f-232">Is Indexed</span></span>             | <span data-ttu-id="2ae1f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-233">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ae1f-234">In Global Catalog</span></span>      | <span data-ttu-id="2ae1f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-235">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ae1f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ae1f-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ae1f-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2ae1f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ae1f-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ae1f-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-240">Search-Flags</span></span>           | <span data-ttu-id="2ae1f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ae1f-241">0x00000000</span></span>                                                |
| <span data-ttu-id="2ae1f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-242">System-Flags</span></span>           | <span data-ttu-id="2ae1f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ae1f-243">0x00000010</span></span>                                                |
| <span data-ttu-id="2ae1f-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ae1f-244">Classes used in</span></span>        | [<span data-ttu-id="2ae1f-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ae1f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ae1f-246">Windows Server 2012</span></span>



| <span data-ttu-id="2ae1f-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ae1f-247">Entry</span></span> | <span data-ttu-id="2ae1f-248">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae1f-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2ae1f-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ae1f-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ae1f-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2ae1f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ae1f-251">System-Only</span></span>            | <span data-ttu-id="2ae1f-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-252">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ae1f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2ae1f-254">True</span><span class="sxs-lookup"><span data-stu-id="2ae1f-254">True</span></span>                                                      |
| <span data-ttu-id="2ae1f-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ae1f-255">Is Indexed</span></span>             | <span data-ttu-id="2ae1f-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-256">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ae1f-257">In Global Catalog</span></span>      | <span data-ttu-id="2ae1f-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ae1f-258">False</span></span>                                                     |
| <span data-ttu-id="2ae1f-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ae1f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ae1f-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ae1f-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2ae1f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ae1f-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ae1f-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2ae1f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-263">Search-Flags</span></span>           | <span data-ttu-id="2ae1f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ae1f-264">0x00000000</span></span>                                                |
| <span data-ttu-id="2ae1f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ae1f-265">System-Flags</span></span>           | <span data-ttu-id="2ae1f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ae1f-266">0x00000010</span></span>                                                |
| <span data-ttu-id="2ae1f-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ae1f-267">Classes used in</span></span>        | [<span data-ttu-id="2ae1f-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2ae1f-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





