---
title: Атрибут ms-DS-Allowed-DNS-суффиксов
description: Список разрешенных суффиксов для атрибута dNSHostName в объектах Computer.
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-Allowed-DNS-суффиксов
- Схема AD атрибута msDS-AllowedDNSSuffixes
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804709"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="423b9-105">Атрибут ms-DS-Allowed-DNS-суффиксов</span><span class="sxs-lookup"><span data-stu-id="423b9-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="423b9-106">Список разрешенных суффиксов для атрибута dNSHostName в объектах Computer.</span><span class="sxs-lookup"><span data-stu-id="423b9-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="423b9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-107">Entry</span></span> | <span data-ttu-id="423b9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="423b9-109">CN</span><span class="sxs-lookup"><span data-stu-id="423b9-109">CN</span></span>                | <span data-ttu-id="423b9-110">MS-DS-Allowed-DNS-суффиксы</span><span class="sxs-lookup"><span data-stu-id="423b9-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="423b9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="423b9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="423b9-112">msDS-AllowedDNSSuffixes</span><span class="sxs-lookup"><span data-stu-id="423b9-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="423b9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="423b9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="423b9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="423b9-114">Update Privilege</span></span>  | <span data-ttu-id="423b9-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="423b9-115">Domain administrator</span></span>                        |
| <span data-ttu-id="423b9-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="423b9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="423b9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-117">Attribute-Id</span></span>      | <span data-ttu-id="423b9-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="423b9-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="423b9-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="423b9-119">System-Id-Guid</span></span>    | <span data-ttu-id="423b9-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="423b9-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="423b9-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="423b9-121">Syntax</span></span>            | [<span data-ttu-id="423b9-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="423b9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="423b9-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="423b9-123">Implementations</span></span>

-   [<span data-ttu-id="423b9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="423b9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="423b9-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="423b9-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="423b9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="423b9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="423b9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="423b9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="423b9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="423b9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="423b9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="423b9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="423b9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="423b9-130">Windows Server 2003</span></span>



| <span data-ttu-id="423b9-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-131">Entry</span></span> | <span data-ttu-id="423b9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="423b9-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="423b9-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="423b9-135">System-Only</span></span>            | <span data-ttu-id="423b9-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-136">False</span></span>                                        |
| <span data-ttu-id="423b9-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="423b9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="423b9-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-138">False</span></span>                                        |
| <span data-ttu-id="423b9-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="423b9-139">Is Indexed</span></span>             | <span data-ttu-id="423b9-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-140">False</span></span>                                        |
| <span data-ttu-id="423b9-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="423b9-141">In Global Catalog</span></span>      | <span data-ttu-id="423b9-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-142">False</span></span>                                        |
| <span data-ttu-id="423b9-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="423b9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="423b9-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="423b9-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="423b9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="423b9-145">Range-Lower</span></span>            | <span data-ttu-id="423b9-146">0</span><span class="sxs-lookup"><span data-stu-id="423b9-146">0</span></span>                                            |
| <span data-ttu-id="423b9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="423b9-147">Range-Upper</span></span>            | <span data-ttu-id="423b9-148">2048</span><span class="sxs-lookup"><span data-stu-id="423b9-148">2048</span></span>                                         |
| <span data-ttu-id="423b9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-149">Search-Flags</span></span>           | <span data-ttu-id="423b9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="423b9-150">0x00000000</span></span>                                   |
| <span data-ttu-id="423b9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-151">System-Flags</span></span>           | <span data-ttu-id="423b9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="423b9-152">0x00000010</span></span>                                   |
| <span data-ttu-id="423b9-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="423b9-153">Classes used in</span></span>        | [<span data-ttu-id="423b9-154">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="423b9-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="423b9-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="423b9-155">ADAM</span></span>



| <span data-ttu-id="423b9-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-156">Entry</span></span> | <span data-ttu-id="423b9-157">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="423b9-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="423b9-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="423b9-160">System-Only</span></span>            | <span data-ttu-id="423b9-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-161">False</span></span>                                        |
| <span data-ttu-id="423b9-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="423b9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="423b9-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-163">False</span></span>                                        |
| <span data-ttu-id="423b9-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="423b9-164">Is Indexed</span></span>             | <span data-ttu-id="423b9-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-165">False</span></span>                                        |
| <span data-ttu-id="423b9-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="423b9-166">In Global Catalog</span></span>      | <span data-ttu-id="423b9-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-167">False</span></span>                                        |
| <span data-ttu-id="423b9-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="423b9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="423b9-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="423b9-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="423b9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="423b9-170">Range-Lower</span></span>            | <span data-ttu-id="423b9-171">0</span><span class="sxs-lookup"><span data-stu-id="423b9-171">0</span></span>                                            |
| <span data-ttu-id="423b9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="423b9-172">Range-Upper</span></span>            | <span data-ttu-id="423b9-173">2048</span><span class="sxs-lookup"><span data-stu-id="423b9-173">2048</span></span>                                         |
| <span data-ttu-id="423b9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-174">Search-Flags</span></span>           | <span data-ttu-id="423b9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="423b9-175">0x00000000</span></span>                                   |
| <span data-ttu-id="423b9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-176">System-Flags</span></span>           | <span data-ttu-id="423b9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="423b9-177">0x00000010</span></span>                                   |
| <span data-ttu-id="423b9-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="423b9-178">Classes used in</span></span>        | [<span data-ttu-id="423b9-179">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="423b9-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="423b9-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="423b9-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="423b9-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-181">Entry</span></span> | <span data-ttu-id="423b9-182">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="423b9-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="423b9-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="423b9-185">System-Only</span></span>            | <span data-ttu-id="423b9-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-186">False</span></span>                                        |
| <span data-ttu-id="423b9-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="423b9-187">Is-Single-Valued</span></span>       | <span data-ttu-id="423b9-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-188">False</span></span>                                        |
| <span data-ttu-id="423b9-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="423b9-189">Is Indexed</span></span>             | <span data-ttu-id="423b9-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-190">False</span></span>                                        |
| <span data-ttu-id="423b9-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="423b9-191">In Global Catalog</span></span>      | <span data-ttu-id="423b9-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-192">False</span></span>                                        |
| <span data-ttu-id="423b9-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="423b9-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="423b9-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="423b9-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="423b9-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="423b9-195">Range-Lower</span></span>            | <span data-ttu-id="423b9-196">0</span><span class="sxs-lookup"><span data-stu-id="423b9-196">0</span></span>                                            |
| <span data-ttu-id="423b9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="423b9-197">Range-Upper</span></span>            | <span data-ttu-id="423b9-198">2048</span><span class="sxs-lookup"><span data-stu-id="423b9-198">2048</span></span>                                         |
| <span data-ttu-id="423b9-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-199">Search-Flags</span></span>           | <span data-ttu-id="423b9-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="423b9-200">0x00000000</span></span>                                   |
| <span data-ttu-id="423b9-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-201">System-Flags</span></span>           | <span data-ttu-id="423b9-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="423b9-202">0x00000010</span></span>                                   |
| <span data-ttu-id="423b9-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="423b9-203">Classes used in</span></span>        | [<span data-ttu-id="423b9-204">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="423b9-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="423b9-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="423b9-205">Windows Server 2008</span></span>



| <span data-ttu-id="423b9-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-206">Entry</span></span> | <span data-ttu-id="423b9-207">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="423b9-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="423b9-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="423b9-210">System-Only</span></span>            | <span data-ttu-id="423b9-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-211">False</span></span>                                        |
| <span data-ttu-id="423b9-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="423b9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="423b9-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-213">False</span></span>                                        |
| <span data-ttu-id="423b9-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="423b9-214">Is Indexed</span></span>             | <span data-ttu-id="423b9-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-215">False</span></span>                                        |
| <span data-ttu-id="423b9-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="423b9-216">In Global Catalog</span></span>      | <span data-ttu-id="423b9-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-217">False</span></span>                                        |
| <span data-ttu-id="423b9-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="423b9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="423b9-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="423b9-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="423b9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="423b9-220">Range-Lower</span></span>            | <span data-ttu-id="423b9-221">0</span><span class="sxs-lookup"><span data-stu-id="423b9-221">0</span></span>                                            |
| <span data-ttu-id="423b9-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="423b9-222">Range-Upper</span></span>            | <span data-ttu-id="423b9-223">2048</span><span class="sxs-lookup"><span data-stu-id="423b9-223">2048</span></span>                                         |
| <span data-ttu-id="423b9-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-224">Search-Flags</span></span>           | <span data-ttu-id="423b9-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="423b9-225">0x00000000</span></span>                                   |
| <span data-ttu-id="423b9-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-226">System-Flags</span></span>           | <span data-ttu-id="423b9-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="423b9-227">0x00000010</span></span>                                   |
| <span data-ttu-id="423b9-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="423b9-228">Classes used in</span></span>        | [<span data-ttu-id="423b9-229">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="423b9-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="423b9-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="423b9-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="423b9-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-231">Entry</span></span> | <span data-ttu-id="423b9-232">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="423b9-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="423b9-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="423b9-235">System-Only</span></span>            | <span data-ttu-id="423b9-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-236">False</span></span>                                        |
| <span data-ttu-id="423b9-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="423b9-237">Is-Single-Valued</span></span>       | <span data-ttu-id="423b9-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-238">False</span></span>                                        |
| <span data-ttu-id="423b9-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="423b9-239">Is Indexed</span></span>             | <span data-ttu-id="423b9-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-240">False</span></span>                                        |
| <span data-ttu-id="423b9-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="423b9-241">In Global Catalog</span></span>      | <span data-ttu-id="423b9-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-242">False</span></span>                                        |
| <span data-ttu-id="423b9-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="423b9-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="423b9-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="423b9-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="423b9-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="423b9-245">Range-Lower</span></span>            | <span data-ttu-id="423b9-246">0</span><span class="sxs-lookup"><span data-stu-id="423b9-246">0</span></span>                                            |
| <span data-ttu-id="423b9-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="423b9-247">Range-Upper</span></span>            | <span data-ttu-id="423b9-248">2048</span><span class="sxs-lookup"><span data-stu-id="423b9-248">2048</span></span>                                         |
| <span data-ttu-id="423b9-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-249">Search-Flags</span></span>           | <span data-ttu-id="423b9-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="423b9-250">0x00000000</span></span>                                   |
| <span data-ttu-id="423b9-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-251">System-Flags</span></span>           | <span data-ttu-id="423b9-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="423b9-252">0x00000010</span></span>                                   |
| <span data-ttu-id="423b9-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="423b9-253">Classes used in</span></span>        | [<span data-ttu-id="423b9-254">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="423b9-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="423b9-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="423b9-255">Windows Server 2012</span></span>



| <span data-ttu-id="423b9-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="423b9-256">Entry</span></span> | <span data-ttu-id="423b9-257">Значение</span><span class="sxs-lookup"><span data-stu-id="423b9-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="423b9-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="423b9-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="423b9-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="423b9-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="423b9-260">System-Only</span></span>            | <span data-ttu-id="423b9-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-261">False</span></span>                                        |
| <span data-ttu-id="423b9-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="423b9-262">Is-Single-Valued</span></span>       | <span data-ttu-id="423b9-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-263">False</span></span>                                        |
| <span data-ttu-id="423b9-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="423b9-264">Is Indexed</span></span>             | <span data-ttu-id="423b9-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-265">False</span></span>                                        |
| <span data-ttu-id="423b9-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="423b9-266">In Global Catalog</span></span>      | <span data-ttu-id="423b9-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="423b9-267">False</span></span>                                        |
| <span data-ttu-id="423b9-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="423b9-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="423b9-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="423b9-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="423b9-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="423b9-270">Range-Lower</span></span>            | <span data-ttu-id="423b9-271">0</span><span class="sxs-lookup"><span data-stu-id="423b9-271">0</span></span>                                            |
| <span data-ttu-id="423b9-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="423b9-272">Range-Upper</span></span>            | <span data-ttu-id="423b9-273">2048</span><span class="sxs-lookup"><span data-stu-id="423b9-273">2048</span></span>                                         |
| <span data-ttu-id="423b9-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-274">Search-Flags</span></span>           | <span data-ttu-id="423b9-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="423b9-275">0x00000000</span></span>                                   |
| <span data-ttu-id="423b9-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="423b9-276">System-Flags</span></span>           | <span data-ttu-id="423b9-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="423b9-277">0x00000010</span></span>                                   |
| <span data-ttu-id="423b9-278">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="423b9-278">Classes used in</span></span>        | [<span data-ttu-id="423b9-279">**Домен — DNS**</span><span class="sxs-lookup"><span data-stu-id="423b9-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





