---
title: Атрибут Pending — CA-Certificates
description: Сертификаты, которые скоро вступят в силу для этого центра сертификации.
ms.assetid: ec803ff6-3408-4361-84ef-33c47a96e66a
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Pending — CA-Certificates
- Схема AD атрибута Пендингкацертификатес
topic_type:
- apiref
api_name:
- Pending-CA-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1990d336c8cfb8efa0eefd1bfd9c1ccf3f8fa93f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804577"
---
# <a name="pending-ca-certificates-attribute"></a><span data-ttu-id="3ac1d-105">Атрибут Pending — CA-Certificates</span><span class="sxs-lookup"><span data-stu-id="3ac1d-105">Pending-CA-Certificates attribute</span></span>

<span data-ttu-id="3ac1d-106">Сертификаты, которые скоро вступят в силу для этого центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-106">The certificates that are about to become effective for this certification authority.</span></span>



| <span data-ttu-id="3ac1d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-107">Entry</span></span> | <span data-ttu-id="3ac1d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3ac1d-109">CN</span><span class="sxs-lookup"><span data-stu-id="3ac1d-109">CN</span></span>                | <span data-ttu-id="3ac1d-110">Ожидающие — CA — сертификаты</span><span class="sxs-lookup"><span data-stu-id="3ac1d-110">Pending-CA-Certificates</span></span>                               |
| <span data-ttu-id="3ac1d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3ac1d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3ac1d-112">пендингкацертификатес</span><span class="sxs-lookup"><span data-stu-id="3ac1d-112">pendingCACertificates</span></span>                                 |
| <span data-ttu-id="3ac1d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3ac1d-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="3ac1d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3ac1d-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="3ac1d-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3ac1d-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="3ac1d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-116">Attribute-Id</span></span>      | <span data-ttu-id="3ac1d-117">1.2.840.113556.1.4.693</span><span class="sxs-lookup"><span data-stu-id="3ac1d-117">1.2.840.113556.1.4.693</span></span>                                |
| <span data-ttu-id="3ac1d-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3ac1d-118">System-Id-Guid</span></span>    | <span data-ttu-id="3ac1d-119">963d273c-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3ac1d-119">963d273c-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="3ac1d-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ac1d-120">Syntax</span></span>            | [<span data-ttu-id="3ac1d-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3ac1d-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3ac1d-122">Implementations</span></span>

