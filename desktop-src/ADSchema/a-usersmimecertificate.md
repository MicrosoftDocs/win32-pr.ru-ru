---
title: Атрибут пользователя SMIME-Certificate
description: Объект распространения сертификата или отмеченные сертификаты.
ms.assetid: 01d13c4f-a29a-40f2-bc39-bde3c68ae259
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута пользователя-SMIME-Certificate
- Схема AD атрибута userSMIMECertificate
topic_type:
- apiref
api_name:
- User-SMIME-Certificate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc5e49ae56408a4aa5e69a7d9676d651877b32
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072092"
---
# <a name="user-smime-certificate-attribute"></a><span data-ttu-id="3aca4-105">Атрибут пользователя SMIME-Certificate</span><span class="sxs-lookup"><span data-stu-id="3aca4-105">User-SMIME-Certificate attribute</span></span>

<span data-ttu-id="3aca4-106">Объект распространения сертификата или отмеченные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="3aca4-106">Certificate distribution object or tagged certificates.</span></span>



| <span data-ttu-id="3aca4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-107">Entry</span></span> | <span data-ttu-id="3aca4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3aca4-109">CN</span><span class="sxs-lookup"><span data-stu-id="3aca4-109">CN</span></span>                | <span data-ttu-id="3aca4-110">Пользователь-SMIME-Certificate</span><span class="sxs-lookup"><span data-stu-id="3aca4-110">User-SMIME-Certificate</span></span>                                |
| <span data-ttu-id="3aca4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3aca4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3aca4-112">userSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="3aca4-112">userSMIMECertificate</span></span>                                  |
| <span data-ttu-id="3aca4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3aca4-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="3aca4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3aca4-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="3aca4-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3aca4-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="3aca4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-116">Attribute-Id</span></span>      | <span data-ttu-id="3aca4-117">2.16.840.1.113730.3.140</span><span class="sxs-lookup"><span data-stu-id="3aca4-117">2.16.840.1.113730.3.140</span></span>                               |
| <span data-ttu-id="3aca4-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3aca4-118">System-Id-Guid</span></span>    | <span data-ttu-id="3aca4-119">e16a9db2-403c-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3aca4-119">e16a9db2-403c-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="3aca4-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3aca4-120">Syntax</span></span>            | [<span data-ttu-id="3aca4-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="3aca4-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3aca4-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3aca4-122">Implementations</span></span>

