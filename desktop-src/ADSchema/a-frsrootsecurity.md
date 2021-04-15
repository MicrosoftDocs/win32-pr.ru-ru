---
title: FRS-root-атрибут безопасности
description: Дескриптор безопасности корня набора реплик для репликации файлов.
ms.assetid: 1db92f68-465a-4d93-ad4d-706ef4761ddc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов FRS-root-Security
- Схема AD атрибута Фрсрутсекурити
topic_type:
- apiref
api_name:
- FRS-Root-Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84059902998b120ad38215257fdddcb1c21ea6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654842"
---
# <a name="frs-root-security-attribute"></a><span data-ttu-id="1b75a-105">FRS-root-атрибут безопасности</span><span class="sxs-lookup"><span data-stu-id="1b75a-105">FRS-Root-Security attribute</span></span>

<span data-ttu-id="1b75a-106">Дескриптор безопасности корня набора реплик для репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="1b75a-106">The security descriptor of replica set root for file replication.</span></span>



| <span data-ttu-id="1b75a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-107">Entry</span></span> | <span data-ttu-id="1b75a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="1b75a-109">CN</span><span class="sxs-lookup"><span data-stu-id="1b75a-109">CN</span></span>                | <span data-ttu-id="1b75a-110">FRS-root-Security</span><span class="sxs-lookup"><span data-stu-id="1b75a-110">FRS-Root-Security</span></span>                                   |
| <span data-ttu-id="1b75a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1b75a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1b75a-112">фрсрутсекурити</span><span class="sxs-lookup"><span data-stu-id="1b75a-112">fRSRootSecurity</span></span>                                     |
| <span data-ttu-id="1b75a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1b75a-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="1b75a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1b75a-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="1b75a-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1b75a-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="1b75a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-116">Attribute-Id</span></span>      | <span data-ttu-id="1b75a-117">1.2.840.113556.1.4.535</span><span class="sxs-lookup"><span data-stu-id="1b75a-117">1.2.840.113556.1.4.535</span></span>                              |
| <span data-ttu-id="1b75a-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1b75a-118">System-Id-Guid</span></span>    | <span data-ttu-id="1b75a-119">5245801f-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1b75a-119">5245801f-ca6a-11d0-afff-0000f80367c1</span></span>                |
| <span data-ttu-id="1b75a-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b75a-120">Syntax</span></span>            | [<span data-ttu-id="1b75a-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="1b75a-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="1b75a-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1b75a-122">Implementations</span></span>

-   [<span data-ttu-id="1b75a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1b75a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1b75a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b75a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b75a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b75a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b75a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b75a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b75a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b75a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b75a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b75a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1b75a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b75a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1b75a-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-130">Entry</span></span> | <span data-ttu-id="1b75a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b75a-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1b75a-132">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-133">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b75a-134">System-Only</span></span>            | <span data-ttu-id="1b75a-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-135">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1b75a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1b75a-137">True</span><span class="sxs-lookup"><span data-stu-id="1b75a-137">True</span></span>                                                                                                       |
| <span data-ttu-id="1b75a-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1b75a-138">Is Indexed</span></span>             | <span data-ttu-id="1b75a-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-139">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1b75a-140">In Global Catalog</span></span>      | <span data-ttu-id="1b75a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-141">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1b75a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b75a-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b75a-143">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b75a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b75a-144">Range-Lower</span></span>            | <span data-ttu-id="1b75a-145">0</span><span class="sxs-lookup"><span data-stu-id="1b75a-145">0</span></span>                                                                                                          |
| <span data-ttu-id="1b75a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b75a-146">Range-Upper</span></span>            | <span data-ttu-id="1b75a-147">65535</span><span class="sxs-lookup"><span data-stu-id="1b75a-147">65535</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-148">Search-Flags</span></span>           | <span data-ttu-id="1b75a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b75a-149">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-150">System-Flags</span></span>           | <span data-ttu-id="1b75a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b75a-151">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1b75a-152">Classes used in</span></span>        | [<span data-ttu-id="1b75a-153">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="1b75a-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b75a-154">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="1b75a-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1b75a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b75a-155">Windows Server 2003</span></span>



| <span data-ttu-id="1b75a-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-156">Entry</span></span> | <span data-ttu-id="1b75a-157">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b75a-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1b75a-158">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-159">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b75a-160">System-Only</span></span>            | <span data-ttu-id="1b75a-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-161">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1b75a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1b75a-163">True</span><span class="sxs-lookup"><span data-stu-id="1b75a-163">True</span></span>                                                                                                       |
| <span data-ttu-id="1b75a-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1b75a-164">Is Indexed</span></span>             | <span data-ttu-id="1b75a-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-165">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1b75a-166">In Global Catalog</span></span>      | <span data-ttu-id="1b75a-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-167">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1b75a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b75a-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b75a-169">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b75a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b75a-170">Range-Lower</span></span>            | <span data-ttu-id="1b75a-171">0</span><span class="sxs-lookup"><span data-stu-id="1b75a-171">0</span></span>                                                                                                          |
| <span data-ttu-id="1b75a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b75a-172">Range-Upper</span></span>            | <span data-ttu-id="1b75a-173">65535</span><span class="sxs-lookup"><span data-stu-id="1b75a-173">65535</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-174">Search-Flags</span></span>           | <span data-ttu-id="1b75a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b75a-175">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-176">System-Flags</span></span>           | <span data-ttu-id="1b75a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b75a-177">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1b75a-178">Classes used in</span></span>        | [<span data-ttu-id="1b75a-179">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="1b75a-179">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b75a-180">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="1b75a-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b75a-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b75a-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b75a-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-182">Entry</span></span> | <span data-ttu-id="1b75a-183">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-183">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b75a-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1b75a-184">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-185">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b75a-186">System-Only</span></span>            | <span data-ttu-id="1b75a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-187">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1b75a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1b75a-189">True</span><span class="sxs-lookup"><span data-stu-id="1b75a-189">True</span></span>                                                                                                       |
| <span data-ttu-id="1b75a-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1b75a-190">Is Indexed</span></span>             | <span data-ttu-id="1b75a-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-191">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1b75a-192">In Global Catalog</span></span>      | <span data-ttu-id="1b75a-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-193">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1b75a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b75a-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b75a-195">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b75a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b75a-196">Range-Lower</span></span>            | <span data-ttu-id="1b75a-197">0</span><span class="sxs-lookup"><span data-stu-id="1b75a-197">0</span></span>                                                                                                          |
| <span data-ttu-id="1b75a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b75a-198">Range-Upper</span></span>            | <span data-ttu-id="1b75a-199">65535</span><span class="sxs-lookup"><span data-stu-id="1b75a-199">65535</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-200">Search-Flags</span></span>           | <span data-ttu-id="1b75a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b75a-201">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-202">System-Flags</span></span>           | <span data-ttu-id="1b75a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b75a-203">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1b75a-204">Classes used in</span></span>        | [<span data-ttu-id="1b75a-205">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="1b75a-205">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b75a-206">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="1b75a-206">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b75a-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b75a-207">Windows Server 2008</span></span>



| <span data-ttu-id="1b75a-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-208">Entry</span></span> | <span data-ttu-id="1b75a-209">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-209">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b75a-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1b75a-210">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-211">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b75a-212">System-Only</span></span>            | <span data-ttu-id="1b75a-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-213">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1b75a-214">Is-Single-Valued</span></span>       | <span data-ttu-id="1b75a-215">True</span><span class="sxs-lookup"><span data-stu-id="1b75a-215">True</span></span>                                                                                                       |
| <span data-ttu-id="1b75a-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1b75a-216">Is Indexed</span></span>             | <span data-ttu-id="1b75a-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-217">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1b75a-218">In Global Catalog</span></span>      | <span data-ttu-id="1b75a-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-219">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1b75a-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b75a-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b75a-221">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b75a-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b75a-222">Range-Lower</span></span>            | <span data-ttu-id="1b75a-223">0</span><span class="sxs-lookup"><span data-stu-id="1b75a-223">0</span></span>                                                                                                          |
| <span data-ttu-id="1b75a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b75a-224">Range-Upper</span></span>            | <span data-ttu-id="1b75a-225">65535</span><span class="sxs-lookup"><span data-stu-id="1b75a-225">65535</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-226">Search-Flags</span></span>           | <span data-ttu-id="1b75a-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b75a-227">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-228">System-Flags</span></span>           | <span data-ttu-id="1b75a-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b75a-229">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1b75a-230">Classes used in</span></span>        | [<span data-ttu-id="1b75a-231">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="1b75a-231">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b75a-232">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="1b75a-232">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b75a-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b75a-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b75a-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-234">Entry</span></span> | <span data-ttu-id="1b75a-235">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-235">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b75a-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1b75a-236">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-237">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b75a-238">System-Only</span></span>            | <span data-ttu-id="1b75a-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-239">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1b75a-240">Is-Single-Valued</span></span>       | <span data-ttu-id="1b75a-241">True</span><span class="sxs-lookup"><span data-stu-id="1b75a-241">True</span></span>                                                                                                       |
| <span data-ttu-id="1b75a-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1b75a-242">Is Indexed</span></span>             | <span data-ttu-id="1b75a-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-243">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1b75a-244">In Global Catalog</span></span>      | <span data-ttu-id="1b75a-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-245">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1b75a-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b75a-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b75a-247">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b75a-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b75a-248">Range-Lower</span></span>            | <span data-ttu-id="1b75a-249">0</span><span class="sxs-lookup"><span data-stu-id="1b75a-249">0</span></span>                                                                                                          |
| <span data-ttu-id="1b75a-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b75a-250">Range-Upper</span></span>            | <span data-ttu-id="1b75a-251">65535</span><span class="sxs-lookup"><span data-stu-id="1b75a-251">65535</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-252">Search-Flags</span></span>           | <span data-ttu-id="1b75a-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b75a-253">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-254">System-Flags</span></span>           | <span data-ttu-id="1b75a-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b75a-255">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-256">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1b75a-256">Classes used in</span></span>        | [<span data-ttu-id="1b75a-257">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="1b75a-257">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b75a-258">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="1b75a-258">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b75a-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b75a-259">Windows Server 2012</span></span>



| <span data-ttu-id="1b75a-260">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b75a-260">Entry</span></span> | <span data-ttu-id="1b75a-261">Значение</span><span class="sxs-lookup"><span data-stu-id="1b75a-261">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b75a-262">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1b75a-262">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b75a-263">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b75a-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b75a-264">System-Only</span></span>            | <span data-ttu-id="1b75a-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-265">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-266">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1b75a-266">Is-Single-Valued</span></span>       | <span data-ttu-id="1b75a-267">True</span><span class="sxs-lookup"><span data-stu-id="1b75a-267">True</span></span>                                                                                                       |
| <span data-ttu-id="1b75a-268">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1b75a-268">Is Indexed</span></span>             | <span data-ttu-id="1b75a-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-269">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-270">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1b75a-270">In Global Catalog</span></span>      | <span data-ttu-id="1b75a-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="1b75a-271">False</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-272">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1b75a-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b75a-273">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b75a-273">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b75a-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b75a-274">Range-Lower</span></span>            | <span data-ttu-id="1b75a-275">0</span><span class="sxs-lookup"><span data-stu-id="1b75a-275">0</span></span>                                                                                                          |
| <span data-ttu-id="1b75a-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b75a-276">Range-Upper</span></span>            | <span data-ttu-id="1b75a-277">65535</span><span class="sxs-lookup"><span data-stu-id="1b75a-277">65535</span></span>                                                                                                      |
| <span data-ttu-id="1b75a-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-278">Search-Flags</span></span>           | <span data-ttu-id="1b75a-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b75a-279">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b75a-280">System-Flags</span></span>           | <span data-ttu-id="1b75a-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b75a-281">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b75a-282">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1b75a-282">Classes used in</span></span>        | [<span data-ttu-id="1b75a-283">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="1b75a-283">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b75a-284">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="1b75a-284">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