-   [<span data-ttu-id="3ac1d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3ac1d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3ac1d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3ac1d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3ac1d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3ac1d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3ac1d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3ac1d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3ac1d-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-130">Entry</span></span> | <span data-ttu-id="3ac1d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ac1d-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3ac1d-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ac1d-134">System-Only</span></span>            | <span data-ttu-id="3ac1d-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-135">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3ac1d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3ac1d-137">True</span><span class="sxs-lookup"><span data-stu-id="3ac1d-137">True</span></span>                                                                   |
| <span data-ttu-id="3ac1d-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3ac1d-138">Is Indexed</span></span>             | <span data-ttu-id="3ac1d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-139">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3ac1d-140">In Global Catalog</span></span>      | <span data-ttu-id="3ac1d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-141">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3ac1d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ac1d-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3ac1d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ac1d-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ac1d-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-146">Search-Flags</span></span>           | <span data-ttu-id="3ac1d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ac1d-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="3ac1d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-148">System-Flags</span></span>           | <span data-ttu-id="3ac1d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ac1d-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="3ac1d-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3ac1d-150">Classes used in</span></span>        | [<span data-ttu-id="3ac1d-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3ac1d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ac1d-152">Windows Server 2003</span></span>



| <span data-ttu-id="3ac1d-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-153">Entry</span></span> | <span data-ttu-id="3ac1d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ac1d-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3ac1d-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ac1d-157">System-Only</span></span>            | <span data-ttu-id="3ac1d-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-158">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3ac1d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="3ac1d-160">True</span><span class="sxs-lookup"><span data-stu-id="3ac1d-160">True</span></span>                                                                   |
| <span data-ttu-id="3ac1d-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3ac1d-161">Is Indexed</span></span>             | <span data-ttu-id="3ac1d-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-162">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3ac1d-163">In Global Catalog</span></span>      | <span data-ttu-id="3ac1d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-164">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3ac1d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ac1d-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3ac1d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ac1d-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ac1d-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-169">Search-Flags</span></span>           | <span data-ttu-id="3ac1d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ac1d-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="3ac1d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-171">System-Flags</span></span>           | <span data-ttu-id="3ac1d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ac1d-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="3ac1d-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3ac1d-173">Classes used in</span></span>        | [<span data-ttu-id="3ac1d-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3ac1d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3ac1d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3ac1d-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-176">Entry</span></span> | <span data-ttu-id="3ac1d-177">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ac1d-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3ac1d-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ac1d-180">System-Only</span></span>            | <span data-ttu-id="3ac1d-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-181">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3ac1d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="3ac1d-183">True</span><span class="sxs-lookup"><span data-stu-id="3ac1d-183">True</span></span>                                                                   |
| <span data-ttu-id="3ac1d-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3ac1d-184">Is Indexed</span></span>             | <span data-ttu-id="3ac1d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-185">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3ac1d-186">In Global Catalog</span></span>      | <span data-ttu-id="3ac1d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-187">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3ac1d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ac1d-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3ac1d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ac1d-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ac1d-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-192">Search-Flags</span></span>           | <span data-ttu-id="3ac1d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ac1d-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="3ac1d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-194">System-Flags</span></span>           | <span data-ttu-id="3ac1d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ac1d-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="3ac1d-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3ac1d-196">Classes used in</span></span>        | [<span data-ttu-id="3ac1d-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3ac1d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ac1d-198">Windows Server 2008</span></span>



| <span data-ttu-id="3ac1d-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-199">Entry</span></span> | <span data-ttu-id="3ac1d-200">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ac1d-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3ac1d-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ac1d-203">System-Only</span></span>            | <span data-ttu-id="3ac1d-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-204">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3ac1d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="3ac1d-206">True</span><span class="sxs-lookup"><span data-stu-id="3ac1d-206">True</span></span>                                                                   |
| <span data-ttu-id="3ac1d-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3ac1d-207">Is Indexed</span></span>             | <span data-ttu-id="3ac1d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-208">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3ac1d-209">In Global Catalog</span></span>      | <span data-ttu-id="3ac1d-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-210">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3ac1d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ac1d-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3ac1d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ac1d-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ac1d-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-215">Search-Flags</span></span>           | <span data-ttu-id="3ac1d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ac1d-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="3ac1d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-217">System-Flags</span></span>           | <span data-ttu-id="3ac1d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ac1d-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="3ac1d-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3ac1d-219">Classes used in</span></span>        | [<span data-ttu-id="3ac1d-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3ac1d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ac1d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3ac1d-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-222">Entry</span></span> | <span data-ttu-id="3ac1d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ac1d-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3ac1d-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ac1d-226">System-Only</span></span>            | <span data-ttu-id="3ac1d-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-227">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3ac1d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="3ac1d-229">True</span><span class="sxs-lookup"><span data-stu-id="3ac1d-229">True</span></span>                                                                   |
| <span data-ttu-id="3ac1d-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3ac1d-230">Is Indexed</span></span>             | <span data-ttu-id="3ac1d-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-231">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3ac1d-232">In Global Catalog</span></span>      | <span data-ttu-id="3ac1d-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-233">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3ac1d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ac1d-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3ac1d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ac1d-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ac1d-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-238">Search-Flags</span></span>           | <span data-ttu-id="3ac1d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ac1d-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="3ac1d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-240">System-Flags</span></span>           | <span data-ttu-id="3ac1d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ac1d-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="3ac1d-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3ac1d-242">Classes used in</span></span>        | [<span data-ttu-id="3ac1d-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3ac1d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ac1d-244">Windows Server 2012</span></span>



| <span data-ttu-id="3ac1d-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="3ac1d-245">Entry</span></span> | <span data-ttu-id="3ac1d-246">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac1d-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ac1d-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3ac1d-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ac1d-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3ac1d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ac1d-249">System-Only</span></span>            | <span data-ttu-id="3ac1d-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-250">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3ac1d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="3ac1d-252">True</span><span class="sxs-lookup"><span data-stu-id="3ac1d-252">True</span></span>                                                                   |
| <span data-ttu-id="3ac1d-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3ac1d-253">Is Indexed</span></span>             | <span data-ttu-id="3ac1d-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-254">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3ac1d-255">In Global Catalog</span></span>      | <span data-ttu-id="3ac1d-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="3ac1d-256">False</span></span>                                                                  |
| <span data-ttu-id="3ac1d-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3ac1d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ac1d-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3ac1d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ac1d-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ac1d-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3ac1d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-261">Search-Flags</span></span>           | <span data-ttu-id="3ac1d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ac1d-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="3ac1d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ac1d-263">System-Flags</span></span>           | <span data-ttu-id="3ac1d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ac1d-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="3ac1d-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3ac1d-265">Classes used in</span></span>        | [<span data-ttu-id="3ac1d-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3ac1d-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





