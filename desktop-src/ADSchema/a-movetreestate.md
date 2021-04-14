---
title: Атрибут перемещения-Tree-State
description: Этот атрибут содержит сведения о состоянии перемещаемого дерева каталогов.
ms.assetid: 13ec6d05-ed17-4a38-b2ae-7ad175f17b52
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута перемещения-дерева
- Схема AD атрибута Моветристате
topic_type:
- apiref
api_name:
- Move-Tree-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3041d54dfcdb97d7c9e1629162908fab1577b60c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493857"
---
# <a name="move-tree-state-attribute"></a><span data-ttu-id="45ece-105">Атрибут перемещения-Tree-State</span><span class="sxs-lookup"><span data-stu-id="45ece-105">Move-Tree-State attribute</span></span>

<span data-ttu-id="45ece-106">Этот атрибут содержит сведения о состоянии перемещаемого дерева каталогов.</span><span class="sxs-lookup"><span data-stu-id="45ece-106">This attribute contains state information for a directory tree that is being moved.</span></span>



| <span data-ttu-id="45ece-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-107">Entry</span></span> | <span data-ttu-id="45ece-108">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="45ece-109">CN</span><span class="sxs-lookup"><span data-stu-id="45ece-109">CN</span></span>                | <span data-ttu-id="45ece-110">Перемещение-дерево-состояние</span><span class="sxs-lookup"><span data-stu-id="45ece-110">Move-Tree-State</span></span>                                       |
| <span data-ttu-id="45ece-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="45ece-111">Ldap-Display-Name</span></span> | <span data-ttu-id="45ece-112">моветристате</span><span class="sxs-lookup"><span data-stu-id="45ece-112">moveTreeState</span></span>                                         |
| <span data-ttu-id="45ece-113">Размер</span><span class="sxs-lookup"><span data-stu-id="45ece-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="45ece-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="45ece-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="45ece-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="45ece-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="45ece-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-116">Attribute-Id</span></span>      | <span data-ttu-id="45ece-117">1.2.840.113556.1.4.1305</span><span class="sxs-lookup"><span data-stu-id="45ece-117">1.2.840.113556.1.4.1305</span></span>                               |
| <span data-ttu-id="45ece-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="45ece-118">System-Id-Guid</span></span>    | <span data-ttu-id="45ece-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="45ece-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="45ece-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45ece-120">Syntax</span></span>            | [<span data-ttu-id="45ece-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="45ece-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="45ece-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="45ece-122">Implementations</span></span>

