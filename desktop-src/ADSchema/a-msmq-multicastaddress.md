---
title: MSMQ — атрибут адреса многоадресной рассылки
description: Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес. Он определяет, будут ли MSMQ принимать сообщения с адреса многоадресной рассылки.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ — схема AD атрибута «адрес многоадресной рассылки»
- Схема AD атрибута MSMQ-MulticastAddress
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535978"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="30ca1-106">MSMQ — атрибут адреса многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="30ca1-107">Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес.</span><span class="sxs-lookup"><span data-stu-id="30ca1-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="30ca1-108">Он определяет, будут ли MSMQ принимать сообщения с адреса многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="30ca1-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="30ca1-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ca1-109">Entry</span></span> | <span data-ttu-id="30ca1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="30ca1-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="30ca1-111">CN</span><span class="sxs-lookup"><span data-stu-id="30ca1-111">CN</span></span>                | <span data-ttu-id="30ca1-112">MSMQ — адрес многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="30ca1-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="30ca1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="30ca1-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="30ca1-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="30ca1-115">Размер</span><span class="sxs-lookup"><span data-stu-id="30ca1-115">Size</span></span>              | <span data-ttu-id="30ca1-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="30ca1-116">4 bytes</span></span>                                     |
| <span data-ttu-id="30ca1-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="30ca1-117">Update Privilege</span></span>  | <span data-ttu-id="30ca1-118">Владелец очереди.</span><span class="sxs-lookup"><span data-stu-id="30ca1-118">The queue owner.</span></span>                            |
| <span data-ttu-id="30ca1-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="30ca1-119">Update Frequency</span></span>  | <span data-ttu-id="30ca1-120">При создании очереди.</span><span class="sxs-lookup"><span data-stu-id="30ca1-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="30ca1-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30ca1-121">Attribute-Id</span></span>      | <span data-ttu-id="30ca1-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="30ca1-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="30ca1-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="30ca1-123">System-Id-Guid</span></span>    | <span data-ttu-id="30ca1-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span><span class="sxs-lookup"><span data-stu-id="30ca1-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="30ca1-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30ca1-125">Syntax</span></span>            | [<span data-ttu-id="30ca1-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="30ca1-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="30ca1-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="30ca1-127">Implementations</span></span>

