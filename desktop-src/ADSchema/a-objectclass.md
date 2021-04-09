---
title: Атрибут Object-Class
description: Список классов, производным от которого является этот класс.
ms.assetid: def98723-2d8a-49ea-84f8-afe6ff9cdfd9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Class
- Схема AD атрибута objectClass
topic_type:
- apiref
api_name:
- Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851d48bcbcc40640af3ee555c343feaab05edf6b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138818"
---
# <a name="object-class-attribute"></a><span data-ttu-id="c6916-105">Атрибут Object-Class</span><span class="sxs-lookup"><span data-stu-id="c6916-105">Object-Class attribute</span></span>

<span data-ttu-id="c6916-106">Список классов, производным от которого является этот класс.</span><span class="sxs-lookup"><span data-stu-id="c6916-106">The list of classes from which this class is derived.</span></span>



| <span data-ttu-id="c6916-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-107">Entry</span></span> | <span data-ttu-id="c6916-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c6916-109">CN</span><span class="sxs-lookup"><span data-stu-id="c6916-109">CN</span></span>                | <span data-ttu-id="c6916-110">Object-Class</span><span class="sxs-lookup"><span data-stu-id="c6916-110">Object-Class</span></span>                                                    |
| <span data-ttu-id="c6916-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c6916-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c6916-112">objectClass</span><span class="sxs-lookup"><span data-stu-id="c6916-112">objectClass</span></span>                                                     |
| <span data-ttu-id="c6916-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c6916-113">Size</span></span>              | <span data-ttu-id="c6916-114">Примерно 20 байт в среднем.</span><span class="sxs-lookup"><span data-stu-id="c6916-114">About 20 bytes on average.</span></span>                                      |
| <span data-ttu-id="c6916-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c6916-115">Update Privilege</span></span>  | <span data-ttu-id="c6916-116">Это значение задается конструктором объекта.</span><span class="sxs-lookup"><span data-stu-id="c6916-116">The designer of the object would set this value.</span></span>                |
| <span data-ttu-id="c6916-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c6916-117">Update Frequency</span></span>  | <span data-ttu-id="c6916-118">Это значение никогда не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="c6916-118">This value should never change.</span></span>                                 |
| <span data-ttu-id="c6916-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-119">Attribute-Id</span></span>      | <span data-ttu-id="c6916-120">2.5.4.0</span><span class="sxs-lookup"><span data-stu-id="c6916-120">2.5.4.0</span></span>                                                         |
| <span data-ttu-id="c6916-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c6916-121">System-Id-Guid</span></span>    | <span data-ttu-id="c6916-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c6916-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="c6916-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6916-123">Syntax</span></span>            | [<span data-ttu-id="c6916-124">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="c6916-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="c6916-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c6916-125">Implementations</span></span>

