---
title: MS-SQL-псевдоним атрибута
description: Псевдоним, используемый для подключения к базе данных. Значение по умолчанию — Alias.
ms.assetid: d129813c-9871-4ed5-968a-b05ab2b96f10
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута псевдонима MS-SQL
- Схема AD атрибута псевдонима mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Alias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31d32697534a2a01358dc9cb724760588687f6f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804397"
---
# <a name="ms-sql-alias-attribute"></a><span data-ttu-id="31807-106">MS-SQL-псевдоним атрибута</span><span class="sxs-lookup"><span data-stu-id="31807-106">MS-SQL-Alias attribute</span></span>

<span data-ttu-id="31807-107">Псевдоним, используемый для подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="31807-107">An alias used to connect to the database.</span></span> <span data-ttu-id="31807-108">Значение по умолчанию — Alias.</span><span class="sxs-lookup"><span data-stu-id="31807-108">Default is set to Alias.</span></span>



| <span data-ttu-id="31807-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-109">Entry</span></span> | <span data-ttu-id="31807-110">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="31807-111">CN</span><span class="sxs-lookup"><span data-stu-id="31807-111">CN</span></span>                | <span data-ttu-id="31807-112">Псевдоним MS-SQL</span><span class="sxs-lookup"><span data-stu-id="31807-112">MS-SQL-Alias</span></span>                                |
| <span data-ttu-id="31807-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="31807-113">Ldap-Display-Name</span></span> | <span data-ttu-id="31807-114">Псевдоним mS-SQL</span><span class="sxs-lookup"><span data-stu-id="31807-114">mS-SQL-Alias</span></span>                                |
| <span data-ttu-id="31807-115">Размер</span><span class="sxs-lookup"><span data-stu-id="31807-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="31807-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="31807-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="31807-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="31807-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="31807-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="31807-118">Attribute-Id</span></span>      | <span data-ttu-id="31807-119">1.2.840.113556.1.4.1395</span><span class="sxs-lookup"><span data-stu-id="31807-119">1.2.840.113556.1.4.1395</span></span>                     |
| <span data-ttu-id="31807-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="31807-120">System-Id-Guid</span></span>    | <span data-ttu-id="31807-121">e0c6baae-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="31807-121">e0c6baae-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="31807-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31807-122">Syntax</span></span>            | [<span data-ttu-id="31807-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="31807-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="31807-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="31807-124">Implementations</span></span>

