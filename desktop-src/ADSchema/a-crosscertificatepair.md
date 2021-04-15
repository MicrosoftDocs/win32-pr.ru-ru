---
title: Атрибут перекрестной пары сертификатов
description: V3 перекрестный сертификат.
ms.assetid: a6a2df06-4792-4874-a507-80c42b0606ec
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута пары сертификатов между сертификатами
- Схема AD атрибута Кроссцертификатепаир
topic_type:
- apiref
api_name:
- Cross-Certificate-Pair
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0c2bee3501cc2116330a75e38d573f2ca2e3eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654968"
---
# <a name="cross-certificate-pair-attribute"></a><span data-ttu-id="85198-105">Атрибут перекрестной пары сертификатов</span><span class="sxs-lookup"><span data-stu-id="85198-105">Cross-Certificate-Pair attribute</span></span>

<span data-ttu-id="85198-106">V3 перекрестный сертификат.</span><span class="sxs-lookup"><span data-stu-id="85198-106">V3 Cross Certificate.</span></span>



| <span data-ttu-id="85198-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-107">Entry</span></span> | <span data-ttu-id="85198-108">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="85198-109">CN</span><span class="sxs-lookup"><span data-stu-id="85198-109">CN</span></span>                | <span data-ttu-id="85198-110">Пара сертификатов между сертификатами</span><span class="sxs-lookup"><span data-stu-id="85198-110">Cross-Certificate-Pair</span></span>                                |
| <span data-ttu-id="85198-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="85198-111">Ldap-Display-Name</span></span> | <span data-ttu-id="85198-112">кроссцертификатепаир</span><span class="sxs-lookup"><span data-stu-id="85198-112">crossCertificatePair</span></span>                                  |
| <span data-ttu-id="85198-113">Размер</span><span class="sxs-lookup"><span data-stu-id="85198-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="85198-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="85198-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="85198-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="85198-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="85198-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="85198-116">Attribute-Id</span></span>      | <span data-ttu-id="85198-117">2.5.4.40</span><span class="sxs-lookup"><span data-stu-id="85198-117">2.5.4.40</span></span>                                              |
| <span data-ttu-id="85198-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="85198-118">System-Id-Guid</span></span>    | <span data-ttu-id="85198-119">167757b2-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="85198-119">167757b2-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="85198-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85198-120">Syntax</span></span>            | [<span data-ttu-id="85198-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="85198-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="85198-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="85198-122">Implementations</span></span>

