---
title: Атрибут Serial-Number
description: Часть спецификации X. 500. Не используется Active Directory.
ms.assetid: e5d68744-226b-42ee-a578-18380ddf4668
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Serial-Number
- Схема AD атрибута serialNumber
topic_type:
- apiref
api_name:
- Serial-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c1bd8435bbc742d3b2135d9f3b024b3196a7e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655290"
---
# <a name="serial-number-attribute"></a><span data-ttu-id="be2f7-106">Атрибут Serial-Number</span><span class="sxs-lookup"><span data-stu-id="be2f7-106">Serial-Number attribute</span></span>

<span data-ttu-id="be2f7-107">Часть спецификации X. 500.</span><span class="sxs-lookup"><span data-stu-id="be2f7-107">Part of X.500 specification.</span></span> <span data-ttu-id="be2f7-108">Не используется Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be2f7-108">Not used by Active Directory.</span></span>



| <span data-ttu-id="be2f7-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-109">Entry</span></span> | <span data-ttu-id="be2f7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="be2f7-111">CN</span><span class="sxs-lookup"><span data-stu-id="be2f7-111">CN</span></span>                | <span data-ttu-id="be2f7-112">Serial-Number</span><span class="sxs-lookup"><span data-stu-id="be2f7-112">Serial-Number</span></span>                        |
| <span data-ttu-id="be2f7-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="be2f7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="be2f7-114">серийный номер</span><span class="sxs-lookup"><span data-stu-id="be2f7-114">serialNumber</span></span>                         |
| <span data-ttu-id="be2f7-115">Размер</span><span class="sxs-lookup"><span data-stu-id="be2f7-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="be2f7-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="be2f7-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="be2f7-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="be2f7-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="be2f7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-118">Attribute-Id</span></span>      | <span data-ttu-id="be2f7-119">2.5.4.5</span><span class="sxs-lookup"><span data-stu-id="be2f7-119">2.5.4.5</span></span>                              |
| <span data-ttu-id="be2f7-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="be2f7-120">System-Id-Guid</span></span>    | <span data-ttu-id="be2f7-121">bf967a32-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="be2f7-121">bf967a32-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="be2f7-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be2f7-122">Syntax</span></span>            | [<span data-ttu-id="be2f7-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="be2f7-123">**String(IA5)**</span></span>](s-string-ia5.md)  |



## <a name="implementations"></a><span data-ttu-id="be2f7-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="be2f7-124">Implementations</span></span>

