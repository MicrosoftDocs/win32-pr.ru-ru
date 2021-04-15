---
title: Атрибут FRS-Version-GUID
description: Если этот параметр указан, изменение этого значения означает, что в этом наборе реплик внесено изменение конфигурации.
ms.assetid: 27cd68c5-a8aa-4c14-bf1d-0eb7c4d9cca5
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута FRS-Version-GUID
- Схема AD атрибута Фрсверсионгуид
topic_type:
- apiref
api_name:
- FRS-Version-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12cfadd1086fbb8ee79bafb8d0ee5f947ff503e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536095"
---
# <a name="frs-version-guid-attribute"></a><span data-ttu-id="674d0-105">Атрибут FRS-Version-GUID</span><span class="sxs-lookup"><span data-stu-id="674d0-105">FRS-Version-GUID attribute</span></span>

<span data-ttu-id="674d0-106">Если этот параметр указан, изменение этого значения означает, что в этом наборе реплик внесено изменение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="674d0-106">If present, changing this value indicates a configuration change has been made on this replica set.</span></span>



| <span data-ttu-id="674d0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-107">Entry</span></span> | <span data-ttu-id="674d0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="674d0-109">CN</span><span class="sxs-lookup"><span data-stu-id="674d0-109">CN</span></span>                | <span data-ttu-id="674d0-110">FRS-Version-GUID</span><span class="sxs-lookup"><span data-stu-id="674d0-110">FRS-Version-GUID</span></span>                                      |
| <span data-ttu-id="674d0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="674d0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="674d0-112">фрсверсионгуид</span><span class="sxs-lookup"><span data-stu-id="674d0-112">fRSVersionGUID</span></span>                                        |
| <span data-ttu-id="674d0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="674d0-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="674d0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="674d0-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="674d0-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="674d0-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="674d0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-116">Attribute-Id</span></span>      | <span data-ttu-id="674d0-117">1.2.840.113556.1.4.43</span><span class="sxs-lookup"><span data-stu-id="674d0-117">1.2.840.113556.1.4.43</span></span>                                 |
| <span data-ttu-id="674d0-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="674d0-118">System-Id-Guid</span></span>    | <span data-ttu-id="674d0-119">26d9736c-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="674d0-119">26d9736c-6070-11d1-a9c6-0000f80367c1</span></span>                  |
| <span data-ttu-id="674d0-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="674d0-120">Syntax</span></span>            | [<span data-ttu-id="674d0-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="674d0-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="674d0-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="674d0-122">Implementations</span></span>

