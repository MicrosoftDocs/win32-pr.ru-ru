---
title: атрибут MS-PKI-Template-Schema-Version
description: Отслеживает обновления схемы класса PKI-Certificate-Template.
ms.assetid: 7ad55f1a-cdb9-4eea-bd09-db4f5e6373ba
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-PKI-Template-Schema-Version
- Схема AD атрибута Мспки-Template-Schema-Version
topic_type:
- apiref
api_name:
- ms-PKI-Template-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc3b7952b55b346da29119775bb9c0f8b825c50
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655137"
---
# <a name="ms-pki-template-schema-version-attribute"></a><span data-ttu-id="bc559-105">атрибут MS-PKI-Template-Schema-Version</span><span class="sxs-lookup"><span data-stu-id="bc559-105">ms-PKI-Template-Schema-Version attribute</span></span>

<span data-ttu-id="bc559-106">Отслеживает обновления схемы класса PKI-Certificate-Template.</span><span class="sxs-lookup"><span data-stu-id="bc559-106">Keeps track of schema updates of the PKI-Certificate-Template class.</span></span>



| <span data-ttu-id="bc559-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc559-107">Entry</span></span> | <span data-ttu-id="bc559-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bc559-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc559-109">CN</span><span class="sxs-lookup"><span data-stu-id="bc559-109">CN</span></span>                | <span data-ttu-id="bc559-110">MS-PKI-Template-Schema-Version</span><span class="sxs-lookup"><span data-stu-id="bc559-110">ms-PKI-Template-Schema-Version</span></span>                                                                    |
| <span data-ttu-id="bc559-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bc559-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bc559-112">Мспки-Template-Schema-Version</span><span class="sxs-lookup"><span data-stu-id="bc559-112">msPKI-Template-Schema-Version</span></span>                                                                     |
| <span data-ttu-id="bc559-113">Размер</span><span class="sxs-lookup"><span data-stu-id="bc559-113">Size</span></span>              | <span data-ttu-id="bc559-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="bc559-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="bc559-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bc559-115">Update Privilege</span></span>  | <span data-ttu-id="bc559-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="bc559-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="bc559-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bc559-117">Update Frequency</span></span>  | <span data-ttu-id="bc559-118">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="bc559-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="bc559-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc559-119">Attribute-Id</span></span>      | <span data-ttu-id="bc559-120">1.2.840.113556.1.4.1434</span><span class="sxs-lookup"><span data-stu-id="bc559-120">1.2.840.113556.1.4.1434</span></span>                                                                           |
| <span data-ttu-id="bc559-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bc559-121">System-Id-Guid</span></span>    | <span data-ttu-id="bc559-122">0c15e9f5-491d-4594-918f-32813a091da9</span><span class="sxs-lookup"><span data-stu-id="bc559-122">0c15e9f5-491d-4594-918f-32813a091da9</span></span>                                                              |
| <span data-ttu-id="bc559-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc559-123">Syntax</span></span>            | [<span data-ttu-id="bc559-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="bc559-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="bc559-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bc559-125">Implementations</span></span>

-   [<span data-ttu-id="bc559-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc559-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc559-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc559-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc559-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc559-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc559-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc559-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc559-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc559-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bc559-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc559-131">Windows Server 2003</span></span>



| <span data-ttu-id="bc559-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc559-132">Entry</span></span> | <span data-ttu-id="bc559-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bc559-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc559-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc559-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc559-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc559-136">System-Only</span></span>            | <span data-ttu-id="bc559-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-137">False</span></span>                                                                   |
| <span data-ttu-id="bc559-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc559-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bc559-139">True</span><span class="sxs-lookup"><span data-stu-id="bc559-139">True</span></span>                                                                    |
| <span data-ttu-id="bc559-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc559-140">Is Indexed</span></span>             | <span data-ttu-id="bc559-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-141">False</span></span>                                                                   |
| <span data-ttu-id="bc559-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc559-142">In Global Catalog</span></span>      | <span data-ttu-id="bc559-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-143">False</span></span>                                                                   |
| <span data-ttu-id="bc559-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc559-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc559-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc559-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc559-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc559-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc559-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-148">Search-Flags</span></span>           | <span data-ttu-id="bc559-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc559-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc559-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-150">System-Flags</span></span>           | <span data-ttu-id="bc559-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc559-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc559-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc559-152">Classes used in</span></span>        | [<span data-ttu-id="bc559-153">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc559-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc559-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc559-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc559-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc559-155">Entry</span></span> | <span data-ttu-id="bc559-156">Значение</span><span class="sxs-lookup"><span data-stu-id="bc559-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc559-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc559-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc559-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc559-159">System-Only</span></span>            | <span data-ttu-id="bc559-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-160">False</span></span>                                                                   |
| <span data-ttu-id="bc559-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc559-161">Is-Single-Valued</span></span>       | <span data-ttu-id="bc559-162">True</span><span class="sxs-lookup"><span data-stu-id="bc559-162">True</span></span>                                                                    |
| <span data-ttu-id="bc559-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc559-163">Is Indexed</span></span>             | <span data-ttu-id="bc559-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-164">False</span></span>                                                                   |
| <span data-ttu-id="bc559-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc559-165">In Global Catalog</span></span>      | <span data-ttu-id="bc559-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-166">False</span></span>                                                                   |
| <span data-ttu-id="bc559-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc559-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc559-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc559-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc559-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc559-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc559-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-171">Search-Flags</span></span>           | <span data-ttu-id="bc559-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc559-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc559-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-173">System-Flags</span></span>           | <span data-ttu-id="bc559-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc559-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc559-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc559-175">Classes used in</span></span>        | [<span data-ttu-id="bc559-176">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc559-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc559-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc559-177">Windows Server 2008</span></span>



| <span data-ttu-id="bc559-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc559-178">Entry</span></span> | <span data-ttu-id="bc559-179">Значение</span><span class="sxs-lookup"><span data-stu-id="bc559-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc559-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc559-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc559-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc559-182">System-Only</span></span>            | <span data-ttu-id="bc559-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-183">False</span></span>                                                                   |
| <span data-ttu-id="bc559-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc559-184">Is-Single-Valued</span></span>       | <span data-ttu-id="bc559-185">True</span><span class="sxs-lookup"><span data-stu-id="bc559-185">True</span></span>                                                                    |
| <span data-ttu-id="bc559-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc559-186">Is Indexed</span></span>             | <span data-ttu-id="bc559-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-187">False</span></span>                                                                   |
| <span data-ttu-id="bc559-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc559-188">In Global Catalog</span></span>      | <span data-ttu-id="bc559-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-189">False</span></span>                                                                   |
| <span data-ttu-id="bc559-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc559-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc559-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc559-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc559-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc559-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc559-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-194">Search-Flags</span></span>           | <span data-ttu-id="bc559-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc559-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc559-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-196">System-Flags</span></span>           | <span data-ttu-id="bc559-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc559-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc559-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc559-198">Classes used in</span></span>        | [<span data-ttu-id="bc559-199">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc559-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc559-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc559-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc559-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc559-201">Entry</span></span> | <span data-ttu-id="bc559-202">Значение</span><span class="sxs-lookup"><span data-stu-id="bc559-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc559-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc559-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc559-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc559-205">System-Only</span></span>            | <span data-ttu-id="bc559-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-206">False</span></span>                                                                   |
| <span data-ttu-id="bc559-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc559-207">Is-Single-Valued</span></span>       | <span data-ttu-id="bc559-208">True</span><span class="sxs-lookup"><span data-stu-id="bc559-208">True</span></span>                                                                    |
| <span data-ttu-id="bc559-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc559-209">Is Indexed</span></span>             | <span data-ttu-id="bc559-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-210">False</span></span>                                                                   |
| <span data-ttu-id="bc559-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc559-211">In Global Catalog</span></span>      | <span data-ttu-id="bc559-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-212">False</span></span>                                                                   |
| <span data-ttu-id="bc559-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc559-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc559-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc559-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc559-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc559-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc559-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-217">Search-Flags</span></span>           | <span data-ttu-id="bc559-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc559-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc559-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-219">System-Flags</span></span>           | <span data-ttu-id="bc559-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc559-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc559-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc559-221">Classes used in</span></span>        | [<span data-ttu-id="bc559-222">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc559-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc559-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc559-223">Windows Server 2012</span></span>



| <span data-ttu-id="bc559-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc559-224">Entry</span></span> | <span data-ttu-id="bc559-225">Значение</span><span class="sxs-lookup"><span data-stu-id="bc559-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bc559-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc559-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc559-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bc559-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc559-228">System-Only</span></span>            | <span data-ttu-id="bc559-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-229">False</span></span>                                                                   |
| <span data-ttu-id="bc559-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc559-230">Is-Single-Valued</span></span>       | <span data-ttu-id="bc559-231">True</span><span class="sxs-lookup"><span data-stu-id="bc559-231">True</span></span>                                                                    |
| <span data-ttu-id="bc559-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc559-232">Is Indexed</span></span>             | <span data-ttu-id="bc559-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-233">False</span></span>                                                                   |
| <span data-ttu-id="bc559-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc559-234">In Global Catalog</span></span>      | <span data-ttu-id="bc559-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc559-235">False</span></span>                                                                   |
| <span data-ttu-id="bc559-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc559-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc559-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc559-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bc559-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc559-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc559-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="bc559-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-240">Search-Flags</span></span>           | <span data-ttu-id="bc559-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc559-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="bc559-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc559-242">System-Flags</span></span>           | <span data-ttu-id="bc559-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc559-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="bc559-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc559-244">Classes used in</span></span>        | [<span data-ttu-id="bc559-245">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="bc559-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





