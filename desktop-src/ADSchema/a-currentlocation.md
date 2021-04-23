---
title: Атрибут Current-Location
description: Расположение компьютера для объекта, который был перемещен.
ms.assetid: b8767fcd-48f5-420c-9cbf-095ab1aee729
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Current-Location
- Схема AD атрибута currentLocation
topic_type:
- apiref
api_name:
- Current-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b37e2acb97806ad6cf72736d39e0c9a0e6c6d217
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655527"
---
# <a name="current-location-attribute"></a><span data-ttu-id="7ce17-105">Атрибут Current-Location</span><span class="sxs-lookup"><span data-stu-id="7ce17-105">Current-Location attribute</span></span>

<span data-ttu-id="7ce17-106">Расположение компьютера для объекта, который был перемещен.</span><span class="sxs-lookup"><span data-stu-id="7ce17-106">The computer location for an object that has moved.</span></span>



| <span data-ttu-id="7ce17-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-107">Entry</span></span> | <span data-ttu-id="7ce17-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="7ce17-109">CN</span><span class="sxs-lookup"><span data-stu-id="7ce17-109">CN</span></span>                | <span data-ttu-id="7ce17-110">Current-Location</span><span class="sxs-lookup"><span data-stu-id="7ce17-110">Current-Location</span></span>                                      |
| <span data-ttu-id="7ce17-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7ce17-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7ce17-112">currentLocation</span><span class="sxs-lookup"><span data-stu-id="7ce17-112">currentLocation</span></span>                                       |
| <span data-ttu-id="7ce17-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7ce17-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="7ce17-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7ce17-114">Update Privilege</span></span>  | <span data-ttu-id="7ce17-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="7ce17-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="7ce17-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7ce17-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="7ce17-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-117">Attribute-Id</span></span>      | <span data-ttu-id="7ce17-118">1.2.840.113556.1.4.335</span><span class="sxs-lookup"><span data-stu-id="7ce17-118">1.2.840.113556.1.4.335</span></span>                                |
| <span data-ttu-id="7ce17-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7ce17-119">System-Id-Guid</span></span>    | <span data-ttu-id="7ce17-120">1f0075fc-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7ce17-120">1f0075fc-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="7ce17-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ce17-121">Syntax</span></span>            | [<span data-ttu-id="7ce17-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="7ce17-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="7ce17-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7ce17-123">Implementations</span></span>

