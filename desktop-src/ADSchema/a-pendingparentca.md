---
title: Атрибут ожидающего наследования CA
description: Ссылка на центры сертификации, которые выдавали ожидающие сертификаты для данного центра сертификации.
ms.assetid: 9cdac673-aecd-4a42-93f5-c869fa136186
ms.tgt_platform: multiple
keywords:
- Схема Active Directory с атрибутом "ожидание-родитель-CA"
- Схема AD атрибута Пендингпарентка
topic_type:
- apiref
api_name:
- Pending-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e100a18980780f4086f09ce39a060703462ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655315"
---
# <a name="pending-parent-ca-attribute"></a><span data-ttu-id="fdfd9-105">Атрибут ожидающего наследования CA</span><span class="sxs-lookup"><span data-stu-id="fdfd9-105">Pending-Parent-CA attribute</span></span>

<span data-ttu-id="fdfd9-106">Ссылка на центры сертификации, которые выдавали ожидающие сертификаты для данного центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="fdfd9-106">Reference to the certification authorities that issued the pending certificates for this certification authority.</span></span>



| <span data-ttu-id="fdfd9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-107">Entry</span></span> | <span data-ttu-id="fdfd9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="fdfd9-109">CN</span><span class="sxs-lookup"><span data-stu-id="fdfd9-109">CN</span></span>                | <span data-ttu-id="fdfd9-110">Ожидающий — родительский ЦС</span><span class="sxs-lookup"><span data-stu-id="fdfd9-110">Pending-Parent-CA</span></span>                       |
| <span data-ttu-id="fdfd9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fdfd9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fdfd9-112">пендингпарентка</span><span class="sxs-lookup"><span data-stu-id="fdfd9-112">pendingParentCA</span></span>                         |
| <span data-ttu-id="fdfd9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="fdfd9-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="fdfd9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fdfd9-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="fdfd9-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fdfd9-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="fdfd9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-116">Attribute-Id</span></span>      | <span data-ttu-id="fdfd9-117">1.2.840.113556.1.4.695</span><span class="sxs-lookup"><span data-stu-id="fdfd9-117">1.2.840.113556.1.4.695</span></span>                  |
| <span data-ttu-id="fdfd9-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fdfd9-118">System-Id-Guid</span></span>    | <span data-ttu-id="fdfd9-119">963d273e-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fdfd9-119">963d273e-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="fdfd9-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdfd9-120">Syntax</span></span>            | [<span data-ttu-id="fdfd9-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="fdfd9-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fdfd9-122">Implementations</span></span>