-   [<span data-ttu-id="be2f7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="be2f7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="be2f7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be2f7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be2f7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be2f7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be2f7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be2f7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be2f7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be2f7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be2f7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be2f7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="be2f7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be2f7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="be2f7-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-132">Entry</span></span> | <span data-ttu-id="be2f7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="be2f7-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2f7-134">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="be2f7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-135">MAPI-Id</span></span>                | <span data-ttu-id="be2f7-136">0x8130</span><span class="sxs-lookup"><span data-stu-id="be2f7-136">0x8130</span></span>                                                                      |
| <span data-ttu-id="be2f7-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2f7-137">System-Only</span></span>            | <span data-ttu-id="be2f7-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-138">False</span></span>                                                                       |
| <span data-ttu-id="be2f7-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2f7-139">Is-Single-Valued</span></span>       | <span data-ttu-id="be2f7-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-140">False</span></span>                                                                       |
| <span data-ttu-id="be2f7-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2f7-141">Is Indexed</span></span>             | <span data-ttu-id="be2f7-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-142">False</span></span>                                                                       |
| <span data-ttu-id="be2f7-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2f7-143">In Global Catalog</span></span>      | <span data-ttu-id="be2f7-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-144">False</span></span>                                                                       |
| <span data-ttu-id="be2f7-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2f7-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2f7-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2f7-146">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="be2f7-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2f7-147">Range-Lower</span></span>            | <span data-ttu-id="be2f7-148">1</span><span class="sxs-lookup"><span data-stu-id="be2f7-148">1</span></span>                                                                           |
| <span data-ttu-id="be2f7-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2f7-149">Range-Upper</span></span>            | <span data-ttu-id="be2f7-150">64</span><span class="sxs-lookup"><span data-stu-id="be2f7-150">64</span></span>                                                                          |
| <span data-ttu-id="be2f7-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-151">Search-Flags</span></span>           | <span data-ttu-id="be2f7-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2f7-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="be2f7-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-153">System-Flags</span></span>           | <span data-ttu-id="be2f7-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2f7-154">0x00000010</span></span>                                                                  |
| <span data-ttu-id="be2f7-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2f7-155">Classes used in</span></span>        | [<span data-ttu-id="be2f7-156">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="be2f7-156">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="be2f7-157">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="be2f7-157">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="be2f7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be2f7-158">Windows Server 2003</span></span>



| <span data-ttu-id="be2f7-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-159">Entry</span></span> | <span data-ttu-id="be2f7-160">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2f7-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2f7-161">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="be2f7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-162">MAPI-Id</span></span>                | <span data-ttu-id="be2f7-163">0x8130</span><span class="sxs-lookup"><span data-stu-id="be2f7-163">0x8130</span></span>                                                                                                            |
| <span data-ttu-id="be2f7-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2f7-164">System-Only</span></span>            | <span data-ttu-id="be2f7-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-165">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2f7-166">Is-Single-Valued</span></span>       | <span data-ttu-id="be2f7-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-167">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2f7-168">Is Indexed</span></span>             | <span data-ttu-id="be2f7-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-169">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2f7-170">In Global Catalog</span></span>      | <span data-ttu-id="be2f7-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-171">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2f7-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2f7-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2f7-173">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="be2f7-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2f7-174">Range-Lower</span></span>            | <span data-ttu-id="be2f7-175">1</span><span class="sxs-lookup"><span data-stu-id="be2f7-175">1</span></span>                                                                                                                 |
| <span data-ttu-id="be2f7-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2f7-176">Range-Upper</span></span>            | <span data-ttu-id="be2f7-177">64</span><span class="sxs-lookup"><span data-stu-id="be2f7-177">64</span></span>                                                                                                                |
| <span data-ttu-id="be2f7-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-178">Search-Flags</span></span>           | <span data-ttu-id="be2f7-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2f7-179">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-180">System-Flags</span></span>           | <span data-ttu-id="be2f7-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2f7-181">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2f7-182">Classes used in</span></span>        | [<span data-ttu-id="be2f7-183">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="be2f7-183">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="be2f7-184">**Человек**</span><span class="sxs-lookup"><span data-stu-id="be2f7-184">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="be2f7-185">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="be2f7-185">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be2f7-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be2f7-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be2f7-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-187">Entry</span></span> | <span data-ttu-id="be2f7-188">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-188">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2f7-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2f7-189">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="be2f7-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-190">MAPI-Id</span></span>                | <span data-ttu-id="be2f7-191">0x8130</span><span class="sxs-lookup"><span data-stu-id="be2f7-191">0x8130</span></span>                                                                                                            |
| <span data-ttu-id="be2f7-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2f7-192">System-Only</span></span>            | <span data-ttu-id="be2f7-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-193">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2f7-194">Is-Single-Valued</span></span>       | <span data-ttu-id="be2f7-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-195">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2f7-196">Is Indexed</span></span>             | <span data-ttu-id="be2f7-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-197">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2f7-198">In Global Catalog</span></span>      | <span data-ttu-id="be2f7-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-199">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2f7-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2f7-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2f7-201">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="be2f7-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2f7-202">Range-Lower</span></span>            | <span data-ttu-id="be2f7-203">1</span><span class="sxs-lookup"><span data-stu-id="be2f7-203">1</span></span>                                                                                                                 |
| <span data-ttu-id="be2f7-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2f7-204">Range-Upper</span></span>            | <span data-ttu-id="be2f7-205">64</span><span class="sxs-lookup"><span data-stu-id="be2f7-205">64</span></span>                                                                                                                |
| <span data-ttu-id="be2f7-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-206">Search-Flags</span></span>           | <span data-ttu-id="be2f7-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2f7-207">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-208">System-Flags</span></span>           | <span data-ttu-id="be2f7-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2f7-209">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-210">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2f7-210">Classes used in</span></span>        | [<span data-ttu-id="be2f7-211">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="be2f7-211">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="be2f7-212">**Человек**</span><span class="sxs-lookup"><span data-stu-id="be2f7-212">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="be2f7-213">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="be2f7-213">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be2f7-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be2f7-214">Windows Server 2008</span></span>



| <span data-ttu-id="be2f7-215">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-215">Entry</span></span> | <span data-ttu-id="be2f7-216">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-216">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2f7-217">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2f7-217">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="be2f7-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-218">MAPI-Id</span></span>                | <span data-ttu-id="be2f7-219">0x8130</span><span class="sxs-lookup"><span data-stu-id="be2f7-219">0x8130</span></span>                                                                                                            |
| <span data-ttu-id="be2f7-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2f7-220">System-Only</span></span>            | <span data-ttu-id="be2f7-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-221">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-222">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2f7-222">Is-Single-Valued</span></span>       | <span data-ttu-id="be2f7-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-223">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-224">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2f7-224">Is Indexed</span></span>             | <span data-ttu-id="be2f7-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-225">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-226">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2f7-226">In Global Catalog</span></span>      | <span data-ttu-id="be2f7-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-227">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-228">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2f7-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2f7-229">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2f7-229">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="be2f7-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2f7-230">Range-Lower</span></span>            | <span data-ttu-id="be2f7-231">1</span><span class="sxs-lookup"><span data-stu-id="be2f7-231">1</span></span>                                                                                                                 |
| <span data-ttu-id="be2f7-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2f7-232">Range-Upper</span></span>            | <span data-ttu-id="be2f7-233">64</span><span class="sxs-lookup"><span data-stu-id="be2f7-233">64</span></span>                                                                                                                |
| <span data-ttu-id="be2f7-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-234">Search-Flags</span></span>           | <span data-ttu-id="be2f7-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2f7-235">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-236">System-Flags</span></span>           | <span data-ttu-id="be2f7-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2f7-237">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-238">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2f7-238">Classes used in</span></span>        | [<span data-ttu-id="be2f7-239">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="be2f7-239">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="be2f7-240">**Человек**</span><span class="sxs-lookup"><span data-stu-id="be2f7-240">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="be2f7-241">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="be2f7-241">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be2f7-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be2f7-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be2f7-243">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-243">Entry</span></span> | <span data-ttu-id="be2f7-244">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-244">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2f7-245">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2f7-245">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="be2f7-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-246">MAPI-Id</span></span>                | <span data-ttu-id="be2f7-247">0x8130</span><span class="sxs-lookup"><span data-stu-id="be2f7-247">0x8130</span></span>                                                                                                            |
| <span data-ttu-id="be2f7-248">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2f7-248">System-Only</span></span>            | <span data-ttu-id="be2f7-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-249">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-250">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2f7-250">Is-Single-Valued</span></span>       | <span data-ttu-id="be2f7-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-251">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-252">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2f7-252">Is Indexed</span></span>             | <span data-ttu-id="be2f7-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-253">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-254">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2f7-254">In Global Catalog</span></span>      | <span data-ttu-id="be2f7-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-255">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-256">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2f7-256">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2f7-257">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2f7-257">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="be2f7-258">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2f7-258">Range-Lower</span></span>            | <span data-ttu-id="be2f7-259">1</span><span class="sxs-lookup"><span data-stu-id="be2f7-259">1</span></span>                                                                                                                 |
| <span data-ttu-id="be2f7-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2f7-260">Range-Upper</span></span>            | <span data-ttu-id="be2f7-261">64</span><span class="sxs-lookup"><span data-stu-id="be2f7-261">64</span></span>                                                                                                                |
| <span data-ttu-id="be2f7-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-262">Search-Flags</span></span>           | <span data-ttu-id="be2f7-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2f7-263">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-264">System-Flags</span></span>           | <span data-ttu-id="be2f7-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2f7-265">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2f7-266">Classes used in</span></span>        | [<span data-ttu-id="be2f7-267">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="be2f7-267">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="be2f7-268">**Человек**</span><span class="sxs-lookup"><span data-stu-id="be2f7-268">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="be2f7-269">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="be2f7-269">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be2f7-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be2f7-270">Windows Server 2012</span></span>



| <span data-ttu-id="be2f7-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2f7-271">Entry</span></span> | <span data-ttu-id="be2f7-272">Значение</span><span class="sxs-lookup"><span data-stu-id="be2f7-272">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2f7-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2f7-273">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="be2f7-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2f7-274">MAPI-Id</span></span>                | <span data-ttu-id="be2f7-275">0x8130</span><span class="sxs-lookup"><span data-stu-id="be2f7-275">0x8130</span></span>                                                                                                            |
| <span data-ttu-id="be2f7-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2f7-276">System-Only</span></span>            | <span data-ttu-id="be2f7-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-277">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2f7-278">Is-Single-Valued</span></span>       | <span data-ttu-id="be2f7-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-279">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2f7-280">Is Indexed</span></span>             | <span data-ttu-id="be2f7-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-281">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2f7-282">In Global Catalog</span></span>      | <span data-ttu-id="be2f7-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2f7-283">False</span></span>                                                                                                             |
| <span data-ttu-id="be2f7-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2f7-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2f7-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2f7-285">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="be2f7-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2f7-286">Range-Lower</span></span>            | <span data-ttu-id="be2f7-287">1</span><span class="sxs-lookup"><span data-stu-id="be2f7-287">1</span></span>                                                                                                                 |
| <span data-ttu-id="be2f7-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2f7-288">Range-Upper</span></span>            | <span data-ttu-id="be2f7-289">64</span><span class="sxs-lookup"><span data-stu-id="be2f7-289">64</span></span>                                                                                                                |
| <span data-ttu-id="be2f7-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-290">Search-Flags</span></span>           | <span data-ttu-id="be2f7-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2f7-291">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2f7-292">System-Flags</span></span>           | <span data-ttu-id="be2f7-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2f7-293">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="be2f7-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2f7-294">Classes used in</span></span>        | [<span data-ttu-id="be2f7-295">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="be2f7-295">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="be2f7-296">**Человек**</span><span class="sxs-lookup"><span data-stu-id="be2f7-296">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="be2f7-297">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="be2f7-297">**Server**</span></span>](c-server.md)<br/> |



 

 





