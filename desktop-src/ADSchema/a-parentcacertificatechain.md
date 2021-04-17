---
title: Атрибут "родители — CA — сертификат-цепочка"
description: Сертификат X. 509v3 в кодировке DER для родительского центра сертификации.
ms.assetid: 37e04c7b-5350-4e48-b3fd-22f97959d26a
ms.tgt_platform: multiple
keywords:
- Родитель-CA — схема AD атрибута цепочки сертификатов
- Схема AD атрибута Паренткацертификатечаин
topic_type:
- apiref
api_name:
- Parent-CA-Certificate-Chain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f27bacb77fb7ab3f1ae712920dace7cb525efc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493731"
---
# <a name="parent-ca-certificate-chain-attribute"></a><span data-ttu-id="30ceb-105">Атрибут "родители — CA — сертификат-цепочка"</span><span class="sxs-lookup"><span data-stu-id="30ceb-105">Parent-CA-Certificate-Chain attribute</span></span>

<span data-ttu-id="30ceb-106">Сертификат X. 509v3 в кодировке DER для родительского центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="30ceb-106">DER-encoded X.509v3 certificate for the parent certification authority.</span></span>



| <span data-ttu-id="30ceb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-107">Entry</span></span> | <span data-ttu-id="30ceb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="30ceb-109">CN</span><span class="sxs-lookup"><span data-stu-id="30ceb-109">CN</span></span>                | <span data-ttu-id="30ceb-110">Родительский ЦС — цепочка сертификатов</span><span class="sxs-lookup"><span data-stu-id="30ceb-110">Parent-CA-Certificate-Chain</span></span>                           |
| <span data-ttu-id="30ceb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="30ceb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="30ceb-112">паренткацертификатечаин</span><span class="sxs-lookup"><span data-stu-id="30ceb-112">parentCACertificateChain</span></span>                              |
| <span data-ttu-id="30ceb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="30ceb-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="30ceb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="30ceb-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="30ceb-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="30ceb-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="30ceb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-116">Attribute-Id</span></span>      | <span data-ttu-id="30ceb-117">1.2.840.113556.1.4.685</span><span class="sxs-lookup"><span data-stu-id="30ceb-117">1.2.840.113556.1.4.685</span></span>                                |
| <span data-ttu-id="30ceb-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="30ceb-118">System-Id-Guid</span></span>    | <span data-ttu-id="30ceb-119">963d2733-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="30ceb-119">963d2733-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="30ceb-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30ceb-120">Syntax</span></span>            | [<span data-ttu-id="30ceb-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="30ceb-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="30ceb-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="30ceb-122">Implementations</span></span>

