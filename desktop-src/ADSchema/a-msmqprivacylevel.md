---
title: MSMQ — атрибут уровня конфиденциальности
description: Уровень конфиденциальности, необходимый для очереди.
ms.assetid: 37addd1c-9c92-4155-99ff-dd711927717f
ms.tgt_platform: multiple
keywords:
- MSMQ — схема AD атрибута уровня конфиденциальности
- Схема AD атрибута Мсмкпривацилевел
topic_type:
- apiref
api_name:
- MSMQ-Privacy-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349bcffb521402b4f915937e205504ece541eee4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989810"
---
# <a name="msmq-privacy-level-attribute"></a><span data-ttu-id="1988e-105">MSMQ — атрибут уровня конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="1988e-105">MSMQ-Privacy-Level attribute</span></span>

<span data-ttu-id="1988e-106">Уровень конфиденциальности, необходимый для очереди.</span><span class="sxs-lookup"><span data-stu-id="1988e-106">The privacy level that is required by the queue.</span></span>



| <span data-ttu-id="1988e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-107">Entry</span></span> | <span data-ttu-id="1988e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1988e-109">CN</span><span class="sxs-lookup"><span data-stu-id="1988e-109">CN</span></span>                | <span data-ttu-id="1988e-110">MSMQ-уровень конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="1988e-110">MSMQ-Privacy-Level</span></span>                   |
| <span data-ttu-id="1988e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1988e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1988e-112">мсмкпривацилевел</span><span class="sxs-lookup"><span data-stu-id="1988e-112">mSMQPrivacyLevel</span></span>                     |
| <span data-ttu-id="1988e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1988e-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="1988e-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1988e-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1988e-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1988e-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1988e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-116">Attribute-Id</span></span>      | <span data-ttu-id="1988e-117">1.2.840.113556.1.4.924</span><span class="sxs-lookup"><span data-stu-id="1988e-117">1.2.840.113556.1.4.924</span></span>               |
| <span data-ttu-id="1988e-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1988e-118">System-Id-Guid</span></span>    | <span data-ttu-id="1988e-119">9a0dc327-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="1988e-119">9a0dc327-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="1988e-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1988e-120">Syntax</span></span>            | [<span data-ttu-id="1988e-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="1988e-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1988e-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1988e-122">Implementations</span></span>

-   [<span data-ttu-id="1988e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1988e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1988e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1988e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1988e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1988e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1988e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1988e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1988e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1988e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1988e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1988e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1988e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1988e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1988e-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-130">Entry</span></span> | <span data-ttu-id="1988e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1988e-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1988e-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1988e-134">System-Only</span></span>            | <span data-ttu-id="1988e-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-135">False</span></span>                                        |
| <span data-ttu-id="1988e-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1988e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1988e-137">True</span><span class="sxs-lookup"><span data-stu-id="1988e-137">True</span></span>                                         |
| <span data-ttu-id="1988e-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1988e-138">Is Indexed</span></span>             | <span data-ttu-id="1988e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-139">False</span></span>                                        |
| <span data-ttu-id="1988e-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1988e-140">In Global Catalog</span></span>      | <span data-ttu-id="1988e-141">True</span><span class="sxs-lookup"><span data-stu-id="1988e-141">True</span></span>                                         |
| <span data-ttu-id="1988e-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1988e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1988e-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1988e-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1988e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1988e-144">Range-Lower</span></span>            | <span data-ttu-id="1988e-145">0</span><span class="sxs-lookup"><span data-stu-id="1988e-145">0</span></span>                                            |
| <span data-ttu-id="1988e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1988e-146">Range-Upper</span></span>            | <span data-ttu-id="1988e-147">2</span><span class="sxs-lookup"><span data-stu-id="1988e-147">2</span></span>                                            |
| <span data-ttu-id="1988e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-148">Search-Flags</span></span>           | <span data-ttu-id="1988e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1988e-149">0x00000000</span></span>                                   |
| <span data-ttu-id="1988e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-150">System-Flags</span></span>           | <span data-ttu-id="1988e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1988e-151">0x00000010</span></span>                                   |
| <span data-ttu-id="1988e-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1988e-152">Classes used in</span></span>        | [<span data-ttu-id="1988e-153">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="1988e-153">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1988e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1988e-154">Windows Server 2003</span></span>



| <span data-ttu-id="1988e-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-155">Entry</span></span> | <span data-ttu-id="1988e-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1988e-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1988e-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1988e-159">System-Only</span></span>            | <span data-ttu-id="1988e-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-160">False</span></span>                                        |
| <span data-ttu-id="1988e-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1988e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1988e-162">True</span><span class="sxs-lookup"><span data-stu-id="1988e-162">True</span></span>                                         |
| <span data-ttu-id="1988e-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1988e-163">Is Indexed</span></span>             | <span data-ttu-id="1988e-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-164">False</span></span>                                        |
| <span data-ttu-id="1988e-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1988e-165">In Global Catalog</span></span>      | <span data-ttu-id="1988e-166">True</span><span class="sxs-lookup"><span data-stu-id="1988e-166">True</span></span>                                         |
| <span data-ttu-id="1988e-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1988e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1988e-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1988e-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1988e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1988e-169">Range-Lower</span></span>            | <span data-ttu-id="1988e-170">0</span><span class="sxs-lookup"><span data-stu-id="1988e-170">0</span></span>                                            |
| <span data-ttu-id="1988e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1988e-171">Range-Upper</span></span>            | <span data-ttu-id="1988e-172">2</span><span class="sxs-lookup"><span data-stu-id="1988e-172">2</span></span>                                            |
| <span data-ttu-id="1988e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-173">Search-Flags</span></span>           | <span data-ttu-id="1988e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1988e-174">0x00000000</span></span>                                   |
| <span data-ttu-id="1988e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-175">System-Flags</span></span>           | <span data-ttu-id="1988e-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1988e-176">0x00000010</span></span>                                   |
| <span data-ttu-id="1988e-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1988e-177">Classes used in</span></span>        | [<span data-ttu-id="1988e-178">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="1988e-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1988e-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1988e-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1988e-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-180">Entry</span></span> | <span data-ttu-id="1988e-181">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1988e-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1988e-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="1988e-184">System-Only</span></span>            | <span data-ttu-id="1988e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-185">False</span></span>                                        |
| <span data-ttu-id="1988e-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1988e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="1988e-187">True</span><span class="sxs-lookup"><span data-stu-id="1988e-187">True</span></span>                                         |
| <span data-ttu-id="1988e-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1988e-188">Is Indexed</span></span>             | <span data-ttu-id="1988e-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-189">False</span></span>                                        |
| <span data-ttu-id="1988e-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1988e-190">In Global Catalog</span></span>      | <span data-ttu-id="1988e-191">True</span><span class="sxs-lookup"><span data-stu-id="1988e-191">True</span></span>                                         |
| <span data-ttu-id="1988e-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1988e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="1988e-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1988e-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1988e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1988e-194">Range-Lower</span></span>            | <span data-ttu-id="1988e-195">0</span><span class="sxs-lookup"><span data-stu-id="1988e-195">0</span></span>                                            |
| <span data-ttu-id="1988e-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1988e-196">Range-Upper</span></span>            | <span data-ttu-id="1988e-197">2</span><span class="sxs-lookup"><span data-stu-id="1988e-197">2</span></span>                                            |
| <span data-ttu-id="1988e-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-198">Search-Flags</span></span>           | <span data-ttu-id="1988e-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1988e-199">0x00000000</span></span>                                   |
| <span data-ttu-id="1988e-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-200">System-Flags</span></span>           | <span data-ttu-id="1988e-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1988e-201">0x00000010</span></span>                                   |
| <span data-ttu-id="1988e-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1988e-202">Classes used in</span></span>        | [<span data-ttu-id="1988e-203">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="1988e-203">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1988e-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1988e-204">Windows Server 2008</span></span>



| <span data-ttu-id="1988e-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-205">Entry</span></span> | <span data-ttu-id="1988e-206">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-206">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1988e-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1988e-207">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-208">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1988e-209">System-Only</span></span>            | <span data-ttu-id="1988e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-210">False</span></span>                                        |
| <span data-ttu-id="1988e-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1988e-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1988e-212">True</span><span class="sxs-lookup"><span data-stu-id="1988e-212">True</span></span>                                         |
| <span data-ttu-id="1988e-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1988e-213">Is Indexed</span></span>             | <span data-ttu-id="1988e-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-214">False</span></span>                                        |
| <span data-ttu-id="1988e-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1988e-215">In Global Catalog</span></span>      | <span data-ttu-id="1988e-216">True</span><span class="sxs-lookup"><span data-stu-id="1988e-216">True</span></span>                                         |
| <span data-ttu-id="1988e-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1988e-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1988e-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1988e-218">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1988e-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1988e-219">Range-Lower</span></span>            | <span data-ttu-id="1988e-220">0</span><span class="sxs-lookup"><span data-stu-id="1988e-220">0</span></span>                                            |
| <span data-ttu-id="1988e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1988e-221">Range-Upper</span></span>            | <span data-ttu-id="1988e-222">2</span><span class="sxs-lookup"><span data-stu-id="1988e-222">2</span></span>                                            |
| <span data-ttu-id="1988e-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-223">Search-Flags</span></span>           | <span data-ttu-id="1988e-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1988e-224">0x00000000</span></span>                                   |
| <span data-ttu-id="1988e-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-225">System-Flags</span></span>           | <span data-ttu-id="1988e-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1988e-226">0x00000010</span></span>                                   |
| <span data-ttu-id="1988e-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1988e-227">Classes used in</span></span>        | [<span data-ttu-id="1988e-228">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="1988e-228">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1988e-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1988e-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1988e-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-230">Entry</span></span> | <span data-ttu-id="1988e-231">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-231">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1988e-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1988e-232">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-233">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="1988e-234">System-Only</span></span>            | <span data-ttu-id="1988e-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-235">False</span></span>                                        |
| <span data-ttu-id="1988e-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1988e-236">Is-Single-Valued</span></span>       | <span data-ttu-id="1988e-237">True</span><span class="sxs-lookup"><span data-stu-id="1988e-237">True</span></span>                                         |
| <span data-ttu-id="1988e-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1988e-238">Is Indexed</span></span>             | <span data-ttu-id="1988e-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-239">False</span></span>                                        |
| <span data-ttu-id="1988e-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1988e-240">In Global Catalog</span></span>      | <span data-ttu-id="1988e-241">True</span><span class="sxs-lookup"><span data-stu-id="1988e-241">True</span></span>                                         |
| <span data-ttu-id="1988e-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1988e-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="1988e-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1988e-243">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1988e-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1988e-244">Range-Lower</span></span>            | <span data-ttu-id="1988e-245">0</span><span class="sxs-lookup"><span data-stu-id="1988e-245">0</span></span>                                            |
| <span data-ttu-id="1988e-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1988e-246">Range-Upper</span></span>            | <span data-ttu-id="1988e-247">2</span><span class="sxs-lookup"><span data-stu-id="1988e-247">2</span></span>                                            |
| <span data-ttu-id="1988e-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-248">Search-Flags</span></span>           | <span data-ttu-id="1988e-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1988e-249">0x00000000</span></span>                                   |
| <span data-ttu-id="1988e-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-250">System-Flags</span></span>           | <span data-ttu-id="1988e-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1988e-251">0x00000010</span></span>                                   |
| <span data-ttu-id="1988e-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1988e-252">Classes used in</span></span>        | [<span data-ttu-id="1988e-253">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="1988e-253">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1988e-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1988e-254">Windows Server 2012</span></span>



| <span data-ttu-id="1988e-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="1988e-255">Entry</span></span> | <span data-ttu-id="1988e-256">Значение</span><span class="sxs-lookup"><span data-stu-id="1988e-256">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1988e-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1988e-257">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1988e-258">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1988e-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="1988e-259">System-Only</span></span>            | <span data-ttu-id="1988e-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-260">False</span></span>                                        |
| <span data-ttu-id="1988e-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1988e-261">Is-Single-Valued</span></span>       | <span data-ttu-id="1988e-262">True</span><span class="sxs-lookup"><span data-stu-id="1988e-262">True</span></span>                                         |
| <span data-ttu-id="1988e-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1988e-263">Is Indexed</span></span>             | <span data-ttu-id="1988e-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="1988e-264">False</span></span>                                        |
| <span data-ttu-id="1988e-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1988e-265">In Global Catalog</span></span>      | <span data-ttu-id="1988e-266">True</span><span class="sxs-lookup"><span data-stu-id="1988e-266">True</span></span>                                         |
| <span data-ttu-id="1988e-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1988e-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="1988e-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1988e-268">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1988e-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1988e-269">Range-Lower</span></span>            | <span data-ttu-id="1988e-270">0</span><span class="sxs-lookup"><span data-stu-id="1988e-270">0</span></span>                                            |
| <span data-ttu-id="1988e-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1988e-271">Range-Upper</span></span>            | <span data-ttu-id="1988e-272">2</span><span class="sxs-lookup"><span data-stu-id="1988e-272">2</span></span>                                            |
| <span data-ttu-id="1988e-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-273">Search-Flags</span></span>           | <span data-ttu-id="1988e-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1988e-274">0x00000000</span></span>                                   |
| <span data-ttu-id="1988e-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1988e-275">System-Flags</span></span>           | <span data-ttu-id="1988e-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1988e-276">0x00000010</span></span>                                   |
| <span data-ttu-id="1988e-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1988e-277">Classes used in</span></span>        | [<span data-ttu-id="1988e-278">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="1988e-278">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





