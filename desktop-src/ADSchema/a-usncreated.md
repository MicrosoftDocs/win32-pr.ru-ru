---
title: Атрибут USN-Created
description: Последовательный номер обновления (USN), назначенный при создании объекта. См. также изменения USN.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута USN-Created
- Схема AD атрибута Уснкреатед
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655031"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="864cc-106">Атрибут USN-Created</span><span class="sxs-lookup"><span data-stu-id="864cc-106">USN-Created attribute</span></span>

<span data-ttu-id="864cc-107">Последовательный номер обновления (USN), назначенный при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="864cc-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="864cc-108">См. также [**изменения USN**](a-usnchanged.md).</span><span class="sxs-lookup"><span data-stu-id="864cc-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="864cc-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-109">Entry</span></span> | <span data-ttu-id="864cc-110">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="864cc-111">CN</span><span class="sxs-lookup"><span data-stu-id="864cc-111">CN</span></span>                | <span data-ttu-id="864cc-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="864cc-112">USN-Created</span></span>                          |
| <span data-ttu-id="864cc-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="864cc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="864cc-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="864cc-114">uSNCreated</span></span>                           |
| <span data-ttu-id="864cc-115">Размер</span><span class="sxs-lookup"><span data-stu-id="864cc-115">Size</span></span>              | <span data-ttu-id="864cc-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="864cc-116">8 bytes</span></span>                              |
| <span data-ttu-id="864cc-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="864cc-117">Update Privilege</span></span>  | <span data-ttu-id="864cc-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="864cc-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="864cc-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="864cc-119">Update Frequency</span></span>  | <span data-ttu-id="864cc-120">При создании объекта.</span><span class="sxs-lookup"><span data-stu-id="864cc-120">When the object is created.</span></span>          |
| <span data-ttu-id="864cc-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-121">Attribute-Id</span></span>      | <span data-ttu-id="864cc-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="864cc-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="864cc-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="864cc-123">System-Id-Guid</span></span>    | <span data-ttu-id="864cc-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="864cc-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="864cc-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="864cc-125">Syntax</span></span>            | [<span data-ttu-id="864cc-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="864cc-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="864cc-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="864cc-127">Implementations</span></span>

-   [<span data-ttu-id="864cc-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="864cc-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="864cc-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="864cc-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="864cc-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="864cc-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="864cc-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="864cc-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="864cc-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="864cc-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="864cc-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="864cc-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="864cc-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="864cc-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="864cc-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="864cc-135">Windows 2000 Server</span></span>



| <span data-ttu-id="864cc-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-136">Entry</span></span> | <span data-ttu-id="864cc-137">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-139">MAPI-Id</span></span>                | <span data-ttu-id="864cc-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-140">0x8154</span></span>                          |
| <span data-ttu-id="864cc-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-141">System-Only</span></span>            | <span data-ttu-id="864cc-142">True</span><span class="sxs-lookup"><span data-stu-id="864cc-142">True</span></span>                            |
| <span data-ttu-id="864cc-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-143">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-144">True</span><span class="sxs-lookup"><span data-stu-id="864cc-144">True</span></span>                            |
| <span data-ttu-id="864cc-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-145">Is Indexed</span></span>             | <span data-ttu-id="864cc-146">True</span><span class="sxs-lookup"><span data-stu-id="864cc-146">True</span></span>                            |
| <span data-ttu-id="864cc-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-147">In Global Catalog</span></span>      | <span data-ttu-id="864cc-148">True</span><span class="sxs-lookup"><span data-stu-id="864cc-148">True</span></span>                            |
| <span data-ttu-id="864cc-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-153">Search-Flags</span></span>           | <span data-ttu-id="864cc-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-154">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-155">System-Flags</span></span>           | <span data-ttu-id="864cc-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-156">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-157">Classes used in</span></span>        | [<span data-ttu-id="864cc-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="864cc-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="864cc-159">Windows Server 2003</span></span>



| <span data-ttu-id="864cc-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-160">Entry</span></span> | <span data-ttu-id="864cc-161">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-163">MAPI-Id</span></span>                | <span data-ttu-id="864cc-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-164">0x8154</span></span>                          |
| <span data-ttu-id="864cc-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-165">System-Only</span></span>            | <span data-ttu-id="864cc-166">True</span><span class="sxs-lookup"><span data-stu-id="864cc-166">True</span></span>                            |
| <span data-ttu-id="864cc-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-167">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-168">True</span><span class="sxs-lookup"><span data-stu-id="864cc-168">True</span></span>                            |
| <span data-ttu-id="864cc-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-169">Is Indexed</span></span>             | <span data-ttu-id="864cc-170">True</span><span class="sxs-lookup"><span data-stu-id="864cc-170">True</span></span>                            |
| <span data-ttu-id="864cc-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-171">In Global Catalog</span></span>      | <span data-ttu-id="864cc-172">True</span><span class="sxs-lookup"><span data-stu-id="864cc-172">True</span></span>                            |
| <span data-ttu-id="864cc-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-177">Search-Flags</span></span>           | <span data-ttu-id="864cc-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-178">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-179">System-Flags</span></span>           | <span data-ttu-id="864cc-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-180">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-181">Classes used in</span></span>        | [<span data-ttu-id="864cc-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="864cc-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="864cc-183">ADAM</span></span>



| <span data-ttu-id="864cc-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-184">Entry</span></span> | <span data-ttu-id="864cc-185">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-187">MAPI-Id</span></span>                | <span data-ttu-id="864cc-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-188">0x8154</span></span>                          |
| <span data-ttu-id="864cc-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-189">System-Only</span></span>            | <span data-ttu-id="864cc-190">True</span><span class="sxs-lookup"><span data-stu-id="864cc-190">True</span></span>                            |
| <span data-ttu-id="864cc-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-191">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-192">True</span><span class="sxs-lookup"><span data-stu-id="864cc-192">True</span></span>                            |
| <span data-ttu-id="864cc-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-193">Is Indexed</span></span>             | <span data-ttu-id="864cc-194">True</span><span class="sxs-lookup"><span data-stu-id="864cc-194">True</span></span>                            |
| <span data-ttu-id="864cc-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-195">In Global Catalog</span></span>      | <span data-ttu-id="864cc-196">True</span><span class="sxs-lookup"><span data-stu-id="864cc-196">True</span></span>                            |
| <span data-ttu-id="864cc-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-201">Search-Flags</span></span>           | <span data-ttu-id="864cc-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-202">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-203">System-Flags</span></span>           | <span data-ttu-id="864cc-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-204">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-205">Classes used in</span></span>        | [<span data-ttu-id="864cc-206">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="864cc-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="864cc-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="864cc-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-208">Entry</span></span> | <span data-ttu-id="864cc-209">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-211">MAPI-Id</span></span>                | <span data-ttu-id="864cc-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-212">0x8154</span></span>                          |
| <span data-ttu-id="864cc-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-213">System-Only</span></span>            | <span data-ttu-id="864cc-214">True</span><span class="sxs-lookup"><span data-stu-id="864cc-214">True</span></span>                            |
| <span data-ttu-id="864cc-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-215">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-216">True</span><span class="sxs-lookup"><span data-stu-id="864cc-216">True</span></span>                            |
| <span data-ttu-id="864cc-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-217">Is Indexed</span></span>             | <span data-ttu-id="864cc-218">True</span><span class="sxs-lookup"><span data-stu-id="864cc-218">True</span></span>                            |
| <span data-ttu-id="864cc-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-219">In Global Catalog</span></span>      | <span data-ttu-id="864cc-220">True</span><span class="sxs-lookup"><span data-stu-id="864cc-220">True</span></span>                            |
| <span data-ttu-id="864cc-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-225">Search-Flags</span></span>           | <span data-ttu-id="864cc-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-226">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-227">System-Flags</span></span>           | <span data-ttu-id="864cc-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-228">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-229">Classes used in</span></span>        | [<span data-ttu-id="864cc-230">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="864cc-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="864cc-231">Windows Server 2008</span></span>



| <span data-ttu-id="864cc-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-232">Entry</span></span> | <span data-ttu-id="864cc-233">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-235">MAPI-Id</span></span>                | <span data-ttu-id="864cc-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-236">0x8154</span></span>                          |
| <span data-ttu-id="864cc-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-237">System-Only</span></span>            | <span data-ttu-id="864cc-238">True</span><span class="sxs-lookup"><span data-stu-id="864cc-238">True</span></span>                            |
| <span data-ttu-id="864cc-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-239">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-240">True</span><span class="sxs-lookup"><span data-stu-id="864cc-240">True</span></span>                            |
| <span data-ttu-id="864cc-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-241">Is Indexed</span></span>             | <span data-ttu-id="864cc-242">True</span><span class="sxs-lookup"><span data-stu-id="864cc-242">True</span></span>                            |
| <span data-ttu-id="864cc-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-243">In Global Catalog</span></span>      | <span data-ttu-id="864cc-244">True</span><span class="sxs-lookup"><span data-stu-id="864cc-244">True</span></span>                            |
| <span data-ttu-id="864cc-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-249">Search-Flags</span></span>           | <span data-ttu-id="864cc-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-250">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-251">System-Flags</span></span>           | <span data-ttu-id="864cc-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-252">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-253">Classes used in</span></span>        | [<span data-ttu-id="864cc-254">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="864cc-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="864cc-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="864cc-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-256">Entry</span></span> | <span data-ttu-id="864cc-257">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-259">MAPI-Id</span></span>                | <span data-ttu-id="864cc-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-260">0x8154</span></span>                          |
| <span data-ttu-id="864cc-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-261">System-Only</span></span>            | <span data-ttu-id="864cc-262">True</span><span class="sxs-lookup"><span data-stu-id="864cc-262">True</span></span>                            |
| <span data-ttu-id="864cc-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-263">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-264">True</span><span class="sxs-lookup"><span data-stu-id="864cc-264">True</span></span>                            |
| <span data-ttu-id="864cc-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-265">Is Indexed</span></span>             | <span data-ttu-id="864cc-266">True</span><span class="sxs-lookup"><span data-stu-id="864cc-266">True</span></span>                            |
| <span data-ttu-id="864cc-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-267">In Global Catalog</span></span>      | <span data-ttu-id="864cc-268">True</span><span class="sxs-lookup"><span data-stu-id="864cc-268">True</span></span>                            |
| <span data-ttu-id="864cc-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-273">Search-Flags</span></span>           | <span data-ttu-id="864cc-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-274">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-275">System-Flags</span></span>           | <span data-ttu-id="864cc-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-276">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-277">Classes used in</span></span>        | [<span data-ttu-id="864cc-278">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="864cc-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="864cc-279">Windows Server 2012</span></span>



| <span data-ttu-id="864cc-280">Ввод</span><span class="sxs-lookup"><span data-stu-id="864cc-280">Entry</span></span> | <span data-ttu-id="864cc-281">Значение</span><span class="sxs-lookup"><span data-stu-id="864cc-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="864cc-282">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="864cc-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="864cc-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="864cc-283">MAPI-Id</span></span>                | <span data-ttu-id="864cc-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="864cc-284">0x8154</span></span>                          |
| <span data-ttu-id="864cc-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="864cc-285">System-Only</span></span>            | <span data-ttu-id="864cc-286">True</span><span class="sxs-lookup"><span data-stu-id="864cc-286">True</span></span>                            |
| <span data-ttu-id="864cc-287">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="864cc-287">Is-Single-Valued</span></span>       | <span data-ttu-id="864cc-288">True</span><span class="sxs-lookup"><span data-stu-id="864cc-288">True</span></span>                            |
| <span data-ttu-id="864cc-289">Индексируется</span><span class="sxs-lookup"><span data-stu-id="864cc-289">Is Indexed</span></span>             | <span data-ttu-id="864cc-290">True</span><span class="sxs-lookup"><span data-stu-id="864cc-290">True</span></span>                            |
| <span data-ttu-id="864cc-291">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="864cc-291">In Global Catalog</span></span>      | <span data-ttu-id="864cc-292">True</span><span class="sxs-lookup"><span data-stu-id="864cc-292">True</span></span>                            |
| <span data-ttu-id="864cc-293">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="864cc-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="864cc-294">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="864cc-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="864cc-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="864cc-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="864cc-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="864cc-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="864cc-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-297">Search-Flags</span></span>           | <span data-ttu-id="864cc-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="864cc-298">0x00000009</span></span>                      |
| <span data-ttu-id="864cc-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="864cc-299">System-Flags</span></span>           | <span data-ttu-id="864cc-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="864cc-300">0x00000013</span></span>                      |
| <span data-ttu-id="864cc-301">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="864cc-301">Classes used in</span></span>        | [<span data-ttu-id="864cc-302">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="864cc-302">**Top**</span></span>](c-top.md)<br/> |



 

 





