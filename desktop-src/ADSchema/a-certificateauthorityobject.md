---
title: Certificate-Authority-атрибут объекта
description: Ссылка на центр сертификации, связанный с точкой распространения списка отзыва сертификатов.
ms.assetid: 8dfd4441-6b45-4dc4-aed8-e33aa7fd099f
ms.tgt_platform: multiple
keywords:
- Schema-Authority — схема AD атрибута объекта
- Схема AD атрибута Цертификатеаусоритйобжект
topic_type:
- apiref
api_name:
- Certificate-Authority-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65ffceb810cd6a4ef3033834dbf0f3c489f1506e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893966"
---
# <a name="certificate-authority-object-attribute"></a><span data-ttu-id="0d287-105">Certificate-Authority-атрибут объекта</span><span class="sxs-lookup"><span data-stu-id="0d287-105">Certificate-Authority-Object attribute</span></span>

<span data-ttu-id="0d287-106">Ссылка на центр сертификации, связанный с точкой распространения списка отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0d287-106">Reference to the certification authority associated with a Certificate Revocation List distribution point.</span></span>



| <span data-ttu-id="0d287-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-107">Entry</span></span> | <span data-ttu-id="0d287-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0d287-109">CN</span><span class="sxs-lookup"><span data-stu-id="0d287-109">CN</span></span>                | <span data-ttu-id="0d287-110">Certificate-Authority-объект</span><span class="sxs-lookup"><span data-stu-id="0d287-110">Certificate-Authority-Object</span></span>            |
| <span data-ttu-id="0d287-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0d287-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0d287-112">цертификатеаусоритйобжект</span><span class="sxs-lookup"><span data-stu-id="0d287-112">certificateAuthorityObject</span></span>              |
| <span data-ttu-id="0d287-113">Размер</span><span class="sxs-lookup"><span data-stu-id="0d287-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="0d287-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0d287-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="0d287-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0d287-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="0d287-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-116">Attribute-Id</span></span>      | <span data-ttu-id="0d287-117">1.2.840.113556.1.4.684</span><span class="sxs-lookup"><span data-stu-id="0d287-117">1.2.840.113556.1.4.684</span></span>                  |
| <span data-ttu-id="0d287-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0d287-118">System-Id-Guid</span></span>    | <span data-ttu-id="0d287-119">963d2732-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0d287-119">963d2732-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="0d287-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d287-120">Syntax</span></span>            | [<span data-ttu-id="0d287-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0d287-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="0d287-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0d287-122">Implementations</span></span>

