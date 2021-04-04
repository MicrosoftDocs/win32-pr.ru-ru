---
title: Атрибут списка изменений отзыва
description: Список сертификатов, отозванных с момента последнего разностного обновления.
ms.assetid: fc755c22-6d4f-4509-abb8-47c4f2f37545
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута списка отзыва изменений
- Схема AD атрибута Делтаревокатионлист
topic_type:
- apiref
api_name:
- Delta-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e866090dfb754c11fb4a25bbe904d5922a8fafd6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138203"
---
# <a name="delta-revocation-list-attribute"></a><span data-ttu-id="1ab9b-105">Атрибут списка изменений отзыва</span><span class="sxs-lookup"><span data-stu-id="1ab9b-105">Delta-Revocation-List attribute</span></span>

<span data-ttu-id="1ab9b-106">Список сертификатов, отозванных с момента последнего разностного обновления.</span><span class="sxs-lookup"><span data-stu-id="1ab9b-106">List of certificates that have been revoked since the last delta update.</span></span>



| <span data-ttu-id="1ab9b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-107">Entry</span></span> | <span data-ttu-id="1ab9b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1ab9b-109">CN</span><span class="sxs-lookup"><span data-stu-id="1ab9b-109">CN</span></span>                | <span data-ttu-id="1ab9b-110">Список отзыва изменений</span><span class="sxs-lookup"><span data-stu-id="1ab9b-110">Delta-Revocation-List</span></span>                                 |
| <span data-ttu-id="1ab9b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1ab9b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1ab9b-112">делтаревокатионлист</span><span class="sxs-lookup"><span data-stu-id="1ab9b-112">deltaRevocationList</span></span>                                   |
| <span data-ttu-id="1ab9b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1ab9b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="1ab9b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1ab9b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="1ab9b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1ab9b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="1ab9b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-116">Attribute-Id</span></span>      | <span data-ttu-id="1ab9b-117">2.5.4.53</span><span class="sxs-lookup"><span data-stu-id="1ab9b-117">2.5.4.53</span></span>                                              |
| <span data-ttu-id="1ab9b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1ab9b-118">System-Id-Guid</span></span>    | <span data-ttu-id="1ab9b-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1ab9b-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="1ab9b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ab9b-120">Syntax</span></span>            | [<span data-ttu-id="1ab9b-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="1ab9b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1ab9b-122">Implementations</span></span>

