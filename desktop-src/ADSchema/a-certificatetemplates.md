---
title: Атрибут Certificate-Templates
description: Содержит сведения о сертификате, выданном сервером сертификатов.
ms.assetid: 1434b8f8-15d9-4dca-bb7b-26c97e269b01
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Certificate-Templates
- Схема AD атрибута Цертификатетемплатес
topic_type:
- apiref
api_name:
- Certificate-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20701d4b904a21af26ac86fdfa90eff13cddf22
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805069"
---
# <a name="certificate-templates-attribute"></a><span data-ttu-id="29c8f-105">Атрибут Certificate-Templates</span><span class="sxs-lookup"><span data-stu-id="29c8f-105">Certificate-Templates attribute</span></span>

<span data-ttu-id="29c8f-106">Содержит сведения о сертификате, выданном сервером сертификатов.</span><span class="sxs-lookup"><span data-stu-id="29c8f-106">Contains information for a certificate issued by a Certificate Server.</span></span>



| <span data-ttu-id="29c8f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-107">Entry</span></span> | <span data-ttu-id="29c8f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="29c8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="29c8f-109">CN</span></span>                | <span data-ttu-id="29c8f-110">Certificate-Templates</span><span class="sxs-lookup"><span data-stu-id="29c8f-110">Certificate-Templates</span></span>                       |
| <span data-ttu-id="29c8f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="29c8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="29c8f-112">цертификатетемплатес</span><span class="sxs-lookup"><span data-stu-id="29c8f-112">certificateTemplates</span></span>                        |
| <span data-ttu-id="29c8f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="29c8f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="29c8f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="29c8f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="29c8f-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="29c8f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="29c8f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-116">Attribute-Id</span></span>      | <span data-ttu-id="29c8f-117">1.2.840.113556.1.4.823</span><span class="sxs-lookup"><span data-stu-id="29c8f-117">1.2.840.113556.1.4.823</span></span>                      |
| <span data-ttu-id="29c8f-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="29c8f-118">System-Id-Guid</span></span>    | <span data-ttu-id="29c8f-119">2a39c5b1-8960-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="29c8f-119">2a39c5b1-8960-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="29c8f-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29c8f-120">Syntax</span></span>            | [<span data-ttu-id="29c8f-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="29c8f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="29c8f-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="29c8f-122">Implementations</span></span>

