---
title: Атрибут USN-Intersite
description: Порядковый номер обновления (USN) для межсайтовой репликации.
ms.assetid: c4a4640b-2890-46ea-9eb9-8acb9e749499
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута USN-Intersite
- Схема AD атрибута Уснинтерсите
topic_type:
- apiref
api_name:
- USN-Intersite
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d101d854650a689679b95282734865ac19f6ced1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493665"
---
# <a name="usn-intersite-attribute"></a><span data-ttu-id="ce16a-105">Атрибут USN-Intersite</span><span class="sxs-lookup"><span data-stu-id="ce16a-105">USN-Intersite attribute</span></span>

<span data-ttu-id="ce16a-106">Порядковый номер обновления (USN) для межсайтовой репликации.</span><span class="sxs-lookup"><span data-stu-id="ce16a-106">The update sequence number (USN) for inter-site replication.</span></span>



| <span data-ttu-id="ce16a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-107">Entry</span></span> | <span data-ttu-id="ce16a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ce16a-109">CN</span><span class="sxs-lookup"><span data-stu-id="ce16a-109">CN</span></span>                | <span data-ttu-id="ce16a-110">USN-Intersite</span><span class="sxs-lookup"><span data-stu-id="ce16a-110">USN-Intersite</span></span>                        |
| <span data-ttu-id="ce16a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ce16a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ce16a-112">уснинтерсите</span><span class="sxs-lookup"><span data-stu-id="ce16a-112">USNIntersite</span></span>                         |
| <span data-ttu-id="ce16a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ce16a-113">Size</span></span>              | <span data-ttu-id="ce16a-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="ce16a-114">4 bytes</span></span>                              |
| <span data-ttu-id="ce16a-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ce16a-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ce16a-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ce16a-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ce16a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-117">Attribute-Id</span></span>      | <span data-ttu-id="ce16a-118">1.2.840.113556.1.2.469</span><span class="sxs-lookup"><span data-stu-id="ce16a-118">1.2.840.113556.1.2.469</span></span>               |
| <span data-ttu-id="ce16a-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ce16a-119">System-Id-Guid</span></span>    | <span data-ttu-id="ce16a-120">a8df7498-c5ea-11d1-bbcb-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="ce16a-120">a8df7498-c5ea-11d1-bbcb-0080c76670c0</span></span> |
| <span data-ttu-id="ce16a-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce16a-121">Syntax</span></span>            | [<span data-ttu-id="ce16a-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ce16a-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ce16a-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ce16a-123">Implementations</span></span>

-   [<span data-ttu-id="ce16a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ce16a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ce16a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ce16a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ce16a-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ce16a-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ce16a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ce16a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ce16a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ce16a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ce16a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ce16a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ce16a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ce16a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ce16a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce16a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ce16a-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-132">Entry</span></span> | <span data-ttu-id="ce16a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-135">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-136">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-136">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-137">System-Only</span></span>            | <span data-ttu-id="ce16a-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-138">False</span></span>                           |
| <span data-ttu-id="ce16a-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-140">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-140">True</span></span>                            |
| <span data-ttu-id="ce16a-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-141">Is Indexed</span></span>             | <span data-ttu-id="ce16a-142">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-142">True</span></span>                            |
| <span data-ttu-id="ce16a-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-143">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-144">False</span></span>                           |
| <span data-ttu-id="ce16a-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-149">Search-Flags</span></span>           | <span data-ttu-id="ce16a-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-150">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-151">System-Flags</span></span>           | <span data-ttu-id="ce16a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-152">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-153">Classes used in</span></span>        | [<span data-ttu-id="ce16a-154">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ce16a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce16a-155">Windows Server 2003</span></span>



| <span data-ttu-id="ce16a-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-156">Entry</span></span> | <span data-ttu-id="ce16a-157">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-159">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-160">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-160">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-161">System-Only</span></span>            | <span data-ttu-id="ce16a-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-162">False</span></span>                           |
| <span data-ttu-id="ce16a-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-164">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-164">True</span></span>                            |
| <span data-ttu-id="ce16a-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-165">Is Indexed</span></span>             | <span data-ttu-id="ce16a-166">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-166">True</span></span>                            |
| <span data-ttu-id="ce16a-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-167">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-168">False</span></span>                           |
| <span data-ttu-id="ce16a-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-173">Search-Flags</span></span>           | <span data-ttu-id="ce16a-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-174">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-175">System-Flags</span></span>           | <span data-ttu-id="ce16a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-176">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-177">Classes used in</span></span>        | [<span data-ttu-id="ce16a-178">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ce16a-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="ce16a-179">ADAM</span></span>



| <span data-ttu-id="ce16a-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-180">Entry</span></span> | <span data-ttu-id="ce16a-181">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-183">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-184">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-184">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-185">System-Only</span></span>            | <span data-ttu-id="ce16a-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-186">False</span></span>                           |
| <span data-ttu-id="ce16a-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-188">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-188">True</span></span>                            |
| <span data-ttu-id="ce16a-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-189">Is Indexed</span></span>             | <span data-ttu-id="ce16a-190">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-190">True</span></span>                            |
| <span data-ttu-id="ce16a-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-191">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-192">False</span></span>                           |
| <span data-ttu-id="ce16a-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-197">Search-Flags</span></span>           | <span data-ttu-id="ce16a-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-198">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-199">System-Flags</span></span>           | <span data-ttu-id="ce16a-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-200">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-201">Classes used in</span></span>        | [<span data-ttu-id="ce16a-202">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ce16a-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ce16a-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ce16a-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-204">Entry</span></span> | <span data-ttu-id="ce16a-205">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-207">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-208">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-208">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-209">System-Only</span></span>            | <span data-ttu-id="ce16a-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-210">False</span></span>                           |
| <span data-ttu-id="ce16a-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-212">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-212">True</span></span>                            |
| <span data-ttu-id="ce16a-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-213">Is Indexed</span></span>             | <span data-ttu-id="ce16a-214">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-214">True</span></span>                            |
| <span data-ttu-id="ce16a-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-215">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-216">False</span></span>                           |
| <span data-ttu-id="ce16a-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-221">Search-Flags</span></span>           | <span data-ttu-id="ce16a-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-222">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-223">System-Flags</span></span>           | <span data-ttu-id="ce16a-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-224">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-225">Classes used in</span></span>        | [<span data-ttu-id="ce16a-226">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ce16a-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce16a-227">Windows Server 2008</span></span>



| <span data-ttu-id="ce16a-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-228">Entry</span></span> | <span data-ttu-id="ce16a-229">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-231">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-232">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-232">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-233">System-Only</span></span>            | <span data-ttu-id="ce16a-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-234">False</span></span>                           |
| <span data-ttu-id="ce16a-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-236">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-236">True</span></span>                            |
| <span data-ttu-id="ce16a-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-237">Is Indexed</span></span>             | <span data-ttu-id="ce16a-238">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-238">True</span></span>                            |
| <span data-ttu-id="ce16a-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-239">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-240">False</span></span>                           |
| <span data-ttu-id="ce16a-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-245">Search-Flags</span></span>           | <span data-ttu-id="ce16a-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-246">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-247">System-Flags</span></span>           | <span data-ttu-id="ce16a-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-248">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-249">Classes used in</span></span>        | [<span data-ttu-id="ce16a-250">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ce16a-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce16a-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ce16a-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-252">Entry</span></span> | <span data-ttu-id="ce16a-253">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-255">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-256">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-256">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-257">System-Only</span></span>            | <span data-ttu-id="ce16a-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-258">False</span></span>                           |
| <span data-ttu-id="ce16a-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-259">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-260">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-260">True</span></span>                            |
| <span data-ttu-id="ce16a-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-261">Is Indexed</span></span>             | <span data-ttu-id="ce16a-262">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-262">True</span></span>                            |
| <span data-ttu-id="ce16a-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-263">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-264">False</span></span>                           |
| <span data-ttu-id="ce16a-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-269">Search-Flags</span></span>           | <span data-ttu-id="ce16a-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-270">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-271">System-Flags</span></span>           | <span data-ttu-id="ce16a-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-272">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-273">Classes used in</span></span>        | [<span data-ttu-id="ce16a-274">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ce16a-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce16a-275">Windows Server 2012</span></span>



| <span data-ttu-id="ce16a-276">Ввод</span><span class="sxs-lookup"><span data-stu-id="ce16a-276">Entry</span></span> | <span data-ttu-id="ce16a-277">Значение</span><span class="sxs-lookup"><span data-stu-id="ce16a-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ce16a-278">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ce16a-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ce16a-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce16a-279">MAPI-Id</span></span>                | <span data-ttu-id="ce16a-280">0x817A</span><span class="sxs-lookup"><span data-stu-id="ce16a-280">0x817A</span></span>                          |
| <span data-ttu-id="ce16a-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce16a-281">System-Only</span></span>            | <span data-ttu-id="ce16a-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-282">False</span></span>                           |
| <span data-ttu-id="ce16a-283">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ce16a-283">Is-Single-Valued</span></span>       | <span data-ttu-id="ce16a-284">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-284">True</span></span>                            |
| <span data-ttu-id="ce16a-285">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ce16a-285">Is Indexed</span></span>             | <span data-ttu-id="ce16a-286">True</span><span class="sxs-lookup"><span data-stu-id="ce16a-286">True</span></span>                            |
| <span data-ttu-id="ce16a-287">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ce16a-287">In Global Catalog</span></span>      | <span data-ttu-id="ce16a-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="ce16a-288">False</span></span>                           |
| <span data-ttu-id="ce16a-289">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ce16a-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce16a-290">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce16a-290">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ce16a-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce16a-291">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ce16a-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce16a-292">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ce16a-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-293">Search-Flags</span></span>           | <span data-ttu-id="ce16a-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce16a-294">0x00000001</span></span>                      |
| <span data-ttu-id="ce16a-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce16a-295">System-Flags</span></span>           | <span data-ttu-id="ce16a-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce16a-296">0x00000010</span></span>                      |
| <span data-ttu-id="ce16a-297">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ce16a-297">Classes used in</span></span>        | [<span data-ttu-id="ce16a-298">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ce16a-298">**Top**</span></span>](c-top.md)<br/> |



 

 





