---
title: атрибут MS-PKI-CERT-Template-OID
description: Указывает идентификатор объекта для шаблона сертификата.
ms.assetid: b239c1cb-35d9-4a98-9591-ea405a1101cd
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута OID MS-PKI-CERT-Template
- Мспки-CERT-Template — схема AD атрибута OID
topic_type:
- apiref
api_name:
- ms-PKI-Cert-Template-OID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadf0c2573dbdeac328a6de55fa8de69781bc28c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655384"
---
# <a name="ms-pki-cert-template-oid-attribute"></a><span data-ttu-id="5d033-105">атрибут MS-PKI-CERT-Template-OID</span><span class="sxs-lookup"><span data-stu-id="5d033-105">ms-PKI-Cert-Template-OID attribute</span></span>

<span data-ttu-id="5d033-106">Указывает идентификатор объекта для шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="5d033-106">Specifies the object identifier for a certificate template.</span></span>



| <span data-ttu-id="5d033-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d033-107">Entry</span></span> | <span data-ttu-id="5d033-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5d033-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-109">CN</span><span class="sxs-lookup"><span data-stu-id="5d033-109">CN</span></span>                | <span data-ttu-id="5d033-110">MS-PKI-CERT-Template-OID</span><span class="sxs-lookup"><span data-stu-id="5d033-110">ms-PKI-Cert-Template-OID</span></span>                                                                          |
| <span data-ttu-id="5d033-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5d033-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5d033-112">Мспки-CERT-Template-OID</span><span class="sxs-lookup"><span data-stu-id="5d033-112">msPKI-Cert-Template-OID</span></span>                                                                           |
| <span data-ttu-id="5d033-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5d033-113">Size</span></span>              | <span data-ttu-id="5d033-114">64 байт</span><span class="sxs-lookup"><span data-stu-id="5d033-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="5d033-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5d033-115">Update Privilege</span></span>  | <span data-ttu-id="5d033-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="5d033-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="5d033-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5d033-117">Update Frequency</span></span>  | <span data-ttu-id="5d033-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="5d033-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="5d033-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d033-119">Attribute-Id</span></span>      | <span data-ttu-id="5d033-120">1.2.840.113556.1.4.1436</span><span class="sxs-lookup"><span data-stu-id="5d033-120">1.2.840.113556.1.4.1436</span></span>                                                                           |
| <span data-ttu-id="5d033-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5d033-121">System-Id-Guid</span></span>    | <span data-ttu-id="5d033-122">3164c36a-ba26-468c-8bda-c1e5cc256728</span><span class="sxs-lookup"><span data-stu-id="5d033-122">3164c36a-ba26-468c-8bda-c1e5cc256728</span></span>                                                              |
| <span data-ttu-id="5d033-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d033-123">Syntax</span></span>            | [<span data-ttu-id="5d033-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="5d033-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="5d033-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5d033-125">Implementations</span></span>

-   [<span data-ttu-id="5d033-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d033-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d033-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d033-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d033-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d033-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d033-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d033-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d033-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d033-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5d033-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d033-131">Windows Server 2003</span></span>



| <span data-ttu-id="5d033-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d033-132">Entry</span></span> | <span data-ttu-id="5d033-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5d033-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d033-134">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d033-135">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d033-136">System-Only</span></span>            | <span data-ttu-id="5d033-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-137">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d033-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5d033-139">True</span><span class="sxs-lookup"><span data-stu-id="5d033-139">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d033-140">Is Indexed</span></span>             | <span data-ttu-id="5d033-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-141">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d033-142">In Global Catalog</span></span>      | <span data-ttu-id="5d033-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-143">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d033-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d033-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d033-145">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="5d033-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d033-146">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d033-147">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-148">Search-Flags</span></span>           | <span data-ttu-id="5d033-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d033-149">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-150">System-Flags</span></span>           | <span data-ttu-id="5d033-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d033-151">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d033-152">Classes used in</span></span>        | [<span data-ttu-id="5d033-153">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="5d033-153">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> [<span data-ttu-id="5d033-154">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="5d033-154">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d033-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d033-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d033-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d033-156">Entry</span></span> | <span data-ttu-id="5d033-157">Значение</span><span class="sxs-lookup"><span data-stu-id="5d033-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d033-158">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d033-159">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d033-160">System-Only</span></span>            | <span data-ttu-id="5d033-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d033-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5d033-163">True</span><span class="sxs-lookup"><span data-stu-id="5d033-163">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d033-164">Is Indexed</span></span>             | <span data-ttu-id="5d033-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d033-166">In Global Catalog</span></span>      | <span data-ttu-id="5d033-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d033-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d033-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d033-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="5d033-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d033-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d033-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-172">Search-Flags</span></span>           | <span data-ttu-id="5d033-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d033-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-174">System-Flags</span></span>           | <span data-ttu-id="5d033-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d033-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d033-176">Classes used in</span></span>        | [<span data-ttu-id="5d033-177">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="5d033-177">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> [<span data-ttu-id="5d033-178">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="5d033-178">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d033-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d033-179">Windows Server 2008</span></span>



| <span data-ttu-id="5d033-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d033-180">Entry</span></span> | <span data-ttu-id="5d033-181">Значение</span><span class="sxs-lookup"><span data-stu-id="5d033-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d033-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d033-183">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d033-184">System-Only</span></span>            | <span data-ttu-id="5d033-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-185">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d033-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5d033-187">True</span><span class="sxs-lookup"><span data-stu-id="5d033-187">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d033-188">Is Indexed</span></span>             | <span data-ttu-id="5d033-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-189">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d033-190">In Global Catalog</span></span>      | <span data-ttu-id="5d033-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-191">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d033-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d033-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d033-193">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="5d033-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d033-194">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d033-195">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-196">Search-Flags</span></span>           | <span data-ttu-id="5d033-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d033-197">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-198">System-Flags</span></span>           | <span data-ttu-id="5d033-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d033-199">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d033-200">Classes used in</span></span>        | [<span data-ttu-id="5d033-201">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="5d033-201">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> [<span data-ttu-id="5d033-202">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="5d033-202">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d033-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d033-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d033-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d033-204">Entry</span></span> | <span data-ttu-id="5d033-205">Значение</span><span class="sxs-lookup"><span data-stu-id="5d033-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d033-206">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d033-207">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d033-208">System-Only</span></span>            | <span data-ttu-id="5d033-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-209">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d033-210">Is-Single-Valued</span></span>       | <span data-ttu-id="5d033-211">True</span><span class="sxs-lookup"><span data-stu-id="5d033-211">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d033-212">Is Indexed</span></span>             | <span data-ttu-id="5d033-213">True</span><span class="sxs-lookup"><span data-stu-id="5d033-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d033-214">In Global Catalog</span></span>      | <span data-ttu-id="5d033-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d033-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d033-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d033-217">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="5d033-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d033-218">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d033-219">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-220">Search-Flags</span></span>           | <span data-ttu-id="5d033-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5d033-221">0x00000001</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-222">System-Flags</span></span>           | <span data-ttu-id="5d033-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d033-223">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d033-224">Classes used in</span></span>        | [<span data-ttu-id="5d033-225">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="5d033-225">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> [<span data-ttu-id="5d033-226">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="5d033-226">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d033-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d033-227">Windows Server 2012</span></span>



| <span data-ttu-id="5d033-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="5d033-228">Entry</span></span> | <span data-ttu-id="5d033-229">Значение</span><span class="sxs-lookup"><span data-stu-id="5d033-229">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5d033-230">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d033-231">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="5d033-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d033-232">System-Only</span></span>            | <span data-ttu-id="5d033-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-233">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5d033-234">Is-Single-Valued</span></span>       | <span data-ttu-id="5d033-235">True</span><span class="sxs-lookup"><span data-stu-id="5d033-235">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5d033-236">Is Indexed</span></span>             | <span data-ttu-id="5d033-237">True</span><span class="sxs-lookup"><span data-stu-id="5d033-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="5d033-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5d033-238">In Global Catalog</span></span>      | <span data-ttu-id="5d033-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d033-239">False</span></span>                                                                                                                                      |
| <span data-ttu-id="5d033-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5d033-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d033-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d033-241">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="5d033-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d033-242">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d033-243">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="5d033-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-244">Search-Flags</span></span>           | <span data-ttu-id="5d033-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5d033-245">0x00000001</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d033-246">System-Flags</span></span>           | <span data-ttu-id="5d033-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d033-247">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="5d033-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5d033-248">Classes used in</span></span>        | [<span data-ttu-id="5d033-249">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="5d033-249">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> [<span data-ttu-id="5d033-250">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="5d033-250">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





