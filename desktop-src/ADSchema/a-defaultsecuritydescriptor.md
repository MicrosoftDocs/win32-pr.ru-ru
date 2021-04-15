---
title: Атрибут-дескриптор безопасности по умолчанию
description: Дескриптор безопасности, назначаемый объекту при его первом создании.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута по умолчанию для дескрипторов безопасности
- Схема AD атрибута Дефаултсекуритидескриптор
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493551"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="bacb9-105">Атрибут-дескриптор безопасности по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bacb9-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="bacb9-106">Дескриптор безопасности, назначаемый объекту при его первом создании.</span><span class="sxs-lookup"><span data-stu-id="bacb9-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="bacb9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-107">Entry</span></span> | <span data-ttu-id="bacb9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bacb9-109">CN</span><span class="sxs-lookup"><span data-stu-id="bacb9-109">CN</span></span>                | <span data-ttu-id="bacb9-110">Дескриптор безопасности по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bacb9-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="bacb9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bacb9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bacb9-112">дефаултсекуритидескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="bacb9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="bacb9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bacb9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bacb9-114">Update Privilege</span></span>  | <span data-ttu-id="bacb9-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="bacb9-115">Schema administrator</span></span>                        |
| <span data-ttu-id="bacb9-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bacb9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bacb9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-117">Attribute-Id</span></span>      | <span data-ttu-id="bacb9-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="bacb9-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="bacb9-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bacb9-119">System-Id-Guid</span></span>    | <span data-ttu-id="bacb9-120">807a6d30-1669-11d0-a064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="bacb9-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="bacb9-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bacb9-121">Syntax</span></span>            | [<span data-ttu-id="bacb9-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="bacb9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bacb9-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bacb9-123">Implementations</span></span>

