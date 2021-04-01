---
title: атрибут MS-PKI-RA-Application-Policies
description: Требуемый OID политики приложения RA в сигнатурах счетчика запроса на сертификат.
ms.assetid: 1ce61107-01aa-4a03-8a00-21890fb610d7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-PKI-RA-Application-Policies
- Схема AD атрибута Мспки-RA-Application-Policies
topic_type:
- apiref
api_name:
- ms-PKI-RA-Application-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01aab7c8da5c6267efe954cac71dc8c9c98c18f4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262244"
---
# <a name="ms-pki-ra-application-policies-attribute"></a><span data-ttu-id="17ea1-105">атрибут MS-PKI-RA-Application-Policies</span><span class="sxs-lookup"><span data-stu-id="17ea1-105">ms-PKI-RA-Application-Policies attribute</span></span>

<span data-ttu-id="17ea1-106">Требуемый OID политики приложения RA в сигнатурах счетчика запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="17ea1-106">The required RA application policy OID in the counter signatures of the certificate request.</span></span>



| <span data-ttu-id="17ea1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="17ea1-107">Entry</span></span> | <span data-ttu-id="17ea1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="17ea1-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ea1-109">CN</span><span class="sxs-lookup"><span data-stu-id="17ea1-109">CN</span></span>                | <span data-ttu-id="17ea1-110">MS-PKI-RA-приложения — политики</span><span class="sxs-lookup"><span data-stu-id="17ea1-110">ms-PKI-RA-Application-Policies</span></span>                                                             |
| <span data-ttu-id="17ea1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="17ea1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="17ea1-112">Мспки-RA-приложение-политики</span><span class="sxs-lookup"><span data-stu-id="17ea1-112">msPKI-RA-Application-Policies</span></span>                                                              |
| <span data-ttu-id="17ea1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="17ea1-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="17ea1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="17ea1-114">Update Privilege</span></span>  | <span data-ttu-id="17ea1-115">Администратор предприятия</span><span class="sxs-lookup"><span data-stu-id="17ea1-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="17ea1-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="17ea1-116">Update Frequency</span></span>  | <span data-ttu-id="17ea1-117">При создании нового шаблона или изменении атрибутов существующих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="17ea1-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="17ea1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17ea1-118">Attribute-Id</span></span>      | <span data-ttu-id="17ea1-119">1.2.840.113556.1.4.1675</span><span class="sxs-lookup"><span data-stu-id="17ea1-119">1.2.840.113556.1.4.1675</span></span>                                                                    |
| <span data-ttu-id="17ea1-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="17ea1-120">System-Id-Guid</span></span>    | <span data-ttu-id="17ea1-121">3c91fbbf-4773-4ccd-a87b-85d53e7bcf6a</span><span class="sxs-lookup"><span data-stu-id="17ea1-121">3c91fbbf-4773-4ccd-a87b-85d53e7bcf6a</span></span>                                                       |
| <span data-ttu-id="17ea1-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17ea1-122">Syntax</span></span>            | [<span data-ttu-id="17ea1-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="17ea1-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="17ea1-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="17ea1-124">Implementations</span></span>

-   [<span data-ttu-id="17ea1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17ea1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17ea1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17ea1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17ea1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17ea1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17ea1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17ea1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17ea1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17ea1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="17ea1-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17ea1-130">Windows Server 2003</span></span>



| <span data-ttu-id="17ea1-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="17ea1-131">Entry</span></span> | <span data-ttu-id="17ea1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="17ea1-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="17ea1-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17ea1-133">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17ea1-134">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="17ea1-135">System-Only</span></span>            | <span data-ttu-id="17ea1-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-136">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17ea1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="17ea1-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-138">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17ea1-139">Is Indexed</span></span>             | <span data-ttu-id="17ea1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-140">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17ea1-141">In Global Catalog</span></span>      | <span data-ttu-id="17ea1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-142">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17ea1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="17ea1-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17ea1-144">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="17ea1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17ea1-145">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17ea1-146">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-147">Search-Flags</span></span>           | <span data-ttu-id="17ea1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17ea1-148">0x00000000</span></span>                                                              |
| <span data-ttu-id="17ea1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-149">System-Flags</span></span>           | <span data-ttu-id="17ea1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17ea1-150">0x00000010</span></span>                                                              |
| <span data-ttu-id="17ea1-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17ea1-151">Classes used in</span></span>        | [<span data-ttu-id="17ea1-152">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="17ea1-152">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17ea1-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17ea1-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17ea1-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="17ea1-154">Entry</span></span> | <span data-ttu-id="17ea1-155">Значение</span><span class="sxs-lookup"><span data-stu-id="17ea1-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="17ea1-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17ea1-156">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17ea1-157">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="17ea1-158">System-Only</span></span>            | <span data-ttu-id="17ea1-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-159">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17ea1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="17ea1-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-161">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17ea1-162">Is Indexed</span></span>             | <span data-ttu-id="17ea1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-163">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17ea1-164">In Global Catalog</span></span>      | <span data-ttu-id="17ea1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-165">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17ea1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="17ea1-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17ea1-167">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="17ea1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17ea1-168">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17ea1-169">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-170">Search-Flags</span></span>           | <span data-ttu-id="17ea1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17ea1-171">0x00000000</span></span>                                                              |
| <span data-ttu-id="17ea1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-172">System-Flags</span></span>           | <span data-ttu-id="17ea1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17ea1-173">0x00000010</span></span>                                                              |
| <span data-ttu-id="17ea1-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17ea1-174">Classes used in</span></span>        | [<span data-ttu-id="17ea1-175">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="17ea1-175">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17ea1-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17ea1-176">Windows Server 2008</span></span>



| <span data-ttu-id="17ea1-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="17ea1-177">Entry</span></span> | <span data-ttu-id="17ea1-178">Значение</span><span class="sxs-lookup"><span data-stu-id="17ea1-178">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="17ea1-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17ea1-179">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17ea1-180">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="17ea1-181">System-Only</span></span>            | <span data-ttu-id="17ea1-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-182">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17ea1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="17ea1-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-184">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17ea1-185">Is Indexed</span></span>             | <span data-ttu-id="17ea1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-186">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17ea1-187">In Global Catalog</span></span>      | <span data-ttu-id="17ea1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-188">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17ea1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="17ea1-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17ea1-190">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="17ea1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17ea1-191">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17ea1-192">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-193">Search-Flags</span></span>           | <span data-ttu-id="17ea1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17ea1-194">0x00000000</span></span>                                                              |
| <span data-ttu-id="17ea1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-195">System-Flags</span></span>           | <span data-ttu-id="17ea1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17ea1-196">0x00000010</span></span>                                                              |
| <span data-ttu-id="17ea1-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17ea1-197">Classes used in</span></span>        | [<span data-ttu-id="17ea1-198">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="17ea1-198">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17ea1-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17ea1-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17ea1-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="17ea1-200">Entry</span></span> | <span data-ttu-id="17ea1-201">Значение</span><span class="sxs-lookup"><span data-stu-id="17ea1-201">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="17ea1-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17ea1-202">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17ea1-203">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="17ea1-204">System-Only</span></span>            | <span data-ttu-id="17ea1-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-205">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17ea1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="17ea1-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-207">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17ea1-208">Is Indexed</span></span>             | <span data-ttu-id="17ea1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-209">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17ea1-210">In Global Catalog</span></span>      | <span data-ttu-id="17ea1-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-211">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17ea1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="17ea1-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17ea1-213">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="17ea1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17ea1-214">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17ea1-215">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-216">Search-Flags</span></span>           | <span data-ttu-id="17ea1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17ea1-217">0x00000000</span></span>                                                              |
| <span data-ttu-id="17ea1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-218">System-Flags</span></span>           | <span data-ttu-id="17ea1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17ea1-219">0x00000010</span></span>                                                              |
| <span data-ttu-id="17ea1-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17ea1-220">Classes used in</span></span>        | [<span data-ttu-id="17ea1-221">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="17ea1-221">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17ea1-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17ea1-222">Windows Server 2012</span></span>



| <span data-ttu-id="17ea1-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="17ea1-223">Entry</span></span> | <span data-ttu-id="17ea1-224">Значение</span><span class="sxs-lookup"><span data-stu-id="17ea1-224">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="17ea1-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17ea1-225">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17ea1-226">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="17ea1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="17ea1-227">System-Only</span></span>            | <span data-ttu-id="17ea1-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-228">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17ea1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="17ea1-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-230">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17ea1-231">Is Indexed</span></span>             | <span data-ttu-id="17ea1-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-232">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17ea1-233">In Global Catalog</span></span>      | <span data-ttu-id="17ea1-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="17ea1-234">False</span></span>                                                                   |
| <span data-ttu-id="17ea1-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17ea1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="17ea1-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17ea1-236">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="17ea1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17ea1-237">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17ea1-238">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="17ea1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-239">Search-Flags</span></span>           | <span data-ttu-id="17ea1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17ea1-240">0x00000000</span></span>                                                              |
| <span data-ttu-id="17ea1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17ea1-241">System-Flags</span></span>           | <span data-ttu-id="17ea1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17ea1-242">0x00000010</span></span>                                                              |
| <span data-ttu-id="17ea1-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17ea1-243">Classes used in</span></span>        | [<span data-ttu-id="17ea1-244">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="17ea1-244">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





