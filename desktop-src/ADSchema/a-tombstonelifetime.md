---
title: Атрибут Tombstone-Lifetime
description: Число дней до удаления удаленного объекта из служб каталогов.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Tombstone-Lifetime
- Схема AD атрибута Томбстонелифетиме
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893630"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="8cf52-105">Атрибут Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="8cf52-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="8cf52-106">Число дней до удаления удаленного объекта из служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="8cf52-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="8cf52-107">Это помогает удалять объекты из реплицируемых серверов и предотвращать восстановление из повторного представления удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="8cf52-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="8cf52-108">Это значение находится в объекте службы каталогов в сетевом адаптере конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8cf52-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="8cf52-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-109">Entry</span></span> | <span data-ttu-id="8cf52-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="8cf52-111">CN</span><span class="sxs-lookup"><span data-stu-id="8cf52-111">CN</span></span>                | <span data-ttu-id="8cf52-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="8cf52-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="8cf52-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8cf52-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8cf52-114">томбстонелифетиме</span><span class="sxs-lookup"><span data-stu-id="8cf52-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="8cf52-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8cf52-115">Size</span></span>              | <span data-ttu-id="8cf52-116">4 байта.</span><span class="sxs-lookup"><span data-stu-id="8cf52-116">4 bytes.</span></span> <span data-ttu-id="8cf52-117">Значение по умолчанию — 60 дней, если значения не заданы.</span><span class="sxs-lookup"><span data-stu-id="8cf52-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="8cf52-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8cf52-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="8cf52-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8cf52-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="8cf52-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-120">Attribute-Id</span></span>      | <span data-ttu-id="8cf52-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="8cf52-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="8cf52-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8cf52-122">System-Id-Guid</span></span>    | <span data-ttu-id="8cf52-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="8cf52-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="8cf52-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cf52-124">Syntax</span></span>            | [<span data-ttu-id="8cf52-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="8cf52-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="8cf52-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8cf52-126">Implementations</span></span>