-   [<span data-ttu-id="85198-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="85198-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="85198-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="85198-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="85198-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="85198-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="85198-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="85198-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="85198-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="85198-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="85198-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="85198-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="85198-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85198-129">Windows 2000 Server</span></span>



| <span data-ttu-id="85198-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-130">Entry</span></span> | <span data-ttu-id="85198-131">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="85198-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="85198-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="85198-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85198-133">MAPI-Id</span></span>                | <span data-ttu-id="85198-134">0x8025</span><span class="sxs-lookup"><span data-stu-id="85198-134">0x8025</span></span>                                                                 |
| <span data-ttu-id="85198-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="85198-135">System-Only</span></span>            | <span data-ttu-id="85198-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-136">False</span></span>                                                                  |
| <span data-ttu-id="85198-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="85198-137">Is-Single-Valued</span></span>       | <span data-ttu-id="85198-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-138">False</span></span>                                                                  |
| <span data-ttu-id="85198-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="85198-139">Is Indexed</span></span>             | <span data-ttu-id="85198-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-140">False</span></span>                                                                  |
| <span data-ttu-id="85198-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="85198-141">In Global Catalog</span></span>      | <span data-ttu-id="85198-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-142">False</span></span>                                                                  |
| <span data-ttu-id="85198-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="85198-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="85198-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="85198-144">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="85198-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85198-145">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85198-146">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-147">Search-Flags</span></span>           | <span data-ttu-id="85198-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85198-148">0x00000000</span></span>                                                             |
| <span data-ttu-id="85198-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-149">System-Flags</span></span>           | <span data-ttu-id="85198-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85198-150">0x00000010</span></span>                                                             |
| <span data-ttu-id="85198-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="85198-151">Classes used in</span></span>        | [<span data-ttu-id="85198-152">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="85198-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="85198-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="85198-153">Windows Server 2003</span></span>



| <span data-ttu-id="85198-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-154">Entry</span></span> | <span data-ttu-id="85198-155">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-155">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="85198-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="85198-156">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="85198-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85198-157">MAPI-Id</span></span>                | <span data-ttu-id="85198-158">0x8025</span><span class="sxs-lookup"><span data-stu-id="85198-158">0x8025</span></span>                                                                 |
| <span data-ttu-id="85198-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="85198-159">System-Only</span></span>            | <span data-ttu-id="85198-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-160">False</span></span>                                                                  |
| <span data-ttu-id="85198-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="85198-161">Is-Single-Valued</span></span>       | <span data-ttu-id="85198-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-162">False</span></span>                                                                  |
| <span data-ttu-id="85198-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="85198-163">Is Indexed</span></span>             | <span data-ttu-id="85198-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-164">False</span></span>                                                                  |
| <span data-ttu-id="85198-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="85198-165">In Global Catalog</span></span>      | <span data-ttu-id="85198-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-166">False</span></span>                                                                  |
| <span data-ttu-id="85198-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="85198-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="85198-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="85198-168">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="85198-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85198-169">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85198-170">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-171">Search-Flags</span></span>           | <span data-ttu-id="85198-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85198-172">0x00000000</span></span>                                                             |
| <span data-ttu-id="85198-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-173">System-Flags</span></span>           | <span data-ttu-id="85198-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85198-174">0x00000010</span></span>                                                             |
| <span data-ttu-id="85198-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="85198-175">Classes used in</span></span>        | [<span data-ttu-id="85198-176">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="85198-176">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="85198-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="85198-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="85198-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-178">Entry</span></span> | <span data-ttu-id="85198-179">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-179">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="85198-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="85198-180">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="85198-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85198-181">MAPI-Id</span></span>                | <span data-ttu-id="85198-182">0x8025</span><span class="sxs-lookup"><span data-stu-id="85198-182">0x8025</span></span>                                                                 |
| <span data-ttu-id="85198-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="85198-183">System-Only</span></span>            | <span data-ttu-id="85198-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-184">False</span></span>                                                                  |
| <span data-ttu-id="85198-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="85198-185">Is-Single-Valued</span></span>       | <span data-ttu-id="85198-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-186">False</span></span>                                                                  |
| <span data-ttu-id="85198-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="85198-187">Is Indexed</span></span>             | <span data-ttu-id="85198-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-188">False</span></span>                                                                  |
| <span data-ttu-id="85198-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="85198-189">In Global Catalog</span></span>      | <span data-ttu-id="85198-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-190">False</span></span>                                                                  |
| <span data-ttu-id="85198-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="85198-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="85198-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="85198-192">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="85198-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85198-193">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85198-194">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-195">Search-Flags</span></span>           | <span data-ttu-id="85198-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85198-196">0x00000000</span></span>                                                             |
| <span data-ttu-id="85198-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-197">System-Flags</span></span>           | <span data-ttu-id="85198-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85198-198">0x00000010</span></span>                                                             |
| <span data-ttu-id="85198-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="85198-199">Classes used in</span></span>        | [<span data-ttu-id="85198-200">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="85198-200">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="85198-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85198-201">Windows Server 2008</span></span>



| <span data-ttu-id="85198-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-202">Entry</span></span> | <span data-ttu-id="85198-203">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-203">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="85198-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="85198-204">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="85198-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85198-205">MAPI-Id</span></span>                | <span data-ttu-id="85198-206">0x8025</span><span class="sxs-lookup"><span data-stu-id="85198-206">0x8025</span></span>                                                                 |
| <span data-ttu-id="85198-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="85198-207">System-Only</span></span>            | <span data-ttu-id="85198-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-208">False</span></span>                                                                  |
| <span data-ttu-id="85198-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="85198-209">Is-Single-Valued</span></span>       | <span data-ttu-id="85198-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-210">False</span></span>                                                                  |
| <span data-ttu-id="85198-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="85198-211">Is Indexed</span></span>             | <span data-ttu-id="85198-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-212">False</span></span>                                                                  |
| <span data-ttu-id="85198-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="85198-213">In Global Catalog</span></span>      | <span data-ttu-id="85198-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-214">False</span></span>                                                                  |
| <span data-ttu-id="85198-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="85198-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="85198-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="85198-216">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="85198-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85198-217">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85198-218">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-219">Search-Flags</span></span>           | <span data-ttu-id="85198-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85198-220">0x00000000</span></span>                                                             |
| <span data-ttu-id="85198-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-221">System-Flags</span></span>           | <span data-ttu-id="85198-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85198-222">0x00000010</span></span>                                                             |
| <span data-ttu-id="85198-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="85198-223">Classes used in</span></span>        | [<span data-ttu-id="85198-224">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="85198-224">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="85198-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85198-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="85198-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-226">Entry</span></span> | <span data-ttu-id="85198-227">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-227">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="85198-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="85198-228">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="85198-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85198-229">MAPI-Id</span></span>                | <span data-ttu-id="85198-230">0x8025</span><span class="sxs-lookup"><span data-stu-id="85198-230">0x8025</span></span>                                                                 |
| <span data-ttu-id="85198-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="85198-231">System-Only</span></span>            | <span data-ttu-id="85198-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-232">False</span></span>                                                                  |
| <span data-ttu-id="85198-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="85198-233">Is-Single-Valued</span></span>       | <span data-ttu-id="85198-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-234">False</span></span>                                                                  |
| <span data-ttu-id="85198-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="85198-235">Is Indexed</span></span>             | <span data-ttu-id="85198-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-236">False</span></span>                                                                  |
| <span data-ttu-id="85198-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="85198-237">In Global Catalog</span></span>      | <span data-ttu-id="85198-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-238">False</span></span>                                                                  |
| <span data-ttu-id="85198-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="85198-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="85198-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="85198-240">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="85198-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85198-241">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85198-242">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-243">Search-Flags</span></span>           | <span data-ttu-id="85198-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85198-244">0x00000000</span></span>                                                             |
| <span data-ttu-id="85198-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-245">System-Flags</span></span>           | <span data-ttu-id="85198-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85198-246">0x00000010</span></span>                                                             |
| <span data-ttu-id="85198-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="85198-247">Classes used in</span></span>        | [<span data-ttu-id="85198-248">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="85198-248">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="85198-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85198-249">Windows Server 2012</span></span>



| <span data-ttu-id="85198-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="85198-250">Entry</span></span> | <span data-ttu-id="85198-251">Значение</span><span class="sxs-lookup"><span data-stu-id="85198-251">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="85198-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="85198-252">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="85198-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85198-253">MAPI-Id</span></span>                | <span data-ttu-id="85198-254">0x8025</span><span class="sxs-lookup"><span data-stu-id="85198-254">0x8025</span></span>                                                                 |
| <span data-ttu-id="85198-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="85198-255">System-Only</span></span>            | <span data-ttu-id="85198-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-256">False</span></span>                                                                  |
| <span data-ttu-id="85198-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="85198-257">Is-Single-Valued</span></span>       | <span data-ttu-id="85198-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-258">False</span></span>                                                                  |
| <span data-ttu-id="85198-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="85198-259">Is Indexed</span></span>             | <span data-ttu-id="85198-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-260">False</span></span>                                                                  |
| <span data-ttu-id="85198-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="85198-261">In Global Catalog</span></span>      | <span data-ttu-id="85198-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="85198-262">False</span></span>                                                                  |
| <span data-ttu-id="85198-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="85198-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="85198-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="85198-264">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="85198-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85198-265">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85198-266">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="85198-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-267">Search-Flags</span></span>           | <span data-ttu-id="85198-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85198-268">0x00000000</span></span>                                                             |
| <span data-ttu-id="85198-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85198-269">System-Flags</span></span>           | <span data-ttu-id="85198-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85198-270">0x00000010</span></span>                                                             |
| <span data-ttu-id="85198-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="85198-271">Classes used in</span></span>        | [<span data-ttu-id="85198-272">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="85198-272">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





