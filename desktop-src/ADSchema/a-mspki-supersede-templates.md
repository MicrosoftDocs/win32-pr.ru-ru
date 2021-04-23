---
title: MS-PKI-замена-атрибут Templates
description: Указывает имена шаблонов сертификатов, заменяемых текущим шаблоном.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- MS-PKI-замена — атрибут шаблона AD
- Мспки — замена атрибута Template AD
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535969"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="ac8b3-105">MS-PKI-замена-атрибут Templates</span><span class="sxs-lookup"><span data-stu-id="ac8b3-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="ac8b3-106">Указывает имена шаблонов сертификатов, заменяемых текущим шаблоном.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="ac8b3-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac8b3-107">Entry</span></span> | <span data-ttu-id="ac8b3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8b3-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8b3-109">CN</span><span class="sxs-lookup"><span data-stu-id="ac8b3-109">CN</span></span>                | <span data-ttu-id="ac8b3-110">MS-PKI-замена — шаблоны</span><span class="sxs-lookup"><span data-stu-id="ac8b3-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="ac8b3-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ac8b3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ac8b3-112">Мспки — Замена шаблонов</span><span class="sxs-lookup"><span data-stu-id="ac8b3-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="ac8b3-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ac8b3-113">Size</span></span>              | <span data-ttu-id="ac8b3-114">64 байт</span><span class="sxs-lookup"><span data-stu-id="ac8b3-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="ac8b3-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ac8b3-115">Update Privilege</span></span>  | <span data-ttu-id="ac8b3-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="ac8b3-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="ac8b3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ac8b3-117">Update Frequency</span></span>  | <span data-ttu-id="ac8b3-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="ac8b3-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="ac8b3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac8b3-119">Attribute-Id</span></span>      | <span data-ttu-id="ac8b3-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="ac8b3-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="ac8b3-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ac8b3-121">System-Id-Guid</span></span>    | <span data-ttu-id="ac8b3-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="ac8b3-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="ac8b3-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac8b3-123">Syntax</span></span>            | [<span data-ttu-id="ac8b3-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="ac8b3-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ac8b3-125">Implementations</span></span>

-   [<span data-ttu-id="ac8b3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac8b3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac8b3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac8b3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac8b3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ac8b3-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac8b3-131">Windows Server 2003</span></span>



| <span data-ttu-id="ac8b3-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac8b3-132">Entry</span></span> | <span data-ttu-id="ac8b3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8b3-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ac8b3-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac8b3-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac8b3-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac8b3-136">System-Only</span></span>            | <span data-ttu-id="ac8b3-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-137">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac8b3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ac8b3-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-139">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac8b3-140">Is Indexed</span></span>             | <span data-ttu-id="ac8b3-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-141">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac8b3-142">In Global Catalog</span></span>      | <span data-ttu-id="ac8b3-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-143">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac8b3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac8b3-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac8b3-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ac8b3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac8b3-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac8b3-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-148">Search-Flags</span></span>           | <span data-ttu-id="ac8b3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac8b3-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="ac8b3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-150">System-Flags</span></span>           | <span data-ttu-id="ac8b3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac8b3-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="ac8b3-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac8b3-152">Classes used in</span></span>        | [<span data-ttu-id="ac8b3-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac8b3-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac8b3-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac8b3-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac8b3-155">Entry</span></span> | <span data-ttu-id="ac8b3-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8b3-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ac8b3-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac8b3-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac8b3-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac8b3-159">System-Only</span></span>            | <span data-ttu-id="ac8b3-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-160">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac8b3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ac8b3-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-162">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac8b3-163">Is Indexed</span></span>             | <span data-ttu-id="ac8b3-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-164">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac8b3-165">In Global Catalog</span></span>      | <span data-ttu-id="ac8b3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-166">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac8b3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac8b3-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac8b3-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ac8b3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac8b3-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac8b3-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-171">Search-Flags</span></span>           | <span data-ttu-id="ac8b3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac8b3-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="ac8b3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-173">System-Flags</span></span>           | <span data-ttu-id="ac8b3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac8b3-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="ac8b3-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac8b3-175">Classes used in</span></span>        | [<span data-ttu-id="ac8b3-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac8b3-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac8b3-177">Windows Server 2008</span></span>



| <span data-ttu-id="ac8b3-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac8b3-178">Entry</span></span> | <span data-ttu-id="ac8b3-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8b3-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ac8b3-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac8b3-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac8b3-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac8b3-182">System-Only</span></span>            | <span data-ttu-id="ac8b3-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-183">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac8b3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ac8b3-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-185">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac8b3-186">Is Indexed</span></span>             | <span data-ttu-id="ac8b3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-187">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac8b3-188">In Global Catalog</span></span>      | <span data-ttu-id="ac8b3-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-189">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac8b3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac8b3-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac8b3-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ac8b3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac8b3-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac8b3-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-194">Search-Flags</span></span>           | <span data-ttu-id="ac8b3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac8b3-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="ac8b3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-196">System-Flags</span></span>           | <span data-ttu-id="ac8b3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac8b3-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="ac8b3-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac8b3-198">Classes used in</span></span>        | [<span data-ttu-id="ac8b3-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac8b3-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac8b3-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac8b3-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac8b3-201">Entry</span></span> | <span data-ttu-id="ac8b3-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8b3-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ac8b3-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac8b3-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac8b3-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac8b3-205">System-Only</span></span>            | <span data-ttu-id="ac8b3-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-206">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac8b3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ac8b3-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-208">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac8b3-209">Is Indexed</span></span>             | <span data-ttu-id="ac8b3-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-210">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac8b3-211">In Global Catalog</span></span>      | <span data-ttu-id="ac8b3-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-212">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac8b3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac8b3-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac8b3-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ac8b3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac8b3-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac8b3-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-217">Search-Flags</span></span>           | <span data-ttu-id="ac8b3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac8b3-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="ac8b3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-219">System-Flags</span></span>           | <span data-ttu-id="ac8b3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac8b3-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="ac8b3-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac8b3-221">Classes used in</span></span>        | [<span data-ttu-id="ac8b3-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac8b3-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac8b3-223">Windows Server 2012</span></span>



| <span data-ttu-id="ac8b3-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac8b3-224">Entry</span></span> | <span data-ttu-id="ac8b3-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8b3-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ac8b3-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac8b3-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac8b3-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="ac8b3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac8b3-228">System-Only</span></span>            | <span data-ttu-id="ac8b3-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-229">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac8b3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ac8b3-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-231">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac8b3-232">Is Indexed</span></span>             | <span data-ttu-id="ac8b3-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-233">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac8b3-234">In Global Catalog</span></span>      | <span data-ttu-id="ac8b3-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac8b3-235">False</span></span>                                                                   |
| <span data-ttu-id="ac8b3-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac8b3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac8b3-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac8b3-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="ac8b3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac8b3-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac8b3-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="ac8b3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-240">Search-Flags</span></span>           | <span data-ttu-id="ac8b3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac8b3-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="ac8b3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac8b3-242">System-Flags</span></span>           | <span data-ttu-id="ac8b3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac8b3-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="ac8b3-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac8b3-244">Classes used in</span></span>        | [<span data-ttu-id="ac8b3-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="ac8b3-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





