---
title: Атрибут Субсчемасубентри
description: Различающееся имя расположения объекта подсхемы, в котором определен класс или атрибут.
ms.assetid: 16beeb31-436c-4ae1-b1f7-fa00abb3bcbb
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Субсчемасубентри
- Схема AD атрибута Субсчемасубентри
topic_type:
- apiref
api_name:
- SubSchemaSubEntry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0278d63d3a6ed9d0f84ad67df87e248af31f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535885"
---
# <a name="subschemasubentry-attribute"></a><span data-ttu-id="eb874-105">Атрибут Субсчемасубентри</span><span class="sxs-lookup"><span data-stu-id="eb874-105">SubSchemaSubEntry attribute</span></span>

<span data-ttu-id="eb874-106">Различающееся имя расположения объекта подсхемы, в котором определен класс или атрибут.</span><span class="sxs-lookup"><span data-stu-id="eb874-106">The distinguished name for the location of the subschema object where a class or attribute is defined.</span></span>



| <span data-ttu-id="eb874-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-107">Entry</span></span> | <span data-ttu-id="eb874-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb874-109">CN</span><span class="sxs-lookup"><span data-stu-id="eb874-109">CN</span></span>                | <span data-ttu-id="eb874-110">субсчемасубентри</span><span class="sxs-lookup"><span data-stu-id="eb874-110">SubSchemaSubEntry</span></span>                                                                |
| <span data-ttu-id="eb874-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="eb874-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eb874-112">субсчемасубентри</span><span class="sxs-lookup"><span data-stu-id="eb874-112">subSchemaSubEntry</span></span>                                                                |
| <span data-ttu-id="eb874-113">Размер</span><span class="sxs-lookup"><span data-stu-id="eb874-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="eb874-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="eb874-114">Update Privilege</span></span>  | <span data-ttu-id="eb874-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="eb874-115">Schema administrator</span></span>                                                             |
| <span data-ttu-id="eb874-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="eb874-116">Update Frequency</span></span>  | <span data-ttu-id="eb874-117">При загрузке Active Directory или при определении нового класса или атрибута.</span><span class="sxs-lookup"><span data-stu-id="eb874-117">When the Active Directory is loaded or when a new class or attribute is defined.</span></span> |
| <span data-ttu-id="eb874-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-118">Attribute-Id</span></span>      | <span data-ttu-id="eb874-119">2.5.18.10</span><span class="sxs-lookup"><span data-stu-id="eb874-119">2.5.18.10</span></span>                                                                        |
| <span data-ttu-id="eb874-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="eb874-120">System-Id-Guid</span></span>    | <span data-ttu-id="eb874-121">9a7ad94d-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="eb874-121">9a7ad94d-ca53-11d1-bbd0-0080c76670c0</span></span>                                             |
| <span data-ttu-id="eb874-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb874-122">Syntax</span></span>            | [<span data-ttu-id="eb874-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="eb874-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                          |



## <a name="implementations"></a><span data-ttu-id="eb874-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="eb874-124">Implementations</span></span>

-   [<span data-ttu-id="eb874-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eb874-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eb874-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eb874-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eb874-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="eb874-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="eb874-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eb874-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eb874-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eb874-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eb874-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eb874-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eb874-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eb874-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eb874-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb874-132">Windows 2000 Server</span></span>



| <span data-ttu-id="eb874-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-133">Entry</span></span> | <span data-ttu-id="eb874-134">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-137">System-Only</span></span>            | <span data-ttu-id="eb874-138">True</span><span class="sxs-lookup"><span data-stu-id="eb874-138">True</span></span>                            |
| <span data-ttu-id="eb874-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-139">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-140">False</span></span>                           |
| <span data-ttu-id="eb874-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-141">Is Indexed</span></span>             | <span data-ttu-id="eb874-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-142">False</span></span>                           |
| <span data-ttu-id="eb874-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-143">In Global Catalog</span></span>      | <span data-ttu-id="eb874-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-144">False</span></span>                           |
| <span data-ttu-id="eb874-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-149">Search-Flags</span></span>           | <span data-ttu-id="eb874-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-150">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-151">System-Flags</span></span>           | <span data-ttu-id="eb874-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-152">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-153">Classes used in</span></span>        | [<span data-ttu-id="eb874-154">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eb874-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb874-155">Windows Server 2003</span></span>



| <span data-ttu-id="eb874-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-156">Entry</span></span> | <span data-ttu-id="eb874-157">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-160">System-Only</span></span>            | <span data-ttu-id="eb874-161">True</span><span class="sxs-lookup"><span data-stu-id="eb874-161">True</span></span>                            |
| <span data-ttu-id="eb874-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-162">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-163">False</span></span>                           |
| <span data-ttu-id="eb874-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-164">Is Indexed</span></span>             | <span data-ttu-id="eb874-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-165">False</span></span>                           |
| <span data-ttu-id="eb874-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-166">In Global Catalog</span></span>      | <span data-ttu-id="eb874-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-167">False</span></span>                           |
| <span data-ttu-id="eb874-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-172">Search-Flags</span></span>           | <span data-ttu-id="eb874-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-173">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-174">System-Flags</span></span>           | <span data-ttu-id="eb874-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-175">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-176">Classes used in</span></span>        | [<span data-ttu-id="eb874-177">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="eb874-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="eb874-178">ADAM</span></span>



| <span data-ttu-id="eb874-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-179">Entry</span></span> | <span data-ttu-id="eb874-180">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-183">System-Only</span></span>            | <span data-ttu-id="eb874-184">True</span><span class="sxs-lookup"><span data-stu-id="eb874-184">True</span></span>                            |
| <span data-ttu-id="eb874-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-185">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-186">False</span></span>                           |
| <span data-ttu-id="eb874-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-187">Is Indexed</span></span>             | <span data-ttu-id="eb874-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-188">False</span></span>                           |
| <span data-ttu-id="eb874-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-189">In Global Catalog</span></span>      | <span data-ttu-id="eb874-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-190">False</span></span>                           |
| <span data-ttu-id="eb874-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-195">Search-Flags</span></span>           | <span data-ttu-id="eb874-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-196">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-197">System-Flags</span></span>           | <span data-ttu-id="eb874-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-198">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-199">Classes used in</span></span>        | [<span data-ttu-id="eb874-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eb874-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eb874-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eb874-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-202">Entry</span></span> | <span data-ttu-id="eb874-203">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-206">System-Only</span></span>            | <span data-ttu-id="eb874-207">True</span><span class="sxs-lookup"><span data-stu-id="eb874-207">True</span></span>                            |
| <span data-ttu-id="eb874-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-208">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-209">False</span></span>                           |
| <span data-ttu-id="eb874-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-210">Is Indexed</span></span>             | <span data-ttu-id="eb874-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-211">False</span></span>                           |
| <span data-ttu-id="eb874-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-212">In Global Catalog</span></span>      | <span data-ttu-id="eb874-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-213">False</span></span>                           |
| <span data-ttu-id="eb874-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-218">Search-Flags</span></span>           | <span data-ttu-id="eb874-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-219">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-220">System-Flags</span></span>           | <span data-ttu-id="eb874-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-221">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-222">Classes used in</span></span>        | [<span data-ttu-id="eb874-223">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eb874-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb874-224">Windows Server 2008</span></span>



| <span data-ttu-id="eb874-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-225">Entry</span></span> | <span data-ttu-id="eb874-226">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-229">System-Only</span></span>            | <span data-ttu-id="eb874-230">True</span><span class="sxs-lookup"><span data-stu-id="eb874-230">True</span></span>                            |
| <span data-ttu-id="eb874-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-231">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-232">False</span></span>                           |
| <span data-ttu-id="eb874-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-233">Is Indexed</span></span>             | <span data-ttu-id="eb874-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-234">False</span></span>                           |
| <span data-ttu-id="eb874-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-235">In Global Catalog</span></span>      | <span data-ttu-id="eb874-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-236">False</span></span>                           |
| <span data-ttu-id="eb874-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-241">Search-Flags</span></span>           | <span data-ttu-id="eb874-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-242">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-243">System-Flags</span></span>           | <span data-ttu-id="eb874-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-244">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-245">Classes used in</span></span>        | [<span data-ttu-id="eb874-246">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eb874-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb874-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eb874-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-248">Entry</span></span> | <span data-ttu-id="eb874-249">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-252">System-Only</span></span>            | <span data-ttu-id="eb874-253">True</span><span class="sxs-lookup"><span data-stu-id="eb874-253">True</span></span>                            |
| <span data-ttu-id="eb874-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-254">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-255">False</span></span>                           |
| <span data-ttu-id="eb874-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-256">Is Indexed</span></span>             | <span data-ttu-id="eb874-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-257">False</span></span>                           |
| <span data-ttu-id="eb874-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-258">In Global Catalog</span></span>      | <span data-ttu-id="eb874-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-259">False</span></span>                           |
| <span data-ttu-id="eb874-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-264">Search-Flags</span></span>           | <span data-ttu-id="eb874-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-265">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-266">System-Flags</span></span>           | <span data-ttu-id="eb874-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-267">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-268">Classes used in</span></span>        | [<span data-ttu-id="eb874-269">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eb874-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb874-270">Windows Server 2012</span></span>



| <span data-ttu-id="eb874-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb874-271">Entry</span></span> | <span data-ttu-id="eb874-272">Значение</span><span class="sxs-lookup"><span data-stu-id="eb874-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eb874-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb874-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb874-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eb874-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb874-275">System-Only</span></span>            | <span data-ttu-id="eb874-276">True</span><span class="sxs-lookup"><span data-stu-id="eb874-276">True</span></span>                            |
| <span data-ttu-id="eb874-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb874-277">Is-Single-Valued</span></span>       | <span data-ttu-id="eb874-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-278">False</span></span>                           |
| <span data-ttu-id="eb874-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb874-279">Is Indexed</span></span>             | <span data-ttu-id="eb874-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-280">False</span></span>                           |
| <span data-ttu-id="eb874-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb874-281">In Global Catalog</span></span>      | <span data-ttu-id="eb874-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb874-282">False</span></span>                           |
| <span data-ttu-id="eb874-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb874-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb874-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb874-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eb874-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb874-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eb874-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb874-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eb874-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-287">Search-Flags</span></span>           | <span data-ttu-id="eb874-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb874-288">0x00000000</span></span>                      |
| <span data-ttu-id="eb874-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb874-289">System-Flags</span></span>           | <span data-ttu-id="eb874-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="eb874-290">0x08000014</span></span>                      |
| <span data-ttu-id="eb874-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb874-291">Classes used in</span></span>        | [<span data-ttu-id="eb874-292">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eb874-292">**Top**</span></span>](c-top.md)<br/> |



 

 





