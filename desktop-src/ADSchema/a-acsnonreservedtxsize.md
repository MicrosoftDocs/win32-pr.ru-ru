---
title: ACS-не зарезервированный — атрибут размера TX
description: Размер контейнера маркера, который приложение может использовать перед резервированием.
ms.assetid: 67a0d6fd-b556-49d2-8c5b-6efebf1052c3
ms.tgt_platform: multiple
keywords:
- ACS-незарезервированная — схема AD атрибута размера TX
- Схема AD атрибута Акснонресерведткссизе
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cd19dde97e3a9fc6ef58165c8dbcbfbebba729
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893998"
---
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="e2747-105">ACS-не зарезервированный — атрибут размера TX</span><span class="sxs-lookup"><span data-stu-id="e2747-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="e2747-106">Размер контейнера маркера, который приложение может использовать перед резервированием.</span><span class="sxs-lookup"><span data-stu-id="e2747-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="e2747-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-107">Entry</span></span> | <span data-ttu-id="e2747-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e2747-109">CN</span><span class="sxs-lookup"><span data-stu-id="e2747-109">CN</span></span>                | <span data-ttu-id="e2747-110">ACS — не зарезервировано — размер TX</span><span class="sxs-lookup"><span data-stu-id="e2747-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="e2747-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e2747-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e2747-112">акснонресерведткссизе</span><span class="sxs-lookup"><span data-stu-id="e2747-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="e2747-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e2747-113">Size</span></span>              | <span data-ttu-id="e2747-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="e2747-114">8 bytes</span></span>                              |
| <span data-ttu-id="e2747-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e2747-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e2747-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e2747-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e2747-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-117">Attribute-Id</span></span>      | <span data-ttu-id="e2747-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="e2747-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="e2747-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e2747-119">System-Id-Guid</span></span>    | <span data-ttu-id="e2747-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e2747-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="e2747-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2747-121">Syntax</span></span>            | [<span data-ttu-id="e2747-122">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="e2747-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e2747-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e2747-123">Implementations</span></span>

