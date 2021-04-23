---
title: Атрибут CRL-Object
description: Ссылка на объект списка отзыва сертификатов, связанный с центром сертификации.
ms.assetid: 6f1abf8e-c93e-48d6-8ca1-a46b43bdd032
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута CRL-Object
- Схема AD атрибута Крлобжект
topic_type:
- apiref
api_name:
- CRL-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5460467dc28803ef2f225fb049f6ff4a9d8c0b47
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138278"
---
# <a name="crl-object-attribute"></a><span data-ttu-id="1778c-105">Атрибут CRL-Object</span><span class="sxs-lookup"><span data-stu-id="1778c-105">CRL-Object attribute</span></span>

<span data-ttu-id="1778c-106">Ссылка на объект списка отзыва сертификатов, связанный с центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="1778c-106">Reference to certificate revocation list object associated with a certification authority.</span></span>



| <span data-ttu-id="1778c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-107">Entry</span></span> | <span data-ttu-id="1778c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1778c-109">CN</span><span class="sxs-lookup"><span data-stu-id="1778c-109">CN</span></span>                | <span data-ttu-id="1778c-110">CRL-Object</span><span class="sxs-lookup"><span data-stu-id="1778c-110">CRL-Object</span></span>                              |
| <span data-ttu-id="1778c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1778c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1778c-112">крлобжект</span><span class="sxs-lookup"><span data-stu-id="1778c-112">cRLObject</span></span>                               |
| <span data-ttu-id="1778c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1778c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="1778c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1778c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="1778c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1778c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="1778c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-116">Attribute-Id</span></span>      | <span data-ttu-id="1778c-117">1.2.840.113556.1.4.689</span><span class="sxs-lookup"><span data-stu-id="1778c-117">1.2.840.113556.1.4.689</span></span>                  |
| <span data-ttu-id="1778c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1778c-118">System-Id-Guid</span></span>    | <span data-ttu-id="1778c-119">963d2737-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1778c-119">963d2737-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="1778c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1778c-120">Syntax</span></span>            | [<span data-ttu-id="1778c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1778c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1778c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1778c-122">Implementations</span></span>