-   [<span data-ttu-id="7ce17-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ce17-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ce17-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ce17-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ce17-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ce17-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ce17-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ce17-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ce17-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ce17-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ce17-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ce17-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ce17-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ce17-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7ce17-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-131">Entry</span></span> | <span data-ttu-id="7ce17-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-132">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7ce17-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ce17-133">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-134">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ce17-135">System-Only</span></span>            | <span data-ttu-id="7ce17-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-136">False</span></span>                                                          |
| <span data-ttu-id="7ce17-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ce17-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7ce17-138">True</span><span class="sxs-lookup"><span data-stu-id="7ce17-138">True</span></span>                                                           |
| <span data-ttu-id="7ce17-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ce17-139">Is Indexed</span></span>             | <span data-ttu-id="7ce17-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-140">False</span></span>                                                          |
| <span data-ttu-id="7ce17-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ce17-141">In Global Catalog</span></span>      | <span data-ttu-id="7ce17-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-142">False</span></span>                                                          |
| <span data-ttu-id="7ce17-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ce17-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ce17-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ce17-144">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7ce17-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ce17-145">Range-Lower</span></span>            | <span data-ttu-id="7ce17-146">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-146">32</span></span>                                                             |
| <span data-ttu-id="7ce17-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ce17-147">Range-Upper</span></span>            | <span data-ttu-id="7ce17-148">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-148">32</span></span>                                                             |
| <span data-ttu-id="7ce17-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-149">Search-Flags</span></span>           | <span data-ttu-id="7ce17-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ce17-150">0x00000000</span></span>                                                     |
| <span data-ttu-id="7ce17-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-151">System-Flags</span></span>           | <span data-ttu-id="7ce17-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ce17-152">0x00000010</span></span>                                                     |
| <span data-ttu-id="7ce17-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ce17-153">Classes used in</span></span>        | [<span data-ttu-id="7ce17-154">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="7ce17-154">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ce17-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ce17-155">Windows Server 2003</span></span>



| <span data-ttu-id="7ce17-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-156">Entry</span></span> | <span data-ttu-id="7ce17-157">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-157">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7ce17-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ce17-158">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-159">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ce17-160">System-Only</span></span>            | <span data-ttu-id="7ce17-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-161">False</span></span>                                                          |
| <span data-ttu-id="7ce17-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ce17-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7ce17-163">True</span><span class="sxs-lookup"><span data-stu-id="7ce17-163">True</span></span>                                                           |
| <span data-ttu-id="7ce17-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ce17-164">Is Indexed</span></span>             | <span data-ttu-id="7ce17-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-165">False</span></span>                                                          |
| <span data-ttu-id="7ce17-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ce17-166">In Global Catalog</span></span>      | <span data-ttu-id="7ce17-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-167">False</span></span>                                                          |
| <span data-ttu-id="7ce17-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ce17-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ce17-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ce17-169">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7ce17-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ce17-170">Range-Lower</span></span>            | <span data-ttu-id="7ce17-171">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-171">32</span></span>                                                             |
| <span data-ttu-id="7ce17-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ce17-172">Range-Upper</span></span>            | <span data-ttu-id="7ce17-173">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-173">32</span></span>                                                             |
| <span data-ttu-id="7ce17-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-174">Search-Flags</span></span>           | <span data-ttu-id="7ce17-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ce17-175">0x00000000</span></span>                                                     |
| <span data-ttu-id="7ce17-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-176">System-Flags</span></span>           | <span data-ttu-id="7ce17-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ce17-177">0x00000010</span></span>                                                     |
| <span data-ttu-id="7ce17-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ce17-178">Classes used in</span></span>        | [<span data-ttu-id="7ce17-179">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="7ce17-179">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ce17-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ce17-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ce17-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-181">Entry</span></span> | <span data-ttu-id="7ce17-182">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-182">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7ce17-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ce17-183">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-184">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ce17-185">System-Only</span></span>            | <span data-ttu-id="7ce17-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-186">False</span></span>                                                          |
| <span data-ttu-id="7ce17-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ce17-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7ce17-188">True</span><span class="sxs-lookup"><span data-stu-id="7ce17-188">True</span></span>                                                           |
| <span data-ttu-id="7ce17-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ce17-189">Is Indexed</span></span>             | <span data-ttu-id="7ce17-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-190">False</span></span>                                                          |
| <span data-ttu-id="7ce17-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ce17-191">In Global Catalog</span></span>      | <span data-ttu-id="7ce17-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-192">False</span></span>                                                          |
| <span data-ttu-id="7ce17-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ce17-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ce17-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ce17-194">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7ce17-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ce17-195">Range-Lower</span></span>            | <span data-ttu-id="7ce17-196">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-196">32</span></span>                                                             |
| <span data-ttu-id="7ce17-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ce17-197">Range-Upper</span></span>            | <span data-ttu-id="7ce17-198">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-198">32</span></span>                                                             |
| <span data-ttu-id="7ce17-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-199">Search-Flags</span></span>           | <span data-ttu-id="7ce17-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ce17-200">0x00000000</span></span>                                                     |
| <span data-ttu-id="7ce17-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-201">System-Flags</span></span>           | <span data-ttu-id="7ce17-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ce17-202">0x00000010</span></span>                                                     |
| <span data-ttu-id="7ce17-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ce17-203">Classes used in</span></span>        | [<span data-ttu-id="7ce17-204">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="7ce17-204">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ce17-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ce17-205">Windows Server 2008</span></span>



| <span data-ttu-id="7ce17-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-206">Entry</span></span> | <span data-ttu-id="7ce17-207">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-207">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7ce17-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ce17-208">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-209">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ce17-210">System-Only</span></span>            | <span data-ttu-id="7ce17-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-211">False</span></span>                                                          |
| <span data-ttu-id="7ce17-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ce17-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7ce17-213">True</span><span class="sxs-lookup"><span data-stu-id="7ce17-213">True</span></span>                                                           |
| <span data-ttu-id="7ce17-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ce17-214">Is Indexed</span></span>             | <span data-ttu-id="7ce17-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-215">False</span></span>                                                          |
| <span data-ttu-id="7ce17-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ce17-216">In Global Catalog</span></span>      | <span data-ttu-id="7ce17-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-217">False</span></span>                                                          |
| <span data-ttu-id="7ce17-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ce17-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ce17-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ce17-219">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7ce17-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ce17-220">Range-Lower</span></span>            | <span data-ttu-id="7ce17-221">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-221">32</span></span>                                                             |
| <span data-ttu-id="7ce17-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ce17-222">Range-Upper</span></span>            | <span data-ttu-id="7ce17-223">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-223">32</span></span>                                                             |
| <span data-ttu-id="7ce17-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-224">Search-Flags</span></span>           | <span data-ttu-id="7ce17-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ce17-225">0x00000000</span></span>                                                     |
| <span data-ttu-id="7ce17-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-226">System-Flags</span></span>           | <span data-ttu-id="7ce17-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ce17-227">0x00000010</span></span>                                                     |
| <span data-ttu-id="7ce17-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ce17-228">Classes used in</span></span>        | [<span data-ttu-id="7ce17-229">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="7ce17-229">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ce17-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ce17-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ce17-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-231">Entry</span></span> | <span data-ttu-id="7ce17-232">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-232">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7ce17-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ce17-233">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-234">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ce17-235">System-Only</span></span>            | <span data-ttu-id="7ce17-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-236">False</span></span>                                                          |
| <span data-ttu-id="7ce17-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ce17-237">Is-Single-Valued</span></span>       | <span data-ttu-id="7ce17-238">True</span><span class="sxs-lookup"><span data-stu-id="7ce17-238">True</span></span>                                                           |
| <span data-ttu-id="7ce17-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ce17-239">Is Indexed</span></span>             | <span data-ttu-id="7ce17-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-240">False</span></span>                                                          |
| <span data-ttu-id="7ce17-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ce17-241">In Global Catalog</span></span>      | <span data-ttu-id="7ce17-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-242">False</span></span>                                                          |
| <span data-ttu-id="7ce17-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ce17-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ce17-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ce17-244">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7ce17-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ce17-245">Range-Lower</span></span>            | <span data-ttu-id="7ce17-246">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-246">32</span></span>                                                             |
| <span data-ttu-id="7ce17-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ce17-247">Range-Upper</span></span>            | <span data-ttu-id="7ce17-248">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-248">32</span></span>                                                             |
| <span data-ttu-id="7ce17-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-249">Search-Flags</span></span>           | <span data-ttu-id="7ce17-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ce17-250">0x00000000</span></span>                                                     |
| <span data-ttu-id="7ce17-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-251">System-Flags</span></span>           | <span data-ttu-id="7ce17-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ce17-252">0x00000010</span></span>                                                     |
| <span data-ttu-id="7ce17-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ce17-253">Classes used in</span></span>        | [<span data-ttu-id="7ce17-254">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="7ce17-254">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ce17-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ce17-255">Windows Server 2012</span></span>



| <span data-ttu-id="7ce17-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ce17-256">Entry</span></span> | <span data-ttu-id="7ce17-257">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce17-257">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7ce17-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ce17-258">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ce17-259">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7ce17-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ce17-260">System-Only</span></span>            | <span data-ttu-id="7ce17-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-261">False</span></span>                                                          |
| <span data-ttu-id="7ce17-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ce17-262">Is-Single-Valued</span></span>       | <span data-ttu-id="7ce17-263">True</span><span class="sxs-lookup"><span data-stu-id="7ce17-263">True</span></span>                                                           |
| <span data-ttu-id="7ce17-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ce17-264">Is Indexed</span></span>             | <span data-ttu-id="7ce17-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-265">False</span></span>                                                          |
| <span data-ttu-id="7ce17-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ce17-266">In Global Catalog</span></span>      | <span data-ttu-id="7ce17-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ce17-267">False</span></span>                                                          |
| <span data-ttu-id="7ce17-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ce17-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ce17-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ce17-269">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7ce17-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ce17-270">Range-Lower</span></span>            | <span data-ttu-id="7ce17-271">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-271">32</span></span>                                                             |
| <span data-ttu-id="7ce17-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ce17-272">Range-Upper</span></span>            | <span data-ttu-id="7ce17-273">32</span><span class="sxs-lookup"><span data-stu-id="7ce17-273">32</span></span>                                                             |
| <span data-ttu-id="7ce17-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-274">Search-Flags</span></span>           | <span data-ttu-id="7ce17-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ce17-275">0x00000000</span></span>                                                     |
| <span data-ttu-id="7ce17-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ce17-276">System-Flags</span></span>           | <span data-ttu-id="7ce17-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ce17-277">0x00000010</span></span>                                                     |
| <span data-ttu-id="7ce17-278">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ce17-278">Classes used in</span></span>        | [<span data-ttu-id="7ce17-279">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="7ce17-279">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> |



 

 





