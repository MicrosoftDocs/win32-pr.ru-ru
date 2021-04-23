---
title: MS-SQL — атрибут языка
description: Язык текущего экземпляра SQL Server.
ms.assetid: 70ab1e8f-aff0-4a1e-ab2c-676a77b0c229
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута языка MS-SQL
- Схема AD атрибута языка mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Language
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fd9a4fb6ede4e656b7cebbfe7c5c920e19d9123
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138226"
---
# <a name="ms-sql-language-attribute"></a><span data-ttu-id="d27ac-105">MS-SQL — атрибут языка</span><span class="sxs-lookup"><span data-stu-id="d27ac-105">MS-SQL-Language attribute</span></span>

<span data-ttu-id="d27ac-106">Язык текущего экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d27ac-106">The language for the current instance of SQL Server.</span></span>



| <span data-ttu-id="d27ac-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-107">Entry</span></span> | <span data-ttu-id="d27ac-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d27ac-109">CN</span><span class="sxs-lookup"><span data-stu-id="d27ac-109">CN</span></span>                | <span data-ttu-id="d27ac-110">Язык MS-SQL-Language</span><span class="sxs-lookup"><span data-stu-id="d27ac-110">MS-SQL-Language</span></span>                             |
| <span data-ttu-id="d27ac-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d27ac-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d27ac-112">Язык mS-SQL-Language</span><span class="sxs-lookup"><span data-stu-id="d27ac-112">mS-SQL-Language</span></span>                             |
| <span data-ttu-id="d27ac-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d27ac-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d27ac-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d27ac-114">Update Privilege</span></span>  | <span data-ttu-id="d27ac-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="d27ac-115">Domain administrator</span></span>                        |
| <span data-ttu-id="d27ac-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d27ac-116">Update Frequency</span></span>  | <span data-ttu-id="d27ac-117">При установке системы.</span><span class="sxs-lookup"><span data-stu-id="d27ac-117">At system setup.</span></span>                            |
| <span data-ttu-id="d27ac-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-118">Attribute-Id</span></span>      | <span data-ttu-id="d27ac-119">1.2.840.113556.1.4.1389</span><span class="sxs-lookup"><span data-stu-id="d27ac-119">1.2.840.113556.1.4.1389</span></span>                     |
| <span data-ttu-id="d27ac-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d27ac-120">System-Id-Guid</span></span>    | <span data-ttu-id="d27ac-121">c57f72f4-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d27ac-121">c57f72f4-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="d27ac-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d27ac-122">Syntax</span></span>            | [<span data-ttu-id="d27ac-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d27ac-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d27ac-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d27ac-124">Implementations</span></span>

