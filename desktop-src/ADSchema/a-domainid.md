---
title: Атрибут domain-ID
description: Ссылка на домен, связанный с центром сертификации.
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "идентификатор домена"
- Схема AD атрибута Домаинид
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c321fdea062ccbca907e22a2d72b06c26110ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416233"
---
# <a name="domain-id-attribute"></a><span data-ttu-id="89a7d-105">Атрибут domain-ID</span><span class="sxs-lookup"><span data-stu-id="89a7d-105">Domain-ID attribute</span></span>

<span data-ttu-id="89a7d-106">Ссылка на домен, связанный с центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="89a7d-106">Reference to a domain that is associated with a certification authority.</span></span>



| <span data-ttu-id="89a7d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-107">Entry</span></span> | <span data-ttu-id="89a7d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="89a7d-109">CN</span><span class="sxs-lookup"><span data-stu-id="89a7d-109">CN</span></span>                | <span data-ttu-id="89a7d-110">Идентификатор домена</span><span class="sxs-lookup"><span data-stu-id="89a7d-110">Domain-ID</span></span>                               |
| <span data-ttu-id="89a7d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="89a7d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="89a7d-112">домаинид</span><span class="sxs-lookup"><span data-stu-id="89a7d-112">domainID</span></span>                                |
| <span data-ttu-id="89a7d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="89a7d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="89a7d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="89a7d-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="89a7d-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="89a7d-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="89a7d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-116">Attribute-Id</span></span>      | <span data-ttu-id="89a7d-117">1.2.840.113556.1.4.686</span><span class="sxs-lookup"><span data-stu-id="89a7d-117">1.2.840.113556.1.4.686</span></span>                  |
| <span data-ttu-id="89a7d-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="89a7d-118">System-Id-Guid</span></span>    | <span data-ttu-id="89a7d-119">963d2734-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="89a7d-119">963d2734-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="89a7d-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89a7d-120">Syntax</span></span>            | [<span data-ttu-id="89a7d-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="89a7d-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="89a7d-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="89a7d-122">Implementations</span></span>

