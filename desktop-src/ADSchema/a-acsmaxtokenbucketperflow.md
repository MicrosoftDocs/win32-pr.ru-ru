---
title: Атрибут ACS-Max-Token-контейнеров-Flow
description: Атрибут ACS-Max-Token-контейнеров-per-Flow предназначен только для внутреннего использования.
ms.assetid: 2c269bda-7b0d-4ef4-8c67-9f5e7c52e3ae
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута "ACS-Max-Token-контейнеров-для потока"
- Схема AD атрибута Аксмакстокенбуккетперфлов
topic_type:
- apiref
api_name:
- ACS-Max-Token-Bucket-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb323af82b270c20478e8af4aafc3ee4142125ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139130"
---
# <a name="acs-max-token-bucket-per-flow-attribute"></a><span data-ttu-id="8a3a3-105">Атрибут ACS-Max-Token-контейнеров-Flow</span><span class="sxs-lookup"><span data-stu-id="8a3a3-105">ACS-Max-Token-Bucket-Per-Flow attribute</span></span>

<span data-ttu-id="8a3a3-106">Атрибут **ACS-Max-Token-контейнеров-per-Flow** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="8a3a3-106">The **ACS-Max-Token-Bucket-Per-Flow** attribute is for internal use only.</span></span> <span data-ttu-id="8a3a3-107">На основе RFC2210.</span><span class="sxs-lookup"><span data-stu-id="8a3a3-107">Based on RFC2210.</span></span>



