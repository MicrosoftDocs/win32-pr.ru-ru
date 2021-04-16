---
title: Атрибут-Security-GUID
description: Идентификатор GUID, используемый для применения учетных данных безопасности к набору объектов.
ms.assetid: df4709ec-273d-4294-8094-f396c10c06e2
ms.tgt_platform: multiple
keywords:
- Attribute-Security-схема AD атрибута GUID
- Схема AD атрибута Аттрибутесекуритигуид
topic_type:
- apiref
api_name:
- Attribute-Security-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b2ada7c6c806bec1c524b0408750144ca1fd8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262274"
---
# <a name="attribute-security-guid-attribute"></a><span data-ttu-id="6d670-105">Атрибут-Security-GUID</span><span class="sxs-lookup"><span data-stu-id="6d670-105">Attribute-Security-GUID attribute</span></span>

<span data-ttu-id="6d670-106">Идентификатор GUID, используемый для применения учетных данных безопасности к набору объектов.</span><span class="sxs-lookup"><span data-stu-id="6d670-106">The GUID to be used to apply security credentials to a set of objects.</span></span>



| <span data-ttu-id="6d670-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-107">Entry</span></span> | <span data-ttu-id="6d670-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6d670-109">CN</span><span class="sxs-lookup"><span data-stu-id="6d670-109">CN</span></span>                | <span data-ttu-id="6d670-110">Attribute-Security-GUID</span><span class="sxs-lookup"><span data-stu-id="6d670-110">Attribute-Security-GUID</span></span>                               |
| <span data-ttu-id="6d670-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6d670-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6d670-112">attributeSecurityGUID</span><span class="sxs-lookup"><span data-stu-id="6d670-112">attributeSecurityGUID</span></span>                                 |
| <span data-ttu-id="6d670-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6d670-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6d670-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6d670-114">Update Privilege</span></span>  | <span data-ttu-id="6d670-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="6d670-115">Schema administrator</span></span>                                  |
| <span data-ttu-id="6d670-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6d670-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6d670-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-117">Attribute-Id</span></span>      | <span data-ttu-id="6d670-118">1.2.840.113556.1.4.149</span><span class="sxs-lookup"><span data-stu-id="6d670-118">1.2.840.113556.1.4.149</span></span>                                |
| <span data-ttu-id="6d670-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6d670-119">System-Id-Guid</span></span>    | <span data-ttu-id="6d670-120">bf967924-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6d670-120">bf967924-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="6d670-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d670-121">Syntax</span></span>            | [<span data-ttu-id="6d670-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="6d670-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6d670-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6d670-123">Implementations</span></span>

