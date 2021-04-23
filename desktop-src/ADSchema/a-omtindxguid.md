---
title: Атрибут ОМТ-Индкс-GUID
description: Идентификатор индекса для записи таблицы Link-Track-Object-Move.
ms.assetid: a426512e-ab9f-4938-a767-7fed83aa755c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ОМТ-Индкс-GUID
- Схема AD атрибута Омтиндксгуид
topic_type:
- apiref
api_name:
- OMT-Indx-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a8a8dd42262a71b7ee09a39dac5cd59b90dfb9a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893334"
---
# <a name="omt-indx-guid-attribute"></a><span data-ttu-id="45985-105">Атрибут ОМТ-Индкс-GUID</span><span class="sxs-lookup"><span data-stu-id="45985-105">OMT-Indx-Guid attribute</span></span>

<span data-ttu-id="45985-106">Идентификатор индекса для записи таблицы Link-Track-Object-Move.</span><span class="sxs-lookup"><span data-stu-id="45985-106">The index identifier for a Link-Track-Object-Move table entry.</span></span>



| <span data-ttu-id="45985-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-107">Entry</span></span> | <span data-ttu-id="45985-108">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="45985-109">CN</span><span class="sxs-lookup"><span data-stu-id="45985-109">CN</span></span>                | <span data-ttu-id="45985-110">ОМТ-Индкс-GUID</span><span class="sxs-lookup"><span data-stu-id="45985-110">OMT-Indx-Guid</span></span>                                         |
| <span data-ttu-id="45985-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="45985-111">Ldap-Display-Name</span></span> | <span data-ttu-id="45985-112">омтиндксгуид</span><span class="sxs-lookup"><span data-stu-id="45985-112">oMTIndxGuid</span></span>                                           |
| <span data-ttu-id="45985-113">Размер</span><span class="sxs-lookup"><span data-stu-id="45985-113">Size</span></span>              | <span data-ttu-id="45985-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="45985-114">16 bytes</span></span>                                              |
| <span data-ttu-id="45985-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="45985-115">Update Privilege</span></span>  | <span data-ttu-id="45985-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="45985-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="45985-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="45985-117">Update Frequency</span></span>  | <span data-ttu-id="45985-118">При каждом изменении ссылки на файл.</span><span class="sxs-lookup"><span data-stu-id="45985-118">Whenever the link for a file changes.</span></span>                 |
| <span data-ttu-id="45985-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="45985-119">Attribute-Id</span></span>      | <span data-ttu-id="45985-120">1.2.840.113556.1.4.333</span><span class="sxs-lookup"><span data-stu-id="45985-120">1.2.840.113556.1.4.333</span></span>                                |
| <span data-ttu-id="45985-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="45985-121">System-Id-Guid</span></span>    | <span data-ttu-id="45985-122">1f0075fa-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="45985-122">1f0075fa-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="45985-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45985-123">Syntax</span></span>            | [<span data-ttu-id="45985-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="45985-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="45985-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="45985-125">Implementations</span></span>

