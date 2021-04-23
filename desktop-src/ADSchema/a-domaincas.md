---
title: Атрибут domain-Certificate-органов
description: Список центров сертификации для данного домена.
ms.assetid: d773bf84-c318-4616-8e16-c14457707722
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "домен-сертификат-центр сертификации"
- Схема AD атрибута Домаинкас
topic_type:
- apiref
api_name:
- Domain-Certificate-Authorities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf68db97be2121bf1efaa0c0854736bd31e6127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989853"
---
# <a name="domain-certificate-authorities-attribute"></a><span data-ttu-id="93600-105">Атрибут domain-Certificate-органов</span><span class="sxs-lookup"><span data-stu-id="93600-105">Domain-Certificate-Authorities attribute</span></span>

<span data-ttu-id="93600-106">Список центров сертификации для данного домена.</span><span class="sxs-lookup"><span data-stu-id="93600-106">List of certification authorities for a given domain.</span></span>



| <span data-ttu-id="93600-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-107">Entry</span></span> | <span data-ttu-id="93600-108">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="93600-109">CN</span><span class="sxs-lookup"><span data-stu-id="93600-109">CN</span></span>                | <span data-ttu-id="93600-110">Домен — центры сертификации</span><span class="sxs-lookup"><span data-stu-id="93600-110">Domain-Certificate-Authorities</span></span>          |
| <span data-ttu-id="93600-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="93600-111">Ldap-Display-Name</span></span> | <span data-ttu-id="93600-112">домаинкас</span><span class="sxs-lookup"><span data-stu-id="93600-112">domainCAs</span></span>                               |
| <span data-ttu-id="93600-113">Размер</span><span class="sxs-lookup"><span data-stu-id="93600-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="93600-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="93600-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="93600-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="93600-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="93600-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93600-116">Attribute-Id</span></span>      | <span data-ttu-id="93600-117">1.2.840.113556.1.4.668</span><span class="sxs-lookup"><span data-stu-id="93600-117">1.2.840.113556.1.4.668</span></span>                  |
| <span data-ttu-id="93600-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="93600-118">System-Id-Guid</span></span>    | <span data-ttu-id="93600-119">7bfdcb7a-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="93600-119">7bfdcb7a-4807-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="93600-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93600-120">Syntax</span></span>            | [<span data-ttu-id="93600-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="93600-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="93600-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="93600-122">Implementations</span></span>

