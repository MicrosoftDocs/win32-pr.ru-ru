---
title: Атрибут MS-SQL-помощью канала NamedPipe
description: Соединение именованного канала.
ms.assetid: d18c911d-06ed-4d08-b584-7b2748620770
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-SQL-помощью канала NamedPipe
- Схема AD атрибута mS-SQL-помощью канала NamedPipe
topic_type:
- apiref
api_name:
- MS-SQL-NamedPipe
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33e231be0561ae8c0e885911cb92954d6ff0d20d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416209"
---
# <a name="ms-sql-namedpipe-attribute"></a><span data-ttu-id="c9be3-105">Атрибут MS-SQL-помощью канала NamedPipe</span><span class="sxs-lookup"><span data-stu-id="c9be3-105">MS-SQL-NamedPipe attribute</span></span>

<span data-ttu-id="c9be3-106">Соединение именованного канала.</span><span class="sxs-lookup"><span data-stu-id="c9be3-106">The named pipe connection.</span></span>



| <span data-ttu-id="c9be3-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-107">Entry</span></span> | <span data-ttu-id="c9be3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c9be3-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9be3-109">CN</span></span>                | <span data-ttu-id="c9be3-110">MS-SQL-помощью канала NamedPipe</span><span class="sxs-lookup"><span data-stu-id="c9be3-110">MS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="c9be3-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c9be3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9be3-112">mS-SQL-помощью канала NamedPipe</span><span class="sxs-lookup"><span data-stu-id="c9be3-112">mS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="c9be3-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c9be3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c9be3-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c9be3-114">Update Privilege</span></span>  | <span data-ttu-id="c9be3-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c9be3-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="c9be3-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c9be3-116">Update Frequency</span></span>  | <span data-ttu-id="c9be3-117">При запуске системы.</span><span class="sxs-lookup"><span data-stu-id="c9be3-117">At system startup.</span></span>                          |
| <span data-ttu-id="c9be3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-118">Attribute-Id</span></span>      | <span data-ttu-id="c9be3-119">1.2.840.113556.1.4.1374</span><span class="sxs-lookup"><span data-stu-id="c9be3-119">1.2.840.113556.1.4.1374</span></span>                     |
| <span data-ttu-id="c9be3-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c9be3-120">System-Id-Guid</span></span>    | <span data-ttu-id="c9be3-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c9be3-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="c9be3-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9be3-122">Syntax</span></span>            | [<span data-ttu-id="c9be3-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c9be3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c9be3-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c9be3-124">Implementations</span></span>