-   [<span data-ttu-id="fdfd9-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fdfd9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fdfd9-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fdfd9-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fdfd9-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fdfd9-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fdfd9-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fdfd9-129">Windows 2000 Server</span></span>



| <span data-ttu-id="fdfd9-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-130">Entry</span></span> | <span data-ttu-id="fdfd9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fdfd9-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdfd9-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfd9-134">System-Only</span></span>            | <span data-ttu-id="fdfd9-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-135">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdfd9-136">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfd9-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-137">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdfd9-138">Is Indexed</span></span>             | <span data-ttu-id="fdfd9-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-139">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdfd9-140">In Global Catalog</span></span>      | <span data-ttu-id="fdfd9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-141">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdfd9-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfd9-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdfd9-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="fdfd9-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfd9-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfd9-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-146">Search-Flags</span></span>           | <span data-ttu-id="fdfd9-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfd9-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="fdfd9-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-148">System-Flags</span></span>           | <span data-ttu-id="fdfd9-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfd9-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="fdfd9-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdfd9-150">Classes used in</span></span>        | [<span data-ttu-id="fdfd9-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fdfd9-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fdfd9-152">Windows Server 2003</span></span>



| <span data-ttu-id="fdfd9-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-153">Entry</span></span> | <span data-ttu-id="fdfd9-154">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fdfd9-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdfd9-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfd9-157">System-Only</span></span>            | <span data-ttu-id="fdfd9-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-158">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdfd9-159">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfd9-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-160">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdfd9-161">Is Indexed</span></span>             | <span data-ttu-id="fdfd9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-162">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdfd9-163">In Global Catalog</span></span>      | <span data-ttu-id="fdfd9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-164">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdfd9-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfd9-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdfd9-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="fdfd9-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfd9-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfd9-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-169">Search-Flags</span></span>           | <span data-ttu-id="fdfd9-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfd9-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="fdfd9-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-171">System-Flags</span></span>           | <span data-ttu-id="fdfd9-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfd9-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="fdfd9-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdfd9-173">Classes used in</span></span>        | [<span data-ttu-id="fdfd9-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fdfd9-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fdfd9-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fdfd9-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-176">Entry</span></span> | <span data-ttu-id="fdfd9-177">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fdfd9-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdfd9-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfd9-180">System-Only</span></span>            | <span data-ttu-id="fdfd9-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-181">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdfd9-182">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfd9-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-183">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdfd9-184">Is Indexed</span></span>             | <span data-ttu-id="fdfd9-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-185">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdfd9-186">In Global Catalog</span></span>      | <span data-ttu-id="fdfd9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-187">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdfd9-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfd9-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdfd9-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="fdfd9-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfd9-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfd9-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-192">Search-Flags</span></span>           | <span data-ttu-id="fdfd9-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfd9-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="fdfd9-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-194">System-Flags</span></span>           | <span data-ttu-id="fdfd9-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfd9-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="fdfd9-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdfd9-196">Classes used in</span></span>        | [<span data-ttu-id="fdfd9-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fdfd9-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdfd9-198">Windows Server 2008</span></span>



| <span data-ttu-id="fdfd9-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-199">Entry</span></span> | <span data-ttu-id="fdfd9-200">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fdfd9-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdfd9-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfd9-203">System-Only</span></span>            | <span data-ttu-id="fdfd9-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-204">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdfd9-205">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfd9-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-206">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdfd9-207">Is Indexed</span></span>             | <span data-ttu-id="fdfd9-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-208">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdfd9-209">In Global Catalog</span></span>      | <span data-ttu-id="fdfd9-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-210">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdfd9-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfd9-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdfd9-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="fdfd9-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfd9-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfd9-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-215">Search-Flags</span></span>           | <span data-ttu-id="fdfd9-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfd9-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="fdfd9-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-217">System-Flags</span></span>           | <span data-ttu-id="fdfd9-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfd9-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="fdfd9-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdfd9-219">Classes used in</span></span>        | [<span data-ttu-id="fdfd9-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fdfd9-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fdfd9-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fdfd9-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-222">Entry</span></span> | <span data-ttu-id="fdfd9-223">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fdfd9-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdfd9-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfd9-226">System-Only</span></span>            | <span data-ttu-id="fdfd9-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-227">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdfd9-228">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfd9-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-229">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdfd9-230">Is Indexed</span></span>             | <span data-ttu-id="fdfd9-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-231">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdfd9-232">In Global Catalog</span></span>      | <span data-ttu-id="fdfd9-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-233">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdfd9-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfd9-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdfd9-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="fdfd9-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfd9-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfd9-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-238">Search-Flags</span></span>           | <span data-ttu-id="fdfd9-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfd9-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="fdfd9-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-240">System-Flags</span></span>           | <span data-ttu-id="fdfd9-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfd9-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="fdfd9-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdfd9-242">Classes used in</span></span>        | [<span data-ttu-id="fdfd9-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fdfd9-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdfd9-244">Windows Server 2012</span></span>



| <span data-ttu-id="fdfd9-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdfd9-245">Entry</span></span> | <span data-ttu-id="fdfd9-246">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfd9-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fdfd9-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdfd9-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfd9-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="fdfd9-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfd9-249">System-Only</span></span>            | <span data-ttu-id="fdfd9-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-250">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdfd9-251">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfd9-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-252">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdfd9-253">Is Indexed</span></span>             | <span data-ttu-id="fdfd9-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-254">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdfd9-255">In Global Catalog</span></span>      | <span data-ttu-id="fdfd9-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdfd9-256">False</span></span>                                                                  |
| <span data-ttu-id="fdfd9-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdfd9-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfd9-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdfd9-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="fdfd9-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfd9-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfd9-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="fdfd9-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-261">Search-Flags</span></span>           | <span data-ttu-id="fdfd9-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfd9-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="fdfd9-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfd9-263">System-Flags</span></span>           | <span data-ttu-id="fdfd9-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfd9-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="fdfd9-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdfd9-265">Classes used in</span></span>        | [<span data-ttu-id="fdfd9-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="fdfd9-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