-   [<span data-ttu-id="0d287-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0d287-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0d287-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0d287-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0d287-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0d287-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0d287-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0d287-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0d287-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0d287-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0d287-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0d287-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0d287-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0d287-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0d287-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-130">Entry</span></span> | <span data-ttu-id="0d287-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d287-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d287-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d287-134">System-Only</span></span>            | <span data-ttu-id="0d287-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-135">False</span></span>                                                               |
| <span data-ttu-id="0d287-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d287-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0d287-137">True</span><span class="sxs-lookup"><span data-stu-id="0d287-137">True</span></span>                                                                |
| <span data-ttu-id="0d287-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d287-138">Is Indexed</span></span>             | <span data-ttu-id="0d287-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-139">False</span></span>                                                               |
| <span data-ttu-id="0d287-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d287-140">In Global Catalog</span></span>      | <span data-ttu-id="0d287-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-141">False</span></span>                                                               |
| <span data-ttu-id="0d287-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d287-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d287-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d287-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="0d287-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d287-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d287-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-146">Search-Flags</span></span>           | <span data-ttu-id="0d287-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d287-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="0d287-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-148">System-Flags</span></span>           | <span data-ttu-id="0d287-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d287-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="0d287-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d287-150">Classes used in</span></span>        | [<span data-ttu-id="0d287-151">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="0d287-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0d287-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d287-152">Windows Server 2003</span></span>



| <span data-ttu-id="0d287-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-153">Entry</span></span> | <span data-ttu-id="0d287-154">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d287-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d287-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d287-157">System-Only</span></span>            | <span data-ttu-id="0d287-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-158">False</span></span>                                                               |
| <span data-ttu-id="0d287-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d287-159">Is-Single-Valued</span></span>       | <span data-ttu-id="0d287-160">True</span><span class="sxs-lookup"><span data-stu-id="0d287-160">True</span></span>                                                                |
| <span data-ttu-id="0d287-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d287-161">Is Indexed</span></span>             | <span data-ttu-id="0d287-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-162">False</span></span>                                                               |
| <span data-ttu-id="0d287-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d287-163">In Global Catalog</span></span>      | <span data-ttu-id="0d287-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-164">False</span></span>                                                               |
| <span data-ttu-id="0d287-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d287-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d287-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d287-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="0d287-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d287-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d287-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-169">Search-Flags</span></span>           | <span data-ttu-id="0d287-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d287-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="0d287-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-171">System-Flags</span></span>           | <span data-ttu-id="0d287-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d287-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="0d287-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d287-173">Classes used in</span></span>        | [<span data-ttu-id="0d287-174">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="0d287-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0d287-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0d287-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0d287-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-176">Entry</span></span> | <span data-ttu-id="0d287-177">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d287-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d287-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d287-180">System-Only</span></span>            | <span data-ttu-id="0d287-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-181">False</span></span>                                                               |
| <span data-ttu-id="0d287-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d287-182">Is-Single-Valued</span></span>       | <span data-ttu-id="0d287-183">True</span><span class="sxs-lookup"><span data-stu-id="0d287-183">True</span></span>                                                                |
| <span data-ttu-id="0d287-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d287-184">Is Indexed</span></span>             | <span data-ttu-id="0d287-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-185">False</span></span>                                                               |
| <span data-ttu-id="0d287-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d287-186">In Global Catalog</span></span>      | <span data-ttu-id="0d287-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-187">False</span></span>                                                               |
| <span data-ttu-id="0d287-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d287-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d287-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d287-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="0d287-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d287-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d287-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-192">Search-Flags</span></span>           | <span data-ttu-id="0d287-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d287-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="0d287-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-194">System-Flags</span></span>           | <span data-ttu-id="0d287-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d287-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="0d287-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d287-196">Classes used in</span></span>        | [<span data-ttu-id="0d287-197">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="0d287-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0d287-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d287-198">Windows Server 2008</span></span>



| <span data-ttu-id="0d287-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-199">Entry</span></span> | <span data-ttu-id="0d287-200">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d287-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d287-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d287-203">System-Only</span></span>            | <span data-ttu-id="0d287-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-204">False</span></span>                                                               |
| <span data-ttu-id="0d287-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d287-205">Is-Single-Valued</span></span>       | <span data-ttu-id="0d287-206">True</span><span class="sxs-lookup"><span data-stu-id="0d287-206">True</span></span>                                                                |
| <span data-ttu-id="0d287-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d287-207">Is Indexed</span></span>             | <span data-ttu-id="0d287-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-208">False</span></span>                                                               |
| <span data-ttu-id="0d287-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d287-209">In Global Catalog</span></span>      | <span data-ttu-id="0d287-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-210">False</span></span>                                                               |
| <span data-ttu-id="0d287-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d287-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d287-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d287-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="0d287-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d287-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d287-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-215">Search-Flags</span></span>           | <span data-ttu-id="0d287-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d287-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="0d287-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-217">System-Flags</span></span>           | <span data-ttu-id="0d287-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d287-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="0d287-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d287-219">Classes used in</span></span>        | [<span data-ttu-id="0d287-220">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="0d287-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0d287-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d287-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0d287-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-222">Entry</span></span> | <span data-ttu-id="0d287-223">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d287-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d287-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d287-226">System-Only</span></span>            | <span data-ttu-id="0d287-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-227">False</span></span>                                                               |
| <span data-ttu-id="0d287-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d287-228">Is-Single-Valued</span></span>       | <span data-ttu-id="0d287-229">True</span><span class="sxs-lookup"><span data-stu-id="0d287-229">True</span></span>                                                                |
| <span data-ttu-id="0d287-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d287-230">Is Indexed</span></span>             | <span data-ttu-id="0d287-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-231">False</span></span>                                                               |
| <span data-ttu-id="0d287-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d287-232">In Global Catalog</span></span>      | <span data-ttu-id="0d287-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-233">False</span></span>                                                               |
| <span data-ttu-id="0d287-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d287-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d287-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d287-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="0d287-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d287-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d287-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-238">Search-Flags</span></span>           | <span data-ttu-id="0d287-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d287-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="0d287-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-240">System-Flags</span></span>           | <span data-ttu-id="0d287-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d287-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="0d287-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d287-242">Classes used in</span></span>        | [<span data-ttu-id="0d287-243">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="0d287-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0d287-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d287-244">Windows Server 2012</span></span>



| <span data-ttu-id="0d287-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d287-245">Entry</span></span> | <span data-ttu-id="0d287-246">Значение</span><span class="sxs-lookup"><span data-stu-id="0d287-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d287-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d287-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d287-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="0d287-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d287-249">System-Only</span></span>            | <span data-ttu-id="0d287-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-250">False</span></span>                                                               |
| <span data-ttu-id="0d287-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d287-251">Is-Single-Valued</span></span>       | <span data-ttu-id="0d287-252">True</span><span class="sxs-lookup"><span data-stu-id="0d287-252">True</span></span>                                                                |
| <span data-ttu-id="0d287-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d287-253">Is Indexed</span></span>             | <span data-ttu-id="0d287-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-254">False</span></span>                                                               |
| <span data-ttu-id="0d287-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d287-255">In Global Catalog</span></span>      | <span data-ttu-id="0d287-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d287-256">False</span></span>                                                               |
| <span data-ttu-id="0d287-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d287-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d287-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d287-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="0d287-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d287-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d287-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="0d287-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-261">Search-Flags</span></span>           | <span data-ttu-id="0d287-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d287-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="0d287-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d287-263">System-Flags</span></span>           | <span data-ttu-id="0d287-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d287-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="0d287-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d287-265">Classes used in</span></span>        | [<span data-ttu-id="0d287-266">**Список CRL-точка распространения**</span><span class="sxs-lookup"><span data-stu-id="0d287-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