-   [<span data-ttu-id="e2747-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e2747-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e2747-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e2747-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e2747-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e2747-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e2747-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e2747-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e2747-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e2747-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e2747-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e2747-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e2747-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2747-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e2747-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-131">Entry</span></span> | <span data-ttu-id="e2747-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e2747-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2747-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2747-135">System-Only</span></span>            | <span data-ttu-id="e2747-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-136">False</span></span>                                        |
| <span data-ttu-id="e2747-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2747-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e2747-138">True</span><span class="sxs-lookup"><span data-stu-id="e2747-138">True</span></span>                                         |
| <span data-ttu-id="e2747-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2747-139">Is Indexed</span></span>             | <span data-ttu-id="e2747-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-140">False</span></span>                                        |
| <span data-ttu-id="e2747-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2747-141">In Global Catalog</span></span>      | <span data-ttu-id="e2747-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-142">False</span></span>                                        |
| <span data-ttu-id="e2747-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2747-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2747-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2747-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e2747-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2747-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e2747-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2747-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e2747-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-147">Search-Flags</span></span>           | <span data-ttu-id="e2747-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2747-148">0x00000000</span></span>                                   |
| <span data-ttu-id="e2747-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-149">System-Flags</span></span>           | <span data-ttu-id="e2747-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2747-150">0x00000010</span></span>                                   |
| <span data-ttu-id="e2747-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2747-151">Classes used in</span></span>        | [<span data-ttu-id="e2747-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="e2747-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e2747-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2747-153">Windows Server 2003</span></span>



| <span data-ttu-id="e2747-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-154">Entry</span></span> | <span data-ttu-id="e2747-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e2747-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2747-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2747-158">System-Only</span></span>            | <span data-ttu-id="e2747-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-159">False</span></span>                                        |
| <span data-ttu-id="e2747-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2747-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e2747-161">True</span><span class="sxs-lookup"><span data-stu-id="e2747-161">True</span></span>                                         |
| <span data-ttu-id="e2747-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2747-162">Is Indexed</span></span>             | <span data-ttu-id="e2747-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-163">False</span></span>                                        |
| <span data-ttu-id="e2747-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2747-164">In Global Catalog</span></span>      | <span data-ttu-id="e2747-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-165">False</span></span>                                        |
| <span data-ttu-id="e2747-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2747-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2747-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2747-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e2747-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2747-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e2747-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2747-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e2747-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-170">Search-Flags</span></span>           | <span data-ttu-id="e2747-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2747-171">0x00000000</span></span>                                   |
| <span data-ttu-id="e2747-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-172">System-Flags</span></span>           | <span data-ttu-id="e2747-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2747-173">0x00000010</span></span>                                   |
| <span data-ttu-id="e2747-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2747-174">Classes used in</span></span>        | [<span data-ttu-id="e2747-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="e2747-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e2747-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e2747-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e2747-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-177">Entry</span></span> | <span data-ttu-id="e2747-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e2747-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2747-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2747-181">System-Only</span></span>            | <span data-ttu-id="e2747-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-182">False</span></span>                                        |
| <span data-ttu-id="e2747-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2747-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e2747-184">True</span><span class="sxs-lookup"><span data-stu-id="e2747-184">True</span></span>                                         |
| <span data-ttu-id="e2747-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2747-185">Is Indexed</span></span>             | <span data-ttu-id="e2747-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-186">False</span></span>                                        |
| <span data-ttu-id="e2747-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2747-187">In Global Catalog</span></span>      | <span data-ttu-id="e2747-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-188">False</span></span>                                        |
| <span data-ttu-id="e2747-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2747-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2747-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2747-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e2747-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2747-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e2747-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2747-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e2747-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-193">Search-Flags</span></span>           | <span data-ttu-id="e2747-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2747-194">0x00000000</span></span>                                   |
| <span data-ttu-id="e2747-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-195">System-Flags</span></span>           | <span data-ttu-id="e2747-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2747-196">0x00000010</span></span>                                   |
| <span data-ttu-id="e2747-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2747-197">Classes used in</span></span>        | [<span data-ttu-id="e2747-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="e2747-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e2747-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2747-199">Windows Server 2008</span></span>



| <span data-ttu-id="e2747-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-200">Entry</span></span> | <span data-ttu-id="e2747-201">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e2747-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2747-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2747-204">System-Only</span></span>            | <span data-ttu-id="e2747-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-205">False</span></span>                                        |
| <span data-ttu-id="e2747-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2747-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e2747-207">True</span><span class="sxs-lookup"><span data-stu-id="e2747-207">True</span></span>                                         |
| <span data-ttu-id="e2747-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2747-208">Is Indexed</span></span>             | <span data-ttu-id="e2747-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-209">False</span></span>                                        |
| <span data-ttu-id="e2747-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2747-210">In Global Catalog</span></span>      | <span data-ttu-id="e2747-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-211">False</span></span>                                        |
| <span data-ttu-id="e2747-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2747-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2747-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2747-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e2747-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2747-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e2747-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2747-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e2747-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-216">Search-Flags</span></span>           | <span data-ttu-id="e2747-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2747-217">0x00000000</span></span>                                   |
| <span data-ttu-id="e2747-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-218">System-Flags</span></span>           | <span data-ttu-id="e2747-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2747-219">0x00000010</span></span>                                   |
| <span data-ttu-id="e2747-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2747-220">Classes used in</span></span>        | [<span data-ttu-id="e2747-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="e2747-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e2747-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2747-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e2747-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-223">Entry</span></span> | <span data-ttu-id="e2747-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e2747-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2747-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2747-227">System-Only</span></span>            | <span data-ttu-id="e2747-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-228">False</span></span>                                        |
| <span data-ttu-id="e2747-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2747-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e2747-230">True</span><span class="sxs-lookup"><span data-stu-id="e2747-230">True</span></span>                                         |
| <span data-ttu-id="e2747-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2747-231">Is Indexed</span></span>             | <span data-ttu-id="e2747-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-232">False</span></span>                                        |
| <span data-ttu-id="e2747-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2747-233">In Global Catalog</span></span>      | <span data-ttu-id="e2747-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-234">False</span></span>                                        |
| <span data-ttu-id="e2747-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2747-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2747-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2747-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e2747-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2747-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e2747-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2747-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e2747-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-239">Search-Flags</span></span>           | <span data-ttu-id="e2747-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2747-240">0x00000000</span></span>                                   |
| <span data-ttu-id="e2747-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-241">System-Flags</span></span>           | <span data-ttu-id="e2747-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2747-242">0x00000010</span></span>                                   |
| <span data-ttu-id="e2747-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2747-243">Classes used in</span></span>        | [<span data-ttu-id="e2747-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="e2747-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e2747-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2747-245">Windows Server 2012</span></span>



| <span data-ttu-id="e2747-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="e2747-246">Entry</span></span> | <span data-ttu-id="e2747-247">Значение</span><span class="sxs-lookup"><span data-stu-id="e2747-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e2747-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e2747-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2747-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e2747-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2747-250">System-Only</span></span>            | <span data-ttu-id="e2747-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-251">False</span></span>                                        |
| <span data-ttu-id="e2747-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e2747-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e2747-253">True</span><span class="sxs-lookup"><span data-stu-id="e2747-253">True</span></span>                                         |
| <span data-ttu-id="e2747-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e2747-254">Is Indexed</span></span>             | <span data-ttu-id="e2747-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-255">False</span></span>                                        |
| <span data-ttu-id="e2747-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e2747-256">In Global Catalog</span></span>      | <span data-ttu-id="e2747-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="e2747-257">False</span></span>                                        |
| <span data-ttu-id="e2747-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e2747-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2747-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2747-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e2747-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2747-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e2747-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2747-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e2747-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-262">Search-Flags</span></span>           | <span data-ttu-id="e2747-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2747-263">0x00000000</span></span>                                   |
| <span data-ttu-id="e2747-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2747-264">System-Flags</span></span>           | <span data-ttu-id="e2747-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2747-265">0x00000010</span></span>                                   |
| <span data-ttu-id="e2747-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e2747-266">Classes used in</span></span>        | [<span data-ttu-id="e2747-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="e2747-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





