---
title: Атрибут When-Created
description: Дата создания этого объекта. Это значение реплицируется и находится в глобальном каталоге.
ms.assetid: d66084f0-5a82-4a8c-86ee-7e41887d9b90
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута When-Created
- Схема AD атрибута Вхенкреатед
topic_type:
- apiref
api_name:
- When-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634918e29a4c8ef9c62d2b8949d253c80fe17d67
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138735"
---
# <a name="when-created-attribute"></a><span data-ttu-id="21b0a-106">Атрибут When-Created</span><span class="sxs-lookup"><span data-stu-id="21b0a-106">When-Created attribute</span></span>

<span data-ttu-id="21b0a-107">Дата создания этого объекта.</span><span class="sxs-lookup"><span data-stu-id="21b0a-107">The date when this object was created.</span></span> <span data-ttu-id="21b0a-108">Это значение реплицируется и находится в глобальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="21b0a-108">This value is replicated and is in the global catalog.</span></span>



| <span data-ttu-id="21b0a-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-109">Entry</span></span> | <span data-ttu-id="21b0a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="21b0a-111">CN</span><span class="sxs-lookup"><span data-stu-id="21b0a-111">CN</span></span>                | <span data-ttu-id="21b0a-112">When-Created</span><span class="sxs-lookup"><span data-stu-id="21b0a-112">When-Created</span></span>                                                  |
| <span data-ttu-id="21b0a-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="21b0a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="21b0a-114">whenCreated</span><span class="sxs-lookup"><span data-stu-id="21b0a-114">whenCreated</span></span>                                                   |
| <span data-ttu-id="21b0a-115">Размер</span><span class="sxs-lookup"><span data-stu-id="21b0a-115">Size</span></span>              | <span data-ttu-id="21b0a-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="21b0a-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="21b0a-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="21b0a-117">Update Privilege</span></span>  | <span data-ttu-id="21b0a-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="21b0a-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="21b0a-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="21b0a-119">Update Frequency</span></span>  | <span data-ttu-id="21b0a-120">При создании объекта.</span><span class="sxs-lookup"><span data-stu-id="21b0a-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="21b0a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-121">Attribute-Id</span></span>      | <span data-ttu-id="21b0a-122">1.2.840.113556.1.2.2</span><span class="sxs-lookup"><span data-stu-id="21b0a-122">1.2.840.113556.1.2.2</span></span>                                          |
| <span data-ttu-id="21b0a-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="21b0a-123">System-Id-Guid</span></span>    | <span data-ttu-id="21b0a-124">bf967a78-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="21b0a-124">bf967a78-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="21b0a-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21b0a-125">Syntax</span></span>            | [<span data-ttu-id="21b0a-126">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="21b0a-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="21b0a-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="21b0a-127">Implementations</span></span>