-   [<span data-ttu-id="bacb9-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bacb9-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bacb9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bacb9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bacb9-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bacb9-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bacb9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bacb9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bacb9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bacb9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bacb9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bacb9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bacb9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bacb9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bacb9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bacb9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bacb9-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-132">Entry</span></span> | <span data-ttu-id="bacb9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-136">System-Only</span></span>            | <span data-ttu-id="bacb9-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-137">False</span></span>                                            |
| <span data-ttu-id="bacb9-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-139">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-139">True</span></span>                                             |
| <span data-ttu-id="bacb9-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-140">Is Indexed</span></span>             | <span data-ttu-id="bacb9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-141">False</span></span>                                            |
| <span data-ttu-id="bacb9-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-142">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-143">False</span></span>                                            |
| <span data-ttu-id="bacb9-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-146">Range-Lower</span></span>            | <span data-ttu-id="bacb9-147">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-147">0</span></span>                                                |
| <span data-ttu-id="bacb9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-148">Range-Upper</span></span>            | <span data-ttu-id="bacb9-149">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-149">32767</span></span>                                            |
| <span data-ttu-id="bacb9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-150">Search-Flags</span></span>           | <span data-ttu-id="bacb9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-151">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-152">System-Flags</span></span>           | <span data-ttu-id="bacb9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-153">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-154">Classes used in</span></span>        | [<span data-ttu-id="bacb9-155">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bacb9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bacb9-156">Windows Server 2003</span></span>



| <span data-ttu-id="bacb9-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-157">Entry</span></span> | <span data-ttu-id="bacb9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-161">System-Only</span></span>            | <span data-ttu-id="bacb9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-162">False</span></span>                                            |
| <span data-ttu-id="bacb9-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-164">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-164">True</span></span>                                             |
| <span data-ttu-id="bacb9-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-165">Is Indexed</span></span>             | <span data-ttu-id="bacb9-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-166">False</span></span>                                            |
| <span data-ttu-id="bacb9-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-167">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-168">False</span></span>                                            |
| <span data-ttu-id="bacb9-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-171">Range-Lower</span></span>            | <span data-ttu-id="bacb9-172">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-172">0</span></span>                                                |
| <span data-ttu-id="bacb9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-173">Range-Upper</span></span>            | <span data-ttu-id="bacb9-174">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-174">32767</span></span>                                            |
| <span data-ttu-id="bacb9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-175">Search-Flags</span></span>           | <span data-ttu-id="bacb9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-176">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-177">System-Flags</span></span>           | <span data-ttu-id="bacb9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-178">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-179">Classes used in</span></span>        | [<span data-ttu-id="bacb9-180">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bacb9-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="bacb9-181">ADAM</span></span>



| <span data-ttu-id="bacb9-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-182">Entry</span></span> | <span data-ttu-id="bacb9-183">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-186">System-Only</span></span>            | <span data-ttu-id="bacb9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-187">False</span></span>                                            |
| <span data-ttu-id="bacb9-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-189">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-189">True</span></span>                                             |
| <span data-ttu-id="bacb9-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-190">Is Indexed</span></span>             | <span data-ttu-id="bacb9-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-191">False</span></span>                                            |
| <span data-ttu-id="bacb9-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-192">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-193">False</span></span>                                            |
| <span data-ttu-id="bacb9-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-196">Range-Lower</span></span>            | <span data-ttu-id="bacb9-197">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-197">0</span></span>                                                |
| <span data-ttu-id="bacb9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-198">Range-Upper</span></span>            | <span data-ttu-id="bacb9-199">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-199">32767</span></span>                                            |
| <span data-ttu-id="bacb9-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-200">Search-Flags</span></span>           | <span data-ttu-id="bacb9-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-201">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-202">System-Flags</span></span>           | <span data-ttu-id="bacb9-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-203">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-204">Classes used in</span></span>        | [<span data-ttu-id="bacb9-205">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bacb9-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bacb9-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bacb9-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-207">Entry</span></span> | <span data-ttu-id="bacb9-208">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-211">System-Only</span></span>            | <span data-ttu-id="bacb9-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-212">False</span></span>                                            |
| <span data-ttu-id="bacb9-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-214">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-214">True</span></span>                                             |
| <span data-ttu-id="bacb9-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-215">Is Indexed</span></span>             | <span data-ttu-id="bacb9-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-216">False</span></span>                                            |
| <span data-ttu-id="bacb9-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-217">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-218">False</span></span>                                            |
| <span data-ttu-id="bacb9-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-221">Range-Lower</span></span>            | <span data-ttu-id="bacb9-222">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-222">0</span></span>                                                |
| <span data-ttu-id="bacb9-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-223">Range-Upper</span></span>            | <span data-ttu-id="bacb9-224">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-224">32767</span></span>                                            |
| <span data-ttu-id="bacb9-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-225">Search-Flags</span></span>           | <span data-ttu-id="bacb9-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-226">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-227">System-Flags</span></span>           | <span data-ttu-id="bacb9-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-228">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-229">Classes used in</span></span>        | [<span data-ttu-id="bacb9-230">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bacb9-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bacb9-231">Windows Server 2008</span></span>



| <span data-ttu-id="bacb9-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-232">Entry</span></span> | <span data-ttu-id="bacb9-233">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-236">System-Only</span></span>            | <span data-ttu-id="bacb9-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-237">False</span></span>                                            |
| <span data-ttu-id="bacb9-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-239">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-239">True</span></span>                                             |
| <span data-ttu-id="bacb9-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-240">Is Indexed</span></span>             | <span data-ttu-id="bacb9-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-241">False</span></span>                                            |
| <span data-ttu-id="bacb9-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-242">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-243">False</span></span>                                            |
| <span data-ttu-id="bacb9-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-246">Range-Lower</span></span>            | <span data-ttu-id="bacb9-247">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-247">0</span></span>                                                |
| <span data-ttu-id="bacb9-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-248">Range-Upper</span></span>            | <span data-ttu-id="bacb9-249">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-249">32767</span></span>                                            |
| <span data-ttu-id="bacb9-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-250">Search-Flags</span></span>           | <span data-ttu-id="bacb9-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-251">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-252">System-Flags</span></span>           | <span data-ttu-id="bacb9-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-253">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-254">Classes used in</span></span>        | [<span data-ttu-id="bacb9-255">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bacb9-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bacb9-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bacb9-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-257">Entry</span></span> | <span data-ttu-id="bacb9-258">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-261">System-Only</span></span>            | <span data-ttu-id="bacb9-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-262">False</span></span>                                            |
| <span data-ttu-id="bacb9-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-264">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-264">True</span></span>                                             |
| <span data-ttu-id="bacb9-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-265">Is Indexed</span></span>             | <span data-ttu-id="bacb9-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-266">False</span></span>                                            |
| <span data-ttu-id="bacb9-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-267">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-268">False</span></span>                                            |
| <span data-ttu-id="bacb9-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-271">Range-Lower</span></span>            | <span data-ttu-id="bacb9-272">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-272">0</span></span>                                                |
| <span data-ttu-id="bacb9-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-273">Range-Upper</span></span>            | <span data-ttu-id="bacb9-274">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-274">32767</span></span>                                            |
| <span data-ttu-id="bacb9-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-275">Search-Flags</span></span>           | <span data-ttu-id="bacb9-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-276">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-277">System-Flags</span></span>           | <span data-ttu-id="bacb9-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-278">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-279">Classes used in</span></span>        | [<span data-ttu-id="bacb9-280">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bacb9-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bacb9-281">Windows Server 2012</span></span>



| <span data-ttu-id="bacb9-282">Ввод</span><span class="sxs-lookup"><span data-stu-id="bacb9-282">Entry</span></span> | <span data-ttu-id="bacb9-283">Значение</span><span class="sxs-lookup"><span data-stu-id="bacb9-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bacb9-284">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bacb9-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bacb9-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bacb9-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="bacb9-286">System-Only</span></span>            | <span data-ttu-id="bacb9-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-287">False</span></span>                                            |
| <span data-ttu-id="bacb9-288">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bacb9-288">Is-Single-Valued</span></span>       | <span data-ttu-id="bacb9-289">True</span><span class="sxs-lookup"><span data-stu-id="bacb9-289">True</span></span>                                             |
| <span data-ttu-id="bacb9-290">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bacb9-290">Is Indexed</span></span>             | <span data-ttu-id="bacb9-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-291">False</span></span>                                            |
| <span data-ttu-id="bacb9-292">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bacb9-292">In Global Catalog</span></span>      | <span data-ttu-id="bacb9-293">Неверно</span><span class="sxs-lookup"><span data-stu-id="bacb9-293">False</span></span>                                            |
| <span data-ttu-id="bacb9-294">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bacb9-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="bacb9-295">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bacb9-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bacb9-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bacb9-296">Range-Lower</span></span>            | <span data-ttu-id="bacb9-297">0</span><span class="sxs-lookup"><span data-stu-id="bacb9-297">0</span></span>                                                |
| <span data-ttu-id="bacb9-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bacb9-298">Range-Upper</span></span>            | <span data-ttu-id="bacb9-299">32767</span><span class="sxs-lookup"><span data-stu-id="bacb9-299">32767</span></span>                                            |
| <span data-ttu-id="bacb9-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-300">Search-Flags</span></span>           | <span data-ttu-id="bacb9-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bacb9-301">0x00000000</span></span>                                       |
| <span data-ttu-id="bacb9-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bacb9-302">System-Flags</span></span>           | <span data-ttu-id="bacb9-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bacb9-303">0x00000010</span></span>                                       |
| <span data-ttu-id="bacb9-304">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bacb9-304">Classes used in</span></span>        | [<span data-ttu-id="bacb9-305">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="bacb9-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





