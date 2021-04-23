---
title: атрибут MS-PKI-RA-Signature
description: Указывает количество подписей центра регистрации, необходимых для запроса на регистрацию.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута подписи MS-PKI-RA-Signature
- Мспки-RA-схема AD атрибута Signature
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655138"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="698b0-105">атрибут MS-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="698b0-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="698b0-106">Указывает количество подписей центра регистрации, необходимых для запроса на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="698b0-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="698b0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="698b0-107">Entry</span></span> | <span data-ttu-id="698b0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="698b0-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="698b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="698b0-109">CN</span></span>                | <span data-ttu-id="698b0-110">MS-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="698b0-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="698b0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="698b0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="698b0-112">Мспки-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="698b0-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="698b0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="698b0-113">Size</span></span>              | <span data-ttu-id="698b0-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="698b0-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="698b0-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="698b0-115">Update Privilege</span></span>  | <span data-ttu-id="698b0-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="698b0-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="698b0-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="698b0-117">Update Frequency</span></span>  | <span data-ttu-id="698b0-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="698b0-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="698b0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="698b0-119">Attribute-Id</span></span>      | <span data-ttu-id="698b0-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="698b0-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="698b0-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="698b0-121">System-Id-Guid</span></span>    | <span data-ttu-id="698b0-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="698b0-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="698b0-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="698b0-123">Syntax</span></span>            | [<span data-ttu-id="698b0-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="698b0-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="698b0-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="698b0-125">Implementations</span></span>

