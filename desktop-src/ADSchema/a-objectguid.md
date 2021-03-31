---
title: Атрибут Object-Guid
description: Уникальный идентификатор объекта.
ms.assetid: fc2d65a3-7472-41ef-9780-d1a7ec965804
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Guid
- Схема AD атрибута objectGUID
topic_type:
- apiref
api_name:
- Object-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e3715c38b629869296e6f8df5dbebd9a515d1b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893726"
---
# <a name="object-guid-attribute"></a><span data-ttu-id="586d0-105">Атрибут Object-Guid</span><span class="sxs-lookup"><span data-stu-id="586d0-105">Object-Guid attribute</span></span>

<span data-ttu-id="586d0-106">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="586d0-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="586d0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-107">Entry</span></span> | <span data-ttu-id="586d0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="586d0-109">CN</span><span class="sxs-lookup"><span data-stu-id="586d0-109">CN</span></span>                | <span data-ttu-id="586d0-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="586d0-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="586d0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="586d0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="586d0-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="586d0-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="586d0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="586d0-113">Size</span></span>              | <span data-ttu-id="586d0-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="586d0-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="586d0-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="586d0-115">Update Privilege</span></span>  | <span data-ttu-id="586d0-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="586d0-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="586d0-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="586d0-117">Update Frequency</span></span>  | <span data-ttu-id="586d0-118">Это значение задается при создании объекта и не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="586d0-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="586d0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-119">Attribute-Id</span></span>      | <span data-ttu-id="586d0-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="586d0-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="586d0-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="586d0-121">System-Id-Guid</span></span>    | <span data-ttu-id="586d0-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="586d0-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="586d0-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="586d0-123">Syntax</span></span>            | [<span data-ttu-id="586d0-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="586d0-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="586d0-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="586d0-125">Implementations</span></span>

-   [<span data-ttu-id="586d0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="586d0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="586d0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="586d0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="586d0-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="586d0-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="586d0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="586d0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="586d0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="586d0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="586d0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="586d0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="586d0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="586d0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="586d0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="586d0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="586d0-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-134">Entry</span></span> | <span data-ttu-id="586d0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-137">MAPI-Id</span></span>                | <span data-ttu-id="586d0-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-138">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-139">System-Only</span></span>            | <span data-ttu-id="586d0-140">True</span><span class="sxs-lookup"><span data-stu-id="586d0-140">True</span></span>                            |
| <span data-ttu-id="586d0-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-142">True</span><span class="sxs-lookup"><span data-stu-id="586d0-142">True</span></span>                            |
| <span data-ttu-id="586d0-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-143">Is Indexed</span></span>             | <span data-ttu-id="586d0-144">True</span><span class="sxs-lookup"><span data-stu-id="586d0-144">True</span></span>                            |
| <span data-ttu-id="586d0-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-145">In Global Catalog</span></span>      | <span data-ttu-id="586d0-146">True</span><span class="sxs-lookup"><span data-stu-id="586d0-146">True</span></span>                            |
| <span data-ttu-id="586d0-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-149">Range-Lower</span></span>            | <span data-ttu-id="586d0-150">16</span><span class="sxs-lookup"><span data-stu-id="586d0-150">16</span></span>                              |
| <span data-ttu-id="586d0-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-151">Range-Upper</span></span>            | <span data-ttu-id="586d0-152">16</span><span class="sxs-lookup"><span data-stu-id="586d0-152">16</span></span>                              |
| <span data-ttu-id="586d0-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-153">Search-Flags</span></span>           | <span data-ttu-id="586d0-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-154">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-155">System-Flags</span></span>           | <span data-ttu-id="586d0-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-156">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-157">Classes used in</span></span>        | [<span data-ttu-id="586d0-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="586d0-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="586d0-159">Windows Server 2003</span></span>



| <span data-ttu-id="586d0-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-160">Entry</span></span> | <span data-ttu-id="586d0-161">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-163">MAPI-Id</span></span>                | <span data-ttu-id="586d0-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-164">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-165">System-Only</span></span>            | <span data-ttu-id="586d0-166">True</span><span class="sxs-lookup"><span data-stu-id="586d0-166">True</span></span>                            |
| <span data-ttu-id="586d0-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-167">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-168">True</span><span class="sxs-lookup"><span data-stu-id="586d0-168">True</span></span>                            |
| <span data-ttu-id="586d0-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-169">Is Indexed</span></span>             | <span data-ttu-id="586d0-170">True</span><span class="sxs-lookup"><span data-stu-id="586d0-170">True</span></span>                            |
| <span data-ttu-id="586d0-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-171">In Global Catalog</span></span>      | <span data-ttu-id="586d0-172">True</span><span class="sxs-lookup"><span data-stu-id="586d0-172">True</span></span>                            |
| <span data-ttu-id="586d0-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-175">Range-Lower</span></span>            | <span data-ttu-id="586d0-176">16</span><span class="sxs-lookup"><span data-stu-id="586d0-176">16</span></span>                              |
| <span data-ttu-id="586d0-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-177">Range-Upper</span></span>            | <span data-ttu-id="586d0-178">16</span><span class="sxs-lookup"><span data-stu-id="586d0-178">16</span></span>                              |
| <span data-ttu-id="586d0-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-179">Search-Flags</span></span>           | <span data-ttu-id="586d0-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-180">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-181">System-Flags</span></span>           | <span data-ttu-id="586d0-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-182">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-183">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-183">Classes used in</span></span>        | [<span data-ttu-id="586d0-184">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="586d0-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="586d0-185">ADAM</span></span>



| <span data-ttu-id="586d0-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-186">Entry</span></span> | <span data-ttu-id="586d0-187">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-189">MAPI-Id</span></span>                | <span data-ttu-id="586d0-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-190">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-191">System-Only</span></span>            | <span data-ttu-id="586d0-192">True</span><span class="sxs-lookup"><span data-stu-id="586d0-192">True</span></span>                            |
| <span data-ttu-id="586d0-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-193">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-194">True</span><span class="sxs-lookup"><span data-stu-id="586d0-194">True</span></span>                            |
| <span data-ttu-id="586d0-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-195">Is Indexed</span></span>             | <span data-ttu-id="586d0-196">True</span><span class="sxs-lookup"><span data-stu-id="586d0-196">True</span></span>                            |
| <span data-ttu-id="586d0-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-197">In Global Catalog</span></span>      | <span data-ttu-id="586d0-198">True</span><span class="sxs-lookup"><span data-stu-id="586d0-198">True</span></span>                            |
| <span data-ttu-id="586d0-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-201">Range-Lower</span></span>            | <span data-ttu-id="586d0-202">16</span><span class="sxs-lookup"><span data-stu-id="586d0-202">16</span></span>                              |
| <span data-ttu-id="586d0-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-203">Range-Upper</span></span>            | <span data-ttu-id="586d0-204">16</span><span class="sxs-lookup"><span data-stu-id="586d0-204">16</span></span>                              |
| <span data-ttu-id="586d0-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-205">Search-Flags</span></span>           | <span data-ttu-id="586d0-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-206">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-207">System-Flags</span></span>           | <span data-ttu-id="586d0-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-208">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-209">Classes used in</span></span>        | [<span data-ttu-id="586d0-210">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="586d0-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="586d0-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="586d0-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-212">Entry</span></span> | <span data-ttu-id="586d0-213">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-215">MAPI-Id</span></span>                | <span data-ttu-id="586d0-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-216">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-217">System-Only</span></span>            | <span data-ttu-id="586d0-218">True</span><span class="sxs-lookup"><span data-stu-id="586d0-218">True</span></span>                            |
| <span data-ttu-id="586d0-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-219">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-220">True</span><span class="sxs-lookup"><span data-stu-id="586d0-220">True</span></span>                            |
| <span data-ttu-id="586d0-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-221">Is Indexed</span></span>             | <span data-ttu-id="586d0-222">True</span><span class="sxs-lookup"><span data-stu-id="586d0-222">True</span></span>                            |
| <span data-ttu-id="586d0-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-223">In Global Catalog</span></span>      | <span data-ttu-id="586d0-224">True</span><span class="sxs-lookup"><span data-stu-id="586d0-224">True</span></span>                            |
| <span data-ttu-id="586d0-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-227">Range-Lower</span></span>            | <span data-ttu-id="586d0-228">16</span><span class="sxs-lookup"><span data-stu-id="586d0-228">16</span></span>                              |
| <span data-ttu-id="586d0-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-229">Range-Upper</span></span>            | <span data-ttu-id="586d0-230">16</span><span class="sxs-lookup"><span data-stu-id="586d0-230">16</span></span>                              |
| <span data-ttu-id="586d0-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-231">Search-Flags</span></span>           | <span data-ttu-id="586d0-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-232">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-233">System-Flags</span></span>           | <span data-ttu-id="586d0-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-234">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-235">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-235">Classes used in</span></span>        | [<span data-ttu-id="586d0-236">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="586d0-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="586d0-237">Windows Server 2008</span></span>



| <span data-ttu-id="586d0-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-238">Entry</span></span> | <span data-ttu-id="586d0-239">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-241">MAPI-Id</span></span>                | <span data-ttu-id="586d0-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-242">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-243">System-Only</span></span>            | <span data-ttu-id="586d0-244">True</span><span class="sxs-lookup"><span data-stu-id="586d0-244">True</span></span>                            |
| <span data-ttu-id="586d0-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-245">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-246">True</span><span class="sxs-lookup"><span data-stu-id="586d0-246">True</span></span>                            |
| <span data-ttu-id="586d0-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-247">Is Indexed</span></span>             | <span data-ttu-id="586d0-248">True</span><span class="sxs-lookup"><span data-stu-id="586d0-248">True</span></span>                            |
| <span data-ttu-id="586d0-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-249">In Global Catalog</span></span>      | <span data-ttu-id="586d0-250">True</span><span class="sxs-lookup"><span data-stu-id="586d0-250">True</span></span>                            |
| <span data-ttu-id="586d0-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-253">Range-Lower</span></span>            | <span data-ttu-id="586d0-254">16</span><span class="sxs-lookup"><span data-stu-id="586d0-254">16</span></span>                              |
| <span data-ttu-id="586d0-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-255">Range-Upper</span></span>            | <span data-ttu-id="586d0-256">16</span><span class="sxs-lookup"><span data-stu-id="586d0-256">16</span></span>                              |
| <span data-ttu-id="586d0-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-257">Search-Flags</span></span>           | <span data-ttu-id="586d0-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-258">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-259">System-Flags</span></span>           | <span data-ttu-id="586d0-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-260">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-261">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-261">Classes used in</span></span>        | [<span data-ttu-id="586d0-262">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="586d0-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="586d0-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="586d0-264">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-264">Entry</span></span> | <span data-ttu-id="586d0-265">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-266">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-267">MAPI-Id</span></span>                | <span data-ttu-id="586d0-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-268">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-269">System-Only</span></span>            | <span data-ttu-id="586d0-270">True</span><span class="sxs-lookup"><span data-stu-id="586d0-270">True</span></span>                            |
| <span data-ttu-id="586d0-271">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-271">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-272">True</span><span class="sxs-lookup"><span data-stu-id="586d0-272">True</span></span>                            |
| <span data-ttu-id="586d0-273">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-273">Is Indexed</span></span>             | <span data-ttu-id="586d0-274">True</span><span class="sxs-lookup"><span data-stu-id="586d0-274">True</span></span>                            |
| <span data-ttu-id="586d0-275">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-275">In Global Catalog</span></span>      | <span data-ttu-id="586d0-276">True</span><span class="sxs-lookup"><span data-stu-id="586d0-276">True</span></span>                            |
| <span data-ttu-id="586d0-277">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-278">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-279">Range-Lower</span></span>            | <span data-ttu-id="586d0-280">16</span><span class="sxs-lookup"><span data-stu-id="586d0-280">16</span></span>                              |
| <span data-ttu-id="586d0-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-281">Range-Upper</span></span>            | <span data-ttu-id="586d0-282">16</span><span class="sxs-lookup"><span data-stu-id="586d0-282">16</span></span>                              |
| <span data-ttu-id="586d0-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-283">Search-Flags</span></span>           | <span data-ttu-id="586d0-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-284">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-285">System-Flags</span></span>           | <span data-ttu-id="586d0-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-286">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-287">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-287">Classes used in</span></span>        | [<span data-ttu-id="586d0-288">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="586d0-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="586d0-289">Windows Server 2012</span></span>



| <span data-ttu-id="586d0-290">Ввод</span><span class="sxs-lookup"><span data-stu-id="586d0-290">Entry</span></span> | <span data-ttu-id="586d0-291">Значение</span><span class="sxs-lookup"><span data-stu-id="586d0-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="586d0-292">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="586d0-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="586d0-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="586d0-293">MAPI-Id</span></span>                | <span data-ttu-id="586d0-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="586d0-294">0x8C6D</span></span>                          |
| <span data-ttu-id="586d0-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="586d0-295">System-Only</span></span>            | <span data-ttu-id="586d0-296">True</span><span class="sxs-lookup"><span data-stu-id="586d0-296">True</span></span>                            |
| <span data-ttu-id="586d0-297">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="586d0-297">Is-Single-Valued</span></span>       | <span data-ttu-id="586d0-298">True</span><span class="sxs-lookup"><span data-stu-id="586d0-298">True</span></span>                            |
| <span data-ttu-id="586d0-299">Индексируется</span><span class="sxs-lookup"><span data-stu-id="586d0-299">Is Indexed</span></span>             | <span data-ttu-id="586d0-300">True</span><span class="sxs-lookup"><span data-stu-id="586d0-300">True</span></span>                            |
| <span data-ttu-id="586d0-301">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="586d0-301">In Global Catalog</span></span>      | <span data-ttu-id="586d0-302">True</span><span class="sxs-lookup"><span data-stu-id="586d0-302">True</span></span>                            |
| <span data-ttu-id="586d0-303">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="586d0-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="586d0-304">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="586d0-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="586d0-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="586d0-305">Range-Lower</span></span>            | <span data-ttu-id="586d0-306">16</span><span class="sxs-lookup"><span data-stu-id="586d0-306">16</span></span>                              |
| <span data-ttu-id="586d0-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="586d0-307">Range-Upper</span></span>            | <span data-ttu-id="586d0-308">16</span><span class="sxs-lookup"><span data-stu-id="586d0-308">16</span></span>                              |
| <span data-ttu-id="586d0-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-309">Search-Flags</span></span>           | <span data-ttu-id="586d0-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="586d0-310">0x00000009</span></span>                      |
| <span data-ttu-id="586d0-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="586d0-311">System-Flags</span></span>           | <span data-ttu-id="586d0-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="586d0-312">0x00000013</span></span>                      |
| <span data-ttu-id="586d0-313">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="586d0-313">Classes used in</span></span>        | [<span data-ttu-id="586d0-314">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="586d0-314">**Top**</span></span>](c-top.md)<br/> |



 

 





