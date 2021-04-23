---
title: Атрибут LDAP-отображаемое имя
description: Имя, используемое клиентами LDAP, например поставщик LDAP ADSI, для чтения и записи атрибута с помощью протокола LDAP.
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута LDAP-отображаемого имени
- Схема AD атрибута lDAPDisplayName
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ffa25777ec4b5139a41ba9e56d8d5f0a9a3d92
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262240"
---
# <a name="ldap-display-name-attribute"></a><span data-ttu-id="de3ad-105">Атрибут LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="de3ad-105">LDAP-Display-Name attribute</span></span>

<span data-ttu-id="de3ad-106">Имя, используемое клиентами LDAP, например поставщик LDAP ADSI, для чтения и записи атрибута с помощью протокола LDAP.</span><span class="sxs-lookup"><span data-stu-id="de3ad-106">The name used by LDAP clients, such as the ADSI LDAP provider, to read and write the attribute by using the LDAP protocol.</span></span>



| <span data-ttu-id="de3ad-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-107">Entry</span></span> | <span data-ttu-id="de3ad-108">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="de3ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="de3ad-109">CN</span></span>                | <span data-ttu-id="de3ad-110">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="de3ad-110">LDAP-Display-Name</span></span>                           |
| <span data-ttu-id="de3ad-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="de3ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="de3ad-112">lDAPDisplayName</span><span class="sxs-lookup"><span data-stu-id="de3ad-112">lDAPDisplayName</span></span>                             |
| <span data-ttu-id="de3ad-113">Размер</span><span class="sxs-lookup"><span data-stu-id="de3ad-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="de3ad-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="de3ad-114">Update Privilege</span></span>  | <span data-ttu-id="de3ad-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="de3ad-115">Schema administrator</span></span>                        |
| <span data-ttu-id="de3ad-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="de3ad-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="de3ad-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-117">Attribute-Id</span></span>      | <span data-ttu-id="de3ad-118">1.2.840.113556.1.2.460</span><span class="sxs-lookup"><span data-stu-id="de3ad-118">1.2.840.113556.1.2.460</span></span>                      |
| <span data-ttu-id="de3ad-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="de3ad-119">System-Id-Guid</span></span>    | <span data-ttu-id="de3ad-120">bf96799a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="de3ad-120">bf96799a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="de3ad-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de3ad-121">Syntax</span></span>            | [<span data-ttu-id="de3ad-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="de3ad-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="de3ad-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="de3ad-123">Implementations</span></span>

