---
title: Список CRL-секционированный--атрибут списка отзыва
description: Инфраструктура открытых ключей \ 8211; списки отзыва.
ms.assetid: ecee7ee6-21e7-4861-a7f5-5e8e3579978a
ms.tgt_platform: multiple
keywords:
- Список CRL — схема AD с секционированным списком отзыва
- Схема AD атрибута Крлпартитионедревокатионлист
topic_type:
- apiref
api_name:
- CRL-Partitioned-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c19629cab11e9e6e02069213487135bea4d2aa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893962"
---
# <a name="crl-partitioned-revocation-list-attribute"></a><span data-ttu-id="fda9f-105">Список CRL-секционированный--атрибут списка отзыва</span><span class="sxs-lookup"><span data-stu-id="fda9f-105">CRL-Partitioned-Revocation-List attribute</span></span>

<span data-ttu-id="fda9f-106">Списки отзыва инфраструктуры открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="fda9f-106">Public Key Infrastructure revocation lists.</span></span>



| <span data-ttu-id="fda9f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-107">Entry</span></span> | <span data-ttu-id="fda9f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="fda9f-109">CN</span><span class="sxs-lookup"><span data-stu-id="fda9f-109">CN</span></span>                | <span data-ttu-id="fda9f-110">Список отзыва сертификатов-секционированный-отзыва</span><span class="sxs-lookup"><span data-stu-id="fda9f-110">CRL-Partitioned-Revocation-List</span></span>                       |
| <span data-ttu-id="fda9f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fda9f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fda9f-112">крлпартитионедревокатионлист</span><span class="sxs-lookup"><span data-stu-id="fda9f-112">cRLPartitionedRevocationList</span></span>                          |
| <span data-ttu-id="fda9f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="fda9f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="fda9f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fda9f-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="fda9f-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fda9f-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="fda9f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-116">Attribute-Id</span></span>      | <span data-ttu-id="fda9f-117">1.2.840.113556.1.4.683</span><span class="sxs-lookup"><span data-stu-id="fda9f-117">1.2.840.113556.1.4.683</span></span>                                |
| <span data-ttu-id="fda9f-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fda9f-118">System-Id-Guid</span></span>    | <span data-ttu-id="fda9f-119">963d2731-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fda9f-119">963d2731-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="fda9f-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fda9f-120">Syntax</span></span>            | [<span data-ttu-id="fda9f-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="fda9f-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="fda9f-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fda9f-122">Implementations</span></span>

