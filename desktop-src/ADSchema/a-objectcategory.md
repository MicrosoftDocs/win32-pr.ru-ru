---
title: Атрибут Object-Category
description: Имя класса объекта, используемое для группирования объектов этого или производных классов.
ms.assetid: 06fd0314-08b0-49eb-867c-463f7e0afee4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Category
- Схема AD атрибута objectCategory
topic_type:
- apiref
api_name:
- Object-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b828e4d466b1013ab3854232859a69707553775f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138542"
---
# <a name="object-category-attribute"></a><span data-ttu-id="f3c61-105">Атрибут Object-Category</span><span class="sxs-lookup"><span data-stu-id="f3c61-105">Object-Category attribute</span></span>

<span data-ttu-id="f3c61-106">Имя класса объекта, используемое для группирования объектов этого или производных классов.</span><span class="sxs-lookup"><span data-stu-id="f3c61-106">An object class name used to group objects of this or derived classes.</span></span>



| <span data-ttu-id="f3c61-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-107">Entry</span></span> | <span data-ttu-id="f3c61-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="f3c61-109">CN</span><span class="sxs-lookup"><span data-stu-id="f3c61-109">CN</span></span>                | <span data-ttu-id="f3c61-110">Object-Category</span><span class="sxs-lookup"><span data-stu-id="f3c61-110">Object-Category</span></span>                                  |
| <span data-ttu-id="f3c61-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f3c61-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f3c61-112">objectCategory</span><span class="sxs-lookup"><span data-stu-id="f3c61-112">objectCategory</span></span>                                   |
| <span data-ttu-id="f3c61-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f3c61-113">Size</span></span>              | <span data-ttu-id="f3c61-114">Примерно 20 байт в среднем.</span><span class="sxs-lookup"><span data-stu-id="f3c61-114">About 20 bytes on average.</span></span>                       |
| <span data-ttu-id="f3c61-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f3c61-115">Update Privilege</span></span>  | <span data-ttu-id="f3c61-116">Это значение задается конструктором объекта.</span><span class="sxs-lookup"><span data-stu-id="f3c61-116">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="f3c61-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f3c61-117">Update Frequency</span></span>  | <span data-ttu-id="f3c61-118">Это значение никогда не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="f3c61-118">This value should never change.</span></span>                  |
| <span data-ttu-id="f3c61-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-119">Attribute-Id</span></span>      | <span data-ttu-id="f3c61-120">1.2.840.113556.1.4.782</span><span class="sxs-lookup"><span data-stu-id="f3c61-120">1.2.840.113556.1.4.782</span></span>                           |
| <span data-ttu-id="f3c61-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f3c61-121">System-Id-Guid</span></span>    | <span data-ttu-id="f3c61-122">26d97369-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f3c61-122">26d97369-6070-11d1-a9c6-0000f80367c1</span></span>             |
| <span data-ttu-id="f3c61-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3c61-123">Syntax</span></span>            | [<span data-ttu-id="f3c61-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f3c61-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="f3c61-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f3c61-125">Implementations</span></span>

-   [<span data-ttu-id="f3c61-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3c61-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3c61-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3c61-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3c61-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f3c61-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f3c61-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3c61-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3c61-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3c61-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3c61-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3c61-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3c61-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3c61-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3c61-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3c61-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f3c61-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-134">Entry</span></span> | <span data-ttu-id="f3c61-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-138">System-Only</span></span>            | <span data-ttu-id="f3c61-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-139">False</span></span>                           |
| <span data-ttu-id="f3c61-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-141">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-141">True</span></span>                            |
| <span data-ttu-id="f3c61-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-142">Is Indexed</span></span>             | <span data-ttu-id="f3c61-143">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-143">True</span></span>                            |
| <span data-ttu-id="f3c61-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-144">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-145">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-145">True</span></span>                            |
| <span data-ttu-id="f3c61-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-150">Search-Flags</span></span>           | <span data-ttu-id="f3c61-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-151">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-152">System-Flags</span></span>           | <span data-ttu-id="f3c61-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-153">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-154">Classes used in</span></span>        | [<span data-ttu-id="f3c61-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3c61-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3c61-156">Windows Server 2003</span></span>



| <span data-ttu-id="f3c61-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-157">Entry</span></span> | <span data-ttu-id="f3c61-158">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-161">System-Only</span></span>            | <span data-ttu-id="f3c61-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-162">False</span></span>                           |
| <span data-ttu-id="f3c61-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-164">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-164">True</span></span>                            |
| <span data-ttu-id="f3c61-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-165">Is Indexed</span></span>             | <span data-ttu-id="f3c61-166">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-166">True</span></span>                            |
| <span data-ttu-id="f3c61-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-167">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-168">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-168">True</span></span>                            |
| <span data-ttu-id="f3c61-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-173">Search-Flags</span></span>           | <span data-ttu-id="f3c61-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-174">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-175">System-Flags</span></span>           | <span data-ttu-id="f3c61-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-176">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-177">Classes used in</span></span>        | [<span data-ttu-id="f3c61-178">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f3c61-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="f3c61-179">ADAM</span></span>



| <span data-ttu-id="f3c61-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-180">Entry</span></span> | <span data-ttu-id="f3c61-181">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-184">System-Only</span></span>            | <span data-ttu-id="f3c61-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-185">False</span></span>                           |
| <span data-ttu-id="f3c61-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-187">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-187">True</span></span>                            |
| <span data-ttu-id="f3c61-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-188">Is Indexed</span></span>             | <span data-ttu-id="f3c61-189">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-189">True</span></span>                            |
| <span data-ttu-id="f3c61-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-190">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-191">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-191">True</span></span>                            |
| <span data-ttu-id="f3c61-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-196">Search-Flags</span></span>           | <span data-ttu-id="f3c61-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-197">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-198">System-Flags</span></span>           | <span data-ttu-id="f3c61-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-199">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-200">Classes used in</span></span>        | [<span data-ttu-id="f3c61-201">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3c61-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3c61-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3c61-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-203">Entry</span></span> | <span data-ttu-id="f3c61-204">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-207">System-Only</span></span>            | <span data-ttu-id="f3c61-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-208">False</span></span>                           |
| <span data-ttu-id="f3c61-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-210">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-210">True</span></span>                            |
| <span data-ttu-id="f3c61-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-211">Is Indexed</span></span>             | <span data-ttu-id="f3c61-212">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-212">True</span></span>                            |
| <span data-ttu-id="f3c61-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-213">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-214">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-214">True</span></span>                            |
| <span data-ttu-id="f3c61-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-219">Search-Flags</span></span>           | <span data-ttu-id="f3c61-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-220">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-221">System-Flags</span></span>           | <span data-ttu-id="f3c61-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-222">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-223">Classes used in</span></span>        | [<span data-ttu-id="f3c61-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3c61-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3c61-225">Windows Server 2008</span></span>



| <span data-ttu-id="f3c61-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-226">Entry</span></span> | <span data-ttu-id="f3c61-227">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-230">System-Only</span></span>            | <span data-ttu-id="f3c61-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-231">False</span></span>                           |
| <span data-ttu-id="f3c61-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-233">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-233">True</span></span>                            |
| <span data-ttu-id="f3c61-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-234">Is Indexed</span></span>             | <span data-ttu-id="f3c61-235">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-235">True</span></span>                            |
| <span data-ttu-id="f3c61-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-236">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-237">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-237">True</span></span>                            |
| <span data-ttu-id="f3c61-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-242">Search-Flags</span></span>           | <span data-ttu-id="f3c61-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-243">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-244">System-Flags</span></span>           | <span data-ttu-id="f3c61-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-245">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-246">Classes used in</span></span>        | [<span data-ttu-id="f3c61-247">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3c61-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3c61-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3c61-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-249">Entry</span></span> | <span data-ttu-id="f3c61-250">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-253">System-Only</span></span>            | <span data-ttu-id="f3c61-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-254">False</span></span>                           |
| <span data-ttu-id="f3c61-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-255">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-256">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-256">True</span></span>                            |
| <span data-ttu-id="f3c61-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-257">Is Indexed</span></span>             | <span data-ttu-id="f3c61-258">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-258">True</span></span>                            |
| <span data-ttu-id="f3c61-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-259">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-260">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-260">True</span></span>                            |
| <span data-ttu-id="f3c61-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-265">Search-Flags</span></span>           | <span data-ttu-id="f3c61-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-266">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-267">System-Flags</span></span>           | <span data-ttu-id="f3c61-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-268">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-269">Classes used in</span></span>        | [<span data-ttu-id="f3c61-270">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3c61-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3c61-271">Windows Server 2012</span></span>



| <span data-ttu-id="f3c61-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="f3c61-272">Entry</span></span> | <span data-ttu-id="f3c61-273">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c61-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3c61-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f3c61-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3c61-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3c61-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3c61-276">System-Only</span></span>            | <span data-ttu-id="f3c61-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="f3c61-277">False</span></span>                           |
| <span data-ttu-id="f3c61-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f3c61-278">Is-Single-Valued</span></span>       | <span data-ttu-id="f3c61-279">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-279">True</span></span>                            |
| <span data-ttu-id="f3c61-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f3c61-280">Is Indexed</span></span>             | <span data-ttu-id="f3c61-281">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-281">True</span></span>                            |
| <span data-ttu-id="f3c61-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f3c61-282">In Global Catalog</span></span>      | <span data-ttu-id="f3c61-283">True</span><span class="sxs-lookup"><span data-stu-id="f3c61-283">True</span></span>                            |
| <span data-ttu-id="f3c61-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f3c61-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3c61-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3c61-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3c61-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3c61-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3c61-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3c61-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3c61-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-288">Search-Flags</span></span>           | <span data-ttu-id="f3c61-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3c61-289">0x00000001</span></span>                      |
| <span data-ttu-id="f3c61-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3c61-290">System-Flags</span></span>           | <span data-ttu-id="f3c61-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3c61-291">0x00000012</span></span>                      |
| <span data-ttu-id="f3c61-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f3c61-292">Classes used in</span></span>        | [<span data-ttu-id="f3c61-293">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f3c61-293">**Top**</span></span>](c-top.md)<br/> |



 

 