-   [<span data-ttu-id="31807-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="31807-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="31807-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="31807-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="31807-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="31807-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="31807-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="31807-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="31807-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="31807-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="31807-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="31807-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="31807-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31807-131">Windows 2000 Server</span></span>



| <span data-ttu-id="31807-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-132">Entry</span></span> | <span data-ttu-id="31807-133">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31807-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31807-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31807-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="31807-136">System-Only</span></span>            | <span data-ttu-id="31807-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="31807-137">False</span></span>                                                         |
| <span data-ttu-id="31807-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31807-138">Is-Single-Valued</span></span>       | <span data-ttu-id="31807-139">True</span><span class="sxs-lookup"><span data-stu-id="31807-139">True</span></span>                                                          |
| <span data-ttu-id="31807-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31807-140">Is Indexed</span></span>             | <span data-ttu-id="31807-141">True</span><span class="sxs-lookup"><span data-stu-id="31807-141">True</span></span>                                                          |
| <span data-ttu-id="31807-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31807-142">In Global Catalog</span></span>      | <span data-ttu-id="31807-143">True</span><span class="sxs-lookup"><span data-stu-id="31807-143">True</span></span>                                                          |
| <span data-ttu-id="31807-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31807-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="31807-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31807-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="31807-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31807-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="31807-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31807-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="31807-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-148">Search-Flags</span></span>           | <span data-ttu-id="31807-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31807-149">0x00000001</span></span>                                                    |
| <span data-ttu-id="31807-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-150">System-Flags</span></span>           | <span data-ttu-id="31807-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31807-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="31807-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31807-152">Classes used in</span></span>        | [<span data-ttu-id="31807-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="31807-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="31807-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31807-154">Windows Server 2003</span></span>



| <span data-ttu-id="31807-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-155">Entry</span></span> | <span data-ttu-id="31807-156">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31807-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31807-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31807-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="31807-159">System-Only</span></span>            | <span data-ttu-id="31807-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="31807-160">False</span></span>                                                         |
| <span data-ttu-id="31807-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31807-161">Is-Single-Valued</span></span>       | <span data-ttu-id="31807-162">True</span><span class="sxs-lookup"><span data-stu-id="31807-162">True</span></span>                                                          |
| <span data-ttu-id="31807-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31807-163">Is Indexed</span></span>             | <span data-ttu-id="31807-164">True</span><span class="sxs-lookup"><span data-stu-id="31807-164">True</span></span>                                                          |
| <span data-ttu-id="31807-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31807-165">In Global Catalog</span></span>      | <span data-ttu-id="31807-166">True</span><span class="sxs-lookup"><span data-stu-id="31807-166">True</span></span>                                                          |
| <span data-ttu-id="31807-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31807-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="31807-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31807-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="31807-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31807-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="31807-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31807-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="31807-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-171">Search-Flags</span></span>           | <span data-ttu-id="31807-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31807-172">0x00000001</span></span>                                                    |
| <span data-ttu-id="31807-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-173">System-Flags</span></span>           | <span data-ttu-id="31807-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31807-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="31807-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31807-175">Classes used in</span></span>        | [<span data-ttu-id="31807-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="31807-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="31807-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="31807-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="31807-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-178">Entry</span></span> | <span data-ttu-id="31807-179">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31807-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31807-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31807-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="31807-182">System-Only</span></span>            | <span data-ttu-id="31807-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="31807-183">False</span></span>                                                         |
| <span data-ttu-id="31807-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31807-184">Is-Single-Valued</span></span>       | <span data-ttu-id="31807-185">True</span><span class="sxs-lookup"><span data-stu-id="31807-185">True</span></span>                                                          |
| <span data-ttu-id="31807-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31807-186">Is Indexed</span></span>             | <span data-ttu-id="31807-187">True</span><span class="sxs-lookup"><span data-stu-id="31807-187">True</span></span>                                                          |
| <span data-ttu-id="31807-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31807-188">In Global Catalog</span></span>      | <span data-ttu-id="31807-189">True</span><span class="sxs-lookup"><span data-stu-id="31807-189">True</span></span>                                                          |
| <span data-ttu-id="31807-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31807-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="31807-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31807-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="31807-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31807-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="31807-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31807-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="31807-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-194">Search-Flags</span></span>           | <span data-ttu-id="31807-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31807-195">0x00000001</span></span>                                                    |
| <span data-ttu-id="31807-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-196">System-Flags</span></span>           | <span data-ttu-id="31807-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31807-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="31807-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31807-198">Classes used in</span></span>        | [<span data-ttu-id="31807-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="31807-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="31807-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31807-200">Windows Server 2008</span></span>



| <span data-ttu-id="31807-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-201">Entry</span></span> | <span data-ttu-id="31807-202">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31807-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31807-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31807-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="31807-205">System-Only</span></span>            | <span data-ttu-id="31807-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="31807-206">False</span></span>                                                         |
| <span data-ttu-id="31807-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31807-207">Is-Single-Valued</span></span>       | <span data-ttu-id="31807-208">True</span><span class="sxs-lookup"><span data-stu-id="31807-208">True</span></span>                                                          |
| <span data-ttu-id="31807-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31807-209">Is Indexed</span></span>             | <span data-ttu-id="31807-210">True</span><span class="sxs-lookup"><span data-stu-id="31807-210">True</span></span>                                                          |
| <span data-ttu-id="31807-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31807-211">In Global Catalog</span></span>      | <span data-ttu-id="31807-212">True</span><span class="sxs-lookup"><span data-stu-id="31807-212">True</span></span>                                                          |
| <span data-ttu-id="31807-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31807-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="31807-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31807-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="31807-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31807-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="31807-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31807-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="31807-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-217">Search-Flags</span></span>           | <span data-ttu-id="31807-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31807-218">0x00000001</span></span>                                                    |
| <span data-ttu-id="31807-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-219">System-Flags</span></span>           | <span data-ttu-id="31807-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31807-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="31807-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31807-221">Classes used in</span></span>        | [<span data-ttu-id="31807-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="31807-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="31807-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31807-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="31807-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-224">Entry</span></span> | <span data-ttu-id="31807-225">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31807-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31807-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31807-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="31807-228">System-Only</span></span>            | <span data-ttu-id="31807-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="31807-229">False</span></span>                                                         |
| <span data-ttu-id="31807-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31807-230">Is-Single-Valued</span></span>       | <span data-ttu-id="31807-231">True</span><span class="sxs-lookup"><span data-stu-id="31807-231">True</span></span>                                                          |
| <span data-ttu-id="31807-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31807-232">Is Indexed</span></span>             | <span data-ttu-id="31807-233">True</span><span class="sxs-lookup"><span data-stu-id="31807-233">True</span></span>                                                          |
| <span data-ttu-id="31807-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31807-234">In Global Catalog</span></span>      | <span data-ttu-id="31807-235">True</span><span class="sxs-lookup"><span data-stu-id="31807-235">True</span></span>                                                          |
| <span data-ttu-id="31807-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31807-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="31807-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31807-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="31807-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31807-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="31807-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31807-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="31807-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-240">Search-Flags</span></span>           | <span data-ttu-id="31807-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31807-241">0x00000001</span></span>                                                    |
| <span data-ttu-id="31807-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-242">System-Flags</span></span>           | <span data-ttu-id="31807-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31807-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="31807-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31807-244">Classes used in</span></span>        | [<span data-ttu-id="31807-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="31807-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="31807-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="31807-246">Windows Server 2012</span></span>



| <span data-ttu-id="31807-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="31807-247">Entry</span></span> | <span data-ttu-id="31807-248">Значение</span><span class="sxs-lookup"><span data-stu-id="31807-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31807-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="31807-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31807-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="31807-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="31807-251">System-Only</span></span>            | <span data-ttu-id="31807-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="31807-252">False</span></span>                                                         |
| <span data-ttu-id="31807-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="31807-253">Is-Single-Valued</span></span>       | <span data-ttu-id="31807-254">True</span><span class="sxs-lookup"><span data-stu-id="31807-254">True</span></span>                                                          |
| <span data-ttu-id="31807-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="31807-255">Is Indexed</span></span>             | <span data-ttu-id="31807-256">True</span><span class="sxs-lookup"><span data-stu-id="31807-256">True</span></span>                                                          |
| <span data-ttu-id="31807-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="31807-257">In Global Catalog</span></span>      | <span data-ttu-id="31807-258">True</span><span class="sxs-lookup"><span data-stu-id="31807-258">True</span></span>                                                          |
| <span data-ttu-id="31807-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="31807-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="31807-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="31807-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="31807-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31807-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="31807-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31807-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="31807-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-263">Search-Flags</span></span>           | <span data-ttu-id="31807-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31807-264">0x00000001</span></span>                                                    |
| <span data-ttu-id="31807-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31807-265">System-Flags</span></span>           | <span data-ttu-id="31807-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31807-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="31807-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="31807-267">Classes used in</span></span>        | [<span data-ttu-id="31807-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="31807-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





