---
title: MS-PKI-Certificate-атрибут политики
description: Содержит список идентификаторов OID политики и их необязательных CSP в выданном сертификате.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута политики MS-PKI-Certificate
- Мспки-схема AD атрибута политики сертификата
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893418"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="bc649-105">MS-PKI-Certificate-атрибут политики</span><span class="sxs-lookup"><span data-stu-id="bc649-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="bc649-106">Содержит список идентификаторов OID политики и их необязательных CSP в выданном сертификате.</span><span class="sxs-lookup"><span data-stu-id="bc649-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="bc649-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc649-107">Entry</span></span> | <span data-ttu-id="bc649-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bc649-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc649-109">CN</span><span class="sxs-lookup"><span data-stu-id="bc649-109">CN</span></span>                | <span data-ttu-id="bc649-110">MS-PKI-Certificate-политика</span><span class="sxs-lookup"><span data-stu-id="bc649-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="bc649-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bc649-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bc649-112">Мспки — политика сертификата</span><span class="sxs-lookup"><span data-stu-id="bc649-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="bc649-113">Размер</span><span class="sxs-lookup"><span data-stu-id="bc649-113">Size</span></span>              | <span data-ttu-id="bc649-114">64 байт больше числа записей.</span><span class="sxs-lookup"><span data-stu-id="bc649-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="bc649-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bc649-115">Update Privilege</span></span>  | <span data-ttu-id="bc649-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="bc649-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="bc649-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bc649-117">Update Frequency</span></span>  | <span data-ttu-id="bc649-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="bc649-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="bc649-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc649-119">Attribute-Id</span></span>      | <span data-ttu-id="bc649-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="bc649-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="bc649-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bc649-121">System-Id-Guid</span></span>    | <span data-ttu-id="bc649-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="bc649-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="bc649-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc649-123">Syntax</span></span>            | [<span data-ttu-id="bc649-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="bc649-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="bc649-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bc649-125">Implementations</span></span>

-   [<span data-ttu-id="bc649-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc649-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc649-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc649-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc649-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc649-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc649-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc649-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc649-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc649-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bc649-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc649-131">Windows Server 2003</span></span>



| <span data-ttu-id="bc649-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc649-132">Entry</span></span> | <span data-ttu-id="bc649-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bc649-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc649-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc649-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc649-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc649-136">System-Only</span></span>            | <span data-ttu-id="bc649-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-137">False</span></span>                                                                   |
| <span data-ttu-id="bc649-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc649-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bc649-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-139">False</span></span>                                                                   |
| <span data-ttu-id="bc649-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc649-140">Is Indexed</span></span>             | <span data-ttu-id="bc649-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-141">False</span></span>                                                                   |
| <span data-ttu-id="bc649-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc649-142">In Global Catalog</span></span>      | <span data-ttu-id="bc649-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-143">False</span></span>                                                                   |
| <span data-ttu-id="bc649-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc649-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc649-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc649-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc649-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc649-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc649-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-148">Search-Flags</span></span>           | <span data-ttu-id="bc649-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc649-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc649-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-150">System-Flags</span></span>           | <span data-ttu-id="bc649-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc649-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc649-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc649-152">Classes used in</span></span>        | [<span data-ttu-id="bc649-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc649-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc649-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc649-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc649-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc649-155">Entry</span></span> | <span data-ttu-id="bc649-156">Значение</span><span class="sxs-lookup"><span data-stu-id="bc649-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc649-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc649-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc649-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc649-159">System-Only</span></span>            | <span data-ttu-id="bc649-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-160">False</span></span>                                                                   |
| <span data-ttu-id="bc649-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc649-161">Is-Single-Valued</span></span>       | <span data-ttu-id="bc649-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-162">False</span></span>                                                                   |
| <span data-ttu-id="bc649-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc649-163">Is Indexed</span></span>             | <span data-ttu-id="bc649-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-164">False</span></span>                                                                   |
| <span data-ttu-id="bc649-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc649-165">In Global Catalog</span></span>      | <span data-ttu-id="bc649-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-166">False</span></span>                                                                   |
| <span data-ttu-id="bc649-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc649-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc649-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc649-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc649-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc649-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc649-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-171">Search-Flags</span></span>           | <span data-ttu-id="bc649-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc649-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc649-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-173">System-Flags</span></span>           | <span data-ttu-id="bc649-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc649-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc649-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc649-175">Classes used in</span></span>        | [<span data-ttu-id="bc649-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc649-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc649-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc649-177">Windows Server 2008</span></span>



| <span data-ttu-id="bc649-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc649-178">Entry</span></span> | <span data-ttu-id="bc649-179">Значение</span><span class="sxs-lookup"><span data-stu-id="bc649-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc649-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc649-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc649-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc649-182">System-Only</span></span>            | <span data-ttu-id="bc649-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-183">False</span></span>                                                                   |
| <span data-ttu-id="bc649-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc649-184">Is-Single-Valued</span></span>       | <span data-ttu-id="bc649-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-185">False</span></span>                                                                   |
| <span data-ttu-id="bc649-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc649-186">Is Indexed</span></span>             | <span data-ttu-id="bc649-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-187">False</span></span>                                                                   |
| <span data-ttu-id="bc649-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc649-188">In Global Catalog</span></span>      | <span data-ttu-id="bc649-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-189">False</span></span>                                                                   |
| <span data-ttu-id="bc649-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc649-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc649-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc649-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc649-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc649-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc649-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-194">Search-Flags</span></span>           | <span data-ttu-id="bc649-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc649-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc649-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-196">System-Flags</span></span>           | <span data-ttu-id="bc649-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc649-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc649-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc649-198">Classes used in</span></span>        | [<span data-ttu-id="bc649-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc649-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc649-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc649-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc649-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc649-201">Entry</span></span> | <span data-ttu-id="bc649-202">Значение</span><span class="sxs-lookup"><span data-stu-id="bc649-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc649-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc649-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc649-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc649-205">System-Only</span></span>            | <span data-ttu-id="bc649-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-206">False</span></span>                                                                   |
| <span data-ttu-id="bc649-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc649-207">Is-Single-Valued</span></span>       | <span data-ttu-id="bc649-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-208">False</span></span>                                                                   |
| <span data-ttu-id="bc649-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc649-209">Is Indexed</span></span>             | <span data-ttu-id="bc649-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-210">False</span></span>                                                                   |
| <span data-ttu-id="bc649-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc649-211">In Global Catalog</span></span>      | <span data-ttu-id="bc649-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-212">False</span></span>                                                                   |
| <span data-ttu-id="bc649-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc649-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc649-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc649-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc649-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc649-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc649-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-217">Search-Flags</span></span>           | <span data-ttu-id="bc649-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc649-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc649-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-219">System-Flags</span></span>           | <span data-ttu-id="bc649-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc649-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc649-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc649-221">Classes used in</span></span>        | [<span data-ttu-id="bc649-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc649-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc649-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc649-223">Windows Server 2012</span></span>



| <span data-ttu-id="bc649-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc649-224">Entry</span></span> | <span data-ttu-id="bc649-225">Значение</span><span class="sxs-lookup"><span data-stu-id="bc649-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc649-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc649-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc649-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc649-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc649-228">System-Only</span></span>            | <span data-ttu-id="bc649-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-229">False</span></span>                                                                   |
| <span data-ttu-id="bc649-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc649-230">Is-Single-Valued</span></span>       | <span data-ttu-id="bc649-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-231">False</span></span>                                                                   |
| <span data-ttu-id="bc649-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc649-232">Is Indexed</span></span>             | <span data-ttu-id="bc649-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-233">False</span></span>                                                                   |
| <span data-ttu-id="bc649-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc649-234">In Global Catalog</span></span>      | <span data-ttu-id="bc649-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc649-235">False</span></span>                                                                   |
| <span data-ttu-id="bc649-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc649-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc649-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc649-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc649-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc649-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc649-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc649-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-240">Search-Flags</span></span>           | <span data-ttu-id="bc649-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc649-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc649-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc649-242">System-Flags</span></span>           | <span data-ttu-id="bc649-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc649-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc649-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc649-244">Classes used in</span></span>        | [<span data-ttu-id="bc649-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc649-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





