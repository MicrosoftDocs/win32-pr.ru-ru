---
title: Атрибут MS-SQL-Регистередовнер
description: Зарегистрированный владелец текущего экземпляра SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-Регистередовнер
- Схема AD атрибута mS-SQL-Регистередовнер
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805051"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="2c6f6-105">Атрибут MS-SQL-Регистередовнер</span><span class="sxs-lookup"><span data-stu-id="2c6f6-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="2c6f6-106">Зарегистрированный владелец текущего экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2c6f6-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="2c6f6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-107">Entry</span></span> | <span data-ttu-id="2c6f6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2c6f6-109">CN</span><span class="sxs-lookup"><span data-stu-id="2c6f6-109">CN</span></span>                | <span data-ttu-id="2c6f6-110">MS-SQL-Регистередовнер</span><span class="sxs-lookup"><span data-stu-id="2c6f6-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="2c6f6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2c6f6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2c6f6-112">mS-SQL-Регистередовнер</span><span class="sxs-lookup"><span data-stu-id="2c6f6-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="2c6f6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2c6f6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2c6f6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2c6f6-114">Update Privilege</span></span>  | <span data-ttu-id="2c6f6-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="2c6f6-115">Domain administrator</span></span>                        |
| <span data-ttu-id="2c6f6-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2c6f6-116">Update Frequency</span></span>  | <span data-ttu-id="2c6f6-117">При установке системы.</span><span class="sxs-lookup"><span data-stu-id="2c6f6-117">At system setup.</span></span>                            |
| <span data-ttu-id="2c6f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-118">Attribute-Id</span></span>      | <span data-ttu-id="2c6f6-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="2c6f6-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="2c6f6-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2c6f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="2c6f6-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2c6f6-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="2c6f6-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c6f6-122">Syntax</span></span>            | [<span data-ttu-id="2c6f6-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2c6f6-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2c6f6-124">Implementations</span></span>

-   [<span data-ttu-id="2c6f6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c6f6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c6f6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c6f6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c6f6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c6f6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c6f6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c6f6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2c6f6-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-132">Entry</span></span> | <span data-ttu-id="2c6f6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f6-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c6f6-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c6f6-136">System-Only</span></span>            | <span data-ttu-id="2c6f6-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c6f6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2c6f6-139">True</span><span class="sxs-lookup"><span data-stu-id="2c6f6-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="2c6f6-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c6f6-140">Is Indexed</span></span>             | <span data-ttu-id="2c6f6-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c6f6-142">In Global Catalog</span></span>      | <span data-ttu-id="2c6f6-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c6f6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c6f6-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c6f6-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="2c6f6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c6f6-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c6f6-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-148">Search-Flags</span></span>           | <span data-ttu-id="2c6f6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c6f6-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-150">System-Flags</span></span>           | <span data-ttu-id="2c6f6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c6f6-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c6f6-152">Classes used in</span></span>        | [<span data-ttu-id="2c6f6-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="2c6f6-154">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c6f6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c6f6-155">Windows Server 2003</span></span>



| <span data-ttu-id="2c6f6-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-156">Entry</span></span> | <span data-ttu-id="2c6f6-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f6-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c6f6-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c6f6-160">System-Only</span></span>            | <span data-ttu-id="2c6f6-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c6f6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2c6f6-163">True</span><span class="sxs-lookup"><span data-stu-id="2c6f6-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="2c6f6-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c6f6-164">Is Indexed</span></span>             | <span data-ttu-id="2c6f6-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c6f6-166">In Global Catalog</span></span>      | <span data-ttu-id="2c6f6-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c6f6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c6f6-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c6f6-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="2c6f6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c6f6-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c6f6-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-172">Search-Flags</span></span>           | <span data-ttu-id="2c6f6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c6f6-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-174">System-Flags</span></span>           | <span data-ttu-id="2c6f6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c6f6-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c6f6-176">Classes used in</span></span>        | [<span data-ttu-id="2c6f6-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="2c6f6-178">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c6f6-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c6f6-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c6f6-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-180">Entry</span></span> | <span data-ttu-id="2c6f6-181">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f6-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c6f6-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c6f6-184">System-Only</span></span>            | <span data-ttu-id="2c6f6-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c6f6-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2c6f6-187">True</span><span class="sxs-lookup"><span data-stu-id="2c6f6-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="2c6f6-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c6f6-188">Is Indexed</span></span>             | <span data-ttu-id="2c6f6-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c6f6-190">In Global Catalog</span></span>      | <span data-ttu-id="2c6f6-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c6f6-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c6f6-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c6f6-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="2c6f6-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c6f6-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c6f6-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-196">Search-Flags</span></span>           | <span data-ttu-id="2c6f6-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c6f6-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-198">System-Flags</span></span>           | <span data-ttu-id="2c6f6-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c6f6-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c6f6-200">Classes used in</span></span>        | [<span data-ttu-id="2c6f6-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="2c6f6-202">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c6f6-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c6f6-203">Windows Server 2008</span></span>



| <span data-ttu-id="2c6f6-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-204">Entry</span></span> | <span data-ttu-id="2c6f6-205">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f6-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c6f6-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c6f6-208">System-Only</span></span>            | <span data-ttu-id="2c6f6-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c6f6-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2c6f6-211">True</span><span class="sxs-lookup"><span data-stu-id="2c6f6-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="2c6f6-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c6f6-212">Is Indexed</span></span>             | <span data-ttu-id="2c6f6-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c6f6-214">In Global Catalog</span></span>      | <span data-ttu-id="2c6f6-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c6f6-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c6f6-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c6f6-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="2c6f6-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c6f6-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c6f6-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-220">Search-Flags</span></span>           | <span data-ttu-id="2c6f6-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c6f6-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-222">System-Flags</span></span>           | <span data-ttu-id="2c6f6-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c6f6-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c6f6-224">Classes used in</span></span>        | [<span data-ttu-id="2c6f6-225">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="2c6f6-226">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c6f6-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c6f6-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c6f6-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-228">Entry</span></span> | <span data-ttu-id="2c6f6-229">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f6-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c6f6-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c6f6-232">System-Only</span></span>            | <span data-ttu-id="2c6f6-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c6f6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2c6f6-235">True</span><span class="sxs-lookup"><span data-stu-id="2c6f6-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="2c6f6-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c6f6-236">Is Indexed</span></span>             | <span data-ttu-id="2c6f6-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c6f6-238">In Global Catalog</span></span>      | <span data-ttu-id="2c6f6-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c6f6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c6f6-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c6f6-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="2c6f6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c6f6-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c6f6-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-244">Search-Flags</span></span>           | <span data-ttu-id="2c6f6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c6f6-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-246">System-Flags</span></span>           | <span data-ttu-id="2c6f6-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c6f6-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c6f6-248">Classes used in</span></span>        | [<span data-ttu-id="2c6f6-249">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="2c6f6-250">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c6f6-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c6f6-251">Windows Server 2012</span></span>



| <span data-ttu-id="2c6f6-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c6f6-252">Entry</span></span> | <span data-ttu-id="2c6f6-253">Значение</span><span class="sxs-lookup"><span data-stu-id="2c6f6-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f6-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c6f6-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c6f6-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c6f6-256">System-Only</span></span>            | <span data-ttu-id="2c6f6-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c6f6-258">Is-Single-Valued</span></span>       | <span data-ttu-id="2c6f6-259">True</span><span class="sxs-lookup"><span data-stu-id="2c6f6-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="2c6f6-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c6f6-260">Is Indexed</span></span>             | <span data-ttu-id="2c6f6-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c6f6-262">In Global Catalog</span></span>      | <span data-ttu-id="2c6f6-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c6f6-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="2c6f6-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c6f6-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c6f6-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c6f6-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="2c6f6-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c6f6-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c6f6-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="2c6f6-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-268">Search-Flags</span></span>           | <span data-ttu-id="2c6f6-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c6f6-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c6f6-270">System-Flags</span></span>           | <span data-ttu-id="2c6f6-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c6f6-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="2c6f6-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c6f6-272">Classes used in</span></span>        | [<span data-ttu-id="2c6f6-273">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="2c6f6-274">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="2c6f6-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





