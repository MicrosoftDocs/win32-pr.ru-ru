---
title: FRS-Update — атрибут timeout
description: Максимальное время (в минутах) ожидания завершения обновления.
ms.assetid: 0c06510e-d4a8-42f8-bf81-13a9f103e237
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени ожидания FRS
- Схема AD атрибута Фрсупдатетимеаут
topic_type:
- apiref
api_name:
- FRS-Update-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73730ec18942f98c07c0a4756bb8c7716e6abfd2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536098"
---
# <a name="frs-update-timeout-attribute"></a><span data-ttu-id="8eb3d-105">FRS-Update — атрибут timeout</span><span class="sxs-lookup"><span data-stu-id="8eb3d-105">FRS-Update-Timeout attribute</span></span>

<span data-ttu-id="8eb3d-106">Максимальное время (в минутах) ожидания завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="8eb3d-106">The maximum time, in minutes, to wait to complete an update before giving up.</span></span>



| <span data-ttu-id="8eb3d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-107">Entry</span></span> | <span data-ttu-id="8eb3d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8eb3d-109">CN</span><span class="sxs-lookup"><span data-stu-id="8eb3d-109">CN</span></span>                | <span data-ttu-id="8eb3d-110">FRS-Update — время ожидания</span><span class="sxs-lookup"><span data-stu-id="8eb3d-110">FRS-Update-Timeout</span></span>                   |
| <span data-ttu-id="8eb3d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8eb3d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8eb3d-112">фрсупдатетимеаут</span><span class="sxs-lookup"><span data-stu-id="8eb3d-112">fRSUpdateTimeout</span></span>                     |
| <span data-ttu-id="8eb3d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8eb3d-113">Size</span></span>              | <span data-ttu-id="8eb3d-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="8eb3d-114">4 bytes</span></span>                              |
| <span data-ttu-id="8eb3d-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8eb3d-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8eb3d-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8eb3d-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8eb3d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-117">Attribute-Id</span></span>      | <span data-ttu-id="8eb3d-118">1.2.840.113556.1.4.485</span><span class="sxs-lookup"><span data-stu-id="8eb3d-118">1.2.840.113556.1.4.485</span></span>               |
| <span data-ttu-id="8eb3d-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8eb3d-119">System-Id-Guid</span></span>    | <span data-ttu-id="8eb3d-120">1be8f172-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="8eb3d-120">1be8f172-a9ff-11d0-afe2-00c04fd930c9</span></span> |
| <span data-ttu-id="8eb3d-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8eb3d-121">Syntax</span></span>            | [<span data-ttu-id="8eb3d-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8eb3d-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8eb3d-123">Implementations</span></span>

-   [<span data-ttu-id="8eb3d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8eb3d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8eb3d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8eb3d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8eb3d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8eb3d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8eb3d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8eb3d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8eb3d-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-131">Entry</span></span> | <span data-ttu-id="8eb3d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3d-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8eb3d-133">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-134">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8eb3d-135">System-Only</span></span>            | <span data-ttu-id="8eb3d-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-136">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8eb3d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8eb3d-138">True</span><span class="sxs-lookup"><span data-stu-id="8eb3d-138">True</span></span>                                                                                                      |
| <span data-ttu-id="8eb3d-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8eb3d-139">Is Indexed</span></span>             | <span data-ttu-id="8eb3d-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-140">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8eb3d-141">In Global Catalog</span></span>      | <span data-ttu-id="8eb3d-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-142">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8eb3d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8eb3d-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8eb3d-144">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="8eb3d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8eb3d-145">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8eb3d-146">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-147">Search-Flags</span></span>           | <span data-ttu-id="8eb3d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8eb3d-148">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-149">System-Flags</span></span>           | <span data-ttu-id="8eb3d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8eb3d-150">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8eb3d-151">Classes used in</span></span>        | [<span data-ttu-id="8eb3d-152">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-152">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8eb3d-153">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-153">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8eb3d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8eb3d-154">Windows Server 2003</span></span>



| <span data-ttu-id="8eb3d-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-155">Entry</span></span> | <span data-ttu-id="8eb3d-156">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-156">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3d-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8eb3d-157">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-158">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8eb3d-159">System-Only</span></span>            | <span data-ttu-id="8eb3d-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-160">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8eb3d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8eb3d-162">True</span><span class="sxs-lookup"><span data-stu-id="8eb3d-162">True</span></span>                                                                                                      |
| <span data-ttu-id="8eb3d-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8eb3d-163">Is Indexed</span></span>             | <span data-ttu-id="8eb3d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-164">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8eb3d-165">In Global Catalog</span></span>      | <span data-ttu-id="8eb3d-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-166">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8eb3d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8eb3d-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8eb3d-168">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="8eb3d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8eb3d-169">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8eb3d-170">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-171">Search-Flags</span></span>           | <span data-ttu-id="8eb3d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8eb3d-172">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-173">System-Flags</span></span>           | <span data-ttu-id="8eb3d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8eb3d-174">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8eb3d-175">Classes used in</span></span>        | [<span data-ttu-id="8eb3d-176">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-176">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8eb3d-177">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-177">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8eb3d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8eb3d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8eb3d-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-179">Entry</span></span> | <span data-ttu-id="8eb3d-180">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-180">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3d-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8eb3d-181">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-182">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="8eb3d-183">System-Only</span></span>            | <span data-ttu-id="8eb3d-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-184">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8eb3d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="8eb3d-186">True</span><span class="sxs-lookup"><span data-stu-id="8eb3d-186">True</span></span>                                                                                                      |
| <span data-ttu-id="8eb3d-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8eb3d-187">Is Indexed</span></span>             | <span data-ttu-id="8eb3d-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-188">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8eb3d-189">In Global Catalog</span></span>      | <span data-ttu-id="8eb3d-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-190">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8eb3d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="8eb3d-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8eb3d-192">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="8eb3d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8eb3d-193">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8eb3d-194">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-195">Search-Flags</span></span>           | <span data-ttu-id="8eb3d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8eb3d-196">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-197">System-Flags</span></span>           | <span data-ttu-id="8eb3d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8eb3d-198">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8eb3d-199">Classes used in</span></span>        | [<span data-ttu-id="8eb3d-200">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-200">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8eb3d-201">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-201">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8eb3d-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eb3d-202">Windows Server 2008</span></span>



| <span data-ttu-id="8eb3d-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-203">Entry</span></span> | <span data-ttu-id="8eb3d-204">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3d-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8eb3d-205">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-206">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="8eb3d-207">System-Only</span></span>            | <span data-ttu-id="8eb3d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-208">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8eb3d-209">Is-Single-Valued</span></span>       | <span data-ttu-id="8eb3d-210">True</span><span class="sxs-lookup"><span data-stu-id="8eb3d-210">True</span></span>                                                                                                      |
| <span data-ttu-id="8eb3d-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8eb3d-211">Is Indexed</span></span>             | <span data-ttu-id="8eb3d-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-212">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8eb3d-213">In Global Catalog</span></span>      | <span data-ttu-id="8eb3d-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-214">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8eb3d-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="8eb3d-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8eb3d-216">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="8eb3d-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8eb3d-217">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8eb3d-218">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-219">Search-Flags</span></span>           | <span data-ttu-id="8eb3d-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8eb3d-220">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-221">System-Flags</span></span>           | <span data-ttu-id="8eb3d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8eb3d-222">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8eb3d-223">Classes used in</span></span>        | [<span data-ttu-id="8eb3d-224">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-224">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8eb3d-225">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-225">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8eb3d-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8eb3d-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8eb3d-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-227">Entry</span></span> | <span data-ttu-id="8eb3d-228">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-228">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3d-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8eb3d-229">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-230">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="8eb3d-231">System-Only</span></span>            | <span data-ttu-id="8eb3d-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-232">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8eb3d-233">Is-Single-Valued</span></span>       | <span data-ttu-id="8eb3d-234">True</span><span class="sxs-lookup"><span data-stu-id="8eb3d-234">True</span></span>                                                                                                      |
| <span data-ttu-id="8eb3d-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8eb3d-235">Is Indexed</span></span>             | <span data-ttu-id="8eb3d-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-236">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8eb3d-237">In Global Catalog</span></span>      | <span data-ttu-id="8eb3d-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-238">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8eb3d-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="8eb3d-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8eb3d-240">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="8eb3d-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8eb3d-241">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8eb3d-242">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-243">Search-Flags</span></span>           | <span data-ttu-id="8eb3d-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8eb3d-244">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-245">System-Flags</span></span>           | <span data-ttu-id="8eb3d-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8eb3d-246">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8eb3d-247">Classes used in</span></span>        | [<span data-ttu-id="8eb3d-248">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-248">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8eb3d-249">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-249">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8eb3d-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8eb3d-250">Windows Server 2012</span></span>



| <span data-ttu-id="8eb3d-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="8eb3d-251">Entry</span></span> | <span data-ttu-id="8eb3d-252">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb3d-252">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3d-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8eb3d-253">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8eb3d-254">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="8eb3d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="8eb3d-255">System-Only</span></span>            | <span data-ttu-id="8eb3d-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-256">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8eb3d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="8eb3d-258">True</span><span class="sxs-lookup"><span data-stu-id="8eb3d-258">True</span></span>                                                                                                      |
| <span data-ttu-id="8eb3d-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8eb3d-259">Is Indexed</span></span>             | <span data-ttu-id="8eb3d-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-260">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8eb3d-261">In Global Catalog</span></span>      | <span data-ttu-id="8eb3d-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="8eb3d-262">False</span></span>                                                                                                     |
| <span data-ttu-id="8eb3d-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8eb3d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="8eb3d-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8eb3d-264">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="8eb3d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8eb3d-265">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8eb3d-266">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="8eb3d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-267">Search-Flags</span></span>           | <span data-ttu-id="8eb3d-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8eb3d-268">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8eb3d-269">System-Flags</span></span>           | <span data-ttu-id="8eb3d-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8eb3d-270">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="8eb3d-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8eb3d-271">Classes used in</span></span>        | [<span data-ttu-id="8eb3d-272">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-272">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8eb3d-273">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="8eb3d-273">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



 

 





