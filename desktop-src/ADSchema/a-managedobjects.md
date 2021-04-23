---
title: Атрибут Managed-Objects
description: Содержит список объектов, управляемых пользователем. В списке перечислены объекты, для которых свойство managedBy свойства имеет значение этого пользователя. Каждый элемент в списке является связанной ссылкой на управляемый объект.
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Managed-Objects
- Схема AD атрибута managedObjects
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654931"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="15097-107">Атрибут Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="15097-107">Managed-Objects attribute</span></span>

<span data-ttu-id="15097-108">Содержит список объектов, управляемых пользователем.</span><span class="sxs-lookup"><span data-stu-id="15097-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="15097-109">В списке перечислены объекты, для которых свойство managedBy свойства имеет значение этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="15097-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="15097-110">Каждый элемент в списке является связанной ссылкой на управляемый объект.</span><span class="sxs-lookup"><span data-stu-id="15097-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="15097-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-111">Entry</span></span> | <span data-ttu-id="15097-112">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15097-113">CN</span><span class="sxs-lookup"><span data-stu-id="15097-113">CN</span></span>                | <span data-ttu-id="15097-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="15097-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="15097-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="15097-115">Ldap-Display-Name</span></span> | <span data-ttu-id="15097-116">managedObjects</span><span class="sxs-lookup"><span data-stu-id="15097-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="15097-117">Размер</span><span class="sxs-lookup"><span data-stu-id="15097-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="15097-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="15097-118">Update Privilege</span></span>  | <span data-ttu-id="15097-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="15097-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="15097-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="15097-120">Update Frequency</span></span>  | <span data-ttu-id="15097-121">При создании записи пользователя и при необходимости изменения управляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="15097-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="15097-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="15097-122">Attribute-Id</span></span>      | <span data-ttu-id="15097-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="15097-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="15097-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="15097-124">System-Id-Guid</span></span>    | <span data-ttu-id="15097-125">0296c124-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="15097-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="15097-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15097-126">Syntax</span></span>            | [<span data-ttu-id="15097-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="15097-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="15097-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="15097-128">Implementations</span></span>

