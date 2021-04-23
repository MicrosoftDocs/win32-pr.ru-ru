---
title: атрибут MS-RRAS-Vendor-Attribute-Entry
description: Строка, позволяющая поставщикам добавлять в DS атрибуты маршрутизатора для использования в запросах в формате AttributeName vendorID AttributeType.
ms.assetid: 07bc4d9b-eba9-456b-be21-cd7bb8a5b0b6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута входа MS-RRAS-Vendor-Attribute
- Схема AD атрибута Мсррасвендораттрибутинтри
topic_type:
- apiref
api_name:
- ms-RRAS-Vendor-Attribute-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ee353122107db5b1247860e9799db861b4d6bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493770"
---
# <a name="ms-rras-vendor-attribute-entry-attribute"></a><span data-ttu-id="d64b7-105">атрибут MS-RRAS-Vendor-Attribute-Entry</span><span class="sxs-lookup"><span data-stu-id="d64b7-105">ms-RRAS-Vendor-Attribute-Entry attribute</span></span>

<span data-ttu-id="d64b7-106">Строка, позволяющая поставщикам добавлять в DS атрибуты маршрутизатора для использования в запросах в формате AttributeName: vendorID: AttributeType.</span><span class="sxs-lookup"><span data-stu-id="d64b7-106">A string that enables vendors to add router attributes to the DS for use in queries, in the form AttributeName:vendorID:AttributeType.</span></span>