-   [<span data-ttu-id="6d670-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d670-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d670-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d670-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d670-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6d670-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6d670-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d670-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d670-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d670-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d670-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d670-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d670-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d670-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d670-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d670-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6d670-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-132">Entry</span></span> | <span data-ttu-id="6d670-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-136">System-Only</span></span>            | <span data-ttu-id="6d670-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-137">False</span></span>                                                    |
| <span data-ttu-id="6d670-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-139">True</span><span class="sxs-lookup"><span data-stu-id="6d670-139">True</span></span>                                                     |
| <span data-ttu-id="6d670-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-140">Is Indexed</span></span>             | <span data-ttu-id="6d670-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-141">False</span></span>                                                    |
| <span data-ttu-id="6d670-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-142">In Global Catalog</span></span>      | <span data-ttu-id="6d670-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-143">False</span></span>                                                    |
| <span data-ttu-id="6d670-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-146">Range-Lower</span></span>            | <span data-ttu-id="6d670-147">16</span><span class="sxs-lookup"><span data-stu-id="6d670-147">16</span></span>                                                       |
| <span data-ttu-id="6d670-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-148">Range-Upper</span></span>            | <span data-ttu-id="6d670-149">16</span><span class="sxs-lookup"><span data-stu-id="6d670-149">16</span></span>                                                       |
| <span data-ttu-id="6d670-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-150">Search-Flags</span></span>           | <span data-ttu-id="6d670-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-151">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-152">System-Flags</span></span>           | <span data-ttu-id="6d670-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-153">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-154">Classes used in</span></span>        | [<span data-ttu-id="6d670-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d670-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d670-156">Windows Server 2003</span></span>



| <span data-ttu-id="6d670-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-157">Entry</span></span> | <span data-ttu-id="6d670-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-160">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-161">System-Only</span></span>            | <span data-ttu-id="6d670-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-162">False</span></span>                                                    |
| <span data-ttu-id="6d670-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-164">True</span><span class="sxs-lookup"><span data-stu-id="6d670-164">True</span></span>                                                     |
| <span data-ttu-id="6d670-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-165">Is Indexed</span></span>             | <span data-ttu-id="6d670-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-166">False</span></span>                                                    |
| <span data-ttu-id="6d670-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-167">In Global Catalog</span></span>      | <span data-ttu-id="6d670-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-168">False</span></span>                                                    |
| <span data-ttu-id="6d670-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-171">Range-Lower</span></span>            | <span data-ttu-id="6d670-172">16</span><span class="sxs-lookup"><span data-stu-id="6d670-172">16</span></span>                                                       |
| <span data-ttu-id="6d670-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-173">Range-Upper</span></span>            | <span data-ttu-id="6d670-174">16</span><span class="sxs-lookup"><span data-stu-id="6d670-174">16</span></span>                                                       |
| <span data-ttu-id="6d670-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-175">Search-Flags</span></span>           | <span data-ttu-id="6d670-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-176">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-177">System-Flags</span></span>           | <span data-ttu-id="6d670-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-178">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-179">Classes used in</span></span>        | [<span data-ttu-id="6d670-180">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6d670-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="6d670-181">ADAM</span></span>



| <span data-ttu-id="6d670-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-182">Entry</span></span> | <span data-ttu-id="6d670-183">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-185">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-186">System-Only</span></span>            | <span data-ttu-id="6d670-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-187">False</span></span>                                                    |
| <span data-ttu-id="6d670-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-189">True</span><span class="sxs-lookup"><span data-stu-id="6d670-189">True</span></span>                                                     |
| <span data-ttu-id="6d670-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-190">Is Indexed</span></span>             | <span data-ttu-id="6d670-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-191">False</span></span>                                                    |
| <span data-ttu-id="6d670-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-192">In Global Catalog</span></span>      | <span data-ttu-id="6d670-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-193">False</span></span>                                                    |
| <span data-ttu-id="6d670-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-196">Range-Lower</span></span>            | <span data-ttu-id="6d670-197">16</span><span class="sxs-lookup"><span data-stu-id="6d670-197">16</span></span>                                                       |
| <span data-ttu-id="6d670-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-198">Range-Upper</span></span>            | <span data-ttu-id="6d670-199">16</span><span class="sxs-lookup"><span data-stu-id="6d670-199">16</span></span>                                                       |
| <span data-ttu-id="6d670-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-200">Search-Flags</span></span>           | <span data-ttu-id="6d670-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-201">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-202">System-Flags</span></span>           | <span data-ttu-id="6d670-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-203">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-204">Classes used in</span></span>        | [<span data-ttu-id="6d670-205">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-205">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d670-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d670-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d670-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-207">Entry</span></span> | <span data-ttu-id="6d670-208">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-208">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-209">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-210">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-211">System-Only</span></span>            | <span data-ttu-id="6d670-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-212">False</span></span>                                                    |
| <span data-ttu-id="6d670-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-214">True</span><span class="sxs-lookup"><span data-stu-id="6d670-214">True</span></span>                                                     |
| <span data-ttu-id="6d670-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-215">Is Indexed</span></span>             | <span data-ttu-id="6d670-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-216">False</span></span>                                                    |
| <span data-ttu-id="6d670-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-217">In Global Catalog</span></span>      | <span data-ttu-id="6d670-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-218">False</span></span>                                                    |
| <span data-ttu-id="6d670-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-221">Range-Lower</span></span>            | <span data-ttu-id="6d670-222">16</span><span class="sxs-lookup"><span data-stu-id="6d670-222">16</span></span>                                                       |
| <span data-ttu-id="6d670-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-223">Range-Upper</span></span>            | <span data-ttu-id="6d670-224">16</span><span class="sxs-lookup"><span data-stu-id="6d670-224">16</span></span>                                                       |
| <span data-ttu-id="6d670-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-225">Search-Flags</span></span>           | <span data-ttu-id="6d670-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-226">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-227">System-Flags</span></span>           | <span data-ttu-id="6d670-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-228">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-229">Classes used in</span></span>        | [<span data-ttu-id="6d670-230">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-230">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d670-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d670-231">Windows Server 2008</span></span>



| <span data-ttu-id="6d670-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-232">Entry</span></span> | <span data-ttu-id="6d670-233">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-233">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-234">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-235">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-236">System-Only</span></span>            | <span data-ttu-id="6d670-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-237">False</span></span>                                                    |
| <span data-ttu-id="6d670-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-238">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-239">True</span><span class="sxs-lookup"><span data-stu-id="6d670-239">True</span></span>                                                     |
| <span data-ttu-id="6d670-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-240">Is Indexed</span></span>             | <span data-ttu-id="6d670-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-241">False</span></span>                                                    |
| <span data-ttu-id="6d670-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-242">In Global Catalog</span></span>      | <span data-ttu-id="6d670-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-243">False</span></span>                                                    |
| <span data-ttu-id="6d670-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-245">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-246">Range-Lower</span></span>            | <span data-ttu-id="6d670-247">16</span><span class="sxs-lookup"><span data-stu-id="6d670-247">16</span></span>                                                       |
| <span data-ttu-id="6d670-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-248">Range-Upper</span></span>            | <span data-ttu-id="6d670-249">16</span><span class="sxs-lookup"><span data-stu-id="6d670-249">16</span></span>                                                       |
| <span data-ttu-id="6d670-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-250">Search-Flags</span></span>           | <span data-ttu-id="6d670-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-251">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-252">System-Flags</span></span>           | <span data-ttu-id="6d670-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-253">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-254">Classes used in</span></span>        | [<span data-ttu-id="6d670-255">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-255">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d670-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d670-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d670-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-257">Entry</span></span> | <span data-ttu-id="6d670-258">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-258">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-259">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-260">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-261">System-Only</span></span>            | <span data-ttu-id="6d670-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-262">False</span></span>                                                    |
| <span data-ttu-id="6d670-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-264">True</span><span class="sxs-lookup"><span data-stu-id="6d670-264">True</span></span>                                                     |
| <span data-ttu-id="6d670-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-265">Is Indexed</span></span>             | <span data-ttu-id="6d670-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-266">False</span></span>                                                    |
| <span data-ttu-id="6d670-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-267">In Global Catalog</span></span>      | <span data-ttu-id="6d670-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-268">False</span></span>                                                    |
| <span data-ttu-id="6d670-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-270">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-271">Range-Lower</span></span>            | <span data-ttu-id="6d670-272">16</span><span class="sxs-lookup"><span data-stu-id="6d670-272">16</span></span>                                                       |
| <span data-ttu-id="6d670-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-273">Range-Upper</span></span>            | <span data-ttu-id="6d670-274">16</span><span class="sxs-lookup"><span data-stu-id="6d670-274">16</span></span>                                                       |
| <span data-ttu-id="6d670-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-275">Search-Flags</span></span>           | <span data-ttu-id="6d670-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-276">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-277">System-Flags</span></span>           | <span data-ttu-id="6d670-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-278">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-279">Classes used in</span></span>        | [<span data-ttu-id="6d670-280">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-280">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d670-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d670-281">Windows Server 2012</span></span>



| <span data-ttu-id="6d670-282">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d670-282">Entry</span></span> | <span data-ttu-id="6d670-283">Значение</span><span class="sxs-lookup"><span data-stu-id="6d670-283">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6d670-284">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6d670-284">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d670-285">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6d670-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d670-286">System-Only</span></span>            | <span data-ttu-id="6d670-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-287">False</span></span>                                                    |
| <span data-ttu-id="6d670-288">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6d670-288">Is-Single-Valued</span></span>       | <span data-ttu-id="6d670-289">True</span><span class="sxs-lookup"><span data-stu-id="6d670-289">True</span></span>                                                     |
| <span data-ttu-id="6d670-290">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6d670-290">Is Indexed</span></span>             | <span data-ttu-id="6d670-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-291">False</span></span>                                                    |
| <span data-ttu-id="6d670-292">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6d670-292">In Global Catalog</span></span>      | <span data-ttu-id="6d670-293">Неверно</span><span class="sxs-lookup"><span data-stu-id="6d670-293">False</span></span>                                                    |
| <span data-ttu-id="6d670-294">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6d670-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d670-295">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d670-295">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6d670-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d670-296">Range-Lower</span></span>            | <span data-ttu-id="6d670-297">16</span><span class="sxs-lookup"><span data-stu-id="6d670-297">16</span></span>                                                       |
| <span data-ttu-id="6d670-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d670-298">Range-Upper</span></span>            | <span data-ttu-id="6d670-299">16</span><span class="sxs-lookup"><span data-stu-id="6d670-299">16</span></span>                                                       |
| <span data-ttu-id="6d670-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-300">Search-Flags</span></span>           | <span data-ttu-id="6d670-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d670-301">0x00000000</span></span>                                               |
| <span data-ttu-id="6d670-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d670-302">System-Flags</span></span>           | <span data-ttu-id="6d670-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d670-303">0x00000010</span></span>                                               |
| <span data-ttu-id="6d670-304">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6d670-304">Classes used in</span></span>        | [<span data-ttu-id="6d670-305">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="6d670-305">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





