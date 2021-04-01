---
title: Атрибут-Machine-ID
description: ИДЕНТИФИКАТОР компьютера, на котором находится объект Link-Track-Vol-Entry.
ms.assetid: 6e957744-c778-4112-8308-e9d1a3e01f56
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута для ИД компьютера
- Схема AD атрибута Куррмачинеид
topic_type:
- apiref
api_name:
- Curr-Machine-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32b9a9f1e633e5041c3524fe79df5e4b4b26950
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989572"
---
# <a name="curr-machine-id-attribute"></a><span data-ttu-id="01f8b-105">Атрибут-Machine-ID</span><span class="sxs-lookup"><span data-stu-id="01f8b-105">Curr-Machine-Id attribute</span></span>

<span data-ttu-id="01f8b-106">ИДЕНТИФИКАТОР компьютера, на котором находится объект Link-Track-Vol-Entry.</span><span class="sxs-lookup"><span data-stu-id="01f8b-106">The ID of the machine where a Link-Track-Vol-Entry object is located.</span></span>



| <span data-ttu-id="01f8b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-107">Entry</span></span> | <span data-ttu-id="01f8b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="01f8b-109">CN</span><span class="sxs-lookup"><span data-stu-id="01f8b-109">CN</span></span>                | <span data-ttu-id="01f8b-110">Идентификатор компьютера</span><span class="sxs-lookup"><span data-stu-id="01f8b-110">Curr-Machine-Id</span></span>                                       |
| <span data-ttu-id="01f8b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="01f8b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="01f8b-112">куррмачинеид</span><span class="sxs-lookup"><span data-stu-id="01f8b-112">currMachineId</span></span>                                         |
| <span data-ttu-id="01f8b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="01f8b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="01f8b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="01f8b-114">Update Privilege</span></span>  | <span data-ttu-id="01f8b-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="01f8b-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="01f8b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="01f8b-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="01f8b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-117">Attribute-Id</span></span>      | <span data-ttu-id="01f8b-118">1.2.840.113556.1.4.337</span><span class="sxs-lookup"><span data-stu-id="01f8b-118">1.2.840.113556.1.4.337</span></span>                                |
| <span data-ttu-id="01f8b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="01f8b-119">System-Id-Guid</span></span>    | <span data-ttu-id="01f8b-120">1f0075fe-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="01f8b-120">1f0075fe-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="01f8b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01f8b-121">Syntax</span></span>            | [<span data-ttu-id="01f8b-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="01f8b-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="01f8b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="01f8b-123">Implementations</span></span>

