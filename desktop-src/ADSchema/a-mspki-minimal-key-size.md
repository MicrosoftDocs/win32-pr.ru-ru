---
title: атрибут MS-PKI-минимальный-Key-size
description: Указывает минимальный размер закрытого ключа.
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута MS-PKI-минимального ключа
- Мспки — схема AD атрибута минимального размера ключа
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138594"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="b0fd6-105">атрибут MS-PKI-минимальный-Key-size</span><span class="sxs-lookup"><span data-stu-id="b0fd6-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="b0fd6-106">Указывает минимальный размер закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b0fd6-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="b0fd6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b0fd6-107">Entry</span></span> | <span data-ttu-id="b0fd6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fd6-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fd6-109">CN</span><span class="sxs-lookup"><span data-stu-id="b0fd6-109">CN</span></span>                | <span data-ttu-id="b0fd6-110">MS-PKI-минимальный-ключ-размер</span><span class="sxs-lookup"><span data-stu-id="b0fd6-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="b0fd6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b0fd6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b0fd6-112">Мспки — минимальный размер ключа</span><span class="sxs-lookup"><span data-stu-id="b0fd6-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="b0fd6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b0fd6-113">Size</span></span>              | <span data-ttu-id="b0fd6-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="b0fd6-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="b0fd6-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b0fd6-115">Update Privilege</span></span>  | <span data-ttu-id="b0fd6-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="b0fd6-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="b0fd6-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b0fd6-117">Update Frequency</span></span>  | <span data-ttu-id="b0fd6-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="b0fd6-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="b0fd6-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0fd6-119">Attribute-Id</span></span>      | <span data-ttu-id="b0fd6-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="b0fd6-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="b0fd6-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b0fd6-121">System-Id-Guid</span></span>    | <span data-ttu-id="b0fd6-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="b0fd6-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="b0fd6-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0fd6-123">Syntax</span></span>            | [<span data-ttu-id="b0fd6-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="b0fd6-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b0fd6-125">Implementations</span></span>

-   [<span data-ttu-id="b0fd6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0fd6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0fd6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0fd6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0fd6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b0fd6-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0fd6-131">Windows Server 2003</span></span>



| <span data-ttu-id="b0fd6-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="b0fd6-132">Entry</span></span> | <span data-ttu-id="b0fd6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fd6-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b0fd6-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b0fd6-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0fd6-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0fd6-136">System-Only</span></span>            | <span data-ttu-id="b0fd6-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-137">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b0fd6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b0fd6-139">True</span><span class="sxs-lookup"><span data-stu-id="b0fd6-139">True</span></span>                                                                    |
| <span data-ttu-id="b0fd6-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b0fd6-140">Is Indexed</span></span>             | <span data-ttu-id="b0fd6-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-141">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b0fd6-142">In Global Catalog</span></span>      | <span data-ttu-id="b0fd6-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-143">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0fd6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0fd6-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0fd6-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b0fd6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0fd6-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0fd6-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-148">Search-Flags</span></span>           | <span data-ttu-id="b0fd6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0fd6-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="b0fd6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-150">System-Flags</span></span>           | <span data-ttu-id="b0fd6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0fd6-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="b0fd6-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b0fd6-152">Classes used in</span></span>        | [<span data-ttu-id="b0fd6-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0fd6-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0fd6-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0fd6-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b0fd6-155">Entry</span></span> | <span data-ttu-id="b0fd6-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fd6-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b0fd6-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b0fd6-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0fd6-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0fd6-159">System-Only</span></span>            | <span data-ttu-id="b0fd6-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-160">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b0fd6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b0fd6-162">True</span><span class="sxs-lookup"><span data-stu-id="b0fd6-162">True</span></span>                                                                    |
| <span data-ttu-id="b0fd6-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b0fd6-163">Is Indexed</span></span>             | <span data-ttu-id="b0fd6-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-164">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b0fd6-165">In Global Catalog</span></span>      | <span data-ttu-id="b0fd6-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-166">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0fd6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0fd6-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0fd6-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b0fd6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0fd6-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0fd6-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-171">Search-Flags</span></span>           | <span data-ttu-id="b0fd6-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0fd6-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="b0fd6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-173">System-Flags</span></span>           | <span data-ttu-id="b0fd6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0fd6-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="b0fd6-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b0fd6-175">Classes used in</span></span>        | [<span data-ttu-id="b0fd6-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b0fd6-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0fd6-177">Windows Server 2008</span></span>



| <span data-ttu-id="b0fd6-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="b0fd6-178">Entry</span></span> | <span data-ttu-id="b0fd6-179">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fd6-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b0fd6-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b0fd6-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0fd6-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0fd6-182">System-Only</span></span>            | <span data-ttu-id="b0fd6-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-183">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b0fd6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b0fd6-185">True</span><span class="sxs-lookup"><span data-stu-id="b0fd6-185">True</span></span>                                                                    |
| <span data-ttu-id="b0fd6-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b0fd6-186">Is Indexed</span></span>             | <span data-ttu-id="b0fd6-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-187">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b0fd6-188">In Global Catalog</span></span>      | <span data-ttu-id="b0fd6-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-189">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0fd6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0fd6-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0fd6-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b0fd6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0fd6-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0fd6-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-194">Search-Flags</span></span>           | <span data-ttu-id="b0fd6-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0fd6-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="b0fd6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-196">System-Flags</span></span>           | <span data-ttu-id="b0fd6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0fd6-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="b0fd6-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b0fd6-198">Classes used in</span></span>        | [<span data-ttu-id="b0fd6-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0fd6-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0fd6-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0fd6-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="b0fd6-201">Entry</span></span> | <span data-ttu-id="b0fd6-202">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fd6-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b0fd6-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b0fd6-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0fd6-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0fd6-205">System-Only</span></span>            | <span data-ttu-id="b0fd6-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-206">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b0fd6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b0fd6-208">True</span><span class="sxs-lookup"><span data-stu-id="b0fd6-208">True</span></span>                                                                    |
| <span data-ttu-id="b0fd6-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b0fd6-209">Is Indexed</span></span>             | <span data-ttu-id="b0fd6-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-210">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b0fd6-211">In Global Catalog</span></span>      | <span data-ttu-id="b0fd6-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-212">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0fd6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0fd6-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0fd6-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b0fd6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0fd6-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0fd6-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-217">Search-Flags</span></span>           | <span data-ttu-id="b0fd6-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0fd6-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="b0fd6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-219">System-Flags</span></span>           | <span data-ttu-id="b0fd6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0fd6-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="b0fd6-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b0fd6-221">Classes used in</span></span>        | [<span data-ttu-id="b0fd6-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b0fd6-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0fd6-223">Windows Server 2012</span></span>



| <span data-ttu-id="b0fd6-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="b0fd6-224">Entry</span></span> | <span data-ttu-id="b0fd6-225">Значение</span><span class="sxs-lookup"><span data-stu-id="b0fd6-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b0fd6-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b0fd6-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0fd6-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b0fd6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0fd6-228">System-Only</span></span>            | <span data-ttu-id="b0fd6-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-229">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b0fd6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b0fd6-231">True</span><span class="sxs-lookup"><span data-stu-id="b0fd6-231">True</span></span>                                                                    |
| <span data-ttu-id="b0fd6-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b0fd6-232">Is Indexed</span></span>             | <span data-ttu-id="b0fd6-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-233">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b0fd6-234">In Global Catalog</span></span>      | <span data-ttu-id="b0fd6-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b0fd6-235">False</span></span>                                                                   |
| <span data-ttu-id="b0fd6-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b0fd6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0fd6-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0fd6-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b0fd6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0fd6-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0fd6-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b0fd6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-240">Search-Flags</span></span>           | <span data-ttu-id="b0fd6-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0fd6-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="b0fd6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0fd6-242">System-Flags</span></span>           | <span data-ttu-id="b0fd6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0fd6-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="b0fd6-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b0fd6-244">Classes used in</span></span>        | [<span data-ttu-id="b0fd6-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="b0fd6-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





