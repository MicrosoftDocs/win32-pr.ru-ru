---
title: Атрибут последнего известного родителя
description: Различающееся имя (DN) последнего известного родителя потерянного объекта.
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- Схема AD последних известных-родительских атрибутов
- Схема AD атрибута lastKnownParent
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655249"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="7b34f-105">Атрибут последнего известного родителя</span><span class="sxs-lookup"><span data-stu-id="7b34f-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="7b34f-106">Различающееся имя (DN) последнего известного родителя потерянного объекта.</span><span class="sxs-lookup"><span data-stu-id="7b34f-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="7b34f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-107">Entry</span></span> | <span data-ttu-id="7b34f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7b34f-109">CN</span><span class="sxs-lookup"><span data-stu-id="7b34f-109">CN</span></span>                | <span data-ttu-id="7b34f-110">Последний-известный-родительский</span><span class="sxs-lookup"><span data-stu-id="7b34f-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="7b34f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7b34f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7b34f-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="7b34f-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="7b34f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7b34f-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7b34f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7b34f-114">Update Privilege</span></span>  | <span data-ttu-id="7b34f-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="7b34f-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="7b34f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7b34f-116">Update Frequency</span></span>  | <span data-ttu-id="7b34f-117">Каждый раз, когда объект потерян.</span><span class="sxs-lookup"><span data-stu-id="7b34f-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="7b34f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-118">Attribute-Id</span></span>      | <span data-ttu-id="7b34f-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="7b34f-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="7b34f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7b34f-120">System-Id-Guid</span></span>    | <span data-ttu-id="7b34f-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7b34f-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="7b34f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b34f-122">Syntax</span></span>            | [<span data-ttu-id="7b34f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7b34f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7b34f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7b34f-124">Implementations</span></span>

-   [<span data-ttu-id="7b34f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7b34f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7b34f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7b34f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7b34f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7b34f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7b34f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7b34f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7b34f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7b34f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7b34f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7b34f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7b34f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7b34f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7b34f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b34f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7b34f-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-133">Entry</span></span> | <span data-ttu-id="7b34f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-137">System-Only</span></span>            | <span data-ttu-id="7b34f-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-138">False</span></span>                           |
| <span data-ttu-id="7b34f-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-140">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-140">True</span></span>                            |
| <span data-ttu-id="7b34f-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-141">Is Indexed</span></span>             | <span data-ttu-id="7b34f-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-142">False</span></span>                           |
| <span data-ttu-id="7b34f-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-143">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-144">False</span></span>                           |
| <span data-ttu-id="7b34f-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-149">Search-Flags</span></span>           | <span data-ttu-id="7b34f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-150">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-151">System-Flags</span></span>           | <span data-ttu-id="7b34f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-152">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-153">Classes used in</span></span>        | [<span data-ttu-id="7b34f-154">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7b34f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7b34f-155">Windows Server 2003</span></span>



| <span data-ttu-id="7b34f-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-156">Entry</span></span> | <span data-ttu-id="7b34f-157">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-160">System-Only</span></span>            | <span data-ttu-id="7b34f-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-161">False</span></span>                           |
| <span data-ttu-id="7b34f-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-163">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-163">True</span></span>                            |
| <span data-ttu-id="7b34f-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-164">Is Indexed</span></span>             | <span data-ttu-id="7b34f-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-165">False</span></span>                           |
| <span data-ttu-id="7b34f-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-166">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-167">False</span></span>                           |
| <span data-ttu-id="7b34f-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-172">Search-Flags</span></span>           | <span data-ttu-id="7b34f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-173">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-174">System-Flags</span></span>           | <span data-ttu-id="7b34f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-175">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-176">Classes used in</span></span>        | [<span data-ttu-id="7b34f-177">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7b34f-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="7b34f-178">ADAM</span></span>



| <span data-ttu-id="7b34f-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-179">Entry</span></span> | <span data-ttu-id="7b34f-180">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-183">System-Only</span></span>            | <span data-ttu-id="7b34f-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-184">False</span></span>                           |
| <span data-ttu-id="7b34f-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-186">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-186">True</span></span>                            |
| <span data-ttu-id="7b34f-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-187">Is Indexed</span></span>             | <span data-ttu-id="7b34f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-188">False</span></span>                           |
| <span data-ttu-id="7b34f-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-189">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-190">False</span></span>                           |
| <span data-ttu-id="7b34f-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-195">Search-Flags</span></span>           | <span data-ttu-id="7b34f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-196">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-197">System-Flags</span></span>           | <span data-ttu-id="7b34f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-198">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-199">Classes used in</span></span>        | [<span data-ttu-id="7b34f-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7b34f-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7b34f-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7b34f-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-202">Entry</span></span> | <span data-ttu-id="7b34f-203">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-206">System-Only</span></span>            | <span data-ttu-id="7b34f-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-207">False</span></span>                           |
| <span data-ttu-id="7b34f-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-209">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-209">True</span></span>                            |
| <span data-ttu-id="7b34f-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-210">Is Indexed</span></span>             | <span data-ttu-id="7b34f-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-211">False</span></span>                           |
| <span data-ttu-id="7b34f-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-212">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-213">False</span></span>                           |
| <span data-ttu-id="7b34f-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-218">Search-Flags</span></span>           | <span data-ttu-id="7b34f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-219">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-220">System-Flags</span></span>           | <span data-ttu-id="7b34f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-221">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-222">Classes used in</span></span>        | [<span data-ttu-id="7b34f-223">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7b34f-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b34f-224">Windows Server 2008</span></span>



| <span data-ttu-id="7b34f-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-225">Entry</span></span> | <span data-ttu-id="7b34f-226">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-229">System-Only</span></span>            | <span data-ttu-id="7b34f-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-230">False</span></span>                           |
| <span data-ttu-id="7b34f-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-232">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-232">True</span></span>                            |
| <span data-ttu-id="7b34f-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-233">Is Indexed</span></span>             | <span data-ttu-id="7b34f-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-234">False</span></span>                           |
| <span data-ttu-id="7b34f-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-235">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-236">False</span></span>                           |
| <span data-ttu-id="7b34f-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-241">Search-Flags</span></span>           | <span data-ttu-id="7b34f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-242">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-243">System-Flags</span></span>           | <span data-ttu-id="7b34f-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-244">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-245">Classes used in</span></span>        | [<span data-ttu-id="7b34f-246">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7b34f-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b34f-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7b34f-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-248">Entry</span></span> | <span data-ttu-id="7b34f-249">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-252">System-Only</span></span>            | <span data-ttu-id="7b34f-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-253">False</span></span>                           |
| <span data-ttu-id="7b34f-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-255">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-255">True</span></span>                            |
| <span data-ttu-id="7b34f-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-256">Is Indexed</span></span>             | <span data-ttu-id="7b34f-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-257">False</span></span>                           |
| <span data-ttu-id="7b34f-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-258">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-259">False</span></span>                           |
| <span data-ttu-id="7b34f-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-264">Search-Flags</span></span>           | <span data-ttu-id="7b34f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-265">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-266">System-Flags</span></span>           | <span data-ttu-id="7b34f-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-267">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-268">Classes used in</span></span>        | [<span data-ttu-id="7b34f-269">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7b34f-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b34f-270">Windows Server 2012</span></span>



| <span data-ttu-id="7b34f-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="7b34f-271">Entry</span></span> | <span data-ttu-id="7b34f-272">Значение</span><span class="sxs-lookup"><span data-stu-id="7b34f-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7b34f-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7b34f-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b34f-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7b34f-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b34f-275">System-Only</span></span>            | <span data-ttu-id="7b34f-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-276">False</span></span>                           |
| <span data-ttu-id="7b34f-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7b34f-277">Is-Single-Valued</span></span>       | <span data-ttu-id="7b34f-278">True</span><span class="sxs-lookup"><span data-stu-id="7b34f-278">True</span></span>                            |
| <span data-ttu-id="7b34f-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7b34f-279">Is Indexed</span></span>             | <span data-ttu-id="7b34f-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-280">False</span></span>                           |
| <span data-ttu-id="7b34f-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7b34f-281">In Global Catalog</span></span>      | <span data-ttu-id="7b34f-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="7b34f-282">False</span></span>                           |
| <span data-ttu-id="7b34f-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7b34f-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b34f-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7b34f-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7b34f-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b34f-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7b34f-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b34f-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7b34f-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-287">Search-Flags</span></span>           | <span data-ttu-id="7b34f-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b34f-288">0x00000000</span></span>                      |
| <span data-ttu-id="7b34f-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b34f-289">System-Flags</span></span>           | <span data-ttu-id="7b34f-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b34f-290">0x00000010</span></span>                      |
| <span data-ttu-id="7b34f-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7b34f-291">Classes used in</span></span>        | [<span data-ttu-id="7b34f-292">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7b34f-292">**Top**</span></span>](c-top.md)<br/> |



 

 





