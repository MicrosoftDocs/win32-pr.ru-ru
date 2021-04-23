---
title: Атрибут защиты от MSMQ, защищенный источником
description: Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес. Он определяет, принимает ли MSMQ сообщения только из защищенного источника (например, HTTPS) для этой очереди.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов, защищенных с самого источника MSMQ
- Схема AD атрибута MSMQ-SecuredSource
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535975"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="58a7d-106">Атрибут защиты от MSMQ, защищенный источником</span><span class="sxs-lookup"><span data-stu-id="58a7d-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="58a7d-107">Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес.</span><span class="sxs-lookup"><span data-stu-id="58a7d-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="58a7d-108">Он определяет, принимает ли MSMQ сообщения только из защищенного источника (например, HTTPS) для этой очереди.</span><span class="sxs-lookup"><span data-stu-id="58a7d-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="58a7d-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a7d-109">Entry</span></span> | <span data-ttu-id="58a7d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="58a7d-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="58a7d-111">CN</span><span class="sxs-lookup"><span data-stu-id="58a7d-111">CN</span></span>                | <span data-ttu-id="58a7d-112">MSMQ — защищенный источник</span><span class="sxs-lookup"><span data-stu-id="58a7d-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="58a7d-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="58a7d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="58a7d-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="58a7d-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="58a7d-115">Размер</span><span class="sxs-lookup"><span data-stu-id="58a7d-115">Size</span></span>              | <span data-ttu-id="58a7d-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="58a7d-116">4 bytes</span></span>                              |
| <span data-ttu-id="58a7d-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="58a7d-117">Update Privilege</span></span>  | <span data-ttu-id="58a7d-118">Владелец очереди.</span><span class="sxs-lookup"><span data-stu-id="58a7d-118">The queue owner.</span></span>                     |
| <span data-ttu-id="58a7d-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="58a7d-119">Update Frequency</span></span>  | <span data-ttu-id="58a7d-120">При создании очереди.</span><span class="sxs-lookup"><span data-stu-id="58a7d-120">When a queue is created.</span></span>             |
| <span data-ttu-id="58a7d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58a7d-121">Attribute-Id</span></span>      | <span data-ttu-id="58a7d-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="58a7d-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="58a7d-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="58a7d-123">System-Id-Guid</span></span>    | <span data-ttu-id="58a7d-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span><span class="sxs-lookup"><span data-stu-id="58a7d-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="58a7d-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58a7d-125">Syntax</span></span>            | [<span data-ttu-id="58a7d-126">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="58a7d-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="58a7d-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="58a7d-127">Implementations</span></span>

