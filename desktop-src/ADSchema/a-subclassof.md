---
title: Атрибут вспомогательного класса
description: Родительский класс класса.
ms.assetid: ff2afb13-5d72-4b8b-9e66-c16fb0ae5e88
ms.tgt_platform: multiple
keywords:
- Схема AD вспомогательного класса атрибута
- Схема AD атрибута списках subClassOf
topic_type:
- apiref
api_name:
- Sub-Class-Of
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90c1e431e8c1e501731070359d379436973ef67
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138451"
---
# <a name="sub-class-of-attribute"></a><span data-ttu-id="6190f-105">Атрибут вспомогательного класса</span><span class="sxs-lookup"><span data-stu-id="6190f-105">Sub-Class-Of attribute</span></span>

<span data-ttu-id="6190f-106">Родительский класс класса.</span><span class="sxs-lookup"><span data-stu-id="6190f-106">The parent class of a class.</span></span>



| <span data-ttu-id="6190f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-107">Entry</span></span> | <span data-ttu-id="6190f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6190f-109">CN</span><span class="sxs-lookup"><span data-stu-id="6190f-109">CN</span></span>                | <span data-ttu-id="6190f-110">Вспомогательный класс</span><span class="sxs-lookup"><span data-stu-id="6190f-110">Sub-Class-Of</span></span>                                                    |
| <span data-ttu-id="6190f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6190f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6190f-112">subClassOf</span><span class="sxs-lookup"><span data-stu-id="6190f-112">subClassOf</span></span>                                                      |
| <span data-ttu-id="6190f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6190f-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="6190f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6190f-114">Update Privilege</span></span>  | <span data-ttu-id="6190f-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="6190f-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="6190f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6190f-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="6190f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-117">Attribute-Id</span></span>      | <span data-ttu-id="6190f-118">1.2.840.113556.1.2.21</span><span class="sxs-lookup"><span data-stu-id="6190f-118">1.2.840.113556.1.2.21</span></span>                                           |
| <span data-ttu-id="6190f-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6190f-119">System-Id-Guid</span></span>    | <span data-ttu-id="6190f-120">bf967a3b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6190f-120">bf967a3b-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="6190f-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6190f-121">Syntax</span></span>            | [<span data-ttu-id="6190f-122">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="6190f-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="6190f-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6190f-123">Implementations</span></span>