-   [<span data-ttu-id="45ece-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="45ece-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="45ece-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="45ece-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="45ece-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="45ece-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="45ece-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="45ece-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="45ece-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="45ece-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="45ece-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="45ece-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="45ece-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="45ece-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="45ece-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45ece-130">Windows 2000 Server</span></span>



| <span data-ttu-id="45ece-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-131">Entry</span></span> | <span data-ttu-id="45ece-132">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-135">System-Only</span></span>            | <span data-ttu-id="45ece-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-136">False</span></span>                                               |
| <span data-ttu-id="45ece-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-137">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-138">False</span></span>                                               |
| <span data-ttu-id="45ece-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-139">Is Indexed</span></span>             | <span data-ttu-id="45ece-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-140">False</span></span>                                               |
| <span data-ttu-id="45ece-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-141">In Global Catalog</span></span>      | <span data-ttu-id="45ece-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-142">False</span></span>                                               |
| <span data-ttu-id="45ece-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-147">Search-Flags</span></span>           | <span data-ttu-id="45ece-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-148">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-149">System-Flags</span></span>           | <span data-ttu-id="45ece-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-150">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-151">Classes used in</span></span>        | [<span data-ttu-id="45ece-152">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-152">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="45ece-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45ece-153">Windows Server 2003</span></span>



| <span data-ttu-id="45ece-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-154">Entry</span></span> | <span data-ttu-id="45ece-155">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-158">System-Only</span></span>            | <span data-ttu-id="45ece-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-159">False</span></span>                                               |
| <span data-ttu-id="45ece-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-160">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-161">False</span></span>                                               |
| <span data-ttu-id="45ece-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-162">Is Indexed</span></span>             | <span data-ttu-id="45ece-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-163">False</span></span>                                               |
| <span data-ttu-id="45ece-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-164">In Global Catalog</span></span>      | <span data-ttu-id="45ece-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-165">False</span></span>                                               |
| <span data-ttu-id="45ece-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-170">Search-Flags</span></span>           | <span data-ttu-id="45ece-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-171">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-172">System-Flags</span></span>           | <span data-ttu-id="45ece-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-173">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-174">Classes used in</span></span>        | [<span data-ttu-id="45ece-175">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-175">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="adam"></a><span data-ttu-id="45ece-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="45ece-176">ADAM</span></span>



| <span data-ttu-id="45ece-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-177">Entry</span></span> | <span data-ttu-id="45ece-178">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-181">System-Only</span></span>            | <span data-ttu-id="45ece-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-182">False</span></span>                                               |
| <span data-ttu-id="45ece-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-183">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-184">False</span></span>                                               |
| <span data-ttu-id="45ece-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-185">Is Indexed</span></span>             | <span data-ttu-id="45ece-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-186">False</span></span>                                               |
| <span data-ttu-id="45ece-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-187">In Global Catalog</span></span>      | <span data-ttu-id="45ece-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-188">False</span></span>                                               |
| <span data-ttu-id="45ece-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-193">Search-Flags</span></span>           | <span data-ttu-id="45ece-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-194">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-195">System-Flags</span></span>           | <span data-ttu-id="45ece-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-196">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-197">Classes used in</span></span>        | [<span data-ttu-id="45ece-198">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-198">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="45ece-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="45ece-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="45ece-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-200">Entry</span></span> | <span data-ttu-id="45ece-201">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-204">System-Only</span></span>            | <span data-ttu-id="45ece-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-205">False</span></span>                                               |
| <span data-ttu-id="45ece-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-206">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-207">False</span></span>                                               |
| <span data-ttu-id="45ece-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-208">Is Indexed</span></span>             | <span data-ttu-id="45ece-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-209">False</span></span>                                               |
| <span data-ttu-id="45ece-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-210">In Global Catalog</span></span>      | <span data-ttu-id="45ece-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-211">False</span></span>                                               |
| <span data-ttu-id="45ece-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-216">Search-Flags</span></span>           | <span data-ttu-id="45ece-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-217">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-218">System-Flags</span></span>           | <span data-ttu-id="45ece-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-219">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-220">Classes used in</span></span>        | [<span data-ttu-id="45ece-221">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-221">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="45ece-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45ece-222">Windows Server 2008</span></span>



| <span data-ttu-id="45ece-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-223">Entry</span></span> | <span data-ttu-id="45ece-224">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-227">System-Only</span></span>            | <span data-ttu-id="45ece-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-228">False</span></span>                                               |
| <span data-ttu-id="45ece-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-229">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-230">False</span></span>                                               |
| <span data-ttu-id="45ece-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-231">Is Indexed</span></span>             | <span data-ttu-id="45ece-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-232">False</span></span>                                               |
| <span data-ttu-id="45ece-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-233">In Global Catalog</span></span>      | <span data-ttu-id="45ece-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-234">False</span></span>                                               |
| <span data-ttu-id="45ece-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-239">Search-Flags</span></span>           | <span data-ttu-id="45ece-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-240">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-241">System-Flags</span></span>           | <span data-ttu-id="45ece-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-242">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-243">Classes used in</span></span>        | [<span data-ttu-id="45ece-244">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-244">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="45ece-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45ece-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="45ece-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-246">Entry</span></span> | <span data-ttu-id="45ece-247">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-250">System-Only</span></span>            | <span data-ttu-id="45ece-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-251">False</span></span>                                               |
| <span data-ttu-id="45ece-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-252">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-253">False</span></span>                                               |
| <span data-ttu-id="45ece-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-254">Is Indexed</span></span>             | <span data-ttu-id="45ece-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-255">False</span></span>                                               |
| <span data-ttu-id="45ece-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-256">In Global Catalog</span></span>      | <span data-ttu-id="45ece-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-257">False</span></span>                                               |
| <span data-ttu-id="45ece-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-262">Search-Flags</span></span>           | <span data-ttu-id="45ece-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-263">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-264">System-Flags</span></span>           | <span data-ttu-id="45ece-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-265">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-266">Classes used in</span></span>        | [<span data-ttu-id="45ece-267">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-267">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="45ece-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45ece-268">Windows Server 2012</span></span>



| <span data-ttu-id="45ece-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="45ece-269">Entry</span></span> | <span data-ttu-id="45ece-270">Значение</span><span class="sxs-lookup"><span data-stu-id="45ece-270">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="45ece-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45ece-271">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45ece-272">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="45ece-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="45ece-273">System-Only</span></span>            | <span data-ttu-id="45ece-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-274">False</span></span>                                               |
| <span data-ttu-id="45ece-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45ece-275">Is-Single-Valued</span></span>       | <span data-ttu-id="45ece-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-276">False</span></span>                                               |
| <span data-ttu-id="45ece-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45ece-277">Is Indexed</span></span>             | <span data-ttu-id="45ece-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-278">False</span></span>                                               |
| <span data-ttu-id="45ece-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45ece-279">In Global Catalog</span></span>      | <span data-ttu-id="45ece-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="45ece-280">False</span></span>                                               |
| <span data-ttu-id="45ece-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45ece-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="45ece-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45ece-282">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="45ece-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45ece-283">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45ece-284">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="45ece-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-285">Search-Flags</span></span>           | <span data-ttu-id="45ece-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45ece-286">0x00000000</span></span>                                          |
| <span data-ttu-id="45ece-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45ece-287">System-Flags</span></span>           | <span data-ttu-id="45ece-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45ece-288">0x00000010</span></span>                                          |
| <span data-ttu-id="45ece-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45ece-289">Classes used in</span></span>        | [<span data-ttu-id="45ece-290">**Потерянные и найденные**</span><span class="sxs-lookup"><span data-stu-id="45ece-290">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



 

 