-   [<span data-ttu-id="93600-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="93600-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="93600-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93600-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93600-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93600-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93600-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93600-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93600-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93600-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93600-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93600-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="93600-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93600-129">Windows 2000 Server</span></span>



| <span data-ttu-id="93600-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-130">Entry</span></span> | <span data-ttu-id="93600-131">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="93600-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93600-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93600-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="93600-134">System-Only</span></span>            | <span data-ttu-id="93600-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-135">False</span></span>                                              |
| <span data-ttu-id="93600-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93600-136">Is-Single-Valued</span></span>       | <span data-ttu-id="93600-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-137">False</span></span>                                              |
| <span data-ttu-id="93600-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93600-138">Is Indexed</span></span>             | <span data-ttu-id="93600-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-139">False</span></span>                                              |
| <span data-ttu-id="93600-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93600-140">In Global Catalog</span></span>      | <span data-ttu-id="93600-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-141">False</span></span>                                              |
| <span data-ttu-id="93600-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93600-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="93600-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93600-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="93600-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93600-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="93600-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93600-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="93600-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-146">Search-Flags</span></span>           | <span data-ttu-id="93600-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93600-147">0x00000000</span></span>                                         |
| <span data-ttu-id="93600-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-148">System-Flags</span></span>           | <span data-ttu-id="93600-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93600-149">0x00000010</span></span>                                         |
| <span data-ttu-id="93600-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93600-150">Classes used in</span></span>        | [<span data-ttu-id="93600-151">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="93600-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="93600-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93600-152">Windows Server 2003</span></span>



| <span data-ttu-id="93600-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-153">Entry</span></span> | <span data-ttu-id="93600-154">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="93600-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93600-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93600-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="93600-157">System-Only</span></span>            | <span data-ttu-id="93600-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-158">False</span></span>                                              |
| <span data-ttu-id="93600-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93600-159">Is-Single-Valued</span></span>       | <span data-ttu-id="93600-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-160">False</span></span>                                              |
| <span data-ttu-id="93600-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93600-161">Is Indexed</span></span>             | <span data-ttu-id="93600-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-162">False</span></span>                                              |
| <span data-ttu-id="93600-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93600-163">In Global Catalog</span></span>      | <span data-ttu-id="93600-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-164">False</span></span>                                              |
| <span data-ttu-id="93600-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93600-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="93600-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93600-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="93600-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93600-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="93600-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93600-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="93600-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-169">Search-Flags</span></span>           | <span data-ttu-id="93600-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93600-170">0x00000000</span></span>                                         |
| <span data-ttu-id="93600-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-171">System-Flags</span></span>           | <span data-ttu-id="93600-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93600-172">0x00000010</span></span>                                         |
| <span data-ttu-id="93600-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93600-173">Classes used in</span></span>        | [<span data-ttu-id="93600-174">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="93600-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93600-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93600-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93600-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-176">Entry</span></span> | <span data-ttu-id="93600-177">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="93600-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93600-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93600-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="93600-180">System-Only</span></span>            | <span data-ttu-id="93600-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-181">False</span></span>                                              |
| <span data-ttu-id="93600-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93600-182">Is-Single-Valued</span></span>       | <span data-ttu-id="93600-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-183">False</span></span>                                              |
| <span data-ttu-id="93600-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93600-184">Is Indexed</span></span>             | <span data-ttu-id="93600-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-185">False</span></span>                                              |
| <span data-ttu-id="93600-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93600-186">In Global Catalog</span></span>      | <span data-ttu-id="93600-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-187">False</span></span>                                              |
| <span data-ttu-id="93600-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93600-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="93600-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93600-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="93600-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93600-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="93600-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93600-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="93600-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-192">Search-Flags</span></span>           | <span data-ttu-id="93600-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93600-193">0x00000000</span></span>                                         |
| <span data-ttu-id="93600-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-194">System-Flags</span></span>           | <span data-ttu-id="93600-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93600-195">0x00000010</span></span>                                         |
| <span data-ttu-id="93600-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93600-196">Classes used in</span></span>        | [<span data-ttu-id="93600-197">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="93600-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93600-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93600-198">Windows Server 2008</span></span>



| <span data-ttu-id="93600-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-199">Entry</span></span> | <span data-ttu-id="93600-200">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="93600-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93600-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93600-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="93600-203">System-Only</span></span>            | <span data-ttu-id="93600-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-204">False</span></span>                                              |
| <span data-ttu-id="93600-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93600-205">Is-Single-Valued</span></span>       | <span data-ttu-id="93600-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-206">False</span></span>                                              |
| <span data-ttu-id="93600-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93600-207">Is Indexed</span></span>             | <span data-ttu-id="93600-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-208">False</span></span>                                              |
| <span data-ttu-id="93600-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93600-209">In Global Catalog</span></span>      | <span data-ttu-id="93600-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-210">False</span></span>                                              |
| <span data-ttu-id="93600-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93600-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="93600-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93600-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="93600-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93600-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="93600-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93600-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="93600-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-215">Search-Flags</span></span>           | <span data-ttu-id="93600-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93600-216">0x00000000</span></span>                                         |
| <span data-ttu-id="93600-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-217">System-Flags</span></span>           | <span data-ttu-id="93600-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93600-218">0x00000010</span></span>                                         |
| <span data-ttu-id="93600-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93600-219">Classes used in</span></span>        | [<span data-ttu-id="93600-220">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="93600-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93600-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93600-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93600-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-222">Entry</span></span> | <span data-ttu-id="93600-223">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="93600-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93600-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93600-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="93600-226">System-Only</span></span>            | <span data-ttu-id="93600-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-227">False</span></span>                                              |
| <span data-ttu-id="93600-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93600-228">Is-Single-Valued</span></span>       | <span data-ttu-id="93600-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-229">False</span></span>                                              |
| <span data-ttu-id="93600-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93600-230">Is Indexed</span></span>             | <span data-ttu-id="93600-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-231">False</span></span>                                              |
| <span data-ttu-id="93600-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93600-232">In Global Catalog</span></span>      | <span data-ttu-id="93600-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-233">False</span></span>                                              |
| <span data-ttu-id="93600-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93600-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="93600-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93600-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="93600-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93600-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="93600-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93600-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="93600-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-238">Search-Flags</span></span>           | <span data-ttu-id="93600-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93600-239">0x00000000</span></span>                                         |
| <span data-ttu-id="93600-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-240">System-Flags</span></span>           | <span data-ttu-id="93600-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93600-241">0x00000010</span></span>                                         |
| <span data-ttu-id="93600-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93600-242">Classes used in</span></span>        | [<span data-ttu-id="93600-243">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="93600-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93600-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93600-244">Windows Server 2012</span></span>



| <span data-ttu-id="93600-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="93600-245">Entry</span></span> | <span data-ttu-id="93600-246">Значение</span><span class="sxs-lookup"><span data-stu-id="93600-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="93600-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93600-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93600-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="93600-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="93600-249">System-Only</span></span>            | <span data-ttu-id="93600-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-250">False</span></span>                                              |
| <span data-ttu-id="93600-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93600-251">Is-Single-Valued</span></span>       | <span data-ttu-id="93600-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-252">False</span></span>                                              |
| <span data-ttu-id="93600-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93600-253">Is Indexed</span></span>             | <span data-ttu-id="93600-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-254">False</span></span>                                              |
| <span data-ttu-id="93600-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93600-255">In Global Catalog</span></span>      | <span data-ttu-id="93600-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="93600-256">False</span></span>                                              |
| <span data-ttu-id="93600-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93600-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="93600-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93600-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="93600-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93600-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="93600-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93600-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="93600-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-261">Search-Flags</span></span>           | <span data-ttu-id="93600-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93600-262">0x00000000</span></span>                                         |
| <span data-ttu-id="93600-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93600-263">System-Flags</span></span>           | <span data-ttu-id="93600-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93600-264">0x00000010</span></span>                                         |
| <span data-ttu-id="93600-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93600-265">Classes used in</span></span>        | [<span data-ttu-id="93600-266">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="93600-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