-   [<span data-ttu-id="698b0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="698b0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="698b0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="698b0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="698b0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="698b0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="698b0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="698b0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="698b0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="698b0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="698b0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="698b0-131">Windows Server 2003</span></span>



| <span data-ttu-id="698b0-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="698b0-132">Entry</span></span> | <span data-ttu-id="698b0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="698b0-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="698b0-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="698b0-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="698b0-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="698b0-136">System-Only</span></span>            | <span data-ttu-id="698b0-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-137">False</span></span>                                                                   |
| <span data-ttu-id="698b0-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="698b0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="698b0-139">True</span><span class="sxs-lookup"><span data-stu-id="698b0-139">True</span></span>                                                                    |
| <span data-ttu-id="698b0-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="698b0-140">Is Indexed</span></span>             | <span data-ttu-id="698b0-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-141">False</span></span>                                                                   |
| <span data-ttu-id="698b0-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="698b0-142">In Global Catalog</span></span>      | <span data-ttu-id="698b0-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-143">False</span></span>                                                                   |
| <span data-ttu-id="698b0-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="698b0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="698b0-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="698b0-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="698b0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="698b0-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="698b0-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-148">Search-Flags</span></span>           | <span data-ttu-id="698b0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="698b0-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="698b0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-150">System-Flags</span></span>           | <span data-ttu-id="698b0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="698b0-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="698b0-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="698b0-152">Classes used in</span></span>        | [<span data-ttu-id="698b0-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="698b0-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="698b0-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="698b0-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="698b0-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="698b0-155">Entry</span></span> | <span data-ttu-id="698b0-156">Значение</span><span class="sxs-lookup"><span data-stu-id="698b0-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="698b0-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="698b0-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="698b0-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="698b0-159">System-Only</span></span>            | <span data-ttu-id="698b0-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-160">False</span></span>                                                                   |
| <span data-ttu-id="698b0-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="698b0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="698b0-162">True</span><span class="sxs-lookup"><span data-stu-id="698b0-162">True</span></span>                                                                    |
| <span data-ttu-id="698b0-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="698b0-163">Is Indexed</span></span>             | <span data-ttu-id="698b0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-164">False</span></span>                                                                   |
| <span data-ttu-id="698b0-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="698b0-165">In Global Catalog</span></span>      | <span data-ttu-id="698b0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-166">False</span></span>                                                                   |
| <span data-ttu-id="698b0-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="698b0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="698b0-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="698b0-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="698b0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="698b0-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="698b0-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-171">Search-Flags</span></span>           | <span data-ttu-id="698b0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="698b0-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="698b0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-173">System-Flags</span></span>           | <span data-ttu-id="698b0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="698b0-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="698b0-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="698b0-175">Classes used in</span></span>        | [<span data-ttu-id="698b0-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="698b0-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="698b0-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="698b0-177">Windows Server 2008</span></span>



| <span data-ttu-id="698b0-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="698b0-178">Entry</span></span> | <span data-ttu-id="698b0-179">Значение</span><span class="sxs-lookup"><span data-stu-id="698b0-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="698b0-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="698b0-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="698b0-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="698b0-182">System-Only</span></span>            | <span data-ttu-id="698b0-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-183">False</span></span>                                                                   |
| <span data-ttu-id="698b0-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="698b0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="698b0-185">True</span><span class="sxs-lookup"><span data-stu-id="698b0-185">True</span></span>                                                                    |
| <span data-ttu-id="698b0-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="698b0-186">Is Indexed</span></span>             | <span data-ttu-id="698b0-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-187">False</span></span>                                                                   |
| <span data-ttu-id="698b0-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="698b0-188">In Global Catalog</span></span>      | <span data-ttu-id="698b0-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-189">False</span></span>                                                                   |
| <span data-ttu-id="698b0-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="698b0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="698b0-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="698b0-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="698b0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="698b0-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="698b0-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-194">Search-Flags</span></span>           | <span data-ttu-id="698b0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="698b0-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="698b0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-196">System-Flags</span></span>           | <span data-ttu-id="698b0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="698b0-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="698b0-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="698b0-198">Classes used in</span></span>        | [<span data-ttu-id="698b0-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="698b0-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="698b0-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="698b0-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="698b0-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="698b0-201">Entry</span></span> | <span data-ttu-id="698b0-202">Значение</span><span class="sxs-lookup"><span data-stu-id="698b0-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="698b0-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="698b0-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="698b0-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="698b0-205">System-Only</span></span>            | <span data-ttu-id="698b0-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-206">False</span></span>                                                                   |
| <span data-ttu-id="698b0-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="698b0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="698b0-208">True</span><span class="sxs-lookup"><span data-stu-id="698b0-208">True</span></span>                                                                    |
| <span data-ttu-id="698b0-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="698b0-209">Is Indexed</span></span>             | <span data-ttu-id="698b0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-210">False</span></span>                                                                   |
| <span data-ttu-id="698b0-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="698b0-211">In Global Catalog</span></span>      | <span data-ttu-id="698b0-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-212">False</span></span>                                                                   |
| <span data-ttu-id="698b0-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="698b0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="698b0-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="698b0-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="698b0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="698b0-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="698b0-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-217">Search-Flags</span></span>           | <span data-ttu-id="698b0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="698b0-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="698b0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-219">System-Flags</span></span>           | <span data-ttu-id="698b0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="698b0-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="698b0-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="698b0-221">Classes used in</span></span>        | [<span data-ttu-id="698b0-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="698b0-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="698b0-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="698b0-223">Windows Server 2012</span></span>



| <span data-ttu-id="698b0-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="698b0-224">Entry</span></span> | <span data-ttu-id="698b0-225">Значение</span><span class="sxs-lookup"><span data-stu-id="698b0-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="698b0-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="698b0-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="698b0-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="698b0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="698b0-228">System-Only</span></span>            | <span data-ttu-id="698b0-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-229">False</span></span>                                                                   |
| <span data-ttu-id="698b0-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="698b0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="698b0-231">True</span><span class="sxs-lookup"><span data-stu-id="698b0-231">True</span></span>                                                                    |
| <span data-ttu-id="698b0-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="698b0-232">Is Indexed</span></span>             | <span data-ttu-id="698b0-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-233">False</span></span>                                                                   |
| <span data-ttu-id="698b0-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="698b0-234">In Global Catalog</span></span>      | <span data-ttu-id="698b0-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="698b0-235">False</span></span>                                                                   |
| <span data-ttu-id="698b0-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="698b0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="698b0-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="698b0-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="698b0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="698b0-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="698b0-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="698b0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-240">Search-Flags</span></span>           | <span data-ttu-id="698b0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="698b0-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="698b0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="698b0-242">System-Flags</span></span>           | <span data-ttu-id="698b0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="698b0-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="698b0-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="698b0-244">Classes used in</span></span>        | [<span data-ttu-id="698b0-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="698b0-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





