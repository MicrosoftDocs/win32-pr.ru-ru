---
title: Атрибут MSMQ-Journal
description: Указывает, должны ли сообщения, полученные в виде очереди, храниться в журнале.
ms.assetid: fb1f73eb-57f4-413f-bd7a-9dfd5e5c797f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MSMQ-Journal
- Схема AD атрибута Мсмкжаурнал
topic_type:
- apiref
api_name:
- MSMQ-Journal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a28e7740e41f8209e37345e934a36d10512bc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655149"
---
# <a name="msmq-journal-attribute"></a><span data-ttu-id="c442b-105">Атрибут MSMQ-Journal</span><span class="sxs-lookup"><span data-stu-id="c442b-105">MSMQ-Journal attribute</span></span>

<span data-ttu-id="c442b-106">Указывает, должны ли сообщения, полученные в виде очереди, храниться в журнале.</span><span class="sxs-lookup"><span data-stu-id="c442b-106">Indicates whether messages retrieved form the queue should be kept in journal.</span></span>



| <span data-ttu-id="c442b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-107">Entry</span></span> | <span data-ttu-id="c442b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c442b-109">CN</span><span class="sxs-lookup"><span data-stu-id="c442b-109">CN</span></span>                | <span data-ttu-id="c442b-110">MSMQ-Journal</span><span class="sxs-lookup"><span data-stu-id="c442b-110">MSMQ-Journal</span></span>                         |
| <span data-ttu-id="c442b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c442b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c442b-112">мсмкжаурнал</span><span class="sxs-lookup"><span data-stu-id="c442b-112">mSMQJournal</span></span>                          |
| <span data-ttu-id="c442b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c442b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="c442b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c442b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c442b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c442b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c442b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-116">Attribute-Id</span></span>      | <span data-ttu-id="c442b-117">1.2.840.113556.1.4.918</span><span class="sxs-lookup"><span data-stu-id="c442b-117">1.2.840.113556.1.4.918</span></span>               |
| <span data-ttu-id="c442b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c442b-118">System-Id-Guid</span></span>    | <span data-ttu-id="c442b-119">9a0dc321-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c442b-119">9a0dc321-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="c442b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c442b-120">Syntax</span></span>            | [<span data-ttu-id="c442b-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="c442b-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c442b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c442b-122">Implementations</span></span>

