---
title: Атрибут OMT-Guid
description: Уникальный идентификатор для записи ссылки-Track-Object-Move.
ms.assetid: c8266178-4d0d-46d6-8fd9-d0c11c11c036
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута OMT-Guid
- Схема AD атрибута Омтгуид
topic_type:
- apiref
api_name:
- OMT-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379cdf49a6ee1a467a0e5120e841e4d2179447be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655325"
---
# <a name="omt-guid-attribute"></a><span data-ttu-id="44ba7-105">Атрибут OMT-Guid</span><span class="sxs-lookup"><span data-stu-id="44ba7-105">OMT-Guid attribute</span></span>

<span data-ttu-id="44ba7-106">Уникальный идентификатор для записи ссылки-Track-Object-Move.</span><span class="sxs-lookup"><span data-stu-id="44ba7-106">The unique identifier for a Link-Track-Object-Move table entry.</span></span>



| <span data-ttu-id="44ba7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-107">Entry</span></span> | <span data-ttu-id="44ba7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="44ba7-109">CN</span><span class="sxs-lookup"><span data-stu-id="44ba7-109">CN</span></span>                | <span data-ttu-id="44ba7-110">OMT-Guid</span><span class="sxs-lookup"><span data-stu-id="44ba7-110">OMT-Guid</span></span>                                              |
| <span data-ttu-id="44ba7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="44ba7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="44ba7-112">омтгуид</span><span class="sxs-lookup"><span data-stu-id="44ba7-112">oMTGuid</span></span>                                               |
| <span data-ttu-id="44ba7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="44ba7-113">Size</span></span>              | <span data-ttu-id="44ba7-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="44ba7-114">16 bytes</span></span>                                              |
| <span data-ttu-id="44ba7-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="44ba7-115">Update Privilege</span></span>  | <span data-ttu-id="44ba7-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="44ba7-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="44ba7-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="44ba7-117">Update Frequency</span></span>  | <span data-ttu-id="44ba7-118">При каждом изменении ссылки на файл.</span><span class="sxs-lookup"><span data-stu-id="44ba7-118">Whenever the link for a file changes.</span></span>                 |
| <span data-ttu-id="44ba7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-119">Attribute-Id</span></span>      | <span data-ttu-id="44ba7-120">1.2.840.113556.1.4.505</span><span class="sxs-lookup"><span data-stu-id="44ba7-120">1.2.840.113556.1.4.505</span></span>                                |
| <span data-ttu-id="44ba7-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="44ba7-121">System-Id-Guid</span></span>    | <span data-ttu-id="44ba7-122">ddac0cf3-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="44ba7-122">ddac0cf3-af8f-11d0-afeb-00c04fd930c9</span></span>                  |
| <span data-ttu-id="44ba7-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44ba7-123">Syntax</span></span>            | [<span data-ttu-id="44ba7-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="44ba7-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="44ba7-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="44ba7-125">Implementations</span></span>

-   [<span data-ttu-id="44ba7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="44ba7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="44ba7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="44ba7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="44ba7-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="44ba7-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="44ba7-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="44ba7-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="44ba7-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="44ba7-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="44ba7-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="44ba7-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="44ba7-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44ba7-132">Windows 2000 Server</span></span>



| <span data-ttu-id="44ba7-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-133">Entry</span></span> | <span data-ttu-id="44ba7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44ba7-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44ba7-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="44ba7-137">System-Only</span></span>            | <span data-ttu-id="44ba7-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-138">False</span></span>                                                          |
| <span data-ttu-id="44ba7-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44ba7-139">Is-Single-Valued</span></span>       | <span data-ttu-id="44ba7-140">True</span><span class="sxs-lookup"><span data-stu-id="44ba7-140">True</span></span>                                                           |
| <span data-ttu-id="44ba7-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44ba7-141">Is Indexed</span></span>             | <span data-ttu-id="44ba7-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-142">False</span></span>                                                          |
| <span data-ttu-id="44ba7-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44ba7-143">In Global Catalog</span></span>      | <span data-ttu-id="44ba7-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-144">False</span></span>                                                          |
| <span data-ttu-id="44ba7-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44ba7-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="44ba7-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44ba7-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="44ba7-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44ba7-147">Range-Lower</span></span>            | <span data-ttu-id="44ba7-148">0</span><span class="sxs-lookup"><span data-stu-id="44ba7-148">0</span></span>                                                              |
| <span data-ttu-id="44ba7-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44ba7-149">Range-Upper</span></span>            | <span data-ttu-id="44ba7-150">16</span><span class="sxs-lookup"><span data-stu-id="44ba7-150">16</span></span>                                                             |
| <span data-ttu-id="44ba7-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-151">Search-Flags</span></span>           | <span data-ttu-id="44ba7-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44ba7-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="44ba7-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-153">System-Flags</span></span>           | <span data-ttu-id="44ba7-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44ba7-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="44ba7-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44ba7-155">Classes used in</span></span>        | [<span data-ttu-id="44ba7-156">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="44ba7-156">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="44ba7-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44ba7-157">Windows Server 2003</span></span>



| <span data-ttu-id="44ba7-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-158">Entry</span></span> | <span data-ttu-id="44ba7-159">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44ba7-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44ba7-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="44ba7-162">System-Only</span></span>            | <span data-ttu-id="44ba7-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-163">False</span></span>                                                          |
| <span data-ttu-id="44ba7-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44ba7-164">Is-Single-Valued</span></span>       | <span data-ttu-id="44ba7-165">True</span><span class="sxs-lookup"><span data-stu-id="44ba7-165">True</span></span>                                                           |
| <span data-ttu-id="44ba7-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44ba7-166">Is Indexed</span></span>             | <span data-ttu-id="44ba7-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-167">False</span></span>                                                          |
| <span data-ttu-id="44ba7-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44ba7-168">In Global Catalog</span></span>      | <span data-ttu-id="44ba7-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-169">False</span></span>                                                          |
| <span data-ttu-id="44ba7-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44ba7-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="44ba7-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44ba7-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="44ba7-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44ba7-172">Range-Lower</span></span>            | <span data-ttu-id="44ba7-173">0</span><span class="sxs-lookup"><span data-stu-id="44ba7-173">0</span></span>                                                              |
| <span data-ttu-id="44ba7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44ba7-174">Range-Upper</span></span>            | <span data-ttu-id="44ba7-175">16</span><span class="sxs-lookup"><span data-stu-id="44ba7-175">16</span></span>                                                             |
| <span data-ttu-id="44ba7-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-176">Search-Flags</span></span>           | <span data-ttu-id="44ba7-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44ba7-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="44ba7-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-178">System-Flags</span></span>           | <span data-ttu-id="44ba7-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44ba7-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="44ba7-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44ba7-180">Classes used in</span></span>        | [<span data-ttu-id="44ba7-181">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="44ba7-181">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="44ba7-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="44ba7-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="44ba7-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-183">Entry</span></span> | <span data-ttu-id="44ba7-184">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44ba7-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44ba7-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="44ba7-187">System-Only</span></span>            | <span data-ttu-id="44ba7-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-188">False</span></span>                                                          |
| <span data-ttu-id="44ba7-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44ba7-189">Is-Single-Valued</span></span>       | <span data-ttu-id="44ba7-190">True</span><span class="sxs-lookup"><span data-stu-id="44ba7-190">True</span></span>                                                           |
| <span data-ttu-id="44ba7-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44ba7-191">Is Indexed</span></span>             | <span data-ttu-id="44ba7-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-192">False</span></span>                                                          |
| <span data-ttu-id="44ba7-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44ba7-193">In Global Catalog</span></span>      | <span data-ttu-id="44ba7-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-194">False</span></span>                                                          |
| <span data-ttu-id="44ba7-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44ba7-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="44ba7-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44ba7-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="44ba7-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44ba7-197">Range-Lower</span></span>            | <span data-ttu-id="44ba7-198">0</span><span class="sxs-lookup"><span data-stu-id="44ba7-198">0</span></span>                                                              |
| <span data-ttu-id="44ba7-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44ba7-199">Range-Upper</span></span>            | <span data-ttu-id="44ba7-200">16</span><span class="sxs-lookup"><span data-stu-id="44ba7-200">16</span></span>                                                             |
| <span data-ttu-id="44ba7-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-201">Search-Flags</span></span>           | <span data-ttu-id="44ba7-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44ba7-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="44ba7-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-203">System-Flags</span></span>           | <span data-ttu-id="44ba7-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44ba7-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="44ba7-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44ba7-205">Classes used in</span></span>        | [<span data-ttu-id="44ba7-206">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="44ba7-206">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="44ba7-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44ba7-207">Windows Server 2008</span></span>



| <span data-ttu-id="44ba7-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-208">Entry</span></span> | <span data-ttu-id="44ba7-209">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44ba7-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44ba7-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="44ba7-212">System-Only</span></span>            | <span data-ttu-id="44ba7-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-213">False</span></span>                                                          |
| <span data-ttu-id="44ba7-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44ba7-214">Is-Single-Valued</span></span>       | <span data-ttu-id="44ba7-215">True</span><span class="sxs-lookup"><span data-stu-id="44ba7-215">True</span></span>                                                           |
| <span data-ttu-id="44ba7-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44ba7-216">Is Indexed</span></span>             | <span data-ttu-id="44ba7-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-217">False</span></span>                                                          |
| <span data-ttu-id="44ba7-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44ba7-218">In Global Catalog</span></span>      | <span data-ttu-id="44ba7-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-219">False</span></span>                                                          |
| <span data-ttu-id="44ba7-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44ba7-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="44ba7-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44ba7-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="44ba7-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44ba7-222">Range-Lower</span></span>            | <span data-ttu-id="44ba7-223">0</span><span class="sxs-lookup"><span data-stu-id="44ba7-223">0</span></span>                                                              |
| <span data-ttu-id="44ba7-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44ba7-224">Range-Upper</span></span>            | <span data-ttu-id="44ba7-225">16</span><span class="sxs-lookup"><span data-stu-id="44ba7-225">16</span></span>                                                             |
| <span data-ttu-id="44ba7-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-226">Search-Flags</span></span>           | <span data-ttu-id="44ba7-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44ba7-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="44ba7-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-228">System-Flags</span></span>           | <span data-ttu-id="44ba7-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44ba7-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="44ba7-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44ba7-230">Classes used in</span></span>        | [<span data-ttu-id="44ba7-231">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="44ba7-231">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="44ba7-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="44ba7-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="44ba7-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-233">Entry</span></span> | <span data-ttu-id="44ba7-234">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44ba7-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44ba7-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="44ba7-237">System-Only</span></span>            | <span data-ttu-id="44ba7-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-238">False</span></span>                                                          |
| <span data-ttu-id="44ba7-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44ba7-239">Is-Single-Valued</span></span>       | <span data-ttu-id="44ba7-240">True</span><span class="sxs-lookup"><span data-stu-id="44ba7-240">True</span></span>                                                           |
| <span data-ttu-id="44ba7-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44ba7-241">Is Indexed</span></span>             | <span data-ttu-id="44ba7-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-242">False</span></span>                                                          |
| <span data-ttu-id="44ba7-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44ba7-243">In Global Catalog</span></span>      | <span data-ttu-id="44ba7-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-244">False</span></span>                                                          |
| <span data-ttu-id="44ba7-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44ba7-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="44ba7-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44ba7-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="44ba7-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44ba7-247">Range-Lower</span></span>            | <span data-ttu-id="44ba7-248">0</span><span class="sxs-lookup"><span data-stu-id="44ba7-248">0</span></span>                                                              |
| <span data-ttu-id="44ba7-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44ba7-249">Range-Upper</span></span>            | <span data-ttu-id="44ba7-250">16</span><span class="sxs-lookup"><span data-stu-id="44ba7-250">16</span></span>                                                             |
| <span data-ttu-id="44ba7-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-251">Search-Flags</span></span>           | <span data-ttu-id="44ba7-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44ba7-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="44ba7-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-253">System-Flags</span></span>           | <span data-ttu-id="44ba7-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44ba7-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="44ba7-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44ba7-255">Classes used in</span></span>        | [<span data-ttu-id="44ba7-256">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="44ba7-256">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="44ba7-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44ba7-257">Windows Server 2012</span></span>



| <span data-ttu-id="44ba7-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="44ba7-258">Entry</span></span> | <span data-ttu-id="44ba7-259">Значение</span><span class="sxs-lookup"><span data-stu-id="44ba7-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44ba7-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44ba7-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44ba7-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="44ba7-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="44ba7-262">System-Only</span></span>            | <span data-ttu-id="44ba7-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-263">False</span></span>                                                          |
| <span data-ttu-id="44ba7-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44ba7-264">Is-Single-Valued</span></span>       | <span data-ttu-id="44ba7-265">True</span><span class="sxs-lookup"><span data-stu-id="44ba7-265">True</span></span>                                                           |
| <span data-ttu-id="44ba7-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44ba7-266">Is Indexed</span></span>             | <span data-ttu-id="44ba7-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-267">False</span></span>                                                          |
| <span data-ttu-id="44ba7-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44ba7-268">In Global Catalog</span></span>      | <span data-ttu-id="44ba7-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="44ba7-269">False</span></span>                                                          |
| <span data-ttu-id="44ba7-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44ba7-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="44ba7-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44ba7-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="44ba7-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44ba7-272">Range-Lower</span></span>            | <span data-ttu-id="44ba7-273">0</span><span class="sxs-lookup"><span data-stu-id="44ba7-273">0</span></span>                                                              |
| <span data-ttu-id="44ba7-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44ba7-274">Range-Upper</span></span>            | <span data-ttu-id="44ba7-275">16</span><span class="sxs-lookup"><span data-stu-id="44ba7-275">16</span></span>                                                             |
| <span data-ttu-id="44ba7-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-276">Search-Flags</span></span>           | <span data-ttu-id="44ba7-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44ba7-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="44ba7-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44ba7-278">System-Flags</span></span>           | <span data-ttu-id="44ba7-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44ba7-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="44ba7-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44ba7-280">Classes used in</span></span>        | [<span data-ttu-id="44ba7-281">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="44ba7-281">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



 

 





