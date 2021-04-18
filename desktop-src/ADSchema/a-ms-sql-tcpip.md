---
title: Атрибут MS-SQL-TCPIP
description: Точка подключения TCP.
ms.assetid: f61f7d54-958e-4f34-852e-222338c26de0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-TCPIP
- Схема AD атрибута mS-SQL-TCPIP
topic_type:
- apiref
api_name:
- MS-SQL-TCPIP
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 098d5e7818789774b425ad9e238f8f3b3a4d5378
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655493"
---
# <a name="ms-sql-tcpip-attribute"></a><span data-ttu-id="b4398-105">Атрибут MS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="b4398-105">MS-SQL-TCPIP attribute</span></span>

<span data-ttu-id="b4398-106">Точка подключения TCP.</span><span class="sxs-lookup"><span data-stu-id="b4398-106">The TCP connection point.</span></span>



| <span data-ttu-id="b4398-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-107">Entry</span></span> | <span data-ttu-id="b4398-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b4398-109">CN</span><span class="sxs-lookup"><span data-stu-id="b4398-109">CN</span></span>                | <span data-ttu-id="b4398-110">MS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="b4398-110">MS-SQL-TCPIP</span></span>                                |
| <span data-ttu-id="b4398-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b4398-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b4398-112">mS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="b4398-112">mS-SQL-TCPIP</span></span>                                |
| <span data-ttu-id="b4398-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b4398-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b4398-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b4398-114">Update Privilege</span></span>  | <span data-ttu-id="b4398-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b4398-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="b4398-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b4398-116">Update Frequency</span></span>  | <span data-ttu-id="b4398-117">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="b4398-117">At system startup.</span></span>                          |
| <span data-ttu-id="b4398-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-118">Attribute-Id</span></span>      | <span data-ttu-id="b4398-119">1.2.840.113556.1.4.1377</span><span class="sxs-lookup"><span data-stu-id="b4398-119">1.2.840.113556.1.4.1377</span></span>                     |
| <span data-ttu-id="b4398-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b4398-120">System-Id-Guid</span></span>    | <span data-ttu-id="b4398-121">8ac263a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b4398-121">8ac263a6-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="b4398-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4398-122">Syntax</span></span>            | [<span data-ttu-id="b4398-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b4398-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b4398-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b4398-124">Implementations</span></span>