-   [<span data-ttu-id="674d0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="674d0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="674d0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="674d0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="674d0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="674d0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="674d0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="674d0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="674d0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="674d0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="674d0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="674d0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="674d0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="674d0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="674d0-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-130">Entry</span></span> | <span data-ttu-id="674d0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="674d0-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="674d0-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="674d0-134">System-Only</span></span>            | <span data-ttu-id="674d0-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-135">False</span></span>                                                     |
| <span data-ttu-id="674d0-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="674d0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="674d0-137">True</span><span class="sxs-lookup"><span data-stu-id="674d0-137">True</span></span>                                                      |
| <span data-ttu-id="674d0-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="674d0-138">Is Indexed</span></span>             | <span data-ttu-id="674d0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-139">False</span></span>                                                     |
| <span data-ttu-id="674d0-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="674d0-140">In Global Catalog</span></span>      | <span data-ttu-id="674d0-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-141">False</span></span>                                                     |
| <span data-ttu-id="674d0-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="674d0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="674d0-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="674d0-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="674d0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674d0-144">Range-Lower</span></span>            | <span data-ttu-id="674d0-145">16</span><span class="sxs-lookup"><span data-stu-id="674d0-145">16</span></span>                                                        |
| <span data-ttu-id="674d0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674d0-146">Range-Upper</span></span>            | <span data-ttu-id="674d0-147">16</span><span class="sxs-lookup"><span data-stu-id="674d0-147">16</span></span>                                                        |
| <span data-ttu-id="674d0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-148">Search-Flags</span></span>           | <span data-ttu-id="674d0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674d0-149">0x00000000</span></span>                                                |
| <span data-ttu-id="674d0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-150">System-Flags</span></span>           | <span data-ttu-id="674d0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674d0-151">0x00000010</span></span>                                                |
| <span data-ttu-id="674d0-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="674d0-152">Classes used in</span></span>        | [<span data-ttu-id="674d0-153">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="674d0-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="674d0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="674d0-154">Windows Server 2003</span></span>



| <span data-ttu-id="674d0-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-155">Entry</span></span> | <span data-ttu-id="674d0-156">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="674d0-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="674d0-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="674d0-159">System-Only</span></span>            | <span data-ttu-id="674d0-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-160">False</span></span>                                                     |
| <span data-ttu-id="674d0-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="674d0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="674d0-162">True</span><span class="sxs-lookup"><span data-stu-id="674d0-162">True</span></span>                                                      |
| <span data-ttu-id="674d0-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="674d0-163">Is Indexed</span></span>             | <span data-ttu-id="674d0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-164">False</span></span>                                                     |
| <span data-ttu-id="674d0-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="674d0-165">In Global Catalog</span></span>      | <span data-ttu-id="674d0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-166">False</span></span>                                                     |
| <span data-ttu-id="674d0-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="674d0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="674d0-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="674d0-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="674d0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674d0-169">Range-Lower</span></span>            | <span data-ttu-id="674d0-170">16</span><span class="sxs-lookup"><span data-stu-id="674d0-170">16</span></span>                                                        |
| <span data-ttu-id="674d0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674d0-171">Range-Upper</span></span>            | <span data-ttu-id="674d0-172">16</span><span class="sxs-lookup"><span data-stu-id="674d0-172">16</span></span>                                                        |
| <span data-ttu-id="674d0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-173">Search-Flags</span></span>           | <span data-ttu-id="674d0-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674d0-174">0x00000000</span></span>                                                |
| <span data-ttu-id="674d0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-175">System-Flags</span></span>           | <span data-ttu-id="674d0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674d0-176">0x00000010</span></span>                                                |
| <span data-ttu-id="674d0-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="674d0-177">Classes used in</span></span>        | [<span data-ttu-id="674d0-178">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="674d0-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="674d0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="674d0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="674d0-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-180">Entry</span></span> | <span data-ttu-id="674d0-181">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="674d0-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="674d0-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="674d0-184">System-Only</span></span>            | <span data-ttu-id="674d0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-185">False</span></span>                                                     |
| <span data-ttu-id="674d0-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="674d0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="674d0-187">True</span><span class="sxs-lookup"><span data-stu-id="674d0-187">True</span></span>                                                      |
| <span data-ttu-id="674d0-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="674d0-188">Is Indexed</span></span>             | <span data-ttu-id="674d0-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-189">False</span></span>                                                     |
| <span data-ttu-id="674d0-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="674d0-190">In Global Catalog</span></span>      | <span data-ttu-id="674d0-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-191">False</span></span>                                                     |
| <span data-ttu-id="674d0-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="674d0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="674d0-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="674d0-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="674d0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674d0-194">Range-Lower</span></span>            | <span data-ttu-id="674d0-195">16</span><span class="sxs-lookup"><span data-stu-id="674d0-195">16</span></span>                                                        |
| <span data-ttu-id="674d0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674d0-196">Range-Upper</span></span>            | <span data-ttu-id="674d0-197">16</span><span class="sxs-lookup"><span data-stu-id="674d0-197">16</span></span>                                                        |
| <span data-ttu-id="674d0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-198">Search-Flags</span></span>           | <span data-ttu-id="674d0-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674d0-199">0x00000000</span></span>                                                |
| <span data-ttu-id="674d0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-200">System-Flags</span></span>           | <span data-ttu-id="674d0-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674d0-201">0x00000010</span></span>                                                |
| <span data-ttu-id="674d0-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="674d0-202">Classes used in</span></span>        | [<span data-ttu-id="674d0-203">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="674d0-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="674d0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="674d0-204">Windows Server 2008</span></span>



| <span data-ttu-id="674d0-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-205">Entry</span></span> | <span data-ttu-id="674d0-206">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="674d0-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="674d0-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="674d0-209">System-Only</span></span>            | <span data-ttu-id="674d0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-210">False</span></span>                                                     |
| <span data-ttu-id="674d0-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="674d0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="674d0-212">True</span><span class="sxs-lookup"><span data-stu-id="674d0-212">True</span></span>                                                      |
| <span data-ttu-id="674d0-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="674d0-213">Is Indexed</span></span>             | <span data-ttu-id="674d0-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-214">False</span></span>                                                     |
| <span data-ttu-id="674d0-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="674d0-215">In Global Catalog</span></span>      | <span data-ttu-id="674d0-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-216">False</span></span>                                                     |
| <span data-ttu-id="674d0-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="674d0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="674d0-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="674d0-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="674d0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674d0-219">Range-Lower</span></span>            | <span data-ttu-id="674d0-220">16</span><span class="sxs-lookup"><span data-stu-id="674d0-220">16</span></span>                                                        |
| <span data-ttu-id="674d0-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674d0-221">Range-Upper</span></span>            | <span data-ttu-id="674d0-222">16</span><span class="sxs-lookup"><span data-stu-id="674d0-222">16</span></span>                                                        |
| <span data-ttu-id="674d0-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-223">Search-Flags</span></span>           | <span data-ttu-id="674d0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674d0-224">0x00000000</span></span>                                                |
| <span data-ttu-id="674d0-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-225">System-Flags</span></span>           | <span data-ttu-id="674d0-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674d0-226">0x00000010</span></span>                                                |
| <span data-ttu-id="674d0-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="674d0-227">Classes used in</span></span>        | [<span data-ttu-id="674d0-228">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="674d0-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="674d0-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="674d0-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="674d0-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-230">Entry</span></span> | <span data-ttu-id="674d0-231">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="674d0-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="674d0-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="674d0-234">System-Only</span></span>            | <span data-ttu-id="674d0-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-235">False</span></span>                                                     |
| <span data-ttu-id="674d0-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="674d0-236">Is-Single-Valued</span></span>       | <span data-ttu-id="674d0-237">True</span><span class="sxs-lookup"><span data-stu-id="674d0-237">True</span></span>                                                      |
| <span data-ttu-id="674d0-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="674d0-238">Is Indexed</span></span>             | <span data-ttu-id="674d0-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-239">False</span></span>                                                     |
| <span data-ttu-id="674d0-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="674d0-240">In Global Catalog</span></span>      | <span data-ttu-id="674d0-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-241">False</span></span>                                                     |
| <span data-ttu-id="674d0-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="674d0-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="674d0-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="674d0-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="674d0-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674d0-244">Range-Lower</span></span>            | <span data-ttu-id="674d0-245">16</span><span class="sxs-lookup"><span data-stu-id="674d0-245">16</span></span>                                                        |
| <span data-ttu-id="674d0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674d0-246">Range-Upper</span></span>            | <span data-ttu-id="674d0-247">16</span><span class="sxs-lookup"><span data-stu-id="674d0-247">16</span></span>                                                        |
| <span data-ttu-id="674d0-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-248">Search-Flags</span></span>           | <span data-ttu-id="674d0-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674d0-249">0x00000000</span></span>                                                |
| <span data-ttu-id="674d0-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-250">System-Flags</span></span>           | <span data-ttu-id="674d0-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674d0-251">0x00000010</span></span>                                                |
| <span data-ttu-id="674d0-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="674d0-252">Classes used in</span></span>        | [<span data-ttu-id="674d0-253">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="674d0-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="674d0-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="674d0-254">Windows Server 2012</span></span>



| <span data-ttu-id="674d0-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="674d0-255">Entry</span></span> | <span data-ttu-id="674d0-256">Значение</span><span class="sxs-lookup"><span data-stu-id="674d0-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="674d0-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="674d0-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674d0-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="674d0-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="674d0-259">System-Only</span></span>            | <span data-ttu-id="674d0-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-260">False</span></span>                                                     |
| <span data-ttu-id="674d0-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="674d0-261">Is-Single-Valued</span></span>       | <span data-ttu-id="674d0-262">True</span><span class="sxs-lookup"><span data-stu-id="674d0-262">True</span></span>                                                      |
| <span data-ttu-id="674d0-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="674d0-263">Is Indexed</span></span>             | <span data-ttu-id="674d0-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-264">False</span></span>                                                     |
| <span data-ttu-id="674d0-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="674d0-265">In Global Catalog</span></span>      | <span data-ttu-id="674d0-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="674d0-266">False</span></span>                                                     |
| <span data-ttu-id="674d0-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="674d0-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="674d0-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="674d0-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="674d0-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674d0-269">Range-Lower</span></span>            | <span data-ttu-id="674d0-270">16</span><span class="sxs-lookup"><span data-stu-id="674d0-270">16</span></span>                                                        |
| <span data-ttu-id="674d0-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674d0-271">Range-Upper</span></span>            | <span data-ttu-id="674d0-272">16</span><span class="sxs-lookup"><span data-stu-id="674d0-272">16</span></span>                                                        |
| <span data-ttu-id="674d0-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-273">Search-Flags</span></span>           | <span data-ttu-id="674d0-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674d0-274">0x00000000</span></span>                                                |
| <span data-ttu-id="674d0-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674d0-275">System-Flags</span></span>           | <span data-ttu-id="674d0-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674d0-276">0x00000010</span></span>                                                |
| <span data-ttu-id="674d0-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="674d0-277">Classes used in</span></span>        | [<span data-ttu-id="674d0-278">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="674d0-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





