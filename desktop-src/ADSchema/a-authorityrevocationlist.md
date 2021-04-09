---
title: "\"Центр-отзыв\"-атрибут списка"
description: Перекрестный сертификат, список отзыва сертификатов.
ms.assetid: a9bc7ed3-4600-41a7-bbe5-4ec546a421fa
ms.tgt_platform: multiple
keywords:
- Список отзыва, схема AD атрибута
- Схема AD атрибута Аусоритиревокатионлист
topic_type:
- apiref
api_name:
- Authority-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccc08cfb43bf4175bb51f2324e22c247d01f042
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139110"
---
# <a name="authority-revocation-list-attribute"></a><span data-ttu-id="6eabe-105">"Центр-отзыв"-атрибут списка</span><span class="sxs-lookup"><span data-stu-id="6eabe-105">Authority-Revocation-List attribute</span></span>

<span data-ttu-id="6eabe-106">Перекрестный сертификат, список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6eabe-106">Cross certificate, Certificate Revocation List.</span></span>



| <span data-ttu-id="6eabe-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-107">Entry</span></span> | <span data-ttu-id="6eabe-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6eabe-109">CN</span><span class="sxs-lookup"><span data-stu-id="6eabe-109">CN</span></span>                | <span data-ttu-id="6eabe-110">Список отзыва центров сертификации</span><span class="sxs-lookup"><span data-stu-id="6eabe-110">Authority-Revocation-List</span></span>                             |
| <span data-ttu-id="6eabe-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6eabe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6eabe-112">аусоритиревокатионлист</span><span class="sxs-lookup"><span data-stu-id="6eabe-112">authorityRevocationList</span></span>                               |
| <span data-ttu-id="6eabe-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6eabe-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6eabe-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6eabe-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6eabe-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6eabe-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6eabe-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-116">Attribute-Id</span></span>      | <span data-ttu-id="6eabe-117">2.5.4.38</span><span class="sxs-lookup"><span data-stu-id="6eabe-117">2.5.4.38</span></span>                                              |
| <span data-ttu-id="6eabe-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6eabe-118">System-Id-Guid</span></span>    | <span data-ttu-id="6eabe-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6eabe-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="6eabe-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6eabe-120">Syntax</span></span>            | [<span data-ttu-id="6eabe-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="6eabe-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6eabe-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6eabe-122">Implementations</span></span>

