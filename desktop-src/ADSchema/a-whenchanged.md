---
title: Атрибут When-Changed
description: Дата последнего изменения этого объекта. Это значение не реплицируется и существует в глобальном каталоге.
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута When-Changed
- Схема AD атрибута whenChanged
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103892890"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="211a6-106">Атрибут When-Changed</span><span class="sxs-lookup"><span data-stu-id="211a6-106">When-Changed attribute</span></span>

<span data-ttu-id="211a6-107">Дата последнего изменения этого объекта.</span><span class="sxs-lookup"><span data-stu-id="211a6-107">The date when this object was last changed.</span></span> <span data-ttu-id="211a6-108">Это значение не реплицируется и существует в глобальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="211a6-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="211a6-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-109">Entry</span></span> | <span data-ttu-id="211a6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="211a6-111">CN</span><span class="sxs-lookup"><span data-stu-id="211a6-111">CN</span></span>                | <span data-ttu-id="211a6-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="211a6-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="211a6-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="211a6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="211a6-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="211a6-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="211a6-115">Размер</span><span class="sxs-lookup"><span data-stu-id="211a6-115">Size</span></span>              | <span data-ttu-id="211a6-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="211a6-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="211a6-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="211a6-117">Update Privilege</span></span>  | <span data-ttu-id="211a6-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="211a6-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="211a6-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="211a6-119">Update Frequency</span></span>  | <span data-ttu-id="211a6-120">При каждом изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="211a6-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="211a6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-121">Attribute-Id</span></span>      | <span data-ttu-id="211a6-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="211a6-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="211a6-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="211a6-123">System-Id-Guid</span></span>    | <span data-ttu-id="211a6-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="211a6-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="211a6-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="211a6-125">Syntax</span></span>            | [<span data-ttu-id="211a6-126">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="211a6-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="211a6-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="211a6-127">Implementations</span></span>

