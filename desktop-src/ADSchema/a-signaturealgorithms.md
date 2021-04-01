---
title: Атрибут Signature-Algorithms
description: Этот атрибут указывает тип алгоритма, который должен использоваться для декодирования цифровой подписи в процессе проверки подлинности.
ms.assetid: f602a009-6823-42e7-b5e4-fb433535b4cc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Signature-Algorithms
- Схема AD атрибута Сигнатуреалгорисмс
topic_type:
- apiref
api_name:
- Signature-Algorithms
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6487155ed8d13735a8201a41c9d1d5b087bb3711
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262260"
---
# <a name="signature-algorithms-attribute"></a><span data-ttu-id="927c3-105">Атрибут Signature-Algorithms</span><span class="sxs-lookup"><span data-stu-id="927c3-105">Signature-Algorithms attribute</span></span>

<span data-ttu-id="927c3-106">Этот атрибут указывает тип алгоритма, который должен использоваться для декодирования цифровой подписи в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="927c3-106">This attribute indicates the type of algorithm that must be used to decode a digital signature during the authentication process.</span></span>



| <span data-ttu-id="927c3-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-107">Entry</span></span> | <span data-ttu-id="927c3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="927c3-109">CN</span><span class="sxs-lookup"><span data-stu-id="927c3-109">CN</span></span>                | <span data-ttu-id="927c3-110">Signature-Algorithms</span><span class="sxs-lookup"><span data-stu-id="927c3-110">Signature-Algorithms</span></span>                        |
| <span data-ttu-id="927c3-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="927c3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="927c3-112">сигнатуреалгорисмс</span><span class="sxs-lookup"><span data-stu-id="927c3-112">signatureAlgorithms</span></span>                         |
| <span data-ttu-id="927c3-113">Размер</span><span class="sxs-lookup"><span data-stu-id="927c3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="927c3-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="927c3-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="927c3-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="927c3-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="927c3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-116">Attribute-Id</span></span>      | <span data-ttu-id="927c3-117">1.2.840.113556.1.4.824</span><span class="sxs-lookup"><span data-stu-id="927c3-117">1.2.840.113556.1.4.824</span></span>                      |
| <span data-ttu-id="927c3-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="927c3-118">System-Id-Guid</span></span>    | <span data-ttu-id="927c3-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="927c3-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="927c3-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="927c3-120">Syntax</span></span>            | [<span data-ttu-id="927c3-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="927c3-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="927c3-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="927c3-122">Implementations</span></span>

-   [<span data-ttu-id="927c3-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="927c3-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="927c3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="927c3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="927c3-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="927c3-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="927c3-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="927c3-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="927c3-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="927c3-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="927c3-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="927c3-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="927c3-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="927c3-129">Windows 2000 Server</span></span>



| <span data-ttu-id="927c3-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-130">Entry</span></span> | <span data-ttu-id="927c3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927c3-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="927c3-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="927c3-134">System-Only</span></span>            | <span data-ttu-id="927c3-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="927c3-136">Is-Single-Valued</span></span>       | <span data-ttu-id="927c3-137">True</span><span class="sxs-lookup"><span data-stu-id="927c3-137">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="927c3-138">Is Indexed</span></span>             | <span data-ttu-id="927c3-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="927c3-140">In Global Catalog</span></span>      | <span data-ttu-id="927c3-141">True</span><span class="sxs-lookup"><span data-stu-id="927c3-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="927c3-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="927c3-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="927c3-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="927c3-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927c3-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927c3-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-146">Search-Flags</span></span>           | <span data-ttu-id="927c3-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927c3-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-148">System-Flags</span></span>           | <span data-ttu-id="927c3-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927c3-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="927c3-150">Classes used in</span></span>        | [<span data-ttu-id="927c3-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="927c3-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="927c3-152">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="927c3-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="927c3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="927c3-153">Windows Server 2003</span></span>



| <span data-ttu-id="927c3-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-154">Entry</span></span> | <span data-ttu-id="927c3-155">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927c3-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="927c3-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="927c3-158">System-Only</span></span>            | <span data-ttu-id="927c3-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="927c3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="927c3-161">True</span><span class="sxs-lookup"><span data-stu-id="927c3-161">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="927c3-162">Is Indexed</span></span>             | <span data-ttu-id="927c3-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="927c3-164">In Global Catalog</span></span>      | <span data-ttu-id="927c3-165">True</span><span class="sxs-lookup"><span data-stu-id="927c3-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="927c3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="927c3-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="927c3-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="927c3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927c3-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927c3-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-170">Search-Flags</span></span>           | <span data-ttu-id="927c3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927c3-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-172">System-Flags</span></span>           | <span data-ttu-id="927c3-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927c3-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="927c3-174">Classes used in</span></span>        | [<span data-ttu-id="927c3-175">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="927c3-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="927c3-176">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="927c3-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="927c3-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="927c3-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="927c3-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-178">Entry</span></span> | <span data-ttu-id="927c3-179">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927c3-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="927c3-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="927c3-182">System-Only</span></span>            | <span data-ttu-id="927c3-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="927c3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="927c3-185">True</span><span class="sxs-lookup"><span data-stu-id="927c3-185">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="927c3-186">Is Indexed</span></span>             | <span data-ttu-id="927c3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="927c3-188">In Global Catalog</span></span>      | <span data-ttu-id="927c3-189">True</span><span class="sxs-lookup"><span data-stu-id="927c3-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="927c3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="927c3-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="927c3-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="927c3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927c3-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927c3-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-194">Search-Flags</span></span>           | <span data-ttu-id="927c3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927c3-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-196">System-Flags</span></span>           | <span data-ttu-id="927c3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927c3-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="927c3-198">Classes used in</span></span>        | [<span data-ttu-id="927c3-199">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="927c3-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="927c3-200">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="927c3-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="927c3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="927c3-201">Windows Server 2008</span></span>



| <span data-ttu-id="927c3-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-202">Entry</span></span> | <span data-ttu-id="927c3-203">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927c3-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="927c3-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="927c3-206">System-Only</span></span>            | <span data-ttu-id="927c3-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="927c3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="927c3-209">True</span><span class="sxs-lookup"><span data-stu-id="927c3-209">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="927c3-210">Is Indexed</span></span>             | <span data-ttu-id="927c3-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="927c3-212">In Global Catalog</span></span>      | <span data-ttu-id="927c3-213">True</span><span class="sxs-lookup"><span data-stu-id="927c3-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="927c3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="927c3-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="927c3-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="927c3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927c3-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927c3-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-218">Search-Flags</span></span>           | <span data-ttu-id="927c3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927c3-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-220">System-Flags</span></span>           | <span data-ttu-id="927c3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927c3-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="927c3-222">Classes used in</span></span>        | [<span data-ttu-id="927c3-223">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="927c3-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="927c3-224">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="927c3-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="927c3-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="927c3-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="927c3-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-226">Entry</span></span> | <span data-ttu-id="927c3-227">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927c3-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="927c3-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="927c3-230">System-Only</span></span>            | <span data-ttu-id="927c3-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="927c3-232">Is-Single-Valued</span></span>       | <span data-ttu-id="927c3-233">True</span><span class="sxs-lookup"><span data-stu-id="927c3-233">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="927c3-234">Is Indexed</span></span>             | <span data-ttu-id="927c3-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="927c3-236">In Global Catalog</span></span>      | <span data-ttu-id="927c3-237">True</span><span class="sxs-lookup"><span data-stu-id="927c3-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="927c3-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="927c3-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="927c3-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="927c3-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927c3-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927c3-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-242">Search-Flags</span></span>           | <span data-ttu-id="927c3-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927c3-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-244">System-Flags</span></span>           | <span data-ttu-id="927c3-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927c3-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="927c3-246">Classes used in</span></span>        | [<span data-ttu-id="927c3-247">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="927c3-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="927c3-248">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="927c3-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="927c3-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="927c3-249">Windows Server 2012</span></span>



| <span data-ttu-id="927c3-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="927c3-250">Entry</span></span> | <span data-ttu-id="927c3-251">Значение</span><span class="sxs-lookup"><span data-stu-id="927c3-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927c3-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="927c3-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927c3-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="927c3-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="927c3-254">System-Only</span></span>            | <span data-ttu-id="927c3-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="927c3-256">Is-Single-Valued</span></span>       | <span data-ttu-id="927c3-257">True</span><span class="sxs-lookup"><span data-stu-id="927c3-257">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="927c3-258">Is Indexed</span></span>             | <span data-ttu-id="927c3-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="927c3-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="927c3-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="927c3-260">In Global Catalog</span></span>      | <span data-ttu-id="927c3-261">True</span><span class="sxs-lookup"><span data-stu-id="927c3-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="927c3-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="927c3-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="927c3-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="927c3-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="927c3-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927c3-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927c3-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="927c3-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-266">Search-Flags</span></span>           | <span data-ttu-id="927c3-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927c3-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927c3-268">System-Flags</span></span>           | <span data-ttu-id="927c3-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927c3-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="927c3-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="927c3-270">Classes used in</span></span>        | [<span data-ttu-id="927c3-271">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="927c3-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="927c3-272">**PKI — регистрация — служба**</span><span class="sxs-lookup"><span data-stu-id="927c3-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 





