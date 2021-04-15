---
title: Print-степлер-атрибут, поддерживаемый
description: Значение TRUE, если принтер поддерживает сшивание. Предоставлено драйвером.
ms.assetid: c0d1cbc5-7657-45a8-b154-a67f57386f52
ms.tgt_platform: multiple
keywords:
- Печатная сшивка — схема AD атрибута, поддерживаемая
- Схема AD атрибута Принтстаплингсуппортед
topic_type:
- apiref
api_name:
- Print-Stapling-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12303d9a18f267ec4eaef3a33dc8ec7350967aa6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654792"
---
# <a name="print-stapling-supported-attribute"></a><span data-ttu-id="afefa-106">Print-степлер-атрибут, поддерживаемый</span><span class="sxs-lookup"><span data-stu-id="afefa-106">Print-Stapling-Supported attribute</span></span>

<span data-ttu-id="afefa-107">**Значение true** , если принтер поддерживает сшивание.</span><span class="sxs-lookup"><span data-stu-id="afefa-107">**TRUE** if the printer supports stapling.</span></span> <span data-ttu-id="afefa-108">Предоставлено драйвером.</span><span class="sxs-lookup"><span data-stu-id="afefa-108">Supplied by the driver.</span></span>



| <span data-ttu-id="afefa-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-109">Entry</span></span> | <span data-ttu-id="afefa-110">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="afefa-111">CN</span><span class="sxs-lookup"><span data-stu-id="afefa-111">CN</span></span>                | <span data-ttu-id="afefa-112">Печать — поддержка сшивания</span><span class="sxs-lookup"><span data-stu-id="afefa-112">Print-Stapling-Supported</span></span>             |
| <span data-ttu-id="afefa-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="afefa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="afefa-114">printStaplingSupported</span><span class="sxs-lookup"><span data-stu-id="afefa-114">printStaplingSupported</span></span>               |
| <span data-ttu-id="afefa-115">Размер</span><span class="sxs-lookup"><span data-stu-id="afefa-115">Size</span></span>              | <span data-ttu-id="afefa-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="afefa-116">4 bytes</span></span>                              |
| <span data-ttu-id="afefa-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="afefa-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="afefa-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="afefa-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="afefa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-119">Attribute-Id</span></span>      | <span data-ttu-id="afefa-120">1.2.840.113556.1.4.281</span><span class="sxs-lookup"><span data-stu-id="afefa-120">1.2.840.113556.1.4.281</span></span>               |
| <span data-ttu-id="afefa-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="afefa-121">System-Id-Guid</span></span>    | <span data-ttu-id="afefa-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="afefa-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span></span> |
| <span data-ttu-id="afefa-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afefa-123">Syntax</span></span>            | [<span data-ttu-id="afefa-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="afefa-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="afefa-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="afefa-125">Implementations</span></span>

-   [<span data-ttu-id="afefa-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="afefa-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="afefa-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afefa-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afefa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afefa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afefa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afefa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afefa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afefa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afefa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afefa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="afefa-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afefa-132">Windows 2000 Server</span></span>



| <span data-ttu-id="afefa-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-133">Entry</span></span> | <span data-ttu-id="afefa-134">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="afefa-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afefa-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="afefa-137">System-Only</span></span>            | <span data-ttu-id="afefa-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-138">False</span></span>                                          |
| <span data-ttu-id="afefa-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afefa-139">Is-Single-Valued</span></span>       | <span data-ttu-id="afefa-140">True</span><span class="sxs-lookup"><span data-stu-id="afefa-140">True</span></span>                                           |
| <span data-ttu-id="afefa-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afefa-141">Is Indexed</span></span>             | <span data-ttu-id="afefa-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-142">False</span></span>                                          |
| <span data-ttu-id="afefa-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afefa-143">In Global Catalog</span></span>      | <span data-ttu-id="afefa-144">True</span><span class="sxs-lookup"><span data-stu-id="afefa-144">True</span></span>                                           |
| <span data-ttu-id="afefa-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afefa-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="afefa-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afefa-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="afefa-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afefa-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="afefa-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afefa-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="afefa-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-149">Search-Flags</span></span>           | <span data-ttu-id="afefa-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afefa-150">0x00000000</span></span>                                     |
| <span data-ttu-id="afefa-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-151">System-Flags</span></span>           | <span data-ttu-id="afefa-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afefa-152">0x00000010</span></span>                                     |
| <span data-ttu-id="afefa-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afefa-153">Classes used in</span></span>        | [<span data-ttu-id="afefa-154">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="afefa-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="afefa-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afefa-155">Windows Server 2003</span></span>



| <span data-ttu-id="afefa-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-156">Entry</span></span> | <span data-ttu-id="afefa-157">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="afefa-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afefa-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="afefa-160">System-Only</span></span>            | <span data-ttu-id="afefa-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-161">False</span></span>                                          |
| <span data-ttu-id="afefa-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afefa-162">Is-Single-Valued</span></span>       | <span data-ttu-id="afefa-163">True</span><span class="sxs-lookup"><span data-stu-id="afefa-163">True</span></span>                                           |
| <span data-ttu-id="afefa-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afefa-164">Is Indexed</span></span>             | <span data-ttu-id="afefa-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-165">False</span></span>                                          |
| <span data-ttu-id="afefa-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afefa-166">In Global Catalog</span></span>      | <span data-ttu-id="afefa-167">True</span><span class="sxs-lookup"><span data-stu-id="afefa-167">True</span></span>                                           |
| <span data-ttu-id="afefa-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afefa-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="afefa-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afefa-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="afefa-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afefa-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="afefa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afefa-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="afefa-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-172">Search-Flags</span></span>           | <span data-ttu-id="afefa-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afefa-173">0x00000000</span></span>                                     |
| <span data-ttu-id="afefa-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-174">System-Flags</span></span>           | <span data-ttu-id="afefa-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afefa-175">0x00000010</span></span>                                     |
| <span data-ttu-id="afefa-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afefa-176">Classes used in</span></span>        | [<span data-ttu-id="afefa-177">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="afefa-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afefa-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afefa-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afefa-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-179">Entry</span></span> | <span data-ttu-id="afefa-180">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="afefa-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afefa-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="afefa-183">System-Only</span></span>            | <span data-ttu-id="afefa-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-184">False</span></span>                                          |
| <span data-ttu-id="afefa-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afefa-185">Is-Single-Valued</span></span>       | <span data-ttu-id="afefa-186">True</span><span class="sxs-lookup"><span data-stu-id="afefa-186">True</span></span>                                           |
| <span data-ttu-id="afefa-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afefa-187">Is Indexed</span></span>             | <span data-ttu-id="afefa-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-188">False</span></span>                                          |
| <span data-ttu-id="afefa-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afefa-189">In Global Catalog</span></span>      | <span data-ttu-id="afefa-190">True</span><span class="sxs-lookup"><span data-stu-id="afefa-190">True</span></span>                                           |
| <span data-ttu-id="afefa-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afefa-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="afefa-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afefa-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="afefa-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afefa-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="afefa-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afefa-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="afefa-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-195">Search-Flags</span></span>           | <span data-ttu-id="afefa-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afefa-196">0x00000000</span></span>                                     |
| <span data-ttu-id="afefa-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-197">System-Flags</span></span>           | <span data-ttu-id="afefa-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afefa-198">0x00000010</span></span>                                     |
| <span data-ttu-id="afefa-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afefa-199">Classes used in</span></span>        | [<span data-ttu-id="afefa-200">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="afefa-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afefa-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afefa-201">Windows Server 2008</span></span>



| <span data-ttu-id="afefa-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-202">Entry</span></span> | <span data-ttu-id="afefa-203">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="afefa-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afefa-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="afefa-206">System-Only</span></span>            | <span data-ttu-id="afefa-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-207">False</span></span>                                          |
| <span data-ttu-id="afefa-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afefa-208">Is-Single-Valued</span></span>       | <span data-ttu-id="afefa-209">True</span><span class="sxs-lookup"><span data-stu-id="afefa-209">True</span></span>                                           |
| <span data-ttu-id="afefa-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afefa-210">Is Indexed</span></span>             | <span data-ttu-id="afefa-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-211">False</span></span>                                          |
| <span data-ttu-id="afefa-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afefa-212">In Global Catalog</span></span>      | <span data-ttu-id="afefa-213">True</span><span class="sxs-lookup"><span data-stu-id="afefa-213">True</span></span>                                           |
| <span data-ttu-id="afefa-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afefa-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="afefa-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afefa-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="afefa-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afefa-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="afefa-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afefa-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="afefa-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-218">Search-Flags</span></span>           | <span data-ttu-id="afefa-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afefa-219">0x00000000</span></span>                                     |
| <span data-ttu-id="afefa-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-220">System-Flags</span></span>           | <span data-ttu-id="afefa-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afefa-221">0x00000010</span></span>                                     |
| <span data-ttu-id="afefa-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afefa-222">Classes used in</span></span>        | [<span data-ttu-id="afefa-223">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="afefa-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afefa-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afefa-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afefa-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-225">Entry</span></span> | <span data-ttu-id="afefa-226">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="afefa-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afefa-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="afefa-229">System-Only</span></span>            | <span data-ttu-id="afefa-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-230">False</span></span>                                          |
| <span data-ttu-id="afefa-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afefa-231">Is-Single-Valued</span></span>       | <span data-ttu-id="afefa-232">True</span><span class="sxs-lookup"><span data-stu-id="afefa-232">True</span></span>                                           |
| <span data-ttu-id="afefa-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afefa-233">Is Indexed</span></span>             | <span data-ttu-id="afefa-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-234">False</span></span>                                          |
| <span data-ttu-id="afefa-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afefa-235">In Global Catalog</span></span>      | <span data-ttu-id="afefa-236">True</span><span class="sxs-lookup"><span data-stu-id="afefa-236">True</span></span>                                           |
| <span data-ttu-id="afefa-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afefa-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="afefa-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afefa-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="afefa-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afefa-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="afefa-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afefa-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="afefa-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-241">Search-Flags</span></span>           | <span data-ttu-id="afefa-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afefa-242">0x00000000</span></span>                                     |
| <span data-ttu-id="afefa-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-243">System-Flags</span></span>           | <span data-ttu-id="afefa-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afefa-244">0x00000010</span></span>                                     |
| <span data-ttu-id="afefa-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afefa-245">Classes used in</span></span>        | [<span data-ttu-id="afefa-246">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="afefa-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afefa-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afefa-247">Windows Server 2012</span></span>



| <span data-ttu-id="afefa-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="afefa-248">Entry</span></span> | <span data-ttu-id="afefa-249">Значение</span><span class="sxs-lookup"><span data-stu-id="afefa-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="afefa-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afefa-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afefa-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="afefa-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="afefa-252">System-Only</span></span>            | <span data-ttu-id="afefa-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-253">False</span></span>                                          |
| <span data-ttu-id="afefa-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afefa-254">Is-Single-Valued</span></span>       | <span data-ttu-id="afefa-255">True</span><span class="sxs-lookup"><span data-stu-id="afefa-255">True</span></span>                                           |
| <span data-ttu-id="afefa-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afefa-256">Is Indexed</span></span>             | <span data-ttu-id="afefa-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="afefa-257">False</span></span>                                          |
| <span data-ttu-id="afefa-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afefa-258">In Global Catalog</span></span>      | <span data-ttu-id="afefa-259">True</span><span class="sxs-lookup"><span data-stu-id="afefa-259">True</span></span>                                           |
| <span data-ttu-id="afefa-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afefa-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="afefa-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afefa-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="afefa-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afefa-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="afefa-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afefa-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="afefa-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-264">Search-Flags</span></span>           | <span data-ttu-id="afefa-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afefa-265">0x00000000</span></span>                                     |
| <span data-ttu-id="afefa-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afefa-266">System-Flags</span></span>           | <span data-ttu-id="afefa-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afefa-267">0x00000010</span></span>                                     |
| <span data-ttu-id="afefa-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afefa-268">Classes used in</span></span>        | [<span data-ttu-id="afefa-269">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="afefa-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