-   [<span data-ttu-id="01f8b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="01f8b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="01f8b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01f8b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01f8b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01f8b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01f8b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01f8b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01f8b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01f8b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01f8b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01f8b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="01f8b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01f8b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="01f8b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-131">Entry</span></span> | <span data-ttu-id="01f8b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-132">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01f8b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01f8b-133">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-134">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f8b-135">System-Only</span></span>            | <span data-ttu-id="01f8b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-136">False</span></span>                                                          |
| <span data-ttu-id="01f8b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01f8b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="01f8b-138">True</span><span class="sxs-lookup"><span data-stu-id="01f8b-138">True</span></span>                                                           |
| <span data-ttu-id="01f8b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01f8b-139">Is Indexed</span></span>             | <span data-ttu-id="01f8b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-140">False</span></span>                                                          |
| <span data-ttu-id="01f8b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01f8b-141">In Global Catalog</span></span>      | <span data-ttu-id="01f8b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-142">False</span></span>                                                          |
| <span data-ttu-id="01f8b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01f8b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f8b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01f8b-144">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01f8b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f8b-145">Range-Lower</span></span>            | <span data-ttu-id="01f8b-146">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-146">16</span></span>                                                             |
| <span data-ttu-id="01f8b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f8b-147">Range-Upper</span></span>            | <span data-ttu-id="01f8b-148">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-148">16</span></span>                                                             |
| <span data-ttu-id="01f8b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-149">Search-Flags</span></span>           | <span data-ttu-id="01f8b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01f8b-150">0x00000000</span></span>                                                     |
| <span data-ttu-id="01f8b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-151">System-Flags</span></span>           | <span data-ttu-id="01f8b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f8b-152">0x00000010</span></span>                                                     |
| <span data-ttu-id="01f8b-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01f8b-153">Classes used in</span></span>        | [<span data-ttu-id="01f8b-154">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="01f8b-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="01f8b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01f8b-155">Windows Server 2003</span></span>



| <span data-ttu-id="01f8b-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-156">Entry</span></span> | <span data-ttu-id="01f8b-157">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-157">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01f8b-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01f8b-158">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-159">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f8b-160">System-Only</span></span>            | <span data-ttu-id="01f8b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-161">False</span></span>                                                          |
| <span data-ttu-id="01f8b-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01f8b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="01f8b-163">True</span><span class="sxs-lookup"><span data-stu-id="01f8b-163">True</span></span>                                                           |
| <span data-ttu-id="01f8b-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01f8b-164">Is Indexed</span></span>             | <span data-ttu-id="01f8b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-165">False</span></span>                                                          |
| <span data-ttu-id="01f8b-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01f8b-166">In Global Catalog</span></span>      | <span data-ttu-id="01f8b-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-167">False</span></span>                                                          |
| <span data-ttu-id="01f8b-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01f8b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f8b-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01f8b-169">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01f8b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f8b-170">Range-Lower</span></span>            | <span data-ttu-id="01f8b-171">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-171">16</span></span>                                                             |
| <span data-ttu-id="01f8b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f8b-172">Range-Upper</span></span>            | <span data-ttu-id="01f8b-173">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-173">16</span></span>                                                             |
| <span data-ttu-id="01f8b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-174">Search-Flags</span></span>           | <span data-ttu-id="01f8b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01f8b-175">0x00000000</span></span>                                                     |
| <span data-ttu-id="01f8b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-176">System-Flags</span></span>           | <span data-ttu-id="01f8b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f8b-177">0x00000010</span></span>                                                     |
| <span data-ttu-id="01f8b-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01f8b-178">Classes used in</span></span>        | [<span data-ttu-id="01f8b-179">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="01f8b-179">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01f8b-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01f8b-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01f8b-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-181">Entry</span></span> | <span data-ttu-id="01f8b-182">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-182">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01f8b-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01f8b-183">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-184">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f8b-185">System-Only</span></span>            | <span data-ttu-id="01f8b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-186">False</span></span>                                                          |
| <span data-ttu-id="01f8b-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01f8b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="01f8b-188">True</span><span class="sxs-lookup"><span data-stu-id="01f8b-188">True</span></span>                                                           |
| <span data-ttu-id="01f8b-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01f8b-189">Is Indexed</span></span>             | <span data-ttu-id="01f8b-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-190">False</span></span>                                                          |
| <span data-ttu-id="01f8b-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01f8b-191">In Global Catalog</span></span>      | <span data-ttu-id="01f8b-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-192">False</span></span>                                                          |
| <span data-ttu-id="01f8b-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01f8b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f8b-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01f8b-194">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01f8b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f8b-195">Range-Lower</span></span>            | <span data-ttu-id="01f8b-196">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-196">16</span></span>                                                             |
| <span data-ttu-id="01f8b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f8b-197">Range-Upper</span></span>            | <span data-ttu-id="01f8b-198">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-198">16</span></span>                                                             |
| <span data-ttu-id="01f8b-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-199">Search-Flags</span></span>           | <span data-ttu-id="01f8b-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01f8b-200">0x00000000</span></span>                                                     |
| <span data-ttu-id="01f8b-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-201">System-Flags</span></span>           | <span data-ttu-id="01f8b-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f8b-202">0x00000010</span></span>                                                     |
| <span data-ttu-id="01f8b-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01f8b-203">Classes used in</span></span>        | [<span data-ttu-id="01f8b-204">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="01f8b-204">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01f8b-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01f8b-205">Windows Server 2008</span></span>



| <span data-ttu-id="01f8b-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-206">Entry</span></span> | <span data-ttu-id="01f8b-207">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-207">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01f8b-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01f8b-208">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-209">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f8b-210">System-Only</span></span>            | <span data-ttu-id="01f8b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-211">False</span></span>                                                          |
| <span data-ttu-id="01f8b-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01f8b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="01f8b-213">True</span><span class="sxs-lookup"><span data-stu-id="01f8b-213">True</span></span>                                                           |
| <span data-ttu-id="01f8b-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01f8b-214">Is Indexed</span></span>             | <span data-ttu-id="01f8b-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-215">False</span></span>                                                          |
| <span data-ttu-id="01f8b-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01f8b-216">In Global Catalog</span></span>      | <span data-ttu-id="01f8b-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-217">False</span></span>                                                          |
| <span data-ttu-id="01f8b-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01f8b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f8b-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01f8b-219">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01f8b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f8b-220">Range-Lower</span></span>            | <span data-ttu-id="01f8b-221">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-221">16</span></span>                                                             |
| <span data-ttu-id="01f8b-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f8b-222">Range-Upper</span></span>            | <span data-ttu-id="01f8b-223">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-223">16</span></span>                                                             |
| <span data-ttu-id="01f8b-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-224">Search-Flags</span></span>           | <span data-ttu-id="01f8b-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01f8b-225">0x00000000</span></span>                                                     |
| <span data-ttu-id="01f8b-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-226">System-Flags</span></span>           | <span data-ttu-id="01f8b-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f8b-227">0x00000010</span></span>                                                     |
| <span data-ttu-id="01f8b-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01f8b-228">Classes used in</span></span>        | [<span data-ttu-id="01f8b-229">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="01f8b-229">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01f8b-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01f8b-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01f8b-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-231">Entry</span></span> | <span data-ttu-id="01f8b-232">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-232">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01f8b-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01f8b-233">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-234">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f8b-235">System-Only</span></span>            | <span data-ttu-id="01f8b-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-236">False</span></span>                                                          |
| <span data-ttu-id="01f8b-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01f8b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="01f8b-238">True</span><span class="sxs-lookup"><span data-stu-id="01f8b-238">True</span></span>                                                           |
| <span data-ttu-id="01f8b-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01f8b-239">Is Indexed</span></span>             | <span data-ttu-id="01f8b-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-240">False</span></span>                                                          |
| <span data-ttu-id="01f8b-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01f8b-241">In Global Catalog</span></span>      | <span data-ttu-id="01f8b-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-242">False</span></span>                                                          |
| <span data-ttu-id="01f8b-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01f8b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f8b-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01f8b-244">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01f8b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f8b-245">Range-Lower</span></span>            | <span data-ttu-id="01f8b-246">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-246">16</span></span>                                                             |
| <span data-ttu-id="01f8b-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f8b-247">Range-Upper</span></span>            | <span data-ttu-id="01f8b-248">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-248">16</span></span>                                                             |
| <span data-ttu-id="01f8b-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-249">Search-Flags</span></span>           | <span data-ttu-id="01f8b-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01f8b-250">0x00000000</span></span>                                                     |
| <span data-ttu-id="01f8b-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-251">System-Flags</span></span>           | <span data-ttu-id="01f8b-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f8b-252">0x00000010</span></span>                                                     |
| <span data-ttu-id="01f8b-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01f8b-253">Classes used in</span></span>        | [<span data-ttu-id="01f8b-254">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="01f8b-254">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01f8b-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01f8b-255">Windows Server 2012</span></span>



| <span data-ttu-id="01f8b-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="01f8b-256">Entry</span></span> | <span data-ttu-id="01f8b-257">Значение</span><span class="sxs-lookup"><span data-stu-id="01f8b-257">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01f8b-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01f8b-258">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f8b-259">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01f8b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f8b-260">System-Only</span></span>            | <span data-ttu-id="01f8b-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-261">False</span></span>                                                          |
| <span data-ttu-id="01f8b-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01f8b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="01f8b-263">True</span><span class="sxs-lookup"><span data-stu-id="01f8b-263">True</span></span>                                                           |
| <span data-ttu-id="01f8b-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01f8b-264">Is Indexed</span></span>             | <span data-ttu-id="01f8b-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-265">False</span></span>                                                          |
| <span data-ttu-id="01f8b-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01f8b-266">In Global Catalog</span></span>      | <span data-ttu-id="01f8b-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="01f8b-267">False</span></span>                                                          |
| <span data-ttu-id="01f8b-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01f8b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f8b-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01f8b-269">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01f8b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f8b-270">Range-Lower</span></span>            | <span data-ttu-id="01f8b-271">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-271">16</span></span>                                                             |
| <span data-ttu-id="01f8b-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f8b-272">Range-Upper</span></span>            | <span data-ttu-id="01f8b-273">16</span><span class="sxs-lookup"><span data-stu-id="01f8b-273">16</span></span>                                                             |
| <span data-ttu-id="01f8b-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-274">Search-Flags</span></span>           | <span data-ttu-id="01f8b-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01f8b-275">0x00000000</span></span>                                                     |
| <span data-ttu-id="01f8b-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f8b-276">System-Flags</span></span>           | <span data-ttu-id="01f8b-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f8b-277">0x00000010</span></span>                                                     |
| <span data-ttu-id="01f8b-278">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01f8b-278">Classes used in</span></span>        | [<span data-ttu-id="01f8b-279">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="01f8b-279">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