-   [<span data-ttu-id="211a6-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="211a6-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="211a6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="211a6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="211a6-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="211a6-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="211a6-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="211a6-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="211a6-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="211a6-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="211a6-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="211a6-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="211a6-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="211a6-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="211a6-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="211a6-135">Windows 2000 Server</span></span>



| <span data-ttu-id="211a6-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-136">Entry</span></span> | <span data-ttu-id="211a6-137">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-139">MAPI-Id</span></span>                | <span data-ttu-id="211a6-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-140">0x3008</span></span>                          |
| <span data-ttu-id="211a6-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-141">System-Only</span></span>            | <span data-ttu-id="211a6-142">True</span><span class="sxs-lookup"><span data-stu-id="211a6-142">True</span></span>                            |
| <span data-ttu-id="211a6-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-143">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-144">True</span><span class="sxs-lookup"><span data-stu-id="211a6-144">True</span></span>                            |
| <span data-ttu-id="211a6-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-145">Is Indexed</span></span>             | <span data-ttu-id="211a6-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-146">False</span></span>                           |
| <span data-ttu-id="211a6-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-147">In Global Catalog</span></span>      | <span data-ttu-id="211a6-148">True</span><span class="sxs-lookup"><span data-stu-id="211a6-148">True</span></span>                            |
| <span data-ttu-id="211a6-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-153">Search-Flags</span></span>           | <span data-ttu-id="211a6-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-154">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-155">System-Flags</span></span>           | <span data-ttu-id="211a6-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-156">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-157">Classes used in</span></span>        | [<span data-ttu-id="211a6-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="211a6-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="211a6-159">Windows Server 2003</span></span>



| <span data-ttu-id="211a6-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-160">Entry</span></span> | <span data-ttu-id="211a6-161">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-163">MAPI-Id</span></span>                | <span data-ttu-id="211a6-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-164">0x3008</span></span>                          |
| <span data-ttu-id="211a6-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-165">System-Only</span></span>            | <span data-ttu-id="211a6-166">True</span><span class="sxs-lookup"><span data-stu-id="211a6-166">True</span></span>                            |
| <span data-ttu-id="211a6-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-167">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-168">True</span><span class="sxs-lookup"><span data-stu-id="211a6-168">True</span></span>                            |
| <span data-ttu-id="211a6-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-169">Is Indexed</span></span>             | <span data-ttu-id="211a6-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-170">False</span></span>                           |
| <span data-ttu-id="211a6-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-171">In Global Catalog</span></span>      | <span data-ttu-id="211a6-172">True</span><span class="sxs-lookup"><span data-stu-id="211a6-172">True</span></span>                            |
| <span data-ttu-id="211a6-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-177">Search-Flags</span></span>           | <span data-ttu-id="211a6-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-178">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-179">System-Flags</span></span>           | <span data-ttu-id="211a6-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-180">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-181">Classes used in</span></span>        | [<span data-ttu-id="211a6-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="211a6-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="211a6-183">ADAM</span></span>



| <span data-ttu-id="211a6-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-184">Entry</span></span> | <span data-ttu-id="211a6-185">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-187">MAPI-Id</span></span>                | <span data-ttu-id="211a6-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-188">0x3008</span></span>                          |
| <span data-ttu-id="211a6-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-189">System-Only</span></span>            | <span data-ttu-id="211a6-190">True</span><span class="sxs-lookup"><span data-stu-id="211a6-190">True</span></span>                            |
| <span data-ttu-id="211a6-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-191">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-192">True</span><span class="sxs-lookup"><span data-stu-id="211a6-192">True</span></span>                            |
| <span data-ttu-id="211a6-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-193">Is Indexed</span></span>             | <span data-ttu-id="211a6-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-194">False</span></span>                           |
| <span data-ttu-id="211a6-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-195">In Global Catalog</span></span>      | <span data-ttu-id="211a6-196">True</span><span class="sxs-lookup"><span data-stu-id="211a6-196">True</span></span>                            |
| <span data-ttu-id="211a6-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-201">Search-Flags</span></span>           | <span data-ttu-id="211a6-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-202">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-203">System-Flags</span></span>           | <span data-ttu-id="211a6-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-204">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-205">Classes used in</span></span>        | [<span data-ttu-id="211a6-206">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="211a6-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="211a6-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="211a6-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-208">Entry</span></span> | <span data-ttu-id="211a6-209">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-211">MAPI-Id</span></span>                | <span data-ttu-id="211a6-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-212">0x3008</span></span>                          |
| <span data-ttu-id="211a6-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-213">System-Only</span></span>            | <span data-ttu-id="211a6-214">True</span><span class="sxs-lookup"><span data-stu-id="211a6-214">True</span></span>                            |
| <span data-ttu-id="211a6-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-215">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-216">True</span><span class="sxs-lookup"><span data-stu-id="211a6-216">True</span></span>                            |
| <span data-ttu-id="211a6-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-217">Is Indexed</span></span>             | <span data-ttu-id="211a6-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-218">False</span></span>                           |
| <span data-ttu-id="211a6-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-219">In Global Catalog</span></span>      | <span data-ttu-id="211a6-220">True</span><span class="sxs-lookup"><span data-stu-id="211a6-220">True</span></span>                            |
| <span data-ttu-id="211a6-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-225">Search-Flags</span></span>           | <span data-ttu-id="211a6-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-226">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-227">System-Flags</span></span>           | <span data-ttu-id="211a6-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-228">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-229">Classes used in</span></span>        | [<span data-ttu-id="211a6-230">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="211a6-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="211a6-231">Windows Server 2008</span></span>



| <span data-ttu-id="211a6-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-232">Entry</span></span> | <span data-ttu-id="211a6-233">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-235">MAPI-Id</span></span>                | <span data-ttu-id="211a6-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-236">0x3008</span></span>                          |
| <span data-ttu-id="211a6-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-237">System-Only</span></span>            | <span data-ttu-id="211a6-238">True</span><span class="sxs-lookup"><span data-stu-id="211a6-238">True</span></span>                            |
| <span data-ttu-id="211a6-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-239">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-240">True</span><span class="sxs-lookup"><span data-stu-id="211a6-240">True</span></span>                            |
| <span data-ttu-id="211a6-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-241">Is Indexed</span></span>             | <span data-ttu-id="211a6-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-242">False</span></span>                           |
| <span data-ttu-id="211a6-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-243">In Global Catalog</span></span>      | <span data-ttu-id="211a6-244">True</span><span class="sxs-lookup"><span data-stu-id="211a6-244">True</span></span>                            |
| <span data-ttu-id="211a6-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-249">Search-Flags</span></span>           | <span data-ttu-id="211a6-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-250">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-251">System-Flags</span></span>           | <span data-ttu-id="211a6-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-252">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-253">Classes used in</span></span>        | [<span data-ttu-id="211a6-254">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="211a6-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="211a6-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="211a6-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-256">Entry</span></span> | <span data-ttu-id="211a6-257">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-259">MAPI-Id</span></span>                | <span data-ttu-id="211a6-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-260">0x3008</span></span>                          |
| <span data-ttu-id="211a6-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-261">System-Only</span></span>            | <span data-ttu-id="211a6-262">True</span><span class="sxs-lookup"><span data-stu-id="211a6-262">True</span></span>                            |
| <span data-ttu-id="211a6-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-263">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-264">True</span><span class="sxs-lookup"><span data-stu-id="211a6-264">True</span></span>                            |
| <span data-ttu-id="211a6-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-265">Is Indexed</span></span>             | <span data-ttu-id="211a6-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-266">False</span></span>                           |
| <span data-ttu-id="211a6-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-267">In Global Catalog</span></span>      | <span data-ttu-id="211a6-268">True</span><span class="sxs-lookup"><span data-stu-id="211a6-268">True</span></span>                            |
| <span data-ttu-id="211a6-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-273">Search-Flags</span></span>           | <span data-ttu-id="211a6-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-274">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-275">System-Flags</span></span>           | <span data-ttu-id="211a6-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-276">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-277">Classes used in</span></span>        | [<span data-ttu-id="211a6-278">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="211a6-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="211a6-279">Windows Server 2012</span></span>



| <span data-ttu-id="211a6-280">Ввод</span><span class="sxs-lookup"><span data-stu-id="211a6-280">Entry</span></span> | <span data-ttu-id="211a6-281">Значение</span><span class="sxs-lookup"><span data-stu-id="211a6-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="211a6-282">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="211a6-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="211a6-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="211a6-283">MAPI-Id</span></span>                | <span data-ttu-id="211a6-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="211a6-284">0x3008</span></span>                          |
| <span data-ttu-id="211a6-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="211a6-285">System-Only</span></span>            | <span data-ttu-id="211a6-286">True</span><span class="sxs-lookup"><span data-stu-id="211a6-286">True</span></span>                            |
| <span data-ttu-id="211a6-287">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="211a6-287">Is-Single-Valued</span></span>       | <span data-ttu-id="211a6-288">True</span><span class="sxs-lookup"><span data-stu-id="211a6-288">True</span></span>                            |
| <span data-ttu-id="211a6-289">Индексируется</span><span class="sxs-lookup"><span data-stu-id="211a6-289">Is Indexed</span></span>             | <span data-ttu-id="211a6-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="211a6-290">False</span></span>                           |
| <span data-ttu-id="211a6-291">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="211a6-291">In Global Catalog</span></span>      | <span data-ttu-id="211a6-292">True</span><span class="sxs-lookup"><span data-stu-id="211a6-292">True</span></span>                            |
| <span data-ttu-id="211a6-293">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="211a6-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="211a6-294">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="211a6-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="211a6-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="211a6-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="211a6-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="211a6-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="211a6-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-297">Search-Flags</span></span>           | <span data-ttu-id="211a6-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="211a6-298">0x00000000</span></span>                      |
| <span data-ttu-id="211a6-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="211a6-299">System-Flags</span></span>           | <span data-ttu-id="211a6-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="211a6-300">0x00000013</span></span>                      |
| <span data-ttu-id="211a6-301">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="211a6-301">Classes used in</span></span>        | [<span data-ttu-id="211a6-302">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="211a6-302">**Top**</span></span>](c-top.md)<br/> |



 

 





