---
title: атрибут MS-PKI-Certificate-Name-Flag
description: Содержит флаги, связанные с созданием имени субъекта в выданном сертификате.
ms.assetid: 7aeeff69-86b5-4251-bd64-bd99b7c9ef4a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута-флага MS-PKI-Certificate-Name
- Мспки — схема AD атрибута-имени сертификата
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Name-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a9a5f8d6db36c3e3b86945fa529572df38ff6df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416313"
---
# <a name="ms-pki-certificate-name-flag-attribute"></a><span data-ttu-id="a1e1f-105">атрибут MS-PKI-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="a1e1f-105">ms-PKI-Certificate-Name-Flag attribute</span></span>

<span data-ttu-id="a1e1f-106">Содержит флаги, связанные с созданием имени субъекта в выданном сертификате.</span><span class="sxs-lookup"><span data-stu-id="a1e1f-106">Contains the flags related to constructing the subject name in an issued certificate.</span></span>



| <span data-ttu-id="a1e1f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1e1f-107">Entry</span></span> | <span data-ttu-id="a1e1f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e1f-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e1f-109">CN</span><span class="sxs-lookup"><span data-stu-id="a1e1f-109">CN</span></span>                | <span data-ttu-id="a1e1f-110">MS-PKI-Certificate-Name — флаг</span><span class="sxs-lookup"><span data-stu-id="a1e1f-110">ms-PKI-Certificate-Name-Flag</span></span>                                                                      |
| <span data-ttu-id="a1e1f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a1e1f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a1e1f-112">Мспки-Certificate-Name — флаг</span><span class="sxs-lookup"><span data-stu-id="a1e1f-112">msPKI-Certificate-Name-Flag</span></span>                                                                       |
| <span data-ttu-id="a1e1f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a1e1f-113">Size</span></span>              | <span data-ttu-id="a1e1f-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="a1e1f-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="a1e1f-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a1e1f-115">Update Privilege</span></span>  | <span data-ttu-id="a1e1f-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="a1e1f-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="a1e1f-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a1e1f-117">Update Frequency</span></span>  | <span data-ttu-id="a1e1f-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="a1e1f-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="a1e1f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1e1f-119">Attribute-Id</span></span>      | <span data-ttu-id="a1e1f-120">1.2.840.113556.1.4.1432</span><span class="sxs-lookup"><span data-stu-id="a1e1f-120">1.2.840.113556.1.4.1432</span></span>                                                                           |
| <span data-ttu-id="a1e1f-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a1e1f-121">System-Id-Guid</span></span>    | <span data-ttu-id="a1e1f-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span><span class="sxs-lookup"><span data-stu-id="a1e1f-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span></span>                                                              |
| <span data-ttu-id="a1e1f-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1e1f-123">Syntax</span></span>            | [<span data-ttu-id="a1e1f-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="a1e1f-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a1e1f-125">Implementations</span></span>

-   [<span data-ttu-id="a1e1f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1e1f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1e1f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1e1f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1e1f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a1e1f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1e1f-131">Windows Server 2003</span></span>



| <span data-ttu-id="a1e1f-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1e1f-132">Entry</span></span> | <span data-ttu-id="a1e1f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e1f-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a1e1f-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1e1f-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e1f-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e1f-136">System-Only</span></span>            | <span data-ttu-id="a1e1f-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-137">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1e1f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e1f-139">True</span><span class="sxs-lookup"><span data-stu-id="a1e1f-139">True</span></span>                                                                    |
| <span data-ttu-id="a1e1f-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1e1f-140">Is Indexed</span></span>             | <span data-ttu-id="a1e1f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-141">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1e1f-142">In Global Catalog</span></span>      | <span data-ttu-id="a1e1f-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-143">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1e1f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e1f-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1e1f-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a1e1f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e1f-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e1f-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-148">Search-Flags</span></span>           | <span data-ttu-id="a1e1f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e1f-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="a1e1f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-150">System-Flags</span></span>           | <span data-ttu-id="a1e1f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e1f-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="a1e1f-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1e1f-152">Classes used in</span></span>        | [<span data-ttu-id="a1e1f-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1e1f-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1e1f-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1e1f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1e1f-155">Entry</span></span> | <span data-ttu-id="a1e1f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e1f-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a1e1f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1e1f-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e1f-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e1f-159">System-Only</span></span>            | <span data-ttu-id="a1e1f-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-160">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1e1f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e1f-162">True</span><span class="sxs-lookup"><span data-stu-id="a1e1f-162">True</span></span>                                                                    |
| <span data-ttu-id="a1e1f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1e1f-163">Is Indexed</span></span>             | <span data-ttu-id="a1e1f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-164">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1e1f-165">In Global Catalog</span></span>      | <span data-ttu-id="a1e1f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-166">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1e1f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e1f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1e1f-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a1e1f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e1f-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e1f-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-171">Search-Flags</span></span>           | <span data-ttu-id="a1e1f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e1f-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="a1e1f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-173">System-Flags</span></span>           | <span data-ttu-id="a1e1f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e1f-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="a1e1f-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1e1f-175">Classes used in</span></span>        | [<span data-ttu-id="a1e1f-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1e1f-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1e1f-177">Windows Server 2008</span></span>



| <span data-ttu-id="a1e1f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1e1f-178">Entry</span></span> | <span data-ttu-id="a1e1f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e1f-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a1e1f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1e1f-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e1f-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e1f-182">System-Only</span></span>            | <span data-ttu-id="a1e1f-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-183">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1e1f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e1f-185">True</span><span class="sxs-lookup"><span data-stu-id="a1e1f-185">True</span></span>                                                                    |
| <span data-ttu-id="a1e1f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1e1f-186">Is Indexed</span></span>             | <span data-ttu-id="a1e1f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-187">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1e1f-188">In Global Catalog</span></span>      | <span data-ttu-id="a1e1f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-189">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1e1f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e1f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1e1f-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a1e1f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e1f-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e1f-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-194">Search-Flags</span></span>           | <span data-ttu-id="a1e1f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e1f-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="a1e1f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-196">System-Flags</span></span>           | <span data-ttu-id="a1e1f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e1f-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="a1e1f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1e1f-198">Classes used in</span></span>        | [<span data-ttu-id="a1e1f-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1e1f-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1e1f-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1e1f-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1e1f-201">Entry</span></span> | <span data-ttu-id="a1e1f-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e1f-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a1e1f-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1e1f-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e1f-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e1f-205">System-Only</span></span>            | <span data-ttu-id="a1e1f-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-206">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1e1f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e1f-208">True</span><span class="sxs-lookup"><span data-stu-id="a1e1f-208">True</span></span>                                                                    |
| <span data-ttu-id="a1e1f-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1e1f-209">Is Indexed</span></span>             | <span data-ttu-id="a1e1f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-210">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1e1f-211">In Global Catalog</span></span>      | <span data-ttu-id="a1e1f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-212">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1e1f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e1f-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1e1f-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a1e1f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e1f-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e1f-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-217">Search-Flags</span></span>           | <span data-ttu-id="a1e1f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e1f-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="a1e1f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-219">System-Flags</span></span>           | <span data-ttu-id="a1e1f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e1f-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="a1e1f-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1e1f-221">Classes used in</span></span>        | [<span data-ttu-id="a1e1f-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1e1f-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1e1f-223">Windows Server 2012</span></span>



| <span data-ttu-id="a1e1f-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1e1f-224">Entry</span></span> | <span data-ttu-id="a1e1f-225">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e1f-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a1e1f-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1e1f-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e1f-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a1e1f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e1f-228">System-Only</span></span>            | <span data-ttu-id="a1e1f-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-229">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1e1f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e1f-231">True</span><span class="sxs-lookup"><span data-stu-id="a1e1f-231">True</span></span>                                                                    |
| <span data-ttu-id="a1e1f-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1e1f-232">Is Indexed</span></span>             | <span data-ttu-id="a1e1f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-233">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1e1f-234">In Global Catalog</span></span>      | <span data-ttu-id="a1e1f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1e1f-235">False</span></span>                                                                   |
| <span data-ttu-id="a1e1f-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1e1f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e1f-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1e1f-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a1e1f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e1f-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e1f-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a1e1f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-240">Search-Flags</span></span>           | <span data-ttu-id="a1e1f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e1f-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="a1e1f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e1f-242">System-Flags</span></span>           | <span data-ttu-id="a1e1f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e1f-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="a1e1f-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1e1f-244">Classes used in</span></span>        | [<span data-ttu-id="a1e1f-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="a1e1f-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





