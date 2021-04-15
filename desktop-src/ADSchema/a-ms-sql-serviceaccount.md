---
title: Атрибут MS-SQL-учетная запись службы
description: Определяемая пользователем строка. Значение по умолчанию — учетная запись службы.
ms.assetid: 0db095c8-8492-45c0-b509-d4082cec2c13
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-учетная запись службы
- Схема AD атрибута mS-SQL-учетная запись службы
topic_type:
- apiref
api_name:
- MS-SQL-ServiceAccount
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab96de3d56dedd3178e579e100f00b77df4edb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654897"
---
# <a name="ms-sql-serviceaccount-attribute"></a><span data-ttu-id="a35a8-106">Атрибут MS-SQL-учетная запись службы</span><span class="sxs-lookup"><span data-stu-id="a35a8-106">MS-SQL-ServiceAccount attribute</span></span>

<span data-ttu-id="a35a8-107">Определяемая пользователем строка.</span><span class="sxs-lookup"><span data-stu-id="a35a8-107">A user defined string.</span></span> <span data-ttu-id="a35a8-108">Значение по умолчанию — учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="a35a8-108">The default is set to ServiceAccount.</span></span>



| <span data-ttu-id="a35a8-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-109">Entry</span></span> | <span data-ttu-id="a35a8-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a35a8-111">CN</span><span class="sxs-lookup"><span data-stu-id="a35a8-111">CN</span></span>                | <span data-ttu-id="a35a8-112">MS-SQL-учетная запись службы</span><span class="sxs-lookup"><span data-stu-id="a35a8-112">MS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="a35a8-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a35a8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a35a8-114">mS-SQL-учетная запись службы</span><span class="sxs-lookup"><span data-stu-id="a35a8-114">mS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="a35a8-115">Размер</span><span class="sxs-lookup"><span data-stu-id="a35a8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a35a8-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a35a8-116">Update Privilege</span></span>  | <span data-ttu-id="a35a8-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="a35a8-117">Domain administrator</span></span>                        |
| <span data-ttu-id="a35a8-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a35a8-118">Update Frequency</span></span>  | <span data-ttu-id="a35a8-119">При установке системы.</span><span class="sxs-lookup"><span data-stu-id="a35a8-119">At system setup.</span></span>                            |
| <span data-ttu-id="a35a8-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-120">Attribute-Id</span></span>      | <span data-ttu-id="a35a8-121">1.2.840.113556.1.4.1369</span><span class="sxs-lookup"><span data-stu-id="a35a8-121">1.2.840.113556.1.4.1369</span></span>                     |
| <span data-ttu-id="a35a8-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a35a8-122">System-Id-Guid</span></span>    | <span data-ttu-id="a35a8-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a35a8-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="a35a8-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a35a8-124">Syntax</span></span>            | [<span data-ttu-id="a35a8-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="a35a8-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a35a8-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a35a8-126">Implementations</span></span>

