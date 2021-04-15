---
title: Атрибут System-вспомогательного класса
description: Список вспомогательных классов, которые не могут быть изменены пользователем.
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута на уровне системы (вспомогательный класс)
- Схема AD атрибута Системауксилиарикласс
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655046"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="be2fb-105">Атрибут System-вспомогательного класса</span><span class="sxs-lookup"><span data-stu-id="be2fb-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="be2fb-106">Список вспомогательных классов, которые не могут быть изменены пользователем.</span><span class="sxs-lookup"><span data-stu-id="be2fb-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="be2fb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-107">Entry</span></span> | <span data-ttu-id="be2fb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="be2fb-109">CN</span><span class="sxs-lookup"><span data-stu-id="be2fb-109">CN</span></span>                | <span data-ttu-id="be2fb-110">Системный-вспомогательный класс</span><span class="sxs-lookup"><span data-stu-id="be2fb-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="be2fb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="be2fb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="be2fb-112">системауксилиарикласс</span><span class="sxs-lookup"><span data-stu-id="be2fb-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="be2fb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="be2fb-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="be2fb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="be2fb-114">Update Privilege</span></span>  | <span data-ttu-id="be2fb-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="be2fb-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="be2fb-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="be2fb-116">Update Frequency</span></span>  | <span data-ttu-id="be2fb-117">При создании класса или добавлении к нему нового вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="be2fb-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="be2fb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-118">Attribute-Id</span></span>      | <span data-ttu-id="be2fb-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="be2fb-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="be2fb-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="be2fb-120">System-Id-Guid</span></span>    | <span data-ttu-id="be2fb-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="be2fb-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="be2fb-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be2fb-122">Syntax</span></span>            | [<span data-ttu-id="be2fb-123">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="be2fb-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="be2fb-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="be2fb-124">Implementations</span></span>

-   [<span data-ttu-id="be2fb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="be2fb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="be2fb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be2fb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be2fb-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="be2fb-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="be2fb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be2fb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be2fb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be2fb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be2fb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be2fb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be2fb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be2fb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="be2fb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be2fb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="be2fb-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-133">Entry</span></span> | <span data-ttu-id="be2fb-134">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-137">System-Only</span></span>            | <span data-ttu-id="be2fb-138">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-138">True</span></span>                                             |
| <span data-ttu-id="be2fb-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-140">False</span></span>                                            |
| <span data-ttu-id="be2fb-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-141">Is Indexed</span></span>             | <span data-ttu-id="be2fb-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-142">False</span></span>                                            |
| <span data-ttu-id="be2fb-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-143">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-144">False</span></span>                                            |
| <span data-ttu-id="be2fb-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-149">Search-Flags</span></span>           | <span data-ttu-id="be2fb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-150">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-151">System-Flags</span></span>           | <span data-ttu-id="be2fb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-152">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-153">Classes used in</span></span>        | [<span data-ttu-id="be2fb-154">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="be2fb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be2fb-155">Windows Server 2003</span></span>



| <span data-ttu-id="be2fb-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-156">Entry</span></span> | <span data-ttu-id="be2fb-157">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-160">System-Only</span></span>            | <span data-ttu-id="be2fb-161">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-161">True</span></span>                                             |
| <span data-ttu-id="be2fb-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-163">False</span></span>                                            |
| <span data-ttu-id="be2fb-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-164">Is Indexed</span></span>             | <span data-ttu-id="be2fb-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-165">False</span></span>                                            |
| <span data-ttu-id="be2fb-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-166">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-167">False</span></span>                                            |
| <span data-ttu-id="be2fb-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-172">Search-Flags</span></span>           | <span data-ttu-id="be2fb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-173">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-174">System-Flags</span></span>           | <span data-ttu-id="be2fb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-175">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-176">Classes used in</span></span>        | [<span data-ttu-id="be2fb-177">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="be2fb-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="be2fb-178">ADAM</span></span>



| <span data-ttu-id="be2fb-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-179">Entry</span></span> | <span data-ttu-id="be2fb-180">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-183">System-Only</span></span>            | <span data-ttu-id="be2fb-184">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-184">True</span></span>                                             |
| <span data-ttu-id="be2fb-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-186">False</span></span>                                            |
| <span data-ttu-id="be2fb-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-187">Is Indexed</span></span>             | <span data-ttu-id="be2fb-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-188">False</span></span>                                            |
| <span data-ttu-id="be2fb-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-189">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-190">False</span></span>                                            |
| <span data-ttu-id="be2fb-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-195">Search-Flags</span></span>           | <span data-ttu-id="be2fb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-196">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-197">System-Flags</span></span>           | <span data-ttu-id="be2fb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-198">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-199">Classes used in</span></span>        | [<span data-ttu-id="be2fb-200">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be2fb-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be2fb-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be2fb-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-202">Entry</span></span> | <span data-ttu-id="be2fb-203">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-206">System-Only</span></span>            | <span data-ttu-id="be2fb-207">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-207">True</span></span>                                             |
| <span data-ttu-id="be2fb-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-209">False</span></span>                                            |
| <span data-ttu-id="be2fb-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-210">Is Indexed</span></span>             | <span data-ttu-id="be2fb-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-211">False</span></span>                                            |
| <span data-ttu-id="be2fb-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-212">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-213">False</span></span>                                            |
| <span data-ttu-id="be2fb-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-218">Search-Flags</span></span>           | <span data-ttu-id="be2fb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-219">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-220">System-Flags</span></span>           | <span data-ttu-id="be2fb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-221">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-222">Classes used in</span></span>        | [<span data-ttu-id="be2fb-223">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be2fb-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be2fb-224">Windows Server 2008</span></span>



| <span data-ttu-id="be2fb-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-225">Entry</span></span> | <span data-ttu-id="be2fb-226">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-229">System-Only</span></span>            | <span data-ttu-id="be2fb-230">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-230">True</span></span>                                             |
| <span data-ttu-id="be2fb-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-232">False</span></span>                                            |
| <span data-ttu-id="be2fb-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-233">Is Indexed</span></span>             | <span data-ttu-id="be2fb-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-234">False</span></span>                                            |
| <span data-ttu-id="be2fb-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-235">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-236">False</span></span>                                            |
| <span data-ttu-id="be2fb-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-241">Search-Flags</span></span>           | <span data-ttu-id="be2fb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-242">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-243">System-Flags</span></span>           | <span data-ttu-id="be2fb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-244">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-245">Classes used in</span></span>        | [<span data-ttu-id="be2fb-246">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be2fb-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be2fb-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be2fb-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-248">Entry</span></span> | <span data-ttu-id="be2fb-249">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-252">System-Only</span></span>            | <span data-ttu-id="be2fb-253">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-253">True</span></span>                                             |
| <span data-ttu-id="be2fb-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-255">False</span></span>                                            |
| <span data-ttu-id="be2fb-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-256">Is Indexed</span></span>             | <span data-ttu-id="be2fb-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-257">False</span></span>                                            |
| <span data-ttu-id="be2fb-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-258">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-259">False</span></span>                                            |
| <span data-ttu-id="be2fb-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-264">Search-Flags</span></span>           | <span data-ttu-id="be2fb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-265">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-266">System-Flags</span></span>           | <span data-ttu-id="be2fb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-267">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-268">Classes used in</span></span>        | [<span data-ttu-id="be2fb-269">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be2fb-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be2fb-270">Windows Server 2012</span></span>



| <span data-ttu-id="be2fb-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="be2fb-271">Entry</span></span> | <span data-ttu-id="be2fb-272">Значение</span><span class="sxs-lookup"><span data-stu-id="be2fb-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be2fb-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be2fb-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be2fb-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="be2fb-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="be2fb-275">System-Only</span></span>            | <span data-ttu-id="be2fb-276">True</span><span class="sxs-lookup"><span data-stu-id="be2fb-276">True</span></span>                                             |
| <span data-ttu-id="be2fb-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be2fb-277">Is-Single-Valued</span></span>       | <span data-ttu-id="be2fb-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-278">False</span></span>                                            |
| <span data-ttu-id="be2fb-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be2fb-279">Is Indexed</span></span>             | <span data-ttu-id="be2fb-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-280">False</span></span>                                            |
| <span data-ttu-id="be2fb-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be2fb-281">In Global Catalog</span></span>      | <span data-ttu-id="be2fb-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="be2fb-282">False</span></span>                                            |
| <span data-ttu-id="be2fb-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be2fb-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="be2fb-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be2fb-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be2fb-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be2fb-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be2fb-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="be2fb-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-287">Search-Flags</span></span>           | <span data-ttu-id="be2fb-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be2fb-288">0x00000000</span></span>                                       |
| <span data-ttu-id="be2fb-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be2fb-289">System-Flags</span></span>           | <span data-ttu-id="be2fb-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be2fb-290">0x00000010</span></span>                                       |
| <span data-ttu-id="be2fb-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be2fb-291">Classes used in</span></span>        | [<span data-ttu-id="be2fb-292">**Class-schema**</span><span class="sxs-lookup"><span data-stu-id="be2fb-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





