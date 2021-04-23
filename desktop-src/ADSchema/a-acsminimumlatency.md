---
title: ACS — атрибут минимальной задержки
description: Атрибут ACS-Minimum-задержка предназначен только для внутреннего использования.
ms.assetid: ec2cca55-9e31-49da-98aa-aa2f6664ea90
ms.tgt_platform: multiple
keywords:
- ACS-схема атрибута минимальной задержки (AD)
- Схема AD атрибута Аксминимумлатенци
topic_type:
- apiref
api_name:
- ACS-Minimum-Latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab7e9e6d5a9ccf626cdf8849ffe0e29504b4a0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072066"
---
# <a name="acs-minimum-latency-attribute"></a><span data-ttu-id="e7052-105">ACS — атрибут минимальной задержки</span><span class="sxs-lookup"><span data-stu-id="e7052-105">ACS-Minimum-Latency attribute</span></span>

<span data-ttu-id="e7052-106">Атрибут **ACS-Minimum-задержка** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7052-106">The **ACS-Minimum-Latency** attribute is for internal use only.</span></span> <span data-ttu-id="e7052-107">На основе RFC2210.</span><span class="sxs-lookup"><span data-stu-id="e7052-107">Based on RFC2210.</span></span>



| <span data-ttu-id="e7052-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-108">Entry</span></span> | <span data-ttu-id="e7052-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e7052-110">CN</span><span class="sxs-lookup"><span data-stu-id="e7052-110">CN</span></span>                | <span data-ttu-id="e7052-111">ACS — Минимальная задержка</span><span class="sxs-lookup"><span data-stu-id="e7052-111">ACS-Minimum-Latency</span></span>                  |
| <span data-ttu-id="e7052-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e7052-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e7052-113">аксминимумлатенци</span><span class="sxs-lookup"><span data-stu-id="e7052-113">aCSMinimumLatency</span></span>                    |
| <span data-ttu-id="e7052-114">Размер</span><span class="sxs-lookup"><span data-stu-id="e7052-114">Size</span></span>              | <span data-ttu-id="e7052-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="e7052-115">8 bytes</span></span>                              |
| <span data-ttu-id="e7052-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e7052-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e7052-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e7052-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e7052-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-118">Attribute-Id</span></span>      | <span data-ttu-id="e7052-119">1.2.840.113556.1.4.1316</span><span class="sxs-lookup"><span data-stu-id="e7052-119">1.2.840.113556.1.4.1316</span></span>              |
| <span data-ttu-id="e7052-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e7052-120">System-Id-Guid</span></span>    | <span data-ttu-id="e7052-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="e7052-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="e7052-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7052-122">Syntax</span></span>            | [<span data-ttu-id="e7052-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="e7052-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e7052-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e7052-124">Implementations</span></span>

-   [<span data-ttu-id="e7052-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e7052-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e7052-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7052-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7052-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7052-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7052-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7052-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7052-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7052-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7052-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7052-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e7052-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7052-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e7052-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-132">Entry</span></span> | <span data-ttu-id="e7052-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7052-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7052-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7052-136">System-Only</span></span>            | <span data-ttu-id="e7052-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-137">False</span></span>                                        |
| <span data-ttu-id="e7052-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7052-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e7052-139">True</span><span class="sxs-lookup"><span data-stu-id="e7052-139">True</span></span>                                         |
| <span data-ttu-id="e7052-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7052-140">Is Indexed</span></span>             | <span data-ttu-id="e7052-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-141">False</span></span>                                        |
| <span data-ttu-id="e7052-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7052-142">In Global Catalog</span></span>      | <span data-ttu-id="e7052-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-143">False</span></span>                                        |
| <span data-ttu-id="e7052-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7052-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7052-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7052-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7052-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7052-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7052-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7052-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7052-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-148">Search-Flags</span></span>           | <span data-ttu-id="e7052-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7052-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e7052-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-150">System-Flags</span></span>           | <span data-ttu-id="e7052-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7052-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e7052-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7052-152">Classes used in</span></span>        | [<span data-ttu-id="e7052-153">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="e7052-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e7052-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7052-154">Windows Server 2003</span></span>



| <span data-ttu-id="e7052-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-155">Entry</span></span> | <span data-ttu-id="e7052-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7052-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7052-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7052-159">System-Only</span></span>            | <span data-ttu-id="e7052-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-160">False</span></span>                                        |
| <span data-ttu-id="e7052-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7052-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e7052-162">True</span><span class="sxs-lookup"><span data-stu-id="e7052-162">True</span></span>                                         |
| <span data-ttu-id="e7052-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7052-163">Is Indexed</span></span>             | <span data-ttu-id="e7052-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-164">False</span></span>                                        |
| <span data-ttu-id="e7052-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7052-165">In Global Catalog</span></span>      | <span data-ttu-id="e7052-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-166">False</span></span>                                        |
| <span data-ttu-id="e7052-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7052-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7052-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7052-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7052-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7052-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7052-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7052-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7052-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-171">Search-Flags</span></span>           | <span data-ttu-id="e7052-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7052-172">0x00000000</span></span>                                   |
| <span data-ttu-id="e7052-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-173">System-Flags</span></span>           | <span data-ttu-id="e7052-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7052-174">0x00000010</span></span>                                   |
| <span data-ttu-id="e7052-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7052-175">Classes used in</span></span>        | [<span data-ttu-id="e7052-176">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="e7052-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7052-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7052-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7052-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-178">Entry</span></span> | <span data-ttu-id="e7052-179">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7052-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7052-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7052-182">System-Only</span></span>            | <span data-ttu-id="e7052-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-183">False</span></span>                                        |
| <span data-ttu-id="e7052-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7052-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e7052-185">True</span><span class="sxs-lookup"><span data-stu-id="e7052-185">True</span></span>                                         |
| <span data-ttu-id="e7052-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7052-186">Is Indexed</span></span>             | <span data-ttu-id="e7052-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-187">False</span></span>                                        |
| <span data-ttu-id="e7052-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7052-188">In Global Catalog</span></span>      | <span data-ttu-id="e7052-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-189">False</span></span>                                        |
| <span data-ttu-id="e7052-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7052-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7052-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7052-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7052-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7052-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7052-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7052-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7052-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-194">Search-Flags</span></span>           | <span data-ttu-id="e7052-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7052-195">0x00000000</span></span>                                   |
| <span data-ttu-id="e7052-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-196">System-Flags</span></span>           | <span data-ttu-id="e7052-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7052-197">0x00000010</span></span>                                   |
| <span data-ttu-id="e7052-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7052-198">Classes used in</span></span>        | [<span data-ttu-id="e7052-199">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="e7052-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7052-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7052-200">Windows Server 2008</span></span>



| <span data-ttu-id="e7052-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-201">Entry</span></span> | <span data-ttu-id="e7052-202">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7052-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7052-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7052-205">System-Only</span></span>            | <span data-ttu-id="e7052-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-206">False</span></span>                                        |
| <span data-ttu-id="e7052-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7052-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e7052-208">True</span><span class="sxs-lookup"><span data-stu-id="e7052-208">True</span></span>                                         |
| <span data-ttu-id="e7052-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7052-209">Is Indexed</span></span>             | <span data-ttu-id="e7052-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-210">False</span></span>                                        |
| <span data-ttu-id="e7052-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7052-211">In Global Catalog</span></span>      | <span data-ttu-id="e7052-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-212">False</span></span>                                        |
| <span data-ttu-id="e7052-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7052-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7052-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7052-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7052-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7052-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7052-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7052-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7052-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-217">Search-Flags</span></span>           | <span data-ttu-id="e7052-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7052-218">0x00000000</span></span>                                   |
| <span data-ttu-id="e7052-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-219">System-Flags</span></span>           | <span data-ttu-id="e7052-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7052-220">0x00000010</span></span>                                   |
| <span data-ttu-id="e7052-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7052-221">Classes used in</span></span>        | [<span data-ttu-id="e7052-222">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="e7052-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7052-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7052-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7052-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-224">Entry</span></span> | <span data-ttu-id="e7052-225">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7052-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7052-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7052-228">System-Only</span></span>            | <span data-ttu-id="e7052-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-229">False</span></span>                                        |
| <span data-ttu-id="e7052-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7052-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e7052-231">True</span><span class="sxs-lookup"><span data-stu-id="e7052-231">True</span></span>                                         |
| <span data-ttu-id="e7052-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7052-232">Is Indexed</span></span>             | <span data-ttu-id="e7052-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-233">False</span></span>                                        |
| <span data-ttu-id="e7052-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7052-234">In Global Catalog</span></span>      | <span data-ttu-id="e7052-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-235">False</span></span>                                        |
| <span data-ttu-id="e7052-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7052-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7052-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7052-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7052-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7052-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7052-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7052-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7052-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-240">Search-Flags</span></span>           | <span data-ttu-id="e7052-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7052-241">0x00000000</span></span>                                   |
| <span data-ttu-id="e7052-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-242">System-Flags</span></span>           | <span data-ttu-id="e7052-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7052-243">0x00000010</span></span>                                   |
| <span data-ttu-id="e7052-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7052-244">Classes used in</span></span>        | [<span data-ttu-id="e7052-245">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="e7052-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7052-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7052-246">Windows Server 2012</span></span>



| <span data-ttu-id="e7052-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7052-247">Entry</span></span> | <span data-ttu-id="e7052-248">Значение</span><span class="sxs-lookup"><span data-stu-id="e7052-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7052-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7052-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7052-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7052-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7052-251">System-Only</span></span>            | <span data-ttu-id="e7052-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-252">False</span></span>                                        |
| <span data-ttu-id="e7052-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7052-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e7052-254">True</span><span class="sxs-lookup"><span data-stu-id="e7052-254">True</span></span>                                         |
| <span data-ttu-id="e7052-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7052-255">Is Indexed</span></span>             | <span data-ttu-id="e7052-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-256">False</span></span>                                        |
| <span data-ttu-id="e7052-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7052-257">In Global Catalog</span></span>      | <span data-ttu-id="e7052-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7052-258">False</span></span>                                        |
| <span data-ttu-id="e7052-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7052-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7052-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7052-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7052-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7052-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7052-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7052-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7052-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-263">Search-Flags</span></span>           | <span data-ttu-id="e7052-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7052-264">0x00000000</span></span>                                   |
| <span data-ttu-id="e7052-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7052-265">System-Flags</span></span>           | <span data-ttu-id="e7052-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7052-266">0x00000010</span></span>                                   |
| <span data-ttu-id="e7052-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7052-267">Classes used in</span></span>        | [<span data-ttu-id="e7052-268">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="e7052-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