-   [<span data-ttu-id="b4398-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4398-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4398-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4398-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4398-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4398-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4398-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4398-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4398-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4398-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4398-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4398-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4398-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4398-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b4398-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-132">Entry</span></span> | <span data-ttu-id="b4398-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4398-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4398-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4398-136">System-Only</span></span>            | <span data-ttu-id="b4398-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-137">False</span></span>                                                     |
| <span data-ttu-id="b4398-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4398-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b4398-139">True</span><span class="sxs-lookup"><span data-stu-id="b4398-139">True</span></span>                                                      |
| <span data-ttu-id="b4398-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4398-140">Is Indexed</span></span>             | <span data-ttu-id="b4398-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-141">False</span></span>                                                     |
| <span data-ttu-id="b4398-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4398-142">In Global Catalog</span></span>      | <span data-ttu-id="b4398-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-143">False</span></span>                                                     |
| <span data-ttu-id="b4398-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4398-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4398-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4398-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b4398-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4398-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4398-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-148">Search-Flags</span></span>           | <span data-ttu-id="b4398-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4398-149">0x00000000</span></span>                                                |
| <span data-ttu-id="b4398-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-150">System-Flags</span></span>           | <span data-ttu-id="b4398-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4398-151">0x00000010</span></span>                                                |
| <span data-ttu-id="b4398-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4398-152">Classes used in</span></span>        | [<span data-ttu-id="b4398-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b4398-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4398-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4398-154">Windows Server 2003</span></span>



| <span data-ttu-id="b4398-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-155">Entry</span></span> | <span data-ttu-id="b4398-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4398-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4398-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4398-159">System-Only</span></span>            | <span data-ttu-id="b4398-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-160">False</span></span>                                                     |
| <span data-ttu-id="b4398-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4398-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b4398-162">True</span><span class="sxs-lookup"><span data-stu-id="b4398-162">True</span></span>                                                      |
| <span data-ttu-id="b4398-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4398-163">Is Indexed</span></span>             | <span data-ttu-id="b4398-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-164">False</span></span>                                                     |
| <span data-ttu-id="b4398-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4398-165">In Global Catalog</span></span>      | <span data-ttu-id="b4398-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-166">False</span></span>                                                     |
| <span data-ttu-id="b4398-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4398-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4398-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4398-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b4398-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4398-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4398-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-171">Search-Flags</span></span>           | <span data-ttu-id="b4398-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4398-172">0x00000000</span></span>                                                |
| <span data-ttu-id="b4398-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-173">System-Flags</span></span>           | <span data-ttu-id="b4398-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4398-174">0x00000010</span></span>                                                |
| <span data-ttu-id="b4398-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4398-175">Classes used in</span></span>        | [<span data-ttu-id="b4398-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b4398-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4398-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4398-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4398-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-178">Entry</span></span> | <span data-ttu-id="b4398-179">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4398-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4398-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4398-182">System-Only</span></span>            | <span data-ttu-id="b4398-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-183">False</span></span>                                                     |
| <span data-ttu-id="b4398-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4398-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b4398-185">True</span><span class="sxs-lookup"><span data-stu-id="b4398-185">True</span></span>                                                      |
| <span data-ttu-id="b4398-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4398-186">Is Indexed</span></span>             | <span data-ttu-id="b4398-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-187">False</span></span>                                                     |
| <span data-ttu-id="b4398-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4398-188">In Global Catalog</span></span>      | <span data-ttu-id="b4398-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-189">False</span></span>                                                     |
| <span data-ttu-id="b4398-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4398-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4398-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4398-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b4398-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4398-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4398-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-194">Search-Flags</span></span>           | <span data-ttu-id="b4398-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4398-195">0x00000000</span></span>                                                |
| <span data-ttu-id="b4398-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-196">System-Flags</span></span>           | <span data-ttu-id="b4398-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4398-197">0x00000010</span></span>                                                |
| <span data-ttu-id="b4398-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4398-198">Classes used in</span></span>        | [<span data-ttu-id="b4398-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b4398-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4398-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4398-200">Windows Server 2008</span></span>



| <span data-ttu-id="b4398-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-201">Entry</span></span> | <span data-ttu-id="b4398-202">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4398-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4398-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4398-205">System-Only</span></span>            | <span data-ttu-id="b4398-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-206">False</span></span>                                                     |
| <span data-ttu-id="b4398-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4398-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b4398-208">True</span><span class="sxs-lookup"><span data-stu-id="b4398-208">True</span></span>                                                      |
| <span data-ttu-id="b4398-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4398-209">Is Indexed</span></span>             | <span data-ttu-id="b4398-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-210">False</span></span>                                                     |
| <span data-ttu-id="b4398-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4398-211">In Global Catalog</span></span>      | <span data-ttu-id="b4398-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-212">False</span></span>                                                     |
| <span data-ttu-id="b4398-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4398-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4398-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4398-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b4398-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4398-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4398-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-217">Search-Flags</span></span>           | <span data-ttu-id="b4398-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4398-218">0x00000000</span></span>                                                |
| <span data-ttu-id="b4398-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-219">System-Flags</span></span>           | <span data-ttu-id="b4398-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4398-220">0x00000010</span></span>                                                |
| <span data-ttu-id="b4398-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4398-221">Classes used in</span></span>        | [<span data-ttu-id="b4398-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b4398-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4398-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4398-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4398-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-224">Entry</span></span> | <span data-ttu-id="b4398-225">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4398-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4398-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4398-228">System-Only</span></span>            | <span data-ttu-id="b4398-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-229">False</span></span>                                                     |
| <span data-ttu-id="b4398-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4398-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b4398-231">True</span><span class="sxs-lookup"><span data-stu-id="b4398-231">True</span></span>                                                      |
| <span data-ttu-id="b4398-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4398-232">Is Indexed</span></span>             | <span data-ttu-id="b4398-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-233">False</span></span>                                                     |
| <span data-ttu-id="b4398-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4398-234">In Global Catalog</span></span>      | <span data-ttu-id="b4398-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-235">False</span></span>                                                     |
| <span data-ttu-id="b4398-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4398-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4398-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4398-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b4398-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4398-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4398-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-240">Search-Flags</span></span>           | <span data-ttu-id="b4398-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4398-241">0x00000000</span></span>                                                |
| <span data-ttu-id="b4398-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-242">System-Flags</span></span>           | <span data-ttu-id="b4398-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4398-243">0x00000010</span></span>                                                |
| <span data-ttu-id="b4398-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4398-244">Classes used in</span></span>        | [<span data-ttu-id="b4398-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b4398-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4398-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4398-246">Windows Server 2012</span></span>



| <span data-ttu-id="b4398-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4398-247">Entry</span></span> | <span data-ttu-id="b4398-248">Значение</span><span class="sxs-lookup"><span data-stu-id="b4398-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4398-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4398-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4398-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b4398-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4398-251">System-Only</span></span>            | <span data-ttu-id="b4398-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-252">False</span></span>                                                     |
| <span data-ttu-id="b4398-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4398-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b4398-254">True</span><span class="sxs-lookup"><span data-stu-id="b4398-254">True</span></span>                                                      |
| <span data-ttu-id="b4398-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4398-255">Is Indexed</span></span>             | <span data-ttu-id="b4398-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-256">False</span></span>                                                     |
| <span data-ttu-id="b4398-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4398-257">In Global Catalog</span></span>      | <span data-ttu-id="b4398-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4398-258">False</span></span>                                                     |
| <span data-ttu-id="b4398-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4398-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4398-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4398-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b4398-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4398-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4398-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b4398-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-263">Search-Flags</span></span>           | <span data-ttu-id="b4398-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4398-264">0x00000000</span></span>                                                |
| <span data-ttu-id="b4398-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4398-265">System-Flags</span></span>           | <span data-ttu-id="b4398-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4398-266">0x00000010</span></span>                                                |
| <span data-ttu-id="b4398-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4398-267">Classes used in</span></span>        | [<span data-ttu-id="b4398-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b4398-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