-   [<span data-ttu-id="89a7d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="89a7d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="89a7d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="89a7d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="89a7d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="89a7d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="89a7d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="89a7d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="89a7d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="89a7d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="89a7d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="89a7d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="89a7d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89a7d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="89a7d-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-130">Entry</span></span> | <span data-ttu-id="89a7d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="89a7d-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="89a7d-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="89a7d-134">System-Only</span></span>            | <span data-ttu-id="89a7d-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-135">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="89a7d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="89a7d-137">True</span><span class="sxs-lookup"><span data-stu-id="89a7d-137">True</span></span>                                                                   |
| <span data-ttu-id="89a7d-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="89a7d-138">Is Indexed</span></span>             | <span data-ttu-id="89a7d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-139">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="89a7d-140">In Global Catalog</span></span>      | <span data-ttu-id="89a7d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-141">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="89a7d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="89a7d-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="89a7d-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="89a7d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89a7d-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89a7d-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-146">Search-Flags</span></span>           | <span data-ttu-id="89a7d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89a7d-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="89a7d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-148">System-Flags</span></span>           | <span data-ttu-id="89a7d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89a7d-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="89a7d-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="89a7d-150">Classes used in</span></span>        | [<span data-ttu-id="89a7d-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="89a7d-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="89a7d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89a7d-152">Windows Server 2003</span></span>



| <span data-ttu-id="89a7d-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-153">Entry</span></span> | <span data-ttu-id="89a7d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="89a7d-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="89a7d-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="89a7d-157">System-Only</span></span>            | <span data-ttu-id="89a7d-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-158">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="89a7d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="89a7d-160">True</span><span class="sxs-lookup"><span data-stu-id="89a7d-160">True</span></span>                                                                   |
| <span data-ttu-id="89a7d-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="89a7d-161">Is Indexed</span></span>             | <span data-ttu-id="89a7d-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-162">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="89a7d-163">In Global Catalog</span></span>      | <span data-ttu-id="89a7d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-164">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="89a7d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="89a7d-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="89a7d-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="89a7d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89a7d-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89a7d-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-169">Search-Flags</span></span>           | <span data-ttu-id="89a7d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89a7d-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="89a7d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-171">System-Flags</span></span>           | <span data-ttu-id="89a7d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89a7d-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="89a7d-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="89a7d-173">Classes used in</span></span>        | [<span data-ttu-id="89a7d-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="89a7d-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="89a7d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="89a7d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="89a7d-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-176">Entry</span></span> | <span data-ttu-id="89a7d-177">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="89a7d-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="89a7d-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="89a7d-180">System-Only</span></span>            | <span data-ttu-id="89a7d-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-181">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="89a7d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="89a7d-183">True</span><span class="sxs-lookup"><span data-stu-id="89a7d-183">True</span></span>                                                                   |
| <span data-ttu-id="89a7d-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="89a7d-184">Is Indexed</span></span>             | <span data-ttu-id="89a7d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-185">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="89a7d-186">In Global Catalog</span></span>      | <span data-ttu-id="89a7d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-187">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="89a7d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="89a7d-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="89a7d-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="89a7d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89a7d-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89a7d-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-192">Search-Flags</span></span>           | <span data-ttu-id="89a7d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89a7d-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="89a7d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-194">System-Flags</span></span>           | <span data-ttu-id="89a7d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89a7d-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="89a7d-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="89a7d-196">Classes used in</span></span>        | [<span data-ttu-id="89a7d-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="89a7d-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="89a7d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89a7d-198">Windows Server 2008</span></span>



| <span data-ttu-id="89a7d-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-199">Entry</span></span> | <span data-ttu-id="89a7d-200">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="89a7d-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="89a7d-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="89a7d-203">System-Only</span></span>            | <span data-ttu-id="89a7d-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-204">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="89a7d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="89a7d-206">True</span><span class="sxs-lookup"><span data-stu-id="89a7d-206">True</span></span>                                                                   |
| <span data-ttu-id="89a7d-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="89a7d-207">Is Indexed</span></span>             | <span data-ttu-id="89a7d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-208">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="89a7d-209">In Global Catalog</span></span>      | <span data-ttu-id="89a7d-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-210">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="89a7d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="89a7d-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="89a7d-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="89a7d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89a7d-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89a7d-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-215">Search-Flags</span></span>           | <span data-ttu-id="89a7d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89a7d-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="89a7d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-217">System-Flags</span></span>           | <span data-ttu-id="89a7d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89a7d-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="89a7d-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="89a7d-219">Classes used in</span></span>        | [<span data-ttu-id="89a7d-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="89a7d-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="89a7d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89a7d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="89a7d-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-222">Entry</span></span> | <span data-ttu-id="89a7d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="89a7d-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="89a7d-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="89a7d-226">System-Only</span></span>            | <span data-ttu-id="89a7d-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-227">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="89a7d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="89a7d-229">True</span><span class="sxs-lookup"><span data-stu-id="89a7d-229">True</span></span>                                                                   |
| <span data-ttu-id="89a7d-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="89a7d-230">Is Indexed</span></span>             | <span data-ttu-id="89a7d-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-231">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="89a7d-232">In Global Catalog</span></span>      | <span data-ttu-id="89a7d-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-233">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="89a7d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="89a7d-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="89a7d-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="89a7d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89a7d-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89a7d-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-238">Search-Flags</span></span>           | <span data-ttu-id="89a7d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89a7d-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="89a7d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-240">System-Flags</span></span>           | <span data-ttu-id="89a7d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89a7d-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="89a7d-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="89a7d-242">Classes used in</span></span>        | [<span data-ttu-id="89a7d-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="89a7d-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="89a7d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89a7d-244">Windows Server 2012</span></span>



| <span data-ttu-id="89a7d-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="89a7d-245">Entry</span></span> | <span data-ttu-id="89a7d-246">Значение</span><span class="sxs-lookup"><span data-stu-id="89a7d-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="89a7d-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="89a7d-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89a7d-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="89a7d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="89a7d-249">System-Only</span></span>            | <span data-ttu-id="89a7d-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-250">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="89a7d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="89a7d-252">True</span><span class="sxs-lookup"><span data-stu-id="89a7d-252">True</span></span>                                                                   |
| <span data-ttu-id="89a7d-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="89a7d-253">Is Indexed</span></span>             | <span data-ttu-id="89a7d-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-254">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="89a7d-255">In Global Catalog</span></span>      | <span data-ttu-id="89a7d-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="89a7d-256">False</span></span>                                                                  |
| <span data-ttu-id="89a7d-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="89a7d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="89a7d-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="89a7d-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="89a7d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89a7d-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89a7d-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="89a7d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-261">Search-Flags</span></span>           | <span data-ttu-id="89a7d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89a7d-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="89a7d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89a7d-263">System-Flags</span></span>           | <span data-ttu-id="89a7d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89a7d-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="89a7d-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="89a7d-265">Classes used in</span></span>        | [<span data-ttu-id="89a7d-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="89a7d-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





