---
title: Атрибут MS-SQL-Уникодесортордер
description: Порядок сортировки Юникода для текущего экземпляра SQL Server.
ms.assetid: c7f9d81d-a9c3-4be9-8ead-cf3d59352dbb
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Уникодесортордер
- Схема AD атрибута mS-SQL-Уникодесортордер
topic_type:
- apiref
api_name:
- MS-SQL-UnicodeSortOrder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9240844a45e8e4ea567ff96df0eb992f316a7787
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535777"
---
# <a name="ms-sql-unicodesortorder-attribute"></a><span data-ttu-id="2e6e4-105">Атрибут MS-SQL-Уникодесортордер</span><span class="sxs-lookup"><span data-stu-id="2e6e4-105">MS-SQL-UnicodeSortOrder attribute</span></span>

<span data-ttu-id="2e6e4-106">Порядок сортировки Юникода для текущего экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2e6e4-106">The Unicode sort order for the current instance of SQL Server.</span></span>



| <span data-ttu-id="2e6e4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-107">Entry</span></span> | <span data-ttu-id="2e6e4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2e6e4-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e6e4-109">CN</span></span>                | <span data-ttu-id="2e6e4-110">MS-SQL-Уникодесортордер</span><span class="sxs-lookup"><span data-stu-id="2e6e4-110">MS-SQL-UnicodeSortOrder</span></span>              |
| <span data-ttu-id="2e6e4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2e6e4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e6e4-112">mS-SQL-Уникодесортордер</span><span class="sxs-lookup"><span data-stu-id="2e6e4-112">mS-SQL-UnicodeSortOrder</span></span>              |
| <span data-ttu-id="2e6e4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2e6e4-113">Size</span></span>              | <span data-ttu-id="2e6e4-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="2e6e4-114">4 bytes</span></span>                              |
| <span data-ttu-id="2e6e4-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2e6e4-115">Update Privilege</span></span>  | <span data-ttu-id="2e6e4-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="2e6e4-116">Domain administrator</span></span>                 |
| <span data-ttu-id="2e6e4-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2e6e4-117">Update Frequency</span></span>  | <span data-ttu-id="2e6e4-118">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="2e6e4-118">At system startup.</span></span>                   |
| <span data-ttu-id="2e6e4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-119">Attribute-Id</span></span>      | <span data-ttu-id="2e6e4-120">1.2.840.113556.1.4.1372</span><span class="sxs-lookup"><span data-stu-id="2e6e4-120">1.2.840.113556.1.4.1372</span></span>              |
| <span data-ttu-id="2e6e4-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2e6e4-121">System-Id-Guid</span></span>    | <span data-ttu-id="2e6e4-122">72dc918a-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2e6e4-122">72dc918a-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="2e6e4-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e6e4-123">Syntax</span></span>            | [<span data-ttu-id="2e6e4-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2e6e4-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2e6e4-125">Implementations</span></span>

