---
title: атрибут MS-PKI-OID-Attribute
description: Атрибут для корпоративного OID.
ms.assetid: 51006c19-333d-4529-b249-bef6e8ab6fd8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-PKI-OID-Attribute
- Схема AD атрибута Мспки-OID-Attribute
topic_type:
- apiref
api_name:
- ms-PKI-OID-Attribute
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f996b6f5ce5b634db5cf3018145b8b10fa7b2709
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655382"
---
# <a name="ms-pki-oid-attribute-attribute"></a><span data-ttu-id="595d2-105">атрибут MS-PKI-OID-Attribute</span><span class="sxs-lookup"><span data-stu-id="595d2-105">ms-PKI-OID-Attribute attribute</span></span>

<span data-ttu-id="595d2-106">Атрибут для корпоративного OID.</span><span class="sxs-lookup"><span data-stu-id="595d2-106">The attribute for the enterprise OID.</span></span>



| <span data-ttu-id="595d2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="595d2-107">Entry</span></span> | <span data-ttu-id="595d2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="595d2-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="595d2-109">CN</span><span class="sxs-lookup"><span data-stu-id="595d2-109">CN</span></span>                | <span data-ttu-id="595d2-110">MS-PKI-OID-атрибут</span><span class="sxs-lookup"><span data-stu-id="595d2-110">ms-PKI-OID-Attribute</span></span>                                                                       |
| <span data-ttu-id="595d2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="595d2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="595d2-112">Мспки-OID-атрибут</span><span class="sxs-lookup"><span data-stu-id="595d2-112">msPKI-OID-Attribute</span></span>                                                                        |
| <span data-ttu-id="595d2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="595d2-113">Size</span></span>              | <span data-ttu-id="595d2-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="595d2-114">4 bytes</span></span>                                                                                    |
| <span data-ttu-id="595d2-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="595d2-115">Update Privilege</span></span>  | <span data-ttu-id="595d2-116">Администратор предприятия</span><span class="sxs-lookup"><span data-stu-id="595d2-116">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="595d2-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="595d2-117">Update Frequency</span></span>  | <span data-ttu-id="595d2-118">При создании нового шаблона или изменении атрибутов существующих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="595d2-118">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="595d2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="595d2-119">Attribute-Id</span></span>      | <span data-ttu-id="595d2-120">1.2.840.113556.1.4.1671</span><span class="sxs-lookup"><span data-stu-id="595d2-120">1.2.840.113556.1.4.1671</span></span>                                                                    |
| <span data-ttu-id="595d2-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="595d2-121">System-Id-Guid</span></span>    | <span data-ttu-id="595d2-122">8c9e1288-5028-4f4f-a704-76d026f246ef</span><span class="sxs-lookup"><span data-stu-id="595d2-122">8c9e1288-5028-4f4f-a704-76d026f246ef</span></span>                                                       |
| <span data-ttu-id="595d2-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="595d2-123">Syntax</span></span>            | [<span data-ttu-id="595d2-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="595d2-124">**Enumeration**</span></span>](s-enumeration.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="595d2-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="595d2-125">Implementations</span></span>

-   [<span data-ttu-id="595d2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="595d2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="595d2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="595d2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="595d2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="595d2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="595d2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="595d2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="595d2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="595d2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="595d2-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="595d2-131">Windows Server 2003</span></span>



| <span data-ttu-id="595d2-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="595d2-132">Entry</span></span> | <span data-ttu-id="595d2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="595d2-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="595d2-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="595d2-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="595d2-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="595d2-136">System-Only</span></span>            | <span data-ttu-id="595d2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-137">False</span></span>                                                              |
| <span data-ttu-id="595d2-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="595d2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="595d2-139">True</span><span class="sxs-lookup"><span data-stu-id="595d2-139">True</span></span>                                                               |
| <span data-ttu-id="595d2-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="595d2-140">Is Indexed</span></span>             | <span data-ttu-id="595d2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-141">False</span></span>                                                              |
| <span data-ttu-id="595d2-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="595d2-142">In Global Catalog</span></span>      | <span data-ttu-id="595d2-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-143">False</span></span>                                                              |
| <span data-ttu-id="595d2-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="595d2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="595d2-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="595d2-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="595d2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="595d2-146">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="595d2-147">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-148">Search-Flags</span></span>           | <span data-ttu-id="595d2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="595d2-149">0x00000000</span></span>                                                         |
| <span data-ttu-id="595d2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-150">System-Flags</span></span>           | <span data-ttu-id="595d2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="595d2-151">0x00000010</span></span>                                                         |
| <span data-ttu-id="595d2-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="595d2-152">Classes used in</span></span>        | [<span data-ttu-id="595d2-153">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="595d2-153">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="595d2-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="595d2-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="595d2-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="595d2-155">Entry</span></span> | <span data-ttu-id="595d2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="595d2-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="595d2-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="595d2-157">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="595d2-158">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="595d2-159">System-Only</span></span>            | <span data-ttu-id="595d2-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-160">False</span></span>                                                              |
| <span data-ttu-id="595d2-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="595d2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="595d2-162">True</span><span class="sxs-lookup"><span data-stu-id="595d2-162">True</span></span>                                                               |
| <span data-ttu-id="595d2-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="595d2-163">Is Indexed</span></span>             | <span data-ttu-id="595d2-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-164">False</span></span>                                                              |
| <span data-ttu-id="595d2-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="595d2-165">In Global Catalog</span></span>      | <span data-ttu-id="595d2-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-166">False</span></span>                                                              |
| <span data-ttu-id="595d2-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="595d2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="595d2-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="595d2-168">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="595d2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="595d2-169">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="595d2-170">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-171">Search-Flags</span></span>           | <span data-ttu-id="595d2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="595d2-172">0x00000000</span></span>                                                         |
| <span data-ttu-id="595d2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-173">System-Flags</span></span>           | <span data-ttu-id="595d2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="595d2-174">0x00000010</span></span>                                                         |
| <span data-ttu-id="595d2-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="595d2-175">Classes used in</span></span>        | [<span data-ttu-id="595d2-176">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="595d2-176">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="595d2-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="595d2-177">Windows Server 2008</span></span>



| <span data-ttu-id="595d2-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="595d2-178">Entry</span></span> | <span data-ttu-id="595d2-179">Значение</span><span class="sxs-lookup"><span data-stu-id="595d2-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="595d2-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="595d2-180">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="595d2-181">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="595d2-182">System-Only</span></span>            | <span data-ttu-id="595d2-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-183">False</span></span>                                                              |
| <span data-ttu-id="595d2-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="595d2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="595d2-185">True</span><span class="sxs-lookup"><span data-stu-id="595d2-185">True</span></span>                                                               |
| <span data-ttu-id="595d2-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="595d2-186">Is Indexed</span></span>             | <span data-ttu-id="595d2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-187">False</span></span>                                                              |
| <span data-ttu-id="595d2-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="595d2-188">In Global Catalog</span></span>      | <span data-ttu-id="595d2-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-189">False</span></span>                                                              |
| <span data-ttu-id="595d2-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="595d2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="595d2-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="595d2-191">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="595d2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="595d2-192">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="595d2-193">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-194">Search-Flags</span></span>           | <span data-ttu-id="595d2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="595d2-195">0x00000000</span></span>                                                         |
| <span data-ttu-id="595d2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-196">System-Flags</span></span>           | <span data-ttu-id="595d2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="595d2-197">0x00000010</span></span>                                                         |
| <span data-ttu-id="595d2-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="595d2-198">Classes used in</span></span>        | [<span data-ttu-id="595d2-199">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="595d2-199">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="595d2-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="595d2-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="595d2-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="595d2-201">Entry</span></span> | <span data-ttu-id="595d2-202">Значение</span><span class="sxs-lookup"><span data-stu-id="595d2-202">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="595d2-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="595d2-203">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="595d2-204">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="595d2-205">System-Only</span></span>            | <span data-ttu-id="595d2-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-206">False</span></span>                                                              |
| <span data-ttu-id="595d2-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="595d2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="595d2-208">True</span><span class="sxs-lookup"><span data-stu-id="595d2-208">True</span></span>                                                               |
| <span data-ttu-id="595d2-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="595d2-209">Is Indexed</span></span>             | <span data-ttu-id="595d2-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-210">False</span></span>                                                              |
| <span data-ttu-id="595d2-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="595d2-211">In Global Catalog</span></span>      | <span data-ttu-id="595d2-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-212">False</span></span>                                                              |
| <span data-ttu-id="595d2-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="595d2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="595d2-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="595d2-214">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="595d2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="595d2-215">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="595d2-216">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-217">Search-Flags</span></span>           | <span data-ttu-id="595d2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="595d2-218">0x00000000</span></span>                                                         |
| <span data-ttu-id="595d2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-219">System-Flags</span></span>           | <span data-ttu-id="595d2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="595d2-220">0x00000010</span></span>                                                         |
| <span data-ttu-id="595d2-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="595d2-221">Classes used in</span></span>        | [<span data-ttu-id="595d2-222">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="595d2-222">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="595d2-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="595d2-223">Windows Server 2012</span></span>



| <span data-ttu-id="595d2-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="595d2-224">Entry</span></span> | <span data-ttu-id="595d2-225">Значение</span><span class="sxs-lookup"><span data-stu-id="595d2-225">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="595d2-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="595d2-226">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="595d2-227">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="595d2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="595d2-228">System-Only</span></span>            | <span data-ttu-id="595d2-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-229">False</span></span>                                                              |
| <span data-ttu-id="595d2-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="595d2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="595d2-231">True</span><span class="sxs-lookup"><span data-stu-id="595d2-231">True</span></span>                                                               |
| <span data-ttu-id="595d2-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="595d2-232">Is Indexed</span></span>             | <span data-ttu-id="595d2-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-233">False</span></span>                                                              |
| <span data-ttu-id="595d2-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="595d2-234">In Global Catalog</span></span>      | <span data-ttu-id="595d2-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="595d2-235">False</span></span>                                                              |
| <span data-ttu-id="595d2-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="595d2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="595d2-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="595d2-237">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="595d2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="595d2-238">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="595d2-239">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="595d2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-240">Search-Flags</span></span>           | <span data-ttu-id="595d2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="595d2-241">0x00000000</span></span>                                                         |
| <span data-ttu-id="595d2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="595d2-242">System-Flags</span></span>           | <span data-ttu-id="595d2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="595d2-243">0x00000010</span></span>                                                         |
| <span data-ttu-id="595d2-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="595d2-244">Classes used in</span></span>        | [<span data-ttu-id="595d2-245">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="595d2-245">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





