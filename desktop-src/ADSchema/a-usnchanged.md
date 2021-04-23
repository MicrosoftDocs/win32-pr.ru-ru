---
title: Атрибут USN-Changed
description: Последовательный номер обновления (USN), назначенный локальным каталогом для последнего изменения, включая создание. См. также созданный USN.
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута USN-Changed
- Схема AD атрибута uSNChanged
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804799"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="678fe-106">Атрибут USN-Changed</span><span class="sxs-lookup"><span data-stu-id="678fe-106">USN-Changed attribute</span></span>

<span data-ttu-id="678fe-107">Последовательный номер обновления (USN), назначенный локальным каталогом для последнего изменения, включая создание.</span><span class="sxs-lookup"><span data-stu-id="678fe-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="678fe-108">См. также [**созданный USN**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="678fe-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="678fe-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-109">Entry</span></span> | <span data-ttu-id="678fe-110">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="678fe-111">CN</span><span class="sxs-lookup"><span data-stu-id="678fe-111">CN</span></span>                | <span data-ttu-id="678fe-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="678fe-112">USN-Changed</span></span>                          |
| <span data-ttu-id="678fe-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="678fe-113">Ldap-Display-Name</span></span> | <span data-ttu-id="678fe-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="678fe-114">uSNChanged</span></span>                           |
| <span data-ttu-id="678fe-115">Размер</span><span class="sxs-lookup"><span data-stu-id="678fe-115">Size</span></span>              | <span data-ttu-id="678fe-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="678fe-116">8 bytes</span></span>                              |
| <span data-ttu-id="678fe-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="678fe-117">Update Privilege</span></span>  | <span data-ttu-id="678fe-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="678fe-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="678fe-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="678fe-119">Update Frequency</span></span>  | <span data-ttu-id="678fe-120">При изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="678fe-120">When the object is changed.</span></span>          |
| <span data-ttu-id="678fe-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-121">Attribute-Id</span></span>      | <span data-ttu-id="678fe-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="678fe-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="678fe-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="678fe-123">System-Id-Guid</span></span>    | <span data-ttu-id="678fe-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="678fe-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="678fe-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="678fe-125">Syntax</span></span>            | [<span data-ttu-id="678fe-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="678fe-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="678fe-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="678fe-127">Implementations</span></span>

-   [<span data-ttu-id="678fe-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="678fe-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="678fe-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="678fe-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="678fe-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="678fe-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="678fe-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="678fe-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="678fe-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="678fe-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="678fe-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="678fe-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="678fe-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="678fe-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="678fe-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="678fe-135">Windows 2000 Server</span></span>



| <span data-ttu-id="678fe-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-136">Entry</span></span> | <span data-ttu-id="678fe-137">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-139">MAPI-Id</span></span>                | <span data-ttu-id="678fe-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-140">0x8029</span></span>                          |
| <span data-ttu-id="678fe-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-141">System-Only</span></span>            | <span data-ttu-id="678fe-142">True</span><span class="sxs-lookup"><span data-stu-id="678fe-142">True</span></span>                            |
| <span data-ttu-id="678fe-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-143">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-144">True</span><span class="sxs-lookup"><span data-stu-id="678fe-144">True</span></span>                            |
| <span data-ttu-id="678fe-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-145">Is Indexed</span></span>             | <span data-ttu-id="678fe-146">True</span><span class="sxs-lookup"><span data-stu-id="678fe-146">True</span></span>                            |
| <span data-ttu-id="678fe-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-147">In Global Catalog</span></span>      | <span data-ttu-id="678fe-148">True</span><span class="sxs-lookup"><span data-stu-id="678fe-148">True</span></span>                            |
| <span data-ttu-id="678fe-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-153">Search-Flags</span></span>           | <span data-ttu-id="678fe-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-154">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-155">System-Flags</span></span>           | <span data-ttu-id="678fe-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-156">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-157">Classes used in</span></span>        | [<span data-ttu-id="678fe-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="678fe-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="678fe-159">Windows Server 2003</span></span>



| <span data-ttu-id="678fe-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-160">Entry</span></span> | <span data-ttu-id="678fe-161">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-163">MAPI-Id</span></span>                | <span data-ttu-id="678fe-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-164">0x8029</span></span>                          |
| <span data-ttu-id="678fe-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-165">System-Only</span></span>            | <span data-ttu-id="678fe-166">True</span><span class="sxs-lookup"><span data-stu-id="678fe-166">True</span></span>                            |
| <span data-ttu-id="678fe-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-167">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-168">True</span><span class="sxs-lookup"><span data-stu-id="678fe-168">True</span></span>                            |
| <span data-ttu-id="678fe-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-169">Is Indexed</span></span>             | <span data-ttu-id="678fe-170">True</span><span class="sxs-lookup"><span data-stu-id="678fe-170">True</span></span>                            |
| <span data-ttu-id="678fe-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-171">In Global Catalog</span></span>      | <span data-ttu-id="678fe-172">True</span><span class="sxs-lookup"><span data-stu-id="678fe-172">True</span></span>                            |
| <span data-ttu-id="678fe-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-177">Search-Flags</span></span>           | <span data-ttu-id="678fe-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-178">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-179">System-Flags</span></span>           | <span data-ttu-id="678fe-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-180">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-181">Classes used in</span></span>        | [<span data-ttu-id="678fe-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="678fe-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="678fe-183">ADAM</span></span>



| <span data-ttu-id="678fe-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-184">Entry</span></span> | <span data-ttu-id="678fe-185">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-187">MAPI-Id</span></span>                | <span data-ttu-id="678fe-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-188">0x8029</span></span>                          |
| <span data-ttu-id="678fe-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-189">System-Only</span></span>            | <span data-ttu-id="678fe-190">True</span><span class="sxs-lookup"><span data-stu-id="678fe-190">True</span></span>                            |
| <span data-ttu-id="678fe-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-191">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-192">True</span><span class="sxs-lookup"><span data-stu-id="678fe-192">True</span></span>                            |
| <span data-ttu-id="678fe-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-193">Is Indexed</span></span>             | <span data-ttu-id="678fe-194">True</span><span class="sxs-lookup"><span data-stu-id="678fe-194">True</span></span>                            |
| <span data-ttu-id="678fe-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-195">In Global Catalog</span></span>      | <span data-ttu-id="678fe-196">True</span><span class="sxs-lookup"><span data-stu-id="678fe-196">True</span></span>                            |
| <span data-ttu-id="678fe-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-201">Search-Flags</span></span>           | <span data-ttu-id="678fe-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-202">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-203">System-Flags</span></span>           | <span data-ttu-id="678fe-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-204">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-205">Classes used in</span></span>        | [<span data-ttu-id="678fe-206">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="678fe-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="678fe-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="678fe-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-208">Entry</span></span> | <span data-ttu-id="678fe-209">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-211">MAPI-Id</span></span>                | <span data-ttu-id="678fe-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-212">0x8029</span></span>                          |
| <span data-ttu-id="678fe-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-213">System-Only</span></span>            | <span data-ttu-id="678fe-214">True</span><span class="sxs-lookup"><span data-stu-id="678fe-214">True</span></span>                            |
| <span data-ttu-id="678fe-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-215">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-216">True</span><span class="sxs-lookup"><span data-stu-id="678fe-216">True</span></span>                            |
| <span data-ttu-id="678fe-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-217">Is Indexed</span></span>             | <span data-ttu-id="678fe-218">True</span><span class="sxs-lookup"><span data-stu-id="678fe-218">True</span></span>                            |
| <span data-ttu-id="678fe-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-219">In Global Catalog</span></span>      | <span data-ttu-id="678fe-220">True</span><span class="sxs-lookup"><span data-stu-id="678fe-220">True</span></span>                            |
| <span data-ttu-id="678fe-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-225">Search-Flags</span></span>           | <span data-ttu-id="678fe-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-226">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-227">System-Flags</span></span>           | <span data-ttu-id="678fe-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-228">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-229">Classes used in</span></span>        | [<span data-ttu-id="678fe-230">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="678fe-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="678fe-231">Windows Server 2008</span></span>



| <span data-ttu-id="678fe-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-232">Entry</span></span> | <span data-ttu-id="678fe-233">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-235">MAPI-Id</span></span>                | <span data-ttu-id="678fe-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-236">0x8029</span></span>                          |
| <span data-ttu-id="678fe-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-237">System-Only</span></span>            | <span data-ttu-id="678fe-238">True</span><span class="sxs-lookup"><span data-stu-id="678fe-238">True</span></span>                            |
| <span data-ttu-id="678fe-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-239">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-240">True</span><span class="sxs-lookup"><span data-stu-id="678fe-240">True</span></span>                            |
| <span data-ttu-id="678fe-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-241">Is Indexed</span></span>             | <span data-ttu-id="678fe-242">True</span><span class="sxs-lookup"><span data-stu-id="678fe-242">True</span></span>                            |
| <span data-ttu-id="678fe-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-243">In Global Catalog</span></span>      | <span data-ttu-id="678fe-244">True</span><span class="sxs-lookup"><span data-stu-id="678fe-244">True</span></span>                            |
| <span data-ttu-id="678fe-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-249">Search-Flags</span></span>           | <span data-ttu-id="678fe-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-250">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-251">System-Flags</span></span>           | <span data-ttu-id="678fe-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-252">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-253">Classes used in</span></span>        | [<span data-ttu-id="678fe-254">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="678fe-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="678fe-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="678fe-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-256">Entry</span></span> | <span data-ttu-id="678fe-257">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-259">MAPI-Id</span></span>                | <span data-ttu-id="678fe-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-260">0x8029</span></span>                          |
| <span data-ttu-id="678fe-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-261">System-Only</span></span>            | <span data-ttu-id="678fe-262">True</span><span class="sxs-lookup"><span data-stu-id="678fe-262">True</span></span>                            |
| <span data-ttu-id="678fe-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-263">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-264">True</span><span class="sxs-lookup"><span data-stu-id="678fe-264">True</span></span>                            |
| <span data-ttu-id="678fe-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-265">Is Indexed</span></span>             | <span data-ttu-id="678fe-266">True</span><span class="sxs-lookup"><span data-stu-id="678fe-266">True</span></span>                            |
| <span data-ttu-id="678fe-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-267">In Global Catalog</span></span>      | <span data-ttu-id="678fe-268">True</span><span class="sxs-lookup"><span data-stu-id="678fe-268">True</span></span>                            |
| <span data-ttu-id="678fe-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-273">Search-Flags</span></span>           | <span data-ttu-id="678fe-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-274">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-275">System-Flags</span></span>           | <span data-ttu-id="678fe-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-276">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-277">Classes used in</span></span>        | [<span data-ttu-id="678fe-278">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="678fe-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="678fe-279">Windows Server 2012</span></span>



| <span data-ttu-id="678fe-280">Ввод</span><span class="sxs-lookup"><span data-stu-id="678fe-280">Entry</span></span> | <span data-ttu-id="678fe-281">Значение</span><span class="sxs-lookup"><span data-stu-id="678fe-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="678fe-282">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="678fe-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="678fe-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="678fe-283">MAPI-Id</span></span>                | <span data-ttu-id="678fe-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="678fe-284">0x8029</span></span>                          |
| <span data-ttu-id="678fe-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="678fe-285">System-Only</span></span>            | <span data-ttu-id="678fe-286">True</span><span class="sxs-lookup"><span data-stu-id="678fe-286">True</span></span>                            |
| <span data-ttu-id="678fe-287">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="678fe-287">Is-Single-Valued</span></span>       | <span data-ttu-id="678fe-288">True</span><span class="sxs-lookup"><span data-stu-id="678fe-288">True</span></span>                            |
| <span data-ttu-id="678fe-289">Индексируется</span><span class="sxs-lookup"><span data-stu-id="678fe-289">Is Indexed</span></span>             | <span data-ttu-id="678fe-290">True</span><span class="sxs-lookup"><span data-stu-id="678fe-290">True</span></span>                            |
| <span data-ttu-id="678fe-291">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="678fe-291">In Global Catalog</span></span>      | <span data-ttu-id="678fe-292">True</span><span class="sxs-lookup"><span data-stu-id="678fe-292">True</span></span>                            |
| <span data-ttu-id="678fe-293">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="678fe-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="678fe-294">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="678fe-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="678fe-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="678fe-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="678fe-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="678fe-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="678fe-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-297">Search-Flags</span></span>           | <span data-ttu-id="678fe-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="678fe-298">0x00000009</span></span>                      |
| <span data-ttu-id="678fe-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="678fe-299">System-Flags</span></span>           | <span data-ttu-id="678fe-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="678fe-300">0x00000013</span></span>                      |
| <span data-ttu-id="678fe-301">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="678fe-301">Classes used in</span></span>        | [<span data-ttu-id="678fe-302">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="678fe-302">**Top**</span></span>](c-top.md)<br/> |



 

 