-   [<span data-ttu-id="1ab9b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ab9b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ab9b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ab9b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ab9b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ab9b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ab9b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ab9b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1ab9b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-130">Entry</span></span> | <span data-ttu-id="1ab9b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab9b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab9b-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-133">MAPI-Id</span></span>                | <span data-ttu-id="1ab9b-134">0x8C46</span><span class="sxs-lookup"><span data-stu-id="1ab9b-134">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="1ab9b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab9b-135">System-Only</span></span>            | <span data-ttu-id="1ab9b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab9b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab9b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab9b-139">Is Indexed</span></span>             | <span data-ttu-id="1ab9b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab9b-141">In Global Catalog</span></span>      | <span data-ttu-id="1ab9b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab9b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab9b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab9b-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="1ab9b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab9b-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab9b-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-147">Search-Flags</span></span>           | <span data-ttu-id="1ab9b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-149">System-Flags</span></span>           | <span data-ttu-id="1ab9b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-150">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab9b-151">Classes used in</span></span>        | [<span data-ttu-id="1ab9b-152">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="1ab9b-153">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ab9b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ab9b-154">Windows Server 2003</span></span>



| <span data-ttu-id="1ab9b-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-155">Entry</span></span> | <span data-ttu-id="1ab9b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab9b-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab9b-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-158">MAPI-Id</span></span>                | <span data-ttu-id="1ab9b-159">0x8C46</span><span class="sxs-lookup"><span data-stu-id="1ab9b-159">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="1ab9b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab9b-160">System-Only</span></span>            | <span data-ttu-id="1ab9b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab9b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab9b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab9b-164">Is Indexed</span></span>             | <span data-ttu-id="1ab9b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab9b-166">In Global Catalog</span></span>      | <span data-ttu-id="1ab9b-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab9b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab9b-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab9b-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="1ab9b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab9b-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab9b-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-172">Search-Flags</span></span>           | <span data-ttu-id="1ab9b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-174">System-Flags</span></span>           | <span data-ttu-id="1ab9b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-175">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab9b-176">Classes used in</span></span>        | [<span data-ttu-id="1ab9b-177">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="1ab9b-178">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ab9b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ab9b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ab9b-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-180">Entry</span></span> | <span data-ttu-id="1ab9b-181">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab9b-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab9b-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-183">MAPI-Id</span></span>                | <span data-ttu-id="1ab9b-184">0x8C46</span><span class="sxs-lookup"><span data-stu-id="1ab9b-184">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="1ab9b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab9b-185">System-Only</span></span>            | <span data-ttu-id="1ab9b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab9b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab9b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab9b-189">Is Indexed</span></span>             | <span data-ttu-id="1ab9b-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab9b-191">In Global Catalog</span></span>      | <span data-ttu-id="1ab9b-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab9b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab9b-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab9b-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="1ab9b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab9b-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab9b-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-197">Search-Flags</span></span>           | <span data-ttu-id="1ab9b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-199">System-Flags</span></span>           | <span data-ttu-id="1ab9b-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab9b-201">Classes used in</span></span>        | [<span data-ttu-id="1ab9b-202">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="1ab9b-203">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ab9b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ab9b-204">Windows Server 2008</span></span>



| <span data-ttu-id="1ab9b-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-205">Entry</span></span> | <span data-ttu-id="1ab9b-206">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab9b-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab9b-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-208">MAPI-Id</span></span>                | <span data-ttu-id="1ab9b-209">0x8C46</span><span class="sxs-lookup"><span data-stu-id="1ab9b-209">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="1ab9b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab9b-210">System-Only</span></span>            | <span data-ttu-id="1ab9b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab9b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab9b-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab9b-214">Is Indexed</span></span>             | <span data-ttu-id="1ab9b-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab9b-216">In Global Catalog</span></span>      | <span data-ttu-id="1ab9b-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab9b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab9b-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab9b-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="1ab9b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab9b-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab9b-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-222">Search-Flags</span></span>           | <span data-ttu-id="1ab9b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-224">System-Flags</span></span>           | <span data-ttu-id="1ab9b-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-225">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab9b-226">Classes used in</span></span>        | [<span data-ttu-id="1ab9b-227">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="1ab9b-228">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ab9b-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ab9b-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ab9b-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-230">Entry</span></span> | <span data-ttu-id="1ab9b-231">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab9b-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab9b-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-233">MAPI-Id</span></span>                | <span data-ttu-id="1ab9b-234">0x8C46</span><span class="sxs-lookup"><span data-stu-id="1ab9b-234">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="1ab9b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab9b-235">System-Only</span></span>            | <span data-ttu-id="1ab9b-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab9b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab9b-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab9b-239">Is Indexed</span></span>             | <span data-ttu-id="1ab9b-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab9b-241">In Global Catalog</span></span>      | <span data-ttu-id="1ab9b-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab9b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab9b-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab9b-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="1ab9b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab9b-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab9b-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-247">Search-Flags</span></span>           | <span data-ttu-id="1ab9b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-249">System-Flags</span></span>           | <span data-ttu-id="1ab9b-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab9b-251">Classes used in</span></span>        | [<span data-ttu-id="1ab9b-252">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="1ab9b-253">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ab9b-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ab9b-254">Windows Server 2012</span></span>



| <span data-ttu-id="1ab9b-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab9b-255">Entry</span></span> | <span data-ttu-id="1ab9b-256">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab9b-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab9b-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab9b-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab9b-258">MAPI-Id</span></span>                | <span data-ttu-id="1ab9b-259">0x8C46</span><span class="sxs-lookup"><span data-stu-id="1ab9b-259">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="1ab9b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab9b-260">System-Only</span></span>            | <span data-ttu-id="1ab9b-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab9b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab9b-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab9b-264">Is Indexed</span></span>             | <span data-ttu-id="1ab9b-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab9b-266">In Global Catalog</span></span>      | <span data-ttu-id="1ab9b-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab9b-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="1ab9b-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab9b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab9b-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab9b-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="1ab9b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab9b-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab9b-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="1ab9b-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-272">Search-Flags</span></span>           | <span data-ttu-id="1ab9b-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab9b-274">System-Flags</span></span>           | <span data-ttu-id="1ab9b-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab9b-275">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="1ab9b-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab9b-276">Classes used in</span></span>        | [<span data-ttu-id="1ab9b-277">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="1ab9b-278">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="1ab9b-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





