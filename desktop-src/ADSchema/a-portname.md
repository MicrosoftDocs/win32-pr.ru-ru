---
title: Атрибут Port-Name
description: Список имен портов. Например, для портов принтеров или последовательных портов.
ms.assetid: 978e5de5-fc72-4b9c-ae15-4f2253d8081a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Port-Name
- Схема AD атрибута Портнаме
topic_type:
- apiref
api_name:
- Port-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cb873e2c16b31b3d72961873dcd438d84d9db9c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493947"
---
# <a name="port-name-attribute"></a><span data-ttu-id="d42a4-106">Атрибут Port-Name</span><span class="sxs-lookup"><span data-stu-id="d42a4-106">Port-Name attribute</span></span>

<span data-ttu-id="d42a4-107">Список имен портов.</span><span class="sxs-lookup"><span data-stu-id="d42a4-107">List of port names.</span></span> <span data-ttu-id="d42a4-108">Например, для портов принтеров или последовательных портов.</span><span class="sxs-lookup"><span data-stu-id="d42a4-108">For example, for printer ports or comm ports.</span></span>



| <span data-ttu-id="d42a4-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-109">Entry</span></span> | <span data-ttu-id="d42a4-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d42a4-111">CN</span><span class="sxs-lookup"><span data-stu-id="d42a4-111">CN</span></span>                | <span data-ttu-id="d42a4-112">Port-Name</span><span class="sxs-lookup"><span data-stu-id="d42a4-112">Port-Name</span></span>                                   |
| <span data-ttu-id="d42a4-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d42a4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d42a4-114">portName</span><span class="sxs-lookup"><span data-stu-id="d42a4-114">portName</span></span>                                    |
| <span data-ttu-id="d42a4-115">Размер</span><span class="sxs-lookup"><span data-stu-id="d42a4-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="d42a4-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d42a4-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d42a4-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d42a4-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d42a4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-118">Attribute-Id</span></span>      | <span data-ttu-id="d42a4-119">1.2.840.113556.1.4.228</span><span class="sxs-lookup"><span data-stu-id="d42a4-119">1.2.840.113556.1.4.228</span></span>                      |
| <span data-ttu-id="d42a4-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d42a4-120">System-Id-Guid</span></span>    | <span data-ttu-id="d42a4-121">281416c4-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d42a4-121">281416c4-1968-11d0-a28f-00aa003049e2</span></span>        |
| <span data-ttu-id="d42a4-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d42a4-122">Syntax</span></span>            | [<span data-ttu-id="d42a4-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d42a4-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d42a4-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d42a4-124">Implementations</span></span>

-   [<span data-ttu-id="d42a4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d42a4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d42a4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d42a4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d42a4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d42a4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d42a4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d42a4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d42a4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d42a4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d42a4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d42a4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d42a4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d42a4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d42a4-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-132">Entry</span></span> | <span data-ttu-id="d42a4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d42a4-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d42a4-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d42a4-136">System-Only</span></span>            | <span data-ttu-id="d42a4-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-137">False</span></span>                                          |
| <span data-ttu-id="d42a4-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d42a4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d42a4-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-139">False</span></span>                                          |
| <span data-ttu-id="d42a4-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d42a4-140">Is Indexed</span></span>             | <span data-ttu-id="d42a4-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-141">False</span></span>                                          |
| <span data-ttu-id="d42a4-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d42a4-142">In Global Catalog</span></span>      | <span data-ttu-id="d42a4-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-143">False</span></span>                                          |
| <span data-ttu-id="d42a4-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d42a4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d42a4-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d42a4-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d42a4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d42a4-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d42a4-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-148">Search-Flags</span></span>           | <span data-ttu-id="d42a4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d42a4-149">0x00000000</span></span>                                     |
| <span data-ttu-id="d42a4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-150">System-Flags</span></span>           | <span data-ttu-id="d42a4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d42a4-151">0x00000010</span></span>                                     |
| <span data-ttu-id="d42a4-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d42a4-152">Classes used in</span></span>        | [<span data-ttu-id="d42a4-153">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="d42a4-153">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d42a4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d42a4-154">Windows Server 2003</span></span>



| <span data-ttu-id="d42a4-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-155">Entry</span></span> | <span data-ttu-id="d42a4-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d42a4-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d42a4-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d42a4-159">System-Only</span></span>            | <span data-ttu-id="d42a4-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-160">False</span></span>                                          |
| <span data-ttu-id="d42a4-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d42a4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d42a4-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-162">False</span></span>                                          |
| <span data-ttu-id="d42a4-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d42a4-163">Is Indexed</span></span>             | <span data-ttu-id="d42a4-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-164">False</span></span>                                          |
| <span data-ttu-id="d42a4-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d42a4-165">In Global Catalog</span></span>      | <span data-ttu-id="d42a4-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-166">False</span></span>                                          |
| <span data-ttu-id="d42a4-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d42a4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d42a4-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d42a4-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d42a4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d42a4-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d42a4-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-171">Search-Flags</span></span>           | <span data-ttu-id="d42a4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d42a4-172">0x00000000</span></span>                                     |
| <span data-ttu-id="d42a4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-173">System-Flags</span></span>           | <span data-ttu-id="d42a4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d42a4-174">0x00000010</span></span>                                     |
| <span data-ttu-id="d42a4-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d42a4-175">Classes used in</span></span>        | [<span data-ttu-id="d42a4-176">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="d42a4-176">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d42a4-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d42a4-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d42a4-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-178">Entry</span></span> | <span data-ttu-id="d42a4-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d42a4-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d42a4-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d42a4-182">System-Only</span></span>            | <span data-ttu-id="d42a4-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-183">False</span></span>                                          |
| <span data-ttu-id="d42a4-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d42a4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d42a4-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-185">False</span></span>                                          |
| <span data-ttu-id="d42a4-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d42a4-186">Is Indexed</span></span>             | <span data-ttu-id="d42a4-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-187">False</span></span>                                          |
| <span data-ttu-id="d42a4-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d42a4-188">In Global Catalog</span></span>      | <span data-ttu-id="d42a4-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-189">False</span></span>                                          |
| <span data-ttu-id="d42a4-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d42a4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d42a4-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d42a4-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d42a4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d42a4-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d42a4-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-194">Search-Flags</span></span>           | <span data-ttu-id="d42a4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d42a4-195">0x00000000</span></span>                                     |
| <span data-ttu-id="d42a4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-196">System-Flags</span></span>           | <span data-ttu-id="d42a4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d42a4-197">0x00000010</span></span>                                     |
| <span data-ttu-id="d42a4-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d42a4-198">Classes used in</span></span>        | [<span data-ttu-id="d42a4-199">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="d42a4-199">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d42a4-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d42a4-200">Windows Server 2008</span></span>



| <span data-ttu-id="d42a4-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-201">Entry</span></span> | <span data-ttu-id="d42a4-202">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d42a4-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d42a4-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d42a4-205">System-Only</span></span>            | <span data-ttu-id="d42a4-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-206">False</span></span>                                          |
| <span data-ttu-id="d42a4-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d42a4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d42a4-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-208">False</span></span>                                          |
| <span data-ttu-id="d42a4-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d42a4-209">Is Indexed</span></span>             | <span data-ttu-id="d42a4-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-210">False</span></span>                                          |
| <span data-ttu-id="d42a4-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d42a4-211">In Global Catalog</span></span>      | <span data-ttu-id="d42a4-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-212">False</span></span>                                          |
| <span data-ttu-id="d42a4-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d42a4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d42a4-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d42a4-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d42a4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d42a4-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d42a4-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-217">Search-Flags</span></span>           | <span data-ttu-id="d42a4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d42a4-218">0x00000000</span></span>                                     |
| <span data-ttu-id="d42a4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-219">System-Flags</span></span>           | <span data-ttu-id="d42a4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d42a4-220">0x00000010</span></span>                                     |
| <span data-ttu-id="d42a4-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d42a4-221">Classes used in</span></span>        | [<span data-ttu-id="d42a4-222">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="d42a4-222">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d42a4-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d42a4-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d42a4-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-224">Entry</span></span> | <span data-ttu-id="d42a4-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d42a4-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d42a4-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d42a4-228">System-Only</span></span>            | <span data-ttu-id="d42a4-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-229">False</span></span>                                          |
| <span data-ttu-id="d42a4-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d42a4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d42a4-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-231">False</span></span>                                          |
| <span data-ttu-id="d42a4-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d42a4-232">Is Indexed</span></span>             | <span data-ttu-id="d42a4-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-233">False</span></span>                                          |
| <span data-ttu-id="d42a4-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d42a4-234">In Global Catalog</span></span>      | <span data-ttu-id="d42a4-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-235">False</span></span>                                          |
| <span data-ttu-id="d42a4-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d42a4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d42a4-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d42a4-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d42a4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d42a4-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d42a4-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-240">Search-Flags</span></span>           | <span data-ttu-id="d42a4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d42a4-241">0x00000000</span></span>                                     |
| <span data-ttu-id="d42a4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-242">System-Flags</span></span>           | <span data-ttu-id="d42a4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d42a4-243">0x00000010</span></span>                                     |
| <span data-ttu-id="d42a4-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d42a4-244">Classes used in</span></span>        | [<span data-ttu-id="d42a4-245">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="d42a4-245">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d42a4-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d42a4-246">Windows Server 2012</span></span>



| <span data-ttu-id="d42a4-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="d42a4-247">Entry</span></span> | <span data-ttu-id="d42a4-248">Значение</span><span class="sxs-lookup"><span data-stu-id="d42a4-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="d42a4-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d42a4-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d42a4-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="d42a4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d42a4-251">System-Only</span></span>            | <span data-ttu-id="d42a4-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-252">False</span></span>                                          |
| <span data-ttu-id="d42a4-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d42a4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d42a4-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-254">False</span></span>                                          |
| <span data-ttu-id="d42a4-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d42a4-255">Is Indexed</span></span>             | <span data-ttu-id="d42a4-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-256">False</span></span>                                          |
| <span data-ttu-id="d42a4-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d42a4-257">In Global Catalog</span></span>      | <span data-ttu-id="d42a4-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="d42a4-258">False</span></span>                                          |
| <span data-ttu-id="d42a4-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d42a4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d42a4-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d42a4-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="d42a4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d42a4-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d42a4-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="d42a4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-263">Search-Flags</span></span>           | <span data-ttu-id="d42a4-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d42a4-264">0x00000000</span></span>                                     |
| <span data-ttu-id="d42a4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d42a4-265">System-Flags</span></span>           | <span data-ttu-id="d42a4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d42a4-266">0x00000010</span></span>                                     |
| <span data-ttu-id="d42a4-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d42a4-267">Classes used in</span></span>        | [<span data-ttu-id="d42a4-268">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="d42a4-268">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





