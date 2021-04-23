---
title: Атрибут списка отзыва сертификатов
description: Представляет список отозванных сертификатов.
ms.assetid: fb7b4888-15c0-475b-a87a-7cb0656963bb
ms.tgt_platform: multiple
keywords:
- Схема удостоверений для атрибута списка отзыва сертификатов
- Схема AD атрибута Цертификатеревокатионлист
topic_type:
- apiref
api_name:
- Certificate-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae77265ffeeae76ae07d608845723b1828772f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138290"
---
# <a name="certificate-revocation-list-attribute"></a><span data-ttu-id="82a85-105">Атрибут списка отзыва сертификатов</span><span class="sxs-lookup"><span data-stu-id="82a85-105">Certificate-Revocation-List attribute</span></span>

<span data-ttu-id="82a85-106">Представляет список отозванных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="82a85-106">Represents a list of certificates that have been revoked.</span></span>



| <span data-ttu-id="82a85-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-107">Entry</span></span> | <span data-ttu-id="82a85-108">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="82a85-109">CN</span><span class="sxs-lookup"><span data-stu-id="82a85-109">CN</span></span>                | <span data-ttu-id="82a85-110">Список отзыва сертификатов</span><span class="sxs-lookup"><span data-stu-id="82a85-110">Certificate-Revocation-List</span></span>                           |
| <span data-ttu-id="82a85-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="82a85-111">Ldap-Display-Name</span></span> | <span data-ttu-id="82a85-112">цертификатеревокатионлист</span><span class="sxs-lookup"><span data-stu-id="82a85-112">certificateRevocationList</span></span>                             |
| <span data-ttu-id="82a85-113">Размер</span><span class="sxs-lookup"><span data-stu-id="82a85-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="82a85-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="82a85-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="82a85-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="82a85-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="82a85-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-116">Attribute-Id</span></span>      | <span data-ttu-id="82a85-117">2.5.4.39</span><span class="sxs-lookup"><span data-stu-id="82a85-117">2.5.4.39</span></span>                                              |
| <span data-ttu-id="82a85-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="82a85-118">System-Id-Guid</span></span>    | <span data-ttu-id="82a85-119">1677579f-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="82a85-119">1677579f-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="82a85-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82a85-120">Syntax</span></span>            | [<span data-ttu-id="82a85-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="82a85-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="82a85-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="82a85-122">Implementations</span></span>