-   [<span data-ttu-id="45985-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="45985-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="45985-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="45985-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="45985-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="45985-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="45985-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="45985-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="45985-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="45985-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="45985-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="45985-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="45985-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45985-132">Windows 2000 Server</span></span>



| <span data-ttu-id="45985-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-133">Entry</span></span> | <span data-ttu-id="45985-134">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="45985-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45985-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45985-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="45985-137">System-Only</span></span>            | <span data-ttu-id="45985-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-138">False</span></span>                                                          |
| <span data-ttu-id="45985-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45985-139">Is-Single-Valued</span></span>       | <span data-ttu-id="45985-140">True</span><span class="sxs-lookup"><span data-stu-id="45985-140">True</span></span>                                                           |
| <span data-ttu-id="45985-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45985-141">Is Indexed</span></span>             | <span data-ttu-id="45985-142">True</span><span class="sxs-lookup"><span data-stu-id="45985-142">True</span></span>                                                           |
| <span data-ttu-id="45985-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45985-143">In Global Catalog</span></span>      | <span data-ttu-id="45985-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-144">False</span></span>                                                          |
| <span data-ttu-id="45985-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45985-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="45985-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45985-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="45985-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45985-147">Range-Lower</span></span>            | <span data-ttu-id="45985-148">0</span><span class="sxs-lookup"><span data-stu-id="45985-148">0</span></span>                                                              |
| <span data-ttu-id="45985-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45985-149">Range-Upper</span></span>            | <span data-ttu-id="45985-150">16</span><span class="sxs-lookup"><span data-stu-id="45985-150">16</span></span>                                                             |
| <span data-ttu-id="45985-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-151">Search-Flags</span></span>           | <span data-ttu-id="45985-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45985-152">0x00000001</span></span>                                                     |
| <span data-ttu-id="45985-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-153">System-Flags</span></span>           | <span data-ttu-id="45985-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45985-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="45985-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45985-155">Classes used in</span></span>        | [<span data-ttu-id="45985-156">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="45985-156">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="45985-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45985-157">Windows Server 2003</span></span>



| <span data-ttu-id="45985-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-158">Entry</span></span> | <span data-ttu-id="45985-159">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="45985-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45985-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45985-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="45985-162">System-Only</span></span>            | <span data-ttu-id="45985-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-163">False</span></span>                                                          |
| <span data-ttu-id="45985-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45985-164">Is-Single-Valued</span></span>       | <span data-ttu-id="45985-165">True</span><span class="sxs-lookup"><span data-stu-id="45985-165">True</span></span>                                                           |
| <span data-ttu-id="45985-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45985-166">Is Indexed</span></span>             | <span data-ttu-id="45985-167">True</span><span class="sxs-lookup"><span data-stu-id="45985-167">True</span></span>                                                           |
| <span data-ttu-id="45985-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45985-168">In Global Catalog</span></span>      | <span data-ttu-id="45985-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-169">False</span></span>                                                          |
| <span data-ttu-id="45985-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45985-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="45985-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45985-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="45985-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45985-172">Range-Lower</span></span>            | <span data-ttu-id="45985-173">0</span><span class="sxs-lookup"><span data-stu-id="45985-173">0</span></span>                                                              |
| <span data-ttu-id="45985-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45985-174">Range-Upper</span></span>            | <span data-ttu-id="45985-175">16</span><span class="sxs-lookup"><span data-stu-id="45985-175">16</span></span>                                                             |
| <span data-ttu-id="45985-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-176">Search-Flags</span></span>           | <span data-ttu-id="45985-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45985-177">0x00000001</span></span>                                                     |
| <span data-ttu-id="45985-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-178">System-Flags</span></span>           | <span data-ttu-id="45985-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45985-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="45985-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45985-180">Classes used in</span></span>        | [<span data-ttu-id="45985-181">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="45985-181">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="45985-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="45985-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="45985-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-183">Entry</span></span> | <span data-ttu-id="45985-184">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="45985-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45985-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45985-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="45985-187">System-Only</span></span>            | <span data-ttu-id="45985-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-188">False</span></span>                                                          |
| <span data-ttu-id="45985-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45985-189">Is-Single-Valued</span></span>       | <span data-ttu-id="45985-190">True</span><span class="sxs-lookup"><span data-stu-id="45985-190">True</span></span>                                                           |
| <span data-ttu-id="45985-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45985-191">Is Indexed</span></span>             | <span data-ttu-id="45985-192">True</span><span class="sxs-lookup"><span data-stu-id="45985-192">True</span></span>                                                           |
| <span data-ttu-id="45985-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45985-193">In Global Catalog</span></span>      | <span data-ttu-id="45985-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-194">False</span></span>                                                          |
| <span data-ttu-id="45985-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45985-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="45985-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45985-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="45985-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45985-197">Range-Lower</span></span>            | <span data-ttu-id="45985-198">0</span><span class="sxs-lookup"><span data-stu-id="45985-198">0</span></span>                                                              |
| <span data-ttu-id="45985-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45985-199">Range-Upper</span></span>            | <span data-ttu-id="45985-200">16</span><span class="sxs-lookup"><span data-stu-id="45985-200">16</span></span>                                                             |
| <span data-ttu-id="45985-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-201">Search-Flags</span></span>           | <span data-ttu-id="45985-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45985-202">0x00000001</span></span>                                                     |
| <span data-ttu-id="45985-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-203">System-Flags</span></span>           | <span data-ttu-id="45985-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45985-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="45985-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45985-205">Classes used in</span></span>        | [<span data-ttu-id="45985-206">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="45985-206">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="45985-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45985-207">Windows Server 2008</span></span>



| <span data-ttu-id="45985-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-208">Entry</span></span> | <span data-ttu-id="45985-209">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="45985-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45985-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45985-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="45985-212">System-Only</span></span>            | <span data-ttu-id="45985-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-213">False</span></span>                                                          |
| <span data-ttu-id="45985-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45985-214">Is-Single-Valued</span></span>       | <span data-ttu-id="45985-215">True</span><span class="sxs-lookup"><span data-stu-id="45985-215">True</span></span>                                                           |
| <span data-ttu-id="45985-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45985-216">Is Indexed</span></span>             | <span data-ttu-id="45985-217">True</span><span class="sxs-lookup"><span data-stu-id="45985-217">True</span></span>                                                           |
| <span data-ttu-id="45985-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45985-218">In Global Catalog</span></span>      | <span data-ttu-id="45985-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-219">False</span></span>                                                          |
| <span data-ttu-id="45985-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45985-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="45985-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45985-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="45985-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45985-222">Range-Lower</span></span>            | <span data-ttu-id="45985-223">0</span><span class="sxs-lookup"><span data-stu-id="45985-223">0</span></span>                                                              |
| <span data-ttu-id="45985-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45985-224">Range-Upper</span></span>            | <span data-ttu-id="45985-225">16</span><span class="sxs-lookup"><span data-stu-id="45985-225">16</span></span>                                                             |
| <span data-ttu-id="45985-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-226">Search-Flags</span></span>           | <span data-ttu-id="45985-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45985-227">0x00000001</span></span>                                                     |
| <span data-ttu-id="45985-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-228">System-Flags</span></span>           | <span data-ttu-id="45985-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45985-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="45985-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45985-230">Classes used in</span></span>        | [<span data-ttu-id="45985-231">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="45985-231">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="45985-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45985-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="45985-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-233">Entry</span></span> | <span data-ttu-id="45985-234">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="45985-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45985-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45985-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="45985-237">System-Only</span></span>            | <span data-ttu-id="45985-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-238">False</span></span>                                                          |
| <span data-ttu-id="45985-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45985-239">Is-Single-Valued</span></span>       | <span data-ttu-id="45985-240">True</span><span class="sxs-lookup"><span data-stu-id="45985-240">True</span></span>                                                           |
| <span data-ttu-id="45985-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45985-241">Is Indexed</span></span>             | <span data-ttu-id="45985-242">True</span><span class="sxs-lookup"><span data-stu-id="45985-242">True</span></span>                                                           |
| <span data-ttu-id="45985-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45985-243">In Global Catalog</span></span>      | <span data-ttu-id="45985-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-244">False</span></span>                                                          |
| <span data-ttu-id="45985-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45985-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="45985-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45985-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="45985-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45985-247">Range-Lower</span></span>            | <span data-ttu-id="45985-248">0</span><span class="sxs-lookup"><span data-stu-id="45985-248">0</span></span>                                                              |
| <span data-ttu-id="45985-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45985-249">Range-Upper</span></span>            | <span data-ttu-id="45985-250">16</span><span class="sxs-lookup"><span data-stu-id="45985-250">16</span></span>                                                             |
| <span data-ttu-id="45985-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-251">Search-Flags</span></span>           | <span data-ttu-id="45985-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45985-252">0x00000001</span></span>                                                     |
| <span data-ttu-id="45985-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-253">System-Flags</span></span>           | <span data-ttu-id="45985-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45985-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="45985-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45985-255">Classes used in</span></span>        | [<span data-ttu-id="45985-256">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="45985-256">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="45985-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45985-257">Windows Server 2012</span></span>



| <span data-ttu-id="45985-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="45985-258">Entry</span></span> | <span data-ttu-id="45985-259">Значение</span><span class="sxs-lookup"><span data-stu-id="45985-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="45985-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45985-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45985-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="45985-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="45985-262">System-Only</span></span>            | <span data-ttu-id="45985-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-263">False</span></span>                                                          |
| <span data-ttu-id="45985-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45985-264">Is-Single-Valued</span></span>       | <span data-ttu-id="45985-265">True</span><span class="sxs-lookup"><span data-stu-id="45985-265">True</span></span>                                                           |
| <span data-ttu-id="45985-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45985-266">Is Indexed</span></span>             | <span data-ttu-id="45985-267">True</span><span class="sxs-lookup"><span data-stu-id="45985-267">True</span></span>                                                           |
| <span data-ttu-id="45985-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45985-268">In Global Catalog</span></span>      | <span data-ttu-id="45985-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="45985-269">False</span></span>                                                          |
| <span data-ttu-id="45985-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45985-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="45985-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45985-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="45985-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45985-272">Range-Lower</span></span>            | <span data-ttu-id="45985-273">0</span><span class="sxs-lookup"><span data-stu-id="45985-273">0</span></span>                                                              |
| <span data-ttu-id="45985-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45985-274">Range-Upper</span></span>            | <span data-ttu-id="45985-275">16</span><span class="sxs-lookup"><span data-stu-id="45985-275">16</span></span>                                                             |
| <span data-ttu-id="45985-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-276">Search-Flags</span></span>           | <span data-ttu-id="45985-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45985-277">0x00000001</span></span>                                                     |
| <span data-ttu-id="45985-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45985-278">System-Flags</span></span>           | <span data-ttu-id="45985-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45985-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="45985-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45985-280">Classes used in</span></span>        | [<span data-ttu-id="45985-281">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="45985-281">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



 

 