-   [<span data-ttu-id="c9be3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9be3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9be3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9be3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9be3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9be3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9be3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9be3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9be3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9be3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9be3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9be3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9be3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9be3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c9be3-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-132">Entry</span></span> | <span data-ttu-id="c9be3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9be3-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9be3-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9be3-136">System-Only</span></span>            | <span data-ttu-id="c9be3-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-137">False</span></span>                                                     |
| <span data-ttu-id="c9be3-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9be3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c9be3-139">True</span><span class="sxs-lookup"><span data-stu-id="c9be3-139">True</span></span>                                                      |
| <span data-ttu-id="c9be3-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9be3-140">Is Indexed</span></span>             | <span data-ttu-id="c9be3-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-141">False</span></span>                                                     |
| <span data-ttu-id="c9be3-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9be3-142">In Global Catalog</span></span>      | <span data-ttu-id="c9be3-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-143">False</span></span>                                                     |
| <span data-ttu-id="c9be3-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9be3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9be3-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9be3-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9be3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9be3-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9be3-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-148">Search-Flags</span></span>           | <span data-ttu-id="c9be3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9be3-149">0x00000000</span></span>                                                |
| <span data-ttu-id="c9be3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-150">System-Flags</span></span>           | <span data-ttu-id="c9be3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9be3-151">0x00000010</span></span>                                                |
| <span data-ttu-id="c9be3-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9be3-152">Classes used in</span></span>        | [<span data-ttu-id="c9be3-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="c9be3-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9be3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9be3-154">Windows Server 2003</span></span>



| <span data-ttu-id="c9be3-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-155">Entry</span></span> | <span data-ttu-id="c9be3-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9be3-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9be3-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9be3-159">System-Only</span></span>            | <span data-ttu-id="c9be3-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-160">False</span></span>                                                     |
| <span data-ttu-id="c9be3-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9be3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c9be3-162">True</span><span class="sxs-lookup"><span data-stu-id="c9be3-162">True</span></span>                                                      |
| <span data-ttu-id="c9be3-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9be3-163">Is Indexed</span></span>             | <span data-ttu-id="c9be3-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-164">False</span></span>                                                     |
| <span data-ttu-id="c9be3-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9be3-165">In Global Catalog</span></span>      | <span data-ttu-id="c9be3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-166">False</span></span>                                                     |
| <span data-ttu-id="c9be3-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9be3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9be3-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9be3-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9be3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9be3-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9be3-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-171">Search-Flags</span></span>           | <span data-ttu-id="c9be3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9be3-172">0x00000000</span></span>                                                |
| <span data-ttu-id="c9be3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-173">System-Flags</span></span>           | <span data-ttu-id="c9be3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9be3-174">0x00000010</span></span>                                                |
| <span data-ttu-id="c9be3-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9be3-175">Classes used in</span></span>        | [<span data-ttu-id="c9be3-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="c9be3-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9be3-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9be3-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9be3-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-178">Entry</span></span> | <span data-ttu-id="c9be3-179">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9be3-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9be3-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9be3-182">System-Only</span></span>            | <span data-ttu-id="c9be3-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-183">False</span></span>                                                     |
| <span data-ttu-id="c9be3-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9be3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c9be3-185">True</span><span class="sxs-lookup"><span data-stu-id="c9be3-185">True</span></span>                                                      |
| <span data-ttu-id="c9be3-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9be3-186">Is Indexed</span></span>             | <span data-ttu-id="c9be3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-187">False</span></span>                                                     |
| <span data-ttu-id="c9be3-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9be3-188">In Global Catalog</span></span>      | <span data-ttu-id="c9be3-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-189">False</span></span>                                                     |
| <span data-ttu-id="c9be3-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9be3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9be3-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9be3-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9be3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9be3-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9be3-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-194">Search-Flags</span></span>           | <span data-ttu-id="c9be3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9be3-195">0x00000000</span></span>                                                |
| <span data-ttu-id="c9be3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-196">System-Flags</span></span>           | <span data-ttu-id="c9be3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9be3-197">0x00000010</span></span>                                                |
| <span data-ttu-id="c9be3-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9be3-198">Classes used in</span></span>        | [<span data-ttu-id="c9be3-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="c9be3-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9be3-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9be3-200">Windows Server 2008</span></span>



| <span data-ttu-id="c9be3-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-201">Entry</span></span> | <span data-ttu-id="c9be3-202">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9be3-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9be3-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9be3-205">System-Only</span></span>            | <span data-ttu-id="c9be3-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-206">False</span></span>                                                     |
| <span data-ttu-id="c9be3-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9be3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c9be3-208">True</span><span class="sxs-lookup"><span data-stu-id="c9be3-208">True</span></span>                                                      |
| <span data-ttu-id="c9be3-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9be3-209">Is Indexed</span></span>             | <span data-ttu-id="c9be3-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-210">False</span></span>                                                     |
| <span data-ttu-id="c9be3-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9be3-211">In Global Catalog</span></span>      | <span data-ttu-id="c9be3-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-212">False</span></span>                                                     |
| <span data-ttu-id="c9be3-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9be3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9be3-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9be3-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9be3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9be3-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9be3-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-217">Search-Flags</span></span>           | <span data-ttu-id="c9be3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9be3-218">0x00000000</span></span>                                                |
| <span data-ttu-id="c9be3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-219">System-Flags</span></span>           | <span data-ttu-id="c9be3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9be3-220">0x00000010</span></span>                                                |
| <span data-ttu-id="c9be3-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9be3-221">Classes used in</span></span>        | [<span data-ttu-id="c9be3-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="c9be3-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9be3-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9be3-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9be3-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-224">Entry</span></span> | <span data-ttu-id="c9be3-225">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9be3-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9be3-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9be3-228">System-Only</span></span>            | <span data-ttu-id="c9be3-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-229">False</span></span>                                                     |
| <span data-ttu-id="c9be3-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9be3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c9be3-231">True</span><span class="sxs-lookup"><span data-stu-id="c9be3-231">True</span></span>                                                      |
| <span data-ttu-id="c9be3-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9be3-232">Is Indexed</span></span>             | <span data-ttu-id="c9be3-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-233">False</span></span>                                                     |
| <span data-ttu-id="c9be3-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9be3-234">In Global Catalog</span></span>      | <span data-ttu-id="c9be3-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-235">False</span></span>                                                     |
| <span data-ttu-id="c9be3-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9be3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9be3-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9be3-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9be3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9be3-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9be3-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-240">Search-Flags</span></span>           | <span data-ttu-id="c9be3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9be3-241">0x00000000</span></span>                                                |
| <span data-ttu-id="c9be3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-242">System-Flags</span></span>           | <span data-ttu-id="c9be3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9be3-243">0x00000010</span></span>                                                |
| <span data-ttu-id="c9be3-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9be3-244">Classes used in</span></span>        | [<span data-ttu-id="c9be3-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="c9be3-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9be3-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9be3-246">Windows Server 2012</span></span>



| <span data-ttu-id="c9be3-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9be3-247">Entry</span></span> | <span data-ttu-id="c9be3-248">Значение</span><span class="sxs-lookup"><span data-stu-id="c9be3-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9be3-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9be3-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9be3-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9be3-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9be3-251">System-Only</span></span>            | <span data-ttu-id="c9be3-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-252">False</span></span>                                                     |
| <span data-ttu-id="c9be3-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9be3-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c9be3-254">True</span><span class="sxs-lookup"><span data-stu-id="c9be3-254">True</span></span>                                                      |
| <span data-ttu-id="c9be3-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9be3-255">Is Indexed</span></span>             | <span data-ttu-id="c9be3-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-256">False</span></span>                                                     |
| <span data-ttu-id="c9be3-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9be3-257">In Global Catalog</span></span>      | <span data-ttu-id="c9be3-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9be3-258">False</span></span>                                                     |
| <span data-ttu-id="c9be3-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9be3-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9be3-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9be3-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9be3-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9be3-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9be3-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9be3-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-263">Search-Flags</span></span>           | <span data-ttu-id="c9be3-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9be3-264">0x00000000</span></span>                                                |
| <span data-ttu-id="c9be3-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9be3-265">System-Flags</span></span>           | <span data-ttu-id="c9be3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9be3-266">0x00000010</span></span>                                                |
| <span data-ttu-id="c9be3-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9be3-267">Classes used in</span></span>        | [<span data-ttu-id="c9be3-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="c9be3-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