-   [<span data-ttu-id="2e6e4-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e6e4-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e6e4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e6e4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e6e4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e6e4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e6e4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e6e4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2e6e4-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-133">Entry</span></span> | <span data-ttu-id="2e6e4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2e6e4-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e6e4-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e6e4-137">System-Only</span></span>            | <span data-ttu-id="2e6e4-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-138">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e6e4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2e6e4-140">True</span><span class="sxs-lookup"><span data-stu-id="2e6e4-140">True</span></span>                                                      |
| <span data-ttu-id="2e6e4-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e6e4-141">Is Indexed</span></span>             | <span data-ttu-id="2e6e4-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-142">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e6e4-143">In Global Catalog</span></span>      | <span data-ttu-id="2e6e4-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-144">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e6e4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e6e4-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e6e4-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2e6e4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e6e4-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e6e4-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-149">Search-Flags</span></span>           | <span data-ttu-id="2e6e4-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e6e4-150">0x00000000</span></span>                                                |
| <span data-ttu-id="2e6e4-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-151">System-Flags</span></span>           | <span data-ttu-id="2e6e4-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e6e4-152">0x00000010</span></span>                                                |
| <span data-ttu-id="2e6e4-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e6e4-153">Classes used in</span></span>        | [<span data-ttu-id="2e6e4-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e6e4-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e6e4-155">Windows Server 2003</span></span>



| <span data-ttu-id="2e6e4-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-156">Entry</span></span> | <span data-ttu-id="2e6e4-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2e6e4-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e6e4-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e6e4-160">System-Only</span></span>            | <span data-ttu-id="2e6e4-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-161">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e6e4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2e6e4-163">True</span><span class="sxs-lookup"><span data-stu-id="2e6e4-163">True</span></span>                                                      |
| <span data-ttu-id="2e6e4-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e6e4-164">Is Indexed</span></span>             | <span data-ttu-id="2e6e4-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-165">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e6e4-166">In Global Catalog</span></span>      | <span data-ttu-id="2e6e4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-167">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e6e4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e6e4-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e6e4-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2e6e4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e6e4-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e6e4-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-172">Search-Flags</span></span>           | <span data-ttu-id="2e6e4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e6e4-173">0x00000000</span></span>                                                |
| <span data-ttu-id="2e6e4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-174">System-Flags</span></span>           | <span data-ttu-id="2e6e4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e6e4-175">0x00000010</span></span>                                                |
| <span data-ttu-id="2e6e4-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e6e4-176">Classes used in</span></span>        | [<span data-ttu-id="2e6e4-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e6e4-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e6e4-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e6e4-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-179">Entry</span></span> | <span data-ttu-id="2e6e4-180">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2e6e4-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e6e4-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e6e4-183">System-Only</span></span>            | <span data-ttu-id="2e6e4-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-184">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e6e4-185">Is-Single-Valued</span></span>       | <span data-ttu-id="2e6e4-186">True</span><span class="sxs-lookup"><span data-stu-id="2e6e4-186">True</span></span>                                                      |
| <span data-ttu-id="2e6e4-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e6e4-187">Is Indexed</span></span>             | <span data-ttu-id="2e6e4-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-188">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e6e4-189">In Global Catalog</span></span>      | <span data-ttu-id="2e6e4-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-190">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e6e4-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e6e4-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e6e4-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2e6e4-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e6e4-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e6e4-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-195">Search-Flags</span></span>           | <span data-ttu-id="2e6e4-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e6e4-196">0x00000000</span></span>                                                |
| <span data-ttu-id="2e6e4-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-197">System-Flags</span></span>           | <span data-ttu-id="2e6e4-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e6e4-198">0x00000010</span></span>                                                |
| <span data-ttu-id="2e6e4-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e6e4-199">Classes used in</span></span>        | [<span data-ttu-id="2e6e4-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e6e4-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e6e4-201">Windows Server 2008</span></span>



| <span data-ttu-id="2e6e4-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-202">Entry</span></span> | <span data-ttu-id="2e6e4-203">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2e6e4-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e6e4-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e6e4-206">System-Only</span></span>            | <span data-ttu-id="2e6e4-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-207">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e6e4-208">Is-Single-Valued</span></span>       | <span data-ttu-id="2e6e4-209">True</span><span class="sxs-lookup"><span data-stu-id="2e6e4-209">True</span></span>                                                      |
| <span data-ttu-id="2e6e4-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e6e4-210">Is Indexed</span></span>             | <span data-ttu-id="2e6e4-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-211">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e6e4-212">In Global Catalog</span></span>      | <span data-ttu-id="2e6e4-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-213">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e6e4-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e6e4-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e6e4-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2e6e4-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e6e4-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e6e4-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-218">Search-Flags</span></span>           | <span data-ttu-id="2e6e4-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e6e4-219">0x00000000</span></span>                                                |
| <span data-ttu-id="2e6e4-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-220">System-Flags</span></span>           | <span data-ttu-id="2e6e4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e6e4-221">0x00000010</span></span>                                                |
| <span data-ttu-id="2e6e4-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e6e4-222">Classes used in</span></span>        | [<span data-ttu-id="2e6e4-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e6e4-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e6e4-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e6e4-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-225">Entry</span></span> | <span data-ttu-id="2e6e4-226">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2e6e4-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e6e4-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e6e4-229">System-Only</span></span>            | <span data-ttu-id="2e6e4-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-230">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e6e4-231">Is-Single-Valued</span></span>       | <span data-ttu-id="2e6e4-232">True</span><span class="sxs-lookup"><span data-stu-id="2e6e4-232">True</span></span>                                                      |
| <span data-ttu-id="2e6e4-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e6e4-233">Is Indexed</span></span>             | <span data-ttu-id="2e6e4-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-234">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e6e4-235">In Global Catalog</span></span>      | <span data-ttu-id="2e6e4-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-236">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e6e4-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e6e4-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e6e4-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2e6e4-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e6e4-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e6e4-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-241">Search-Flags</span></span>           | <span data-ttu-id="2e6e4-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e6e4-242">0x00000000</span></span>                                                |
| <span data-ttu-id="2e6e4-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-243">System-Flags</span></span>           | <span data-ttu-id="2e6e4-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e6e4-244">0x00000010</span></span>                                                |
| <span data-ttu-id="2e6e4-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e6e4-245">Classes used in</span></span>        | [<span data-ttu-id="2e6e4-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e6e4-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e6e4-247">Windows Server 2012</span></span>



| <span data-ttu-id="2e6e4-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e6e4-248">Entry</span></span> | <span data-ttu-id="2e6e4-249">Значение</span><span class="sxs-lookup"><span data-stu-id="2e6e4-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2e6e4-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e6e4-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e6e4-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="2e6e4-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e6e4-252">System-Only</span></span>            | <span data-ttu-id="2e6e4-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-253">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e6e4-254">Is-Single-Valued</span></span>       | <span data-ttu-id="2e6e4-255">True</span><span class="sxs-lookup"><span data-stu-id="2e6e4-255">True</span></span>                                                      |
| <span data-ttu-id="2e6e4-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e6e4-256">Is Indexed</span></span>             | <span data-ttu-id="2e6e4-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-257">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e6e4-258">In Global Catalog</span></span>      | <span data-ttu-id="2e6e4-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e6e4-259">False</span></span>                                                     |
| <span data-ttu-id="2e6e4-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e6e4-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e6e4-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e6e4-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="2e6e4-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e6e4-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e6e4-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="2e6e4-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-264">Search-Flags</span></span>           | <span data-ttu-id="2e6e4-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e6e4-265">0x00000000</span></span>                                                |
| <span data-ttu-id="2e6e4-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e6e4-266">System-Flags</span></span>           | <span data-ttu-id="2e6e4-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e6e4-267">0x00000010</span></span>                                                |
| <span data-ttu-id="2e6e4-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e6e4-268">Classes used in</span></span>        | [<span data-ttu-id="2e6e4-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2e6e4-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