-   [<span data-ttu-id="30ca1-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="30ca1-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="30ca1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="30ca1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="30ca1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30ca1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30ca1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30ca1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30ca1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30ca1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="30ca1-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30ca1-133">Windows Server 2003</span></span>



| <span data-ttu-id="30ca1-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ca1-134">Entry</span></span> | <span data-ttu-id="30ca1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="30ca1-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="30ca1-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ca1-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ca1-138">System-Only</span></span>            | <span data-ttu-id="30ca1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-139">False</span></span>                                        |
| <span data-ttu-id="30ca1-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ca1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="30ca1-141">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-141">True</span></span>                                         |
| <span data-ttu-id="30ca1-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ca1-142">Is Indexed</span></span>             | <span data-ttu-id="30ca1-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-143">False</span></span>                                        |
| <span data-ttu-id="30ca1-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ca1-144">In Global Catalog</span></span>      | <span data-ttu-id="30ca1-145">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-145">True</span></span>                                         |
| <span data-ttu-id="30ca1-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ca1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ca1-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ca1-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="30ca1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ca1-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ca1-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-150">Search-Flags</span></span>           | <span data-ttu-id="30ca1-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ca1-151">0x00000000</span></span>                                   |
| <span data-ttu-id="30ca1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-152">System-Flags</span></span>           | <span data-ttu-id="30ca1-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ca1-153">0x00000010</span></span>                                   |
| <span data-ttu-id="30ca1-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ca1-154">Classes used in</span></span>        | [<span data-ttu-id="30ca1-155">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="30ca1-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="30ca1-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="30ca1-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="30ca1-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ca1-157">Entry</span></span> | <span data-ttu-id="30ca1-158">Значение</span><span class="sxs-lookup"><span data-stu-id="30ca1-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="30ca1-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ca1-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ca1-161">System-Only</span></span>            | <span data-ttu-id="30ca1-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-162">False</span></span>                                        |
| <span data-ttu-id="30ca1-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ca1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="30ca1-164">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-164">True</span></span>                                         |
| <span data-ttu-id="30ca1-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ca1-165">Is Indexed</span></span>             | <span data-ttu-id="30ca1-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-166">False</span></span>                                        |
| <span data-ttu-id="30ca1-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ca1-167">In Global Catalog</span></span>      | <span data-ttu-id="30ca1-168">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-168">True</span></span>                                         |
| <span data-ttu-id="30ca1-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ca1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ca1-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ca1-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="30ca1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ca1-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ca1-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-173">Search-Flags</span></span>           | <span data-ttu-id="30ca1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ca1-174">0x00000000</span></span>                                   |
| <span data-ttu-id="30ca1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-175">System-Flags</span></span>           | <span data-ttu-id="30ca1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ca1-176">0x00000010</span></span>                                   |
| <span data-ttu-id="30ca1-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ca1-177">Classes used in</span></span>        | [<span data-ttu-id="30ca1-178">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="30ca1-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="30ca1-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30ca1-179">Windows Server 2008</span></span>



| <span data-ttu-id="30ca1-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ca1-180">Entry</span></span> | <span data-ttu-id="30ca1-181">Значение</span><span class="sxs-lookup"><span data-stu-id="30ca1-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="30ca1-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ca1-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ca1-184">System-Only</span></span>            | <span data-ttu-id="30ca1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-185">False</span></span>                                        |
| <span data-ttu-id="30ca1-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ca1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="30ca1-187">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-187">True</span></span>                                         |
| <span data-ttu-id="30ca1-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ca1-188">Is Indexed</span></span>             | <span data-ttu-id="30ca1-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-189">False</span></span>                                        |
| <span data-ttu-id="30ca1-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ca1-190">In Global Catalog</span></span>      | <span data-ttu-id="30ca1-191">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-191">True</span></span>                                         |
| <span data-ttu-id="30ca1-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ca1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ca1-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ca1-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="30ca1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ca1-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ca1-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-196">Search-Flags</span></span>           | <span data-ttu-id="30ca1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ca1-197">0x00000000</span></span>                                   |
| <span data-ttu-id="30ca1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-198">System-Flags</span></span>           | <span data-ttu-id="30ca1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ca1-199">0x00000010</span></span>                                   |
| <span data-ttu-id="30ca1-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ca1-200">Classes used in</span></span>        | [<span data-ttu-id="30ca1-201">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="30ca1-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30ca1-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30ca1-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30ca1-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ca1-203">Entry</span></span> | <span data-ttu-id="30ca1-204">Значение</span><span class="sxs-lookup"><span data-stu-id="30ca1-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="30ca1-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ca1-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ca1-207">System-Only</span></span>            | <span data-ttu-id="30ca1-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-208">False</span></span>                                        |
| <span data-ttu-id="30ca1-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ca1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="30ca1-210">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-210">True</span></span>                                         |
| <span data-ttu-id="30ca1-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ca1-211">Is Indexed</span></span>             | <span data-ttu-id="30ca1-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-212">False</span></span>                                        |
| <span data-ttu-id="30ca1-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ca1-213">In Global Catalog</span></span>      | <span data-ttu-id="30ca1-214">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-214">True</span></span>                                         |
| <span data-ttu-id="30ca1-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ca1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ca1-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ca1-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="30ca1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ca1-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ca1-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-219">Search-Flags</span></span>           | <span data-ttu-id="30ca1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ca1-220">0x00000000</span></span>                                   |
| <span data-ttu-id="30ca1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-221">System-Flags</span></span>           | <span data-ttu-id="30ca1-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ca1-222">0x00000010</span></span>                                   |
| <span data-ttu-id="30ca1-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ca1-223">Classes used in</span></span>        | [<span data-ttu-id="30ca1-224">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="30ca1-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30ca1-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30ca1-225">Windows Server 2012</span></span>



| <span data-ttu-id="30ca1-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="30ca1-226">Entry</span></span> | <span data-ttu-id="30ca1-227">Значение</span><span class="sxs-lookup"><span data-stu-id="30ca1-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="30ca1-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="30ca1-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30ca1-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="30ca1-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="30ca1-230">System-Only</span></span>            | <span data-ttu-id="30ca1-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-231">False</span></span>                                        |
| <span data-ttu-id="30ca1-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="30ca1-232">Is-Single-Valued</span></span>       | <span data-ttu-id="30ca1-233">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-233">True</span></span>                                         |
| <span data-ttu-id="30ca1-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="30ca1-234">Is Indexed</span></span>             | <span data-ttu-id="30ca1-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="30ca1-235">False</span></span>                                        |
| <span data-ttu-id="30ca1-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="30ca1-236">In Global Catalog</span></span>      | <span data-ttu-id="30ca1-237">True</span><span class="sxs-lookup"><span data-stu-id="30ca1-237">True</span></span>                                         |
| <span data-ttu-id="30ca1-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="30ca1-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="30ca1-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30ca1-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="30ca1-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30ca1-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30ca1-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="30ca1-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-242">Search-Flags</span></span>           | <span data-ttu-id="30ca1-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30ca1-243">0x00000000</span></span>                                   |
| <span data-ttu-id="30ca1-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30ca1-244">System-Flags</span></span>           | <span data-ttu-id="30ca1-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30ca1-245">0x00000010</span></span>                                   |
| <span data-ttu-id="30ca1-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="30ca1-246">Classes used in</span></span>        | [<span data-ttu-id="30ca1-247">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="30ca1-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