-   [<span data-ttu-id="8cf52-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8cf52-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8cf52-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cf52-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cf52-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8cf52-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8cf52-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cf52-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cf52-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cf52-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cf52-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cf52-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cf52-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cf52-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8cf52-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cf52-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8cf52-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-135">Entry</span></span> | <span data-ttu-id="8cf52-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-138">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-139">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-140">System-Only</span></span>            | <span data-ttu-id="8cf52-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-141">False</span></span>                                            |
| <span data-ttu-id="8cf52-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-142">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-143">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-143">True</span></span>                                             |
| <span data-ttu-id="8cf52-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-144">Is Indexed</span></span>             | <span data-ttu-id="8cf52-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-145">False</span></span>                                            |
| <span data-ttu-id="8cf52-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-146">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-147">False</span></span>                                            |
| <span data-ttu-id="8cf52-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-152">Search-Flags</span></span>           | <span data-ttu-id="8cf52-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-153">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-154">System-Flags</span></span>           | <span data-ttu-id="8cf52-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-155">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-156">Classes used in</span></span>        | [<span data-ttu-id="8cf52-157">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8cf52-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cf52-158">Windows Server 2003</span></span>



| <span data-ttu-id="8cf52-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-159">Entry</span></span> | <span data-ttu-id="8cf52-160">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-162">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-163">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-164">System-Only</span></span>            | <span data-ttu-id="8cf52-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-165">False</span></span>                                            |
| <span data-ttu-id="8cf52-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-166">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-167">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-167">True</span></span>                                             |
| <span data-ttu-id="8cf52-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-168">Is Indexed</span></span>             | <span data-ttu-id="8cf52-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-169">False</span></span>                                            |
| <span data-ttu-id="8cf52-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-170">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-171">False</span></span>                                            |
| <span data-ttu-id="8cf52-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-176">Search-Flags</span></span>           | <span data-ttu-id="8cf52-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-177">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-178">System-Flags</span></span>           | <span data-ttu-id="8cf52-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-179">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-180">Classes used in</span></span>        | [<span data-ttu-id="8cf52-181">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8cf52-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="8cf52-182">ADAM</span></span>



| <span data-ttu-id="8cf52-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-183">Entry</span></span> | <span data-ttu-id="8cf52-184">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-186">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-187">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-188">System-Only</span></span>            | <span data-ttu-id="8cf52-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-189">False</span></span>                                            |
| <span data-ttu-id="8cf52-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-190">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-191">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-191">True</span></span>                                             |
| <span data-ttu-id="8cf52-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-192">Is Indexed</span></span>             | <span data-ttu-id="8cf52-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-193">False</span></span>                                            |
| <span data-ttu-id="8cf52-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-194">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-195">False</span></span>                                            |
| <span data-ttu-id="8cf52-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-200">Search-Flags</span></span>           | <span data-ttu-id="8cf52-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-201">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-202">System-Flags</span></span>           | <span data-ttu-id="8cf52-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-203">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-204">Classes used in</span></span>        | [<span data-ttu-id="8cf52-205">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cf52-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cf52-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cf52-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-207">Entry</span></span> | <span data-ttu-id="8cf52-208">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-210">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-211">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-212">System-Only</span></span>            | <span data-ttu-id="8cf52-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-213">False</span></span>                                            |
| <span data-ttu-id="8cf52-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-214">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-215">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-215">True</span></span>                                             |
| <span data-ttu-id="8cf52-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-216">Is Indexed</span></span>             | <span data-ttu-id="8cf52-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-217">False</span></span>                                            |
| <span data-ttu-id="8cf52-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-218">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-219">False</span></span>                                            |
| <span data-ttu-id="8cf52-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-224">Search-Flags</span></span>           | <span data-ttu-id="8cf52-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-225">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-226">System-Flags</span></span>           | <span data-ttu-id="8cf52-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-227">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-228">Classes used in</span></span>        | [<span data-ttu-id="8cf52-229">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cf52-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cf52-230">Windows Server 2008</span></span>



| <span data-ttu-id="8cf52-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-231">Entry</span></span> | <span data-ttu-id="8cf52-232">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-234">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-235">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-236">System-Only</span></span>            | <span data-ttu-id="8cf52-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-237">False</span></span>                                            |
| <span data-ttu-id="8cf52-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-238">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-239">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-239">True</span></span>                                             |
| <span data-ttu-id="8cf52-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-240">Is Indexed</span></span>             | <span data-ttu-id="8cf52-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-241">False</span></span>                                            |
| <span data-ttu-id="8cf52-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-242">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-243">False</span></span>                                            |
| <span data-ttu-id="8cf52-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-248">Search-Flags</span></span>           | <span data-ttu-id="8cf52-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-249">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-250">System-Flags</span></span>           | <span data-ttu-id="8cf52-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-251">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-252">Classes used in</span></span>        | [<span data-ttu-id="8cf52-253">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cf52-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cf52-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cf52-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-255">Entry</span></span> | <span data-ttu-id="8cf52-256">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-258">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-259">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-260">System-Only</span></span>            | <span data-ttu-id="8cf52-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-261">False</span></span>                                            |
| <span data-ttu-id="8cf52-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-262">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-263">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-263">True</span></span>                                             |
| <span data-ttu-id="8cf52-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-264">Is Indexed</span></span>             | <span data-ttu-id="8cf52-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-265">False</span></span>                                            |
| <span data-ttu-id="8cf52-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-266">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-267">False</span></span>                                            |
| <span data-ttu-id="8cf52-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-272">Search-Flags</span></span>           | <span data-ttu-id="8cf52-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-273">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-274">System-Flags</span></span>           | <span data-ttu-id="8cf52-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-275">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-276">Classes used in</span></span>        | [<span data-ttu-id="8cf52-277">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cf52-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cf52-278">Windows Server 2012</span></span>



| <span data-ttu-id="8cf52-279">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cf52-279">Entry</span></span> | <span data-ttu-id="8cf52-280">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf52-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8cf52-281">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cf52-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8cf52-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf52-282">MAPI-Id</span></span>                | <span data-ttu-id="8cf52-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="8cf52-283">0x8145</span></span>                                           |
| <span data-ttu-id="8cf52-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf52-284">System-Only</span></span>            | <span data-ttu-id="8cf52-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-285">False</span></span>                                            |
| <span data-ttu-id="8cf52-286">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cf52-286">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf52-287">True</span><span class="sxs-lookup"><span data-stu-id="8cf52-287">True</span></span>                                             |
| <span data-ttu-id="8cf52-288">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cf52-288">Is Indexed</span></span>             | <span data-ttu-id="8cf52-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-289">False</span></span>                                            |
| <span data-ttu-id="8cf52-290">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cf52-290">In Global Catalog</span></span>      | <span data-ttu-id="8cf52-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cf52-291">False</span></span>                                            |
| <span data-ttu-id="8cf52-292">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cf52-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf52-293">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cf52-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8cf52-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf52-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf52-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8cf52-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-296">Search-Flags</span></span>           | <span data-ttu-id="8cf52-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf52-297">0x00000000</span></span>                                       |
| <span data-ttu-id="8cf52-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf52-298">System-Flags</span></span>           | <span data-ttu-id="8cf52-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf52-299">0x00000010</span></span>                                       |
| <span data-ttu-id="8cf52-300">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cf52-300">Classes used in</span></span>        | [<span data-ttu-id="8cf52-301">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="8cf52-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





