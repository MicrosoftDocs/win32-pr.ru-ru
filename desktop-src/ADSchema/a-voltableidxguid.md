---
title: Атрибут Vol-Table-idx-GUID
description: Идентификатор индекса для записи таблицы Link-Track-Volume.
ms.assetid: f6df4ff1-87aa-480e-90f5-0a47822cd461
ms.tgt_platform: multiple
keywords:
- Vol-Table-idx-схема AD атрибута GUID
- Схема AD атрибута Волтаблеидксгуид
topic_type:
- apiref
api_name:
- Vol-Table-Idx-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a760d99b6883ea070e2f06daf11227056ea74a08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536107"
---
# <a name="vol-table-idx-guid-attribute"></a><span data-ttu-id="0dd2c-105">Атрибут Vol-Table-idx-GUID</span><span class="sxs-lookup"><span data-stu-id="0dd2c-105">Vol-Table-Idx-GUID attribute</span></span>

<span data-ttu-id="0dd2c-106">Идентификатор индекса для записи таблицы Link-Track-Volume.</span><span class="sxs-lookup"><span data-stu-id="0dd2c-106">The index identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="0dd2c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-107">Entry</span></span> | <span data-ttu-id="0dd2c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0dd2c-109">CN</span><span class="sxs-lookup"><span data-stu-id="0dd2c-109">CN</span></span>                | <span data-ttu-id="0dd2c-110">Vol-Table-idx-GUID</span><span class="sxs-lookup"><span data-stu-id="0dd2c-110">Vol-Table-Idx-GUID</span></span>                                    |
| <span data-ttu-id="0dd2c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0dd2c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0dd2c-112">волтаблеидксгуид</span><span class="sxs-lookup"><span data-stu-id="0dd2c-112">volTableIdxGUID</span></span>                                       |
| <span data-ttu-id="0dd2c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="0dd2c-113">Size</span></span>              | <span data-ttu-id="0dd2c-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="0dd2c-114">16 bytes</span></span>                                              |
| <span data-ttu-id="0dd2c-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0dd2c-115">Update Privilege</span></span>  | <span data-ttu-id="0dd2c-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="0dd2c-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="0dd2c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0dd2c-117">Update Frequency</span></span>  | <span data-ttu-id="0dd2c-118">При создании новой ссылки на файл.</span><span class="sxs-lookup"><span data-stu-id="0dd2c-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="0dd2c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-119">Attribute-Id</span></span>      | <span data-ttu-id="0dd2c-120">1.2.840.113556.1.4.334</span><span class="sxs-lookup"><span data-stu-id="0dd2c-120">1.2.840.113556.1.4.334</span></span>                                |
| <span data-ttu-id="0dd2c-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0dd2c-121">System-Id-Guid</span></span>    | <span data-ttu-id="0dd2c-122">1f0075fb-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="0dd2c-122">1f0075fb-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="0dd2c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dd2c-123">Syntax</span></span>            | [<span data-ttu-id="0dd2c-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0dd2c-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0dd2c-125">Implementations</span></span>

-   [<span data-ttu-id="0dd2c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0dd2c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0dd2c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0dd2c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0dd2c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0dd2c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0dd2c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0dd2c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0dd2c-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-133">Entry</span></span> | <span data-ttu-id="0dd2c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0dd2c-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0dd2c-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dd2c-137">System-Only</span></span>            | <span data-ttu-id="0dd2c-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-138">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0dd2c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0dd2c-140">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-140">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0dd2c-141">Is Indexed</span></span>             | <span data-ttu-id="0dd2c-142">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-142">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0dd2c-143">In Global Catalog</span></span>      | <span data-ttu-id="0dd2c-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-144">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0dd2c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dd2c-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0dd2c-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0dd2c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dd2c-147">Range-Lower</span></span>            | <span data-ttu-id="0dd2c-148">0</span><span class="sxs-lookup"><span data-stu-id="0dd2c-148">0</span></span>                                                              |
| <span data-ttu-id="0dd2c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dd2c-149">Range-Upper</span></span>            | <span data-ttu-id="0dd2c-150">16</span><span class="sxs-lookup"><span data-stu-id="0dd2c-150">16</span></span>                                                             |
| <span data-ttu-id="0dd2c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-151">Search-Flags</span></span>           | <span data-ttu-id="0dd2c-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0dd2c-152">0x00000001</span></span>                                                     |
| <span data-ttu-id="0dd2c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-153">System-Flags</span></span>           | <span data-ttu-id="0dd2c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dd2c-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="0dd2c-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0dd2c-155">Classes used in</span></span>        | [<span data-ttu-id="0dd2c-156">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0dd2c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0dd2c-157">Windows Server 2003</span></span>



| <span data-ttu-id="0dd2c-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-158">Entry</span></span> | <span data-ttu-id="0dd2c-159">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0dd2c-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0dd2c-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dd2c-162">System-Only</span></span>            | <span data-ttu-id="0dd2c-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-163">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0dd2c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="0dd2c-165">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-165">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0dd2c-166">Is Indexed</span></span>             | <span data-ttu-id="0dd2c-167">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-167">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0dd2c-168">In Global Catalog</span></span>      | <span data-ttu-id="0dd2c-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-169">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0dd2c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dd2c-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0dd2c-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0dd2c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dd2c-172">Range-Lower</span></span>            | <span data-ttu-id="0dd2c-173">0</span><span class="sxs-lookup"><span data-stu-id="0dd2c-173">0</span></span>                                                              |
| <span data-ttu-id="0dd2c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dd2c-174">Range-Upper</span></span>            | <span data-ttu-id="0dd2c-175">16</span><span class="sxs-lookup"><span data-stu-id="0dd2c-175">16</span></span>                                                             |
| <span data-ttu-id="0dd2c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-176">Search-Flags</span></span>           | <span data-ttu-id="0dd2c-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0dd2c-177">0x00000001</span></span>                                                     |
| <span data-ttu-id="0dd2c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-178">System-Flags</span></span>           | <span data-ttu-id="0dd2c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dd2c-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="0dd2c-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0dd2c-180">Classes used in</span></span>        | [<span data-ttu-id="0dd2c-181">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0dd2c-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0dd2c-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0dd2c-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-183">Entry</span></span> | <span data-ttu-id="0dd2c-184">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0dd2c-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0dd2c-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dd2c-187">System-Only</span></span>            | <span data-ttu-id="0dd2c-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-188">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0dd2c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="0dd2c-190">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-190">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0dd2c-191">Is Indexed</span></span>             | <span data-ttu-id="0dd2c-192">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-192">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0dd2c-193">In Global Catalog</span></span>      | <span data-ttu-id="0dd2c-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-194">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0dd2c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dd2c-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0dd2c-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0dd2c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dd2c-197">Range-Lower</span></span>            | <span data-ttu-id="0dd2c-198">0</span><span class="sxs-lookup"><span data-stu-id="0dd2c-198">0</span></span>                                                              |
| <span data-ttu-id="0dd2c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dd2c-199">Range-Upper</span></span>            | <span data-ttu-id="0dd2c-200">16</span><span class="sxs-lookup"><span data-stu-id="0dd2c-200">16</span></span>                                                             |
| <span data-ttu-id="0dd2c-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-201">Search-Flags</span></span>           | <span data-ttu-id="0dd2c-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0dd2c-202">0x00000001</span></span>                                                     |
| <span data-ttu-id="0dd2c-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-203">System-Flags</span></span>           | <span data-ttu-id="0dd2c-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dd2c-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="0dd2c-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0dd2c-205">Classes used in</span></span>        | [<span data-ttu-id="0dd2c-206">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0dd2c-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dd2c-207">Windows Server 2008</span></span>



| <span data-ttu-id="0dd2c-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-208">Entry</span></span> | <span data-ttu-id="0dd2c-209">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0dd2c-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0dd2c-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dd2c-212">System-Only</span></span>            | <span data-ttu-id="0dd2c-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-213">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0dd2c-214">Is-Single-Valued</span></span>       | <span data-ttu-id="0dd2c-215">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-215">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0dd2c-216">Is Indexed</span></span>             | <span data-ttu-id="0dd2c-217">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-217">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0dd2c-218">In Global Catalog</span></span>      | <span data-ttu-id="0dd2c-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-219">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0dd2c-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dd2c-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0dd2c-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0dd2c-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dd2c-222">Range-Lower</span></span>            | <span data-ttu-id="0dd2c-223">0</span><span class="sxs-lookup"><span data-stu-id="0dd2c-223">0</span></span>                                                              |
| <span data-ttu-id="0dd2c-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dd2c-224">Range-Upper</span></span>            | <span data-ttu-id="0dd2c-225">16</span><span class="sxs-lookup"><span data-stu-id="0dd2c-225">16</span></span>                                                             |
| <span data-ttu-id="0dd2c-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-226">Search-Flags</span></span>           | <span data-ttu-id="0dd2c-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0dd2c-227">0x00000001</span></span>                                                     |
| <span data-ttu-id="0dd2c-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-228">System-Flags</span></span>           | <span data-ttu-id="0dd2c-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dd2c-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="0dd2c-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0dd2c-230">Classes used in</span></span>        | [<span data-ttu-id="0dd2c-231">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0dd2c-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0dd2c-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0dd2c-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-233">Entry</span></span> | <span data-ttu-id="0dd2c-234">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0dd2c-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0dd2c-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dd2c-237">System-Only</span></span>            | <span data-ttu-id="0dd2c-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-238">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0dd2c-239">Is-Single-Valued</span></span>       | <span data-ttu-id="0dd2c-240">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-240">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0dd2c-241">Is Indexed</span></span>             | <span data-ttu-id="0dd2c-242">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-242">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0dd2c-243">In Global Catalog</span></span>      | <span data-ttu-id="0dd2c-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-244">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0dd2c-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dd2c-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0dd2c-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0dd2c-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dd2c-247">Range-Lower</span></span>            | <span data-ttu-id="0dd2c-248">0</span><span class="sxs-lookup"><span data-stu-id="0dd2c-248">0</span></span>                                                              |
| <span data-ttu-id="0dd2c-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dd2c-249">Range-Upper</span></span>            | <span data-ttu-id="0dd2c-250">16</span><span class="sxs-lookup"><span data-stu-id="0dd2c-250">16</span></span>                                                             |
| <span data-ttu-id="0dd2c-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-251">Search-Flags</span></span>           | <span data-ttu-id="0dd2c-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0dd2c-252">0x00000001</span></span>                                                     |
| <span data-ttu-id="0dd2c-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-253">System-Flags</span></span>           | <span data-ttu-id="0dd2c-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dd2c-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="0dd2c-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0dd2c-255">Classes used in</span></span>        | [<span data-ttu-id="0dd2c-256">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0dd2c-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0dd2c-257">Windows Server 2012</span></span>



| <span data-ttu-id="0dd2c-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="0dd2c-258">Entry</span></span> | <span data-ttu-id="0dd2c-259">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2c-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0dd2c-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0dd2c-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dd2c-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0dd2c-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dd2c-262">System-Only</span></span>            | <span data-ttu-id="0dd2c-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-263">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0dd2c-264">Is-Single-Valued</span></span>       | <span data-ttu-id="0dd2c-265">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-265">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0dd2c-266">Is Indexed</span></span>             | <span data-ttu-id="0dd2c-267">True</span><span class="sxs-lookup"><span data-stu-id="0dd2c-267">True</span></span>                                                           |
| <span data-ttu-id="0dd2c-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0dd2c-268">In Global Catalog</span></span>      | <span data-ttu-id="0dd2c-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="0dd2c-269">False</span></span>                                                          |
| <span data-ttu-id="0dd2c-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0dd2c-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dd2c-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0dd2c-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0dd2c-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dd2c-272">Range-Lower</span></span>            | <span data-ttu-id="0dd2c-273">0</span><span class="sxs-lookup"><span data-stu-id="0dd2c-273">0</span></span>                                                              |
| <span data-ttu-id="0dd2c-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dd2c-274">Range-Upper</span></span>            | <span data-ttu-id="0dd2c-275">16</span><span class="sxs-lookup"><span data-stu-id="0dd2c-275">16</span></span>                                                             |
| <span data-ttu-id="0dd2c-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-276">Search-Flags</span></span>           | <span data-ttu-id="0dd2c-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0dd2c-277">0x00000001</span></span>                                                     |
| <span data-ttu-id="0dd2c-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dd2c-278">System-Flags</span></span>           | <span data-ttu-id="0dd2c-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dd2c-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="0dd2c-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0dd2c-280">Classes used in</span></span>        | [<span data-ttu-id="0dd2c-281">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="0dd2c-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





