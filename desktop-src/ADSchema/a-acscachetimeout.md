---
title: ACS-Кэш-атрибут времени ожидания
description: Период времени до истечения срока действия объектов ACS, кэшируемых службой ACS.
ms.assetid: 8927ca01-d550-42df-8a14-96ddbea3fdb8
ms.tgt_platform: multiple
keywords:
- ACS-кэширование-схема AD атрибута timeout
- Схема AD атрибута Акскачетимеаут
topic_type:
- apiref
api_name:
- ACS-Cache-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bb72ca9708c3e4edd8f1229d887439ff133d201
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893146"
---
# <a name="acs-cache-timeout-attribute"></a><span data-ttu-id="cf5dc-105">ACS-Кэш-атрибут времени ожидания</span><span class="sxs-lookup"><span data-stu-id="cf5dc-105">ACS-Cache-Timeout attribute</span></span>

<span data-ttu-id="cf5dc-106">Период времени до истечения срока действия объектов ACS, кэшируемых службой ACS.</span><span class="sxs-lookup"><span data-stu-id="cf5dc-106">The amount of time before the expiration of ACS objects that are cached by the ACS service.</span></span>



| <span data-ttu-id="cf5dc-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-107">Entry</span></span> | <span data-ttu-id="cf5dc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cf5dc-109">CN</span><span class="sxs-lookup"><span data-stu-id="cf5dc-109">CN</span></span>                | <span data-ttu-id="cf5dc-110">ACS — Кэш — время ожидания</span><span class="sxs-lookup"><span data-stu-id="cf5dc-110">ACS-Cache-Timeout</span></span>                    |
| <span data-ttu-id="cf5dc-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cf5dc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cf5dc-112">акскачетимеаут</span><span class="sxs-lookup"><span data-stu-id="cf5dc-112">aCSCacheTimeout</span></span>                      |
| <span data-ttu-id="cf5dc-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cf5dc-113">Size</span></span>              | <span data-ttu-id="cf5dc-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="cf5dc-114">4 bytes</span></span>                              |
| <span data-ttu-id="cf5dc-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cf5dc-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cf5dc-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cf5dc-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cf5dc-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-117">Attribute-Id</span></span>      | <span data-ttu-id="cf5dc-118">1.2.840.113556.1.4.779</span><span class="sxs-lookup"><span data-stu-id="cf5dc-118">1.2.840.113556.1.4.779</span></span>               |
| <span data-ttu-id="cf5dc-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cf5dc-119">System-Id-Guid</span></span>    | <span data-ttu-id="cf5dc-120">1cb355a1-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="cf5dc-120">1cb355a1-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="cf5dc-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf5dc-121">Syntax</span></span>            | [<span data-ttu-id="cf5dc-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cf5dc-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cf5dc-123">Implementations</span></span>

-   [<span data-ttu-id="cf5dc-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf5dc-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf5dc-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf5dc-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf5dc-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf5dc-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf5dc-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf5dc-130">Windows 2000 Server</span></span>



| <span data-ttu-id="cf5dc-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-131">Entry</span></span> | <span data-ttu-id="cf5dc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cf5dc-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf5dc-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf5dc-135">System-Only</span></span>            | <span data-ttu-id="cf5dc-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-136">False</span></span>                                        |
| <span data-ttu-id="cf5dc-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf5dc-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cf5dc-138">True</span><span class="sxs-lookup"><span data-stu-id="cf5dc-138">True</span></span>                                         |
| <span data-ttu-id="cf5dc-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf5dc-139">Is Indexed</span></span>             | <span data-ttu-id="cf5dc-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-140">False</span></span>                                        |
| <span data-ttu-id="cf5dc-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf5dc-141">In Global Catalog</span></span>      | <span data-ttu-id="cf5dc-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-142">False</span></span>                                        |
| <span data-ttu-id="cf5dc-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf5dc-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf5dc-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf5dc-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cf5dc-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf5dc-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf5dc-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-147">Search-Flags</span></span>           | <span data-ttu-id="cf5dc-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf5dc-148">0x00000000</span></span>                                   |
| <span data-ttu-id="cf5dc-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-149">System-Flags</span></span>           | <span data-ttu-id="cf5dc-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf5dc-150">0x00000010</span></span>                                   |
| <span data-ttu-id="cf5dc-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf5dc-151">Classes used in</span></span>        | [<span data-ttu-id="cf5dc-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf5dc-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf5dc-153">Windows Server 2003</span></span>



| <span data-ttu-id="cf5dc-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-154">Entry</span></span> | <span data-ttu-id="cf5dc-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cf5dc-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf5dc-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf5dc-158">System-Only</span></span>            | <span data-ttu-id="cf5dc-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-159">False</span></span>                                        |
| <span data-ttu-id="cf5dc-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf5dc-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cf5dc-161">True</span><span class="sxs-lookup"><span data-stu-id="cf5dc-161">True</span></span>                                         |
| <span data-ttu-id="cf5dc-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf5dc-162">Is Indexed</span></span>             | <span data-ttu-id="cf5dc-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-163">False</span></span>                                        |
| <span data-ttu-id="cf5dc-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf5dc-164">In Global Catalog</span></span>      | <span data-ttu-id="cf5dc-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-165">False</span></span>                                        |
| <span data-ttu-id="cf5dc-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf5dc-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf5dc-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf5dc-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cf5dc-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf5dc-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf5dc-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-170">Search-Flags</span></span>           | <span data-ttu-id="cf5dc-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf5dc-171">0x00000000</span></span>                                   |
| <span data-ttu-id="cf5dc-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-172">System-Flags</span></span>           | <span data-ttu-id="cf5dc-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf5dc-173">0x00000010</span></span>                                   |
| <span data-ttu-id="cf5dc-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf5dc-174">Classes used in</span></span>        | [<span data-ttu-id="cf5dc-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf5dc-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf5dc-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf5dc-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-177">Entry</span></span> | <span data-ttu-id="cf5dc-178">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cf5dc-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf5dc-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf5dc-181">System-Only</span></span>            | <span data-ttu-id="cf5dc-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-182">False</span></span>                                        |
| <span data-ttu-id="cf5dc-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf5dc-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cf5dc-184">True</span><span class="sxs-lookup"><span data-stu-id="cf5dc-184">True</span></span>                                         |
| <span data-ttu-id="cf5dc-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf5dc-185">Is Indexed</span></span>             | <span data-ttu-id="cf5dc-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-186">False</span></span>                                        |
| <span data-ttu-id="cf5dc-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf5dc-187">In Global Catalog</span></span>      | <span data-ttu-id="cf5dc-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-188">False</span></span>                                        |
| <span data-ttu-id="cf5dc-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf5dc-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf5dc-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf5dc-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cf5dc-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf5dc-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf5dc-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-193">Search-Flags</span></span>           | <span data-ttu-id="cf5dc-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf5dc-194">0x00000000</span></span>                                   |
| <span data-ttu-id="cf5dc-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-195">System-Flags</span></span>           | <span data-ttu-id="cf5dc-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf5dc-196">0x00000010</span></span>                                   |
| <span data-ttu-id="cf5dc-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf5dc-197">Classes used in</span></span>        | [<span data-ttu-id="cf5dc-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf5dc-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf5dc-199">Windows Server 2008</span></span>



| <span data-ttu-id="cf5dc-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-200">Entry</span></span> | <span data-ttu-id="cf5dc-201">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cf5dc-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf5dc-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf5dc-204">System-Only</span></span>            | <span data-ttu-id="cf5dc-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-205">False</span></span>                                        |
| <span data-ttu-id="cf5dc-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf5dc-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cf5dc-207">True</span><span class="sxs-lookup"><span data-stu-id="cf5dc-207">True</span></span>                                         |
| <span data-ttu-id="cf5dc-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf5dc-208">Is Indexed</span></span>             | <span data-ttu-id="cf5dc-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-209">False</span></span>                                        |
| <span data-ttu-id="cf5dc-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf5dc-210">In Global Catalog</span></span>      | <span data-ttu-id="cf5dc-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-211">False</span></span>                                        |
| <span data-ttu-id="cf5dc-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf5dc-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf5dc-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf5dc-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cf5dc-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf5dc-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf5dc-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-216">Search-Flags</span></span>           | <span data-ttu-id="cf5dc-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf5dc-217">0x00000000</span></span>                                   |
| <span data-ttu-id="cf5dc-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-218">System-Flags</span></span>           | <span data-ttu-id="cf5dc-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf5dc-219">0x00000010</span></span>                                   |
| <span data-ttu-id="cf5dc-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf5dc-220">Classes used in</span></span>        | [<span data-ttu-id="cf5dc-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf5dc-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf5dc-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf5dc-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-223">Entry</span></span> | <span data-ttu-id="cf5dc-224">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cf5dc-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf5dc-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf5dc-227">System-Only</span></span>            | <span data-ttu-id="cf5dc-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-228">False</span></span>                                        |
| <span data-ttu-id="cf5dc-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf5dc-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cf5dc-230">True</span><span class="sxs-lookup"><span data-stu-id="cf5dc-230">True</span></span>                                         |
| <span data-ttu-id="cf5dc-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf5dc-231">Is Indexed</span></span>             | <span data-ttu-id="cf5dc-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-232">False</span></span>                                        |
| <span data-ttu-id="cf5dc-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf5dc-233">In Global Catalog</span></span>      | <span data-ttu-id="cf5dc-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-234">False</span></span>                                        |
| <span data-ttu-id="cf5dc-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf5dc-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf5dc-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf5dc-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cf5dc-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf5dc-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf5dc-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-239">Search-Flags</span></span>           | <span data-ttu-id="cf5dc-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf5dc-240">0x00000000</span></span>                                   |
| <span data-ttu-id="cf5dc-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-241">System-Flags</span></span>           | <span data-ttu-id="cf5dc-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf5dc-242">0x00000010</span></span>                                   |
| <span data-ttu-id="cf5dc-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf5dc-243">Classes used in</span></span>        | [<span data-ttu-id="cf5dc-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf5dc-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf5dc-245">Windows Server 2012</span></span>



| <span data-ttu-id="cf5dc-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf5dc-246">Entry</span></span> | <span data-ttu-id="cf5dc-247">Значение</span><span class="sxs-lookup"><span data-stu-id="cf5dc-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cf5dc-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf5dc-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf5dc-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cf5dc-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf5dc-250">System-Only</span></span>            | <span data-ttu-id="cf5dc-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-251">False</span></span>                                        |
| <span data-ttu-id="cf5dc-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf5dc-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cf5dc-253">True</span><span class="sxs-lookup"><span data-stu-id="cf5dc-253">True</span></span>                                         |
| <span data-ttu-id="cf5dc-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf5dc-254">Is Indexed</span></span>             | <span data-ttu-id="cf5dc-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-255">False</span></span>                                        |
| <span data-ttu-id="cf5dc-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf5dc-256">In Global Catalog</span></span>      | <span data-ttu-id="cf5dc-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf5dc-257">False</span></span>                                        |
| <span data-ttu-id="cf5dc-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf5dc-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf5dc-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf5dc-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cf5dc-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf5dc-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf5dc-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cf5dc-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-262">Search-Flags</span></span>           | <span data-ttu-id="cf5dc-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf5dc-263">0x00000000</span></span>                                   |
| <span data-ttu-id="cf5dc-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf5dc-264">System-Flags</span></span>           | <span data-ttu-id="cf5dc-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf5dc-265">0x00000010</span></span>                                   |
| <span data-ttu-id="cf5dc-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf5dc-266">Classes used in</span></span>        | [<span data-ttu-id="cf5dc-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="cf5dc-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