-   [<span data-ttu-id="de3ad-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="de3ad-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="de3ad-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de3ad-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de3ad-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="de3ad-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="de3ad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de3ad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de3ad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de3ad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de3ad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de3ad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de3ad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de3ad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="de3ad-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de3ad-131">Windows 2000 Server</span></span>



| <span data-ttu-id="de3ad-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-132">Entry</span></span> | <span data-ttu-id="de3ad-133">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-134">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-135">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-136">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-136">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-137">System-Only</span></span>            | <span data-ttu-id="de3ad-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-138">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-139">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-140">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-140">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-141">Is Indexed</span></span>             | <span data-ttu-id="de3ad-142">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-142">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-143">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-144">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-144">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-146">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-147">Range-Lower</span></span>            | <span data-ttu-id="de3ad-148">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-148">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-149">Range-Upper</span></span>            | <span data-ttu-id="de3ad-150">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-150">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-151">Search-Flags</span></span>           | <span data-ttu-id="de3ad-152">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-152">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-153">System-Flags</span></span>           | <span data-ttu-id="de3ad-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-154">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-155">Classes used in</span></span>        | [<span data-ttu-id="de3ad-156">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-157">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-157">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="de3ad-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de3ad-158">Windows Server 2003</span></span>



| <span data-ttu-id="de3ad-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-159">Entry</span></span> | <span data-ttu-id="de3ad-160">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-161">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-162">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-163">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-163">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-164">System-Only</span></span>            | <span data-ttu-id="de3ad-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-165">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-166">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-167">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-167">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-168">Is Indexed</span></span>             | <span data-ttu-id="de3ad-169">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-169">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-170">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-171">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-171">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-174">Range-Lower</span></span>            | <span data-ttu-id="de3ad-175">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-175">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-176">Range-Upper</span></span>            | <span data-ttu-id="de3ad-177">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-177">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-178">Search-Flags</span></span>           | <span data-ttu-id="de3ad-179">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-179">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-180">System-Flags</span></span>           | <span data-ttu-id="de3ad-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-182">Classes used in</span></span>        | [<span data-ttu-id="de3ad-183">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-184">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="de3ad-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="de3ad-185">ADAM</span></span>



| <span data-ttu-id="de3ad-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-186">Entry</span></span> | <span data-ttu-id="de3ad-187">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-189">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-190">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-190">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-191">System-Only</span></span>            | <span data-ttu-id="de3ad-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-192">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-193">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-194">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-194">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-195">Is Indexed</span></span>             | <span data-ttu-id="de3ad-196">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-196">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-197">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-198">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-198">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-200">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-201">Range-Lower</span></span>            | <span data-ttu-id="de3ad-202">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-202">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-203">Range-Upper</span></span>            | <span data-ttu-id="de3ad-204">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-204">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-205">Search-Flags</span></span>           | <span data-ttu-id="de3ad-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-206">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-207">System-Flags</span></span>           | <span data-ttu-id="de3ad-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-208">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-209">Classes used in</span></span>        | [<span data-ttu-id="de3ad-210">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-210">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-211">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-211">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de3ad-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de3ad-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de3ad-213">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-213">Entry</span></span> | <span data-ttu-id="de3ad-214">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-214">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-215">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-215">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-216">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-217">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-217">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-218">System-Only</span></span>            | <span data-ttu-id="de3ad-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-219">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-220">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-220">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-221">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-221">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-222">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-222">Is Indexed</span></span>             | <span data-ttu-id="de3ad-223">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-223">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-224">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-224">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-225">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-225">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-226">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-227">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-227">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-228">Range-Lower</span></span>            | <span data-ttu-id="de3ad-229">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-229">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-230">Range-Upper</span></span>            | <span data-ttu-id="de3ad-231">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-231">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-232">Search-Flags</span></span>           | <span data-ttu-id="de3ad-233">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-233">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-234">System-Flags</span></span>           | <span data-ttu-id="de3ad-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-235">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-236">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-236">Classes used in</span></span>        | [<span data-ttu-id="de3ad-237">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-237">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-238">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de3ad-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de3ad-239">Windows Server 2008</span></span>



| <span data-ttu-id="de3ad-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-240">Entry</span></span> | <span data-ttu-id="de3ad-241">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-241">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-242">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-243">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-244">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-244">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-245">System-Only</span></span>            | <span data-ttu-id="de3ad-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-246">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-247">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-247">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-248">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-248">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-249">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-249">Is Indexed</span></span>             | <span data-ttu-id="de3ad-250">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-250">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-251">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-251">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-252">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-252">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-253">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-254">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-254">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-255">Range-Lower</span></span>            | <span data-ttu-id="de3ad-256">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-256">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-257">Range-Upper</span></span>            | <span data-ttu-id="de3ad-258">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-258">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-259">Search-Flags</span></span>           | <span data-ttu-id="de3ad-260">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-260">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-261">System-Flags</span></span>           | <span data-ttu-id="de3ad-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-262">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-263">Classes used in</span></span>        | [<span data-ttu-id="de3ad-264">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-264">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-265">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-265">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de3ad-266">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de3ad-266">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de3ad-267">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-267">Entry</span></span> | <span data-ttu-id="de3ad-268">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-268">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-269">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-269">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-270">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-271">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-271">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-272">System-Only</span></span>            | <span data-ttu-id="de3ad-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-273">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-274">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-274">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-275">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-275">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-276">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-276">Is Indexed</span></span>             | <span data-ttu-id="de3ad-277">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-277">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-278">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-278">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-279">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-279">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-280">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-281">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-281">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-282">Range-Lower</span></span>            | <span data-ttu-id="de3ad-283">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-283">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-284">Range-Upper</span></span>            | <span data-ttu-id="de3ad-285">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-285">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-286">Search-Flags</span></span>           | <span data-ttu-id="de3ad-287">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-287">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-288">System-Flags</span></span>           | <span data-ttu-id="de3ad-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-289">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-290">Classes used in</span></span>        | [<span data-ttu-id="de3ad-291">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-292">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de3ad-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de3ad-293">Windows Server 2012</span></span>



| <span data-ttu-id="de3ad-294">Ввод</span><span class="sxs-lookup"><span data-stu-id="de3ad-294">Entry</span></span> | <span data-ttu-id="de3ad-295">Значение</span><span class="sxs-lookup"><span data-stu-id="de3ad-295">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ad-296">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de3ad-296">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="de3ad-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de3ad-297">MAPI-Id</span></span>                | <span data-ttu-id="de3ad-298">0x8171</span><span class="sxs-lookup"><span data-stu-id="de3ad-298">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="de3ad-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="de3ad-299">System-Only</span></span>            | <span data-ttu-id="de3ad-300">Неверно</span><span class="sxs-lookup"><span data-stu-id="de3ad-300">False</span></span>                                                                                                     |
| <span data-ttu-id="de3ad-301">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de3ad-301">Is-Single-Valued</span></span>       | <span data-ttu-id="de3ad-302">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-302">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-303">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de3ad-303">Is Indexed</span></span>             | <span data-ttu-id="de3ad-304">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-304">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-305">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de3ad-305">In Global Catalog</span></span>      | <span data-ttu-id="de3ad-306">True</span><span class="sxs-lookup"><span data-stu-id="de3ad-306">True</span></span>                                                                                                      |
| <span data-ttu-id="de3ad-307">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de3ad-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="de3ad-308">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de3ad-308">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="de3ad-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de3ad-309">Range-Lower</span></span>            | <span data-ttu-id="de3ad-310">1</span><span class="sxs-lookup"><span data-stu-id="de3ad-310">1</span></span>                                                                                                         |
| <span data-ttu-id="de3ad-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de3ad-311">Range-Upper</span></span>            | <span data-ttu-id="de3ad-312">256</span><span class="sxs-lookup"><span data-stu-id="de3ad-312">256</span></span>                                                                                                       |
| <span data-ttu-id="de3ad-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-313">Search-Flags</span></span>           | <span data-ttu-id="de3ad-314">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de3ad-314">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="de3ad-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de3ad-315">System-Flags</span></span>           | <span data-ttu-id="de3ad-316">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de3ad-316">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="de3ad-317">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de3ad-317">Classes used in</span></span>        | [<span data-ttu-id="de3ad-318">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-318">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="de3ad-319">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="de3ad-319">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





