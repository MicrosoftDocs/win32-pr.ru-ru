---
title: Атрибут DSA-Signature
description: DSA-Signature объекта — это идентификатор вызова последнего каталога для изменения объекта.
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DSA-Signature
- Схема AD атрибута Дсасигнатуре
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654863"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="61a67-105">Атрибут DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="61a67-105">DSA-Signature attribute</span></span>

<span data-ttu-id="61a67-106">DSA-Signature объекта — это идентификатор вызова последнего каталога для изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="61a67-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="61a67-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-107">Entry</span></span> | <span data-ttu-id="61a67-108">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="61a67-109">CN</span><span class="sxs-lookup"><span data-stu-id="61a67-109">CN</span></span>                | <span data-ttu-id="61a67-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="61a67-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="61a67-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="61a67-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61a67-112">дсасигнатуре</span><span class="sxs-lookup"><span data-stu-id="61a67-112">dSASignature</span></span>                                          |
| <span data-ttu-id="61a67-113">Размер</span><span class="sxs-lookup"><span data-stu-id="61a67-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="61a67-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="61a67-114">Update Privilege</span></span>  | <span data-ttu-id="61a67-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="61a67-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="61a67-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="61a67-116">Update Frequency</span></span>  | <span data-ttu-id="61a67-117">При каждом изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="61a67-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="61a67-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-118">Attribute-Id</span></span>      | <span data-ttu-id="61a67-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="61a67-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="61a67-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="61a67-120">System-Id-Guid</span></span>    | <span data-ttu-id="61a67-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="61a67-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="61a67-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61a67-122">Syntax</span></span>            | [<span data-ttu-id="61a67-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="61a67-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="61a67-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="61a67-124">Implementations</span></span>