-   [<span data-ttu-id="c442b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c442b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c442b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c442b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c442b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c442b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c442b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c442b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c442b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c442b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c442b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c442b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c442b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c442b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c442b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-130">Entry</span></span> | <span data-ttu-id="c442b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c442b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c442b-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c442b-134">System-Only</span></span>            | <span data-ttu-id="c442b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-135">False</span></span>                                        |
| <span data-ttu-id="c442b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c442b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c442b-137">True</span><span class="sxs-lookup"><span data-stu-id="c442b-137">True</span></span>                                         |
| <span data-ttu-id="c442b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c442b-138">Is Indexed</span></span>             | <span data-ttu-id="c442b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-139">False</span></span>                                        |
| <span data-ttu-id="c442b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c442b-140">In Global Catalog</span></span>      | <span data-ttu-id="c442b-141">True</span><span class="sxs-lookup"><span data-stu-id="c442b-141">True</span></span>                                         |
| <span data-ttu-id="c442b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c442b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c442b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c442b-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c442b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c442b-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c442b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c442b-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c442b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-146">Search-Flags</span></span>           | <span data-ttu-id="c442b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c442b-147">0x00000000</span></span>                                   |
| <span data-ttu-id="c442b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-148">System-Flags</span></span>           | <span data-ttu-id="c442b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c442b-149">0x00000010</span></span>                                   |
| <span data-ttu-id="c442b-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c442b-150">Classes used in</span></span>        | [<span data-ttu-id="c442b-151">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c442b-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c442b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c442b-152">Windows Server 2003</span></span>



| <span data-ttu-id="c442b-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-153">Entry</span></span> | <span data-ttu-id="c442b-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c442b-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c442b-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c442b-157">System-Only</span></span>            | <span data-ttu-id="c442b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-158">False</span></span>                                        |
| <span data-ttu-id="c442b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c442b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c442b-160">True</span><span class="sxs-lookup"><span data-stu-id="c442b-160">True</span></span>                                         |
| <span data-ttu-id="c442b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c442b-161">Is Indexed</span></span>             | <span data-ttu-id="c442b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-162">False</span></span>                                        |
| <span data-ttu-id="c442b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c442b-163">In Global Catalog</span></span>      | <span data-ttu-id="c442b-164">True</span><span class="sxs-lookup"><span data-stu-id="c442b-164">True</span></span>                                         |
| <span data-ttu-id="c442b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c442b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c442b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c442b-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c442b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c442b-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c442b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c442b-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c442b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-169">Search-Flags</span></span>           | <span data-ttu-id="c442b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c442b-170">0x00000000</span></span>                                   |
| <span data-ttu-id="c442b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-171">System-Flags</span></span>           | <span data-ttu-id="c442b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c442b-172">0x00000010</span></span>                                   |
| <span data-ttu-id="c442b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c442b-173">Classes used in</span></span>        | [<span data-ttu-id="c442b-174">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c442b-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c442b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c442b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c442b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-176">Entry</span></span> | <span data-ttu-id="c442b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c442b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c442b-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c442b-180">System-Only</span></span>            | <span data-ttu-id="c442b-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-181">False</span></span>                                        |
| <span data-ttu-id="c442b-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c442b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c442b-183">True</span><span class="sxs-lookup"><span data-stu-id="c442b-183">True</span></span>                                         |
| <span data-ttu-id="c442b-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c442b-184">Is Indexed</span></span>             | <span data-ttu-id="c442b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-185">False</span></span>                                        |
| <span data-ttu-id="c442b-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c442b-186">In Global Catalog</span></span>      | <span data-ttu-id="c442b-187">True</span><span class="sxs-lookup"><span data-stu-id="c442b-187">True</span></span>                                         |
| <span data-ttu-id="c442b-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c442b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c442b-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c442b-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c442b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c442b-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c442b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c442b-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c442b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-192">Search-Flags</span></span>           | <span data-ttu-id="c442b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c442b-193">0x00000000</span></span>                                   |
| <span data-ttu-id="c442b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-194">System-Flags</span></span>           | <span data-ttu-id="c442b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c442b-195">0x00000010</span></span>                                   |
| <span data-ttu-id="c442b-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c442b-196">Classes used in</span></span>        | [<span data-ttu-id="c442b-197">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c442b-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c442b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c442b-198">Windows Server 2008</span></span>



| <span data-ttu-id="c442b-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-199">Entry</span></span> | <span data-ttu-id="c442b-200">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c442b-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c442b-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c442b-203">System-Only</span></span>            | <span data-ttu-id="c442b-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-204">False</span></span>                                        |
| <span data-ttu-id="c442b-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c442b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c442b-206">True</span><span class="sxs-lookup"><span data-stu-id="c442b-206">True</span></span>                                         |
| <span data-ttu-id="c442b-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c442b-207">Is Indexed</span></span>             | <span data-ttu-id="c442b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-208">False</span></span>                                        |
| <span data-ttu-id="c442b-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c442b-209">In Global Catalog</span></span>      | <span data-ttu-id="c442b-210">True</span><span class="sxs-lookup"><span data-stu-id="c442b-210">True</span></span>                                         |
| <span data-ttu-id="c442b-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c442b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c442b-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c442b-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c442b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c442b-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c442b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c442b-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c442b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-215">Search-Flags</span></span>           | <span data-ttu-id="c442b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c442b-216">0x00000000</span></span>                                   |
| <span data-ttu-id="c442b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-217">System-Flags</span></span>           | <span data-ttu-id="c442b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c442b-218">0x00000010</span></span>                                   |
| <span data-ttu-id="c442b-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c442b-219">Classes used in</span></span>        | [<span data-ttu-id="c442b-220">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c442b-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c442b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c442b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c442b-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-222">Entry</span></span> | <span data-ttu-id="c442b-223">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c442b-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c442b-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c442b-226">System-Only</span></span>            | <span data-ttu-id="c442b-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-227">False</span></span>                                        |
| <span data-ttu-id="c442b-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c442b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c442b-229">True</span><span class="sxs-lookup"><span data-stu-id="c442b-229">True</span></span>                                         |
| <span data-ttu-id="c442b-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c442b-230">Is Indexed</span></span>             | <span data-ttu-id="c442b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-231">False</span></span>                                        |
| <span data-ttu-id="c442b-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c442b-232">In Global Catalog</span></span>      | <span data-ttu-id="c442b-233">True</span><span class="sxs-lookup"><span data-stu-id="c442b-233">True</span></span>                                         |
| <span data-ttu-id="c442b-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c442b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c442b-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c442b-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c442b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c442b-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c442b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c442b-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c442b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-238">Search-Flags</span></span>           | <span data-ttu-id="c442b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c442b-239">0x00000000</span></span>                                   |
| <span data-ttu-id="c442b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-240">System-Flags</span></span>           | <span data-ttu-id="c442b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c442b-241">0x00000010</span></span>                                   |
| <span data-ttu-id="c442b-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c442b-242">Classes used in</span></span>        | [<span data-ttu-id="c442b-243">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c442b-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c442b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c442b-244">Windows Server 2012</span></span>



| <span data-ttu-id="c442b-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="c442b-245">Entry</span></span> | <span data-ttu-id="c442b-246">Значение</span><span class="sxs-lookup"><span data-stu-id="c442b-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c442b-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c442b-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c442b-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c442b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c442b-249">System-Only</span></span>            | <span data-ttu-id="c442b-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-250">False</span></span>                                        |
| <span data-ttu-id="c442b-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c442b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c442b-252">True</span><span class="sxs-lookup"><span data-stu-id="c442b-252">True</span></span>                                         |
| <span data-ttu-id="c442b-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c442b-253">Is Indexed</span></span>             | <span data-ttu-id="c442b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="c442b-254">False</span></span>                                        |
| <span data-ttu-id="c442b-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c442b-255">In Global Catalog</span></span>      | <span data-ttu-id="c442b-256">True</span><span class="sxs-lookup"><span data-stu-id="c442b-256">True</span></span>                                         |
| <span data-ttu-id="c442b-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c442b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c442b-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c442b-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c442b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c442b-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c442b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c442b-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c442b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-261">Search-Flags</span></span>           | <span data-ttu-id="c442b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c442b-262">0x00000000</span></span>                                   |
| <span data-ttu-id="c442b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c442b-263">System-Flags</span></span>           | <span data-ttu-id="c442b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c442b-264">0x00000010</span></span>                                   |
| <span data-ttu-id="c442b-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c442b-265">Classes used in</span></span>        | [<span data-ttu-id="c442b-266">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c442b-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