-   [<span data-ttu-id="58a7d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58a7d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58a7d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58a7d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58a7d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58a7d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58a7d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58a7d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58a7d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58a7d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="58a7d-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58a7d-133">Windows Server 2003</span></span>



| <span data-ttu-id="58a7d-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a7d-134">Entry</span></span> | <span data-ttu-id="58a7d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="58a7d-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="58a7d-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a7d-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a7d-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a7d-138">System-Only</span></span>            | <span data-ttu-id="58a7d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-139">False</span></span>                                        |
| <span data-ttu-id="58a7d-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a7d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="58a7d-141">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-141">True</span></span>                                         |
| <span data-ttu-id="58a7d-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a7d-142">Is Indexed</span></span>             | <span data-ttu-id="58a7d-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-143">False</span></span>                                        |
| <span data-ttu-id="58a7d-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a7d-144">In Global Catalog</span></span>      | <span data-ttu-id="58a7d-145">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-145">True</span></span>                                         |
| <span data-ttu-id="58a7d-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a7d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a7d-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a7d-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="58a7d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a7d-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a7d-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-150">Search-Flags</span></span>           | <span data-ttu-id="58a7d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a7d-151">0x00000000</span></span>                                   |
| <span data-ttu-id="58a7d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-152">System-Flags</span></span>           | <span data-ttu-id="58a7d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a7d-153">0x00000010</span></span>                                   |
| <span data-ttu-id="58a7d-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a7d-154">Classes used in</span></span>        | [<span data-ttu-id="58a7d-155">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="58a7d-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58a7d-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58a7d-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58a7d-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a7d-157">Entry</span></span> | <span data-ttu-id="58a7d-158">Значение</span><span class="sxs-lookup"><span data-stu-id="58a7d-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="58a7d-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a7d-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a7d-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a7d-161">System-Only</span></span>            | <span data-ttu-id="58a7d-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-162">False</span></span>                                        |
| <span data-ttu-id="58a7d-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a7d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="58a7d-164">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-164">True</span></span>                                         |
| <span data-ttu-id="58a7d-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a7d-165">Is Indexed</span></span>             | <span data-ttu-id="58a7d-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-166">False</span></span>                                        |
| <span data-ttu-id="58a7d-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a7d-167">In Global Catalog</span></span>      | <span data-ttu-id="58a7d-168">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-168">True</span></span>                                         |
| <span data-ttu-id="58a7d-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a7d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a7d-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a7d-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="58a7d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a7d-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a7d-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-173">Search-Flags</span></span>           | <span data-ttu-id="58a7d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a7d-174">0x00000000</span></span>                                   |
| <span data-ttu-id="58a7d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-175">System-Flags</span></span>           | <span data-ttu-id="58a7d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a7d-176">0x00000010</span></span>                                   |
| <span data-ttu-id="58a7d-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a7d-177">Classes used in</span></span>        | [<span data-ttu-id="58a7d-178">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="58a7d-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58a7d-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58a7d-179">Windows Server 2008</span></span>



| <span data-ttu-id="58a7d-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a7d-180">Entry</span></span> | <span data-ttu-id="58a7d-181">Значение</span><span class="sxs-lookup"><span data-stu-id="58a7d-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="58a7d-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a7d-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a7d-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a7d-184">System-Only</span></span>            | <span data-ttu-id="58a7d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-185">False</span></span>                                        |
| <span data-ttu-id="58a7d-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a7d-186">Is-Single-Valued</span></span>       | <span data-ttu-id="58a7d-187">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-187">True</span></span>                                         |
| <span data-ttu-id="58a7d-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a7d-188">Is Indexed</span></span>             | <span data-ttu-id="58a7d-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-189">False</span></span>                                        |
| <span data-ttu-id="58a7d-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a7d-190">In Global Catalog</span></span>      | <span data-ttu-id="58a7d-191">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-191">True</span></span>                                         |
| <span data-ttu-id="58a7d-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a7d-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a7d-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a7d-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="58a7d-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a7d-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a7d-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-196">Search-Flags</span></span>           | <span data-ttu-id="58a7d-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a7d-197">0x00000000</span></span>                                   |
| <span data-ttu-id="58a7d-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-198">System-Flags</span></span>           | <span data-ttu-id="58a7d-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a7d-199">0x00000010</span></span>                                   |
| <span data-ttu-id="58a7d-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a7d-200">Classes used in</span></span>        | [<span data-ttu-id="58a7d-201">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="58a7d-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58a7d-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58a7d-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58a7d-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a7d-203">Entry</span></span> | <span data-ttu-id="58a7d-204">Значение</span><span class="sxs-lookup"><span data-stu-id="58a7d-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="58a7d-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a7d-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a7d-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a7d-207">System-Only</span></span>            | <span data-ttu-id="58a7d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-208">False</span></span>                                        |
| <span data-ttu-id="58a7d-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a7d-209">Is-Single-Valued</span></span>       | <span data-ttu-id="58a7d-210">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-210">True</span></span>                                         |
| <span data-ttu-id="58a7d-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a7d-211">Is Indexed</span></span>             | <span data-ttu-id="58a7d-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-212">False</span></span>                                        |
| <span data-ttu-id="58a7d-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a7d-213">In Global Catalog</span></span>      | <span data-ttu-id="58a7d-214">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-214">True</span></span>                                         |
| <span data-ttu-id="58a7d-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a7d-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a7d-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a7d-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="58a7d-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a7d-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a7d-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-219">Search-Flags</span></span>           | <span data-ttu-id="58a7d-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a7d-220">0x00000000</span></span>                                   |
| <span data-ttu-id="58a7d-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-221">System-Flags</span></span>           | <span data-ttu-id="58a7d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a7d-222">0x00000010</span></span>                                   |
| <span data-ttu-id="58a7d-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a7d-223">Classes used in</span></span>        | [<span data-ttu-id="58a7d-224">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="58a7d-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58a7d-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58a7d-225">Windows Server 2012</span></span>



| <span data-ttu-id="58a7d-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a7d-226">Entry</span></span> | <span data-ttu-id="58a7d-227">Значение</span><span class="sxs-lookup"><span data-stu-id="58a7d-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="58a7d-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a7d-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a7d-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="58a7d-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a7d-230">System-Only</span></span>            | <span data-ttu-id="58a7d-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-231">False</span></span>                                        |
| <span data-ttu-id="58a7d-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a7d-232">Is-Single-Valued</span></span>       | <span data-ttu-id="58a7d-233">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-233">True</span></span>                                         |
| <span data-ttu-id="58a7d-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a7d-234">Is Indexed</span></span>             | <span data-ttu-id="58a7d-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a7d-235">False</span></span>                                        |
| <span data-ttu-id="58a7d-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a7d-236">In Global Catalog</span></span>      | <span data-ttu-id="58a7d-237">True</span><span class="sxs-lookup"><span data-stu-id="58a7d-237">True</span></span>                                         |
| <span data-ttu-id="58a7d-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a7d-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a7d-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a7d-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="58a7d-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a7d-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a7d-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="58a7d-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-242">Search-Flags</span></span>           | <span data-ttu-id="58a7d-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a7d-243">0x00000000</span></span>                                   |
| <span data-ttu-id="58a7d-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a7d-244">System-Flags</span></span>           | <span data-ttu-id="58a7d-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a7d-245">0x00000010</span></span>                                   |
| <span data-ttu-id="58a7d-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a7d-246">Classes used in</span></span>        | [<span data-ttu-id="58a7d-247">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="58a7d-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





