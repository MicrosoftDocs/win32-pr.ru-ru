---
title: атрибут MS-PKI-OID-User-Notice
description: Уведомление пользователя для OID политики издателя предприятия.
ms.assetid: b7cfc5fd-99d8-4ddd-bc8f-5e5505eb1f1b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-PKI-OID-пользователь-уведомление
- Схема AD атрибута Мспки-OID-User-Notice
topic_type:
- apiref
api_name:
- ms-PKI-OID-User-Notice
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a40f39dc9d6eb8e033435d2803a658edcaacf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655381"
---
# <a name="ms-pki-oid-user-notice-attribute"></a><span data-ttu-id="28068-105">атрибут MS-PKI-OID-User-Notice</span><span class="sxs-lookup"><span data-stu-id="28068-105">ms-PKI-OID-User-Notice attribute</span></span>

<span data-ttu-id="28068-106">Уведомление пользователя для OID политики издателя предприятия.</span><span class="sxs-lookup"><span data-stu-id="28068-106">The user notice for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="28068-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="28068-107">Entry</span></span> | <span data-ttu-id="28068-108">Значение</span><span class="sxs-lookup"><span data-stu-id="28068-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="28068-109">CN</span><span class="sxs-lookup"><span data-stu-id="28068-109">CN</span></span>                | <span data-ttu-id="28068-110">MS-PKI-OID-пользователь — уведомление</span><span class="sxs-lookup"><span data-stu-id="28068-110">ms-PKI-OID-User-Notice</span></span>                                                                     |
| <span data-ttu-id="28068-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="28068-111">Ldap-Display-Name</span></span> | <span data-ttu-id="28068-112">Мспки-OID-пользователь-уведомление</span><span class="sxs-lookup"><span data-stu-id="28068-112">msPKI-OID-User-Notice</span></span>                                                                      |
| <span data-ttu-id="28068-113">Размер</span><span class="sxs-lookup"><span data-stu-id="28068-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="28068-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="28068-114">Update Privilege</span></span>  | <span data-ttu-id="28068-115">Администратор предприятия</span><span class="sxs-lookup"><span data-stu-id="28068-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="28068-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="28068-116">Update Frequency</span></span>  | <span data-ttu-id="28068-117">При создании нового шаблона или изменении атрибутов существующих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="28068-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="28068-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28068-118">Attribute-Id</span></span>      | <span data-ttu-id="28068-119">1.2.840.113556.1.4.1673</span><span class="sxs-lookup"><span data-stu-id="28068-119">1.2.840.113556.1.4.1673</span></span>                                                                    |
| <span data-ttu-id="28068-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="28068-120">System-Id-Guid</span></span>    | <span data-ttu-id="28068-121">04c4da7a-e114-4e69-88de-e293f2d3b395</span><span class="sxs-lookup"><span data-stu-id="28068-121">04c4da7a-e114-4e69-88de-e293f2d3b395</span></span>                                                       |
| <span data-ttu-id="28068-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28068-122">Syntax</span></span>            | [<span data-ttu-id="28068-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="28068-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="28068-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="28068-124">Implementations</span></span>

-   [<span data-ttu-id="28068-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28068-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28068-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28068-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28068-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28068-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28068-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28068-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28068-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28068-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="28068-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28068-130">Windows Server 2003</span></span>



| <span data-ttu-id="28068-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="28068-131">Entry</span></span> | <span data-ttu-id="28068-132">Значение</span><span class="sxs-lookup"><span data-stu-id="28068-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28068-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28068-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28068-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="28068-135">System-Only</span></span>            | <span data-ttu-id="28068-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-136">False</span></span>                                                              |
| <span data-ttu-id="28068-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28068-137">Is-Single-Valued</span></span>       | <span data-ttu-id="28068-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-138">False</span></span>                                                              |
| <span data-ttu-id="28068-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28068-139">Is Indexed</span></span>             | <span data-ttu-id="28068-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-140">False</span></span>                                                              |
| <span data-ttu-id="28068-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28068-141">In Global Catalog</span></span>      | <span data-ttu-id="28068-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-142">False</span></span>                                                              |
| <span data-ttu-id="28068-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28068-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="28068-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28068-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28068-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28068-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28068-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-147">Search-Flags</span></span>           | <span data-ttu-id="28068-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28068-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="28068-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-149">System-Flags</span></span>           | <span data-ttu-id="28068-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28068-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="28068-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28068-151">Classes used in</span></span>        | [<span data-ttu-id="28068-152">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="28068-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28068-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28068-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28068-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="28068-154">Entry</span></span> | <span data-ttu-id="28068-155">Значение</span><span class="sxs-lookup"><span data-stu-id="28068-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28068-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28068-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28068-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="28068-158">System-Only</span></span>            | <span data-ttu-id="28068-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-159">False</span></span>                                                              |
| <span data-ttu-id="28068-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28068-160">Is-Single-Valued</span></span>       | <span data-ttu-id="28068-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-161">False</span></span>                                                              |
| <span data-ttu-id="28068-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28068-162">Is Indexed</span></span>             | <span data-ttu-id="28068-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-163">False</span></span>                                                              |
| <span data-ttu-id="28068-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28068-164">In Global Catalog</span></span>      | <span data-ttu-id="28068-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-165">False</span></span>                                                              |
| <span data-ttu-id="28068-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28068-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="28068-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28068-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28068-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28068-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28068-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-170">Search-Flags</span></span>           | <span data-ttu-id="28068-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28068-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="28068-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-172">System-Flags</span></span>           | <span data-ttu-id="28068-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28068-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="28068-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28068-174">Classes used in</span></span>        | [<span data-ttu-id="28068-175">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="28068-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28068-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28068-176">Windows Server 2008</span></span>



| <span data-ttu-id="28068-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="28068-177">Entry</span></span> | <span data-ttu-id="28068-178">Значение</span><span class="sxs-lookup"><span data-stu-id="28068-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28068-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28068-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28068-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="28068-181">System-Only</span></span>            | <span data-ttu-id="28068-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-182">False</span></span>                                                              |
| <span data-ttu-id="28068-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28068-183">Is-Single-Valued</span></span>       | <span data-ttu-id="28068-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-184">False</span></span>                                                              |
| <span data-ttu-id="28068-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28068-185">Is Indexed</span></span>             | <span data-ttu-id="28068-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-186">False</span></span>                                                              |
| <span data-ttu-id="28068-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28068-187">In Global Catalog</span></span>      | <span data-ttu-id="28068-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-188">False</span></span>                                                              |
| <span data-ttu-id="28068-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28068-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="28068-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28068-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28068-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28068-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28068-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-193">Search-Flags</span></span>           | <span data-ttu-id="28068-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28068-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="28068-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-195">System-Flags</span></span>           | <span data-ttu-id="28068-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28068-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="28068-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28068-197">Classes used in</span></span>        | [<span data-ttu-id="28068-198">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="28068-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28068-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28068-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28068-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="28068-200">Entry</span></span> | <span data-ttu-id="28068-201">Значение</span><span class="sxs-lookup"><span data-stu-id="28068-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28068-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28068-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28068-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="28068-204">System-Only</span></span>            | <span data-ttu-id="28068-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-205">False</span></span>                                                              |
| <span data-ttu-id="28068-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28068-206">Is-Single-Valued</span></span>       | <span data-ttu-id="28068-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-207">False</span></span>                                                              |
| <span data-ttu-id="28068-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28068-208">Is Indexed</span></span>             | <span data-ttu-id="28068-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-209">False</span></span>                                                              |
| <span data-ttu-id="28068-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28068-210">In Global Catalog</span></span>      | <span data-ttu-id="28068-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-211">False</span></span>                                                              |
| <span data-ttu-id="28068-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28068-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="28068-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28068-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28068-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28068-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28068-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-216">Search-Flags</span></span>           | <span data-ttu-id="28068-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28068-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="28068-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-218">System-Flags</span></span>           | <span data-ttu-id="28068-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28068-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="28068-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28068-220">Classes used in</span></span>        | [<span data-ttu-id="28068-221">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="28068-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28068-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28068-222">Windows Server 2012</span></span>



| <span data-ttu-id="28068-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="28068-223">Entry</span></span> | <span data-ttu-id="28068-224">Значение</span><span class="sxs-lookup"><span data-stu-id="28068-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="28068-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28068-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28068-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="28068-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="28068-227">System-Only</span></span>            | <span data-ttu-id="28068-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-228">False</span></span>                                                              |
| <span data-ttu-id="28068-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28068-229">Is-Single-Valued</span></span>       | <span data-ttu-id="28068-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-230">False</span></span>                                                              |
| <span data-ttu-id="28068-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28068-231">Is Indexed</span></span>             | <span data-ttu-id="28068-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-232">False</span></span>                                                              |
| <span data-ttu-id="28068-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28068-233">In Global Catalog</span></span>      | <span data-ttu-id="28068-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="28068-234">False</span></span>                                                              |
| <span data-ttu-id="28068-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28068-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="28068-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28068-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="28068-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28068-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28068-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="28068-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-239">Search-Flags</span></span>           | <span data-ttu-id="28068-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28068-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="28068-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28068-241">System-Flags</span></span>           | <span data-ttu-id="28068-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28068-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="28068-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28068-243">Classes used in</span></span>        | [<span data-ttu-id="28068-244">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="28068-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





