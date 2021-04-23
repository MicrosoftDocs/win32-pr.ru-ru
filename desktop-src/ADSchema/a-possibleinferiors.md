---
title: Атрибут Possible-Inferiors
description: Список объектов, которые может содержать этот объект.
ms.assetid: f5588b24-7e50-4a65-bc70-a6b649b84fcb
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Possible-Inferiors
- Схема AD атрибута Поссиблеинфериорс
topic_type:
- apiref
api_name:
- Possible-Inferiors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b42808fc3e47eaef66a58b62f2ca2527374a95
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989513"
---
# <a name="possible-inferiors-attribute"></a><span data-ttu-id="3f68c-105">Атрибут Possible-Inferiors</span><span class="sxs-lookup"><span data-stu-id="3f68c-105">Possible-Inferiors attribute</span></span>

<span data-ttu-id="3f68c-106">Список объектов, которые может содержать этот объект.</span><span class="sxs-lookup"><span data-stu-id="3f68c-106">The list of objects that this object can contain.</span></span>



| <span data-ttu-id="3f68c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-107">Entry</span></span> | <span data-ttu-id="3f68c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="3f68c-109">CN</span><span class="sxs-lookup"><span data-stu-id="3f68c-109">CN</span></span>                | <span data-ttu-id="3f68c-110">Possible-Inferiors</span><span class="sxs-lookup"><span data-stu-id="3f68c-110">Possible-Inferiors</span></span>                                              |
| <span data-ttu-id="3f68c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3f68c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3f68c-112">поссиблеинфериорс</span><span class="sxs-lookup"><span data-stu-id="3f68c-112">possibleInferiors</span></span>                                               |
| <span data-ttu-id="3f68c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3f68c-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="3f68c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3f68c-114">Update Privilege</span></span>  | <span data-ttu-id="3f68c-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="3f68c-115">Domain administrator</span></span>                                            |
| <span data-ttu-id="3f68c-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3f68c-116">Update Frequency</span></span>  | <span data-ttu-id="3f68c-117">При определении класса.</span><span class="sxs-lookup"><span data-stu-id="3f68c-117">When the class is defined.</span></span>                                      |
| <span data-ttu-id="3f68c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-118">Attribute-Id</span></span>      | <span data-ttu-id="3f68c-119">1.2.840.113556.1.4.915</span><span class="sxs-lookup"><span data-stu-id="3f68c-119">1.2.840.113556.1.4.915</span></span>                                          |
| <span data-ttu-id="3f68c-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3f68c-120">System-Id-Guid</span></span>    | <span data-ttu-id="3f68c-121">9a7ad94c-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="3f68c-121">9a7ad94c-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="3f68c-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f68c-122">Syntax</span></span>            | [<span data-ttu-id="3f68c-123">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="3f68c-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="3f68c-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3f68c-124">Implementations</span></span>

-   [<span data-ttu-id="3f68c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3f68c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3f68c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3f68c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3f68c-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3f68c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3f68c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3f68c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3f68c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f68c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f68c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f68c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f68c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f68c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3f68c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f68c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="3f68c-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-133">Entry</span></span> | <span data-ttu-id="3f68c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-137">System-Only</span></span>            | <span data-ttu-id="3f68c-138">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-138">True</span></span>                            |
| <span data-ttu-id="3f68c-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-140">False</span></span>                           |
| <span data-ttu-id="3f68c-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-141">Is Indexed</span></span>             | <span data-ttu-id="3f68c-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-142">False</span></span>                           |
| <span data-ttu-id="3f68c-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-143">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-144">False</span></span>                           |
| <span data-ttu-id="3f68c-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-149">Search-Flags</span></span>           | <span data-ttu-id="3f68c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-150">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-151">System-Flags</span></span>           | <span data-ttu-id="3f68c-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-152">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-153">Classes used in</span></span>        | [<span data-ttu-id="3f68c-154">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3f68c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f68c-155">Windows Server 2003</span></span>



| <span data-ttu-id="3f68c-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-156">Entry</span></span> | <span data-ttu-id="3f68c-157">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-160">System-Only</span></span>            | <span data-ttu-id="3f68c-161">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-161">True</span></span>                            |
| <span data-ttu-id="3f68c-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-163">False</span></span>                           |
| <span data-ttu-id="3f68c-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-164">Is Indexed</span></span>             | <span data-ttu-id="3f68c-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-165">False</span></span>                           |
| <span data-ttu-id="3f68c-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-166">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-167">False</span></span>                           |
| <span data-ttu-id="3f68c-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-172">Search-Flags</span></span>           | <span data-ttu-id="3f68c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-173">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-174">System-Flags</span></span>           | <span data-ttu-id="3f68c-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-175">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-176">Classes used in</span></span>        | [<span data-ttu-id="3f68c-177">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3f68c-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="3f68c-178">ADAM</span></span>



| <span data-ttu-id="3f68c-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-179">Entry</span></span> | <span data-ttu-id="3f68c-180">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-183">System-Only</span></span>            | <span data-ttu-id="3f68c-184">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-184">True</span></span>                            |
| <span data-ttu-id="3f68c-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-186">False</span></span>                           |
| <span data-ttu-id="3f68c-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-187">Is Indexed</span></span>             | <span data-ttu-id="3f68c-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-188">False</span></span>                           |
| <span data-ttu-id="3f68c-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-189">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-190">False</span></span>                           |
| <span data-ttu-id="3f68c-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-195">Search-Flags</span></span>           | <span data-ttu-id="3f68c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-196">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-197">System-Flags</span></span>           | <span data-ttu-id="3f68c-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-198">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-199">Classes used in</span></span>        | [<span data-ttu-id="3f68c-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3f68c-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3f68c-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3f68c-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-202">Entry</span></span> | <span data-ttu-id="3f68c-203">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-206">System-Only</span></span>            | <span data-ttu-id="3f68c-207">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-207">True</span></span>                            |
| <span data-ttu-id="3f68c-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-209">False</span></span>                           |
| <span data-ttu-id="3f68c-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-210">Is Indexed</span></span>             | <span data-ttu-id="3f68c-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-211">False</span></span>                           |
| <span data-ttu-id="3f68c-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-212">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-213">False</span></span>                           |
| <span data-ttu-id="3f68c-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-218">Search-Flags</span></span>           | <span data-ttu-id="3f68c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-219">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-220">System-Flags</span></span>           | <span data-ttu-id="3f68c-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-221">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-222">Classes used in</span></span>        | [<span data-ttu-id="3f68c-223">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3f68c-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f68c-224">Windows Server 2008</span></span>



| <span data-ttu-id="3f68c-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-225">Entry</span></span> | <span data-ttu-id="3f68c-226">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-229">System-Only</span></span>            | <span data-ttu-id="3f68c-230">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-230">True</span></span>                            |
| <span data-ttu-id="3f68c-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-232">False</span></span>                           |
| <span data-ttu-id="3f68c-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-233">Is Indexed</span></span>             | <span data-ttu-id="3f68c-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-234">False</span></span>                           |
| <span data-ttu-id="3f68c-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-235">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-236">False</span></span>                           |
| <span data-ttu-id="3f68c-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-241">Search-Flags</span></span>           | <span data-ttu-id="3f68c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-242">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-243">System-Flags</span></span>           | <span data-ttu-id="3f68c-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-244">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-245">Classes used in</span></span>        | [<span data-ttu-id="3f68c-246">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f68c-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f68c-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f68c-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-248">Entry</span></span> | <span data-ttu-id="3f68c-249">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-252">System-Only</span></span>            | <span data-ttu-id="3f68c-253">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-253">True</span></span>                            |
| <span data-ttu-id="3f68c-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-255">False</span></span>                           |
| <span data-ttu-id="3f68c-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-256">Is Indexed</span></span>             | <span data-ttu-id="3f68c-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-257">False</span></span>                           |
| <span data-ttu-id="3f68c-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-258">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-259">False</span></span>                           |
| <span data-ttu-id="3f68c-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-264">Search-Flags</span></span>           | <span data-ttu-id="3f68c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-265">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-266">System-Flags</span></span>           | <span data-ttu-id="3f68c-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-267">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-268">Classes used in</span></span>        | [<span data-ttu-id="3f68c-269">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3f68c-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f68c-270">Windows Server 2012</span></span>



| <span data-ttu-id="3f68c-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="3f68c-271">Entry</span></span> | <span data-ttu-id="3f68c-272">Значение</span><span class="sxs-lookup"><span data-stu-id="3f68c-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3f68c-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3f68c-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f68c-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3f68c-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f68c-275">System-Only</span></span>            | <span data-ttu-id="3f68c-276">True</span><span class="sxs-lookup"><span data-stu-id="3f68c-276">True</span></span>                            |
| <span data-ttu-id="3f68c-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3f68c-277">Is-Single-Valued</span></span>       | <span data-ttu-id="3f68c-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-278">False</span></span>                           |
| <span data-ttu-id="3f68c-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3f68c-279">Is Indexed</span></span>             | <span data-ttu-id="3f68c-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-280">False</span></span>                           |
| <span data-ttu-id="3f68c-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3f68c-281">In Global Catalog</span></span>      | <span data-ttu-id="3f68c-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f68c-282">False</span></span>                           |
| <span data-ttu-id="3f68c-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3f68c-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f68c-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3f68c-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3f68c-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f68c-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3f68c-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f68c-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3f68c-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-287">Search-Flags</span></span>           | <span data-ttu-id="3f68c-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f68c-288">0x00000000</span></span>                      |
| <span data-ttu-id="3f68c-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f68c-289">System-Flags</span></span>           | <span data-ttu-id="3f68c-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3f68c-290">0x08000014</span></span>                      |
| <span data-ttu-id="3f68c-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3f68c-291">Classes used in</span></span>        | [<span data-ttu-id="3f68c-292">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="3f68c-292">**Top**</span></span>](c-top.md)<br/> |



 

 