-   [<span data-ttu-id="1778c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1778c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1778c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1778c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1778c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1778c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1778c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1778c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1778c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1778c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1778c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1778c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1778c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1778c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1778c-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-130">Entry</span></span> | <span data-ttu-id="1778c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1778c-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1778c-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1778c-134">System-Only</span></span>            | <span data-ttu-id="1778c-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-135">False</span></span>                                                                  |
| <span data-ttu-id="1778c-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1778c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1778c-137">True</span><span class="sxs-lookup"><span data-stu-id="1778c-137">True</span></span>                                                                   |
| <span data-ttu-id="1778c-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1778c-138">Is Indexed</span></span>             | <span data-ttu-id="1778c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-139">False</span></span>                                                                  |
| <span data-ttu-id="1778c-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1778c-140">In Global Catalog</span></span>      | <span data-ttu-id="1778c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-141">False</span></span>                                                                  |
| <span data-ttu-id="1778c-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1778c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1778c-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1778c-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1778c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1778c-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1778c-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-146">Search-Flags</span></span>           | <span data-ttu-id="1778c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1778c-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="1778c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-148">System-Flags</span></span>           | <span data-ttu-id="1778c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1778c-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="1778c-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1778c-150">Classes used in</span></span>        | [<span data-ttu-id="1778c-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1778c-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1778c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1778c-152">Windows Server 2003</span></span>



| <span data-ttu-id="1778c-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-153">Entry</span></span> | <span data-ttu-id="1778c-154">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1778c-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1778c-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1778c-157">System-Only</span></span>            | <span data-ttu-id="1778c-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-158">False</span></span>                                                                  |
| <span data-ttu-id="1778c-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1778c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1778c-160">True</span><span class="sxs-lookup"><span data-stu-id="1778c-160">True</span></span>                                                                   |
| <span data-ttu-id="1778c-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1778c-161">Is Indexed</span></span>             | <span data-ttu-id="1778c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-162">False</span></span>                                                                  |
| <span data-ttu-id="1778c-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1778c-163">In Global Catalog</span></span>      | <span data-ttu-id="1778c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-164">False</span></span>                                                                  |
| <span data-ttu-id="1778c-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1778c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1778c-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1778c-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1778c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1778c-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1778c-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-169">Search-Flags</span></span>           | <span data-ttu-id="1778c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1778c-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="1778c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-171">System-Flags</span></span>           | <span data-ttu-id="1778c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1778c-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="1778c-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1778c-173">Classes used in</span></span>        | [<span data-ttu-id="1778c-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1778c-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1778c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1778c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1778c-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-176">Entry</span></span> | <span data-ttu-id="1778c-177">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1778c-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1778c-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1778c-180">System-Only</span></span>            | <span data-ttu-id="1778c-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-181">False</span></span>                                                                  |
| <span data-ttu-id="1778c-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1778c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1778c-183">True</span><span class="sxs-lookup"><span data-stu-id="1778c-183">True</span></span>                                                                   |
| <span data-ttu-id="1778c-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1778c-184">Is Indexed</span></span>             | <span data-ttu-id="1778c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-185">False</span></span>                                                                  |
| <span data-ttu-id="1778c-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1778c-186">In Global Catalog</span></span>      | <span data-ttu-id="1778c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-187">False</span></span>                                                                  |
| <span data-ttu-id="1778c-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1778c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1778c-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1778c-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1778c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1778c-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1778c-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-192">Search-Flags</span></span>           | <span data-ttu-id="1778c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1778c-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="1778c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-194">System-Flags</span></span>           | <span data-ttu-id="1778c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1778c-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="1778c-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1778c-196">Classes used in</span></span>        | [<span data-ttu-id="1778c-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1778c-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1778c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1778c-198">Windows Server 2008</span></span>



| <span data-ttu-id="1778c-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-199">Entry</span></span> | <span data-ttu-id="1778c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1778c-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1778c-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1778c-203">System-Only</span></span>            | <span data-ttu-id="1778c-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-204">False</span></span>                                                                  |
| <span data-ttu-id="1778c-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1778c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1778c-206">True</span><span class="sxs-lookup"><span data-stu-id="1778c-206">True</span></span>                                                                   |
| <span data-ttu-id="1778c-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1778c-207">Is Indexed</span></span>             | <span data-ttu-id="1778c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-208">False</span></span>                                                                  |
| <span data-ttu-id="1778c-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1778c-209">In Global Catalog</span></span>      | <span data-ttu-id="1778c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-210">False</span></span>                                                                  |
| <span data-ttu-id="1778c-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1778c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1778c-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1778c-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1778c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1778c-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1778c-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-215">Search-Flags</span></span>           | <span data-ttu-id="1778c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1778c-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="1778c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-217">System-Flags</span></span>           | <span data-ttu-id="1778c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1778c-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="1778c-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1778c-219">Classes used in</span></span>        | [<span data-ttu-id="1778c-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1778c-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1778c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1778c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1778c-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-222">Entry</span></span> | <span data-ttu-id="1778c-223">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1778c-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1778c-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1778c-226">System-Only</span></span>            | <span data-ttu-id="1778c-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-227">False</span></span>                                                                  |
| <span data-ttu-id="1778c-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1778c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1778c-229">True</span><span class="sxs-lookup"><span data-stu-id="1778c-229">True</span></span>                                                                   |
| <span data-ttu-id="1778c-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1778c-230">Is Indexed</span></span>             | <span data-ttu-id="1778c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-231">False</span></span>                                                                  |
| <span data-ttu-id="1778c-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1778c-232">In Global Catalog</span></span>      | <span data-ttu-id="1778c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-233">False</span></span>                                                                  |
| <span data-ttu-id="1778c-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1778c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1778c-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1778c-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1778c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1778c-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1778c-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-238">Search-Flags</span></span>           | <span data-ttu-id="1778c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1778c-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="1778c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-240">System-Flags</span></span>           | <span data-ttu-id="1778c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1778c-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="1778c-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1778c-242">Classes used in</span></span>        | [<span data-ttu-id="1778c-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1778c-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1778c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1778c-244">Windows Server 2012</span></span>



| <span data-ttu-id="1778c-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="1778c-245">Entry</span></span> | <span data-ttu-id="1778c-246">Значение</span><span class="sxs-lookup"><span data-stu-id="1778c-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1778c-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1778c-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1778c-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1778c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="1778c-249">System-Only</span></span>            | <span data-ttu-id="1778c-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-250">False</span></span>                                                                  |
| <span data-ttu-id="1778c-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1778c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="1778c-252">True</span><span class="sxs-lookup"><span data-stu-id="1778c-252">True</span></span>                                                                   |
| <span data-ttu-id="1778c-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1778c-253">Is Indexed</span></span>             | <span data-ttu-id="1778c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-254">False</span></span>                                                                  |
| <span data-ttu-id="1778c-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1778c-255">In Global Catalog</span></span>      | <span data-ttu-id="1778c-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="1778c-256">False</span></span>                                                                  |
| <span data-ttu-id="1778c-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1778c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="1778c-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1778c-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1778c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1778c-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1778c-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1778c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-261">Search-Flags</span></span>           | <span data-ttu-id="1778c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1778c-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="1778c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1778c-263">System-Flags</span></span>           | <span data-ttu-id="1778c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1778c-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="1778c-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1778c-265">Classes used in</span></span>        | [<span data-ttu-id="1778c-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1778c-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





