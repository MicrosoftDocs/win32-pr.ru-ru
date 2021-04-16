---
title: Атрибут MSMQ-Queue-Name-ext
description: Содержит суффикс имени очереди (если таковой имеется).
ms.assetid: 24194fef-410b-437f-9bef-edb0b2be2e24
ms.tgt_platform: multiple
keywords:
- Служба MSMQ-Queue-Name-ext атрибут AD
- Схема AD атрибута Мсмккуеуенамикст
topic_type:
- apiref
api_name:
- MSMQ-Queue-Name-Ext
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77bd0ccfffa00d43d73dd6b2bca94bd25bcde2e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655146"
---
# <a name="msmq-queue-name-ext-attribute"></a><span data-ttu-id="e6ff0-105">Атрибут MSMQ-Queue-Name-ext</span><span class="sxs-lookup"><span data-stu-id="e6ff0-105">MSMQ-Queue-Name-Ext attribute</span></span>

<span data-ttu-id="e6ff0-106">Содержит суффикс имени очереди (если таковой имеется).</span><span class="sxs-lookup"><span data-stu-id="e6ff0-106">Contains the suffix of the queue name (if there is one).</span></span>



| <span data-ttu-id="e6ff0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-107">Entry</span></span> | <span data-ttu-id="e6ff0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e6ff0-109">CN</span><span class="sxs-lookup"><span data-stu-id="e6ff0-109">CN</span></span>                | <span data-ttu-id="e6ff0-110">MSMQ-Queue-Name-ext</span><span class="sxs-lookup"><span data-stu-id="e6ff0-110">MSMQ-Queue-Name-Ext</span></span>                         |
| <span data-ttu-id="e6ff0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e6ff0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e6ff0-112">мсмккуеуенамикст</span><span class="sxs-lookup"><span data-stu-id="e6ff0-112">mSMQQueueNameExt</span></span>                            |
| <span data-ttu-id="e6ff0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e6ff0-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e6ff0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e6ff0-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e6ff0-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e6ff0-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e6ff0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-116">Attribute-Id</span></span>      | <span data-ttu-id="e6ff0-117">1.2.840.113556.1.4.1243</span><span class="sxs-lookup"><span data-stu-id="e6ff0-117">1.2.840.113556.1.4.1243</span></span>                     |
| <span data-ttu-id="e6ff0-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e6ff0-118">System-Id-Guid</span></span>    | <span data-ttu-id="e6ff0-119">2df90d87-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="e6ff0-119">2df90d87-009f-11d2-aa4c-00c04fd7d83a</span></span>        |
| <span data-ttu-id="e6ff0-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6ff0-120">Syntax</span></span>            | [<span data-ttu-id="e6ff0-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e6ff0-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e6ff0-122">Implementations</span></span>

-   [<span data-ttu-id="e6ff0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e6ff0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e6ff0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e6ff0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6ff0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6ff0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e6ff0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6ff0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e6ff0-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-130">Entry</span></span> | <span data-ttu-id="e6ff0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ff0-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff0-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff0-134">System-Only</span></span>            | <span data-ttu-id="e6ff0-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-135">False</span></span>                                        |
| <span data-ttu-id="e6ff0-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff0-137">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-137">True</span></span>                                         |
| <span data-ttu-id="e6ff0-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff0-138">Is Indexed</span></span>             | <span data-ttu-id="e6ff0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-139">False</span></span>                                        |
| <span data-ttu-id="e6ff0-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff0-140">In Global Catalog</span></span>      | <span data-ttu-id="e6ff0-141">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-141">True</span></span>                                         |
| <span data-ttu-id="e6ff0-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff0-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ff0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff0-144">Range-Lower</span></span>            | <span data-ttu-id="e6ff0-145">0</span><span class="sxs-lookup"><span data-stu-id="e6ff0-145">0</span></span>                                            |
| <span data-ttu-id="e6ff0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff0-146">Range-Upper</span></span>            | <span data-ttu-id="e6ff0-147">92</span><span class="sxs-lookup"><span data-stu-id="e6ff0-147">92</span></span>                                           |
| <span data-ttu-id="e6ff0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-148">Search-Flags</span></span>           | <span data-ttu-id="e6ff0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff0-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ff0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-150">System-Flags</span></span>           | <span data-ttu-id="e6ff0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff0-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ff0-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff0-152">Classes used in</span></span>        | [<span data-ttu-id="e6ff0-153">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-153">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e6ff0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6ff0-154">Windows Server 2003</span></span>



| <span data-ttu-id="e6ff0-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-155">Entry</span></span> | <span data-ttu-id="e6ff0-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ff0-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff0-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff0-159">System-Only</span></span>            | <span data-ttu-id="e6ff0-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-160">False</span></span>                                        |
| <span data-ttu-id="e6ff0-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff0-162">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-162">True</span></span>                                         |
| <span data-ttu-id="e6ff0-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff0-163">Is Indexed</span></span>             | <span data-ttu-id="e6ff0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-164">False</span></span>                                        |
| <span data-ttu-id="e6ff0-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff0-165">In Global Catalog</span></span>      | <span data-ttu-id="e6ff0-166">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-166">True</span></span>                                         |
| <span data-ttu-id="e6ff0-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff0-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ff0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff0-169">Range-Lower</span></span>            | <span data-ttu-id="e6ff0-170">0</span><span class="sxs-lookup"><span data-stu-id="e6ff0-170">0</span></span>                                            |
| <span data-ttu-id="e6ff0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff0-171">Range-Upper</span></span>            | <span data-ttu-id="e6ff0-172">92</span><span class="sxs-lookup"><span data-stu-id="e6ff0-172">92</span></span>                                           |
| <span data-ttu-id="e6ff0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-173">Search-Flags</span></span>           | <span data-ttu-id="e6ff0-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff0-174">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ff0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-175">System-Flags</span></span>           | <span data-ttu-id="e6ff0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff0-176">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ff0-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff0-177">Classes used in</span></span>        | [<span data-ttu-id="e6ff0-178">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e6ff0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e6ff0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e6ff0-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-180">Entry</span></span> | <span data-ttu-id="e6ff0-181">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ff0-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff0-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff0-184">System-Only</span></span>            | <span data-ttu-id="e6ff0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-185">False</span></span>                                        |
| <span data-ttu-id="e6ff0-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff0-187">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-187">True</span></span>                                         |
| <span data-ttu-id="e6ff0-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff0-188">Is Indexed</span></span>             | <span data-ttu-id="e6ff0-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-189">False</span></span>                                        |
| <span data-ttu-id="e6ff0-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff0-190">In Global Catalog</span></span>      | <span data-ttu-id="e6ff0-191">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-191">True</span></span>                                         |
| <span data-ttu-id="e6ff0-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff0-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ff0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff0-194">Range-Lower</span></span>            | <span data-ttu-id="e6ff0-195">0</span><span class="sxs-lookup"><span data-stu-id="e6ff0-195">0</span></span>                                            |
| <span data-ttu-id="e6ff0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff0-196">Range-Upper</span></span>            | <span data-ttu-id="e6ff0-197">92</span><span class="sxs-lookup"><span data-stu-id="e6ff0-197">92</span></span>                                           |
| <span data-ttu-id="e6ff0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-198">Search-Flags</span></span>           | <span data-ttu-id="e6ff0-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff0-199">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ff0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-200">System-Flags</span></span>           | <span data-ttu-id="e6ff0-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff0-201">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ff0-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff0-202">Classes used in</span></span>        | [<span data-ttu-id="e6ff0-203">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-203">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e6ff0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ff0-204">Windows Server 2008</span></span>



| <span data-ttu-id="e6ff0-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-205">Entry</span></span> | <span data-ttu-id="e6ff0-206">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-206">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ff0-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff0-207">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-208">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff0-209">System-Only</span></span>            | <span data-ttu-id="e6ff0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-210">False</span></span>                                        |
| <span data-ttu-id="e6ff0-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff0-212">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-212">True</span></span>                                         |
| <span data-ttu-id="e6ff0-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff0-213">Is Indexed</span></span>             | <span data-ttu-id="e6ff0-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-214">False</span></span>                                        |
| <span data-ttu-id="e6ff0-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff0-215">In Global Catalog</span></span>      | <span data-ttu-id="e6ff0-216">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-216">True</span></span>                                         |
| <span data-ttu-id="e6ff0-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff0-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-218">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ff0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff0-219">Range-Lower</span></span>            | <span data-ttu-id="e6ff0-220">0</span><span class="sxs-lookup"><span data-stu-id="e6ff0-220">0</span></span>                                            |
| <span data-ttu-id="e6ff0-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff0-221">Range-Upper</span></span>            | <span data-ttu-id="e6ff0-222">92</span><span class="sxs-lookup"><span data-stu-id="e6ff0-222">92</span></span>                                           |
| <span data-ttu-id="e6ff0-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-223">Search-Flags</span></span>           | <span data-ttu-id="e6ff0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff0-224">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ff0-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-225">System-Flags</span></span>           | <span data-ttu-id="e6ff0-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff0-226">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ff0-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff0-227">Classes used in</span></span>        | [<span data-ttu-id="e6ff0-228">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-228">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6ff0-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6ff0-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6ff0-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-230">Entry</span></span> | <span data-ttu-id="e6ff0-231">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-231">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ff0-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff0-232">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-233">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff0-234">System-Only</span></span>            | <span data-ttu-id="e6ff0-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-235">False</span></span>                                        |
| <span data-ttu-id="e6ff0-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff0-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff0-237">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-237">True</span></span>                                         |
| <span data-ttu-id="e6ff0-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff0-238">Is Indexed</span></span>             | <span data-ttu-id="e6ff0-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-239">False</span></span>                                        |
| <span data-ttu-id="e6ff0-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff0-240">In Global Catalog</span></span>      | <span data-ttu-id="e6ff0-241">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-241">True</span></span>                                         |
| <span data-ttu-id="e6ff0-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff0-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff0-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-243">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ff0-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff0-244">Range-Lower</span></span>            | <span data-ttu-id="e6ff0-245">0</span><span class="sxs-lookup"><span data-stu-id="e6ff0-245">0</span></span>                                            |
| <span data-ttu-id="e6ff0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff0-246">Range-Upper</span></span>            | <span data-ttu-id="e6ff0-247">92</span><span class="sxs-lookup"><span data-stu-id="e6ff0-247">92</span></span>                                           |
| <span data-ttu-id="e6ff0-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-248">Search-Flags</span></span>           | <span data-ttu-id="e6ff0-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff0-249">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ff0-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-250">System-Flags</span></span>           | <span data-ttu-id="e6ff0-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff0-251">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ff0-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff0-252">Classes used in</span></span>        | [<span data-ttu-id="e6ff0-253">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-253">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6ff0-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6ff0-254">Windows Server 2012</span></span>



| <span data-ttu-id="e6ff0-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff0-255">Entry</span></span> | <span data-ttu-id="e6ff0-256">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff0-256">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ff0-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff0-257">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff0-258">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ff0-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff0-259">System-Only</span></span>            | <span data-ttu-id="e6ff0-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-260">False</span></span>                                        |
| <span data-ttu-id="e6ff0-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff0-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff0-262">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-262">True</span></span>                                         |
| <span data-ttu-id="e6ff0-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff0-263">Is Indexed</span></span>             | <span data-ttu-id="e6ff0-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff0-264">False</span></span>                                        |
| <span data-ttu-id="e6ff0-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff0-265">In Global Catalog</span></span>      | <span data-ttu-id="e6ff0-266">True</span><span class="sxs-lookup"><span data-stu-id="e6ff0-266">True</span></span>                                         |
| <span data-ttu-id="e6ff0-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff0-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff0-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-268">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ff0-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff0-269">Range-Lower</span></span>            | <span data-ttu-id="e6ff0-270">0</span><span class="sxs-lookup"><span data-stu-id="e6ff0-270">0</span></span>                                            |
| <span data-ttu-id="e6ff0-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff0-271">Range-Upper</span></span>            | <span data-ttu-id="e6ff0-272">92</span><span class="sxs-lookup"><span data-stu-id="e6ff0-272">92</span></span>                                           |
| <span data-ttu-id="e6ff0-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-273">Search-Flags</span></span>           | <span data-ttu-id="e6ff0-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff0-274">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ff0-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff0-275">System-Flags</span></span>           | <span data-ttu-id="e6ff0-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff0-276">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ff0-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff0-277">Classes used in</span></span>        | [<span data-ttu-id="e6ff0-278">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="e6ff0-278">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





