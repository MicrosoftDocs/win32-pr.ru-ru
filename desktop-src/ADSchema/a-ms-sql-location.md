---
title: MS-SQL-атрибут Location
description: Определяемая пользователем строка. Значение по умолчанию — Location.
ms.assetid: e0d8a83f-a979-49a8-a92d-842c18c8f9fd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Location в MS-SQL
- Схема AD атрибута Location в mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ffa71a40e7deff12385e0e45eb16d8dcc998269
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654904"
---
# <a name="ms-sql-location-attribute"></a><span data-ttu-id="73bff-106">MS-SQL-атрибут Location</span><span class="sxs-lookup"><span data-stu-id="73bff-106">MS-SQL-Location attribute</span></span>

<span data-ttu-id="73bff-107">Определяемая пользователем строка.</span><span class="sxs-lookup"><span data-stu-id="73bff-107">A user defined string.</span></span> <span data-ttu-id="73bff-108">Значение по умолчанию — Location.</span><span class="sxs-lookup"><span data-stu-id="73bff-108">Default is set to Location.</span></span>



| <span data-ttu-id="73bff-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-109">Entry</span></span> | <span data-ttu-id="73bff-110">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="73bff-111">CN</span><span class="sxs-lookup"><span data-stu-id="73bff-111">CN</span></span>                | <span data-ttu-id="73bff-112">MS-SQL — расположение</span><span class="sxs-lookup"><span data-stu-id="73bff-112">MS-SQL-Location</span></span>                             |
| <span data-ttu-id="73bff-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="73bff-113">Ldap-Display-Name</span></span> | <span data-ttu-id="73bff-114">mS-SQL — расположение</span><span class="sxs-lookup"><span data-stu-id="73bff-114">mS-SQL-Location</span></span>                             |
| <span data-ttu-id="73bff-115">Размер</span><span class="sxs-lookup"><span data-stu-id="73bff-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="73bff-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="73bff-116">Update Privilege</span></span>  | <span data-ttu-id="73bff-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="73bff-117">Domain administrator</span></span>                        |
| <span data-ttu-id="73bff-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="73bff-118">Update Frequency</span></span>  | <span data-ttu-id="73bff-119">При установке системы.</span><span class="sxs-lookup"><span data-stu-id="73bff-119">At system setup.</span></span>                            |
| <span data-ttu-id="73bff-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-120">Attribute-Id</span></span>      | <span data-ttu-id="73bff-121">1.2.840.113556.1.4.1366</span><span class="sxs-lookup"><span data-stu-id="73bff-121">1.2.840.113556.1.4.1366</span></span>                     |
| <span data-ttu-id="73bff-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="73bff-122">System-Id-Guid</span></span>    | <span data-ttu-id="73bff-123">561c9644-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="73bff-123">561c9644-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="73bff-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73bff-124">Syntax</span></span>            | [<span data-ttu-id="73bff-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="73bff-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="73bff-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="73bff-126">Implementations</span></span>

