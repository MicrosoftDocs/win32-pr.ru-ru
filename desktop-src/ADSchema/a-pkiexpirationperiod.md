---
title: PKI — атрибут периода истечения срока действия
description: Срок действия шаблона сертификата.
ms.assetid: 6b3f7497-b156-4afe-ae93-ccb96d9ba403
ms.tgt_platform: multiple
keywords:
- PKI — схема AD атрибута периода истечения срока действия
- Схема AD атрибута Пкиекспиратионпериод
topic_type:
- apiref
api_name:
- PKI-Expiration-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6553bbeb23c6b810c5fcb7b82a4ffdee0f303ee2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493725"
---
# <a name="pki-expiration-period-attribute"></a><span data-ttu-id="39e71-105">PKI — атрибут периода истечения срока действия</span><span class="sxs-lookup"><span data-stu-id="39e71-105">PKI-Expiration-Period attribute</span></span>

<span data-ttu-id="39e71-106">Срок действия шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="39e71-106">The validity period for the certificate template.</span></span>



| <span data-ttu-id="39e71-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-107">Entry</span></span> | <span data-ttu-id="39e71-108">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="39e71-109">CN</span><span class="sxs-lookup"><span data-stu-id="39e71-109">CN</span></span>                | <span data-ttu-id="39e71-110">PKI-срок действия — период</span><span class="sxs-lookup"><span data-stu-id="39e71-110">PKI-Expiration-Period</span></span>                                 |
| <span data-ttu-id="39e71-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="39e71-111">Ldap-Display-Name</span></span> | <span data-ttu-id="39e71-112">пкиекспиратионпериод</span><span class="sxs-lookup"><span data-stu-id="39e71-112">pKIExpirationPeriod</span></span>                                   |
| <span data-ttu-id="39e71-113">Размер</span><span class="sxs-lookup"><span data-stu-id="39e71-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="39e71-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="39e71-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="39e71-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="39e71-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="39e71-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-116">Attribute-Id</span></span>      | <span data-ttu-id="39e71-117">1.2.840.113556.1.4.1331</span><span class="sxs-lookup"><span data-stu-id="39e71-117">1.2.840.113556.1.4.1331</span></span>                               |
| <span data-ttu-id="39e71-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="39e71-118">System-Id-Guid</span></span>    | <span data-ttu-id="39e71-119">041570d2-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="39e71-119">041570d2-3b9e-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="39e71-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39e71-120">Syntax</span></span>            | [<span data-ttu-id="39e71-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="39e71-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="39e71-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="39e71-122">Implementations</span></span>

