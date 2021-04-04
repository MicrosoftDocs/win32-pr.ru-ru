---
title: атрибут MS-PKI-регистрация-флаг
description: Содержит флаги, связанные с регистрацией.
ms.assetid: e854acb1-75f4-4379-b404-8fa096419ee6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута-флага регистрации MS-PKI
- Мспки — схема AD атрибута-флага регистрации
topic_type:
- apiref
api_name:
- ms-PKI-Enrollment-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df092e28633bd5825c422e306bf7a65982b32a8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989675"
---
# <a name="ms-pki-enrollment-flag-attribute"></a><span data-ttu-id="ed6ca-105">атрибут MS-PKI-регистрация-флаг</span><span class="sxs-lookup"><span data-stu-id="ed6ca-105">ms-PKI-Enrollment-Flag attribute</span></span>

<span data-ttu-id="ed6ca-106">Содержит флаги, связанные с регистрацией.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-106">Contains the enrollment related flags.</span></span>



| <span data-ttu-id="ed6ca-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed6ca-107">Entry</span></span> | <span data-ttu-id="ed6ca-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ed6ca-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed6ca-109">CN</span><span class="sxs-lookup"><span data-stu-id="ed6ca-109">CN</span></span>                | <span data-ttu-id="ed6ca-110">Флаг MS-PKI-регистрации</span><span class="sxs-lookup"><span data-stu-id="ed6ca-110">ms-PKI-Enrollment-Flag</span></span>                                                                            |
| <span data-ttu-id="ed6ca-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ed6ca-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ed6ca-112">Мспки-флаг регистрации</span><span class="sxs-lookup"><span data-stu-id="ed6ca-112">msPKI-Enrollment-Flag</span></span>                                                                             |
| <span data-ttu-id="ed6ca-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ed6ca-113">Size</span></span>              | <span data-ttu-id="ed6ca-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="ed6ca-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="ed6ca-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ed6ca-115">Update Privilege</span></span>  | <span data-ttu-id="ed6ca-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="ed6ca-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="ed6ca-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ed6ca-117">Update Frequency</span></span>  | <span data-ttu-id="ed6ca-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="ed6ca-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="ed6ca-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed6ca-119">Attribute-Id</span></span>      | <span data-ttu-id="ed6ca-120">1.2.840.113556.1.4.1430</span><span class="sxs-lookup"><span data-stu-id="ed6ca-120">1.2.840.113556.1.4.1430</span></span>                                                                           |
| <span data-ttu-id="ed6ca-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ed6ca-121">System-Id-Guid</span></span>    | <span data-ttu-id="ed6ca-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span><span class="sxs-lookup"><span data-stu-id="ed6ca-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span></span>                                                              |
| <span data-ttu-id="ed6ca-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed6ca-123">Syntax</span></span>            | [<span data-ttu-id="ed6ca-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="ed6ca-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ed6ca-125">Implementations</span></span>

-   [<span data-ttu-id="ed6ca-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ed6ca-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ed6ca-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ed6ca-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ed6ca-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ed6ca-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed6ca-131">Windows Server 2003</span></span>



| <span data-ttu-id="ed6ca-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed6ca-132">Entry</span></span> | <span data-ttu-id="ed6ca-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ed6ca-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ed6ca-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ed6ca-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed6ca-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed6ca-136">System-Only</span></span>            | <span data-ttu-id="ed6ca-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-137">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ed6ca-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ed6ca-139">True</span><span class="sxs-lookup"><span data-stu-id="ed6ca-139">True</span></span>                                                                    |
| <span data-ttu-id="ed6ca-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ed6ca-140">Is Indexed</span></span>             | <span data-ttu-id="ed6ca-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-141">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ed6ca-142">In Global Catalog</span></span>      | <span data-ttu-id="ed6ca-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-143">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ed6ca-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed6ca-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ed6ca-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed6ca-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed6ca-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-148">Search-Flags</span></span>           | <span data-ttu-id="ed6ca-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed6ca-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="ed6ca-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-150">System-Flags</span></span>           | <span data-ttu-id="ed6ca-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed6ca-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="ed6ca-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ed6ca-152">Classes used in</span></span>        | [<span data-ttu-id="ed6ca-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ed6ca-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ed6ca-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ed6ca-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed6ca-155">Entry</span></span> | <span data-ttu-id="ed6ca-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ed6ca-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ed6ca-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ed6ca-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed6ca-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed6ca-159">System-Only</span></span>            | <span data-ttu-id="ed6ca-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-160">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ed6ca-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ed6ca-162">True</span><span class="sxs-lookup"><span data-stu-id="ed6ca-162">True</span></span>                                                                    |
| <span data-ttu-id="ed6ca-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ed6ca-163">Is Indexed</span></span>             | <span data-ttu-id="ed6ca-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-164">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ed6ca-165">In Global Catalog</span></span>      | <span data-ttu-id="ed6ca-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-166">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ed6ca-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed6ca-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ed6ca-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed6ca-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed6ca-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-171">Search-Flags</span></span>           | <span data-ttu-id="ed6ca-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed6ca-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="ed6ca-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-173">System-Flags</span></span>           | <span data-ttu-id="ed6ca-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed6ca-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="ed6ca-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ed6ca-175">Classes used in</span></span>        | [<span data-ttu-id="ed6ca-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ed6ca-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed6ca-177">Windows Server 2008</span></span>



| <span data-ttu-id="ed6ca-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed6ca-178">Entry</span></span> | <span data-ttu-id="ed6ca-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ed6ca-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ed6ca-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ed6ca-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed6ca-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed6ca-182">System-Only</span></span>            | <span data-ttu-id="ed6ca-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-183">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ed6ca-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ed6ca-185">True</span><span class="sxs-lookup"><span data-stu-id="ed6ca-185">True</span></span>                                                                    |
| <span data-ttu-id="ed6ca-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ed6ca-186">Is Indexed</span></span>             | <span data-ttu-id="ed6ca-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-187">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ed6ca-188">In Global Catalog</span></span>      | <span data-ttu-id="ed6ca-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-189">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ed6ca-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed6ca-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ed6ca-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed6ca-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed6ca-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-194">Search-Flags</span></span>           | <span data-ttu-id="ed6ca-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed6ca-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="ed6ca-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-196">System-Flags</span></span>           | <span data-ttu-id="ed6ca-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed6ca-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="ed6ca-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ed6ca-198">Classes used in</span></span>        | [<span data-ttu-id="ed6ca-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ed6ca-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed6ca-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ed6ca-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed6ca-201">Entry</span></span> | <span data-ttu-id="ed6ca-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ed6ca-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ed6ca-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ed6ca-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed6ca-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed6ca-205">System-Only</span></span>            | <span data-ttu-id="ed6ca-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-206">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ed6ca-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ed6ca-208">True</span><span class="sxs-lookup"><span data-stu-id="ed6ca-208">True</span></span>                                                                    |
| <span data-ttu-id="ed6ca-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ed6ca-209">Is Indexed</span></span>             | <span data-ttu-id="ed6ca-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-210">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ed6ca-211">In Global Catalog</span></span>      | <span data-ttu-id="ed6ca-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-212">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ed6ca-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed6ca-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ed6ca-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed6ca-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed6ca-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-217">Search-Flags</span></span>           | <span data-ttu-id="ed6ca-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed6ca-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="ed6ca-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-219">System-Flags</span></span>           | <span data-ttu-id="ed6ca-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed6ca-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="ed6ca-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ed6ca-221">Classes used in</span></span>        | [<span data-ttu-id="ed6ca-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ed6ca-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed6ca-223">Windows Server 2012</span></span>



| <span data-ttu-id="ed6ca-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed6ca-224">Entry</span></span> | <span data-ttu-id="ed6ca-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ed6ca-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ed6ca-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ed6ca-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed6ca-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ed6ca-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed6ca-228">System-Only</span></span>            | <span data-ttu-id="ed6ca-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-229">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ed6ca-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ed6ca-231">True</span><span class="sxs-lookup"><span data-stu-id="ed6ca-231">True</span></span>                                                                    |
| <span data-ttu-id="ed6ca-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ed6ca-232">Is Indexed</span></span>             | <span data-ttu-id="ed6ca-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-233">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ed6ca-234">In Global Catalog</span></span>      | <span data-ttu-id="ed6ca-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed6ca-235">False</span></span>                                                                   |
| <span data-ttu-id="ed6ca-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ed6ca-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed6ca-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ed6ca-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed6ca-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed6ca-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ed6ca-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-240">Search-Flags</span></span>           | <span data-ttu-id="ed6ca-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed6ca-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="ed6ca-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed6ca-242">System-Flags</span></span>           | <span data-ttu-id="ed6ca-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed6ca-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="ed6ca-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ed6ca-244">Classes used in</span></span>        | [<span data-ttu-id="ed6ca-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