-   [<span data-ttu-id="73bff-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="73bff-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="73bff-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="73bff-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="73bff-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="73bff-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="73bff-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="73bff-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="73bff-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="73bff-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="73bff-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="73bff-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="73bff-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="73bff-133">Windows 2000 Server</span></span>



| <span data-ttu-id="73bff-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-134">Entry</span></span> | <span data-ttu-id="73bff-135">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73bff-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="73bff-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="73bff-138">System-Only</span></span>            | <span data-ttu-id="73bff-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-139">False</span></span>                                                     |
| <span data-ttu-id="73bff-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="73bff-140">Is-Single-Valued</span></span>       | <span data-ttu-id="73bff-141">True</span><span class="sxs-lookup"><span data-stu-id="73bff-141">True</span></span>                                                      |
| <span data-ttu-id="73bff-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="73bff-142">Is Indexed</span></span>             | <span data-ttu-id="73bff-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-143">False</span></span>                                                     |
| <span data-ttu-id="73bff-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="73bff-144">In Global Catalog</span></span>      | <span data-ttu-id="73bff-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-145">False</span></span>                                                     |
| <span data-ttu-id="73bff-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="73bff-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="73bff-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73bff-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="73bff-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73bff-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73bff-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-150">Search-Flags</span></span>           | <span data-ttu-id="73bff-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73bff-151">0x00000000</span></span>                                                |
| <span data-ttu-id="73bff-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-152">System-Flags</span></span>           | <span data-ttu-id="73bff-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73bff-153">0x00000010</span></span>                                                |
| <span data-ttu-id="73bff-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="73bff-154">Classes used in</span></span>        | [<span data-ttu-id="73bff-155">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="73bff-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="73bff-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="73bff-156">Windows Server 2003</span></span>



| <span data-ttu-id="73bff-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-157">Entry</span></span> | <span data-ttu-id="73bff-158">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73bff-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="73bff-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="73bff-161">System-Only</span></span>            | <span data-ttu-id="73bff-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-162">False</span></span>                                                     |
| <span data-ttu-id="73bff-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="73bff-163">Is-Single-Valued</span></span>       | <span data-ttu-id="73bff-164">True</span><span class="sxs-lookup"><span data-stu-id="73bff-164">True</span></span>                                                      |
| <span data-ttu-id="73bff-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="73bff-165">Is Indexed</span></span>             | <span data-ttu-id="73bff-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-166">False</span></span>                                                     |
| <span data-ttu-id="73bff-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="73bff-167">In Global Catalog</span></span>      | <span data-ttu-id="73bff-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-168">False</span></span>                                                     |
| <span data-ttu-id="73bff-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="73bff-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="73bff-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73bff-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="73bff-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73bff-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73bff-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-173">Search-Flags</span></span>           | <span data-ttu-id="73bff-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73bff-174">0x00000000</span></span>                                                |
| <span data-ttu-id="73bff-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-175">System-Flags</span></span>           | <span data-ttu-id="73bff-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73bff-176">0x00000010</span></span>                                                |
| <span data-ttu-id="73bff-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="73bff-177">Classes used in</span></span>        | [<span data-ttu-id="73bff-178">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="73bff-178">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="73bff-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="73bff-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="73bff-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-180">Entry</span></span> | <span data-ttu-id="73bff-181">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73bff-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="73bff-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="73bff-184">System-Only</span></span>            | <span data-ttu-id="73bff-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-185">False</span></span>                                                     |
| <span data-ttu-id="73bff-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="73bff-186">Is-Single-Valued</span></span>       | <span data-ttu-id="73bff-187">True</span><span class="sxs-lookup"><span data-stu-id="73bff-187">True</span></span>                                                      |
| <span data-ttu-id="73bff-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="73bff-188">Is Indexed</span></span>             | <span data-ttu-id="73bff-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-189">False</span></span>                                                     |
| <span data-ttu-id="73bff-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="73bff-190">In Global Catalog</span></span>      | <span data-ttu-id="73bff-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-191">False</span></span>                                                     |
| <span data-ttu-id="73bff-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="73bff-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="73bff-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73bff-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="73bff-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73bff-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73bff-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-196">Search-Flags</span></span>           | <span data-ttu-id="73bff-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73bff-197">0x00000000</span></span>                                                |
| <span data-ttu-id="73bff-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-198">System-Flags</span></span>           | <span data-ttu-id="73bff-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73bff-199">0x00000010</span></span>                                                |
| <span data-ttu-id="73bff-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="73bff-200">Classes used in</span></span>        | [<span data-ttu-id="73bff-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="73bff-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="73bff-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73bff-202">Windows Server 2008</span></span>



| <span data-ttu-id="73bff-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-203">Entry</span></span> | <span data-ttu-id="73bff-204">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73bff-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="73bff-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="73bff-207">System-Only</span></span>            | <span data-ttu-id="73bff-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-208">False</span></span>                                                     |
| <span data-ttu-id="73bff-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="73bff-209">Is-Single-Valued</span></span>       | <span data-ttu-id="73bff-210">True</span><span class="sxs-lookup"><span data-stu-id="73bff-210">True</span></span>                                                      |
| <span data-ttu-id="73bff-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="73bff-211">Is Indexed</span></span>             | <span data-ttu-id="73bff-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-212">False</span></span>                                                     |
| <span data-ttu-id="73bff-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="73bff-213">In Global Catalog</span></span>      | <span data-ttu-id="73bff-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-214">False</span></span>                                                     |
| <span data-ttu-id="73bff-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="73bff-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="73bff-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73bff-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="73bff-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73bff-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73bff-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-219">Search-Flags</span></span>           | <span data-ttu-id="73bff-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73bff-220">0x00000000</span></span>                                                |
| <span data-ttu-id="73bff-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-221">System-Flags</span></span>           | <span data-ttu-id="73bff-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73bff-222">0x00000010</span></span>                                                |
| <span data-ttu-id="73bff-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="73bff-223">Classes used in</span></span>        | [<span data-ttu-id="73bff-224">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="73bff-224">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="73bff-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73bff-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="73bff-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-226">Entry</span></span> | <span data-ttu-id="73bff-227">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73bff-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="73bff-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="73bff-230">System-Only</span></span>            | <span data-ttu-id="73bff-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-231">False</span></span>                                                     |
| <span data-ttu-id="73bff-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="73bff-232">Is-Single-Valued</span></span>       | <span data-ttu-id="73bff-233">True</span><span class="sxs-lookup"><span data-stu-id="73bff-233">True</span></span>                                                      |
| <span data-ttu-id="73bff-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="73bff-234">Is Indexed</span></span>             | <span data-ttu-id="73bff-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-235">False</span></span>                                                     |
| <span data-ttu-id="73bff-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="73bff-236">In Global Catalog</span></span>      | <span data-ttu-id="73bff-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-237">False</span></span>                                                     |
| <span data-ttu-id="73bff-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="73bff-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="73bff-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73bff-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="73bff-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73bff-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73bff-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-242">Search-Flags</span></span>           | <span data-ttu-id="73bff-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73bff-243">0x00000000</span></span>                                                |
| <span data-ttu-id="73bff-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-244">System-Flags</span></span>           | <span data-ttu-id="73bff-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73bff-245">0x00000010</span></span>                                                |
| <span data-ttu-id="73bff-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="73bff-246">Classes used in</span></span>        | [<span data-ttu-id="73bff-247">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="73bff-247">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="73bff-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73bff-248">Windows Server 2012</span></span>



| <span data-ttu-id="73bff-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="73bff-249">Entry</span></span> | <span data-ttu-id="73bff-250">Значение</span><span class="sxs-lookup"><span data-stu-id="73bff-250">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73bff-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="73bff-251">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73bff-252">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="73bff-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="73bff-253">System-Only</span></span>            | <span data-ttu-id="73bff-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-254">False</span></span>                                                     |
| <span data-ttu-id="73bff-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="73bff-255">Is-Single-Valued</span></span>       | <span data-ttu-id="73bff-256">True</span><span class="sxs-lookup"><span data-stu-id="73bff-256">True</span></span>                                                      |
| <span data-ttu-id="73bff-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="73bff-257">Is Indexed</span></span>             | <span data-ttu-id="73bff-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-258">False</span></span>                                                     |
| <span data-ttu-id="73bff-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="73bff-259">In Global Catalog</span></span>      | <span data-ttu-id="73bff-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="73bff-260">False</span></span>                                                     |
| <span data-ttu-id="73bff-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="73bff-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="73bff-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73bff-262">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="73bff-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73bff-263">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73bff-264">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="73bff-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-265">Search-Flags</span></span>           | <span data-ttu-id="73bff-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73bff-266">0x00000000</span></span>                                                |
| <span data-ttu-id="73bff-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73bff-267">System-Flags</span></span>           | <span data-ttu-id="73bff-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73bff-268">0x00000010</span></span>                                                |
| <span data-ttu-id="73bff-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="73bff-269">Classes used in</span></span>        | [<span data-ttu-id="73bff-270">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="73bff-270">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