-   [<span data-ttu-id="3aca4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3aca4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3aca4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3aca4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3aca4-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3aca4-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3aca4-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3aca4-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3aca4-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3aca4-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3aca4-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3aca4-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3aca4-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3aca4-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3aca4-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-130">Entry</span></span> | <span data-ttu-id="3aca4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="3aca4-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3aca4-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="3aca4-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-133">MAPI-Id</span></span>                | <span data-ttu-id="3aca4-134">0x3A70</span><span class="sxs-lookup"><span data-stu-id="3aca4-134">0x3A70</span></span>                                               |
| <span data-ttu-id="3aca4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aca4-135">System-Only</span></span>            | <span data-ttu-id="3aca4-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-136">False</span></span>                                                |
| <span data-ttu-id="3aca4-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3aca4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3aca4-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-138">False</span></span>                                                |
| <span data-ttu-id="3aca4-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3aca4-139">Is Indexed</span></span>             | <span data-ttu-id="3aca4-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-140">False</span></span>                                                |
| <span data-ttu-id="3aca4-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3aca4-141">In Global Catalog</span></span>      | <span data-ttu-id="3aca4-142">True</span><span class="sxs-lookup"><span data-stu-id="3aca4-142">True</span></span>                                                 |
| <span data-ttu-id="3aca4-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3aca4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aca4-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3aca4-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="3aca4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aca4-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="3aca4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aca4-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="3aca4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-147">Search-Flags</span></span>           | <span data-ttu-id="3aca4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-148">0x00000000</span></span>                                           |
| <span data-ttu-id="3aca4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-149">System-Flags</span></span>           | <span data-ttu-id="3aca4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3aca4-150">0x00000010</span></span>                                           |
| <span data-ttu-id="3aca4-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3aca4-151">Classes used in</span></span>        | [<span data-ttu-id="3aca4-152">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="3aca4-152">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3aca4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3aca4-153">Windows Server 2003</span></span>



| <span data-ttu-id="3aca4-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-154">Entry</span></span> | <span data-ttu-id="3aca4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aca4-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3aca4-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-157">MAPI-Id</span></span>                | <span data-ttu-id="3aca4-158">0x3A70</span><span class="sxs-lookup"><span data-stu-id="3aca4-158">0x3A70</span></span>                                                                                                                                     |
| <span data-ttu-id="3aca4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aca4-159">System-Only</span></span>            | <span data-ttu-id="3aca4-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-160">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3aca4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3aca4-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-162">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3aca4-163">Is Indexed</span></span>             | <span data-ttu-id="3aca4-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-164">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3aca4-165">In Global Catalog</span></span>      | <span data-ttu-id="3aca4-166">True</span><span class="sxs-lookup"><span data-stu-id="3aca4-166">True</span></span>                                                                                                                                       |
| <span data-ttu-id="3aca4-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3aca4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aca4-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3aca4-168">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3aca4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aca4-169">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aca4-170">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-171">Search-Flags</span></span>           | <span data-ttu-id="3aca4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-172">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-173">System-Flags</span></span>           | <span data-ttu-id="3aca4-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-174">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3aca4-175">Classes used in</span></span>        | [<span data-ttu-id="3aca4-176">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3aca4-176">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3aca4-177">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="3aca4-177">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="3aca4-178">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="3aca4-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3aca4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3aca4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3aca4-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-180">Entry</span></span> | <span data-ttu-id="3aca4-181">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aca4-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3aca4-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-183">MAPI-Id</span></span>                | <span data-ttu-id="3aca4-184">0x3A70</span><span class="sxs-lookup"><span data-stu-id="3aca4-184">0x3A70</span></span>                                                                                                                                     |
| <span data-ttu-id="3aca4-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aca4-185">System-Only</span></span>            | <span data-ttu-id="3aca4-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3aca4-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3aca4-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3aca4-189">Is Indexed</span></span>             | <span data-ttu-id="3aca4-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3aca4-191">In Global Catalog</span></span>      | <span data-ttu-id="3aca4-192">True</span><span class="sxs-lookup"><span data-stu-id="3aca4-192">True</span></span>                                                                                                                                       |
| <span data-ttu-id="3aca4-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3aca4-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aca4-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3aca4-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3aca4-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aca4-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aca4-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-197">Search-Flags</span></span>           | <span data-ttu-id="3aca4-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-199">System-Flags</span></span>           | <span data-ttu-id="3aca4-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3aca4-201">Classes used in</span></span>        | [<span data-ttu-id="3aca4-202">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3aca4-202">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3aca4-203">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="3aca4-203">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="3aca4-204">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="3aca4-204">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3aca4-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aca4-205">Windows Server 2008</span></span>



| <span data-ttu-id="3aca4-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-206">Entry</span></span> | <span data-ttu-id="3aca4-207">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-207">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aca4-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3aca4-208">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-209">MAPI-Id</span></span>                | <span data-ttu-id="3aca4-210">0x3A70</span><span class="sxs-lookup"><span data-stu-id="3aca4-210">0x3A70</span></span>                                                                                                                                     |
| <span data-ttu-id="3aca4-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aca4-211">System-Only</span></span>            | <span data-ttu-id="3aca4-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-212">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3aca4-213">Is-Single-Valued</span></span>       | <span data-ttu-id="3aca4-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-214">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3aca4-215">Is Indexed</span></span>             | <span data-ttu-id="3aca4-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-216">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3aca4-217">In Global Catalog</span></span>      | <span data-ttu-id="3aca4-218">True</span><span class="sxs-lookup"><span data-stu-id="3aca4-218">True</span></span>                                                                                                                                       |
| <span data-ttu-id="3aca4-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3aca4-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aca4-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3aca4-220">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3aca4-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aca4-221">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aca4-222">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-223">Search-Flags</span></span>           | <span data-ttu-id="3aca4-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-224">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-225">System-Flags</span></span>           | <span data-ttu-id="3aca4-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-226">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3aca4-227">Classes used in</span></span>        | [<span data-ttu-id="3aca4-228">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3aca4-228">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3aca4-229">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="3aca4-229">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="3aca4-230">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="3aca4-230">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3aca4-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3aca4-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3aca4-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-232">Entry</span></span> | <span data-ttu-id="3aca4-233">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aca4-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3aca4-234">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-235">MAPI-Id</span></span>                | <span data-ttu-id="3aca4-236">0x3A70</span><span class="sxs-lookup"><span data-stu-id="3aca4-236">0x3A70</span></span>                                                                                                                                     |
| <span data-ttu-id="3aca4-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aca4-237">System-Only</span></span>            | <span data-ttu-id="3aca4-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3aca4-239">Is-Single-Valued</span></span>       | <span data-ttu-id="3aca4-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3aca4-241">Is Indexed</span></span>             | <span data-ttu-id="3aca4-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3aca4-243">In Global Catalog</span></span>      | <span data-ttu-id="3aca4-244">True</span><span class="sxs-lookup"><span data-stu-id="3aca4-244">True</span></span>                                                                                                                                       |
| <span data-ttu-id="3aca4-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3aca4-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aca4-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3aca4-246">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3aca4-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aca4-247">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aca4-248">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-249">Search-Flags</span></span>           | <span data-ttu-id="3aca4-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-251">System-Flags</span></span>           | <span data-ttu-id="3aca4-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-252">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3aca4-253">Classes used in</span></span>        | [<span data-ttu-id="3aca4-254">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3aca4-254">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3aca4-255">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="3aca4-255">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="3aca4-256">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="3aca4-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3aca4-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3aca4-257">Windows Server 2012</span></span>



| <span data-ttu-id="3aca4-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="3aca4-258">Entry</span></span> | <span data-ttu-id="3aca4-259">Значение</span><span class="sxs-lookup"><span data-stu-id="3aca4-259">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aca4-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3aca4-260">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aca4-261">MAPI-Id</span></span>                | <span data-ttu-id="3aca4-262">0x3A70</span><span class="sxs-lookup"><span data-stu-id="3aca4-262">0x3A70</span></span>                                                                                                                                     |
| <span data-ttu-id="3aca4-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aca4-263">System-Only</span></span>            | <span data-ttu-id="3aca4-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-264">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-265">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3aca4-265">Is-Single-Valued</span></span>       | <span data-ttu-id="3aca4-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-266">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-267">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3aca4-267">Is Indexed</span></span>             | <span data-ttu-id="3aca4-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="3aca4-268">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3aca4-269">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3aca4-269">In Global Catalog</span></span>      | <span data-ttu-id="3aca4-270">True</span><span class="sxs-lookup"><span data-stu-id="3aca4-270">True</span></span>                                                                                                                                       |
| <span data-ttu-id="3aca4-271">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3aca4-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aca4-272">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3aca4-272">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3aca4-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aca4-273">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aca4-274">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3aca4-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-275">Search-Flags</span></span>           | <span data-ttu-id="3aca4-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-276">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aca4-277">System-Flags</span></span>           | <span data-ttu-id="3aca4-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aca4-278">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3aca4-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3aca4-279">Classes used in</span></span>        | [<span data-ttu-id="3aca4-280">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3aca4-280">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3aca4-281">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="3aca4-281">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="3aca4-282">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="3aca4-282">**User**</span></span>](c-user.md)<br/> |



 

 