-   [<span data-ttu-id="82a85-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="82a85-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="82a85-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="82a85-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="82a85-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="82a85-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="82a85-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="82a85-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="82a85-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="82a85-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="82a85-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="82a85-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="82a85-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82a85-129">Windows 2000 Server</span></span>



| <span data-ttu-id="82a85-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-130">Entry</span></span> | <span data-ttu-id="82a85-131">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a85-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82a85-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="82a85-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-133">MAPI-Id</span></span>                | <span data-ttu-id="82a85-134">0x8016</span><span class="sxs-lookup"><span data-stu-id="82a85-134">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="82a85-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="82a85-135">System-Only</span></span>            | <span data-ttu-id="82a85-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82a85-137">Is-Single-Valued</span></span>       | <span data-ttu-id="82a85-138">True</span><span class="sxs-lookup"><span data-stu-id="82a85-138">True</span></span>                                                                                                                                       |
| <span data-ttu-id="82a85-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82a85-139">Is Indexed</span></span>             | <span data-ttu-id="82a85-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82a85-141">In Global Catalog</span></span>      | <span data-ttu-id="82a85-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82a85-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="82a85-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82a85-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="82a85-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82a85-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82a85-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-147">Search-Flags</span></span>           | <span data-ttu-id="82a85-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82a85-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-149">System-Flags</span></span>           | <span data-ttu-id="82a85-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82a85-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82a85-151">Classes used in</span></span>        | [<span data-ttu-id="82a85-152">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="82a85-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="82a85-153">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="82a85-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="82a85-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="82a85-154">Windows Server 2003</span></span>



| <span data-ttu-id="82a85-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-155">Entry</span></span> | <span data-ttu-id="82a85-156">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a85-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82a85-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="82a85-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-158">MAPI-Id</span></span>                | <span data-ttu-id="82a85-159">0x8016</span><span class="sxs-lookup"><span data-stu-id="82a85-159">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="82a85-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="82a85-160">System-Only</span></span>            | <span data-ttu-id="82a85-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82a85-162">Is-Single-Valued</span></span>       | <span data-ttu-id="82a85-163">True</span><span class="sxs-lookup"><span data-stu-id="82a85-163">True</span></span>                                                                                                                                       |
| <span data-ttu-id="82a85-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82a85-164">Is Indexed</span></span>             | <span data-ttu-id="82a85-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82a85-166">In Global Catalog</span></span>      | <span data-ttu-id="82a85-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82a85-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="82a85-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82a85-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="82a85-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82a85-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82a85-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-172">Search-Flags</span></span>           | <span data-ttu-id="82a85-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82a85-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-174">System-Flags</span></span>           | <span data-ttu-id="82a85-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82a85-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82a85-176">Classes used in</span></span>        | [<span data-ttu-id="82a85-177">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="82a85-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="82a85-178">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="82a85-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="82a85-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="82a85-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="82a85-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-180">Entry</span></span> | <span data-ttu-id="82a85-181">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a85-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82a85-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="82a85-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-183">MAPI-Id</span></span>                | <span data-ttu-id="82a85-184">0x8016</span><span class="sxs-lookup"><span data-stu-id="82a85-184">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="82a85-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="82a85-185">System-Only</span></span>            | <span data-ttu-id="82a85-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82a85-187">Is-Single-Valued</span></span>       | <span data-ttu-id="82a85-188">True</span><span class="sxs-lookup"><span data-stu-id="82a85-188">True</span></span>                                                                                                                                       |
| <span data-ttu-id="82a85-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82a85-189">Is Indexed</span></span>             | <span data-ttu-id="82a85-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82a85-191">In Global Catalog</span></span>      | <span data-ttu-id="82a85-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82a85-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="82a85-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82a85-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="82a85-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82a85-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82a85-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-197">Search-Flags</span></span>           | <span data-ttu-id="82a85-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82a85-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-199">System-Flags</span></span>           | <span data-ttu-id="82a85-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82a85-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82a85-201">Classes used in</span></span>        | [<span data-ttu-id="82a85-202">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="82a85-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="82a85-203">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="82a85-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="82a85-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82a85-204">Windows Server 2008</span></span>



| <span data-ttu-id="82a85-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-205">Entry</span></span> | <span data-ttu-id="82a85-206">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a85-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82a85-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="82a85-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-208">MAPI-Id</span></span>                | <span data-ttu-id="82a85-209">0x8016</span><span class="sxs-lookup"><span data-stu-id="82a85-209">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="82a85-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="82a85-210">System-Only</span></span>            | <span data-ttu-id="82a85-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82a85-212">Is-Single-Valued</span></span>       | <span data-ttu-id="82a85-213">True</span><span class="sxs-lookup"><span data-stu-id="82a85-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="82a85-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82a85-214">Is Indexed</span></span>             | <span data-ttu-id="82a85-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82a85-216">In Global Catalog</span></span>      | <span data-ttu-id="82a85-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82a85-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="82a85-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82a85-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="82a85-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82a85-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82a85-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-222">Search-Flags</span></span>           | <span data-ttu-id="82a85-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82a85-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-224">System-Flags</span></span>           | <span data-ttu-id="82a85-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82a85-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82a85-226">Classes used in</span></span>        | [<span data-ttu-id="82a85-227">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="82a85-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="82a85-228">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="82a85-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="82a85-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="82a85-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="82a85-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-230">Entry</span></span> | <span data-ttu-id="82a85-231">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a85-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82a85-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="82a85-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-233">MAPI-Id</span></span>                | <span data-ttu-id="82a85-234">0x8016</span><span class="sxs-lookup"><span data-stu-id="82a85-234">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="82a85-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="82a85-235">System-Only</span></span>            | <span data-ttu-id="82a85-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82a85-237">Is-Single-Valued</span></span>       | <span data-ttu-id="82a85-238">True</span><span class="sxs-lookup"><span data-stu-id="82a85-238">True</span></span>                                                                                                                                       |
| <span data-ttu-id="82a85-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82a85-239">Is Indexed</span></span>             | <span data-ttu-id="82a85-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82a85-241">In Global Catalog</span></span>      | <span data-ttu-id="82a85-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82a85-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="82a85-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82a85-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="82a85-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82a85-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82a85-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-247">Search-Flags</span></span>           | <span data-ttu-id="82a85-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82a85-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-249">System-Flags</span></span>           | <span data-ttu-id="82a85-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82a85-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82a85-251">Classes used in</span></span>        | [<span data-ttu-id="82a85-252">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="82a85-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="82a85-253">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="82a85-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="82a85-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82a85-254">Windows Server 2012</span></span>



| <span data-ttu-id="82a85-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="82a85-255">Entry</span></span> | <span data-ttu-id="82a85-256">Значение</span><span class="sxs-lookup"><span data-stu-id="82a85-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a85-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82a85-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="82a85-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82a85-258">MAPI-Id</span></span>                | <span data-ttu-id="82a85-259">0x8016</span><span class="sxs-lookup"><span data-stu-id="82a85-259">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="82a85-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="82a85-260">System-Only</span></span>            | <span data-ttu-id="82a85-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82a85-262">Is-Single-Valued</span></span>       | <span data-ttu-id="82a85-263">True</span><span class="sxs-lookup"><span data-stu-id="82a85-263">True</span></span>                                                                                                                                       |
| <span data-ttu-id="82a85-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82a85-264">Is Indexed</span></span>             | <span data-ttu-id="82a85-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82a85-266">In Global Catalog</span></span>      | <span data-ttu-id="82a85-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="82a85-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="82a85-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82a85-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="82a85-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82a85-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="82a85-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82a85-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82a85-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="82a85-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-272">Search-Flags</span></span>           | <span data-ttu-id="82a85-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82a85-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82a85-274">System-Flags</span></span>           | <span data-ttu-id="82a85-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82a85-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="82a85-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82a85-276">Classes used in</span></span>        | [<span data-ttu-id="82a85-277">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="82a85-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="82a85-278">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="82a85-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





