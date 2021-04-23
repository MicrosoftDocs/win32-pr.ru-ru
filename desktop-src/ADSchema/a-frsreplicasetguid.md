---
title: Атрибут FRS-реплика Set-GUID
description: Идентификатор GUID, определяющий набор реплик FRS.
ms.assetid: c916e10a-bf4e-4dbd-8a22-4a88f3933af0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута FRS реплики Set-GUID
- Схема AD атрибута Фрсрепликасетгуид
topic_type:
- apiref
api_name:
- FRS-Replica-Set-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a914c937771c4ea5548fd21bc35efd05486a899
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654947"
---
# <a name="frs-replica-set-guid-attribute"></a><span data-ttu-id="6f4a7-105">Атрибут FRS-реплика Set-GUID</span><span class="sxs-lookup"><span data-stu-id="6f4a7-105">FRS-Replica-Set-GUID attribute</span></span>

<span data-ttu-id="6f4a7-106">Идентификатор GUID, определяющий набор реплик FRS.</span><span class="sxs-lookup"><span data-stu-id="6f4a7-106">GUID that identifies an FRS Replica Set.</span></span>



| <span data-ttu-id="6f4a7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-107">Entry</span></span> | <span data-ttu-id="6f4a7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6f4a7-109">CN</span><span class="sxs-lookup"><span data-stu-id="6f4a7-109">CN</span></span>                | <span data-ttu-id="6f4a7-110">FRS-Replica-Set-GUID</span><span class="sxs-lookup"><span data-stu-id="6f4a7-110">FRS-Replica-Set-GUID</span></span>                                  |
| <span data-ttu-id="6f4a7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6f4a7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6f4a7-112">фрсрепликасетгуид</span><span class="sxs-lookup"><span data-stu-id="6f4a7-112">fRSReplicaSetGUID</span></span>                                     |
| <span data-ttu-id="6f4a7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6f4a7-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6f4a7-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6f4a7-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6f4a7-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6f4a7-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6f4a7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-116">Attribute-Id</span></span>      | <span data-ttu-id="6f4a7-117">1.2.840.113556.1.4.533</span><span class="sxs-lookup"><span data-stu-id="6f4a7-117">1.2.840.113556.1.4.533</span></span>                                |
| <span data-ttu-id="6f4a7-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6f4a7-118">System-Id-Guid</span></span>    | <span data-ttu-id="6f4a7-119">5245801a-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6f4a7-119">5245801a-ca6a-11d0-afff-0000f80367c1</span></span>                  |
| <span data-ttu-id="6f4a7-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f4a7-120">Syntax</span></span>            | [<span data-ttu-id="6f4a7-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6f4a7-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6f4a7-122">Implementations</span></span>

-   [<span data-ttu-id="6f4a7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f4a7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f4a7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f4a7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f4a7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f4a7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f4a7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f4a7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6f4a7-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-130">Entry</span></span> | <span data-ttu-id="6f4a7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6f4a7-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6f4a7-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f4a7-134">System-Only</span></span>            | <span data-ttu-id="6f4a7-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-135">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6f4a7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6f4a7-137">True</span><span class="sxs-lookup"><span data-stu-id="6f4a7-137">True</span></span>                                                      |
| <span data-ttu-id="6f4a7-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6f4a7-138">Is Indexed</span></span>             | <span data-ttu-id="6f4a7-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-139">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6f4a7-140">In Global Catalog</span></span>      | <span data-ttu-id="6f4a7-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-141">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6f4a7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f4a7-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f4a7-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6f4a7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f4a7-144">Range-Lower</span></span>            | <span data-ttu-id="6f4a7-145">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-145">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f4a7-146">Range-Upper</span></span>            | <span data-ttu-id="6f4a7-147">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-147">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-148">Search-Flags</span></span>           | <span data-ttu-id="6f4a7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f4a7-149">0x00000000</span></span>                                                |
| <span data-ttu-id="6f4a7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-150">System-Flags</span></span>           | <span data-ttu-id="6f4a7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4a7-151">0x00000010</span></span>                                                |
| <span data-ttu-id="6f4a7-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6f4a7-152">Classes used in</span></span>        | [<span data-ttu-id="6f4a7-153">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f4a7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f4a7-154">Windows Server 2003</span></span>



| <span data-ttu-id="6f4a7-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-155">Entry</span></span> | <span data-ttu-id="6f4a7-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6f4a7-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6f4a7-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f4a7-159">System-Only</span></span>            | <span data-ttu-id="6f4a7-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-160">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6f4a7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6f4a7-162">True</span><span class="sxs-lookup"><span data-stu-id="6f4a7-162">True</span></span>                                                      |
| <span data-ttu-id="6f4a7-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6f4a7-163">Is Indexed</span></span>             | <span data-ttu-id="6f4a7-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-164">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6f4a7-165">In Global Catalog</span></span>      | <span data-ttu-id="6f4a7-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-166">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6f4a7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f4a7-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f4a7-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6f4a7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f4a7-169">Range-Lower</span></span>            | <span data-ttu-id="6f4a7-170">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-170">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f4a7-171">Range-Upper</span></span>            | <span data-ttu-id="6f4a7-172">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-172">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-173">Search-Flags</span></span>           | <span data-ttu-id="6f4a7-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f4a7-174">0x00000000</span></span>                                                |
| <span data-ttu-id="6f4a7-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-175">System-Flags</span></span>           | <span data-ttu-id="6f4a7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4a7-176">0x00000010</span></span>                                                |
| <span data-ttu-id="6f4a7-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6f4a7-177">Classes used in</span></span>        | [<span data-ttu-id="6f4a7-178">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f4a7-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f4a7-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f4a7-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-180">Entry</span></span> | <span data-ttu-id="6f4a7-181">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6f4a7-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6f4a7-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f4a7-184">System-Only</span></span>            | <span data-ttu-id="6f4a7-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-185">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6f4a7-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6f4a7-187">True</span><span class="sxs-lookup"><span data-stu-id="6f4a7-187">True</span></span>                                                      |
| <span data-ttu-id="6f4a7-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6f4a7-188">Is Indexed</span></span>             | <span data-ttu-id="6f4a7-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-189">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6f4a7-190">In Global Catalog</span></span>      | <span data-ttu-id="6f4a7-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-191">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6f4a7-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f4a7-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f4a7-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6f4a7-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f4a7-194">Range-Lower</span></span>            | <span data-ttu-id="6f4a7-195">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-195">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f4a7-196">Range-Upper</span></span>            | <span data-ttu-id="6f4a7-197">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-197">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-198">Search-Flags</span></span>           | <span data-ttu-id="6f4a7-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f4a7-199">0x00000000</span></span>                                                |
| <span data-ttu-id="6f4a7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-200">System-Flags</span></span>           | <span data-ttu-id="6f4a7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4a7-201">0x00000010</span></span>                                                |
| <span data-ttu-id="6f4a7-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6f4a7-202">Classes used in</span></span>        | [<span data-ttu-id="6f4a7-203">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f4a7-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f4a7-204">Windows Server 2008</span></span>



| <span data-ttu-id="6f4a7-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-205">Entry</span></span> | <span data-ttu-id="6f4a7-206">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6f4a7-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6f4a7-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f4a7-209">System-Only</span></span>            | <span data-ttu-id="6f4a7-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-210">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6f4a7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6f4a7-212">True</span><span class="sxs-lookup"><span data-stu-id="6f4a7-212">True</span></span>                                                      |
| <span data-ttu-id="6f4a7-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6f4a7-213">Is Indexed</span></span>             | <span data-ttu-id="6f4a7-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-214">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6f4a7-215">In Global Catalog</span></span>      | <span data-ttu-id="6f4a7-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-216">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6f4a7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f4a7-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f4a7-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6f4a7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f4a7-219">Range-Lower</span></span>            | <span data-ttu-id="6f4a7-220">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-220">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f4a7-221">Range-Upper</span></span>            | <span data-ttu-id="6f4a7-222">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-222">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-223">Search-Flags</span></span>           | <span data-ttu-id="6f4a7-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f4a7-224">0x00000000</span></span>                                                |
| <span data-ttu-id="6f4a7-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-225">System-Flags</span></span>           | <span data-ttu-id="6f4a7-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4a7-226">0x00000010</span></span>                                                |
| <span data-ttu-id="6f4a7-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6f4a7-227">Classes used in</span></span>        | [<span data-ttu-id="6f4a7-228">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f4a7-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f4a7-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f4a7-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-230">Entry</span></span> | <span data-ttu-id="6f4a7-231">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6f4a7-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6f4a7-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f4a7-234">System-Only</span></span>            | <span data-ttu-id="6f4a7-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-235">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6f4a7-236">Is-Single-Valued</span></span>       | <span data-ttu-id="6f4a7-237">True</span><span class="sxs-lookup"><span data-stu-id="6f4a7-237">True</span></span>                                                      |
| <span data-ttu-id="6f4a7-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6f4a7-238">Is Indexed</span></span>             | <span data-ttu-id="6f4a7-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-239">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6f4a7-240">In Global Catalog</span></span>      | <span data-ttu-id="6f4a7-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-241">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6f4a7-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f4a7-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f4a7-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6f4a7-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f4a7-244">Range-Lower</span></span>            | <span data-ttu-id="6f4a7-245">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-245">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f4a7-246">Range-Upper</span></span>            | <span data-ttu-id="6f4a7-247">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-247">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-248">Search-Flags</span></span>           | <span data-ttu-id="6f4a7-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f4a7-249">0x00000000</span></span>                                                |
| <span data-ttu-id="6f4a7-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-250">System-Flags</span></span>           | <span data-ttu-id="6f4a7-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4a7-251">0x00000010</span></span>                                                |
| <span data-ttu-id="6f4a7-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6f4a7-252">Classes used in</span></span>        | [<span data-ttu-id="6f4a7-253">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f4a7-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f4a7-254">Windows Server 2012</span></span>



| <span data-ttu-id="6f4a7-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="6f4a7-255">Entry</span></span> | <span data-ttu-id="6f4a7-256">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4a7-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6f4a7-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6f4a7-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f4a7-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6f4a7-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f4a7-259">System-Only</span></span>            | <span data-ttu-id="6f4a7-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-260">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6f4a7-261">Is-Single-Valued</span></span>       | <span data-ttu-id="6f4a7-262">True</span><span class="sxs-lookup"><span data-stu-id="6f4a7-262">True</span></span>                                                      |
| <span data-ttu-id="6f4a7-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6f4a7-263">Is Indexed</span></span>             | <span data-ttu-id="6f4a7-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-264">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6f4a7-265">In Global Catalog</span></span>      | <span data-ttu-id="6f4a7-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6f4a7-266">False</span></span>                                                     |
| <span data-ttu-id="6f4a7-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6f4a7-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f4a7-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f4a7-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6f4a7-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f4a7-269">Range-Lower</span></span>            | <span data-ttu-id="6f4a7-270">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-270">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f4a7-271">Range-Upper</span></span>            | <span data-ttu-id="6f4a7-272">16</span><span class="sxs-lookup"><span data-stu-id="6f4a7-272">16</span></span>                                                        |
| <span data-ttu-id="6f4a7-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-273">Search-Flags</span></span>           | <span data-ttu-id="6f4a7-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f4a7-274">0x00000000</span></span>                                                |
| <span data-ttu-id="6f4a7-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f4a7-275">System-Flags</span></span>           | <span data-ttu-id="6f4a7-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4a7-276">0x00000010</span></span>                                                |
| <span data-ttu-id="6f4a7-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6f4a7-277">Classes used in</span></span>        | [<span data-ttu-id="6f4a7-278">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6f4a7-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





