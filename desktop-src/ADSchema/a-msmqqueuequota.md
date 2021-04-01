---
title: MSMQ — очередь — атрибут квоты
description: Квота сообщений очереди.
ms.assetid: 45a9d6f0-5cd7-414d-97c5-18a7e41a5062
ms.tgt_platform: multiple
keywords:
- Схема Active Directory для атрибута квоты MSMQ
- Схема AD атрибута Мсмккуеуекуота
topic_type:
- apiref
api_name:
- MSMQ-Queue-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70e2719b6bfe738a0bc6646716582e9dcc72fe7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804949"
---
# <a name="msmq-queue-quota-attribute"></a><span data-ttu-id="6fb1a-105">MSMQ — очередь — атрибут квоты</span><span class="sxs-lookup"><span data-stu-id="6fb1a-105">MSMQ-Queue-Quota attribute</span></span>

<span data-ttu-id="6fb1a-106">Квота сообщений очереди.</span><span class="sxs-lookup"><span data-stu-id="6fb1a-106">A message quota of the queue.</span></span>



| <span data-ttu-id="6fb1a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-107">Entry</span></span> | <span data-ttu-id="6fb1a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6fb1a-109">CN</span><span class="sxs-lookup"><span data-stu-id="6fb1a-109">CN</span></span>                | <span data-ttu-id="6fb1a-110">Очередь MSMQ — квота</span><span class="sxs-lookup"><span data-stu-id="6fb1a-110">MSMQ-Queue-Quota</span></span>                     |
| <span data-ttu-id="6fb1a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6fb1a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6fb1a-112">мсмккуеуекуота</span><span class="sxs-lookup"><span data-stu-id="6fb1a-112">mSMQQueueQuota</span></span>                       |
| <span data-ttu-id="6fb1a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6fb1a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="6fb1a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6fb1a-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6fb1a-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6fb1a-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6fb1a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-116">Attribute-Id</span></span>      | <span data-ttu-id="6fb1a-117">1.2.840.113556.1.4.962</span><span class="sxs-lookup"><span data-stu-id="6fb1a-117">1.2.840.113556.1.4.962</span></span>               |
| <span data-ttu-id="6fb1a-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6fb1a-118">System-Id-Guid</span></span>    | <span data-ttu-id="6fb1a-119">3f6b8e12-d57f-11d1-90a2-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="6fb1a-119">3f6b8e12-d57f-11d1-90a2-00c04fd91ab1</span></span> |
| <span data-ttu-id="6fb1a-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fb1a-120">Syntax</span></span>            | [<span data-ttu-id="6fb1a-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6fb1a-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6fb1a-122">Implementations</span></span>

-   [<span data-ttu-id="6fb1a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6fb1a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6fb1a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6fb1a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6fb1a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6fb1a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6fb1a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6fb1a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6fb1a-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-130">Entry</span></span> | <span data-ttu-id="6fb1a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6fb1a-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fb1a-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb1a-134">System-Only</span></span>            | <span data-ttu-id="6fb1a-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-135">False</span></span>                                        |
| <span data-ttu-id="6fb1a-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fb1a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb1a-137">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-137">True</span></span>                                         |
| <span data-ttu-id="6fb1a-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fb1a-138">Is Indexed</span></span>             | <span data-ttu-id="6fb1a-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-139">False</span></span>                                        |
| <span data-ttu-id="6fb1a-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fb1a-140">In Global Catalog</span></span>      | <span data-ttu-id="6fb1a-141">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-141">True</span></span>                                         |
| <span data-ttu-id="6fb1a-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fb1a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb1a-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fb1a-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6fb1a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb1a-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb1a-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-146">Search-Flags</span></span>           | <span data-ttu-id="6fb1a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb1a-147">0x00000000</span></span>                                   |
| <span data-ttu-id="6fb1a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-148">System-Flags</span></span>           | <span data-ttu-id="6fb1a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb1a-149">0x00000010</span></span>                                   |
| <span data-ttu-id="6fb1a-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fb1a-150">Classes used in</span></span>        | [<span data-ttu-id="6fb1a-151">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6fb1a-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6fb1a-152">Windows Server 2003</span></span>



| <span data-ttu-id="6fb1a-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-153">Entry</span></span> | <span data-ttu-id="6fb1a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6fb1a-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fb1a-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb1a-157">System-Only</span></span>            | <span data-ttu-id="6fb1a-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-158">False</span></span>                                        |
| <span data-ttu-id="6fb1a-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fb1a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb1a-160">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-160">True</span></span>                                         |
| <span data-ttu-id="6fb1a-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fb1a-161">Is Indexed</span></span>             | <span data-ttu-id="6fb1a-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-162">False</span></span>                                        |
| <span data-ttu-id="6fb1a-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fb1a-163">In Global Catalog</span></span>      | <span data-ttu-id="6fb1a-164">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-164">True</span></span>                                         |
| <span data-ttu-id="6fb1a-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fb1a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb1a-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fb1a-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6fb1a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb1a-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb1a-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-169">Search-Flags</span></span>           | <span data-ttu-id="6fb1a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb1a-170">0x00000000</span></span>                                   |
| <span data-ttu-id="6fb1a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-171">System-Flags</span></span>           | <span data-ttu-id="6fb1a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb1a-172">0x00000010</span></span>                                   |
| <span data-ttu-id="6fb1a-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fb1a-173">Classes used in</span></span>        | [<span data-ttu-id="6fb1a-174">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6fb1a-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6fb1a-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6fb1a-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-176">Entry</span></span> | <span data-ttu-id="6fb1a-177">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6fb1a-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fb1a-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb1a-180">System-Only</span></span>            | <span data-ttu-id="6fb1a-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-181">False</span></span>                                        |
| <span data-ttu-id="6fb1a-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fb1a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb1a-183">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-183">True</span></span>                                         |
| <span data-ttu-id="6fb1a-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fb1a-184">Is Indexed</span></span>             | <span data-ttu-id="6fb1a-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-185">False</span></span>                                        |
| <span data-ttu-id="6fb1a-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fb1a-186">In Global Catalog</span></span>      | <span data-ttu-id="6fb1a-187">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-187">True</span></span>                                         |
| <span data-ttu-id="6fb1a-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fb1a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb1a-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fb1a-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6fb1a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb1a-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb1a-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-192">Search-Flags</span></span>           | <span data-ttu-id="6fb1a-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb1a-193">0x00000000</span></span>                                   |
| <span data-ttu-id="6fb1a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-194">System-Flags</span></span>           | <span data-ttu-id="6fb1a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb1a-195">0x00000010</span></span>                                   |
| <span data-ttu-id="6fb1a-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fb1a-196">Classes used in</span></span>        | [<span data-ttu-id="6fb1a-197">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6fb1a-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fb1a-198">Windows Server 2008</span></span>



| <span data-ttu-id="6fb1a-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-199">Entry</span></span> | <span data-ttu-id="6fb1a-200">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6fb1a-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fb1a-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb1a-203">System-Only</span></span>            | <span data-ttu-id="6fb1a-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-204">False</span></span>                                        |
| <span data-ttu-id="6fb1a-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fb1a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb1a-206">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-206">True</span></span>                                         |
| <span data-ttu-id="6fb1a-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fb1a-207">Is Indexed</span></span>             | <span data-ttu-id="6fb1a-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-208">False</span></span>                                        |
| <span data-ttu-id="6fb1a-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fb1a-209">In Global Catalog</span></span>      | <span data-ttu-id="6fb1a-210">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-210">True</span></span>                                         |
| <span data-ttu-id="6fb1a-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fb1a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb1a-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fb1a-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6fb1a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb1a-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb1a-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-215">Search-Flags</span></span>           | <span data-ttu-id="6fb1a-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb1a-216">0x00000000</span></span>                                   |
| <span data-ttu-id="6fb1a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-217">System-Flags</span></span>           | <span data-ttu-id="6fb1a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb1a-218">0x00000010</span></span>                                   |
| <span data-ttu-id="6fb1a-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fb1a-219">Classes used in</span></span>        | [<span data-ttu-id="6fb1a-220">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6fb1a-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fb1a-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6fb1a-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-222">Entry</span></span> | <span data-ttu-id="6fb1a-223">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6fb1a-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fb1a-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb1a-226">System-Only</span></span>            | <span data-ttu-id="6fb1a-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-227">False</span></span>                                        |
| <span data-ttu-id="6fb1a-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fb1a-228">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb1a-229">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-229">True</span></span>                                         |
| <span data-ttu-id="6fb1a-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fb1a-230">Is Indexed</span></span>             | <span data-ttu-id="6fb1a-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-231">False</span></span>                                        |
| <span data-ttu-id="6fb1a-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fb1a-232">In Global Catalog</span></span>      | <span data-ttu-id="6fb1a-233">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-233">True</span></span>                                         |
| <span data-ttu-id="6fb1a-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fb1a-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb1a-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fb1a-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6fb1a-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb1a-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb1a-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-238">Search-Flags</span></span>           | <span data-ttu-id="6fb1a-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb1a-239">0x00000000</span></span>                                   |
| <span data-ttu-id="6fb1a-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-240">System-Flags</span></span>           | <span data-ttu-id="6fb1a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb1a-241">0x00000010</span></span>                                   |
| <span data-ttu-id="6fb1a-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fb1a-242">Classes used in</span></span>        | [<span data-ttu-id="6fb1a-243">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6fb1a-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fb1a-244">Windows Server 2012</span></span>



| <span data-ttu-id="6fb1a-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fb1a-245">Entry</span></span> | <span data-ttu-id="6fb1a-246">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb1a-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6fb1a-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fb1a-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb1a-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6fb1a-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb1a-249">System-Only</span></span>            | <span data-ttu-id="6fb1a-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-250">False</span></span>                                        |
| <span data-ttu-id="6fb1a-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fb1a-251">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb1a-252">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-252">True</span></span>                                         |
| <span data-ttu-id="6fb1a-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fb1a-253">Is Indexed</span></span>             | <span data-ttu-id="6fb1a-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fb1a-254">False</span></span>                                        |
| <span data-ttu-id="6fb1a-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fb1a-255">In Global Catalog</span></span>      | <span data-ttu-id="6fb1a-256">True</span><span class="sxs-lookup"><span data-stu-id="6fb1a-256">True</span></span>                                         |
| <span data-ttu-id="6fb1a-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fb1a-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb1a-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fb1a-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6fb1a-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb1a-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb1a-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6fb1a-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-261">Search-Flags</span></span>           | <span data-ttu-id="6fb1a-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb1a-262">0x00000000</span></span>                                   |
| <span data-ttu-id="6fb1a-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb1a-263">System-Flags</span></span>           | <span data-ttu-id="6fb1a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb1a-264">0x00000010</span></span>                                   |
| <span data-ttu-id="6fb1a-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fb1a-265">Classes used in</span></span>        | [<span data-ttu-id="6fb1a-266">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fb1a-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





