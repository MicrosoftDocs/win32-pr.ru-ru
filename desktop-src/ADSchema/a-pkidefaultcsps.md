---
title: PKI — атрибут CSP по умолчанию
description: Список поставщиков служб шифрования для шаблона сертификата.
ms.assetid: 1291f909-919e-47ea-a5cf-69bc7e520c28
ms.tgt_platform: multiple
keywords:
- PKI — схема AD атрибута CSP по умолчанию
- Схема AD атрибута Пкидефаулткспс
topic_type:
- apiref
api_name:
- PKI-Default-CSPs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d572334c07c4ac88a4372dbfa4ac1b3bc714e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103892994"
---
# <a name="pki-default-csps-attribute"></a><span data-ttu-id="8e2c9-105">PKI — атрибут CSP по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8e2c9-105">PKI-Default-CSPs attribute</span></span>

<span data-ttu-id="8e2c9-106">Список поставщиков служб шифрования для шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-106">The list of cryptographic service providers for the certificate template.</span></span>



| <span data-ttu-id="8e2c9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-107">Entry</span></span> | <span data-ttu-id="8e2c9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8e2c9-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e2c9-109">CN</span></span>                | <span data-ttu-id="8e2c9-110">PKI-Default-CSP</span><span class="sxs-lookup"><span data-stu-id="8e2c9-110">PKI-Default-CSPs</span></span>                            |
| <span data-ttu-id="8e2c9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8e2c9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8e2c9-112">пкидефаулткспс</span><span class="sxs-lookup"><span data-stu-id="8e2c9-112">pKIDefaultCSPs</span></span>                              |
| <span data-ttu-id="8e2c9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8e2c9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8e2c9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8e2c9-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="8e2c9-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8e2c9-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8e2c9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-116">Attribute-Id</span></span>      | <span data-ttu-id="8e2c9-117">1.2.840.113556.1.4.1334</span><span class="sxs-lookup"><span data-stu-id="8e2c9-117">1.2.840.113556.1.4.1334</span></span>                     |
| <span data-ttu-id="8e2c9-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8e2c9-118">System-Id-Guid</span></span>    | <span data-ttu-id="8e2c9-119">1ef6336e-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="8e2c9-119">1ef6336e-3b9e-11d2-90cc-00c04fd91ab1</span></span>        |
| <span data-ttu-id="8e2c9-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e2c9-120">Syntax</span></span>            | [<span data-ttu-id="8e2c9-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8e2c9-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8e2c9-122">Implementations</span></span>

-   [<span data-ttu-id="8e2c9-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8e2c9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e2c9-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e2c9-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e2c9-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e2c9-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8e2c9-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e2c9-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8e2c9-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-130">Entry</span></span> | <span data-ttu-id="8e2c9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8e2c9-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e2c9-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e2c9-134">System-Only</span></span>            | <span data-ttu-id="8e2c9-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-135">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e2c9-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8e2c9-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-137">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e2c9-138">Is Indexed</span></span>             | <span data-ttu-id="8e2c9-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-139">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e2c9-140">In Global Catalog</span></span>      | <span data-ttu-id="8e2c9-141">True</span><span class="sxs-lookup"><span data-stu-id="8e2c9-141">True</span></span>                                                                    |
| <span data-ttu-id="8e2c9-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e2c9-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e2c9-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e2c9-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8e2c9-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e2c9-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e2c9-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-146">Search-Flags</span></span>           | <span data-ttu-id="8e2c9-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e2c9-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="8e2c9-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-148">System-Flags</span></span>           | <span data-ttu-id="8e2c9-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e2c9-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="8e2c9-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e2c9-150">Classes used in</span></span>        | [<span data-ttu-id="8e2c9-151">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8e2c9-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e2c9-152">Windows Server 2003</span></span>



| <span data-ttu-id="8e2c9-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-153">Entry</span></span> | <span data-ttu-id="8e2c9-154">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8e2c9-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e2c9-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e2c9-157">System-Only</span></span>            | <span data-ttu-id="8e2c9-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-158">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e2c9-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8e2c9-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-160">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e2c9-161">Is Indexed</span></span>             | <span data-ttu-id="8e2c9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-162">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e2c9-163">In Global Catalog</span></span>      | <span data-ttu-id="8e2c9-164">True</span><span class="sxs-lookup"><span data-stu-id="8e2c9-164">True</span></span>                                                                    |
| <span data-ttu-id="8e2c9-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e2c9-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e2c9-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e2c9-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8e2c9-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e2c9-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e2c9-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-169">Search-Flags</span></span>           | <span data-ttu-id="8e2c9-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e2c9-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="8e2c9-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-171">System-Flags</span></span>           | <span data-ttu-id="8e2c9-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e2c9-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="8e2c9-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e2c9-173">Classes used in</span></span>        | [<span data-ttu-id="8e2c9-174">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e2c9-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e2c9-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e2c9-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-176">Entry</span></span> | <span data-ttu-id="8e2c9-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8e2c9-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e2c9-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e2c9-180">System-Only</span></span>            | <span data-ttu-id="8e2c9-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-181">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e2c9-182">Is-Single-Valued</span></span>       | <span data-ttu-id="8e2c9-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-183">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e2c9-184">Is Indexed</span></span>             | <span data-ttu-id="8e2c9-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-185">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e2c9-186">In Global Catalog</span></span>      | <span data-ttu-id="8e2c9-187">True</span><span class="sxs-lookup"><span data-stu-id="8e2c9-187">True</span></span>                                                                    |
| <span data-ttu-id="8e2c9-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e2c9-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e2c9-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e2c9-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8e2c9-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e2c9-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e2c9-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-192">Search-Flags</span></span>           | <span data-ttu-id="8e2c9-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e2c9-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="8e2c9-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-194">System-Flags</span></span>           | <span data-ttu-id="8e2c9-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e2c9-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="8e2c9-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e2c9-196">Classes used in</span></span>        | [<span data-ttu-id="8e2c9-197">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e2c9-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e2c9-198">Windows Server 2008</span></span>



| <span data-ttu-id="8e2c9-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-199">Entry</span></span> | <span data-ttu-id="8e2c9-200">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8e2c9-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e2c9-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e2c9-203">System-Only</span></span>            | <span data-ttu-id="8e2c9-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-204">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e2c9-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8e2c9-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-206">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e2c9-207">Is Indexed</span></span>             | <span data-ttu-id="8e2c9-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-208">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e2c9-209">In Global Catalog</span></span>      | <span data-ttu-id="8e2c9-210">True</span><span class="sxs-lookup"><span data-stu-id="8e2c9-210">True</span></span>                                                                    |
| <span data-ttu-id="8e2c9-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e2c9-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e2c9-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e2c9-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8e2c9-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e2c9-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e2c9-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-215">Search-Flags</span></span>           | <span data-ttu-id="8e2c9-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e2c9-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="8e2c9-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-217">System-Flags</span></span>           | <span data-ttu-id="8e2c9-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e2c9-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="8e2c9-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e2c9-219">Classes used in</span></span>        | [<span data-ttu-id="8e2c9-220">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e2c9-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e2c9-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e2c9-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-222">Entry</span></span> | <span data-ttu-id="8e2c9-223">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8e2c9-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e2c9-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e2c9-226">System-Only</span></span>            | <span data-ttu-id="8e2c9-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-227">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e2c9-228">Is-Single-Valued</span></span>       | <span data-ttu-id="8e2c9-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-229">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e2c9-230">Is Indexed</span></span>             | <span data-ttu-id="8e2c9-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-231">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e2c9-232">In Global Catalog</span></span>      | <span data-ttu-id="8e2c9-233">True</span><span class="sxs-lookup"><span data-stu-id="8e2c9-233">True</span></span>                                                                    |
| <span data-ttu-id="8e2c9-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e2c9-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e2c9-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e2c9-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8e2c9-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e2c9-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e2c9-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-238">Search-Flags</span></span>           | <span data-ttu-id="8e2c9-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e2c9-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="8e2c9-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-240">System-Flags</span></span>           | <span data-ttu-id="8e2c9-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e2c9-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="8e2c9-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e2c9-242">Classes used in</span></span>        | [<span data-ttu-id="8e2c9-243">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e2c9-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e2c9-244">Windows Server 2012</span></span>



| <span data-ttu-id="8e2c9-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e2c9-245">Entry</span></span> | <span data-ttu-id="8e2c9-246">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2c9-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8e2c9-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e2c9-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e2c9-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8e2c9-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e2c9-249">System-Only</span></span>            | <span data-ttu-id="8e2c9-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-250">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e2c9-251">Is-Single-Valued</span></span>       | <span data-ttu-id="8e2c9-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-252">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e2c9-253">Is Indexed</span></span>             | <span data-ttu-id="8e2c9-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e2c9-254">False</span></span>                                                                   |
| <span data-ttu-id="8e2c9-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e2c9-255">In Global Catalog</span></span>      | <span data-ttu-id="8e2c9-256">True</span><span class="sxs-lookup"><span data-stu-id="8e2c9-256">True</span></span>                                                                    |
| <span data-ttu-id="8e2c9-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e2c9-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e2c9-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e2c9-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8e2c9-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e2c9-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e2c9-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8e2c9-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-261">Search-Flags</span></span>           | <span data-ttu-id="8e2c9-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e2c9-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="8e2c9-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e2c9-263">System-Flags</span></span>           | <span data-ttu-id="8e2c9-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e2c9-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="8e2c9-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e2c9-265">Classes used in</span></span>        | [<span data-ttu-id="8e2c9-266">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="8e2c9-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





