---
title: Атрибут Object-Count
description: Квота на записанные файлы для заданного тома.
ms.assetid: 22900e97-d3d3-49cc-a2c3-1f557fe383b1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Count
- Схема AD атрибута objectCount
topic_type:
- apiref
api_name:
- Object-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9a93f4f84a9fb01922659bddd6b9fc1982e58e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893338"
---
# <a name="object-count-attribute"></a><span data-ttu-id="5d1b0-105">Атрибут Object-Count</span><span class="sxs-lookup"><span data-stu-id="5d1b0-105">Object-Count attribute</span></span>

<span data-ttu-id="5d1b0-106">Квота на записанные файлы для заданного тома.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-106">Tracked file quota for a given volume.</span></span>



| <span data-ttu-id="5d1b0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-107">Entry</span></span> | <span data-ttu-id="5d1b0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5d1b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="5d1b0-109">CN</span></span>                | <span data-ttu-id="5d1b0-110">Object-Count</span><span class="sxs-lookup"><span data-stu-id="5d1b0-110">Object-Count</span></span>                         |
| <span data-ttu-id="5d1b0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5d1b0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5d1b0-112">objectCount</span><span class="sxs-lookup"><span data-stu-id="5d1b0-112">objectCount</span></span>                          |
| <span data-ttu-id="5d1b0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5d1b0-113">Size</span></span>              | <span data-ttu-id="5d1b0-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="5d1b0-114">4 bytes</span></span>                              |
| <span data-ttu-id="5d1b0-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5d1b0-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5d1b0-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5d1b0-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5d1b0-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-117">Attribute-Id</span></span>      | <span data-ttu-id="5d1b0-118">1.2.840.113556.1.4.506</span><span class="sxs-lookup"><span data-stu-id="5d1b0-118">1.2.840.113556.1.4.506</span></span>               |
| <span data-ttu-id="5d1b0-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5d1b0-119">System-Id-Guid</span></span>    | <span data-ttu-id="5d1b0-120">34aaa216-b699-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5d1b0-120">34aaa216-b699-11d0-afee-0000f80367c1</span></span> |
| <span data-ttu-id="5d1b0-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d1b0-121">Syntax</span></span>            | [<span data-ttu-id="5d1b0-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="5d1b0-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5d1b0-123">Implementations</span></span>

-   [<span data-ttu-id="5d1b0-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5d1b0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d1b0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d1b0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d1b0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d1b0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5d1b0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d1b0-130">Windows 2000 Server</span></span>



| <span data-ttu-id="5d1b0-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-131">Entry</span></span> | <span data-ttu-id="5d1b0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-132">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5d1b0-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d1b0-133">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-134">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d1b0-135">System-Only</span></span>            | <span data-ttu-id="5d1b0-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-136">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d1b0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5d1b0-138">True</span><span class="sxs-lookup"><span data-stu-id="5d1b0-138">True</span></span>                                                           |
| <span data-ttu-id="5d1b0-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d1b0-139">Is Indexed</span></span>             | <span data-ttu-id="5d1b0-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-140">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d1b0-141">In Global Catalog</span></span>      | <span data-ttu-id="5d1b0-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-142">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d1b0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d1b0-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d1b0-144">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="5d1b0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d1b0-145">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d1b0-146">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-147">Search-Flags</span></span>           | <span data-ttu-id="5d1b0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d1b0-148">0x00000000</span></span>                                                     |
| <span data-ttu-id="5d1b0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-149">System-Flags</span></span>           | <span data-ttu-id="5d1b0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d1b0-150">0x00000010</span></span>                                                     |
| <span data-ttu-id="5d1b0-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d1b0-151">Classes used in</span></span>        | [<span data-ttu-id="5d1b0-152">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-152">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5d1b0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d1b0-153">Windows Server 2003</span></span>



| <span data-ttu-id="5d1b0-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-154">Entry</span></span> | <span data-ttu-id="5d1b0-155">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-155">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5d1b0-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d1b0-156">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-157">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d1b0-158">System-Only</span></span>            | <span data-ttu-id="5d1b0-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-159">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d1b0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5d1b0-161">True</span><span class="sxs-lookup"><span data-stu-id="5d1b0-161">True</span></span>                                                           |
| <span data-ttu-id="5d1b0-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d1b0-162">Is Indexed</span></span>             | <span data-ttu-id="5d1b0-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-163">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d1b0-164">In Global Catalog</span></span>      | <span data-ttu-id="5d1b0-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-165">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d1b0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d1b0-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d1b0-167">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="5d1b0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d1b0-168">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d1b0-169">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-170">Search-Flags</span></span>           | <span data-ttu-id="5d1b0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d1b0-171">0x00000000</span></span>                                                     |
| <span data-ttu-id="5d1b0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-172">System-Flags</span></span>           | <span data-ttu-id="5d1b0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d1b0-173">0x00000010</span></span>                                                     |
| <span data-ttu-id="5d1b0-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d1b0-174">Classes used in</span></span>        | [<span data-ttu-id="5d1b0-175">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-175">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d1b0-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d1b0-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d1b0-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-177">Entry</span></span> | <span data-ttu-id="5d1b0-178">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-178">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5d1b0-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d1b0-179">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-180">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d1b0-181">System-Only</span></span>            | <span data-ttu-id="5d1b0-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-182">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d1b0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5d1b0-184">True</span><span class="sxs-lookup"><span data-stu-id="5d1b0-184">True</span></span>                                                           |
| <span data-ttu-id="5d1b0-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d1b0-185">Is Indexed</span></span>             | <span data-ttu-id="5d1b0-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-186">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d1b0-187">In Global Catalog</span></span>      | <span data-ttu-id="5d1b0-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-188">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d1b0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d1b0-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d1b0-190">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="5d1b0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d1b0-191">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d1b0-192">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-193">Search-Flags</span></span>           | <span data-ttu-id="5d1b0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d1b0-194">0x00000000</span></span>                                                     |
| <span data-ttu-id="5d1b0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-195">System-Flags</span></span>           | <span data-ttu-id="5d1b0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d1b0-196">0x00000010</span></span>                                                     |
| <span data-ttu-id="5d1b0-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d1b0-197">Classes used in</span></span>        | [<span data-ttu-id="5d1b0-198">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-198">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d1b0-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d1b0-199">Windows Server 2008</span></span>



| <span data-ttu-id="5d1b0-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-200">Entry</span></span> | <span data-ttu-id="5d1b0-201">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-201">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5d1b0-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d1b0-202">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-203">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d1b0-204">System-Only</span></span>            | <span data-ttu-id="5d1b0-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-205">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d1b0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5d1b0-207">True</span><span class="sxs-lookup"><span data-stu-id="5d1b0-207">True</span></span>                                                           |
| <span data-ttu-id="5d1b0-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d1b0-208">Is Indexed</span></span>             | <span data-ttu-id="5d1b0-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-209">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d1b0-210">In Global Catalog</span></span>      | <span data-ttu-id="5d1b0-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-211">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d1b0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d1b0-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d1b0-213">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="5d1b0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d1b0-214">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d1b0-215">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-216">Search-Flags</span></span>           | <span data-ttu-id="5d1b0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d1b0-217">0x00000000</span></span>                                                     |
| <span data-ttu-id="5d1b0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-218">System-Flags</span></span>           | <span data-ttu-id="5d1b0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d1b0-219">0x00000010</span></span>                                                     |
| <span data-ttu-id="5d1b0-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d1b0-220">Classes used in</span></span>        | [<span data-ttu-id="5d1b0-221">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-221">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d1b0-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d1b0-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d1b0-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-223">Entry</span></span> | <span data-ttu-id="5d1b0-224">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-224">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5d1b0-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d1b0-225">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-226">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d1b0-227">System-Only</span></span>            | <span data-ttu-id="5d1b0-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-228">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d1b0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5d1b0-230">True</span><span class="sxs-lookup"><span data-stu-id="5d1b0-230">True</span></span>                                                           |
| <span data-ttu-id="5d1b0-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d1b0-231">Is Indexed</span></span>             | <span data-ttu-id="5d1b0-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-232">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d1b0-233">In Global Catalog</span></span>      | <span data-ttu-id="5d1b0-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-234">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d1b0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d1b0-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d1b0-236">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="5d1b0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d1b0-237">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d1b0-238">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-239">Search-Flags</span></span>           | <span data-ttu-id="5d1b0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d1b0-240">0x00000000</span></span>                                                     |
| <span data-ttu-id="5d1b0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-241">System-Flags</span></span>           | <span data-ttu-id="5d1b0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d1b0-242">0x00000010</span></span>                                                     |
| <span data-ttu-id="5d1b0-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d1b0-243">Classes used in</span></span>        | [<span data-ttu-id="5d1b0-244">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-244">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d1b0-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d1b0-245">Windows Server 2012</span></span>



| <span data-ttu-id="5d1b0-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d1b0-246">Entry</span></span> | <span data-ttu-id="5d1b0-247">Значение</span><span class="sxs-lookup"><span data-stu-id="5d1b0-247">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5d1b0-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d1b0-248">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d1b0-249">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="5d1b0-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d1b0-250">System-Only</span></span>            | <span data-ttu-id="5d1b0-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-251">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d1b0-252">Is-Single-Valued</span></span>       | <span data-ttu-id="5d1b0-253">True</span><span class="sxs-lookup"><span data-stu-id="5d1b0-253">True</span></span>                                                           |
| <span data-ttu-id="5d1b0-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d1b0-254">Is Indexed</span></span>             | <span data-ttu-id="5d1b0-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-255">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d1b0-256">In Global Catalog</span></span>      | <span data-ttu-id="5d1b0-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d1b0-257">False</span></span>                                                          |
| <span data-ttu-id="5d1b0-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d1b0-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d1b0-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d1b0-259">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="5d1b0-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d1b0-260">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d1b0-261">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="5d1b0-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-262">Search-Flags</span></span>           | <span data-ttu-id="5d1b0-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d1b0-263">0x00000000</span></span>                                                     |
| <span data-ttu-id="5d1b0-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d1b0-264">System-Flags</span></span>           | <span data-ttu-id="5d1b0-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d1b0-265">0x00000010</span></span>                                                     |
| <span data-ttu-id="5d1b0-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d1b0-266">Classes used in</span></span>        | [<span data-ttu-id="5d1b0-267">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="5d1b0-267">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





