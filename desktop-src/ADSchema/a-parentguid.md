---
title: Атрибут parent-GUID
description: Это сконструированный атрибут, созданный для поддержки элемента управления DirSync. Этот атрибут содержит objectGuid родителя объекта при репликации создания, переименования или перемещения объекта.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута parent-GUID
- Схема AD атрибута Парентгуид
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893705"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="d2abf-106">Атрибут parent-GUID</span><span class="sxs-lookup"><span data-stu-id="d2abf-106">Parent-GUID attribute</span></span>

<span data-ttu-id="d2abf-107">Это сконструированный атрибут, созданный для поддержки элемента управления DirSync.</span><span class="sxs-lookup"><span data-stu-id="d2abf-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="d2abf-108">Этот атрибут содержит objectGuid родителя объекта при репликации создания, переименования или перемещения объекта.</span><span class="sxs-lookup"><span data-stu-id="d2abf-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="d2abf-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-109">Entry</span></span> | <span data-ttu-id="d2abf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d2abf-111">CN</span><span class="sxs-lookup"><span data-stu-id="d2abf-111">CN</span></span>                | <span data-ttu-id="d2abf-112">Родительский элемент — GUID</span><span class="sxs-lookup"><span data-stu-id="d2abf-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="d2abf-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d2abf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d2abf-114">парентгуид</span><span class="sxs-lookup"><span data-stu-id="d2abf-114">parentGUID</span></span>                                            |
| <span data-ttu-id="d2abf-115">Размер</span><span class="sxs-lookup"><span data-stu-id="d2abf-115">Size</span></span>              | <span data-ttu-id="d2abf-116">16 байт</span><span class="sxs-lookup"><span data-stu-id="d2abf-116">16 bytes</span></span>                                              |
| <span data-ttu-id="d2abf-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d2abf-117">Update Privilege</span></span>  | <span data-ttu-id="d2abf-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="d2abf-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="d2abf-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d2abf-119">Update Frequency</span></span>  | <span data-ttu-id="d2abf-120">Во время репликации</span><span class="sxs-lookup"><span data-stu-id="d2abf-120">During replication</span></span>                                    |
| <span data-ttu-id="d2abf-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-121">Attribute-Id</span></span>      | <span data-ttu-id="d2abf-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="d2abf-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="d2abf-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d2abf-123">System-Id-Guid</span></span>    | <span data-ttu-id="d2abf-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="d2abf-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="d2abf-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2abf-125">Syntax</span></span>            | [<span data-ttu-id="d2abf-126">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="d2abf-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d2abf-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d2abf-127">Implementations</span></span>

-   [<span data-ttu-id="d2abf-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2abf-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2abf-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2abf-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2abf-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d2abf-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d2abf-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2abf-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2abf-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2abf-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2abf-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2abf-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2abf-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2abf-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2abf-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2abf-135">Windows 2000 Server</span></span>



| <span data-ttu-id="d2abf-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-136">Entry</span></span> | <span data-ttu-id="d2abf-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-140">System-Only</span></span>            | <span data-ttu-id="d2abf-141">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-141">True</span></span>         |
| <span data-ttu-id="d2abf-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-143">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-143">True</span></span>         |
| <span data-ttu-id="d2abf-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-144">Is Indexed</span></span>             | <span data-ttu-id="d2abf-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-145">False</span></span>        |
| <span data-ttu-id="d2abf-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-146">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-147">False</span></span>        |
| <span data-ttu-id="d2abf-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-152">Search-Flags</span></span>           | <span data-ttu-id="d2abf-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-153">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-154">System-Flags</span></span>           | <span data-ttu-id="d2abf-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-155">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="d2abf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2abf-157">Windows Server 2003</span></span>



| <span data-ttu-id="d2abf-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-158">Entry</span></span> | <span data-ttu-id="d2abf-159">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-162">System-Only</span></span>            | <span data-ttu-id="d2abf-163">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-163">True</span></span>         |
| <span data-ttu-id="d2abf-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-165">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-165">True</span></span>         |
| <span data-ttu-id="d2abf-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-166">Is Indexed</span></span>             | <span data-ttu-id="d2abf-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-167">False</span></span>        |
| <span data-ttu-id="d2abf-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-168">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-169">False</span></span>        |
| <span data-ttu-id="d2abf-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-174">Search-Flags</span></span>           | <span data-ttu-id="d2abf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-175">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-176">System-Flags</span></span>           | <span data-ttu-id="d2abf-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-177">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="d2abf-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="d2abf-179">ADAM</span></span>



| <span data-ttu-id="d2abf-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-180">Entry</span></span> | <span data-ttu-id="d2abf-181">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-184">System-Only</span></span>            | <span data-ttu-id="d2abf-185">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-185">True</span></span>         |
| <span data-ttu-id="d2abf-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-187">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-187">True</span></span>         |
| <span data-ttu-id="d2abf-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-188">Is Indexed</span></span>             | <span data-ttu-id="d2abf-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-189">False</span></span>        |
| <span data-ttu-id="d2abf-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-190">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-191">False</span></span>        |
| <span data-ttu-id="d2abf-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-196">Search-Flags</span></span>           | <span data-ttu-id="d2abf-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-197">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-198">System-Flags</span></span>           | <span data-ttu-id="d2abf-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-199">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2abf-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2abf-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2abf-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-202">Entry</span></span> | <span data-ttu-id="d2abf-203">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-206">System-Only</span></span>            | <span data-ttu-id="d2abf-207">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-207">True</span></span>         |
| <span data-ttu-id="d2abf-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-209">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-209">True</span></span>         |
| <span data-ttu-id="d2abf-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-210">Is Indexed</span></span>             | <span data-ttu-id="d2abf-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-211">False</span></span>        |
| <span data-ttu-id="d2abf-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-212">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-213">False</span></span>        |
| <span data-ttu-id="d2abf-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-218">Search-Flags</span></span>           | <span data-ttu-id="d2abf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-219">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-220">System-Flags</span></span>           | <span data-ttu-id="d2abf-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-221">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="d2abf-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2abf-223">Windows Server 2008</span></span>



| <span data-ttu-id="d2abf-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-224">Entry</span></span> | <span data-ttu-id="d2abf-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-228">System-Only</span></span>            | <span data-ttu-id="d2abf-229">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-229">True</span></span>         |
| <span data-ttu-id="d2abf-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-231">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-231">True</span></span>         |
| <span data-ttu-id="d2abf-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-232">Is Indexed</span></span>             | <span data-ttu-id="d2abf-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-233">False</span></span>        |
| <span data-ttu-id="d2abf-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-234">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-235">False</span></span>        |
| <span data-ttu-id="d2abf-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-240">Search-Flags</span></span>           | <span data-ttu-id="d2abf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-241">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-242">System-Flags</span></span>           | <span data-ttu-id="d2abf-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-243">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2abf-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2abf-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2abf-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-246">Entry</span></span> | <span data-ttu-id="d2abf-247">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-250">System-Only</span></span>            | <span data-ttu-id="d2abf-251">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-251">True</span></span>         |
| <span data-ttu-id="d2abf-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-253">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-253">True</span></span>         |
| <span data-ttu-id="d2abf-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-254">Is Indexed</span></span>             | <span data-ttu-id="d2abf-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-255">False</span></span>        |
| <span data-ttu-id="d2abf-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-256">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-257">False</span></span>        |
| <span data-ttu-id="d2abf-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-262">Search-Flags</span></span>           | <span data-ttu-id="d2abf-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-263">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-264">System-Flags</span></span>           | <span data-ttu-id="d2abf-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-265">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="d2abf-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2abf-267">Windows Server 2012</span></span>



| <span data-ttu-id="d2abf-268">Ввод</span><span class="sxs-lookup"><span data-stu-id="d2abf-268">Entry</span></span> | <span data-ttu-id="d2abf-269">Значение</span><span class="sxs-lookup"><span data-stu-id="d2abf-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d2abf-270">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d2abf-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2abf-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d2abf-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2abf-272">System-Only</span></span>            | <span data-ttu-id="d2abf-273">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-273">True</span></span>         |
| <span data-ttu-id="d2abf-274">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d2abf-274">Is-Single-Valued</span></span>       | <span data-ttu-id="d2abf-275">True</span><span class="sxs-lookup"><span data-stu-id="d2abf-275">True</span></span>         |
| <span data-ttu-id="d2abf-276">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d2abf-276">Is Indexed</span></span>             | <span data-ttu-id="d2abf-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-277">False</span></span>        |
| <span data-ttu-id="d2abf-278">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2abf-278">In Global Catalog</span></span>      | <span data-ttu-id="d2abf-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="d2abf-279">False</span></span>        |
| <span data-ttu-id="d2abf-280">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d2abf-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2abf-281">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2abf-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d2abf-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2abf-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d2abf-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2abf-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d2abf-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-284">Search-Flags</span></span>           | <span data-ttu-id="d2abf-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2abf-285">0x00000000</span></span>   |
| <span data-ttu-id="d2abf-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2abf-286">System-Flags</span></span>           | <span data-ttu-id="d2abf-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="d2abf-287">0x08000014</span></span>   |
| <span data-ttu-id="d2abf-288">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d2abf-288">Classes used in</span></span>        | \-           |



 

 