-   [<span data-ttu-id="fda9f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fda9f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fda9f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fda9f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fda9f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fda9f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fda9f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fda9f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fda9f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fda9f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fda9f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fda9f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fda9f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fda9f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="fda9f-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-130">Entry</span></span> | <span data-ttu-id="fda9f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fda9f-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fda9f-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda9f-134">System-Only</span></span>            | <span data-ttu-id="fda9f-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-135">False</span></span>                                                               |
| <span data-ttu-id="fda9f-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fda9f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="fda9f-137">True</span><span class="sxs-lookup"><span data-stu-id="fda9f-137">True</span></span>                                                                |
| <span data-ttu-id="fda9f-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fda9f-138">Is Indexed</span></span>             | <span data-ttu-id="fda9f-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-139">False</span></span>                                                               |
| <span data-ttu-id="fda9f-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fda9f-140">In Global Catalog</span></span>      | <span data-ttu-id="fda9f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-141">False</span></span>                                                               |
| <span data-ttu-id="fda9f-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fda9f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda9f-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fda9f-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fda9f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda9f-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda9f-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-146">Search-Flags</span></span>           | <span data-ttu-id="fda9f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda9f-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="fda9f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-148">System-Flags</span></span>           | <span data-ttu-id="fda9f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda9f-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="fda9f-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fda9f-150">Classes used in</span></span>        | [<span data-ttu-id="fda9f-151">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="fda9f-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fda9f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fda9f-152">Windows Server 2003</span></span>



| <span data-ttu-id="fda9f-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-153">Entry</span></span> | <span data-ttu-id="fda9f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fda9f-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fda9f-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda9f-157">System-Only</span></span>            | <span data-ttu-id="fda9f-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-158">False</span></span>                                                               |
| <span data-ttu-id="fda9f-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fda9f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="fda9f-160">True</span><span class="sxs-lookup"><span data-stu-id="fda9f-160">True</span></span>                                                                |
| <span data-ttu-id="fda9f-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fda9f-161">Is Indexed</span></span>             | <span data-ttu-id="fda9f-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-162">False</span></span>                                                               |
| <span data-ttu-id="fda9f-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fda9f-163">In Global Catalog</span></span>      | <span data-ttu-id="fda9f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-164">False</span></span>                                                               |
| <span data-ttu-id="fda9f-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fda9f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda9f-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fda9f-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fda9f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda9f-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda9f-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-169">Search-Flags</span></span>           | <span data-ttu-id="fda9f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda9f-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="fda9f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-171">System-Flags</span></span>           | <span data-ttu-id="fda9f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda9f-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="fda9f-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fda9f-173">Classes used in</span></span>        | [<span data-ttu-id="fda9f-174">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="fda9f-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fda9f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fda9f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fda9f-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-176">Entry</span></span> | <span data-ttu-id="fda9f-177">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fda9f-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fda9f-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda9f-180">System-Only</span></span>            | <span data-ttu-id="fda9f-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-181">False</span></span>                                                               |
| <span data-ttu-id="fda9f-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fda9f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="fda9f-183">True</span><span class="sxs-lookup"><span data-stu-id="fda9f-183">True</span></span>                                                                |
| <span data-ttu-id="fda9f-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fda9f-184">Is Indexed</span></span>             | <span data-ttu-id="fda9f-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-185">False</span></span>                                                               |
| <span data-ttu-id="fda9f-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fda9f-186">In Global Catalog</span></span>      | <span data-ttu-id="fda9f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-187">False</span></span>                                                               |
| <span data-ttu-id="fda9f-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fda9f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda9f-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fda9f-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fda9f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda9f-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda9f-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-192">Search-Flags</span></span>           | <span data-ttu-id="fda9f-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda9f-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="fda9f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-194">System-Flags</span></span>           | <span data-ttu-id="fda9f-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda9f-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="fda9f-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fda9f-196">Classes used in</span></span>        | [<span data-ttu-id="fda9f-197">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="fda9f-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fda9f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fda9f-198">Windows Server 2008</span></span>



| <span data-ttu-id="fda9f-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-199">Entry</span></span> | <span data-ttu-id="fda9f-200">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fda9f-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fda9f-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda9f-203">System-Only</span></span>            | <span data-ttu-id="fda9f-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-204">False</span></span>                                                               |
| <span data-ttu-id="fda9f-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fda9f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="fda9f-206">True</span><span class="sxs-lookup"><span data-stu-id="fda9f-206">True</span></span>                                                                |
| <span data-ttu-id="fda9f-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fda9f-207">Is Indexed</span></span>             | <span data-ttu-id="fda9f-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-208">False</span></span>                                                               |
| <span data-ttu-id="fda9f-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fda9f-209">In Global Catalog</span></span>      | <span data-ttu-id="fda9f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-210">False</span></span>                                                               |
| <span data-ttu-id="fda9f-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fda9f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda9f-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fda9f-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fda9f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda9f-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda9f-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-215">Search-Flags</span></span>           | <span data-ttu-id="fda9f-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda9f-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="fda9f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-217">System-Flags</span></span>           | <span data-ttu-id="fda9f-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda9f-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="fda9f-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fda9f-219">Classes used in</span></span>        | [<span data-ttu-id="fda9f-220">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="fda9f-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fda9f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fda9f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fda9f-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-222">Entry</span></span> | <span data-ttu-id="fda9f-223">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fda9f-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fda9f-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda9f-226">System-Only</span></span>            | <span data-ttu-id="fda9f-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-227">False</span></span>                                                               |
| <span data-ttu-id="fda9f-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fda9f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="fda9f-229">True</span><span class="sxs-lookup"><span data-stu-id="fda9f-229">True</span></span>                                                                |
| <span data-ttu-id="fda9f-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fda9f-230">Is Indexed</span></span>             | <span data-ttu-id="fda9f-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-231">False</span></span>                                                               |
| <span data-ttu-id="fda9f-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fda9f-232">In Global Catalog</span></span>      | <span data-ttu-id="fda9f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-233">False</span></span>                                                               |
| <span data-ttu-id="fda9f-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fda9f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda9f-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fda9f-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fda9f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda9f-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda9f-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-238">Search-Flags</span></span>           | <span data-ttu-id="fda9f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda9f-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="fda9f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-240">System-Flags</span></span>           | <span data-ttu-id="fda9f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda9f-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="fda9f-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fda9f-242">Classes used in</span></span>        | [<span data-ttu-id="fda9f-243">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="fda9f-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fda9f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fda9f-244">Windows Server 2012</span></span>



| <span data-ttu-id="fda9f-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="fda9f-245">Entry</span></span> | <span data-ttu-id="fda9f-246">Значение</span><span class="sxs-lookup"><span data-stu-id="fda9f-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fda9f-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fda9f-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fda9f-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fda9f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="fda9f-249">System-Only</span></span>            | <span data-ttu-id="fda9f-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-250">False</span></span>                                                               |
| <span data-ttu-id="fda9f-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fda9f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="fda9f-252">True</span><span class="sxs-lookup"><span data-stu-id="fda9f-252">True</span></span>                                                                |
| <span data-ttu-id="fda9f-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fda9f-253">Is Indexed</span></span>             | <span data-ttu-id="fda9f-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-254">False</span></span>                                                               |
| <span data-ttu-id="fda9f-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fda9f-255">In Global Catalog</span></span>      | <span data-ttu-id="fda9f-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="fda9f-256">False</span></span>                                                               |
| <span data-ttu-id="fda9f-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fda9f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="fda9f-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fda9f-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fda9f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fda9f-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fda9f-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fda9f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-261">Search-Flags</span></span>           | <span data-ttu-id="fda9f-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fda9f-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="fda9f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fda9f-263">System-Flags</span></span>           | <span data-ttu-id="fda9f-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fda9f-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="fda9f-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fda9f-265">Classes used in</span></span>        | [<span data-ttu-id="fda9f-266">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="fda9f-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





