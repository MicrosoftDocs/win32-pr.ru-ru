---
title: Атрибут Vol-Table-GUID
description: Уникальный идентификатор для записи таблицы Link-Track-Volume.
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Vol-Table-GUID
- Схема AD атрибута Волтаблегуид
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a23bcd088304b4a683ce3ff0f203d3c82fecf8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493656"
---
# <a name="vol-table-guid-attribute"></a><span data-ttu-id="051a0-105">Атрибут Vol-Table-GUID</span><span class="sxs-lookup"><span data-stu-id="051a0-105">Vol-Table-GUID attribute</span></span>

<span data-ttu-id="051a0-106">Уникальный идентификатор для записи таблицы Link-Track-Volume.</span><span class="sxs-lookup"><span data-stu-id="051a0-106">The unique identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="051a0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-107">Entry</span></span> | <span data-ttu-id="051a0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="051a0-109">CN</span><span class="sxs-lookup"><span data-stu-id="051a0-109">CN</span></span>                | <span data-ttu-id="051a0-110">Vol-Таблица-GUID</span><span class="sxs-lookup"><span data-stu-id="051a0-110">Vol-Table-GUID</span></span>                                        |
| <span data-ttu-id="051a0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="051a0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="051a0-112">волтаблегуид</span><span class="sxs-lookup"><span data-stu-id="051a0-112">volTableGUID</span></span>                                          |
| <span data-ttu-id="051a0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="051a0-113">Size</span></span>              | <span data-ttu-id="051a0-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="051a0-114">16 bytes</span></span>                                              |
| <span data-ttu-id="051a0-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="051a0-115">Update Privilege</span></span>  | <span data-ttu-id="051a0-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="051a0-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="051a0-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="051a0-117">Update Frequency</span></span>  | <span data-ttu-id="051a0-118">При создании новой ссылки на файл.</span><span class="sxs-lookup"><span data-stu-id="051a0-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="051a0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-119">Attribute-Id</span></span>      | <span data-ttu-id="051a0-120">1.2.840.113556.1.4.336</span><span class="sxs-lookup"><span data-stu-id="051a0-120">1.2.840.113556.1.4.336</span></span>                                |
| <span data-ttu-id="051a0-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="051a0-121">System-Id-Guid</span></span>    | <span data-ttu-id="051a0-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="051a0-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="051a0-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="051a0-123">Syntax</span></span>            | [<span data-ttu-id="051a0-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="051a0-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="051a0-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="051a0-125">Implementations</span></span>

-   [<span data-ttu-id="051a0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="051a0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="051a0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="051a0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="051a0-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="051a0-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="051a0-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="051a0-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="051a0-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="051a0-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="051a0-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="051a0-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="051a0-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="051a0-132">Windows 2000 Server</span></span>



| <span data-ttu-id="051a0-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-133">Entry</span></span> | <span data-ttu-id="051a0-134">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="051a0-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="051a0-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="051a0-137">System-Only</span></span>            | <span data-ttu-id="051a0-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-138">False</span></span>                                                          |
| <span data-ttu-id="051a0-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="051a0-139">Is-Single-Valued</span></span>       | <span data-ttu-id="051a0-140">True</span><span class="sxs-lookup"><span data-stu-id="051a0-140">True</span></span>                                                           |
| <span data-ttu-id="051a0-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="051a0-141">Is Indexed</span></span>             | <span data-ttu-id="051a0-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-142">False</span></span>                                                          |
| <span data-ttu-id="051a0-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="051a0-143">In Global Catalog</span></span>      | <span data-ttu-id="051a0-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-144">False</span></span>                                                          |
| <span data-ttu-id="051a0-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="051a0-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="051a0-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="051a0-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="051a0-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="051a0-147">Range-Lower</span></span>            | <span data-ttu-id="051a0-148">0</span><span class="sxs-lookup"><span data-stu-id="051a0-148">0</span></span>                                                              |
| <span data-ttu-id="051a0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="051a0-149">Range-Upper</span></span>            | <span data-ttu-id="051a0-150">16</span><span class="sxs-lookup"><span data-stu-id="051a0-150">16</span></span>                                                             |
| <span data-ttu-id="051a0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-151">Search-Flags</span></span>           | <span data-ttu-id="051a0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="051a0-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="051a0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-153">System-Flags</span></span>           | <span data-ttu-id="051a0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="051a0-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="051a0-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="051a0-155">Classes used in</span></span>        | [<span data-ttu-id="051a0-156">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="051a0-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="051a0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="051a0-157">Windows Server 2003</span></span>



| <span data-ttu-id="051a0-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-158">Entry</span></span> | <span data-ttu-id="051a0-159">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="051a0-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="051a0-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="051a0-162">System-Only</span></span>            | <span data-ttu-id="051a0-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-163">False</span></span>                                                          |
| <span data-ttu-id="051a0-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="051a0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="051a0-165">True</span><span class="sxs-lookup"><span data-stu-id="051a0-165">True</span></span>                                                           |
| <span data-ttu-id="051a0-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="051a0-166">Is Indexed</span></span>             | <span data-ttu-id="051a0-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-167">False</span></span>                                                          |
| <span data-ttu-id="051a0-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="051a0-168">In Global Catalog</span></span>      | <span data-ttu-id="051a0-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-169">False</span></span>                                                          |
| <span data-ttu-id="051a0-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="051a0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="051a0-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="051a0-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="051a0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="051a0-172">Range-Lower</span></span>            | <span data-ttu-id="051a0-173">0</span><span class="sxs-lookup"><span data-stu-id="051a0-173">0</span></span>                                                              |
| <span data-ttu-id="051a0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="051a0-174">Range-Upper</span></span>            | <span data-ttu-id="051a0-175">16</span><span class="sxs-lookup"><span data-stu-id="051a0-175">16</span></span>                                                             |
| <span data-ttu-id="051a0-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-176">Search-Flags</span></span>           | <span data-ttu-id="051a0-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="051a0-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="051a0-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-178">System-Flags</span></span>           | <span data-ttu-id="051a0-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="051a0-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="051a0-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="051a0-180">Classes used in</span></span>        | [<span data-ttu-id="051a0-181">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="051a0-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="051a0-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="051a0-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="051a0-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-183">Entry</span></span> | <span data-ttu-id="051a0-184">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="051a0-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="051a0-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="051a0-187">System-Only</span></span>            | <span data-ttu-id="051a0-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-188">False</span></span>                                                          |
| <span data-ttu-id="051a0-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="051a0-189">Is-Single-Valued</span></span>       | <span data-ttu-id="051a0-190">True</span><span class="sxs-lookup"><span data-stu-id="051a0-190">True</span></span>                                                           |
| <span data-ttu-id="051a0-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="051a0-191">Is Indexed</span></span>             | <span data-ttu-id="051a0-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-192">False</span></span>                                                          |
| <span data-ttu-id="051a0-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="051a0-193">In Global Catalog</span></span>      | <span data-ttu-id="051a0-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-194">False</span></span>                                                          |
| <span data-ttu-id="051a0-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="051a0-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="051a0-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="051a0-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="051a0-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="051a0-197">Range-Lower</span></span>            | <span data-ttu-id="051a0-198">0</span><span class="sxs-lookup"><span data-stu-id="051a0-198">0</span></span>                                                              |
| <span data-ttu-id="051a0-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="051a0-199">Range-Upper</span></span>            | <span data-ttu-id="051a0-200">16</span><span class="sxs-lookup"><span data-stu-id="051a0-200">16</span></span>                                                             |
| <span data-ttu-id="051a0-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-201">Search-Flags</span></span>           | <span data-ttu-id="051a0-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="051a0-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="051a0-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-203">System-Flags</span></span>           | <span data-ttu-id="051a0-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="051a0-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="051a0-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="051a0-205">Classes used in</span></span>        | [<span data-ttu-id="051a0-206">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="051a0-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="051a0-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="051a0-207">Windows Server 2008</span></span>



| <span data-ttu-id="051a0-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-208">Entry</span></span> | <span data-ttu-id="051a0-209">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="051a0-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="051a0-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="051a0-212">System-Only</span></span>            | <span data-ttu-id="051a0-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-213">False</span></span>                                                          |
| <span data-ttu-id="051a0-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="051a0-214">Is-Single-Valued</span></span>       | <span data-ttu-id="051a0-215">True</span><span class="sxs-lookup"><span data-stu-id="051a0-215">True</span></span>                                                           |
| <span data-ttu-id="051a0-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="051a0-216">Is Indexed</span></span>             | <span data-ttu-id="051a0-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-217">False</span></span>                                                          |
| <span data-ttu-id="051a0-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="051a0-218">In Global Catalog</span></span>      | <span data-ttu-id="051a0-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-219">False</span></span>                                                          |
| <span data-ttu-id="051a0-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="051a0-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="051a0-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="051a0-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="051a0-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="051a0-222">Range-Lower</span></span>            | <span data-ttu-id="051a0-223">0</span><span class="sxs-lookup"><span data-stu-id="051a0-223">0</span></span>                                                              |
| <span data-ttu-id="051a0-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="051a0-224">Range-Upper</span></span>            | <span data-ttu-id="051a0-225">16</span><span class="sxs-lookup"><span data-stu-id="051a0-225">16</span></span>                                                             |
| <span data-ttu-id="051a0-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-226">Search-Flags</span></span>           | <span data-ttu-id="051a0-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="051a0-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="051a0-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-228">System-Flags</span></span>           | <span data-ttu-id="051a0-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="051a0-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="051a0-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="051a0-230">Classes used in</span></span>        | [<span data-ttu-id="051a0-231">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="051a0-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="051a0-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="051a0-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="051a0-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-233">Entry</span></span> | <span data-ttu-id="051a0-234">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="051a0-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="051a0-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="051a0-237">System-Only</span></span>            | <span data-ttu-id="051a0-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-238">False</span></span>                                                          |
| <span data-ttu-id="051a0-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="051a0-239">Is-Single-Valued</span></span>       | <span data-ttu-id="051a0-240">True</span><span class="sxs-lookup"><span data-stu-id="051a0-240">True</span></span>                                                           |
| <span data-ttu-id="051a0-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="051a0-241">Is Indexed</span></span>             | <span data-ttu-id="051a0-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-242">False</span></span>                                                          |
| <span data-ttu-id="051a0-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="051a0-243">In Global Catalog</span></span>      | <span data-ttu-id="051a0-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-244">False</span></span>                                                          |
| <span data-ttu-id="051a0-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="051a0-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="051a0-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="051a0-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="051a0-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="051a0-247">Range-Lower</span></span>            | <span data-ttu-id="051a0-248">0</span><span class="sxs-lookup"><span data-stu-id="051a0-248">0</span></span>                                                              |
| <span data-ttu-id="051a0-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="051a0-249">Range-Upper</span></span>            | <span data-ttu-id="051a0-250">16</span><span class="sxs-lookup"><span data-stu-id="051a0-250">16</span></span>                                                             |
| <span data-ttu-id="051a0-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-251">Search-Flags</span></span>           | <span data-ttu-id="051a0-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="051a0-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="051a0-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-253">System-Flags</span></span>           | <span data-ttu-id="051a0-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="051a0-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="051a0-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="051a0-255">Classes used in</span></span>        | [<span data-ttu-id="051a0-256">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="051a0-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="051a0-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="051a0-257">Windows Server 2012</span></span>



| <span data-ttu-id="051a0-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="051a0-258">Entry</span></span> | <span data-ttu-id="051a0-259">Значение</span><span class="sxs-lookup"><span data-stu-id="051a0-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="051a0-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="051a0-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="051a0-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="051a0-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="051a0-262">System-Only</span></span>            | <span data-ttu-id="051a0-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-263">False</span></span>                                                          |
| <span data-ttu-id="051a0-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="051a0-264">Is-Single-Valued</span></span>       | <span data-ttu-id="051a0-265">True</span><span class="sxs-lookup"><span data-stu-id="051a0-265">True</span></span>                                                           |
| <span data-ttu-id="051a0-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="051a0-266">Is Indexed</span></span>             | <span data-ttu-id="051a0-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-267">False</span></span>                                                          |
| <span data-ttu-id="051a0-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="051a0-268">In Global Catalog</span></span>      | <span data-ttu-id="051a0-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="051a0-269">False</span></span>                                                          |
| <span data-ttu-id="051a0-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="051a0-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="051a0-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="051a0-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="051a0-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="051a0-272">Range-Lower</span></span>            | <span data-ttu-id="051a0-273">0</span><span class="sxs-lookup"><span data-stu-id="051a0-273">0</span></span>                                                              |
| <span data-ttu-id="051a0-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="051a0-274">Range-Upper</span></span>            | <span data-ttu-id="051a0-275">16</span><span class="sxs-lookup"><span data-stu-id="051a0-275">16</span></span>                                                             |
| <span data-ttu-id="051a0-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-276">Search-Flags</span></span>           | <span data-ttu-id="051a0-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="051a0-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="051a0-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="051a0-278">System-Flags</span></span>           | <span data-ttu-id="051a0-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="051a0-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="051a0-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="051a0-280">Classes used in</span></span>        | [<span data-ttu-id="051a0-281">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="051a0-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