-   [<span data-ttu-id="39e71-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39e71-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39e71-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39e71-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39e71-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39e71-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39e71-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39e71-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39e71-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39e71-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39e71-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39e71-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39e71-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39e71-129">Windows 2000 Server</span></span>



| <span data-ttu-id="39e71-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-130">Entry</span></span> | <span data-ttu-id="39e71-131">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="39e71-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="39e71-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="39e71-134">System-Only</span></span>            | <span data-ttu-id="39e71-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-135">False</span></span>                                                                   |
| <span data-ttu-id="39e71-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="39e71-136">Is-Single-Valued</span></span>       | <span data-ttu-id="39e71-137">True</span><span class="sxs-lookup"><span data-stu-id="39e71-137">True</span></span>                                                                    |
| <span data-ttu-id="39e71-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="39e71-138">Is Indexed</span></span>             | <span data-ttu-id="39e71-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-139">False</span></span>                                                                   |
| <span data-ttu-id="39e71-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="39e71-140">In Global Catalog</span></span>      | <span data-ttu-id="39e71-141">True</span><span class="sxs-lookup"><span data-stu-id="39e71-141">True</span></span>                                                                    |
| <span data-ttu-id="39e71-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="39e71-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="39e71-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="39e71-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="39e71-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39e71-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39e71-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-146">Search-Flags</span></span>           | <span data-ttu-id="39e71-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39e71-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="39e71-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-148">System-Flags</span></span>           | <span data-ttu-id="39e71-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39e71-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="39e71-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="39e71-150">Classes used in</span></span>        | [<span data-ttu-id="39e71-151">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="39e71-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39e71-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39e71-152">Windows Server 2003</span></span>



| <span data-ttu-id="39e71-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-153">Entry</span></span> | <span data-ttu-id="39e71-154">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="39e71-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="39e71-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="39e71-157">System-Only</span></span>            | <span data-ttu-id="39e71-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-158">False</span></span>                                                                   |
| <span data-ttu-id="39e71-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="39e71-159">Is-Single-Valued</span></span>       | <span data-ttu-id="39e71-160">True</span><span class="sxs-lookup"><span data-stu-id="39e71-160">True</span></span>                                                                    |
| <span data-ttu-id="39e71-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="39e71-161">Is Indexed</span></span>             | <span data-ttu-id="39e71-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-162">False</span></span>                                                                   |
| <span data-ttu-id="39e71-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="39e71-163">In Global Catalog</span></span>      | <span data-ttu-id="39e71-164">True</span><span class="sxs-lookup"><span data-stu-id="39e71-164">True</span></span>                                                                    |
| <span data-ttu-id="39e71-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="39e71-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="39e71-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="39e71-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="39e71-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39e71-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39e71-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-169">Search-Flags</span></span>           | <span data-ttu-id="39e71-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39e71-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="39e71-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-171">System-Flags</span></span>           | <span data-ttu-id="39e71-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39e71-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="39e71-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="39e71-173">Classes used in</span></span>        | [<span data-ttu-id="39e71-174">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="39e71-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39e71-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39e71-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39e71-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-176">Entry</span></span> | <span data-ttu-id="39e71-177">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="39e71-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="39e71-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="39e71-180">System-Only</span></span>            | <span data-ttu-id="39e71-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-181">False</span></span>                                                                   |
| <span data-ttu-id="39e71-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="39e71-182">Is-Single-Valued</span></span>       | <span data-ttu-id="39e71-183">True</span><span class="sxs-lookup"><span data-stu-id="39e71-183">True</span></span>                                                                    |
| <span data-ttu-id="39e71-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="39e71-184">Is Indexed</span></span>             | <span data-ttu-id="39e71-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-185">False</span></span>                                                                   |
| <span data-ttu-id="39e71-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="39e71-186">In Global Catalog</span></span>      | <span data-ttu-id="39e71-187">True</span><span class="sxs-lookup"><span data-stu-id="39e71-187">True</span></span>                                                                    |
| <span data-ttu-id="39e71-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="39e71-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="39e71-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="39e71-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="39e71-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39e71-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39e71-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-192">Search-Flags</span></span>           | <span data-ttu-id="39e71-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39e71-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="39e71-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-194">System-Flags</span></span>           | <span data-ttu-id="39e71-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39e71-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="39e71-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="39e71-196">Classes used in</span></span>        | [<span data-ttu-id="39e71-197">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="39e71-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39e71-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39e71-198">Windows Server 2008</span></span>



| <span data-ttu-id="39e71-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-199">Entry</span></span> | <span data-ttu-id="39e71-200">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="39e71-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="39e71-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="39e71-203">System-Only</span></span>            | <span data-ttu-id="39e71-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-204">False</span></span>                                                                   |
| <span data-ttu-id="39e71-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="39e71-205">Is-Single-Valued</span></span>       | <span data-ttu-id="39e71-206">True</span><span class="sxs-lookup"><span data-stu-id="39e71-206">True</span></span>                                                                    |
| <span data-ttu-id="39e71-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="39e71-207">Is Indexed</span></span>             | <span data-ttu-id="39e71-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-208">False</span></span>                                                                   |
| <span data-ttu-id="39e71-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="39e71-209">In Global Catalog</span></span>      | <span data-ttu-id="39e71-210">True</span><span class="sxs-lookup"><span data-stu-id="39e71-210">True</span></span>                                                                    |
| <span data-ttu-id="39e71-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="39e71-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="39e71-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="39e71-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="39e71-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39e71-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39e71-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-215">Search-Flags</span></span>           | <span data-ttu-id="39e71-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39e71-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="39e71-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-217">System-Flags</span></span>           | <span data-ttu-id="39e71-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39e71-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="39e71-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="39e71-219">Classes used in</span></span>        | [<span data-ttu-id="39e71-220">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="39e71-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39e71-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39e71-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39e71-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-222">Entry</span></span> | <span data-ttu-id="39e71-223">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="39e71-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="39e71-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="39e71-226">System-Only</span></span>            | <span data-ttu-id="39e71-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-227">False</span></span>                                                                   |
| <span data-ttu-id="39e71-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="39e71-228">Is-Single-Valued</span></span>       | <span data-ttu-id="39e71-229">True</span><span class="sxs-lookup"><span data-stu-id="39e71-229">True</span></span>                                                                    |
| <span data-ttu-id="39e71-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="39e71-230">Is Indexed</span></span>             | <span data-ttu-id="39e71-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-231">False</span></span>                                                                   |
| <span data-ttu-id="39e71-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="39e71-232">In Global Catalog</span></span>      | <span data-ttu-id="39e71-233">True</span><span class="sxs-lookup"><span data-stu-id="39e71-233">True</span></span>                                                                    |
| <span data-ttu-id="39e71-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="39e71-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="39e71-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="39e71-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="39e71-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39e71-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39e71-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-238">Search-Flags</span></span>           | <span data-ttu-id="39e71-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39e71-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="39e71-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-240">System-Flags</span></span>           | <span data-ttu-id="39e71-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39e71-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="39e71-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="39e71-242">Classes used in</span></span>        | [<span data-ttu-id="39e71-243">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="39e71-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39e71-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39e71-244">Windows Server 2012</span></span>



| <span data-ttu-id="39e71-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="39e71-245">Entry</span></span> | <span data-ttu-id="39e71-246">Значение</span><span class="sxs-lookup"><span data-stu-id="39e71-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="39e71-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="39e71-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39e71-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="39e71-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="39e71-249">System-Only</span></span>            | <span data-ttu-id="39e71-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-250">False</span></span>                                                                   |
| <span data-ttu-id="39e71-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="39e71-251">Is-Single-Valued</span></span>       | <span data-ttu-id="39e71-252">True</span><span class="sxs-lookup"><span data-stu-id="39e71-252">True</span></span>                                                                    |
| <span data-ttu-id="39e71-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="39e71-253">Is Indexed</span></span>             | <span data-ttu-id="39e71-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="39e71-254">False</span></span>                                                                   |
| <span data-ttu-id="39e71-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="39e71-255">In Global Catalog</span></span>      | <span data-ttu-id="39e71-256">True</span><span class="sxs-lookup"><span data-stu-id="39e71-256">True</span></span>                                                                    |
| <span data-ttu-id="39e71-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="39e71-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="39e71-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="39e71-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="39e71-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39e71-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39e71-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="39e71-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-261">Search-Flags</span></span>           | <span data-ttu-id="39e71-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39e71-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="39e71-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39e71-263">System-Flags</span></span>           | <span data-ttu-id="39e71-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39e71-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="39e71-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="39e71-265">Classes used in</span></span>        | [<span data-ttu-id="39e71-266">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="39e71-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