-   [<span data-ttu-id="30ceb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="30ceb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="30ceb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="30ceb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="30ceb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="30ceb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="30ceb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30ceb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30ceb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30ceb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30ceb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30ceb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="30ceb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30ceb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="30ceb-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-130">Entry</span></span> | <span data-ttu-id="30ceb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="30ceb-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ceb-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ceb-134">System-Only</span></span>            | <span data-ttu-id="30ceb-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-135">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ceb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="30ceb-137">True</span><span class="sxs-lookup"><span data-stu-id="30ceb-137">True</span></span>                                                                   |
| <span data-ttu-id="30ceb-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ceb-138">Is Indexed</span></span>             | <span data-ttu-id="30ceb-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-139">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ceb-140">In Global Catalog</span></span>      | <span data-ttu-id="30ceb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-141">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ceb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ceb-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ceb-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="30ceb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ceb-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ceb-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-146">Search-Flags</span></span>           | <span data-ttu-id="30ceb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ceb-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="30ceb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-148">System-Flags</span></span>           | <span data-ttu-id="30ceb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ceb-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="30ceb-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ceb-150">Classes used in</span></span>        | [<span data-ttu-id="30ceb-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="30ceb-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="30ceb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30ceb-152">Windows Server 2003</span></span>



| <span data-ttu-id="30ceb-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-153">Entry</span></span> | <span data-ttu-id="30ceb-154">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="30ceb-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ceb-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ceb-157">System-Only</span></span>            | <span data-ttu-id="30ceb-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-158">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ceb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="30ceb-160">True</span><span class="sxs-lookup"><span data-stu-id="30ceb-160">True</span></span>                                                                   |
| <span data-ttu-id="30ceb-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ceb-161">Is Indexed</span></span>             | <span data-ttu-id="30ceb-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-162">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ceb-163">In Global Catalog</span></span>      | <span data-ttu-id="30ceb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-164">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ceb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ceb-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ceb-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="30ceb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ceb-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ceb-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-169">Search-Flags</span></span>           | <span data-ttu-id="30ceb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ceb-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="30ceb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-171">System-Flags</span></span>           | <span data-ttu-id="30ceb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ceb-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="30ceb-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ceb-173">Classes used in</span></span>        | [<span data-ttu-id="30ceb-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="30ceb-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="30ceb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="30ceb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="30ceb-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-176">Entry</span></span> | <span data-ttu-id="30ceb-177">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="30ceb-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ceb-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ceb-180">System-Only</span></span>            | <span data-ttu-id="30ceb-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-181">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ceb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="30ceb-183">True</span><span class="sxs-lookup"><span data-stu-id="30ceb-183">True</span></span>                                                                   |
| <span data-ttu-id="30ceb-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ceb-184">Is Indexed</span></span>             | <span data-ttu-id="30ceb-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-185">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ceb-186">In Global Catalog</span></span>      | <span data-ttu-id="30ceb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-187">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ceb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ceb-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ceb-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="30ceb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ceb-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ceb-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-192">Search-Flags</span></span>           | <span data-ttu-id="30ceb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ceb-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="30ceb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-194">System-Flags</span></span>           | <span data-ttu-id="30ceb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ceb-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="30ceb-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ceb-196">Classes used in</span></span>        | [<span data-ttu-id="30ceb-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="30ceb-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="30ceb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30ceb-198">Windows Server 2008</span></span>



| <span data-ttu-id="30ceb-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-199">Entry</span></span> | <span data-ttu-id="30ceb-200">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="30ceb-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ceb-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ceb-203">System-Only</span></span>            | <span data-ttu-id="30ceb-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-204">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ceb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="30ceb-206">True</span><span class="sxs-lookup"><span data-stu-id="30ceb-206">True</span></span>                                                                   |
| <span data-ttu-id="30ceb-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ceb-207">Is Indexed</span></span>             | <span data-ttu-id="30ceb-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-208">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ceb-209">In Global Catalog</span></span>      | <span data-ttu-id="30ceb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-210">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ceb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ceb-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ceb-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="30ceb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ceb-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ceb-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-215">Search-Flags</span></span>           | <span data-ttu-id="30ceb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ceb-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="30ceb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-217">System-Flags</span></span>           | <span data-ttu-id="30ceb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ceb-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="30ceb-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ceb-219">Classes used in</span></span>        | [<span data-ttu-id="30ceb-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="30ceb-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30ceb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30ceb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30ceb-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-222">Entry</span></span> | <span data-ttu-id="30ceb-223">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="30ceb-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ceb-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ceb-226">System-Only</span></span>            | <span data-ttu-id="30ceb-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-227">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ceb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="30ceb-229">True</span><span class="sxs-lookup"><span data-stu-id="30ceb-229">True</span></span>                                                                   |
| <span data-ttu-id="30ceb-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ceb-230">Is Indexed</span></span>             | <span data-ttu-id="30ceb-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-231">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ceb-232">In Global Catalog</span></span>      | <span data-ttu-id="30ceb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-233">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ceb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ceb-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ceb-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="30ceb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ceb-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ceb-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-238">Search-Flags</span></span>           | <span data-ttu-id="30ceb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ceb-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="30ceb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-240">System-Flags</span></span>           | <span data-ttu-id="30ceb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ceb-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="30ceb-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ceb-242">Classes used in</span></span>        | [<span data-ttu-id="30ceb-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="30ceb-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30ceb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30ceb-244">Windows Server 2012</span></span>



| <span data-ttu-id="30ceb-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ceb-245">Entry</span></span> | <span data-ttu-id="30ceb-246">Значение</span><span class="sxs-lookup"><span data-stu-id="30ceb-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="30ceb-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ceb-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ceb-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="30ceb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ceb-249">System-Only</span></span>            | <span data-ttu-id="30ceb-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-250">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ceb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="30ceb-252">True</span><span class="sxs-lookup"><span data-stu-id="30ceb-252">True</span></span>                                                                   |
| <span data-ttu-id="30ceb-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ceb-253">Is Indexed</span></span>             | <span data-ttu-id="30ceb-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-254">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ceb-255">In Global Catalog</span></span>      | <span data-ttu-id="30ceb-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ceb-256">False</span></span>                                                                  |
| <span data-ttu-id="30ceb-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ceb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ceb-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ceb-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="30ceb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ceb-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ceb-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="30ceb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-261">Search-Flags</span></span>           | <span data-ttu-id="30ceb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ceb-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="30ceb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ceb-263">System-Flags</span></span>           | <span data-ttu-id="30ceb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ceb-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="30ceb-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ceb-265">Classes used in</span></span>        | [<span data-ttu-id="30ceb-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="30ceb-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