-   [<span data-ttu-id="29c8f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29c8f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29c8f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29c8f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29c8f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29c8f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29c8f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29c8f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29c8f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29c8f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29c8f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29c8f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29c8f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29c8f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="29c8f-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-130">Entry</span></span> | <span data-ttu-id="29c8f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c8f-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29c8f-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="29c8f-134">System-Only</span></span>            | <span data-ttu-id="29c8f-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29c8f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="29c8f-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-137">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29c8f-138">Is Indexed</span></span>             | <span data-ttu-id="29c8f-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29c8f-140">In Global Catalog</span></span>      | <span data-ttu-id="29c8f-141">True</span><span class="sxs-lookup"><span data-stu-id="29c8f-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="29c8f-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29c8f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="29c8f-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29c8f-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="29c8f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29c8f-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29c8f-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-146">Search-Flags</span></span>           | <span data-ttu-id="29c8f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29c8f-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-148">System-Flags</span></span>           | <span data-ttu-id="29c8f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29c8f-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29c8f-150">Classes used in</span></span>        | [<span data-ttu-id="29c8f-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="29c8f-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="29c8f-152">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="29c8f-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29c8f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29c8f-153">Windows Server 2003</span></span>



| <span data-ttu-id="29c8f-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-154">Entry</span></span> | <span data-ttu-id="29c8f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c8f-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29c8f-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="29c8f-158">System-Only</span></span>            | <span data-ttu-id="29c8f-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29c8f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="29c8f-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29c8f-162">Is Indexed</span></span>             | <span data-ttu-id="29c8f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29c8f-164">In Global Catalog</span></span>      | <span data-ttu-id="29c8f-165">True</span><span class="sxs-lookup"><span data-stu-id="29c8f-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="29c8f-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29c8f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="29c8f-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29c8f-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="29c8f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29c8f-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29c8f-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-170">Search-Flags</span></span>           | <span data-ttu-id="29c8f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29c8f-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-172">System-Flags</span></span>           | <span data-ttu-id="29c8f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29c8f-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29c8f-174">Classes used in</span></span>        | [<span data-ttu-id="29c8f-175">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="29c8f-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="29c8f-176">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="29c8f-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29c8f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29c8f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29c8f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-178">Entry</span></span> | <span data-ttu-id="29c8f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c8f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29c8f-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="29c8f-182">System-Only</span></span>            | <span data-ttu-id="29c8f-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29c8f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="29c8f-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-185">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29c8f-186">Is Indexed</span></span>             | <span data-ttu-id="29c8f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29c8f-188">In Global Catalog</span></span>      | <span data-ttu-id="29c8f-189">True</span><span class="sxs-lookup"><span data-stu-id="29c8f-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="29c8f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29c8f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="29c8f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29c8f-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="29c8f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29c8f-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29c8f-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-194">Search-Flags</span></span>           | <span data-ttu-id="29c8f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29c8f-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-196">System-Flags</span></span>           | <span data-ttu-id="29c8f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29c8f-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29c8f-198">Classes used in</span></span>        | [<span data-ttu-id="29c8f-199">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="29c8f-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="29c8f-200">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="29c8f-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29c8f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29c8f-201">Windows Server 2008</span></span>



| <span data-ttu-id="29c8f-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-202">Entry</span></span> | <span data-ttu-id="29c8f-203">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c8f-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29c8f-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="29c8f-206">System-Only</span></span>            | <span data-ttu-id="29c8f-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29c8f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="29c8f-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-209">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29c8f-210">Is Indexed</span></span>             | <span data-ttu-id="29c8f-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29c8f-212">In Global Catalog</span></span>      | <span data-ttu-id="29c8f-213">True</span><span class="sxs-lookup"><span data-stu-id="29c8f-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="29c8f-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29c8f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="29c8f-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29c8f-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="29c8f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29c8f-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29c8f-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-218">Search-Flags</span></span>           | <span data-ttu-id="29c8f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29c8f-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-220">System-Flags</span></span>           | <span data-ttu-id="29c8f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29c8f-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29c8f-222">Classes used in</span></span>        | [<span data-ttu-id="29c8f-223">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="29c8f-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="29c8f-224">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="29c8f-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29c8f-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29c8f-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29c8f-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-226">Entry</span></span> | <span data-ttu-id="29c8f-227">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c8f-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29c8f-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="29c8f-230">System-Only</span></span>            | <span data-ttu-id="29c8f-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29c8f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="29c8f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-233">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29c8f-234">Is Indexed</span></span>             | <span data-ttu-id="29c8f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29c8f-236">In Global Catalog</span></span>      | <span data-ttu-id="29c8f-237">True</span><span class="sxs-lookup"><span data-stu-id="29c8f-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="29c8f-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29c8f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="29c8f-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29c8f-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="29c8f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29c8f-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29c8f-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-242">Search-Flags</span></span>           | <span data-ttu-id="29c8f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29c8f-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-244">System-Flags</span></span>           | <span data-ttu-id="29c8f-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29c8f-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29c8f-246">Classes used in</span></span>        | [<span data-ttu-id="29c8f-247">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="29c8f-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="29c8f-248">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="29c8f-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29c8f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29c8f-249">Windows Server 2012</span></span>



| <span data-ttu-id="29c8f-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="29c8f-250">Entry</span></span> | <span data-ttu-id="29c8f-251">Значение</span><span class="sxs-lookup"><span data-stu-id="29c8f-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c8f-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29c8f-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29c8f-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="29c8f-254">System-Only</span></span>            | <span data-ttu-id="29c8f-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29c8f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="29c8f-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-257">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29c8f-258">Is Indexed</span></span>             | <span data-ttu-id="29c8f-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="29c8f-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="29c8f-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29c8f-260">In Global Catalog</span></span>      | <span data-ttu-id="29c8f-261">True</span><span class="sxs-lookup"><span data-stu-id="29c8f-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="29c8f-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29c8f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="29c8f-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29c8f-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="29c8f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29c8f-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29c8f-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="29c8f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-266">Search-Flags</span></span>           | <span data-ttu-id="29c8f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29c8f-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29c8f-268">System-Flags</span></span>           | <span data-ttu-id="29c8f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29c8f-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="29c8f-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29c8f-270">Classes used in</span></span>        | [<span data-ttu-id="29c8f-271">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="29c8f-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="29c8f-272">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="29c8f-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 