| <span data-ttu-id="8a3a3-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-108">Entry</span></span> | <span data-ttu-id="8a3a3-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8a3a3-110">CN</span><span class="sxs-lookup"><span data-stu-id="8a3a3-110">CN</span></span>                | <span data-ttu-id="8a3a3-111">ACS-Max-Token-контейнер-на поток</span><span class="sxs-lookup"><span data-stu-id="8a3a3-111">ACS-Max-Token-Bucket-Per-Flow</span></span>        |
| <span data-ttu-id="8a3a3-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8a3a3-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8a3a3-113">аксмакстокенбуккетперфлов</span><span class="sxs-lookup"><span data-stu-id="8a3a3-113">aCSMaxTokenBucketPerFlow</span></span>             |
| <span data-ttu-id="8a3a3-114">Размер</span><span class="sxs-lookup"><span data-stu-id="8a3a3-114">Size</span></span>              | <span data-ttu-id="8a3a3-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="8a3a3-115">8 bytes</span></span>                              |
| <span data-ttu-id="8a3a3-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8a3a3-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8a3a3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8a3a3-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8a3a3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-118">Attribute-Id</span></span>      | <span data-ttu-id="8a3a3-119">1.2.840.113556.1.4.1313</span><span class="sxs-lookup"><span data-stu-id="8a3a3-119">1.2.840.113556.1.4.1313</span></span>              |
| <span data-ttu-id="8a3a3-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8a3a3-120">System-Id-Guid</span></span>    | <span data-ttu-id="8a3a3-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="8a3a3-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="8a3a3-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a3a3-122">Syntax</span></span>            | [<span data-ttu-id="8a3a3-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8a3a3-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8a3a3-124">Implementations</span></span>

-   [<span data-ttu-id="8a3a3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a3a3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a3a3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a3a3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a3a3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a3a3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a3a3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a3a3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8a3a3-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-132">Entry</span></span> | <span data-ttu-id="8a3a3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8a3a3-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a3a3-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a3a3-136">System-Only</span></span>            | <span data-ttu-id="8a3a3-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-137">False</span></span>                                        |
| <span data-ttu-id="8a3a3-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a3a3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8a3a3-139">True</span><span class="sxs-lookup"><span data-stu-id="8a3a3-139">True</span></span>                                         |
| <span data-ttu-id="8a3a3-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a3a3-140">Is Indexed</span></span>             | <span data-ttu-id="8a3a3-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-141">False</span></span>                                        |
| <span data-ttu-id="8a3a3-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a3a3-142">In Global Catalog</span></span>      | <span data-ttu-id="8a3a3-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-143">False</span></span>                                        |
| <span data-ttu-id="8a3a3-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a3a3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a3a3-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a3a3-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8a3a3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a3a3-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a3a3-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-148">Search-Flags</span></span>           | <span data-ttu-id="8a3a3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3a3-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8a3a3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-150">System-Flags</span></span>           | <span data-ttu-id="8a3a3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a3a3-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8a3a3-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a3a3-152">Classes used in</span></span>        | [<span data-ttu-id="8a3a3-153">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a3a3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a3a3-154">Windows Server 2003</span></span>



| <span data-ttu-id="8a3a3-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-155">Entry</span></span> | <span data-ttu-id="8a3a3-156">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8a3a3-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a3a3-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a3a3-159">System-Only</span></span>            | <span data-ttu-id="8a3a3-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-160">False</span></span>                                        |
| <span data-ttu-id="8a3a3-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a3a3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8a3a3-162">True</span><span class="sxs-lookup"><span data-stu-id="8a3a3-162">True</span></span>                                         |
| <span data-ttu-id="8a3a3-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a3a3-163">Is Indexed</span></span>             | <span data-ttu-id="8a3a3-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-164">False</span></span>                                        |
| <span data-ttu-id="8a3a3-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a3a3-165">In Global Catalog</span></span>      | <span data-ttu-id="8a3a3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-166">False</span></span>                                        |
| <span data-ttu-id="8a3a3-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a3a3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a3a3-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a3a3-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8a3a3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a3a3-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a3a3-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-171">Search-Flags</span></span>           | <span data-ttu-id="8a3a3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3a3-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8a3a3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-173">System-Flags</span></span>           | <span data-ttu-id="8a3a3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a3a3-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8a3a3-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a3a3-175">Classes used in</span></span>        | [<span data-ttu-id="8a3a3-176">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a3a3-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a3a3-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a3a3-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-178">Entry</span></span> | <span data-ttu-id="8a3a3-179">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8a3a3-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a3a3-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a3a3-182">System-Only</span></span>            | <span data-ttu-id="8a3a3-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-183">False</span></span>                                        |
| <span data-ttu-id="8a3a3-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a3a3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8a3a3-185">True</span><span class="sxs-lookup"><span data-stu-id="8a3a3-185">True</span></span>                                         |
| <span data-ttu-id="8a3a3-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a3a3-186">Is Indexed</span></span>             | <span data-ttu-id="8a3a3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-187">False</span></span>                                        |
| <span data-ttu-id="8a3a3-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a3a3-188">In Global Catalog</span></span>      | <span data-ttu-id="8a3a3-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-189">False</span></span>                                        |
| <span data-ttu-id="8a3a3-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a3a3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a3a3-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a3a3-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8a3a3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a3a3-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a3a3-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-194">Search-Flags</span></span>           | <span data-ttu-id="8a3a3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3a3-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8a3a3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-196">System-Flags</span></span>           | <span data-ttu-id="8a3a3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a3a3-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8a3a3-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a3a3-198">Classes used in</span></span>        | [<span data-ttu-id="8a3a3-199">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a3a3-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a3a3-200">Windows Server 2008</span></span>



| <span data-ttu-id="8a3a3-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-201">Entry</span></span> | <span data-ttu-id="8a3a3-202">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8a3a3-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a3a3-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a3a3-205">System-Only</span></span>            | <span data-ttu-id="8a3a3-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-206">False</span></span>                                        |
| <span data-ttu-id="8a3a3-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a3a3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8a3a3-208">True</span><span class="sxs-lookup"><span data-stu-id="8a3a3-208">True</span></span>                                         |
| <span data-ttu-id="8a3a3-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a3a3-209">Is Indexed</span></span>             | <span data-ttu-id="8a3a3-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-210">False</span></span>                                        |
| <span data-ttu-id="8a3a3-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a3a3-211">In Global Catalog</span></span>      | <span data-ttu-id="8a3a3-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-212">False</span></span>                                        |
| <span data-ttu-id="8a3a3-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a3a3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a3a3-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a3a3-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8a3a3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a3a3-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a3a3-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-217">Search-Flags</span></span>           | <span data-ttu-id="8a3a3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3a3-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8a3a3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-219">System-Flags</span></span>           | <span data-ttu-id="8a3a3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a3a3-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8a3a3-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a3a3-221">Classes used in</span></span>        | [<span data-ttu-id="8a3a3-222">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a3a3-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a3a3-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a3a3-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-224">Entry</span></span> | <span data-ttu-id="8a3a3-225">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8a3a3-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a3a3-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a3a3-228">System-Only</span></span>            | <span data-ttu-id="8a3a3-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-229">False</span></span>                                        |
| <span data-ttu-id="8a3a3-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a3a3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8a3a3-231">True</span><span class="sxs-lookup"><span data-stu-id="8a3a3-231">True</span></span>                                         |
| <span data-ttu-id="8a3a3-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a3a3-232">Is Indexed</span></span>             | <span data-ttu-id="8a3a3-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-233">False</span></span>                                        |
| <span data-ttu-id="8a3a3-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a3a3-234">In Global Catalog</span></span>      | <span data-ttu-id="8a3a3-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-235">False</span></span>                                        |
| <span data-ttu-id="8a3a3-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a3a3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a3a3-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a3a3-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8a3a3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a3a3-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a3a3-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-240">Search-Flags</span></span>           | <span data-ttu-id="8a3a3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3a3-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8a3a3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-242">System-Flags</span></span>           | <span data-ttu-id="8a3a3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a3a3-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8a3a3-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a3a3-244">Classes used in</span></span>        | [<span data-ttu-id="8a3a3-245">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a3a3-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a3a3-246">Windows Server 2012</span></span>



| <span data-ttu-id="8a3a3-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a3a3-247">Entry</span></span> | <span data-ttu-id="8a3a3-248">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a3-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8a3a3-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a3a3-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a3a3-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8a3a3-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a3a3-251">System-Only</span></span>            | <span data-ttu-id="8a3a3-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-252">False</span></span>                                        |
| <span data-ttu-id="8a3a3-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a3a3-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8a3a3-254">True</span><span class="sxs-lookup"><span data-stu-id="8a3a3-254">True</span></span>                                         |
| <span data-ttu-id="8a3a3-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a3a3-255">Is Indexed</span></span>             | <span data-ttu-id="8a3a3-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-256">False</span></span>                                        |
| <span data-ttu-id="8a3a3-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a3a3-257">In Global Catalog</span></span>      | <span data-ttu-id="8a3a3-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a3a3-258">False</span></span>                                        |
| <span data-ttu-id="8a3a3-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a3a3-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a3a3-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a3a3-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8a3a3-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a3a3-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a3a3-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8a3a3-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-263">Search-Flags</span></span>           | <span data-ttu-id="8a3a3-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3a3-264">0x00000000</span></span>                                   |
| <span data-ttu-id="8a3a3-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a3a3-265">System-Flags</span></span>           | <span data-ttu-id="8a3a3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a3a3-266">0x00000010</span></span>                                   |
| <span data-ttu-id="8a3a3-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a3a3-267">Classes used in</span></span>        | [<span data-ttu-id="8a3a3-268">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="8a3a3-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