| <span data-ttu-id="d64b7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-107">Entry</span></span> | <span data-ttu-id="d64b7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d64b7-109">CN</span><span class="sxs-lookup"><span data-stu-id="d64b7-109">CN</span></span>                | <span data-ttu-id="d64b7-110">MS-RRAS-Vendor-Attribute-Entry</span><span class="sxs-lookup"><span data-stu-id="d64b7-110">ms-RRAS-Vendor-Attribute-Entry</span></span>              |
| <span data-ttu-id="d64b7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d64b7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d64b7-112">мсррасвендораттрибутинтри</span><span class="sxs-lookup"><span data-stu-id="d64b7-112">msRRASVendorAttributeEntry</span></span>                  |
| <span data-ttu-id="d64b7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d64b7-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d64b7-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d64b7-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d64b7-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d64b7-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d64b7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-116">Attribute-Id</span></span>      | <span data-ttu-id="d64b7-117">1.2.840.113556.1.4.883</span><span class="sxs-lookup"><span data-stu-id="d64b7-117">1.2.840.113556.1.4.883</span></span>                      |
| <span data-ttu-id="d64b7-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d64b7-118">System-Id-Guid</span></span>    | <span data-ttu-id="d64b7-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d64b7-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span></span>        |
| <span data-ttu-id="d64b7-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d64b7-120">Syntax</span></span>            | [<span data-ttu-id="d64b7-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d64b7-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d64b7-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d64b7-122">Implementations</span></span>

-   [<span data-ttu-id="d64b7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d64b7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d64b7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d64b7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d64b7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d64b7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d64b7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d64b7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d64b7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d64b7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d64b7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d64b7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d64b7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d64b7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="d64b7-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-130">Entry</span></span> | <span data-ttu-id="d64b7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b7-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d64b7-132">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-133">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="d64b7-134">System-Only</span></span>            | <span data-ttu-id="d64b7-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-135">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d64b7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="d64b7-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-137">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d64b7-138">Is Indexed</span></span>             | <span data-ttu-id="d64b7-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-139">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d64b7-140">In Global Catalog</span></span>      | <span data-ttu-id="d64b7-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-141">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d64b7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="d64b7-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d64b7-143">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="d64b7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d64b7-144">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d64b7-145">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-146">Search-Flags</span></span>           | <span data-ttu-id="d64b7-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d64b7-147">0x00000000</span></span>                                                                          |
| <span data-ttu-id="d64b7-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-148">System-Flags</span></span>           | <span data-ttu-id="d64b7-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d64b7-149">0x00000010</span></span>                                                                          |
| <span data-ttu-id="d64b7-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d64b7-150">Classes used in</span></span>        | [<span data-ttu-id="d64b7-151">**RRAS-Admin-Dictionary**</span><span class="sxs-lookup"><span data-stu-id="d64b7-151">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d64b7-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d64b7-152">Windows Server 2003</span></span>



| <span data-ttu-id="d64b7-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-153">Entry</span></span> | <span data-ttu-id="d64b7-154">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b7-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d64b7-155">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-156">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="d64b7-157">System-Only</span></span>            | <span data-ttu-id="d64b7-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-158">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d64b7-159">Is-Single-Valued</span></span>       | <span data-ttu-id="d64b7-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-160">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d64b7-161">Is Indexed</span></span>             | <span data-ttu-id="d64b7-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-162">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d64b7-163">In Global Catalog</span></span>      | <span data-ttu-id="d64b7-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-164">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d64b7-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="d64b7-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d64b7-166">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="d64b7-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d64b7-167">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d64b7-168">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-169">Search-Flags</span></span>           | <span data-ttu-id="d64b7-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d64b7-170">0x00000000</span></span>                                                                          |
| <span data-ttu-id="d64b7-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-171">System-Flags</span></span>           | <span data-ttu-id="d64b7-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d64b7-172">0x00000010</span></span>                                                                          |
| <span data-ttu-id="d64b7-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d64b7-173">Classes used in</span></span>        | [<span data-ttu-id="d64b7-174">**RRAS-Admin-Dictionary**</span><span class="sxs-lookup"><span data-stu-id="d64b7-174">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d64b7-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d64b7-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d64b7-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-176">Entry</span></span> | <span data-ttu-id="d64b7-177">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b7-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d64b7-178">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-179">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="d64b7-180">System-Only</span></span>            | <span data-ttu-id="d64b7-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-181">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d64b7-182">Is-Single-Valued</span></span>       | <span data-ttu-id="d64b7-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-183">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d64b7-184">Is Indexed</span></span>             | <span data-ttu-id="d64b7-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-185">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d64b7-186">In Global Catalog</span></span>      | <span data-ttu-id="d64b7-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-187">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d64b7-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="d64b7-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d64b7-189">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="d64b7-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d64b7-190">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d64b7-191">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-192">Search-Flags</span></span>           | <span data-ttu-id="d64b7-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d64b7-193">0x00000000</span></span>                                                                          |
| <span data-ttu-id="d64b7-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-194">System-Flags</span></span>           | <span data-ttu-id="d64b7-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d64b7-195">0x00000010</span></span>                                                                          |
| <span data-ttu-id="d64b7-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d64b7-196">Classes used in</span></span>        | [<span data-ttu-id="d64b7-197">**RRAS-Admin-Dictionary**</span><span class="sxs-lookup"><span data-stu-id="d64b7-197">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d64b7-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d64b7-198">Windows Server 2008</span></span>



| <span data-ttu-id="d64b7-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-199">Entry</span></span> | <span data-ttu-id="d64b7-200">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b7-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d64b7-201">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-202">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="d64b7-203">System-Only</span></span>            | <span data-ttu-id="d64b7-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-204">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d64b7-205">Is-Single-Valued</span></span>       | <span data-ttu-id="d64b7-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-206">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d64b7-207">Is Indexed</span></span>             | <span data-ttu-id="d64b7-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-208">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d64b7-209">In Global Catalog</span></span>      | <span data-ttu-id="d64b7-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-210">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d64b7-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="d64b7-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d64b7-212">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="d64b7-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d64b7-213">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d64b7-214">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-215">Search-Flags</span></span>           | <span data-ttu-id="d64b7-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d64b7-216">0x00000000</span></span>                                                                          |
| <span data-ttu-id="d64b7-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-217">System-Flags</span></span>           | <span data-ttu-id="d64b7-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d64b7-218">0x00000010</span></span>                                                                          |
| <span data-ttu-id="d64b7-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d64b7-219">Classes used in</span></span>        | [<span data-ttu-id="d64b7-220">**RRAS-Admin-Dictionary**</span><span class="sxs-lookup"><span data-stu-id="d64b7-220">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d64b7-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d64b7-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d64b7-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-222">Entry</span></span> | <span data-ttu-id="d64b7-223">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b7-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d64b7-224">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-225">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="d64b7-226">System-Only</span></span>            | <span data-ttu-id="d64b7-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-227">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d64b7-228">Is-Single-Valued</span></span>       | <span data-ttu-id="d64b7-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-229">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d64b7-230">Is Indexed</span></span>             | <span data-ttu-id="d64b7-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-231">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d64b7-232">In Global Catalog</span></span>      | <span data-ttu-id="d64b7-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-233">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d64b7-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="d64b7-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d64b7-235">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="d64b7-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d64b7-236">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d64b7-237">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-238">Search-Flags</span></span>           | <span data-ttu-id="d64b7-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d64b7-239">0x00000000</span></span>                                                                          |
| <span data-ttu-id="d64b7-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-240">System-Flags</span></span>           | <span data-ttu-id="d64b7-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d64b7-241">0x00000010</span></span>                                                                          |
| <span data-ttu-id="d64b7-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d64b7-242">Classes used in</span></span>        | [<span data-ttu-id="d64b7-243">**RRAS-Admin-Dictionary**</span><span class="sxs-lookup"><span data-stu-id="d64b7-243">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d64b7-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d64b7-244">Windows Server 2012</span></span>



| <span data-ttu-id="d64b7-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b7-245">Entry</span></span> | <span data-ttu-id="d64b7-246">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b7-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b7-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d64b7-247">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d64b7-248">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="d64b7-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="d64b7-249">System-Only</span></span>            | <span data-ttu-id="d64b7-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-250">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d64b7-251">Is-Single-Valued</span></span>       | <span data-ttu-id="d64b7-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-252">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d64b7-253">Is Indexed</span></span>             | <span data-ttu-id="d64b7-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-254">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d64b7-255">In Global Catalog</span></span>      | <span data-ttu-id="d64b7-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="d64b7-256">False</span></span>                                                                               |
| <span data-ttu-id="d64b7-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d64b7-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="d64b7-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d64b7-258">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="d64b7-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d64b7-259">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d64b7-260">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="d64b7-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-261">Search-Flags</span></span>           | <span data-ttu-id="d64b7-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d64b7-262">0x00000000</span></span>                                                                          |
| <span data-ttu-id="d64b7-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d64b7-263">System-Flags</span></span>           | <span data-ttu-id="d64b7-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d64b7-264">0x00000010</span></span>                                                                          |
| <span data-ttu-id="d64b7-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d64b7-265">Classes used in</span></span>        | [<span data-ttu-id="d64b7-266">**RRAS-Admin-Dictionary**</span><span class="sxs-lookup"><span data-stu-id="d64b7-266">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



 

 