-   [<span data-ttu-id="c6916-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c6916-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c6916-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c6916-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c6916-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c6916-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c6916-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c6916-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c6916-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c6916-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c6916-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c6916-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c6916-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c6916-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c6916-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6916-133">Windows 2000 Server</span></span>



| <span data-ttu-id="c6916-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-134">Entry</span></span> | <span data-ttu-id="c6916-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-138">System-Only</span></span>            | <span data-ttu-id="c6916-139">True</span><span class="sxs-lookup"><span data-stu-id="c6916-139">True</span></span>                            |
| <span data-ttu-id="c6916-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-141">False</span></span>                           |
| <span data-ttu-id="c6916-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-142">Is Indexed</span></span>             | <span data-ttu-id="c6916-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-143">False</span></span>                           |
| <span data-ttu-id="c6916-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-144">In Global Catalog</span></span>      | <span data-ttu-id="c6916-145">True</span><span class="sxs-lookup"><span data-stu-id="c6916-145">True</span></span>                            |
| <span data-ttu-id="c6916-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-150">Search-Flags</span></span>           | <span data-ttu-id="c6916-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c6916-151">0x00000008</span></span>                      |
| <span data-ttu-id="c6916-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-152">System-Flags</span></span>           | <span data-ttu-id="c6916-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-153">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-154">Classes used in</span></span>        | [<span data-ttu-id="c6916-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c6916-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6916-156">Windows Server 2003</span></span>



| <span data-ttu-id="c6916-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-157">Entry</span></span> | <span data-ttu-id="c6916-158">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-161">System-Only</span></span>            | <span data-ttu-id="c6916-162">True</span><span class="sxs-lookup"><span data-stu-id="c6916-162">True</span></span>                            |
| <span data-ttu-id="c6916-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-164">False</span></span>                           |
| <span data-ttu-id="c6916-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-165">Is Indexed</span></span>             | <span data-ttu-id="c6916-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-166">False</span></span>                           |
| <span data-ttu-id="c6916-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-167">In Global Catalog</span></span>      | <span data-ttu-id="c6916-168">True</span><span class="sxs-lookup"><span data-stu-id="c6916-168">True</span></span>                            |
| <span data-ttu-id="c6916-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-173">Search-Flags</span></span>           | <span data-ttu-id="c6916-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c6916-174">0x00000008</span></span>                      |
| <span data-ttu-id="c6916-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-175">System-Flags</span></span>           | <span data-ttu-id="c6916-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-176">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-177">Classes used in</span></span>        | [<span data-ttu-id="c6916-178">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c6916-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="c6916-179">ADAM</span></span>



| <span data-ttu-id="c6916-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-180">Entry</span></span> | <span data-ttu-id="c6916-181">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-184">System-Only</span></span>            | <span data-ttu-id="c6916-185">True</span><span class="sxs-lookup"><span data-stu-id="c6916-185">True</span></span>                            |
| <span data-ttu-id="c6916-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-187">False</span></span>                           |
| <span data-ttu-id="c6916-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-188">Is Indexed</span></span>             | <span data-ttu-id="c6916-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-189">False</span></span>                           |
| <span data-ttu-id="c6916-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-190">In Global Catalog</span></span>      | <span data-ttu-id="c6916-191">True</span><span class="sxs-lookup"><span data-stu-id="c6916-191">True</span></span>                            |
| <span data-ttu-id="c6916-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-196">Search-Flags</span></span>           | <span data-ttu-id="c6916-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c6916-197">0x00000008</span></span>                      |
| <span data-ttu-id="c6916-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-198">System-Flags</span></span>           | <span data-ttu-id="c6916-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-199">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-200">Classes used in</span></span>        | [<span data-ttu-id="c6916-201">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c6916-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c6916-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c6916-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-203">Entry</span></span> | <span data-ttu-id="c6916-204">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-207">System-Only</span></span>            | <span data-ttu-id="c6916-208">True</span><span class="sxs-lookup"><span data-stu-id="c6916-208">True</span></span>                            |
| <span data-ttu-id="c6916-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-210">False</span></span>                           |
| <span data-ttu-id="c6916-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-211">Is Indexed</span></span>             | <span data-ttu-id="c6916-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-212">False</span></span>                           |
| <span data-ttu-id="c6916-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-213">In Global Catalog</span></span>      | <span data-ttu-id="c6916-214">True</span><span class="sxs-lookup"><span data-stu-id="c6916-214">True</span></span>                            |
| <span data-ttu-id="c6916-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-219">Search-Flags</span></span>           | <span data-ttu-id="c6916-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c6916-220">0x00000008</span></span>                      |
| <span data-ttu-id="c6916-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-221">System-Flags</span></span>           | <span data-ttu-id="c6916-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-222">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-223">Classes used in</span></span>        | [<span data-ttu-id="c6916-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c6916-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6916-225">Windows Server 2008</span></span>



| <span data-ttu-id="c6916-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-226">Entry</span></span> | <span data-ttu-id="c6916-227">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-230">System-Only</span></span>            | <span data-ttu-id="c6916-231">True</span><span class="sxs-lookup"><span data-stu-id="c6916-231">True</span></span>                            |
| <span data-ttu-id="c6916-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-232">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-233">False</span></span>                           |
| <span data-ttu-id="c6916-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-234">Is Indexed</span></span>             | <span data-ttu-id="c6916-235">True</span><span class="sxs-lookup"><span data-stu-id="c6916-235">True</span></span>                            |
| <span data-ttu-id="c6916-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-236">In Global Catalog</span></span>      | <span data-ttu-id="c6916-237">True</span><span class="sxs-lookup"><span data-stu-id="c6916-237">True</span></span>                            |
| <span data-ttu-id="c6916-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-242">Search-Flags</span></span>           | <span data-ttu-id="c6916-243">0x00000009</span><span class="sxs-lookup"><span data-stu-id="c6916-243">0x00000009</span></span>                      |
| <span data-ttu-id="c6916-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-244">System-Flags</span></span>           | <span data-ttu-id="c6916-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-245">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-246">Classes used in</span></span>        | [<span data-ttu-id="c6916-247">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c6916-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6916-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c6916-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-249">Entry</span></span> | <span data-ttu-id="c6916-250">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-253">System-Only</span></span>            | <span data-ttu-id="c6916-254">True</span><span class="sxs-lookup"><span data-stu-id="c6916-254">True</span></span>                            |
| <span data-ttu-id="c6916-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-255">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-256">False</span></span>                           |
| <span data-ttu-id="c6916-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-257">Is Indexed</span></span>             | <span data-ttu-id="c6916-258">True</span><span class="sxs-lookup"><span data-stu-id="c6916-258">True</span></span>                            |
| <span data-ttu-id="c6916-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-259">In Global Catalog</span></span>      | <span data-ttu-id="c6916-260">True</span><span class="sxs-lookup"><span data-stu-id="c6916-260">True</span></span>                            |
| <span data-ttu-id="c6916-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-265">Search-Flags</span></span>           | <span data-ttu-id="c6916-266">0x00000009</span><span class="sxs-lookup"><span data-stu-id="c6916-266">0x00000009</span></span>                      |
| <span data-ttu-id="c6916-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-267">System-Flags</span></span>           | <span data-ttu-id="c6916-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-268">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-269">Classes used in</span></span>        | [<span data-ttu-id="c6916-270">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c6916-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6916-271">Windows Server 2012</span></span>



| <span data-ttu-id="c6916-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6916-272">Entry</span></span> | <span data-ttu-id="c6916-273">Значение</span><span class="sxs-lookup"><span data-stu-id="c6916-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c6916-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6916-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6916-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c6916-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6916-276">System-Only</span></span>            | <span data-ttu-id="c6916-277">True</span><span class="sxs-lookup"><span data-stu-id="c6916-277">True</span></span>                            |
| <span data-ttu-id="c6916-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6916-278">Is-Single-Valued</span></span>       | <span data-ttu-id="c6916-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6916-279">False</span></span>                           |
| <span data-ttu-id="c6916-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6916-280">Is Indexed</span></span>             | <span data-ttu-id="c6916-281">True</span><span class="sxs-lookup"><span data-stu-id="c6916-281">True</span></span>                            |
| <span data-ttu-id="c6916-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6916-282">In Global Catalog</span></span>      | <span data-ttu-id="c6916-283">True</span><span class="sxs-lookup"><span data-stu-id="c6916-283">True</span></span>                            |
| <span data-ttu-id="c6916-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6916-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6916-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6916-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c6916-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6916-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c6916-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6916-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c6916-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-288">Search-Flags</span></span>           | <span data-ttu-id="c6916-289">0x00000009</span><span class="sxs-lookup"><span data-stu-id="c6916-289">0x00000009</span></span>                      |
| <span data-ttu-id="c6916-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6916-290">System-Flags</span></span>           | <span data-ttu-id="c6916-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c6916-291">0x00000012</span></span>                      |
| <span data-ttu-id="c6916-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6916-292">Classes used in</span></span>        | [<span data-ttu-id="c6916-293">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c6916-293">**Top**</span></span>](c-top.md)<br/> |



 

 





