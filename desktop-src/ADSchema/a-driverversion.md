---
title: Атрибут Driver-Version
description: Номер версии драйвера устройства.
ms.assetid: 915690aa-1a5e-4cef-8737-6a44e935d33a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Driver-Version
- Схема AD атрибута Дриверверсион
topic_type:
- apiref
api_name:
- Driver-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc7bf7f0ae559028d942e801a8f91f81a18a9a8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654959"
---
# <a name="driver-version-attribute"></a><span data-ttu-id="b9f2c-105">Атрибут Driver-Version</span><span class="sxs-lookup"><span data-stu-id="b9f2c-105">Driver-Version attribute</span></span>

<span data-ttu-id="b9f2c-106">Номер версии драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="b9f2c-106">The Version number of device driver.</span></span>



| <span data-ttu-id="b9f2c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-107">Entry</span></span> | <span data-ttu-id="b9f2c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b9f2c-109">CN</span><span class="sxs-lookup"><span data-stu-id="b9f2c-109">CN</span></span>                | <span data-ttu-id="b9f2c-110">Driver-Version</span><span class="sxs-lookup"><span data-stu-id="b9f2c-110">Driver-Version</span></span>                       |
| <span data-ttu-id="b9f2c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b9f2c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b9f2c-112">driverVersion</span><span class="sxs-lookup"><span data-stu-id="b9f2c-112">driverVersion</span></span>                        |
| <span data-ttu-id="b9f2c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b9f2c-113">Size</span></span>              | <span data-ttu-id="b9f2c-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="b9f2c-114">4 bytes</span></span>                              |
| <span data-ttu-id="b9f2c-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b9f2c-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b9f2c-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b9f2c-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b9f2c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-117">Attribute-Id</span></span>      | <span data-ttu-id="b9f2c-118">1.2.840.113556.1.4.276</span><span class="sxs-lookup"><span data-stu-id="b9f2c-118">1.2.840.113556.1.4.276</span></span>               |
| <span data-ttu-id="b9f2c-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b9f2c-119">System-Id-Guid</span></span>    | <span data-ttu-id="b9f2c-120">ba305f6e-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b9f2c-120">ba305f6e-47e3-11d0-a1a6-00c04fd930c9</span></span> |
| <span data-ttu-id="b9f2c-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9f2c-121">Syntax</span></span>            | [<span data-ttu-id="b9f2c-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b9f2c-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b9f2c-123">Implementations</span></span>

-   [<span data-ttu-id="b9f2c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b9f2c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b9f2c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b9f2c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b9f2c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b9f2c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b9f2c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b9f2c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b9f2c-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-131">Entry</span></span> | <span data-ttu-id="b9f2c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b9f2c-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f2c-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f2c-135">System-Only</span></span>            | <span data-ttu-id="b9f2c-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-136">False</span></span>                                          |
| <span data-ttu-id="b9f2c-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f2c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f2c-138">True</span><span class="sxs-lookup"><span data-stu-id="b9f2c-138">True</span></span>                                           |
| <span data-ttu-id="b9f2c-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f2c-139">Is Indexed</span></span>             | <span data-ttu-id="b9f2c-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-140">False</span></span>                                          |
| <span data-ttu-id="b9f2c-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f2c-141">In Global Catalog</span></span>      | <span data-ttu-id="b9f2c-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-142">False</span></span>                                          |
| <span data-ttu-id="b9f2c-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f2c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f2c-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f2c-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b9f2c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f2c-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f2c-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-147">Search-Flags</span></span>           | <span data-ttu-id="b9f2c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f2c-148">0x00000000</span></span>                                     |
| <span data-ttu-id="b9f2c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-149">System-Flags</span></span>           | <span data-ttu-id="b9f2c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f2c-150">0x00000010</span></span>                                     |
| <span data-ttu-id="b9f2c-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f2c-151">Classes used in</span></span>        | [<span data-ttu-id="b9f2c-152">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b9f2c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9f2c-153">Windows Server 2003</span></span>



| <span data-ttu-id="b9f2c-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-154">Entry</span></span> | <span data-ttu-id="b9f2c-155">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b9f2c-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f2c-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f2c-158">System-Only</span></span>            | <span data-ttu-id="b9f2c-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-159">False</span></span>                                          |
| <span data-ttu-id="b9f2c-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f2c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f2c-161">True</span><span class="sxs-lookup"><span data-stu-id="b9f2c-161">True</span></span>                                           |
| <span data-ttu-id="b9f2c-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f2c-162">Is Indexed</span></span>             | <span data-ttu-id="b9f2c-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-163">False</span></span>                                          |
| <span data-ttu-id="b9f2c-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f2c-164">In Global Catalog</span></span>      | <span data-ttu-id="b9f2c-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-165">False</span></span>                                          |
| <span data-ttu-id="b9f2c-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f2c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f2c-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f2c-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b9f2c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f2c-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f2c-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-170">Search-Flags</span></span>           | <span data-ttu-id="b9f2c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f2c-171">0x00000000</span></span>                                     |
| <span data-ttu-id="b9f2c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-172">System-Flags</span></span>           | <span data-ttu-id="b9f2c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f2c-173">0x00000010</span></span>                                     |
| <span data-ttu-id="b9f2c-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f2c-174">Classes used in</span></span>        | [<span data-ttu-id="b9f2c-175">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b9f2c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b9f2c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b9f2c-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-177">Entry</span></span> | <span data-ttu-id="b9f2c-178">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b9f2c-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f2c-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f2c-181">System-Only</span></span>            | <span data-ttu-id="b9f2c-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-182">False</span></span>                                          |
| <span data-ttu-id="b9f2c-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f2c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f2c-184">True</span><span class="sxs-lookup"><span data-stu-id="b9f2c-184">True</span></span>                                           |
| <span data-ttu-id="b9f2c-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f2c-185">Is Indexed</span></span>             | <span data-ttu-id="b9f2c-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-186">False</span></span>                                          |
| <span data-ttu-id="b9f2c-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f2c-187">In Global Catalog</span></span>      | <span data-ttu-id="b9f2c-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-188">False</span></span>                                          |
| <span data-ttu-id="b9f2c-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f2c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f2c-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f2c-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b9f2c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f2c-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f2c-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-193">Search-Flags</span></span>           | <span data-ttu-id="b9f2c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f2c-194">0x00000000</span></span>                                     |
| <span data-ttu-id="b9f2c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-195">System-Flags</span></span>           | <span data-ttu-id="b9f2c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f2c-196">0x00000010</span></span>                                     |
| <span data-ttu-id="b9f2c-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f2c-197">Classes used in</span></span>        | [<span data-ttu-id="b9f2c-198">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b9f2c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9f2c-199">Windows Server 2008</span></span>



| <span data-ttu-id="b9f2c-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-200">Entry</span></span> | <span data-ttu-id="b9f2c-201">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b9f2c-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f2c-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f2c-204">System-Only</span></span>            | <span data-ttu-id="b9f2c-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-205">False</span></span>                                          |
| <span data-ttu-id="b9f2c-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f2c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f2c-207">True</span><span class="sxs-lookup"><span data-stu-id="b9f2c-207">True</span></span>                                           |
| <span data-ttu-id="b9f2c-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f2c-208">Is Indexed</span></span>             | <span data-ttu-id="b9f2c-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-209">False</span></span>                                          |
| <span data-ttu-id="b9f2c-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f2c-210">In Global Catalog</span></span>      | <span data-ttu-id="b9f2c-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-211">False</span></span>                                          |
| <span data-ttu-id="b9f2c-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f2c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f2c-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f2c-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b9f2c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f2c-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f2c-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-216">Search-Flags</span></span>           | <span data-ttu-id="b9f2c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f2c-217">0x00000000</span></span>                                     |
| <span data-ttu-id="b9f2c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-218">System-Flags</span></span>           | <span data-ttu-id="b9f2c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f2c-219">0x00000010</span></span>                                     |
| <span data-ttu-id="b9f2c-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f2c-220">Classes used in</span></span>        | [<span data-ttu-id="b9f2c-221">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b9f2c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9f2c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b9f2c-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-223">Entry</span></span> | <span data-ttu-id="b9f2c-224">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b9f2c-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f2c-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f2c-227">System-Only</span></span>            | <span data-ttu-id="b9f2c-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-228">False</span></span>                                          |
| <span data-ttu-id="b9f2c-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f2c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f2c-230">True</span><span class="sxs-lookup"><span data-stu-id="b9f2c-230">True</span></span>                                           |
| <span data-ttu-id="b9f2c-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f2c-231">Is Indexed</span></span>             | <span data-ttu-id="b9f2c-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-232">False</span></span>                                          |
| <span data-ttu-id="b9f2c-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f2c-233">In Global Catalog</span></span>      | <span data-ttu-id="b9f2c-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-234">False</span></span>                                          |
| <span data-ttu-id="b9f2c-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f2c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f2c-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f2c-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b9f2c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f2c-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f2c-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-239">Search-Flags</span></span>           | <span data-ttu-id="b9f2c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f2c-240">0x00000000</span></span>                                     |
| <span data-ttu-id="b9f2c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-241">System-Flags</span></span>           | <span data-ttu-id="b9f2c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f2c-242">0x00000010</span></span>                                     |
| <span data-ttu-id="b9f2c-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f2c-243">Classes used in</span></span>        | [<span data-ttu-id="b9f2c-244">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b9f2c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9f2c-245">Windows Server 2012</span></span>



| <span data-ttu-id="b9f2c-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f2c-246">Entry</span></span> | <span data-ttu-id="b9f2c-247">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f2c-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b9f2c-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f2c-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f2c-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b9f2c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f2c-250">System-Only</span></span>            | <span data-ttu-id="b9f2c-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-251">False</span></span>                                          |
| <span data-ttu-id="b9f2c-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f2c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f2c-253">True</span><span class="sxs-lookup"><span data-stu-id="b9f2c-253">True</span></span>                                           |
| <span data-ttu-id="b9f2c-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f2c-254">Is Indexed</span></span>             | <span data-ttu-id="b9f2c-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-255">False</span></span>                                          |
| <span data-ttu-id="b9f2c-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f2c-256">In Global Catalog</span></span>      | <span data-ttu-id="b9f2c-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f2c-257">False</span></span>                                          |
| <span data-ttu-id="b9f2c-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f2c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f2c-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f2c-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b9f2c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f2c-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f2c-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b9f2c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-262">Search-Flags</span></span>           | <span data-ttu-id="b9f2c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f2c-263">0x00000000</span></span>                                     |
| <span data-ttu-id="b9f2c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f2c-264">System-Flags</span></span>           | <span data-ttu-id="b9f2c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f2c-265">0x00000010</span></span>                                     |
| <span data-ttu-id="b9f2c-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f2c-266">Classes used in</span></span>        | [<span data-ttu-id="b9f2c-267">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b9f2c-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