-   [<span data-ttu-id="6eabe-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6eabe-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6eabe-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6eabe-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6eabe-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6eabe-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6eabe-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6eabe-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6eabe-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6eabe-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6eabe-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6eabe-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6eabe-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6eabe-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6eabe-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-130">Entry</span></span> | <span data-ttu-id="6eabe-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eabe-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6eabe-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-133">MAPI-Id</span></span>                | <span data-ttu-id="6eabe-134">0x8026</span><span class="sxs-lookup"><span data-stu-id="6eabe-134">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="6eabe-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eabe-135">System-Only</span></span>            | <span data-ttu-id="6eabe-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6eabe-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6eabe-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6eabe-139">Is Indexed</span></span>             | <span data-ttu-id="6eabe-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6eabe-141">In Global Catalog</span></span>      | <span data-ttu-id="6eabe-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6eabe-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eabe-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6eabe-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="6eabe-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eabe-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eabe-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-147">Search-Flags</span></span>           | <span data-ttu-id="6eabe-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eabe-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-149">System-Flags</span></span>           | <span data-ttu-id="6eabe-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6eabe-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6eabe-151">Classes used in</span></span>        | [<span data-ttu-id="6eabe-152">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="6eabe-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="6eabe-153">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="6eabe-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6eabe-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6eabe-154">Windows Server 2003</span></span>



| <span data-ttu-id="6eabe-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-155">Entry</span></span> | <span data-ttu-id="6eabe-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eabe-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6eabe-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-158">MAPI-Id</span></span>                | <span data-ttu-id="6eabe-159">0x8026</span><span class="sxs-lookup"><span data-stu-id="6eabe-159">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="6eabe-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eabe-160">System-Only</span></span>            | <span data-ttu-id="6eabe-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6eabe-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6eabe-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6eabe-164">Is Indexed</span></span>             | <span data-ttu-id="6eabe-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6eabe-166">In Global Catalog</span></span>      | <span data-ttu-id="6eabe-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6eabe-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eabe-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6eabe-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="6eabe-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eabe-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eabe-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-172">Search-Flags</span></span>           | <span data-ttu-id="6eabe-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eabe-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-174">System-Flags</span></span>           | <span data-ttu-id="6eabe-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6eabe-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6eabe-176">Classes used in</span></span>        | [<span data-ttu-id="6eabe-177">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="6eabe-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="6eabe-178">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="6eabe-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6eabe-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6eabe-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6eabe-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-180">Entry</span></span> | <span data-ttu-id="6eabe-181">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eabe-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6eabe-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-183">MAPI-Id</span></span>                | <span data-ttu-id="6eabe-184">0x8026</span><span class="sxs-lookup"><span data-stu-id="6eabe-184">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="6eabe-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eabe-185">System-Only</span></span>            | <span data-ttu-id="6eabe-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6eabe-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6eabe-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6eabe-189">Is Indexed</span></span>             | <span data-ttu-id="6eabe-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6eabe-191">In Global Catalog</span></span>      | <span data-ttu-id="6eabe-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6eabe-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eabe-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6eabe-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="6eabe-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eabe-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eabe-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-197">Search-Flags</span></span>           | <span data-ttu-id="6eabe-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eabe-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-199">System-Flags</span></span>           | <span data-ttu-id="6eabe-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6eabe-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6eabe-201">Classes used in</span></span>        | [<span data-ttu-id="6eabe-202">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="6eabe-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="6eabe-203">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="6eabe-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6eabe-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eabe-204">Windows Server 2008</span></span>



| <span data-ttu-id="6eabe-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-205">Entry</span></span> | <span data-ttu-id="6eabe-206">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eabe-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6eabe-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-208">MAPI-Id</span></span>                | <span data-ttu-id="6eabe-209">0x8026</span><span class="sxs-lookup"><span data-stu-id="6eabe-209">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="6eabe-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eabe-210">System-Only</span></span>            | <span data-ttu-id="6eabe-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6eabe-212">Is-Single-Valued</span></span>       | <span data-ttu-id="6eabe-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6eabe-214">Is Indexed</span></span>             | <span data-ttu-id="6eabe-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6eabe-216">In Global Catalog</span></span>      | <span data-ttu-id="6eabe-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6eabe-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eabe-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6eabe-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="6eabe-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eabe-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eabe-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-222">Search-Flags</span></span>           | <span data-ttu-id="6eabe-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eabe-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-224">System-Flags</span></span>           | <span data-ttu-id="6eabe-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6eabe-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6eabe-226">Classes used in</span></span>        | [<span data-ttu-id="6eabe-227">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="6eabe-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="6eabe-228">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="6eabe-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6eabe-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6eabe-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6eabe-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-230">Entry</span></span> | <span data-ttu-id="6eabe-231">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eabe-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6eabe-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-233">MAPI-Id</span></span>                | <span data-ttu-id="6eabe-234">0x8026</span><span class="sxs-lookup"><span data-stu-id="6eabe-234">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="6eabe-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eabe-235">System-Only</span></span>            | <span data-ttu-id="6eabe-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6eabe-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6eabe-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6eabe-239">Is Indexed</span></span>             | <span data-ttu-id="6eabe-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6eabe-241">In Global Catalog</span></span>      | <span data-ttu-id="6eabe-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6eabe-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eabe-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6eabe-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="6eabe-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eabe-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eabe-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-247">Search-Flags</span></span>           | <span data-ttu-id="6eabe-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eabe-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-249">System-Flags</span></span>           | <span data-ttu-id="6eabe-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6eabe-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6eabe-251">Classes used in</span></span>        | [<span data-ttu-id="6eabe-252">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="6eabe-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="6eabe-253">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="6eabe-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6eabe-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6eabe-254">Windows Server 2012</span></span>



| <span data-ttu-id="6eabe-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="6eabe-255">Entry</span></span> | <span data-ttu-id="6eabe-256">Значение</span><span class="sxs-lookup"><span data-stu-id="6eabe-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eabe-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6eabe-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eabe-258">MAPI-Id</span></span>                | <span data-ttu-id="6eabe-259">0x8026</span><span class="sxs-lookup"><span data-stu-id="6eabe-259">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="6eabe-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eabe-260">System-Only</span></span>            | <span data-ttu-id="6eabe-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6eabe-262">Is-Single-Valued</span></span>       | <span data-ttu-id="6eabe-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6eabe-264">Is Indexed</span></span>             | <span data-ttu-id="6eabe-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6eabe-266">In Global Catalog</span></span>      | <span data-ttu-id="6eabe-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="6eabe-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="6eabe-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6eabe-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eabe-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6eabe-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="6eabe-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eabe-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eabe-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="6eabe-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-272">Search-Flags</span></span>           | <span data-ttu-id="6eabe-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eabe-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eabe-274">System-Flags</span></span>           | <span data-ttu-id="6eabe-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6eabe-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="6eabe-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6eabe-276">Classes used in</span></span>        | [<span data-ttu-id="6eabe-277">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="6eabe-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="6eabe-278">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="6eabe-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





