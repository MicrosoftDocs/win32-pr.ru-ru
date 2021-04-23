---
title: атрибут MS-PKI-OID-CPS
description: CPS (инструкция политики сертификата) для OID политики издателя предприятия.
ms.assetid: 94c5115e-a8d2-49d1-9fd2-f362e95550dc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-PKI-OID-CPS
- Схема AD атрибута Мспки-OID-CPS
topic_type:
- apiref
api_name:
- ms-PKI-OID-CPS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 218fc0eabe7311f46dba769f84b972a495138d3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893417"
---
# <a name="ms-pki-oid-cps-attribute"></a><span data-ttu-id="d7b35-105">атрибут MS-PKI-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="d7b35-105">ms-PKI-OID-CPS attribute</span></span>

<span data-ttu-id="d7b35-106">CPS (инструкция политики сертификата) для OID политики издателя предприятия.</span><span class="sxs-lookup"><span data-stu-id="d7b35-106">The CPS (Certificate Policy Statement) for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="d7b35-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d7b35-107">Entry</span></span> | <span data-ttu-id="d7b35-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b35-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b35-109">CN</span><span class="sxs-lookup"><span data-stu-id="d7b35-109">CN</span></span>                | <span data-ttu-id="d7b35-110">MS-PKI-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="d7b35-110">ms-PKI-OID-CPS</span></span>                                                                             |
| <span data-ttu-id="d7b35-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d7b35-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d7b35-112">Мспки-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="d7b35-112">msPKI-OID-CPS</span></span>                                                                              |
| <span data-ttu-id="d7b35-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d7b35-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="d7b35-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d7b35-114">Update Privilege</span></span>  | <span data-ttu-id="d7b35-115">Администратор предприятия</span><span class="sxs-lookup"><span data-stu-id="d7b35-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="d7b35-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d7b35-116">Update Frequency</span></span>  | <span data-ttu-id="d7b35-117">При создании нового шаблона или изменении атрибутов существующих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="d7b35-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="d7b35-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d7b35-118">Attribute-Id</span></span>      | <span data-ttu-id="d7b35-119">1.2.840.113556.1.4.1672</span><span class="sxs-lookup"><span data-stu-id="d7b35-119">1.2.840.113556.1.4.1672</span></span>                                                                    |
| <span data-ttu-id="d7b35-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d7b35-120">System-Id-Guid</span></span>    | <span data-ttu-id="d7b35-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span><span class="sxs-lookup"><span data-stu-id="d7b35-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span></span>                                                       |
| <span data-ttu-id="d7b35-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b35-122">Syntax</span></span>            | [<span data-ttu-id="d7b35-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d7b35-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="d7b35-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d7b35-124">Implementations</span></span>

-   [<span data-ttu-id="d7b35-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d7b35-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d7b35-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d7b35-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d7b35-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d7b35-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d7b35-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d7b35-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d7b35-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d7b35-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d7b35-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7b35-130">Windows Server 2003</span></span>



| <span data-ttu-id="d7b35-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="d7b35-131">Entry</span></span> | <span data-ttu-id="d7b35-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b35-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d7b35-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d7b35-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7b35-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7b35-135">System-Only</span></span>            | <span data-ttu-id="d7b35-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-136">False</span></span>                                                              |
| <span data-ttu-id="d7b35-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d7b35-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d7b35-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-138">False</span></span>                                                              |
| <span data-ttu-id="d7b35-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d7b35-139">Is Indexed</span></span>             | <span data-ttu-id="d7b35-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-140">False</span></span>                                                              |
| <span data-ttu-id="d7b35-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d7b35-141">In Global Catalog</span></span>      | <span data-ttu-id="d7b35-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-142">False</span></span>                                                              |
| <span data-ttu-id="d7b35-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d7b35-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7b35-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d7b35-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="d7b35-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7b35-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7b35-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-147">Search-Flags</span></span>           | <span data-ttu-id="d7b35-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7b35-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="d7b35-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-149">System-Flags</span></span>           | <span data-ttu-id="d7b35-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7b35-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="d7b35-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d7b35-151">Classes used in</span></span>        | [<span data-ttu-id="d7b35-152">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="d7b35-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d7b35-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d7b35-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d7b35-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="d7b35-154">Entry</span></span> | <span data-ttu-id="d7b35-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b35-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d7b35-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d7b35-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7b35-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7b35-158">System-Only</span></span>            | <span data-ttu-id="d7b35-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-159">False</span></span>                                                              |
| <span data-ttu-id="d7b35-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d7b35-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d7b35-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-161">False</span></span>                                                              |
| <span data-ttu-id="d7b35-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d7b35-162">Is Indexed</span></span>             | <span data-ttu-id="d7b35-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-163">False</span></span>                                                              |
| <span data-ttu-id="d7b35-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d7b35-164">In Global Catalog</span></span>      | <span data-ttu-id="d7b35-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-165">False</span></span>                                                              |
| <span data-ttu-id="d7b35-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d7b35-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7b35-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d7b35-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="d7b35-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7b35-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7b35-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-170">Search-Flags</span></span>           | <span data-ttu-id="d7b35-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7b35-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="d7b35-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-172">System-Flags</span></span>           | <span data-ttu-id="d7b35-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7b35-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="d7b35-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d7b35-174">Classes used in</span></span>        | [<span data-ttu-id="d7b35-175">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="d7b35-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d7b35-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7b35-176">Windows Server 2008</span></span>



| <span data-ttu-id="d7b35-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="d7b35-177">Entry</span></span> | <span data-ttu-id="d7b35-178">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b35-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d7b35-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d7b35-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7b35-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7b35-181">System-Only</span></span>            | <span data-ttu-id="d7b35-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-182">False</span></span>                                                              |
| <span data-ttu-id="d7b35-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d7b35-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d7b35-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-184">False</span></span>                                                              |
| <span data-ttu-id="d7b35-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d7b35-185">Is Indexed</span></span>             | <span data-ttu-id="d7b35-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-186">False</span></span>                                                              |
| <span data-ttu-id="d7b35-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d7b35-187">In Global Catalog</span></span>      | <span data-ttu-id="d7b35-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-188">False</span></span>                                                              |
| <span data-ttu-id="d7b35-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d7b35-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7b35-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d7b35-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="d7b35-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7b35-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7b35-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-193">Search-Flags</span></span>           | <span data-ttu-id="d7b35-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7b35-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="d7b35-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-195">System-Flags</span></span>           | <span data-ttu-id="d7b35-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7b35-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="d7b35-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d7b35-197">Classes used in</span></span>        | [<span data-ttu-id="d7b35-198">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="d7b35-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d7b35-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7b35-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d7b35-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="d7b35-200">Entry</span></span> | <span data-ttu-id="d7b35-201">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b35-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d7b35-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d7b35-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7b35-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7b35-204">System-Only</span></span>            | <span data-ttu-id="d7b35-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-205">False</span></span>                                                              |
| <span data-ttu-id="d7b35-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d7b35-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d7b35-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-207">False</span></span>                                                              |
| <span data-ttu-id="d7b35-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d7b35-208">Is Indexed</span></span>             | <span data-ttu-id="d7b35-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-209">False</span></span>                                                              |
| <span data-ttu-id="d7b35-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d7b35-210">In Global Catalog</span></span>      | <span data-ttu-id="d7b35-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-211">False</span></span>                                                              |
| <span data-ttu-id="d7b35-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d7b35-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7b35-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d7b35-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="d7b35-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7b35-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7b35-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-216">Search-Flags</span></span>           | <span data-ttu-id="d7b35-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7b35-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="d7b35-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-218">System-Flags</span></span>           | <span data-ttu-id="d7b35-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7b35-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="d7b35-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d7b35-220">Classes used in</span></span>        | [<span data-ttu-id="d7b35-221">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="d7b35-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d7b35-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7b35-222">Windows Server 2012</span></span>



| <span data-ttu-id="d7b35-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="d7b35-223">Entry</span></span> | <span data-ttu-id="d7b35-224">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b35-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d7b35-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d7b35-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7b35-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="d7b35-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7b35-227">System-Only</span></span>            | <span data-ttu-id="d7b35-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-228">False</span></span>                                                              |
| <span data-ttu-id="d7b35-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d7b35-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d7b35-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-230">False</span></span>                                                              |
| <span data-ttu-id="d7b35-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d7b35-231">Is Indexed</span></span>             | <span data-ttu-id="d7b35-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-232">False</span></span>                                                              |
| <span data-ttu-id="d7b35-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d7b35-233">In Global Catalog</span></span>      | <span data-ttu-id="d7b35-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="d7b35-234">False</span></span>                                                              |
| <span data-ttu-id="d7b35-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d7b35-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7b35-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d7b35-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="d7b35-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7b35-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7b35-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="d7b35-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-239">Search-Flags</span></span>           | <span data-ttu-id="d7b35-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7b35-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="d7b35-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7b35-241">System-Flags</span></span>           | <span data-ttu-id="d7b35-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7b35-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="d7b35-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d7b35-243">Classes used in</span></span>        | [<span data-ttu-id="d7b35-244">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="d7b35-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





