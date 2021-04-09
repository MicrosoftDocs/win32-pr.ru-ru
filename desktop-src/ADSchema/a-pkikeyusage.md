---
title: PKI — атрибут использования ключа
description: Расширение использования ключа для шаблона сертификата.
ms.assetid: 9b3bb28e-7519-4911-9777-f9612bff2d51
ms.tgt_platform: multiple
keywords:
- PKI — схема AD атрибута использования ключа
- Схема AD атрибута Пкикэйусаже
topic_type:
- apiref
api_name:
- PKI-Key-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08c5c5b72091060fb475f3becba4f230293c875
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893314"
---
# <a name="pki-key-usage-attribute"></a><span data-ttu-id="699c5-105">PKI — атрибут использования ключа</span><span class="sxs-lookup"><span data-stu-id="699c5-105">PKI-Key-Usage attribute</span></span>

<span data-ttu-id="699c5-106">Расширение использования ключа для шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="699c5-106">The key usage extension for the certificate template.</span></span>



| <span data-ttu-id="699c5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-107">Entry</span></span> | <span data-ttu-id="699c5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="699c5-109">CN</span><span class="sxs-lookup"><span data-stu-id="699c5-109">CN</span></span>                | <span data-ttu-id="699c5-110">PKI — использование ключа</span><span class="sxs-lookup"><span data-stu-id="699c5-110">PKI-Key-Usage</span></span>                                         |
| <span data-ttu-id="699c5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="699c5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="699c5-112">пкикэйусаже</span><span class="sxs-lookup"><span data-stu-id="699c5-112">pKIKeyUsage</span></span>                                           |
| <span data-ttu-id="699c5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="699c5-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="699c5-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="699c5-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="699c5-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="699c5-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="699c5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-116">Attribute-Id</span></span>      | <span data-ttu-id="699c5-117">1.2.840.113556.1.4.1328</span><span class="sxs-lookup"><span data-stu-id="699c5-117">1.2.840.113556.1.4.1328</span></span>                               |
| <span data-ttu-id="699c5-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="699c5-118">System-Id-Guid</span></span>    | <span data-ttu-id="699c5-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="699c5-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="699c5-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="699c5-120">Syntax</span></span>            | [<span data-ttu-id="699c5-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="699c5-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="699c5-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="699c5-122">Implementations</span></span>

-   [<span data-ttu-id="699c5-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="699c5-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="699c5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="699c5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="699c5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="699c5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="699c5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="699c5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="699c5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="699c5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="699c5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="699c5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="699c5-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="699c5-129">Windows 2000 Server</span></span>



| <span data-ttu-id="699c5-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-130">Entry</span></span> | <span data-ttu-id="699c5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="699c5-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c5-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c5-134">System-Only</span></span>            | <span data-ttu-id="699c5-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-135">False</span></span>                                                                   |
| <span data-ttu-id="699c5-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="699c5-137">True</span><span class="sxs-lookup"><span data-stu-id="699c5-137">True</span></span>                                                                    |
| <span data-ttu-id="699c5-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c5-138">Is Indexed</span></span>             | <span data-ttu-id="699c5-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-139">False</span></span>                                                                   |
| <span data-ttu-id="699c5-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c5-140">In Global Catalog</span></span>      | <span data-ttu-id="699c5-141">True</span><span class="sxs-lookup"><span data-stu-id="699c5-141">True</span></span>                                                                    |
| <span data-ttu-id="699c5-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c5-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c5-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="699c5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c5-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c5-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-146">Search-Flags</span></span>           | <span data-ttu-id="699c5-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c5-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="699c5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-148">System-Flags</span></span>           | <span data-ttu-id="699c5-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c5-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="699c5-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c5-150">Classes used in</span></span>        | [<span data-ttu-id="699c5-151">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="699c5-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="699c5-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="699c5-152">Windows Server 2003</span></span>



| <span data-ttu-id="699c5-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-153">Entry</span></span> | <span data-ttu-id="699c5-154">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="699c5-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c5-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c5-157">System-Only</span></span>            | <span data-ttu-id="699c5-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-158">False</span></span>                                                                   |
| <span data-ttu-id="699c5-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c5-159">Is-Single-Valued</span></span>       | <span data-ttu-id="699c5-160">True</span><span class="sxs-lookup"><span data-stu-id="699c5-160">True</span></span>                                                                    |
| <span data-ttu-id="699c5-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c5-161">Is Indexed</span></span>             | <span data-ttu-id="699c5-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-162">False</span></span>                                                                   |
| <span data-ttu-id="699c5-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c5-163">In Global Catalog</span></span>      | <span data-ttu-id="699c5-164">True</span><span class="sxs-lookup"><span data-stu-id="699c5-164">True</span></span>                                                                    |
| <span data-ttu-id="699c5-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c5-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c5-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c5-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="699c5-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c5-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c5-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-169">Search-Flags</span></span>           | <span data-ttu-id="699c5-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c5-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="699c5-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-171">System-Flags</span></span>           | <span data-ttu-id="699c5-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c5-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="699c5-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c5-173">Classes used in</span></span>        | [<span data-ttu-id="699c5-174">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="699c5-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="699c5-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="699c5-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="699c5-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-176">Entry</span></span> | <span data-ttu-id="699c5-177">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="699c5-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c5-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c5-180">System-Only</span></span>            | <span data-ttu-id="699c5-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-181">False</span></span>                                                                   |
| <span data-ttu-id="699c5-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c5-182">Is-Single-Valued</span></span>       | <span data-ttu-id="699c5-183">True</span><span class="sxs-lookup"><span data-stu-id="699c5-183">True</span></span>                                                                    |
| <span data-ttu-id="699c5-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c5-184">Is Indexed</span></span>             | <span data-ttu-id="699c5-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-185">False</span></span>                                                                   |
| <span data-ttu-id="699c5-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c5-186">In Global Catalog</span></span>      | <span data-ttu-id="699c5-187">True</span><span class="sxs-lookup"><span data-stu-id="699c5-187">True</span></span>                                                                    |
| <span data-ttu-id="699c5-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c5-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c5-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c5-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="699c5-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c5-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c5-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-192">Search-Flags</span></span>           | <span data-ttu-id="699c5-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c5-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="699c5-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-194">System-Flags</span></span>           | <span data-ttu-id="699c5-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c5-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="699c5-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c5-196">Classes used in</span></span>        | [<span data-ttu-id="699c5-197">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="699c5-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="699c5-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="699c5-198">Windows Server 2008</span></span>



| <span data-ttu-id="699c5-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-199">Entry</span></span> | <span data-ttu-id="699c5-200">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="699c5-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c5-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c5-203">System-Only</span></span>            | <span data-ttu-id="699c5-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-204">False</span></span>                                                                   |
| <span data-ttu-id="699c5-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c5-205">Is-Single-Valued</span></span>       | <span data-ttu-id="699c5-206">True</span><span class="sxs-lookup"><span data-stu-id="699c5-206">True</span></span>                                                                    |
| <span data-ttu-id="699c5-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c5-207">Is Indexed</span></span>             | <span data-ttu-id="699c5-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-208">False</span></span>                                                                   |
| <span data-ttu-id="699c5-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c5-209">In Global Catalog</span></span>      | <span data-ttu-id="699c5-210">True</span><span class="sxs-lookup"><span data-stu-id="699c5-210">True</span></span>                                                                    |
| <span data-ttu-id="699c5-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c5-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c5-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c5-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="699c5-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c5-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c5-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-215">Search-Flags</span></span>           | <span data-ttu-id="699c5-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c5-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="699c5-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-217">System-Flags</span></span>           | <span data-ttu-id="699c5-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c5-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="699c5-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c5-219">Classes used in</span></span>        | [<span data-ttu-id="699c5-220">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="699c5-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="699c5-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="699c5-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="699c5-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-222">Entry</span></span> | <span data-ttu-id="699c5-223">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="699c5-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c5-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c5-226">System-Only</span></span>            | <span data-ttu-id="699c5-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-227">False</span></span>                                                                   |
| <span data-ttu-id="699c5-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c5-228">Is-Single-Valued</span></span>       | <span data-ttu-id="699c5-229">True</span><span class="sxs-lookup"><span data-stu-id="699c5-229">True</span></span>                                                                    |
| <span data-ttu-id="699c5-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c5-230">Is Indexed</span></span>             | <span data-ttu-id="699c5-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-231">False</span></span>                                                                   |
| <span data-ttu-id="699c5-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c5-232">In Global Catalog</span></span>      | <span data-ttu-id="699c5-233">True</span><span class="sxs-lookup"><span data-stu-id="699c5-233">True</span></span>                                                                    |
| <span data-ttu-id="699c5-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c5-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c5-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c5-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="699c5-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c5-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c5-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-238">Search-Flags</span></span>           | <span data-ttu-id="699c5-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c5-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="699c5-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-240">System-Flags</span></span>           | <span data-ttu-id="699c5-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c5-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="699c5-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c5-242">Classes used in</span></span>        | [<span data-ttu-id="699c5-243">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="699c5-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="699c5-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="699c5-244">Windows Server 2012</span></span>



| <span data-ttu-id="699c5-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c5-245">Entry</span></span> | <span data-ttu-id="699c5-246">Значение</span><span class="sxs-lookup"><span data-stu-id="699c5-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="699c5-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c5-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c5-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="699c5-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c5-249">System-Only</span></span>            | <span data-ttu-id="699c5-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-250">False</span></span>                                                                   |
| <span data-ttu-id="699c5-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c5-251">Is-Single-Valued</span></span>       | <span data-ttu-id="699c5-252">True</span><span class="sxs-lookup"><span data-stu-id="699c5-252">True</span></span>                                                                    |
| <span data-ttu-id="699c5-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c5-253">Is Indexed</span></span>             | <span data-ttu-id="699c5-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c5-254">False</span></span>                                                                   |
| <span data-ttu-id="699c5-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c5-255">In Global Catalog</span></span>      | <span data-ttu-id="699c5-256">True</span><span class="sxs-lookup"><span data-stu-id="699c5-256">True</span></span>                                                                    |
| <span data-ttu-id="699c5-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c5-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c5-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c5-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="699c5-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c5-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c5-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="699c5-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-261">Search-Flags</span></span>           | <span data-ttu-id="699c5-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c5-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="699c5-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c5-263">System-Flags</span></span>           | <span data-ttu-id="699c5-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c5-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="699c5-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c5-265">Classes used in</span></span>        | [<span data-ttu-id="699c5-266">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="699c5-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