-   [<span data-ttu-id="61a67-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="61a67-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="61a67-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61a67-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61a67-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="61a67-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="61a67-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61a67-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61a67-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61a67-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61a67-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61a67-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61a67-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61a67-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="61a67-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61a67-132">Windows 2000 Server</span></span>



| <span data-ttu-id="61a67-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-133">Entry</span></span> | <span data-ttu-id="61a67-134">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-136">MAPI-Id</span></span>                | <span data-ttu-id="61a67-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-137">0x8077</span></span>                          |
| <span data-ttu-id="61a67-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-138">System-Only</span></span>            | <span data-ttu-id="61a67-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-139">False</span></span>                           |
| <span data-ttu-id="61a67-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-140">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-141">True</span><span class="sxs-lookup"><span data-stu-id="61a67-141">True</span></span>                            |
| <span data-ttu-id="61a67-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-142">Is Indexed</span></span>             | <span data-ttu-id="61a67-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-143">False</span></span>                           |
| <span data-ttu-id="61a67-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-144">In Global Catalog</span></span>      | <span data-ttu-id="61a67-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-145">False</span></span>                           |
| <span data-ttu-id="61a67-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-150">Search-Flags</span></span>           | <span data-ttu-id="61a67-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-151">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-152">System-Flags</span></span>           | <span data-ttu-id="61a67-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-153">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-154">Classes used in</span></span>        | [<span data-ttu-id="61a67-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="61a67-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61a67-156">Windows Server 2003</span></span>



| <span data-ttu-id="61a67-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-157">Entry</span></span> | <span data-ttu-id="61a67-158">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-160">MAPI-Id</span></span>                | <span data-ttu-id="61a67-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-161">0x8077</span></span>                          |
| <span data-ttu-id="61a67-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-162">System-Only</span></span>            | <span data-ttu-id="61a67-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-163">False</span></span>                           |
| <span data-ttu-id="61a67-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-164">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-165">True</span><span class="sxs-lookup"><span data-stu-id="61a67-165">True</span></span>                            |
| <span data-ttu-id="61a67-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-166">Is Indexed</span></span>             | <span data-ttu-id="61a67-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-167">False</span></span>                           |
| <span data-ttu-id="61a67-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-168">In Global Catalog</span></span>      | <span data-ttu-id="61a67-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-169">False</span></span>                           |
| <span data-ttu-id="61a67-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-174">Search-Flags</span></span>           | <span data-ttu-id="61a67-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-175">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-176">System-Flags</span></span>           | <span data-ttu-id="61a67-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-177">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-178">Classes used in</span></span>        | [<span data-ttu-id="61a67-179">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="61a67-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="61a67-180">ADAM</span></span>



| <span data-ttu-id="61a67-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-181">Entry</span></span> | <span data-ttu-id="61a67-182">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-184">MAPI-Id</span></span>                | <span data-ttu-id="61a67-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-185">0x8077</span></span>                          |
| <span data-ttu-id="61a67-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-186">System-Only</span></span>            | <span data-ttu-id="61a67-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-187">False</span></span>                           |
| <span data-ttu-id="61a67-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-188">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-189">True</span><span class="sxs-lookup"><span data-stu-id="61a67-189">True</span></span>                            |
| <span data-ttu-id="61a67-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-190">Is Indexed</span></span>             | <span data-ttu-id="61a67-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-191">False</span></span>                           |
| <span data-ttu-id="61a67-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-192">In Global Catalog</span></span>      | <span data-ttu-id="61a67-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-193">False</span></span>                           |
| <span data-ttu-id="61a67-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-198">Search-Flags</span></span>           | <span data-ttu-id="61a67-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-199">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-200">System-Flags</span></span>           | <span data-ttu-id="61a67-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-201">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-202">Classes used in</span></span>        | [<span data-ttu-id="61a67-203">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61a67-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61a67-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61a67-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-205">Entry</span></span> | <span data-ttu-id="61a67-206">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-208">MAPI-Id</span></span>                | <span data-ttu-id="61a67-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-209">0x8077</span></span>                          |
| <span data-ttu-id="61a67-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-210">System-Only</span></span>            | <span data-ttu-id="61a67-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-211">False</span></span>                           |
| <span data-ttu-id="61a67-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-212">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-213">True</span><span class="sxs-lookup"><span data-stu-id="61a67-213">True</span></span>                            |
| <span data-ttu-id="61a67-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-214">Is Indexed</span></span>             | <span data-ttu-id="61a67-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-215">False</span></span>                           |
| <span data-ttu-id="61a67-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-216">In Global Catalog</span></span>      | <span data-ttu-id="61a67-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-217">False</span></span>                           |
| <span data-ttu-id="61a67-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-222">Search-Flags</span></span>           | <span data-ttu-id="61a67-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-223">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-224">System-Flags</span></span>           | <span data-ttu-id="61a67-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-225">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-226">Classes used in</span></span>        | [<span data-ttu-id="61a67-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61a67-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61a67-228">Windows Server 2008</span></span>



| <span data-ttu-id="61a67-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-229">Entry</span></span> | <span data-ttu-id="61a67-230">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-232">MAPI-Id</span></span>                | <span data-ttu-id="61a67-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-233">0x8077</span></span>                          |
| <span data-ttu-id="61a67-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-234">System-Only</span></span>            | <span data-ttu-id="61a67-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-235">False</span></span>                           |
| <span data-ttu-id="61a67-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-236">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-237">True</span><span class="sxs-lookup"><span data-stu-id="61a67-237">True</span></span>                            |
| <span data-ttu-id="61a67-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-238">Is Indexed</span></span>             | <span data-ttu-id="61a67-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-239">False</span></span>                           |
| <span data-ttu-id="61a67-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-240">In Global Catalog</span></span>      | <span data-ttu-id="61a67-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-241">False</span></span>                           |
| <span data-ttu-id="61a67-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-246">Search-Flags</span></span>           | <span data-ttu-id="61a67-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-247">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-248">System-Flags</span></span>           | <span data-ttu-id="61a67-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-249">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-250">Classes used in</span></span>        | [<span data-ttu-id="61a67-251">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61a67-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61a67-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61a67-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-253">Entry</span></span> | <span data-ttu-id="61a67-254">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-256">MAPI-Id</span></span>                | <span data-ttu-id="61a67-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-257">0x8077</span></span>                          |
| <span data-ttu-id="61a67-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-258">System-Only</span></span>            | <span data-ttu-id="61a67-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-259">False</span></span>                           |
| <span data-ttu-id="61a67-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-260">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-261">True</span><span class="sxs-lookup"><span data-stu-id="61a67-261">True</span></span>                            |
| <span data-ttu-id="61a67-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-262">Is Indexed</span></span>             | <span data-ttu-id="61a67-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-263">False</span></span>                           |
| <span data-ttu-id="61a67-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-264">In Global Catalog</span></span>      | <span data-ttu-id="61a67-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-265">False</span></span>                           |
| <span data-ttu-id="61a67-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-270">Search-Flags</span></span>           | <span data-ttu-id="61a67-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-271">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-272">System-Flags</span></span>           | <span data-ttu-id="61a67-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-273">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-274">Classes used in</span></span>        | [<span data-ttu-id="61a67-275">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61a67-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61a67-276">Windows Server 2012</span></span>



| <span data-ttu-id="61a67-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="61a67-277">Entry</span></span> | <span data-ttu-id="61a67-278">Значение</span><span class="sxs-lookup"><span data-stu-id="61a67-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61a67-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61a67-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61a67-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61a67-280">MAPI-Id</span></span>                | <span data-ttu-id="61a67-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="61a67-281">0x8077</span></span>                          |
| <span data-ttu-id="61a67-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="61a67-282">System-Only</span></span>            | <span data-ttu-id="61a67-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-283">False</span></span>                           |
| <span data-ttu-id="61a67-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61a67-284">Is-Single-Valued</span></span>       | <span data-ttu-id="61a67-285">True</span><span class="sxs-lookup"><span data-stu-id="61a67-285">True</span></span>                            |
| <span data-ttu-id="61a67-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61a67-286">Is Indexed</span></span>             | <span data-ttu-id="61a67-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-287">False</span></span>                           |
| <span data-ttu-id="61a67-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61a67-288">In Global Catalog</span></span>      | <span data-ttu-id="61a67-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="61a67-289">False</span></span>                           |
| <span data-ttu-id="61a67-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61a67-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="61a67-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61a67-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61a67-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61a67-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61a67-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61a67-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61a67-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-294">Search-Flags</span></span>           | <span data-ttu-id="61a67-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61a67-295">0x00000000</span></span>                      |
| <span data-ttu-id="61a67-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61a67-296">System-Flags</span></span>           | <span data-ttu-id="61a67-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61a67-297">0x00000010</span></span>                      |
| <span data-ttu-id="61a67-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61a67-298">Classes used in</span></span>        | [<span data-ttu-id="61a67-299">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="61a67-299">**Top**</span></span>](c-top.md)<br/> |



 

 





