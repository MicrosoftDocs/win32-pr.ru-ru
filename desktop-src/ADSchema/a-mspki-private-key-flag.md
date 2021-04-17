---
title: атрибут MS-PKI-Private-Key-Flag
description: Содержит флаги, связанные с закрытым ключом.
ms.assetid: 5d5246b0-eca4-461e-956b-cdfa36576b14
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-PKI-Private-Key-Flag
- Схема AD атрибута Мспки-Private-Key-Flag
topic_type:
- apiref
api_name:
- ms-PKI-Private-Key-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc80873afcb65b323a5ea072520ef85535effb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536227"
---
# <a name="ms-pki-private-key-flag-attribute"></a><span data-ttu-id="d219c-105">атрибут MS-PKI-Private-Key-Flag</span><span class="sxs-lookup"><span data-stu-id="d219c-105">ms-PKI-Private-Key-Flag attribute</span></span>

<span data-ttu-id="d219c-106">Содержит флаги, связанные с закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="d219c-106">Contains the private key related flags.</span></span>



| <span data-ttu-id="d219c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d219c-107">Entry</span></span> | <span data-ttu-id="d219c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d219c-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d219c-109">CN</span><span class="sxs-lookup"><span data-stu-id="d219c-109">CN</span></span>                | <span data-ttu-id="d219c-110">MS-PKI-закрытый-Key-флаг</span><span class="sxs-lookup"><span data-stu-id="d219c-110">ms-PKI-Private-Key-Flag</span></span>                                                                           |
| <span data-ttu-id="d219c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d219c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d219c-112">Мспки-закрытый-ключ-флаг</span><span class="sxs-lookup"><span data-stu-id="d219c-112">msPKI-Private-Key-Flag</span></span>                                                                            |
| <span data-ttu-id="d219c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d219c-113">Size</span></span>              | <span data-ttu-id="d219c-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="d219c-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="d219c-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d219c-115">Update Privilege</span></span>  | <span data-ttu-id="d219c-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="d219c-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="d219c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d219c-117">Update Frequency</span></span>  | <span data-ttu-id="d219c-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="d219c-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="d219c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d219c-119">Attribute-Id</span></span>      | <span data-ttu-id="d219c-120">1.2.840.113556.1.4.1431</span><span class="sxs-lookup"><span data-stu-id="d219c-120">1.2.840.113556.1.4.1431</span></span>                                                                           |
| <span data-ttu-id="d219c-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d219c-121">System-Id-Guid</span></span>    | <span data-ttu-id="d219c-122">bab04ac2-0435-4709-9307-28380e7c7001</span><span class="sxs-lookup"><span data-stu-id="d219c-122">bab04ac2-0435-4709-9307-28380e7c7001</span></span>                                                              |
| <span data-ttu-id="d219c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d219c-123">Syntax</span></span>            | [<span data-ttu-id="d219c-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="d219c-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="d219c-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d219c-125">Implementations</span></span>

-   [<span data-ttu-id="d219c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d219c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d219c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d219c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d219c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d219c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d219c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d219c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d219c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d219c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d219c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d219c-131">Windows Server 2003</span></span>



| <span data-ttu-id="d219c-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="d219c-132">Entry</span></span> | <span data-ttu-id="d219c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d219c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d219c-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d219c-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d219c-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d219c-136">System-Only</span></span>            | <span data-ttu-id="d219c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-137">False</span></span>                                                                   |
| <span data-ttu-id="d219c-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d219c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d219c-139">True</span><span class="sxs-lookup"><span data-stu-id="d219c-139">True</span></span>                                                                    |
| <span data-ttu-id="d219c-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d219c-140">Is Indexed</span></span>             | <span data-ttu-id="d219c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-141">False</span></span>                                                                   |
| <span data-ttu-id="d219c-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d219c-142">In Global Catalog</span></span>      | <span data-ttu-id="d219c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-143">False</span></span>                                                                   |
| <span data-ttu-id="d219c-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d219c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d219c-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d219c-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d219c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d219c-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d219c-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-148">Search-Flags</span></span>           | <span data-ttu-id="d219c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d219c-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="d219c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-150">System-Flags</span></span>           | <span data-ttu-id="d219c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d219c-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="d219c-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d219c-152">Classes used in</span></span>        | [<span data-ttu-id="d219c-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="d219c-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d219c-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d219c-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d219c-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="d219c-155">Entry</span></span> | <span data-ttu-id="d219c-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d219c-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d219c-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d219c-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d219c-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d219c-159">System-Only</span></span>            | <span data-ttu-id="d219c-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-160">False</span></span>                                                                   |
| <span data-ttu-id="d219c-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d219c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d219c-162">True</span><span class="sxs-lookup"><span data-stu-id="d219c-162">True</span></span>                                                                    |
| <span data-ttu-id="d219c-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d219c-163">Is Indexed</span></span>             | <span data-ttu-id="d219c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-164">False</span></span>                                                                   |
| <span data-ttu-id="d219c-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d219c-165">In Global Catalog</span></span>      | <span data-ttu-id="d219c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-166">False</span></span>                                                                   |
| <span data-ttu-id="d219c-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d219c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d219c-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d219c-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d219c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d219c-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d219c-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-171">Search-Flags</span></span>           | <span data-ttu-id="d219c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d219c-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="d219c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-173">System-Flags</span></span>           | <span data-ttu-id="d219c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d219c-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="d219c-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d219c-175">Classes used in</span></span>        | [<span data-ttu-id="d219c-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="d219c-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d219c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d219c-177">Windows Server 2008</span></span>



| <span data-ttu-id="d219c-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="d219c-178">Entry</span></span> | <span data-ttu-id="d219c-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d219c-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d219c-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d219c-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d219c-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d219c-182">System-Only</span></span>            | <span data-ttu-id="d219c-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-183">False</span></span>                                                                   |
| <span data-ttu-id="d219c-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d219c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d219c-185">True</span><span class="sxs-lookup"><span data-stu-id="d219c-185">True</span></span>                                                                    |
| <span data-ttu-id="d219c-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d219c-186">Is Indexed</span></span>             | <span data-ttu-id="d219c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-187">False</span></span>                                                                   |
| <span data-ttu-id="d219c-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d219c-188">In Global Catalog</span></span>      | <span data-ttu-id="d219c-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-189">False</span></span>                                                                   |
| <span data-ttu-id="d219c-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d219c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d219c-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d219c-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d219c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d219c-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d219c-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-194">Search-Flags</span></span>           | <span data-ttu-id="d219c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d219c-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="d219c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-196">System-Flags</span></span>           | <span data-ttu-id="d219c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d219c-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="d219c-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d219c-198">Classes used in</span></span>        | [<span data-ttu-id="d219c-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="d219c-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d219c-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d219c-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d219c-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="d219c-201">Entry</span></span> | <span data-ttu-id="d219c-202">Значение</span><span class="sxs-lookup"><span data-stu-id="d219c-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d219c-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d219c-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d219c-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d219c-205">System-Only</span></span>            | <span data-ttu-id="d219c-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-206">False</span></span>                                                                   |
| <span data-ttu-id="d219c-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d219c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d219c-208">True</span><span class="sxs-lookup"><span data-stu-id="d219c-208">True</span></span>                                                                    |
| <span data-ttu-id="d219c-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d219c-209">Is Indexed</span></span>             | <span data-ttu-id="d219c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-210">False</span></span>                                                                   |
| <span data-ttu-id="d219c-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d219c-211">In Global Catalog</span></span>      | <span data-ttu-id="d219c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-212">False</span></span>                                                                   |
| <span data-ttu-id="d219c-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d219c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d219c-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d219c-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d219c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d219c-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d219c-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-217">Search-Flags</span></span>           | <span data-ttu-id="d219c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d219c-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="d219c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-219">System-Flags</span></span>           | <span data-ttu-id="d219c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d219c-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="d219c-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d219c-221">Classes used in</span></span>        | [<span data-ttu-id="d219c-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="d219c-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d219c-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d219c-223">Windows Server 2012</span></span>



| <span data-ttu-id="d219c-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="d219c-224">Entry</span></span> | <span data-ttu-id="d219c-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d219c-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d219c-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d219c-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d219c-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d219c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d219c-228">System-Only</span></span>            | <span data-ttu-id="d219c-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-229">False</span></span>                                                                   |
| <span data-ttu-id="d219c-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d219c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d219c-231">True</span><span class="sxs-lookup"><span data-stu-id="d219c-231">True</span></span>                                                                    |
| <span data-ttu-id="d219c-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d219c-232">Is Indexed</span></span>             | <span data-ttu-id="d219c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-233">False</span></span>                                                                   |
| <span data-ttu-id="d219c-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d219c-234">In Global Catalog</span></span>      | <span data-ttu-id="d219c-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d219c-235">False</span></span>                                                                   |
| <span data-ttu-id="d219c-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d219c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d219c-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d219c-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d219c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d219c-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d219c-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d219c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-240">Search-Flags</span></span>           | <span data-ttu-id="d219c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d219c-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="d219c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d219c-242">System-Flags</span></span>           | <span data-ttu-id="d219c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d219c-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="d219c-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d219c-244">Classes used in</span></span>        | [<span data-ttu-id="d219c-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="d219c-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





