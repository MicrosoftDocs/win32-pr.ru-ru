---
title: Атрибут Applies-To
description: Содержит список классов объектов, к которым применяется расширенное право. В списке класс объекта представлен свойством schemaIDGUID для своего объекта Счемакласс.
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Applies-To
- Схема AD атрибута appliesTo
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139118"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="905a4-106">Атрибут Applies-To</span><span class="sxs-lookup"><span data-stu-id="905a4-106">Applies-To attribute</span></span>

<span data-ttu-id="905a4-107">Содержит список классов объектов, к которым применяется расширенное право.</span><span class="sxs-lookup"><span data-stu-id="905a4-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="905a4-108">В списке класс объекта представлен свойством schemaIDGUID для своего объекта Счемакласс.</span><span class="sxs-lookup"><span data-stu-id="905a4-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="905a4-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-109">Entry</span></span> | <span data-ttu-id="905a4-110">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="905a4-111">CN</span><span class="sxs-lookup"><span data-stu-id="905a4-111">CN</span></span>                | <span data-ttu-id="905a4-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="905a4-112">Applies-To</span></span>                                  |
| <span data-ttu-id="905a4-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="905a4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="905a4-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="905a4-114">appliesTo</span></span>                                   |
| <span data-ttu-id="905a4-115">Размер</span><span class="sxs-lookup"><span data-stu-id="905a4-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="905a4-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="905a4-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="905a4-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="905a4-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="905a4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-118">Attribute-Id</span></span>      | <span data-ttu-id="905a4-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="905a4-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="905a4-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="905a4-120">System-Id-Guid</span></span>    | <span data-ttu-id="905a4-121">8297931d-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="905a4-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="905a4-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="905a4-122">Syntax</span></span>            | [<span data-ttu-id="905a4-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="905a4-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="905a4-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="905a4-124">Implementations</span></span>

-   [<span data-ttu-id="905a4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="905a4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="905a4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="905a4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="905a4-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="905a4-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="905a4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="905a4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="905a4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="905a4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="905a4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="905a4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="905a4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="905a4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="905a4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="905a4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="905a4-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-133">Entry</span></span> | <span data-ttu-id="905a4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-137">System-Only</span></span>            | <span data-ttu-id="905a4-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-138">False</span></span>                                                           |
| <span data-ttu-id="905a4-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-140">False</span></span>                                                           |
| <span data-ttu-id="905a4-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-141">Is Indexed</span></span>             | <span data-ttu-id="905a4-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-142">False</span></span>                                                           |
| <span data-ttu-id="905a4-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-143">In Global Catalog</span></span>      | <span data-ttu-id="905a4-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-144">False</span></span>                                                           |
| <span data-ttu-id="905a4-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-147">Range-Lower</span></span>            | <span data-ttu-id="905a4-148">36</span><span class="sxs-lookup"><span data-stu-id="905a4-148">36</span></span>                                                              |
| <span data-ttu-id="905a4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-149">Range-Upper</span></span>            | <span data-ttu-id="905a4-150">36</span><span class="sxs-lookup"><span data-stu-id="905a4-150">36</span></span>                                                              |
| <span data-ttu-id="905a4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-151">Search-Flags</span></span>           | <span data-ttu-id="905a4-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-153">System-Flags</span></span>           | <span data-ttu-id="905a4-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-155">Classes used in</span></span>        | [<span data-ttu-id="905a4-156">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="905a4-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="905a4-157">Windows Server 2003</span></span>



| <span data-ttu-id="905a4-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-158">Entry</span></span> | <span data-ttu-id="905a4-159">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-162">System-Only</span></span>            | <span data-ttu-id="905a4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-163">False</span></span>                                                           |
| <span data-ttu-id="905a4-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-164">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-165">False</span></span>                                                           |
| <span data-ttu-id="905a4-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-166">Is Indexed</span></span>             | <span data-ttu-id="905a4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-167">False</span></span>                                                           |
| <span data-ttu-id="905a4-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-168">In Global Catalog</span></span>      | <span data-ttu-id="905a4-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-169">False</span></span>                                                           |
| <span data-ttu-id="905a4-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-172">Range-Lower</span></span>            | <span data-ttu-id="905a4-173">36</span><span class="sxs-lookup"><span data-stu-id="905a4-173">36</span></span>                                                              |
| <span data-ttu-id="905a4-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-174">Range-Upper</span></span>            | <span data-ttu-id="905a4-175">36</span><span class="sxs-lookup"><span data-stu-id="905a4-175">36</span></span>                                                              |
| <span data-ttu-id="905a4-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-176">Search-Flags</span></span>           | <span data-ttu-id="905a4-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-178">System-Flags</span></span>           | <span data-ttu-id="905a4-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-180">Classes used in</span></span>        | [<span data-ttu-id="905a4-181">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="905a4-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="905a4-182">ADAM</span></span>



| <span data-ttu-id="905a4-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-183">Entry</span></span> | <span data-ttu-id="905a4-184">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-187">System-Only</span></span>            | <span data-ttu-id="905a4-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-188">False</span></span>                                                           |
| <span data-ttu-id="905a4-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-189">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-190">False</span></span>                                                           |
| <span data-ttu-id="905a4-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-191">Is Indexed</span></span>             | <span data-ttu-id="905a4-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-192">False</span></span>                                                           |
| <span data-ttu-id="905a4-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-193">In Global Catalog</span></span>      | <span data-ttu-id="905a4-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-194">False</span></span>                                                           |
| <span data-ttu-id="905a4-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-197">Range-Lower</span></span>            | <span data-ttu-id="905a4-198">36</span><span class="sxs-lookup"><span data-stu-id="905a4-198">36</span></span>                                                              |
| <span data-ttu-id="905a4-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-199">Range-Upper</span></span>            | <span data-ttu-id="905a4-200">36</span><span class="sxs-lookup"><span data-stu-id="905a4-200">36</span></span>                                                              |
| <span data-ttu-id="905a4-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-201">Search-Flags</span></span>           | <span data-ttu-id="905a4-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-203">System-Flags</span></span>           | <span data-ttu-id="905a4-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-205">Classes used in</span></span>        | [<span data-ttu-id="905a4-206">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="905a4-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="905a4-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="905a4-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-208">Entry</span></span> | <span data-ttu-id="905a4-209">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-212">System-Only</span></span>            | <span data-ttu-id="905a4-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-213">False</span></span>                                                           |
| <span data-ttu-id="905a4-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-214">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-215">False</span></span>                                                           |
| <span data-ttu-id="905a4-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-216">Is Indexed</span></span>             | <span data-ttu-id="905a4-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-217">False</span></span>                                                           |
| <span data-ttu-id="905a4-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-218">In Global Catalog</span></span>      | <span data-ttu-id="905a4-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-219">False</span></span>                                                           |
| <span data-ttu-id="905a4-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-222">Range-Lower</span></span>            | <span data-ttu-id="905a4-223">36</span><span class="sxs-lookup"><span data-stu-id="905a4-223">36</span></span>                                                              |
| <span data-ttu-id="905a4-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-224">Range-Upper</span></span>            | <span data-ttu-id="905a4-225">36</span><span class="sxs-lookup"><span data-stu-id="905a4-225">36</span></span>                                                              |
| <span data-ttu-id="905a4-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-226">Search-Flags</span></span>           | <span data-ttu-id="905a4-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-228">System-Flags</span></span>           | <span data-ttu-id="905a4-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-230">Classes used in</span></span>        | [<span data-ttu-id="905a4-231">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="905a4-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="905a4-232">Windows Server 2008</span></span>



| <span data-ttu-id="905a4-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-233">Entry</span></span> | <span data-ttu-id="905a4-234">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-237">System-Only</span></span>            | <span data-ttu-id="905a4-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-238">False</span></span>                                                           |
| <span data-ttu-id="905a4-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-239">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-240">False</span></span>                                                           |
| <span data-ttu-id="905a4-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-241">Is Indexed</span></span>             | <span data-ttu-id="905a4-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-242">False</span></span>                                                           |
| <span data-ttu-id="905a4-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-243">In Global Catalog</span></span>      | <span data-ttu-id="905a4-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-244">False</span></span>                                                           |
| <span data-ttu-id="905a4-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-247">Range-Lower</span></span>            | <span data-ttu-id="905a4-248">36</span><span class="sxs-lookup"><span data-stu-id="905a4-248">36</span></span>                                                              |
| <span data-ttu-id="905a4-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-249">Range-Upper</span></span>            | <span data-ttu-id="905a4-250">36</span><span class="sxs-lookup"><span data-stu-id="905a4-250">36</span></span>                                                              |
| <span data-ttu-id="905a4-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-251">Search-Flags</span></span>           | <span data-ttu-id="905a4-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-253">System-Flags</span></span>           | <span data-ttu-id="905a4-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-255">Classes used in</span></span>        | [<span data-ttu-id="905a4-256">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="905a4-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="905a4-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="905a4-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-258">Entry</span></span> | <span data-ttu-id="905a4-259">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-262">System-Only</span></span>            | <span data-ttu-id="905a4-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-263">False</span></span>                                                           |
| <span data-ttu-id="905a4-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-264">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-265">False</span></span>                                                           |
| <span data-ttu-id="905a4-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-266">Is Indexed</span></span>             | <span data-ttu-id="905a4-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-267">False</span></span>                                                           |
| <span data-ttu-id="905a4-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-268">In Global Catalog</span></span>      | <span data-ttu-id="905a4-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-269">False</span></span>                                                           |
| <span data-ttu-id="905a4-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-272">Range-Lower</span></span>            | <span data-ttu-id="905a4-273">36</span><span class="sxs-lookup"><span data-stu-id="905a4-273">36</span></span>                                                              |
| <span data-ttu-id="905a4-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-274">Range-Upper</span></span>            | <span data-ttu-id="905a4-275">36</span><span class="sxs-lookup"><span data-stu-id="905a4-275">36</span></span>                                                              |
| <span data-ttu-id="905a4-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-276">Search-Flags</span></span>           | <span data-ttu-id="905a4-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-278">System-Flags</span></span>           | <span data-ttu-id="905a4-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-280">Classes used in</span></span>        | [<span data-ttu-id="905a4-281">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="905a4-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="905a4-282">Windows Server 2012</span></span>



| <span data-ttu-id="905a4-283">Ввод</span><span class="sxs-lookup"><span data-stu-id="905a4-283">Entry</span></span> | <span data-ttu-id="905a4-284">Значение</span><span class="sxs-lookup"><span data-stu-id="905a4-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="905a4-285">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="905a4-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905a4-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="905a4-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="905a4-287">System-Only</span></span>            | <span data-ttu-id="905a4-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-288">False</span></span>                                                           |
| <span data-ttu-id="905a4-289">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="905a4-289">Is-Single-Valued</span></span>       | <span data-ttu-id="905a4-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-290">False</span></span>                                                           |
| <span data-ttu-id="905a4-291">Индексируется</span><span class="sxs-lookup"><span data-stu-id="905a4-291">Is Indexed</span></span>             | <span data-ttu-id="905a4-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-292">False</span></span>                                                           |
| <span data-ttu-id="905a4-293">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="905a4-293">In Global Catalog</span></span>      | <span data-ttu-id="905a4-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="905a4-294">False</span></span>                                                           |
| <span data-ttu-id="905a4-295">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="905a4-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="905a4-296">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="905a4-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="905a4-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905a4-297">Range-Lower</span></span>            | <span data-ttu-id="905a4-298">36</span><span class="sxs-lookup"><span data-stu-id="905a4-298">36</span></span>                                                              |
| <span data-ttu-id="905a4-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905a4-299">Range-Upper</span></span>            | <span data-ttu-id="905a4-300">36</span><span class="sxs-lookup"><span data-stu-id="905a4-300">36</span></span>                                                              |
| <span data-ttu-id="905a4-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-301">Search-Flags</span></span>           | <span data-ttu-id="905a4-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="905a4-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="905a4-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905a4-303">System-Flags</span></span>           | <span data-ttu-id="905a4-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905a4-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="905a4-305">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="905a4-305">Classes used in</span></span>        | [<span data-ttu-id="905a4-306">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="905a4-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





