---
title: Атрибут Reports
description: Содержит список пользователей, непосредственно сообщающих пользователю. Пользователи, перечисленные как отчеты, имеют свойство "Диспетчер свойств", установленное для этого пользователя. Каждый элемент в списке представляет собой связанную ссылку на объект, представляющий пользователя.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов отчетов
- Схема AD атрибута directReports
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655504"
---
# <a name="reports-attribute"></a><span data-ttu-id="b184a-107">Атрибут Reports</span><span class="sxs-lookup"><span data-stu-id="b184a-107">Reports attribute</span></span>

<span data-ttu-id="b184a-108">Содержит список пользователей, непосредственно сообщающих пользователю.</span><span class="sxs-lookup"><span data-stu-id="b184a-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="b184a-109">Пользователи, перечисленные как отчеты, имеют свойство "Диспетчер свойств", установленное для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b184a-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="b184a-110">Каждый элемент в списке представляет собой связанную ссылку на объект, представляющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="b184a-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="b184a-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-111">Entry</span></span> | <span data-ttu-id="b184a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="b184a-113">CN</span><span class="sxs-lookup"><span data-stu-id="b184a-113">CN</span></span>                | <span data-ttu-id="b184a-114">Отчеты</span><span class="sxs-lookup"><span data-stu-id="b184a-114">Reports</span></span>                                         |
| <span data-ttu-id="b184a-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b184a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b184a-116">directReports</span><span class="sxs-lookup"><span data-stu-id="b184a-116">directReports</span></span>                                   |
| <span data-ttu-id="b184a-117">Размер</span><span class="sxs-lookup"><span data-stu-id="b184a-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="b184a-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b184a-118">Update Privilege</span></span>  | <span data-ttu-id="b184a-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b184a-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="b184a-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b184a-120">Update Frequency</span></span>  | <span data-ttu-id="b184a-121">При каждом изменении непосредственных подчиненных пользователей.</span><span class="sxs-lookup"><span data-stu-id="b184a-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="b184a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-122">Attribute-Id</span></span>      | <span data-ttu-id="b184a-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="b184a-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="b184a-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b184a-124">System-Id-Guid</span></span>    | <span data-ttu-id="b184a-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b184a-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="b184a-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b184a-126">Syntax</span></span>            | [<span data-ttu-id="b184a-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b184a-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="b184a-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b184a-128">Implementations</span></span>

-   [<span data-ttu-id="b184a-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b184a-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b184a-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b184a-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b184a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b184a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b184a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b184a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b184a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b184a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b184a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b184a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b184a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b184a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b184a-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-136">Entry</span></span> | <span data-ttu-id="b184a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b184a-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b184a-138">Link-Id</span></span>                | <span data-ttu-id="b184a-139">43</span><span class="sxs-lookup"><span data-stu-id="b184a-139">43</span></span>                              |
| <span data-ttu-id="b184a-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-140">MAPI-Id</span></span>                | <span data-ttu-id="b184a-141">0x800E</span><span class="sxs-lookup"><span data-stu-id="b184a-141">0x800E</span></span>                          |
| <span data-ttu-id="b184a-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="b184a-142">System-Only</span></span>            | <span data-ttu-id="b184a-143">True</span><span class="sxs-lookup"><span data-stu-id="b184a-143">True</span></span>                            |
| <span data-ttu-id="b184a-144">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b184a-144">Is-Single-Valued</span></span>       | <span data-ttu-id="b184a-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-145">False</span></span>                           |
| <span data-ttu-id="b184a-146">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b184a-146">Is Indexed</span></span>             | <span data-ttu-id="b184a-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-147">False</span></span>                           |
| <span data-ttu-id="b184a-148">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b184a-148">In Global Catalog</span></span>      | <span data-ttu-id="b184a-149">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-149">False</span></span>                           |
| <span data-ttu-id="b184a-150">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b184a-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="b184a-151">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b184a-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b184a-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b184a-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b184a-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b184a-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b184a-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-154">Search-Flags</span></span>           | <span data-ttu-id="b184a-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b184a-155">0x00000000</span></span>                      |
| <span data-ttu-id="b184a-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-156">System-Flags</span></span>           | <span data-ttu-id="b184a-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b184a-157">0x00000010</span></span>                      |
| <span data-ttu-id="b184a-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b184a-158">Classes used in</span></span>        | [<span data-ttu-id="b184a-159">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b184a-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b184a-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b184a-160">Windows Server 2003</span></span>



| <span data-ttu-id="b184a-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-161">Entry</span></span> | <span data-ttu-id="b184a-162">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b184a-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b184a-163">Link-Id</span></span>                | <span data-ttu-id="b184a-164">43</span><span class="sxs-lookup"><span data-stu-id="b184a-164">43</span></span>                              |
| <span data-ttu-id="b184a-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-165">MAPI-Id</span></span>                | <span data-ttu-id="b184a-166">0x800E</span><span class="sxs-lookup"><span data-stu-id="b184a-166">0x800E</span></span>                          |
| <span data-ttu-id="b184a-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="b184a-167">System-Only</span></span>            | <span data-ttu-id="b184a-168">True</span><span class="sxs-lookup"><span data-stu-id="b184a-168">True</span></span>                            |
| <span data-ttu-id="b184a-169">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b184a-169">Is-Single-Valued</span></span>       | <span data-ttu-id="b184a-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-170">False</span></span>                           |
| <span data-ttu-id="b184a-171">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b184a-171">Is Indexed</span></span>             | <span data-ttu-id="b184a-172">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-172">False</span></span>                           |
| <span data-ttu-id="b184a-173">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b184a-173">In Global Catalog</span></span>      | <span data-ttu-id="b184a-174">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-174">False</span></span>                           |
| <span data-ttu-id="b184a-175">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b184a-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="b184a-176">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b184a-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b184a-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b184a-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b184a-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b184a-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b184a-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-179">Search-Flags</span></span>           | <span data-ttu-id="b184a-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b184a-180">0x00000000</span></span>                      |
| <span data-ttu-id="b184a-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-181">System-Flags</span></span>           | <span data-ttu-id="b184a-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b184a-182">0x00000010</span></span>                      |
| <span data-ttu-id="b184a-183">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b184a-183">Classes used in</span></span>        | [<span data-ttu-id="b184a-184">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b184a-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b184a-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b184a-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b184a-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-186">Entry</span></span> | <span data-ttu-id="b184a-187">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b184a-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b184a-188">Link-Id</span></span>                | <span data-ttu-id="b184a-189">43</span><span class="sxs-lookup"><span data-stu-id="b184a-189">43</span></span>                              |
| <span data-ttu-id="b184a-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-190">MAPI-Id</span></span>                | <span data-ttu-id="b184a-191">0x800E</span><span class="sxs-lookup"><span data-stu-id="b184a-191">0x800E</span></span>                          |
| <span data-ttu-id="b184a-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="b184a-192">System-Only</span></span>            | <span data-ttu-id="b184a-193">True</span><span class="sxs-lookup"><span data-stu-id="b184a-193">True</span></span>                            |
| <span data-ttu-id="b184a-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b184a-194">Is-Single-Valued</span></span>       | <span data-ttu-id="b184a-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-195">False</span></span>                           |
| <span data-ttu-id="b184a-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b184a-196">Is Indexed</span></span>             | <span data-ttu-id="b184a-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-197">False</span></span>                           |
| <span data-ttu-id="b184a-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b184a-198">In Global Catalog</span></span>      | <span data-ttu-id="b184a-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-199">False</span></span>                           |
| <span data-ttu-id="b184a-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b184a-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="b184a-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b184a-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b184a-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b184a-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b184a-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b184a-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b184a-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-204">Search-Flags</span></span>           | <span data-ttu-id="b184a-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b184a-205">0x00000000</span></span>                      |
| <span data-ttu-id="b184a-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-206">System-Flags</span></span>           | <span data-ttu-id="b184a-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b184a-207">0x00000010</span></span>                      |
| <span data-ttu-id="b184a-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b184a-208">Classes used in</span></span>        | [<span data-ttu-id="b184a-209">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b184a-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b184a-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b184a-210">Windows Server 2008</span></span>



| <span data-ttu-id="b184a-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-211">Entry</span></span> | <span data-ttu-id="b184a-212">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b184a-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b184a-213">Link-Id</span></span>                | <span data-ttu-id="b184a-214">43</span><span class="sxs-lookup"><span data-stu-id="b184a-214">43</span></span>                              |
| <span data-ttu-id="b184a-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-215">MAPI-Id</span></span>                | <span data-ttu-id="b184a-216">0x800E</span><span class="sxs-lookup"><span data-stu-id="b184a-216">0x800E</span></span>                          |
| <span data-ttu-id="b184a-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b184a-217">System-Only</span></span>            | <span data-ttu-id="b184a-218">True</span><span class="sxs-lookup"><span data-stu-id="b184a-218">True</span></span>                            |
| <span data-ttu-id="b184a-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b184a-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b184a-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-220">False</span></span>                           |
| <span data-ttu-id="b184a-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b184a-221">Is Indexed</span></span>             | <span data-ttu-id="b184a-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-222">False</span></span>                           |
| <span data-ttu-id="b184a-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b184a-223">In Global Catalog</span></span>      | <span data-ttu-id="b184a-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-224">False</span></span>                           |
| <span data-ttu-id="b184a-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b184a-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b184a-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b184a-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b184a-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b184a-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b184a-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b184a-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b184a-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-229">Search-Flags</span></span>           | <span data-ttu-id="b184a-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b184a-230">0x00000000</span></span>                      |
| <span data-ttu-id="b184a-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-231">System-Flags</span></span>           | <span data-ttu-id="b184a-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b184a-232">0x00000010</span></span>                      |
| <span data-ttu-id="b184a-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b184a-233">Classes used in</span></span>        | [<span data-ttu-id="b184a-234">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b184a-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b184a-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b184a-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b184a-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-236">Entry</span></span> | <span data-ttu-id="b184a-237">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b184a-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b184a-238">Link-Id</span></span>                | <span data-ttu-id="b184a-239">43</span><span class="sxs-lookup"><span data-stu-id="b184a-239">43</span></span>                              |
| <span data-ttu-id="b184a-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-240">MAPI-Id</span></span>                | <span data-ttu-id="b184a-241">0x800E</span><span class="sxs-lookup"><span data-stu-id="b184a-241">0x800E</span></span>                          |
| <span data-ttu-id="b184a-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="b184a-242">System-Only</span></span>            | <span data-ttu-id="b184a-243">True</span><span class="sxs-lookup"><span data-stu-id="b184a-243">True</span></span>                            |
| <span data-ttu-id="b184a-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b184a-244">Is-Single-Valued</span></span>       | <span data-ttu-id="b184a-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-245">False</span></span>                           |
| <span data-ttu-id="b184a-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b184a-246">Is Indexed</span></span>             | <span data-ttu-id="b184a-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-247">False</span></span>                           |
| <span data-ttu-id="b184a-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b184a-248">In Global Catalog</span></span>      | <span data-ttu-id="b184a-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-249">False</span></span>                           |
| <span data-ttu-id="b184a-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b184a-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="b184a-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b184a-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b184a-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b184a-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b184a-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b184a-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b184a-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-254">Search-Flags</span></span>           | <span data-ttu-id="b184a-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b184a-255">0x00000000</span></span>                      |
| <span data-ttu-id="b184a-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-256">System-Flags</span></span>           | <span data-ttu-id="b184a-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b184a-257">0x00000010</span></span>                      |
| <span data-ttu-id="b184a-258">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b184a-258">Classes used in</span></span>        | [<span data-ttu-id="b184a-259">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b184a-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b184a-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b184a-260">Windows Server 2012</span></span>



| <span data-ttu-id="b184a-261">Ввод</span><span class="sxs-lookup"><span data-stu-id="b184a-261">Entry</span></span> | <span data-ttu-id="b184a-262">Значение</span><span class="sxs-lookup"><span data-stu-id="b184a-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b184a-263">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b184a-263">Link-Id</span></span>                | <span data-ttu-id="b184a-264">43</span><span class="sxs-lookup"><span data-stu-id="b184a-264">43</span></span>                              |
| <span data-ttu-id="b184a-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b184a-265">MAPI-Id</span></span>                | <span data-ttu-id="b184a-266">0x800E</span><span class="sxs-lookup"><span data-stu-id="b184a-266">0x800E</span></span>                          |
| <span data-ttu-id="b184a-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="b184a-267">System-Only</span></span>            | <span data-ttu-id="b184a-268">True</span><span class="sxs-lookup"><span data-stu-id="b184a-268">True</span></span>                            |
| <span data-ttu-id="b184a-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b184a-269">Is-Single-Valued</span></span>       | <span data-ttu-id="b184a-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-270">False</span></span>                           |
| <span data-ttu-id="b184a-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b184a-271">Is Indexed</span></span>             | <span data-ttu-id="b184a-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-272">False</span></span>                           |
| <span data-ttu-id="b184a-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b184a-273">In Global Catalog</span></span>      | <span data-ttu-id="b184a-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="b184a-274">False</span></span>                           |
| <span data-ttu-id="b184a-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b184a-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="b184a-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b184a-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b184a-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b184a-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b184a-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b184a-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b184a-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-279">Search-Flags</span></span>           | <span data-ttu-id="b184a-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b184a-280">0x00000000</span></span>                      |
| <span data-ttu-id="b184a-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b184a-281">System-Flags</span></span>           | <span data-ttu-id="b184a-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b184a-282">0x00000010</span></span>                      |
| <span data-ttu-id="b184a-283">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b184a-283">Classes used in</span></span>        | [<span data-ttu-id="b184a-284">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b184a-284">**Top**</span></span>](c-top.md)<br/> |



 

 