-   [<span data-ttu-id="21b0a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21b0a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21b0a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21b0a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21b0a-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="21b0a-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="21b0a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21b0a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21b0a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21b0a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21b0a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21b0a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21b0a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21b0a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21b0a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21b0a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="21b0a-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-136">Entry</span></span> | <span data-ttu-id="21b0a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-139">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-140">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-140">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-141">System-Only</span></span>            | <span data-ttu-id="21b0a-142">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-142">True</span></span>                            |
| <span data-ttu-id="21b0a-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-143">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-144">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-144">True</span></span>                            |
| <span data-ttu-id="21b0a-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-145">Is Indexed</span></span>             | <span data-ttu-id="21b0a-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-146">False</span></span>                           |
| <span data-ttu-id="21b0a-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-147">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-148">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-148">True</span></span>                            |
| <span data-ttu-id="21b0a-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-153">Search-Flags</span></span>           | <span data-ttu-id="21b0a-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-154">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-155">System-Flags</span></span>           | <span data-ttu-id="21b0a-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b0a-156">0x00000010</span></span>                      |
| <span data-ttu-id="21b0a-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-157">Classes used in</span></span>        | [<span data-ttu-id="21b0a-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21b0a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21b0a-159">Windows Server 2003</span></span>



| <span data-ttu-id="21b0a-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-160">Entry</span></span> | <span data-ttu-id="21b0a-161">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-163">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-164">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-164">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-165">System-Only</span></span>            | <span data-ttu-id="21b0a-166">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-166">True</span></span>                            |
| <span data-ttu-id="21b0a-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-167">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-168">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-168">True</span></span>                            |
| <span data-ttu-id="21b0a-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-169">Is Indexed</span></span>             | <span data-ttu-id="21b0a-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-170">False</span></span>                           |
| <span data-ttu-id="21b0a-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-171">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-172">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-172">True</span></span>                            |
| <span data-ttu-id="21b0a-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-177">Search-Flags</span></span>           | <span data-ttu-id="21b0a-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-178">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-179">System-Flags</span></span>           | <span data-ttu-id="21b0a-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="21b0a-180">0x00000012</span></span>                      |
| <span data-ttu-id="21b0a-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-181">Classes used in</span></span>        | [<span data-ttu-id="21b0a-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="21b0a-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="21b0a-183">ADAM</span></span>



| <span data-ttu-id="21b0a-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-184">Entry</span></span> | <span data-ttu-id="21b0a-185">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-187">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-188">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-188">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-189">System-Only</span></span>            | <span data-ttu-id="21b0a-190">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-190">True</span></span>                            |
| <span data-ttu-id="21b0a-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-191">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-192">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-192">True</span></span>                            |
| <span data-ttu-id="21b0a-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-193">Is Indexed</span></span>             | <span data-ttu-id="21b0a-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-194">False</span></span>                           |
| <span data-ttu-id="21b0a-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-195">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-196">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-196">True</span></span>                            |
| <span data-ttu-id="21b0a-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-201">Search-Flags</span></span>           | <span data-ttu-id="21b0a-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-202">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-203">System-Flags</span></span>           | <span data-ttu-id="21b0a-204">0x00000012</span><span class="sxs-lookup"><span data-stu-id="21b0a-204">0x00000012</span></span>                      |
| <span data-ttu-id="21b0a-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-205">Classes used in</span></span>        | [<span data-ttu-id="21b0a-206">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21b0a-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21b0a-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21b0a-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-208">Entry</span></span> | <span data-ttu-id="21b0a-209">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-211">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-212">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-212">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-213">System-Only</span></span>            | <span data-ttu-id="21b0a-214">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-214">True</span></span>                            |
| <span data-ttu-id="21b0a-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-215">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-216">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-216">True</span></span>                            |
| <span data-ttu-id="21b0a-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-217">Is Indexed</span></span>             | <span data-ttu-id="21b0a-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-218">False</span></span>                           |
| <span data-ttu-id="21b0a-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-219">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-220">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-220">True</span></span>                            |
| <span data-ttu-id="21b0a-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-225">Search-Flags</span></span>           | <span data-ttu-id="21b0a-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-226">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-227">System-Flags</span></span>           | <span data-ttu-id="21b0a-228">0x00000012</span><span class="sxs-lookup"><span data-stu-id="21b0a-228">0x00000012</span></span>                      |
| <span data-ttu-id="21b0a-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-229">Classes used in</span></span>        | [<span data-ttu-id="21b0a-230">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21b0a-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21b0a-231">Windows Server 2008</span></span>



| <span data-ttu-id="21b0a-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-232">Entry</span></span> | <span data-ttu-id="21b0a-233">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-235">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-236">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-236">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-237">System-Only</span></span>            | <span data-ttu-id="21b0a-238">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-238">True</span></span>                            |
| <span data-ttu-id="21b0a-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-239">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-240">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-240">True</span></span>                            |
| <span data-ttu-id="21b0a-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-241">Is Indexed</span></span>             | <span data-ttu-id="21b0a-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-242">False</span></span>                           |
| <span data-ttu-id="21b0a-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-243">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-244">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-244">True</span></span>                            |
| <span data-ttu-id="21b0a-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-249">Search-Flags</span></span>           | <span data-ttu-id="21b0a-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-250">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-251">System-Flags</span></span>           | <span data-ttu-id="21b0a-252">0x00000012</span><span class="sxs-lookup"><span data-stu-id="21b0a-252">0x00000012</span></span>                      |
| <span data-ttu-id="21b0a-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-253">Classes used in</span></span>        | [<span data-ttu-id="21b0a-254">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21b0a-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21b0a-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21b0a-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-256">Entry</span></span> | <span data-ttu-id="21b0a-257">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-259">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-260">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-260">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-261">System-Only</span></span>            | <span data-ttu-id="21b0a-262">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-262">True</span></span>                            |
| <span data-ttu-id="21b0a-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-263">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-264">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-264">True</span></span>                            |
| <span data-ttu-id="21b0a-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-265">Is Indexed</span></span>             | <span data-ttu-id="21b0a-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-266">False</span></span>                           |
| <span data-ttu-id="21b0a-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-267">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-268">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-268">True</span></span>                            |
| <span data-ttu-id="21b0a-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-273">Search-Flags</span></span>           | <span data-ttu-id="21b0a-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-274">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-275">System-Flags</span></span>           | <span data-ttu-id="21b0a-276">0x00000012</span><span class="sxs-lookup"><span data-stu-id="21b0a-276">0x00000012</span></span>                      |
| <span data-ttu-id="21b0a-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-277">Classes used in</span></span>        | [<span data-ttu-id="21b0a-278">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21b0a-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21b0a-279">Windows Server 2012</span></span>



| <span data-ttu-id="21b0a-280">Ввод</span><span class="sxs-lookup"><span data-stu-id="21b0a-280">Entry</span></span> | <span data-ttu-id="21b0a-281">Значение</span><span class="sxs-lookup"><span data-stu-id="21b0a-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21b0a-282">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21b0a-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21b0a-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b0a-283">MAPI-Id</span></span>                | <span data-ttu-id="21b0a-284">0x3007</span><span class="sxs-lookup"><span data-stu-id="21b0a-284">0x3007</span></span>                          |
| <span data-ttu-id="21b0a-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b0a-285">System-Only</span></span>            | <span data-ttu-id="21b0a-286">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-286">True</span></span>                            |
| <span data-ttu-id="21b0a-287">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21b0a-287">Is-Single-Valued</span></span>       | <span data-ttu-id="21b0a-288">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-288">True</span></span>                            |
| <span data-ttu-id="21b0a-289">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21b0a-289">Is Indexed</span></span>             | <span data-ttu-id="21b0a-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="21b0a-290">False</span></span>                           |
| <span data-ttu-id="21b0a-291">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21b0a-291">In Global Catalog</span></span>      | <span data-ttu-id="21b0a-292">True</span><span class="sxs-lookup"><span data-stu-id="21b0a-292">True</span></span>                            |
| <span data-ttu-id="21b0a-293">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21b0a-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b0a-294">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21b0a-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21b0a-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b0a-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21b0a-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b0a-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21b0a-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-297">Search-Flags</span></span>           | <span data-ttu-id="21b0a-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b0a-298">0x00000000</span></span>                      |
| <span data-ttu-id="21b0a-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b0a-299">System-Flags</span></span>           | <span data-ttu-id="21b0a-300">0x00000012</span><span class="sxs-lookup"><span data-stu-id="21b0a-300">0x00000012</span></span>                      |
| <span data-ttu-id="21b0a-301">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21b0a-301">Classes used in</span></span>        | [<span data-ttu-id="21b0a-302">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="21b0a-302">**Top**</span></span>](c-top.md)<br/> |



 

 





