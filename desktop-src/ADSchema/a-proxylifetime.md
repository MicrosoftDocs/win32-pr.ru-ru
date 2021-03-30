---
title: Атрибут Proxy-Lifetime
description: Содержит время существования прокси-объекта.
ms.assetid: 67170516-fd8e-4126-8a39-deab9d228cf6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Proxy-Lifetime
- Схема AD атрибута Проксилифетиме
topic_type:
- apiref
api_name:
- Proxy-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f69dce5dff51c942bff26643220096a909b4b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804840"
---
# <a name="proxy-lifetime-attribute"></a><span data-ttu-id="b4d6b-105">Атрибут Proxy-Lifetime</span><span class="sxs-lookup"><span data-stu-id="b4d6b-105">Proxy-Lifetime attribute</span></span>

<span data-ttu-id="b4d6b-106">Содержит время существования прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="b4d6b-106">Contains the lifetime for a proxy object.</span></span>



| <span data-ttu-id="b4d6b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-107">Entry</span></span> | <span data-ttu-id="b4d6b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b4d6b-109">CN</span><span class="sxs-lookup"><span data-stu-id="b4d6b-109">CN</span></span>                | <span data-ttu-id="b4d6b-110">Proxy-Lifetime</span><span class="sxs-lookup"><span data-stu-id="b4d6b-110">Proxy-Lifetime</span></span>                       |
| <span data-ttu-id="b4d6b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b4d6b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b4d6b-112">проксилифетиме</span><span class="sxs-lookup"><span data-stu-id="b4d6b-112">proxyLifetime</span></span>                        |
| <span data-ttu-id="b4d6b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b4d6b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b4d6b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b4d6b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b4d6b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b4d6b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b4d6b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-116">Attribute-Id</span></span>      | <span data-ttu-id="b4d6b-117">1.2.840.113556.1.4.103</span><span class="sxs-lookup"><span data-stu-id="b4d6b-117">1.2.840.113556.1.4.103</span></span>               |
| <span data-ttu-id="b4d6b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b4d6b-118">System-Id-Guid</span></span>    | <span data-ttu-id="b4d6b-119">bf967a07-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b4d6b-119">bf967a07-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b4d6b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4d6b-120">Syntax</span></span>            | [<span data-ttu-id="b4d6b-121">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b4d6b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b4d6b-122">Implementations</span></span>

-   [<span data-ttu-id="b4d6b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4d6b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4d6b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4d6b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4d6b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4d6b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4d6b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4d6b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b4d6b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-130">Entry</span></span> | <span data-ttu-id="b4d6b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b4d6b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4d6b-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4d6b-134">System-Only</span></span>            | <span data-ttu-id="b4d6b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-135">False</span></span>                                              |
| <span data-ttu-id="b4d6b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4d6b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b4d6b-137">True</span><span class="sxs-lookup"><span data-stu-id="b4d6b-137">True</span></span>                                               |
| <span data-ttu-id="b4d6b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4d6b-138">Is Indexed</span></span>             | <span data-ttu-id="b4d6b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-139">False</span></span>                                              |
| <span data-ttu-id="b4d6b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4d6b-140">In Global Catalog</span></span>      | <span data-ttu-id="b4d6b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-141">False</span></span>                                              |
| <span data-ttu-id="b4d6b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4d6b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4d6b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4d6b-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b4d6b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4d6b-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4d6b-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-146">Search-Flags</span></span>           | <span data-ttu-id="b4d6b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4d6b-147">0x00000000</span></span>                                         |
| <span data-ttu-id="b4d6b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-148">System-Flags</span></span>           | <span data-ttu-id="b4d6b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4d6b-149">0x00000010</span></span>                                         |
| <span data-ttu-id="b4d6b-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4d6b-150">Classes used in</span></span>        | [<span data-ttu-id="b4d6b-151">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4d6b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4d6b-152">Windows Server 2003</span></span>



| <span data-ttu-id="b4d6b-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-153">Entry</span></span> | <span data-ttu-id="b4d6b-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b4d6b-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4d6b-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4d6b-157">System-Only</span></span>            | <span data-ttu-id="b4d6b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-158">False</span></span>                                              |
| <span data-ttu-id="b4d6b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4d6b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b4d6b-160">True</span><span class="sxs-lookup"><span data-stu-id="b4d6b-160">True</span></span>                                               |
| <span data-ttu-id="b4d6b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4d6b-161">Is Indexed</span></span>             | <span data-ttu-id="b4d6b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-162">False</span></span>                                              |
| <span data-ttu-id="b4d6b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4d6b-163">In Global Catalog</span></span>      | <span data-ttu-id="b4d6b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-164">False</span></span>                                              |
| <span data-ttu-id="b4d6b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4d6b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4d6b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4d6b-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b4d6b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4d6b-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4d6b-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-169">Search-Flags</span></span>           | <span data-ttu-id="b4d6b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4d6b-170">0x00000000</span></span>                                         |
| <span data-ttu-id="b4d6b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-171">System-Flags</span></span>           | <span data-ttu-id="b4d6b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4d6b-172">0x00000010</span></span>                                         |
| <span data-ttu-id="b4d6b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4d6b-173">Classes used in</span></span>        | [<span data-ttu-id="b4d6b-174">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4d6b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4d6b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4d6b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-176">Entry</span></span> | <span data-ttu-id="b4d6b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b4d6b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4d6b-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4d6b-180">System-Only</span></span>            | <span data-ttu-id="b4d6b-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-181">False</span></span>                                              |
| <span data-ttu-id="b4d6b-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4d6b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b4d6b-183">True</span><span class="sxs-lookup"><span data-stu-id="b4d6b-183">True</span></span>                                               |
| <span data-ttu-id="b4d6b-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4d6b-184">Is Indexed</span></span>             | <span data-ttu-id="b4d6b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-185">False</span></span>                                              |
| <span data-ttu-id="b4d6b-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4d6b-186">In Global Catalog</span></span>      | <span data-ttu-id="b4d6b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-187">False</span></span>                                              |
| <span data-ttu-id="b4d6b-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4d6b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4d6b-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4d6b-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b4d6b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4d6b-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4d6b-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-192">Search-Flags</span></span>           | <span data-ttu-id="b4d6b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4d6b-193">0x00000000</span></span>                                         |
| <span data-ttu-id="b4d6b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-194">System-Flags</span></span>           | <span data-ttu-id="b4d6b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4d6b-195">0x00000010</span></span>                                         |
| <span data-ttu-id="b4d6b-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4d6b-196">Classes used in</span></span>        | [<span data-ttu-id="b4d6b-197">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4d6b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4d6b-198">Windows Server 2008</span></span>



| <span data-ttu-id="b4d6b-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-199">Entry</span></span> | <span data-ttu-id="b4d6b-200">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b4d6b-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4d6b-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4d6b-203">System-Only</span></span>            | <span data-ttu-id="b4d6b-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-204">False</span></span>                                              |
| <span data-ttu-id="b4d6b-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4d6b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b4d6b-206">True</span><span class="sxs-lookup"><span data-stu-id="b4d6b-206">True</span></span>                                               |
| <span data-ttu-id="b4d6b-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4d6b-207">Is Indexed</span></span>             | <span data-ttu-id="b4d6b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-208">False</span></span>                                              |
| <span data-ttu-id="b4d6b-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4d6b-209">In Global Catalog</span></span>      | <span data-ttu-id="b4d6b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-210">False</span></span>                                              |
| <span data-ttu-id="b4d6b-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4d6b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4d6b-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4d6b-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b4d6b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4d6b-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4d6b-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-215">Search-Flags</span></span>           | <span data-ttu-id="b4d6b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4d6b-216">0x00000000</span></span>                                         |
| <span data-ttu-id="b4d6b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-217">System-Flags</span></span>           | <span data-ttu-id="b4d6b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4d6b-218">0x00000010</span></span>                                         |
| <span data-ttu-id="b4d6b-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4d6b-219">Classes used in</span></span>        | [<span data-ttu-id="b4d6b-220">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4d6b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4d6b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4d6b-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-222">Entry</span></span> | <span data-ttu-id="b4d6b-223">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b4d6b-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4d6b-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4d6b-226">System-Only</span></span>            | <span data-ttu-id="b4d6b-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-227">False</span></span>                                              |
| <span data-ttu-id="b4d6b-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4d6b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="b4d6b-229">True</span><span class="sxs-lookup"><span data-stu-id="b4d6b-229">True</span></span>                                               |
| <span data-ttu-id="b4d6b-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4d6b-230">Is Indexed</span></span>             | <span data-ttu-id="b4d6b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-231">False</span></span>                                              |
| <span data-ttu-id="b4d6b-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4d6b-232">In Global Catalog</span></span>      | <span data-ttu-id="b4d6b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-233">False</span></span>                                              |
| <span data-ttu-id="b4d6b-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4d6b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4d6b-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4d6b-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b4d6b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4d6b-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4d6b-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-238">Search-Flags</span></span>           | <span data-ttu-id="b4d6b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4d6b-239">0x00000000</span></span>                                         |
| <span data-ttu-id="b4d6b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-240">System-Flags</span></span>           | <span data-ttu-id="b4d6b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4d6b-241">0x00000010</span></span>                                         |
| <span data-ttu-id="b4d6b-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4d6b-242">Classes used in</span></span>        | [<span data-ttu-id="b4d6b-243">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4d6b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4d6b-244">Windows Server 2012</span></span>



| <span data-ttu-id="b4d6b-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4d6b-245">Entry</span></span> | <span data-ttu-id="b4d6b-246">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d6b-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b4d6b-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4d6b-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4d6b-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b4d6b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4d6b-249">System-Only</span></span>            | <span data-ttu-id="b4d6b-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-250">False</span></span>                                              |
| <span data-ttu-id="b4d6b-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4d6b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b4d6b-252">True</span><span class="sxs-lookup"><span data-stu-id="b4d6b-252">True</span></span>                                               |
| <span data-ttu-id="b4d6b-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4d6b-253">Is Indexed</span></span>             | <span data-ttu-id="b4d6b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-254">False</span></span>                                              |
| <span data-ttu-id="b4d6b-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4d6b-255">In Global Catalog</span></span>      | <span data-ttu-id="b4d6b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4d6b-256">False</span></span>                                              |
| <span data-ttu-id="b4d6b-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4d6b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4d6b-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4d6b-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b4d6b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4d6b-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4d6b-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b4d6b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-261">Search-Flags</span></span>           | <span data-ttu-id="b4d6b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4d6b-262">0x00000000</span></span>                                         |
| <span data-ttu-id="b4d6b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4d6b-263">System-Flags</span></span>           | <span data-ttu-id="b4d6b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4d6b-264">0x00000010</span></span>                                         |
| <span data-ttu-id="b4d6b-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4d6b-265">Classes used in</span></span>        | [<span data-ttu-id="b4d6b-266">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="b4d6b-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