-   [<span data-ttu-id="d27ac-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d27ac-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d27ac-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d27ac-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d27ac-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d27ac-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d27ac-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d27ac-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d27ac-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d27ac-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d27ac-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d27ac-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d27ac-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d27ac-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d27ac-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-132">Entry</span></span> | <span data-ttu-id="d27ac-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d27ac-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d27ac-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27ac-136">System-Only</span></span>            | <span data-ttu-id="d27ac-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-137">False</span></span>                                                       |
| <span data-ttu-id="d27ac-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d27ac-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d27ac-139">True</span><span class="sxs-lookup"><span data-stu-id="d27ac-139">True</span></span>                                                        |
| <span data-ttu-id="d27ac-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d27ac-140">Is Indexed</span></span>             | <span data-ttu-id="d27ac-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-141">False</span></span>                                                       |
| <span data-ttu-id="d27ac-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d27ac-142">In Global Catalog</span></span>      | <span data-ttu-id="d27ac-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-143">False</span></span>                                                       |
| <span data-ttu-id="d27ac-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d27ac-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27ac-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d27ac-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d27ac-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27ac-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27ac-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-148">Search-Flags</span></span>           | <span data-ttu-id="d27ac-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27ac-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="d27ac-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-150">System-Flags</span></span>           | <span data-ttu-id="d27ac-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27ac-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="d27ac-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d27ac-152">Classes used in</span></span>        | [<span data-ttu-id="d27ac-153">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="d27ac-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d27ac-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d27ac-154">Windows Server 2003</span></span>



| <span data-ttu-id="d27ac-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-155">Entry</span></span> | <span data-ttu-id="d27ac-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d27ac-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d27ac-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27ac-159">System-Only</span></span>            | <span data-ttu-id="d27ac-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-160">False</span></span>                                                       |
| <span data-ttu-id="d27ac-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d27ac-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d27ac-162">True</span><span class="sxs-lookup"><span data-stu-id="d27ac-162">True</span></span>                                                        |
| <span data-ttu-id="d27ac-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d27ac-163">Is Indexed</span></span>             | <span data-ttu-id="d27ac-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-164">False</span></span>                                                       |
| <span data-ttu-id="d27ac-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d27ac-165">In Global Catalog</span></span>      | <span data-ttu-id="d27ac-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-166">False</span></span>                                                       |
| <span data-ttu-id="d27ac-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d27ac-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27ac-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d27ac-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d27ac-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27ac-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27ac-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-171">Search-Flags</span></span>           | <span data-ttu-id="d27ac-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27ac-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="d27ac-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-173">System-Flags</span></span>           | <span data-ttu-id="d27ac-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27ac-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="d27ac-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d27ac-175">Classes used in</span></span>        | [<span data-ttu-id="d27ac-176">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="d27ac-176">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d27ac-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d27ac-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d27ac-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-178">Entry</span></span> | <span data-ttu-id="d27ac-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d27ac-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d27ac-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27ac-182">System-Only</span></span>            | <span data-ttu-id="d27ac-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-183">False</span></span>                                                       |
| <span data-ttu-id="d27ac-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d27ac-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d27ac-185">True</span><span class="sxs-lookup"><span data-stu-id="d27ac-185">True</span></span>                                                        |
| <span data-ttu-id="d27ac-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d27ac-186">Is Indexed</span></span>             | <span data-ttu-id="d27ac-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-187">False</span></span>                                                       |
| <span data-ttu-id="d27ac-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d27ac-188">In Global Catalog</span></span>      | <span data-ttu-id="d27ac-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-189">False</span></span>                                                       |
| <span data-ttu-id="d27ac-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d27ac-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27ac-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d27ac-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d27ac-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27ac-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27ac-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-194">Search-Flags</span></span>           | <span data-ttu-id="d27ac-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27ac-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="d27ac-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-196">System-Flags</span></span>           | <span data-ttu-id="d27ac-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27ac-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="d27ac-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d27ac-198">Classes used in</span></span>        | [<span data-ttu-id="d27ac-199">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="d27ac-199">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d27ac-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d27ac-200">Windows Server 2008</span></span>



| <span data-ttu-id="d27ac-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-201">Entry</span></span> | <span data-ttu-id="d27ac-202">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d27ac-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d27ac-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27ac-205">System-Only</span></span>            | <span data-ttu-id="d27ac-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-206">False</span></span>                                                       |
| <span data-ttu-id="d27ac-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d27ac-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d27ac-208">True</span><span class="sxs-lookup"><span data-stu-id="d27ac-208">True</span></span>                                                        |
| <span data-ttu-id="d27ac-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d27ac-209">Is Indexed</span></span>             | <span data-ttu-id="d27ac-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-210">False</span></span>                                                       |
| <span data-ttu-id="d27ac-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d27ac-211">In Global Catalog</span></span>      | <span data-ttu-id="d27ac-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-212">False</span></span>                                                       |
| <span data-ttu-id="d27ac-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d27ac-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27ac-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d27ac-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d27ac-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27ac-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27ac-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-217">Search-Flags</span></span>           | <span data-ttu-id="d27ac-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27ac-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="d27ac-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-219">System-Flags</span></span>           | <span data-ttu-id="d27ac-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27ac-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="d27ac-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d27ac-221">Classes used in</span></span>        | [<span data-ttu-id="d27ac-222">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="d27ac-222">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d27ac-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d27ac-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d27ac-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-224">Entry</span></span> | <span data-ttu-id="d27ac-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d27ac-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d27ac-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27ac-228">System-Only</span></span>            | <span data-ttu-id="d27ac-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-229">False</span></span>                                                       |
| <span data-ttu-id="d27ac-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d27ac-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d27ac-231">True</span><span class="sxs-lookup"><span data-stu-id="d27ac-231">True</span></span>                                                        |
| <span data-ttu-id="d27ac-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d27ac-232">Is Indexed</span></span>             | <span data-ttu-id="d27ac-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-233">False</span></span>                                                       |
| <span data-ttu-id="d27ac-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d27ac-234">In Global Catalog</span></span>      | <span data-ttu-id="d27ac-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-235">False</span></span>                                                       |
| <span data-ttu-id="d27ac-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d27ac-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27ac-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d27ac-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d27ac-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27ac-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27ac-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-240">Search-Flags</span></span>           | <span data-ttu-id="d27ac-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27ac-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="d27ac-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-242">System-Flags</span></span>           | <span data-ttu-id="d27ac-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27ac-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="d27ac-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d27ac-244">Classes used in</span></span>        | [<span data-ttu-id="d27ac-245">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="d27ac-245">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d27ac-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d27ac-246">Windows Server 2012</span></span>



| <span data-ttu-id="d27ac-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="d27ac-247">Entry</span></span> | <span data-ttu-id="d27ac-248">Значение</span><span class="sxs-lookup"><span data-stu-id="d27ac-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d27ac-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d27ac-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27ac-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d27ac-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27ac-251">System-Only</span></span>            | <span data-ttu-id="d27ac-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-252">False</span></span>                                                       |
| <span data-ttu-id="d27ac-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d27ac-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d27ac-254">True</span><span class="sxs-lookup"><span data-stu-id="d27ac-254">True</span></span>                                                        |
| <span data-ttu-id="d27ac-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d27ac-255">Is Indexed</span></span>             | <span data-ttu-id="d27ac-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-256">False</span></span>                                                       |
| <span data-ttu-id="d27ac-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d27ac-257">In Global Catalog</span></span>      | <span data-ttu-id="d27ac-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="d27ac-258">False</span></span>                                                       |
| <span data-ttu-id="d27ac-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d27ac-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27ac-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d27ac-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d27ac-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27ac-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27ac-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d27ac-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-263">Search-Flags</span></span>           | <span data-ttu-id="d27ac-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27ac-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="d27ac-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27ac-265">System-Flags</span></span>           | <span data-ttu-id="d27ac-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27ac-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="d27ac-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d27ac-267">Classes used in</span></span>        | [<span data-ttu-id="d27ac-268">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="d27ac-268">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





