---
title: Атрибут Allowed-Attributes
description: Атрибуты, которые будут разрешены для назначения классу.
ms.assetid: ea73d3b9-51fc-486e-a5c7-f5123c5620bf
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Allowed-Attributes
- Схема AD атрибута Алловедаттрибутес
topic_type:
- apiref
api_name:
- Allowed-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3049a6d03d17cb68062a38508baa09a4cdc91d6f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138318"
---
# <a name="allowed-attributes-attribute"></a><span data-ttu-id="d46e0-105">Атрибут Allowed-Attributes</span><span class="sxs-lookup"><span data-stu-id="d46e0-105">Allowed-Attributes attribute</span></span>

<span data-ttu-id="d46e0-106">Атрибуты, которые будут разрешены для назначения классу.</span><span class="sxs-lookup"><span data-stu-id="d46e0-106">Attributes that will be permitted to be assigned to a class.</span></span>



| <span data-ttu-id="d46e0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-107">Entry</span></span> | <span data-ttu-id="d46e0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d46e0-109">CN</span><span class="sxs-lookup"><span data-stu-id="d46e0-109">CN</span></span>                | <span data-ttu-id="d46e0-110">Allowed-Attributes</span><span class="sxs-lookup"><span data-stu-id="d46e0-110">Allowed-Attributes</span></span>                                              |
| <span data-ttu-id="d46e0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d46e0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d46e0-112">алловедаттрибутес</span><span class="sxs-lookup"><span data-stu-id="d46e0-112">allowedAttributes</span></span>                                               |
| <span data-ttu-id="d46e0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d46e0-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="d46e0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d46e0-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="d46e0-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d46e0-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="d46e0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-116">Attribute-Id</span></span>      | <span data-ttu-id="d46e0-117">1.2.840.113556.1.4.913</span><span class="sxs-lookup"><span data-stu-id="d46e0-117">1.2.840.113556.1.4.913</span></span>                                          |
| <span data-ttu-id="d46e0-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d46e0-118">System-Id-Guid</span></span>    | <span data-ttu-id="d46e0-119">9a7ad940-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="d46e0-119">9a7ad940-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="d46e0-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d46e0-120">Syntax</span></span>            | [<span data-ttu-id="d46e0-121">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="d46e0-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="d46e0-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d46e0-122">Implementations</span></span>

-   [<span data-ttu-id="d46e0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d46e0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d46e0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d46e0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d46e0-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d46e0-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d46e0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d46e0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d46e0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d46e0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d46e0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d46e0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d46e0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d46e0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d46e0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d46e0-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d46e0-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-131">Entry</span></span> | <span data-ttu-id="d46e0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-135">System-Only</span></span>            | <span data-ttu-id="d46e0-136">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-136">True</span></span>                            |
| <span data-ttu-id="d46e0-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-138">False</span></span>                           |
| <span data-ttu-id="d46e0-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-139">Is Indexed</span></span>             | <span data-ttu-id="d46e0-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-140">False</span></span>                           |
| <span data-ttu-id="d46e0-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-141">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-142">False</span></span>                           |
| <span data-ttu-id="d46e0-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-147">Search-Flags</span></span>           | <span data-ttu-id="d46e0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-148">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-149">System-Flags</span></span>           | <span data-ttu-id="d46e0-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-150">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-151">Classes used in</span></span>        | [<span data-ttu-id="d46e0-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d46e0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d46e0-153">Windows Server 2003</span></span>



| <span data-ttu-id="d46e0-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-154">Entry</span></span> | <span data-ttu-id="d46e0-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-158">System-Only</span></span>            | <span data-ttu-id="d46e0-159">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-159">True</span></span>                            |
| <span data-ttu-id="d46e0-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-161">False</span></span>                           |
| <span data-ttu-id="d46e0-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-162">Is Indexed</span></span>             | <span data-ttu-id="d46e0-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-163">False</span></span>                           |
| <span data-ttu-id="d46e0-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-164">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-165">False</span></span>                           |
| <span data-ttu-id="d46e0-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-170">Search-Flags</span></span>           | <span data-ttu-id="d46e0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-171">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-172">System-Flags</span></span>           | <span data-ttu-id="d46e0-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-173">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-174">Classes used in</span></span>        | [<span data-ttu-id="d46e0-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d46e0-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="d46e0-176">ADAM</span></span>



| <span data-ttu-id="d46e0-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-177">Entry</span></span> | <span data-ttu-id="d46e0-178">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-181">System-Only</span></span>            | <span data-ttu-id="d46e0-182">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-182">True</span></span>                            |
| <span data-ttu-id="d46e0-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-184">False</span></span>                           |
| <span data-ttu-id="d46e0-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-185">Is Indexed</span></span>             | <span data-ttu-id="d46e0-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-186">False</span></span>                           |
| <span data-ttu-id="d46e0-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-187">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-188">False</span></span>                           |
| <span data-ttu-id="d46e0-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-193">Search-Flags</span></span>           | <span data-ttu-id="d46e0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-194">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-195">System-Flags</span></span>           | <span data-ttu-id="d46e0-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-196">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-197">Classes used in</span></span>        | [<span data-ttu-id="d46e0-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d46e0-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d46e0-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d46e0-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-200">Entry</span></span> | <span data-ttu-id="d46e0-201">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-204">System-Only</span></span>            | <span data-ttu-id="d46e0-205">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-205">True</span></span>                            |
| <span data-ttu-id="d46e0-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-207">False</span></span>                           |
| <span data-ttu-id="d46e0-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-208">Is Indexed</span></span>             | <span data-ttu-id="d46e0-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-209">False</span></span>                           |
| <span data-ttu-id="d46e0-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-210">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-211">False</span></span>                           |
| <span data-ttu-id="d46e0-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-216">Search-Flags</span></span>           | <span data-ttu-id="d46e0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-217">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-218">System-Flags</span></span>           | <span data-ttu-id="d46e0-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-219">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-220">Classes used in</span></span>        | [<span data-ttu-id="d46e0-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d46e0-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d46e0-222">Windows Server 2008</span></span>



| <span data-ttu-id="d46e0-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-223">Entry</span></span> | <span data-ttu-id="d46e0-224">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-227">System-Only</span></span>            | <span data-ttu-id="d46e0-228">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-228">True</span></span>                            |
| <span data-ttu-id="d46e0-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-230">False</span></span>                           |
| <span data-ttu-id="d46e0-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-231">Is Indexed</span></span>             | <span data-ttu-id="d46e0-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-232">False</span></span>                           |
| <span data-ttu-id="d46e0-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-233">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-234">False</span></span>                           |
| <span data-ttu-id="d46e0-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-239">Search-Flags</span></span>           | <span data-ttu-id="d46e0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-240">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-241">System-Flags</span></span>           | <span data-ttu-id="d46e0-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-242">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-243">Classes used in</span></span>        | [<span data-ttu-id="d46e0-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d46e0-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d46e0-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d46e0-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-246">Entry</span></span> | <span data-ttu-id="d46e0-247">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-250">System-Only</span></span>            | <span data-ttu-id="d46e0-251">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-251">True</span></span>                            |
| <span data-ttu-id="d46e0-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-253">False</span></span>                           |
| <span data-ttu-id="d46e0-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-254">Is Indexed</span></span>             | <span data-ttu-id="d46e0-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-255">False</span></span>                           |
| <span data-ttu-id="d46e0-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-256">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-257">False</span></span>                           |
| <span data-ttu-id="d46e0-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-262">Search-Flags</span></span>           | <span data-ttu-id="d46e0-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-263">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-264">System-Flags</span></span>           | <span data-ttu-id="d46e0-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-265">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-266">Classes used in</span></span>        | [<span data-ttu-id="d46e0-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d46e0-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d46e0-268">Windows Server 2012</span></span>



| <span data-ttu-id="d46e0-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="d46e0-269">Entry</span></span> | <span data-ttu-id="d46e0-270">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e0-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d46e0-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d46e0-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d46e0-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d46e0-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="d46e0-273">System-Only</span></span>            | <span data-ttu-id="d46e0-274">True</span><span class="sxs-lookup"><span data-stu-id="d46e0-274">True</span></span>                            |
| <span data-ttu-id="d46e0-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d46e0-275">Is-Single-Valued</span></span>       | <span data-ttu-id="d46e0-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-276">False</span></span>                           |
| <span data-ttu-id="d46e0-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d46e0-277">Is Indexed</span></span>             | <span data-ttu-id="d46e0-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-278">False</span></span>                           |
| <span data-ttu-id="d46e0-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d46e0-279">In Global Catalog</span></span>      | <span data-ttu-id="d46e0-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="d46e0-280">False</span></span>                           |
| <span data-ttu-id="d46e0-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d46e0-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="d46e0-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d46e0-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d46e0-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d46e0-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d46e0-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d46e0-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d46e0-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-285">Search-Flags</span></span>           | <span data-ttu-id="d46e0-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d46e0-286">0x00000000</span></span>                      |
| <span data-ttu-id="d46e0-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d46e0-287">System-Flags</span></span>           | <span data-ttu-id="d46e0-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d46e0-288">0x08000014</span></span>                      |
| <span data-ttu-id="d46e0-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d46e0-289">Classes used in</span></span>        | [<span data-ttu-id="d46e0-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d46e0-290">**Top**</span></span>](c-top.md)<br/> |



 

 





