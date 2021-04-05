---
title: CA — атрибут Certificate-DN
description: Полное различающееся имя из сертификата ЦС.
ms.assetid: 51d1a9f8-d3d7-4ac9-b029-fa66b6799820
ms.tgt_platform: multiple
keywords:
- CA — схема AD атрибута Certificate-DN
- Схема AD атрибута Кацертификатедн
topic_type:
- apiref
api_name:
- CA-Certificate-DN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f6dcdf7faf3bcb93bcb029a373e19faed68e91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072062"
---
# <a name="ca-certificate-dn-attribute"></a><span data-ttu-id="463fb-105">CA — атрибут Certificate-DN</span><span class="sxs-lookup"><span data-stu-id="463fb-105">CA-Certificate-DN attribute</span></span>

<span data-ttu-id="463fb-106">Полное различающееся имя из сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="463fb-106">Full distinguished name from the CA certificate.</span></span>



| <span data-ttu-id="463fb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-107">Entry</span></span> | <span data-ttu-id="463fb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="463fb-109">CN</span><span class="sxs-lookup"><span data-stu-id="463fb-109">CN</span></span>                | <span data-ttu-id="463fb-110">CA — certificate-DN</span><span class="sxs-lookup"><span data-stu-id="463fb-110">CA-Certificate-DN</span></span>                           |
| <span data-ttu-id="463fb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="463fb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="463fb-112">кацертификатедн</span><span class="sxs-lookup"><span data-stu-id="463fb-112">cACertificateDN</span></span>                             |
| <span data-ttu-id="463fb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="463fb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="463fb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="463fb-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="463fb-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="463fb-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="463fb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-116">Attribute-Id</span></span>      | <span data-ttu-id="463fb-117">1.2.840.113556.1.4.697</span><span class="sxs-lookup"><span data-stu-id="463fb-117">1.2.840.113556.1.4.697</span></span>                      |
| <span data-ttu-id="463fb-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="463fb-118">System-Id-Guid</span></span>    | <span data-ttu-id="463fb-119">963d2740-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="463fb-119">963d2740-48be-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="463fb-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="463fb-120">Syntax</span></span>            | [<span data-ttu-id="463fb-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="463fb-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="463fb-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="463fb-122">Implementations</span></span>

-   [<span data-ttu-id="463fb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="463fb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="463fb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="463fb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="463fb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="463fb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="463fb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="463fb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="463fb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="463fb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="463fb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="463fb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="463fb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="463fb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="463fb-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-130">Entry</span></span> | <span data-ttu-id="463fb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="463fb-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="463fb-134">System-Only</span></span>            | <span data-ttu-id="463fb-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="463fb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="463fb-137">True</span><span class="sxs-lookup"><span data-stu-id="463fb-137">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="463fb-138">Is Indexed</span></span>             | <span data-ttu-id="463fb-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="463fb-140">In Global Catalog</span></span>      | <span data-ttu-id="463fb-141">True</span><span class="sxs-lookup"><span data-stu-id="463fb-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="463fb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="463fb-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="463fb-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="463fb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="463fb-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="463fb-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-146">Search-Flags</span></span>           | <span data-ttu-id="463fb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="463fb-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-148">System-Flags</span></span>           | <span data-ttu-id="463fb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="463fb-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="463fb-150">Classes used in</span></span>        | [<span data-ttu-id="463fb-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="463fb-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="463fb-152">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="463fb-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="463fb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="463fb-153">Windows Server 2003</span></span>



| <span data-ttu-id="463fb-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-154">Entry</span></span> | <span data-ttu-id="463fb-155">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="463fb-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="463fb-158">System-Only</span></span>            | <span data-ttu-id="463fb-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="463fb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="463fb-161">True</span><span class="sxs-lookup"><span data-stu-id="463fb-161">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="463fb-162">Is Indexed</span></span>             | <span data-ttu-id="463fb-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="463fb-164">In Global Catalog</span></span>      | <span data-ttu-id="463fb-165">True</span><span class="sxs-lookup"><span data-stu-id="463fb-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="463fb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="463fb-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="463fb-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="463fb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="463fb-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="463fb-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-170">Search-Flags</span></span>           | <span data-ttu-id="463fb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="463fb-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-172">System-Flags</span></span>           | <span data-ttu-id="463fb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="463fb-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="463fb-174">Classes used in</span></span>        | [<span data-ttu-id="463fb-175">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="463fb-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="463fb-176">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="463fb-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="463fb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="463fb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="463fb-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-178">Entry</span></span> | <span data-ttu-id="463fb-179">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="463fb-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="463fb-182">System-Only</span></span>            | <span data-ttu-id="463fb-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="463fb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="463fb-185">True</span><span class="sxs-lookup"><span data-stu-id="463fb-185">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="463fb-186">Is Indexed</span></span>             | <span data-ttu-id="463fb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="463fb-188">In Global Catalog</span></span>      | <span data-ttu-id="463fb-189">True</span><span class="sxs-lookup"><span data-stu-id="463fb-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="463fb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="463fb-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="463fb-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="463fb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="463fb-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="463fb-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-194">Search-Flags</span></span>           | <span data-ttu-id="463fb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="463fb-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-196">System-Flags</span></span>           | <span data-ttu-id="463fb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="463fb-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="463fb-198">Classes used in</span></span>        | [<span data-ttu-id="463fb-199">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="463fb-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="463fb-200">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="463fb-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="463fb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="463fb-201">Windows Server 2008</span></span>



| <span data-ttu-id="463fb-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-202">Entry</span></span> | <span data-ttu-id="463fb-203">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="463fb-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="463fb-206">System-Only</span></span>            | <span data-ttu-id="463fb-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="463fb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="463fb-209">True</span><span class="sxs-lookup"><span data-stu-id="463fb-209">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="463fb-210">Is Indexed</span></span>             | <span data-ttu-id="463fb-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="463fb-212">In Global Catalog</span></span>      | <span data-ttu-id="463fb-213">True</span><span class="sxs-lookup"><span data-stu-id="463fb-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="463fb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="463fb-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="463fb-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="463fb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="463fb-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="463fb-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-218">Search-Flags</span></span>           | <span data-ttu-id="463fb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="463fb-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-220">System-Flags</span></span>           | <span data-ttu-id="463fb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="463fb-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="463fb-222">Classes used in</span></span>        | [<span data-ttu-id="463fb-223">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="463fb-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="463fb-224">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="463fb-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="463fb-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="463fb-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="463fb-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-226">Entry</span></span> | <span data-ttu-id="463fb-227">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="463fb-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="463fb-230">System-Only</span></span>            | <span data-ttu-id="463fb-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="463fb-232">Is-Single-Valued</span></span>       | <span data-ttu-id="463fb-233">True</span><span class="sxs-lookup"><span data-stu-id="463fb-233">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="463fb-234">Is Indexed</span></span>             | <span data-ttu-id="463fb-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="463fb-236">In Global Catalog</span></span>      | <span data-ttu-id="463fb-237">True</span><span class="sxs-lookup"><span data-stu-id="463fb-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="463fb-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="463fb-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="463fb-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="463fb-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="463fb-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="463fb-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-242">Search-Flags</span></span>           | <span data-ttu-id="463fb-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="463fb-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-244">System-Flags</span></span>           | <span data-ttu-id="463fb-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="463fb-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="463fb-246">Classes used in</span></span>        | [<span data-ttu-id="463fb-247">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="463fb-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="463fb-248">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="463fb-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="463fb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="463fb-249">Windows Server 2012</span></span>



| <span data-ttu-id="463fb-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="463fb-250">Entry</span></span> | <span data-ttu-id="463fb-251">Значение</span><span class="sxs-lookup"><span data-stu-id="463fb-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="463fb-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="463fb-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="463fb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="463fb-254">System-Only</span></span>            | <span data-ttu-id="463fb-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="463fb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="463fb-257">True</span><span class="sxs-lookup"><span data-stu-id="463fb-257">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="463fb-258">Is Indexed</span></span>             | <span data-ttu-id="463fb-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="463fb-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="463fb-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="463fb-260">In Global Catalog</span></span>      | <span data-ttu-id="463fb-261">True</span><span class="sxs-lookup"><span data-stu-id="463fb-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="463fb-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="463fb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="463fb-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="463fb-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="463fb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="463fb-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="463fb-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="463fb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-266">Search-Flags</span></span>           | <span data-ttu-id="463fb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="463fb-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="463fb-268">System-Flags</span></span>           | <span data-ttu-id="463fb-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="463fb-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="463fb-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="463fb-270">Classes used in</span></span>        | [<span data-ttu-id="463fb-271">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="463fb-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="463fb-272">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="463fb-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 