-   [<span data-ttu-id="15097-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="15097-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="15097-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="15097-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="15097-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="15097-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="15097-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="15097-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="15097-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="15097-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="15097-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="15097-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="15097-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="15097-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="15097-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="15097-136">Windows 2000 Server</span></span>



| <span data-ttu-id="15097-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-137">Entry</span></span> | <span data-ttu-id="15097-138">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-139">Link-Id</span></span>                | <span data-ttu-id="15097-140">73</span><span class="sxs-lookup"><span data-stu-id="15097-140">73</span></span>                              |
| <span data-ttu-id="15097-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-141">MAPI-Id</span></span>                | <span data-ttu-id="15097-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-142">0x8024</span></span>                          |
| <span data-ttu-id="15097-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-143">System-Only</span></span>            | <span data-ttu-id="15097-144">True</span><span class="sxs-lookup"><span data-stu-id="15097-144">True</span></span>                            |
| <span data-ttu-id="15097-145">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-145">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-146">False</span></span>                           |
| <span data-ttu-id="15097-147">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-147">Is Indexed</span></span>             | <span data-ttu-id="15097-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-148">False</span></span>                           |
| <span data-ttu-id="15097-149">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-149">In Global Catalog</span></span>      | <span data-ttu-id="15097-150">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-150">False</span></span>                           |
| <span data-ttu-id="15097-151">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-152">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-155">Search-Flags</span></span>           | <span data-ttu-id="15097-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-156">0x00000000</span></span>                      |
| <span data-ttu-id="15097-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-157">System-Flags</span></span>           | <span data-ttu-id="15097-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-158">0x00000010</span></span>                      |
| <span data-ttu-id="15097-159">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-159">Classes used in</span></span>        | [<span data-ttu-id="15097-160">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="15097-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15097-161">Windows Server 2003</span></span>



| <span data-ttu-id="15097-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-162">Entry</span></span> | <span data-ttu-id="15097-163">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-164">Link-Id</span></span>                | <span data-ttu-id="15097-165">73</span><span class="sxs-lookup"><span data-stu-id="15097-165">73</span></span>                              |
| <span data-ttu-id="15097-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-166">MAPI-Id</span></span>                | <span data-ttu-id="15097-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-167">0x8024</span></span>                          |
| <span data-ttu-id="15097-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-168">System-Only</span></span>            | <span data-ttu-id="15097-169">True</span><span class="sxs-lookup"><span data-stu-id="15097-169">True</span></span>                            |
| <span data-ttu-id="15097-170">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-170">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-171">False</span></span>                           |
| <span data-ttu-id="15097-172">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-172">Is Indexed</span></span>             | <span data-ttu-id="15097-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-173">False</span></span>                           |
| <span data-ttu-id="15097-174">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-174">In Global Catalog</span></span>      | <span data-ttu-id="15097-175">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-175">False</span></span>                           |
| <span data-ttu-id="15097-176">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-177">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-180">Search-Flags</span></span>           | <span data-ttu-id="15097-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-181">0x00000000</span></span>                      |
| <span data-ttu-id="15097-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-182">System-Flags</span></span>           | <span data-ttu-id="15097-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-183">0x00000010</span></span>                      |
| <span data-ttu-id="15097-184">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-184">Classes used in</span></span>        | [<span data-ttu-id="15097-185">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="15097-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="15097-186">ADAM</span></span>



| <span data-ttu-id="15097-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-187">Entry</span></span> | <span data-ttu-id="15097-188">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-189">Link-Id</span></span>                | <span data-ttu-id="15097-190">73</span><span class="sxs-lookup"><span data-stu-id="15097-190">73</span></span>                              |
| <span data-ttu-id="15097-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-191">MAPI-Id</span></span>                | <span data-ttu-id="15097-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-192">0x8024</span></span>                          |
| <span data-ttu-id="15097-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-193">System-Only</span></span>            | <span data-ttu-id="15097-194">True</span><span class="sxs-lookup"><span data-stu-id="15097-194">True</span></span>                            |
| <span data-ttu-id="15097-195">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-195">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-196">False</span></span>                           |
| <span data-ttu-id="15097-197">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-197">Is Indexed</span></span>             | <span data-ttu-id="15097-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-198">False</span></span>                           |
| <span data-ttu-id="15097-199">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-199">In Global Catalog</span></span>      | <span data-ttu-id="15097-200">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-200">False</span></span>                           |
| <span data-ttu-id="15097-201">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-202">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-205">Search-Flags</span></span>           | <span data-ttu-id="15097-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-206">0x00000000</span></span>                      |
| <span data-ttu-id="15097-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-207">System-Flags</span></span>           | <span data-ttu-id="15097-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-208">0x00000010</span></span>                      |
| <span data-ttu-id="15097-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-209">Classes used in</span></span>        | [<span data-ttu-id="15097-210">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="15097-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15097-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="15097-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-212">Entry</span></span> | <span data-ttu-id="15097-213">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-214">Link-Id</span></span>                | <span data-ttu-id="15097-215">73</span><span class="sxs-lookup"><span data-stu-id="15097-215">73</span></span>                              |
| <span data-ttu-id="15097-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-216">MAPI-Id</span></span>                | <span data-ttu-id="15097-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-217">0x8024</span></span>                          |
| <span data-ttu-id="15097-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-218">System-Only</span></span>            | <span data-ttu-id="15097-219">True</span><span class="sxs-lookup"><span data-stu-id="15097-219">True</span></span>                            |
| <span data-ttu-id="15097-220">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-220">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-221">False</span></span>                           |
| <span data-ttu-id="15097-222">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-222">Is Indexed</span></span>             | <span data-ttu-id="15097-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-223">False</span></span>                           |
| <span data-ttu-id="15097-224">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-224">In Global Catalog</span></span>      | <span data-ttu-id="15097-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-225">False</span></span>                           |
| <span data-ttu-id="15097-226">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-227">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-230">Search-Flags</span></span>           | <span data-ttu-id="15097-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-231">0x00000000</span></span>                      |
| <span data-ttu-id="15097-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-232">System-Flags</span></span>           | <span data-ttu-id="15097-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-233">0x00000010</span></span>                      |
| <span data-ttu-id="15097-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-234">Classes used in</span></span>        | [<span data-ttu-id="15097-235">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="15097-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15097-236">Windows Server 2008</span></span>



| <span data-ttu-id="15097-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-237">Entry</span></span> | <span data-ttu-id="15097-238">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-239">Link-Id</span></span>                | <span data-ttu-id="15097-240">73</span><span class="sxs-lookup"><span data-stu-id="15097-240">73</span></span>                              |
| <span data-ttu-id="15097-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-241">MAPI-Id</span></span>                | <span data-ttu-id="15097-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-242">0x8024</span></span>                          |
| <span data-ttu-id="15097-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-243">System-Only</span></span>            | <span data-ttu-id="15097-244">True</span><span class="sxs-lookup"><span data-stu-id="15097-244">True</span></span>                            |
| <span data-ttu-id="15097-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-245">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-246">False</span></span>                           |
| <span data-ttu-id="15097-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-247">Is Indexed</span></span>             | <span data-ttu-id="15097-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-248">False</span></span>                           |
| <span data-ttu-id="15097-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-249">In Global Catalog</span></span>      | <span data-ttu-id="15097-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-250">False</span></span>                           |
| <span data-ttu-id="15097-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-255">Search-Flags</span></span>           | <span data-ttu-id="15097-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-256">0x00000000</span></span>                      |
| <span data-ttu-id="15097-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-257">System-Flags</span></span>           | <span data-ttu-id="15097-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-258">0x00000010</span></span>                      |
| <span data-ttu-id="15097-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-259">Classes used in</span></span>        | [<span data-ttu-id="15097-260">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="15097-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15097-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="15097-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-262">Entry</span></span> | <span data-ttu-id="15097-263">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-264">Link-Id</span></span>                | <span data-ttu-id="15097-265">73</span><span class="sxs-lookup"><span data-stu-id="15097-265">73</span></span>                              |
| <span data-ttu-id="15097-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-266">MAPI-Id</span></span>                | <span data-ttu-id="15097-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-267">0x8024</span></span>                          |
| <span data-ttu-id="15097-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-268">System-Only</span></span>            | <span data-ttu-id="15097-269">True</span><span class="sxs-lookup"><span data-stu-id="15097-269">True</span></span>                            |
| <span data-ttu-id="15097-270">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-270">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-271">False</span></span>                           |
| <span data-ttu-id="15097-272">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-272">Is Indexed</span></span>             | <span data-ttu-id="15097-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-273">False</span></span>                           |
| <span data-ttu-id="15097-274">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-274">In Global Catalog</span></span>      | <span data-ttu-id="15097-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-275">False</span></span>                           |
| <span data-ttu-id="15097-276">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-277">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-280">Search-Flags</span></span>           | <span data-ttu-id="15097-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-281">0x00000000</span></span>                      |
| <span data-ttu-id="15097-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-282">System-Flags</span></span>           | <span data-ttu-id="15097-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-283">0x00000010</span></span>                      |
| <span data-ttu-id="15097-284">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-284">Classes used in</span></span>        | [<span data-ttu-id="15097-285">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="15097-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15097-286">Windows Server 2012</span></span>



| <span data-ttu-id="15097-287">Ввод</span><span class="sxs-lookup"><span data-stu-id="15097-287">Entry</span></span> | <span data-ttu-id="15097-288">Значение</span><span class="sxs-lookup"><span data-stu-id="15097-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15097-289">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="15097-289">Link-Id</span></span>                | <span data-ttu-id="15097-290">73</span><span class="sxs-lookup"><span data-stu-id="15097-290">73</span></span>                              |
| <span data-ttu-id="15097-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15097-291">MAPI-Id</span></span>                | <span data-ttu-id="15097-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="15097-292">0x8024</span></span>                          |
| <span data-ttu-id="15097-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="15097-293">System-Only</span></span>            | <span data-ttu-id="15097-294">True</span><span class="sxs-lookup"><span data-stu-id="15097-294">True</span></span>                            |
| <span data-ttu-id="15097-295">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="15097-295">Is-Single-Valued</span></span>       | <span data-ttu-id="15097-296">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-296">False</span></span>                           |
| <span data-ttu-id="15097-297">Индексируется</span><span class="sxs-lookup"><span data-stu-id="15097-297">Is Indexed</span></span>             | <span data-ttu-id="15097-298">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-298">False</span></span>                           |
| <span data-ttu-id="15097-299">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="15097-299">In Global Catalog</span></span>      | <span data-ttu-id="15097-300">Неверно</span><span class="sxs-lookup"><span data-stu-id="15097-300">False</span></span>                           |
| <span data-ttu-id="15097-301">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="15097-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="15097-302">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15097-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15097-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15097-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15097-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15097-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15097-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-305">Search-Flags</span></span>           | <span data-ttu-id="15097-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15097-306">0x00000000</span></span>                      |
| <span data-ttu-id="15097-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15097-307">System-Flags</span></span>           | <span data-ttu-id="15097-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15097-308">0x00000010</span></span>                      |
| <span data-ttu-id="15097-309">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="15097-309">Classes used in</span></span>        | [<span data-ttu-id="15097-310">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="15097-310">**Top**</span></span>](c-top.md)<br/> |



 

 