-   [<span data-ttu-id="a35a8-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a35a8-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a35a8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a35a8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a35a8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a35a8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a35a8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a35a8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a35a8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a35a8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a35a8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a35a8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a35a8-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a35a8-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a35a8-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-134">Entry</span></span> | <span data-ttu-id="a35a8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35a8-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a35a8-136">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-137">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a35a8-138">System-Only</span></span>            | <span data-ttu-id="a35a8-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-139">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a35a8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a35a8-141">True</span><span class="sxs-lookup"><span data-stu-id="a35a8-141">True</span></span>                                                                                                                  |
| <span data-ttu-id="a35a8-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a35a8-142">Is Indexed</span></span>             | <span data-ttu-id="a35a8-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a35a8-144">In Global Catalog</span></span>      | <span data-ttu-id="a35a8-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-145">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a35a8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a35a8-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a35a8-147">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="a35a8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a35a8-148">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a35a8-149">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-150">Search-Flags</span></span>           | <span data-ttu-id="a35a8-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a35a8-151">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-152">System-Flags</span></span>           | <span data-ttu-id="a35a8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a35a8-153">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a35a8-154">Classes used in</span></span>        | [<span data-ttu-id="a35a8-155">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="a35a8-156">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-156">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a35a8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a35a8-157">Windows Server 2003</span></span>



| <span data-ttu-id="a35a8-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-158">Entry</span></span> | <span data-ttu-id="a35a8-159">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35a8-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a35a8-160">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-161">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a35a8-162">System-Only</span></span>            | <span data-ttu-id="a35a8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-163">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a35a8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a35a8-165">True</span><span class="sxs-lookup"><span data-stu-id="a35a8-165">True</span></span>                                                                                                                  |
| <span data-ttu-id="a35a8-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a35a8-166">Is Indexed</span></span>             | <span data-ttu-id="a35a8-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a35a8-168">In Global Catalog</span></span>      | <span data-ttu-id="a35a8-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-169">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a35a8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a35a8-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a35a8-171">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="a35a8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a35a8-172">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a35a8-173">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-174">Search-Flags</span></span>           | <span data-ttu-id="a35a8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a35a8-175">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-176">System-Flags</span></span>           | <span data-ttu-id="a35a8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a35a8-177">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a35a8-178">Classes used in</span></span>        | [<span data-ttu-id="a35a8-179">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-179">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="a35a8-180">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-180">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a35a8-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a35a8-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a35a8-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-182">Entry</span></span> | <span data-ttu-id="a35a8-183">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35a8-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a35a8-184">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-185">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a35a8-186">System-Only</span></span>            | <span data-ttu-id="a35a8-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-187">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a35a8-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a35a8-189">True</span><span class="sxs-lookup"><span data-stu-id="a35a8-189">True</span></span>                                                                                                                  |
| <span data-ttu-id="a35a8-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a35a8-190">Is Indexed</span></span>             | <span data-ttu-id="a35a8-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a35a8-192">In Global Catalog</span></span>      | <span data-ttu-id="a35a8-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-193">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a35a8-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a35a8-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a35a8-195">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="a35a8-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a35a8-196">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a35a8-197">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-198">Search-Flags</span></span>           | <span data-ttu-id="a35a8-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a35a8-199">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-200">System-Flags</span></span>           | <span data-ttu-id="a35a8-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a35a8-201">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a35a8-202">Classes used in</span></span>        | [<span data-ttu-id="a35a8-203">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-203">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="a35a8-204">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-204">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a35a8-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a35a8-205">Windows Server 2008</span></span>



| <span data-ttu-id="a35a8-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-206">Entry</span></span> | <span data-ttu-id="a35a8-207">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35a8-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a35a8-208">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-209">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="a35a8-210">System-Only</span></span>            | <span data-ttu-id="a35a8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-211">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a35a8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="a35a8-213">True</span><span class="sxs-lookup"><span data-stu-id="a35a8-213">True</span></span>                                                                                                                  |
| <span data-ttu-id="a35a8-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a35a8-214">Is Indexed</span></span>             | <span data-ttu-id="a35a8-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a35a8-216">In Global Catalog</span></span>      | <span data-ttu-id="a35a8-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-217">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a35a8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="a35a8-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a35a8-219">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="a35a8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a35a8-220">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a35a8-221">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-222">Search-Flags</span></span>           | <span data-ttu-id="a35a8-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a35a8-223">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-224">System-Flags</span></span>           | <span data-ttu-id="a35a8-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a35a8-225">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a35a8-226">Classes used in</span></span>        | [<span data-ttu-id="a35a8-227">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-227">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="a35a8-228">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-228">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a35a8-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a35a8-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a35a8-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-230">Entry</span></span> | <span data-ttu-id="a35a8-231">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35a8-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a35a8-232">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-233">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a35a8-234">System-Only</span></span>            | <span data-ttu-id="a35a8-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-235">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a35a8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a35a8-237">True</span><span class="sxs-lookup"><span data-stu-id="a35a8-237">True</span></span>                                                                                                                  |
| <span data-ttu-id="a35a8-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a35a8-238">Is Indexed</span></span>             | <span data-ttu-id="a35a8-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a35a8-240">In Global Catalog</span></span>      | <span data-ttu-id="a35a8-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-241">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a35a8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a35a8-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a35a8-243">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="a35a8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a35a8-244">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a35a8-245">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-246">Search-Flags</span></span>           | <span data-ttu-id="a35a8-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a35a8-247">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-248">System-Flags</span></span>           | <span data-ttu-id="a35a8-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a35a8-249">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a35a8-250">Classes used in</span></span>        | [<span data-ttu-id="a35a8-251">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-251">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="a35a8-252">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-252">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a35a8-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a35a8-253">Windows Server 2012</span></span>



| <span data-ttu-id="a35a8-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="a35a8-254">Entry</span></span> | <span data-ttu-id="a35a8-255">Значение</span><span class="sxs-lookup"><span data-stu-id="a35a8-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35a8-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a35a8-256">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a35a8-257">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="a35a8-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="a35a8-258">System-Only</span></span>            | <span data-ttu-id="a35a8-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-259">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a35a8-260">Is-Single-Valued</span></span>       | <span data-ttu-id="a35a8-261">True</span><span class="sxs-lookup"><span data-stu-id="a35a8-261">True</span></span>                                                                                                                  |
| <span data-ttu-id="a35a8-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a35a8-262">Is Indexed</span></span>             | <span data-ttu-id="a35a8-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a35a8-264">In Global Catalog</span></span>      | <span data-ttu-id="a35a8-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="a35a8-265">False</span></span>                                                                                                                 |
| <span data-ttu-id="a35a8-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a35a8-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="a35a8-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a35a8-267">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="a35a8-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a35a8-268">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a35a8-269">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="a35a8-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-270">Search-Flags</span></span>           | <span data-ttu-id="a35a8-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a35a8-271">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a35a8-272">System-Flags</span></span>           | <span data-ttu-id="a35a8-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a35a8-273">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="a35a8-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a35a8-274">Classes used in</span></span>        | [<span data-ttu-id="a35a8-275">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-275">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="a35a8-276">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="a35a8-276">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





