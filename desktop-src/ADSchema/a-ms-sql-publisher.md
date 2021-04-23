---
title: Атрибут MS-SQL-Publisher
description: Имя базы данных издателя для репликации.
ms.assetid: f5efb16d-ea0a-4015-aa6f-de7bf7401eb4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Publisher
- Схема AD атрибута mS-SQL-Publisher
topic_type:
- apiref
api_name:
- MS-SQL-Publisher
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12a9833918e540877bf58978c5c314165d60044
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804379"
---
# <a name="ms-sql-publisher-attribute"></a><span data-ttu-id="8e9a4-105">Атрибут MS-SQL-Publisher</span><span class="sxs-lookup"><span data-stu-id="8e9a4-105">MS-SQL-Publisher attribute</span></span>

<span data-ttu-id="8e9a4-106">Имя базы данных издателя для репликации.</span><span class="sxs-lookup"><span data-stu-id="8e9a4-106">The name of the publisher database for replication.</span></span>



| <span data-ttu-id="8e9a4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-107">Entry</span></span> | <span data-ttu-id="8e9a4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8e9a4-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e9a4-109">CN</span></span>                | <span data-ttu-id="8e9a4-110">Издатель MS-SQL-Publisher</span><span class="sxs-lookup"><span data-stu-id="8e9a4-110">MS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="8e9a4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8e9a4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8e9a4-112">Издатель mS-SQL-Publisher</span><span class="sxs-lookup"><span data-stu-id="8e9a4-112">mS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="8e9a4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8e9a4-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8e9a4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8e9a4-114">Update Privilege</span></span>  | <span data-ttu-id="8e9a4-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="8e9a4-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8e9a4-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8e9a4-116">Update Frequency</span></span>  | <span data-ttu-id="8e9a4-117">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="8e9a4-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="8e9a4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-118">Attribute-Id</span></span>      | <span data-ttu-id="8e9a4-119">1.2.840.113556.1.4.1402</span><span class="sxs-lookup"><span data-stu-id="8e9a4-119">1.2.840.113556.1.4.1402</span></span>                     |
| <span data-ttu-id="8e9a4-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8e9a4-120">System-Id-Guid</span></span>    | <span data-ttu-id="8e9a4-121">c1676858-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="8e9a4-121">c1676858-d34b-11d2-999a-0000f87a57d4</span></span>        |
| <span data-ttu-id="8e9a4-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e9a4-122">Syntax</span></span>            | [<span data-ttu-id="8e9a4-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8e9a4-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8e9a4-124">Implementations</span></span>

-   [<span data-ttu-id="8e9a4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8e9a4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e9a4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e9a4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e9a4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e9a4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8e9a4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e9a4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8e9a4-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-132">Entry</span></span> | <span data-ttu-id="8e9a4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e9a4-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e9a4-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e9a4-136">System-Only</span></span>            | <span data-ttu-id="8e9a4-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-137">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e9a4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8e9a4-139">True</span><span class="sxs-lookup"><span data-stu-id="8e9a4-139">True</span></span>                                                                |
| <span data-ttu-id="8e9a4-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e9a4-140">Is Indexed</span></span>             | <span data-ttu-id="8e9a4-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-141">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e9a4-142">In Global Catalog</span></span>      | <span data-ttu-id="8e9a4-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-143">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e9a4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e9a4-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e9a4-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8e9a4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e9a4-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e9a4-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-148">Search-Flags</span></span>           | <span data-ttu-id="8e9a4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e9a4-149">0x00000000</span></span>                                                          |
| <span data-ttu-id="8e9a4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-150">System-Flags</span></span>           | <span data-ttu-id="8e9a4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e9a4-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="8e9a4-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e9a4-152">Classes used in</span></span>        | [<span data-ttu-id="8e9a4-153">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8e9a4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e9a4-154">Windows Server 2003</span></span>



| <span data-ttu-id="8e9a4-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-155">Entry</span></span> | <span data-ttu-id="8e9a4-156">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e9a4-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e9a4-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e9a4-159">System-Only</span></span>            | <span data-ttu-id="8e9a4-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-160">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e9a4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8e9a4-162">True</span><span class="sxs-lookup"><span data-stu-id="8e9a4-162">True</span></span>                                                                |
| <span data-ttu-id="8e9a4-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e9a4-163">Is Indexed</span></span>             | <span data-ttu-id="8e9a4-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-164">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e9a4-165">In Global Catalog</span></span>      | <span data-ttu-id="8e9a4-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-166">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e9a4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e9a4-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e9a4-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8e9a4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e9a4-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e9a4-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-171">Search-Flags</span></span>           | <span data-ttu-id="8e9a4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e9a4-172">0x00000000</span></span>                                                          |
| <span data-ttu-id="8e9a4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-173">System-Flags</span></span>           | <span data-ttu-id="8e9a4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e9a4-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="8e9a4-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e9a4-175">Classes used in</span></span>        | [<span data-ttu-id="8e9a4-176">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e9a4-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e9a4-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e9a4-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-178">Entry</span></span> | <span data-ttu-id="8e9a4-179">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e9a4-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e9a4-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e9a4-182">System-Only</span></span>            | <span data-ttu-id="8e9a4-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-183">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e9a4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8e9a4-185">True</span><span class="sxs-lookup"><span data-stu-id="8e9a4-185">True</span></span>                                                                |
| <span data-ttu-id="8e9a4-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e9a4-186">Is Indexed</span></span>             | <span data-ttu-id="8e9a4-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-187">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e9a4-188">In Global Catalog</span></span>      | <span data-ttu-id="8e9a4-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-189">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e9a4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e9a4-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e9a4-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8e9a4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e9a4-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e9a4-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-194">Search-Flags</span></span>           | <span data-ttu-id="8e9a4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e9a4-195">0x00000000</span></span>                                                          |
| <span data-ttu-id="8e9a4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-196">System-Flags</span></span>           | <span data-ttu-id="8e9a4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e9a4-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="8e9a4-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e9a4-198">Classes used in</span></span>        | [<span data-ttu-id="8e9a4-199">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e9a4-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e9a4-200">Windows Server 2008</span></span>



| <span data-ttu-id="8e9a4-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-201">Entry</span></span> | <span data-ttu-id="8e9a4-202">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e9a4-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e9a4-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e9a4-205">System-Only</span></span>            | <span data-ttu-id="8e9a4-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-206">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e9a4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8e9a4-208">True</span><span class="sxs-lookup"><span data-stu-id="8e9a4-208">True</span></span>                                                                |
| <span data-ttu-id="8e9a4-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e9a4-209">Is Indexed</span></span>             | <span data-ttu-id="8e9a4-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-210">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e9a4-211">In Global Catalog</span></span>      | <span data-ttu-id="8e9a4-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-212">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e9a4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e9a4-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e9a4-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8e9a4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e9a4-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e9a4-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-217">Search-Flags</span></span>           | <span data-ttu-id="8e9a4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e9a4-218">0x00000000</span></span>                                                          |
| <span data-ttu-id="8e9a4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-219">System-Flags</span></span>           | <span data-ttu-id="8e9a4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e9a4-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="8e9a4-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e9a4-221">Classes used in</span></span>        | [<span data-ttu-id="8e9a4-222">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e9a4-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e9a4-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e9a4-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-224">Entry</span></span> | <span data-ttu-id="8e9a4-225">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e9a4-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e9a4-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e9a4-228">System-Only</span></span>            | <span data-ttu-id="8e9a4-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-229">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e9a4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8e9a4-231">True</span><span class="sxs-lookup"><span data-stu-id="8e9a4-231">True</span></span>                                                                |
| <span data-ttu-id="8e9a4-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e9a4-232">Is Indexed</span></span>             | <span data-ttu-id="8e9a4-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-233">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e9a4-234">In Global Catalog</span></span>      | <span data-ttu-id="8e9a4-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-235">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e9a4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e9a4-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e9a4-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8e9a4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e9a4-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e9a4-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-240">Search-Flags</span></span>           | <span data-ttu-id="8e9a4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e9a4-241">0x00000000</span></span>                                                          |
| <span data-ttu-id="8e9a4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-242">System-Flags</span></span>           | <span data-ttu-id="8e9a4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e9a4-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="8e9a4-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e9a4-244">Classes used in</span></span>        | [<span data-ttu-id="8e9a4-245">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e9a4-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e9a4-246">Windows Server 2012</span></span>



| <span data-ttu-id="8e9a4-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e9a4-247">Entry</span></span> | <span data-ttu-id="8e9a4-248">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9a4-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e9a4-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e9a4-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e9a4-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8e9a4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e9a4-251">System-Only</span></span>            | <span data-ttu-id="8e9a4-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-252">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e9a4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8e9a4-254">True</span><span class="sxs-lookup"><span data-stu-id="8e9a4-254">True</span></span>                                                                |
| <span data-ttu-id="8e9a4-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e9a4-255">Is Indexed</span></span>             | <span data-ttu-id="8e9a4-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-256">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e9a4-257">In Global Catalog</span></span>      | <span data-ttu-id="8e9a4-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e9a4-258">False</span></span>                                                               |
| <span data-ttu-id="8e9a4-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e9a4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e9a4-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e9a4-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8e9a4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e9a4-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e9a4-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8e9a4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-263">Search-Flags</span></span>           | <span data-ttu-id="8e9a4-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e9a4-264">0x00000000</span></span>                                                          |
| <span data-ttu-id="8e9a4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e9a4-265">System-Flags</span></span>           | <span data-ttu-id="8e9a4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e9a4-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="8e9a4-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e9a4-267">Classes used in</span></span>        | [<span data-ttu-id="8e9a4-268">**MS-SQL-Склпубликатион**</span><span class="sxs-lookup"><span data-stu-id="8e9a4-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





