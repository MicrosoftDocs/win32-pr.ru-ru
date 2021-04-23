---
title: Атрибут Prefix-Map
description: Атрибут Prefix-Map предназначен только для внутреннего использования.
ms.assetid: 814b8d47-ade9-49d9-a755-a47f7a9322c4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Prefix-Map
- Схема AD атрибута Префиксмап
topic_type:
- apiref
api_name:
- Prefix-Map
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354776b279551ae116d72a98c87cfeaa779529a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138519"
---
# <a name="prefix-map-attribute"></a><span data-ttu-id="ebe02-105">Атрибут Prefix-Map</span><span class="sxs-lookup"><span data-stu-id="ebe02-105">Prefix-Map attribute</span></span>

<span data-ttu-id="ebe02-106">Атрибут **префиксной схемы** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="ebe02-106">The **Prefix-Map** attribute is for internal use only.</span></span>



| <span data-ttu-id="ebe02-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-107">Entry</span></span> | <span data-ttu-id="ebe02-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ebe02-109">CN</span><span class="sxs-lookup"><span data-stu-id="ebe02-109">CN</span></span>                | <span data-ttu-id="ebe02-110">Prefix-Map</span><span class="sxs-lookup"><span data-stu-id="ebe02-110">Prefix-Map</span></span>                                            |
| <span data-ttu-id="ebe02-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ebe02-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ebe02-112">префиксмап</span><span class="sxs-lookup"><span data-stu-id="ebe02-112">prefixMap</span></span>                                             |
| <span data-ttu-id="ebe02-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ebe02-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ebe02-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ebe02-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ebe02-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ebe02-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ebe02-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-116">Attribute-Id</span></span>      | <span data-ttu-id="ebe02-117">1.2.840.113556.1.4.538</span><span class="sxs-lookup"><span data-stu-id="ebe02-117">1.2.840.113556.1.4.538</span></span>                                |
| <span data-ttu-id="ebe02-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ebe02-118">System-Id-Guid</span></span>    | <span data-ttu-id="ebe02-119">52458022-ca6a-11D0-аффф-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ebe02-119">52458022-ca6a-11d0-afff-0000f80367c1</span></span>                  |
| <span data-ttu-id="ebe02-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebe02-120">Syntax</span></span>            | [<span data-ttu-id="ebe02-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="ebe02-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ebe02-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ebe02-122">Implementations</span></span>

-   [<span data-ttu-id="ebe02-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ebe02-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ebe02-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ebe02-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ebe02-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ebe02-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ebe02-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ebe02-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ebe02-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ebe02-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ebe02-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ebe02-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ebe02-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ebe02-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ebe02-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ebe02-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ebe02-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-131">Entry</span></span> | <span data-ttu-id="ebe02-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-135">System-Only</span></span>            | <span data-ttu-id="ebe02-136">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-136">True</span></span>                            |
| <span data-ttu-id="ebe02-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-138">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-138">True</span></span>                            |
| <span data-ttu-id="ebe02-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-139">Is Indexed</span></span>             | <span data-ttu-id="ebe02-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-140">False</span></span>                           |
| <span data-ttu-id="ebe02-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-141">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-142">False</span></span>                           |
| <span data-ttu-id="ebe02-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-147">Search-Flags</span></span>           | <span data-ttu-id="ebe02-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-148">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-149">System-Flags</span></span>           | <span data-ttu-id="ebe02-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-150">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-151">Classes used in</span></span>        | [<span data-ttu-id="ebe02-152">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-152">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ebe02-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebe02-153">Windows Server 2003</span></span>



| <span data-ttu-id="ebe02-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-154">Entry</span></span> | <span data-ttu-id="ebe02-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-158">System-Only</span></span>            | <span data-ttu-id="ebe02-159">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-159">True</span></span>                            |
| <span data-ttu-id="ebe02-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-161">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-161">True</span></span>                            |
| <span data-ttu-id="ebe02-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-162">Is Indexed</span></span>             | <span data-ttu-id="ebe02-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-163">False</span></span>                           |
| <span data-ttu-id="ebe02-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-164">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-165">False</span></span>                           |
| <span data-ttu-id="ebe02-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-170">Search-Flags</span></span>           | <span data-ttu-id="ebe02-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-171">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-172">System-Flags</span></span>           | <span data-ttu-id="ebe02-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-173">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-174">Classes used in</span></span>        | [<span data-ttu-id="ebe02-175">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-175">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ebe02-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="ebe02-176">ADAM</span></span>



| <span data-ttu-id="ebe02-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-177">Entry</span></span> | <span data-ttu-id="ebe02-178">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-181">System-Only</span></span>            | <span data-ttu-id="ebe02-182">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-182">True</span></span>                            |
| <span data-ttu-id="ebe02-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-184">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-184">True</span></span>                            |
| <span data-ttu-id="ebe02-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-185">Is Indexed</span></span>             | <span data-ttu-id="ebe02-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-186">False</span></span>                           |
| <span data-ttu-id="ebe02-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-187">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-188">False</span></span>                           |
| <span data-ttu-id="ebe02-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-193">Search-Flags</span></span>           | <span data-ttu-id="ebe02-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-194">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-195">System-Flags</span></span>           | <span data-ttu-id="ebe02-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-196">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-197">Classes used in</span></span>        | [<span data-ttu-id="ebe02-198">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-198">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ebe02-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ebe02-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ebe02-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-200">Entry</span></span> | <span data-ttu-id="ebe02-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-204">System-Only</span></span>            | <span data-ttu-id="ebe02-205">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-205">True</span></span>                            |
| <span data-ttu-id="ebe02-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-207">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-207">True</span></span>                            |
| <span data-ttu-id="ebe02-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-208">Is Indexed</span></span>             | <span data-ttu-id="ebe02-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-209">False</span></span>                           |
| <span data-ttu-id="ebe02-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-210">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-211">False</span></span>                           |
| <span data-ttu-id="ebe02-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-216">Search-Flags</span></span>           | <span data-ttu-id="ebe02-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-217">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-218">System-Flags</span></span>           | <span data-ttu-id="ebe02-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-219">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-220">Classes used in</span></span>        | [<span data-ttu-id="ebe02-221">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-221">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ebe02-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebe02-222">Windows Server 2008</span></span>



| <span data-ttu-id="ebe02-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-223">Entry</span></span> | <span data-ttu-id="ebe02-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-227">System-Only</span></span>            | <span data-ttu-id="ebe02-228">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-228">True</span></span>                            |
| <span data-ttu-id="ebe02-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-230">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-230">True</span></span>                            |
| <span data-ttu-id="ebe02-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-231">Is Indexed</span></span>             | <span data-ttu-id="ebe02-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-232">False</span></span>                           |
| <span data-ttu-id="ebe02-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-233">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-234">False</span></span>                           |
| <span data-ttu-id="ebe02-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-239">Search-Flags</span></span>           | <span data-ttu-id="ebe02-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-240">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-241">System-Flags</span></span>           | <span data-ttu-id="ebe02-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-242">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-243">Classes used in</span></span>        | [<span data-ttu-id="ebe02-244">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-244">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ebe02-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebe02-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ebe02-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-246">Entry</span></span> | <span data-ttu-id="ebe02-247">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-250">System-Only</span></span>            | <span data-ttu-id="ebe02-251">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-251">True</span></span>                            |
| <span data-ttu-id="ebe02-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-253">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-253">True</span></span>                            |
| <span data-ttu-id="ebe02-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-254">Is Indexed</span></span>             | <span data-ttu-id="ebe02-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-255">False</span></span>                           |
| <span data-ttu-id="ebe02-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-256">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-257">False</span></span>                           |
| <span data-ttu-id="ebe02-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-262">Search-Flags</span></span>           | <span data-ttu-id="ebe02-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-263">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-264">System-Flags</span></span>           | <span data-ttu-id="ebe02-265">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-265">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-266">Classes used in</span></span>        | [<span data-ttu-id="ebe02-267">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-267">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ebe02-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ebe02-268">Windows Server 2012</span></span>



| <span data-ttu-id="ebe02-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebe02-269">Entry</span></span> | <span data-ttu-id="ebe02-270">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe02-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ebe02-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe02-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebe02-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ebe02-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebe02-273">System-Only</span></span>            | <span data-ttu-id="ebe02-274">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-274">True</span></span>                            |
| <span data-ttu-id="ebe02-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebe02-275">Is-Single-Valued</span></span>       | <span data-ttu-id="ebe02-276">True</span><span class="sxs-lookup"><span data-stu-id="ebe02-276">True</span></span>                            |
| <span data-ttu-id="ebe02-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebe02-277">Is Indexed</span></span>             | <span data-ttu-id="ebe02-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-278">False</span></span>                           |
| <span data-ttu-id="ebe02-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebe02-279">In Global Catalog</span></span>      | <span data-ttu-id="ebe02-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebe02-280">False</span></span>                           |
| <span data-ttu-id="ebe02-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebe02-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebe02-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebe02-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ebe02-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebe02-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ebe02-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebe02-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ebe02-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-285">Search-Flags</span></span>           | <span data-ttu-id="ebe02-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebe02-286">0x00000000</span></span>                      |
| <span data-ttu-id="ebe02-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebe02-287">System-Flags</span></span>           | <span data-ttu-id="ebe02-288">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ebe02-288">0x00000011</span></span>                      |
| <span data-ttu-id="ebe02-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebe02-289">Classes used in</span></span>        | [<span data-ttu-id="ebe02-290">**дмд**</span><span class="sxs-lookup"><span data-stu-id="ebe02-290">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