-   [<span data-ttu-id="6190f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6190f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6190f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6190f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6190f-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6190f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6190f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6190f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6190f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6190f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6190f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6190f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6190f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6190f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6190f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6190f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6190f-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-132">Entry</span></span> | <span data-ttu-id="6190f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-136">System-Only</span></span>            | <span data-ttu-id="6190f-137">True</span><span class="sxs-lookup"><span data-stu-id="6190f-137">True</span></span>                                             |
| <span data-ttu-id="6190f-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-139">True</span><span class="sxs-lookup"><span data-stu-id="6190f-139">True</span></span>                                             |
| <span data-ttu-id="6190f-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-140">Is Indexed</span></span>             | <span data-ttu-id="6190f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-141">False</span></span>                                            |
| <span data-ttu-id="6190f-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-142">In Global Catalog</span></span>      | <span data-ttu-id="6190f-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-143">False</span></span>                                            |
| <span data-ttu-id="6190f-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-148">Search-Flags</span></span>           | <span data-ttu-id="6190f-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-149">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-150">System-Flags</span></span>           | <span data-ttu-id="6190f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-151">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-152">Classes used in</span></span>        | [<span data-ttu-id="6190f-153">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6190f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6190f-154">Windows Server 2003</span></span>



| <span data-ttu-id="6190f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-155">Entry</span></span> | <span data-ttu-id="6190f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-159">System-Only</span></span>            | <span data-ttu-id="6190f-160">True</span><span class="sxs-lookup"><span data-stu-id="6190f-160">True</span></span>                                             |
| <span data-ttu-id="6190f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-162">True</span><span class="sxs-lookup"><span data-stu-id="6190f-162">True</span></span>                                             |
| <span data-ttu-id="6190f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-163">Is Indexed</span></span>             | <span data-ttu-id="6190f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-164">False</span></span>                                            |
| <span data-ttu-id="6190f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-165">In Global Catalog</span></span>      | <span data-ttu-id="6190f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-166">False</span></span>                                            |
| <span data-ttu-id="6190f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-171">Search-Flags</span></span>           | <span data-ttu-id="6190f-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-172">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-173">System-Flags</span></span>           | <span data-ttu-id="6190f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-174">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-175">Classes used in</span></span>        | [<span data-ttu-id="6190f-176">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6190f-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="6190f-177">ADAM</span></span>



| <span data-ttu-id="6190f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-178">Entry</span></span> | <span data-ttu-id="6190f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-182">System-Only</span></span>            | <span data-ttu-id="6190f-183">True</span><span class="sxs-lookup"><span data-stu-id="6190f-183">True</span></span>                                             |
| <span data-ttu-id="6190f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-185">True</span><span class="sxs-lookup"><span data-stu-id="6190f-185">True</span></span>                                             |
| <span data-ttu-id="6190f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-186">Is Indexed</span></span>             | <span data-ttu-id="6190f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-187">False</span></span>                                            |
| <span data-ttu-id="6190f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-188">In Global Catalog</span></span>      | <span data-ttu-id="6190f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-189">False</span></span>                                            |
| <span data-ttu-id="6190f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-194">Search-Flags</span></span>           | <span data-ttu-id="6190f-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-195">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-196">System-Flags</span></span>           | <span data-ttu-id="6190f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-197">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-198">Classes used in</span></span>        | [<span data-ttu-id="6190f-199">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6190f-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6190f-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6190f-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-201">Entry</span></span> | <span data-ttu-id="6190f-202">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-205">System-Only</span></span>            | <span data-ttu-id="6190f-206">True</span><span class="sxs-lookup"><span data-stu-id="6190f-206">True</span></span>                                             |
| <span data-ttu-id="6190f-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-208">True</span><span class="sxs-lookup"><span data-stu-id="6190f-208">True</span></span>                                             |
| <span data-ttu-id="6190f-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-209">Is Indexed</span></span>             | <span data-ttu-id="6190f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-210">False</span></span>                                            |
| <span data-ttu-id="6190f-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-211">In Global Catalog</span></span>      | <span data-ttu-id="6190f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-212">False</span></span>                                            |
| <span data-ttu-id="6190f-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-217">Search-Flags</span></span>           | <span data-ttu-id="6190f-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-218">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-219">System-Flags</span></span>           | <span data-ttu-id="6190f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-220">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-221">Classes used in</span></span>        | [<span data-ttu-id="6190f-222">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6190f-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6190f-223">Windows Server 2008</span></span>



| <span data-ttu-id="6190f-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-224">Entry</span></span> | <span data-ttu-id="6190f-225">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-228">System-Only</span></span>            | <span data-ttu-id="6190f-229">True</span><span class="sxs-lookup"><span data-stu-id="6190f-229">True</span></span>                                             |
| <span data-ttu-id="6190f-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-231">True</span><span class="sxs-lookup"><span data-stu-id="6190f-231">True</span></span>                                             |
| <span data-ttu-id="6190f-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-232">Is Indexed</span></span>             | <span data-ttu-id="6190f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-233">False</span></span>                                            |
| <span data-ttu-id="6190f-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-234">In Global Catalog</span></span>      | <span data-ttu-id="6190f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-235">False</span></span>                                            |
| <span data-ttu-id="6190f-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-240">Search-Flags</span></span>           | <span data-ttu-id="6190f-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-241">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-242">System-Flags</span></span>           | <span data-ttu-id="6190f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-243">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-244">Classes used in</span></span>        | [<span data-ttu-id="6190f-245">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6190f-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6190f-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6190f-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-247">Entry</span></span> | <span data-ttu-id="6190f-248">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-251">System-Only</span></span>            | <span data-ttu-id="6190f-252">True</span><span class="sxs-lookup"><span data-stu-id="6190f-252">True</span></span>                                             |
| <span data-ttu-id="6190f-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-254">True</span><span class="sxs-lookup"><span data-stu-id="6190f-254">True</span></span>                                             |
| <span data-ttu-id="6190f-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-255">Is Indexed</span></span>             | <span data-ttu-id="6190f-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-256">False</span></span>                                            |
| <span data-ttu-id="6190f-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-257">In Global Catalog</span></span>      | <span data-ttu-id="6190f-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-258">False</span></span>                                            |
| <span data-ttu-id="6190f-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-263">Search-Flags</span></span>           | <span data-ttu-id="6190f-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-264">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-265">System-Flags</span></span>           | <span data-ttu-id="6190f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-266">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-267">Classes used in</span></span>        | [<span data-ttu-id="6190f-268">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6190f-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6190f-269">Windows Server 2012</span></span>



| <span data-ttu-id="6190f-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="6190f-270">Entry</span></span> | <span data-ttu-id="6190f-271">Значение</span><span class="sxs-lookup"><span data-stu-id="6190f-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6190f-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6190f-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6190f-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6190f-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="6190f-274">System-Only</span></span>            | <span data-ttu-id="6190f-275">True</span><span class="sxs-lookup"><span data-stu-id="6190f-275">True</span></span>                                             |
| <span data-ttu-id="6190f-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6190f-276">Is-Single-Valued</span></span>       | <span data-ttu-id="6190f-277">True</span><span class="sxs-lookup"><span data-stu-id="6190f-277">True</span></span>                                             |
| <span data-ttu-id="6190f-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6190f-278">Is Indexed</span></span>             | <span data-ttu-id="6190f-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-279">False</span></span>                                            |
| <span data-ttu-id="6190f-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6190f-280">In Global Catalog</span></span>      | <span data-ttu-id="6190f-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="6190f-281">False</span></span>                                            |
| <span data-ttu-id="6190f-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6190f-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="6190f-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6190f-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6190f-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6190f-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6190f-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6190f-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6190f-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-286">Search-Flags</span></span>           | <span data-ttu-id="6190f-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6190f-287">0x00000008</span></span>                                       |
| <span data-ttu-id="6190f-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6190f-288">System-Flags</span></span>           | <span data-ttu-id="6190f-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6190f-289">0x00000010</span></span>                                       |
| <span data-ttu-id="6190f-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6190f-290">Classes used in</span></span>        | [<span data-ttu-id="6190f-291">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="6190f-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





