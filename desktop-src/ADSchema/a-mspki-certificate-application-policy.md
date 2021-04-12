---
title: MS-PKI-Certificate-приложение-атрибут политики
description: OID политики приложения в сертификате.
ms.assetid: 91e98ec9-0e8d-4950-a62c-9b6901ec4d97
ms.tgt_platform: multiple
keywords:
- Active-PKI-Certificate — схема AD атрибута политики приложения
- Мспки-Certificate — схема AD атрибута политики приложения
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Application-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9436415fb9361454fc5f872802516fa455ff980b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416261"
---
# <a name="ms-pki-certificate-application-policy-attribute"></a><span data-ttu-id="e07ff-105">MS-PKI-Certificate-приложение-атрибут политики</span><span class="sxs-lookup"><span data-stu-id="e07ff-105">ms-PKI-Certificate-Application-Policy attribute</span></span>

<span data-ttu-id="e07ff-106">OID политики приложения в сертификате.</span><span class="sxs-lookup"><span data-stu-id="e07ff-106">The application policy OID's in a certificate.</span></span>



| <span data-ttu-id="e07ff-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e07ff-107">Entry</span></span> | <span data-ttu-id="e07ff-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ff-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07ff-109">CN</span><span class="sxs-lookup"><span data-stu-id="e07ff-109">CN</span></span>                | <span data-ttu-id="e07ff-110">MS-PKI-Certificate-приложение-политика</span><span class="sxs-lookup"><span data-stu-id="e07ff-110">ms-PKI-Certificate-Application-Policy</span></span>                                                      |
| <span data-ttu-id="e07ff-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e07ff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e07ff-112">Мспки-Certificate-приложение-политика</span><span class="sxs-lookup"><span data-stu-id="e07ff-112">msPKI-Certificate-Application-Policy</span></span>                                                       |
| <span data-ttu-id="e07ff-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e07ff-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="e07ff-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e07ff-114">Update Privilege</span></span>  | <span data-ttu-id="e07ff-115">Администратор предприятия</span><span class="sxs-lookup"><span data-stu-id="e07ff-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="e07ff-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e07ff-116">Update Frequency</span></span>  | <span data-ttu-id="e07ff-117">При создании нового шаблона или изменении атрибутов существующих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="e07ff-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="e07ff-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e07ff-118">Attribute-Id</span></span>      | <span data-ttu-id="e07ff-119">1.2.840.113556.1.4.1674</span><span class="sxs-lookup"><span data-stu-id="e07ff-119">1.2.840.113556.1.4.1674</span></span>                                                                    |
| <span data-ttu-id="e07ff-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e07ff-120">System-Id-Guid</span></span>    | <span data-ttu-id="e07ff-121">dbd90548-aa37-4202-9966-8c537ba5ce32</span><span class="sxs-lookup"><span data-stu-id="e07ff-121">dbd90548-aa37-4202-9966-8c537ba5ce32</span></span>                                                       |
| <span data-ttu-id="e07ff-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e07ff-122">Syntax</span></span>            | [<span data-ttu-id="e07ff-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e07ff-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="e07ff-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e07ff-124">Implementations</span></span>

-   [<span data-ttu-id="e07ff-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e07ff-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e07ff-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e07ff-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e07ff-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e07ff-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e07ff-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e07ff-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e07ff-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e07ff-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e07ff-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e07ff-130">Windows Server 2003</span></span>



| <span data-ttu-id="e07ff-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e07ff-131">Entry</span></span> | <span data-ttu-id="e07ff-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ff-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e07ff-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e07ff-133">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07ff-134">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07ff-135">System-Only</span></span>            | <span data-ttu-id="e07ff-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-136">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e07ff-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e07ff-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-138">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e07ff-139">Is Indexed</span></span>             | <span data-ttu-id="e07ff-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-140">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e07ff-141">In Global Catalog</span></span>      | <span data-ttu-id="e07ff-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-142">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e07ff-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07ff-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e07ff-144">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e07ff-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07ff-145">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07ff-146">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-147">Search-Flags</span></span>           | <span data-ttu-id="e07ff-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e07ff-148">0x00000000</span></span>                                                              |
| <span data-ttu-id="e07ff-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-149">System-Flags</span></span>           | <span data-ttu-id="e07ff-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07ff-150">0x00000010</span></span>                                                              |
| <span data-ttu-id="e07ff-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e07ff-151">Classes used in</span></span>        | [<span data-ttu-id="e07ff-152">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="e07ff-152">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e07ff-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e07ff-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e07ff-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e07ff-154">Entry</span></span> | <span data-ttu-id="e07ff-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ff-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e07ff-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e07ff-156">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07ff-157">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07ff-158">System-Only</span></span>            | <span data-ttu-id="e07ff-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-159">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e07ff-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e07ff-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-161">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e07ff-162">Is Indexed</span></span>             | <span data-ttu-id="e07ff-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-163">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e07ff-164">In Global Catalog</span></span>      | <span data-ttu-id="e07ff-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-165">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e07ff-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07ff-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e07ff-167">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e07ff-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07ff-168">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07ff-169">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-170">Search-Flags</span></span>           | <span data-ttu-id="e07ff-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e07ff-171">0x00000000</span></span>                                                              |
| <span data-ttu-id="e07ff-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-172">System-Flags</span></span>           | <span data-ttu-id="e07ff-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07ff-173">0x00000010</span></span>                                                              |
| <span data-ttu-id="e07ff-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e07ff-174">Classes used in</span></span>        | [<span data-ttu-id="e07ff-175">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="e07ff-175">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e07ff-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e07ff-176">Windows Server 2008</span></span>



| <span data-ttu-id="e07ff-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="e07ff-177">Entry</span></span> | <span data-ttu-id="e07ff-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ff-178">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e07ff-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e07ff-179">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07ff-180">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07ff-181">System-Only</span></span>            | <span data-ttu-id="e07ff-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-182">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e07ff-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e07ff-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-184">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e07ff-185">Is Indexed</span></span>             | <span data-ttu-id="e07ff-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-186">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e07ff-187">In Global Catalog</span></span>      | <span data-ttu-id="e07ff-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-188">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e07ff-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07ff-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e07ff-190">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e07ff-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07ff-191">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07ff-192">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-193">Search-Flags</span></span>           | <span data-ttu-id="e07ff-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e07ff-194">0x00000000</span></span>                                                              |
| <span data-ttu-id="e07ff-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-195">System-Flags</span></span>           | <span data-ttu-id="e07ff-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07ff-196">0x00000010</span></span>                                                              |
| <span data-ttu-id="e07ff-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e07ff-197">Classes used in</span></span>        | [<span data-ttu-id="e07ff-198">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="e07ff-198">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e07ff-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e07ff-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e07ff-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e07ff-200">Entry</span></span> | <span data-ttu-id="e07ff-201">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ff-201">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e07ff-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e07ff-202">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07ff-203">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07ff-204">System-Only</span></span>            | <span data-ttu-id="e07ff-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-205">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e07ff-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e07ff-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-207">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e07ff-208">Is Indexed</span></span>             | <span data-ttu-id="e07ff-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-209">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e07ff-210">In Global Catalog</span></span>      | <span data-ttu-id="e07ff-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-211">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e07ff-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07ff-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e07ff-213">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e07ff-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07ff-214">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07ff-215">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-216">Search-Flags</span></span>           | <span data-ttu-id="e07ff-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e07ff-217">0x00000000</span></span>                                                              |
| <span data-ttu-id="e07ff-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-218">System-Flags</span></span>           | <span data-ttu-id="e07ff-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07ff-219">0x00000010</span></span>                                                              |
| <span data-ttu-id="e07ff-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e07ff-220">Classes used in</span></span>        | [<span data-ttu-id="e07ff-221">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="e07ff-221">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e07ff-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e07ff-222">Windows Server 2012</span></span>



| <span data-ttu-id="e07ff-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="e07ff-223">Entry</span></span> | <span data-ttu-id="e07ff-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ff-224">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e07ff-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e07ff-225">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07ff-226">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e07ff-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07ff-227">System-Only</span></span>            | <span data-ttu-id="e07ff-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-228">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e07ff-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e07ff-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-230">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e07ff-231">Is Indexed</span></span>             | <span data-ttu-id="e07ff-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-232">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e07ff-233">In Global Catalog</span></span>      | <span data-ttu-id="e07ff-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e07ff-234">False</span></span>                                                                   |
| <span data-ttu-id="e07ff-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e07ff-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07ff-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e07ff-236">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e07ff-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07ff-237">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07ff-238">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e07ff-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-239">Search-Flags</span></span>           | <span data-ttu-id="e07ff-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e07ff-240">0x00000000</span></span>                                                              |
| <span data-ttu-id="e07ff-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07ff-241">System-Flags</span></span>           | <span data-ttu-id="e07ff-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07ff-242">0x00000010</span></span>                                                              |
| <span data-ttu-id="e07ff-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e07ff-243">Classes used in</span></span>        | [<span data-ttu-id="e07ff-244">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="e07ff-244">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





