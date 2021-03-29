---
title: MSMQ — атрибут базового приоритета
description: Базовый приоритет сообщений, переданных в эту очередь.
ms.assetid: bcb2b13d-67f0-44d1-ae2c-129528fdf36d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута с базовым приоритетом MSMQ
- Схема AD атрибута Мсмкбасеприорити
topic_type:
- apiref
api_name:
- MSMQ-Base-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ea41f559b6fe9c9ef3dd43aed8ad5df3809702
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989680"
---
# <a name="msmq-base-priority-attribute"></a><span data-ttu-id="69c3d-105">MSMQ — атрибут базового приоритета</span><span class="sxs-lookup"><span data-stu-id="69c3d-105">MSMQ-Base-Priority attribute</span></span>

<span data-ttu-id="69c3d-106">Базовый приоритет сообщений, переданных в эту очередь.</span><span class="sxs-lookup"><span data-stu-id="69c3d-106">The base priority of messages transmitted to this queue.</span></span>



| <span data-ttu-id="69c3d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-107">Entry</span></span> | <span data-ttu-id="69c3d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="69c3d-109">CN</span><span class="sxs-lookup"><span data-stu-id="69c3d-109">CN</span></span>                | <span data-ttu-id="69c3d-110">MSMQ — базовый приоритет</span><span class="sxs-lookup"><span data-stu-id="69c3d-110">MSMQ-Base-Priority</span></span>                   |
| <span data-ttu-id="69c3d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="69c3d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69c3d-112">мсмкбасеприорити</span><span class="sxs-lookup"><span data-stu-id="69c3d-112">mSMQBasePriority</span></span>                     |
| <span data-ttu-id="69c3d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="69c3d-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="69c3d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="69c3d-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="69c3d-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="69c3d-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="69c3d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-116">Attribute-Id</span></span>      | <span data-ttu-id="69c3d-117">1.2.840.113556.1.4.920</span><span class="sxs-lookup"><span data-stu-id="69c3d-117">1.2.840.113556.1.4.920</span></span>               |
| <span data-ttu-id="69c3d-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="69c3d-118">System-Id-Guid</span></span>    | <span data-ttu-id="69c3d-119">9a0dc323-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="69c3d-119">9a0dc323-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="69c3d-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69c3d-120">Syntax</span></span>            | [<span data-ttu-id="69c3d-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="69c3d-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="69c3d-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="69c3d-122">Implementations</span></span>

-   [<span data-ttu-id="69c3d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69c3d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69c3d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69c3d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69c3d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69c3d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69c3d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69c3d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69c3d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69c3d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69c3d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69c3d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="69c3d-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-130">Entry</span></span> | <span data-ttu-id="69c3d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69c3d-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69c3d-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-134">System-Only</span></span>            | <span data-ttu-id="69c3d-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-135">False</span></span>                                        |
| <span data-ttu-id="69c3d-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69c3d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-137">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-137">True</span></span>                                         |
| <span data-ttu-id="69c3d-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69c3d-138">Is Indexed</span></span>             | <span data-ttu-id="69c3d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-139">False</span></span>                                        |
| <span data-ttu-id="69c3d-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69c3d-140">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-141">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-141">True</span></span>                                         |
| <span data-ttu-id="69c3d-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69c3d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69c3d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-146">Search-Flags</span></span>           | <span data-ttu-id="69c3d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-147">0x00000000</span></span>                                   |
| <span data-ttu-id="69c3d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-148">System-Flags</span></span>           | <span data-ttu-id="69c3d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-149">0x00000010</span></span>                                   |
| <span data-ttu-id="69c3d-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69c3d-150">Classes used in</span></span>        | [<span data-ttu-id="69c3d-151">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="69c3d-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69c3d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69c3d-152">Windows Server 2003</span></span>



| <span data-ttu-id="69c3d-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-153">Entry</span></span> | <span data-ttu-id="69c3d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69c3d-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69c3d-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-157">System-Only</span></span>            | <span data-ttu-id="69c3d-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-158">False</span></span>                                        |
| <span data-ttu-id="69c3d-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69c3d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-160">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-160">True</span></span>                                         |
| <span data-ttu-id="69c3d-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69c3d-161">Is Indexed</span></span>             | <span data-ttu-id="69c3d-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-162">False</span></span>                                        |
| <span data-ttu-id="69c3d-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69c3d-163">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-164">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-164">True</span></span>                                         |
| <span data-ttu-id="69c3d-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69c3d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69c3d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-169">Search-Flags</span></span>           | <span data-ttu-id="69c3d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-170">0x00000000</span></span>                                   |
| <span data-ttu-id="69c3d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-171">System-Flags</span></span>           | <span data-ttu-id="69c3d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-172">0x00000010</span></span>                                   |
| <span data-ttu-id="69c3d-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69c3d-173">Classes used in</span></span>        | [<span data-ttu-id="69c3d-174">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="69c3d-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69c3d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69c3d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69c3d-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-176">Entry</span></span> | <span data-ttu-id="69c3d-177">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69c3d-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69c3d-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-180">System-Only</span></span>            | <span data-ttu-id="69c3d-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-181">False</span></span>                                        |
| <span data-ttu-id="69c3d-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69c3d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-183">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-183">True</span></span>                                         |
| <span data-ttu-id="69c3d-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69c3d-184">Is Indexed</span></span>             | <span data-ttu-id="69c3d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-185">False</span></span>                                        |
| <span data-ttu-id="69c3d-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69c3d-186">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-187">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-187">True</span></span>                                         |
| <span data-ttu-id="69c3d-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69c3d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69c3d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-192">Search-Flags</span></span>           | <span data-ttu-id="69c3d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-193">0x00000000</span></span>                                   |
| <span data-ttu-id="69c3d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-194">System-Flags</span></span>           | <span data-ttu-id="69c3d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-195">0x00000010</span></span>                                   |
| <span data-ttu-id="69c3d-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69c3d-196">Classes used in</span></span>        | [<span data-ttu-id="69c3d-197">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="69c3d-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69c3d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69c3d-198">Windows Server 2008</span></span>



| <span data-ttu-id="69c3d-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-199">Entry</span></span> | <span data-ttu-id="69c3d-200">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69c3d-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69c3d-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-203">System-Only</span></span>            | <span data-ttu-id="69c3d-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-204">False</span></span>                                        |
| <span data-ttu-id="69c3d-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69c3d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-206">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-206">True</span></span>                                         |
| <span data-ttu-id="69c3d-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69c3d-207">Is Indexed</span></span>             | <span data-ttu-id="69c3d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-208">False</span></span>                                        |
| <span data-ttu-id="69c3d-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69c3d-209">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-210">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-210">True</span></span>                                         |
| <span data-ttu-id="69c3d-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69c3d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69c3d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-215">Search-Flags</span></span>           | <span data-ttu-id="69c3d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-216">0x00000000</span></span>                                   |
| <span data-ttu-id="69c3d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-217">System-Flags</span></span>           | <span data-ttu-id="69c3d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-218">0x00000010</span></span>                                   |
| <span data-ttu-id="69c3d-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69c3d-219">Classes used in</span></span>        | [<span data-ttu-id="69c3d-220">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="69c3d-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69c3d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69c3d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69c3d-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-222">Entry</span></span> | <span data-ttu-id="69c3d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69c3d-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69c3d-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-226">System-Only</span></span>            | <span data-ttu-id="69c3d-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-227">False</span></span>                                        |
| <span data-ttu-id="69c3d-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69c3d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-229">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-229">True</span></span>                                         |
| <span data-ttu-id="69c3d-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69c3d-230">Is Indexed</span></span>             | <span data-ttu-id="69c3d-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-231">False</span></span>                                        |
| <span data-ttu-id="69c3d-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69c3d-232">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-233">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-233">True</span></span>                                         |
| <span data-ttu-id="69c3d-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69c3d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69c3d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-238">Search-Flags</span></span>           | <span data-ttu-id="69c3d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-239">0x00000000</span></span>                                   |
| <span data-ttu-id="69c3d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-240">System-Flags</span></span>           | <span data-ttu-id="69c3d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-241">0x00000010</span></span>                                   |
| <span data-ttu-id="69c3d-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69c3d-242">Classes used in</span></span>        | [<span data-ttu-id="69c3d-243">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="69c3d-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69c3d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69c3d-244">Windows Server 2012</span></span>



| <span data-ttu-id="69c3d-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="69c3d-245">Entry</span></span> | <span data-ttu-id="69c3d-246">Значение</span><span class="sxs-lookup"><span data-stu-id="69c3d-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69c3d-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="69c3d-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69c3d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-249">System-Only</span></span>            | <span data-ttu-id="69c3d-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-250">False</span></span>                                        |
| <span data-ttu-id="69c3d-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="69c3d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-252">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-252">True</span></span>                                         |
| <span data-ttu-id="69c3d-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="69c3d-253">Is Indexed</span></span>             | <span data-ttu-id="69c3d-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="69c3d-254">False</span></span>                                        |
| <span data-ttu-id="69c3d-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="69c3d-255">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-256">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-256">True</span></span>                                         |
| <span data-ttu-id="69c3d-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="69c3d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69c3d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69c3d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-261">Search-Flags</span></span>           | <span data-ttu-id="69c3d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-262">0x00000000</span></span>                                   |
| <span data-ttu-id="69c3d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-263">System-Flags</span></span>           | <span data-ttu-id="69c3d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-264">0x00000010</span></span>                                   |
| <span data-ttu-id="69c3d-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="69c3d-265">Classes used in</span></span>        | [<span data-ttu-id="69c3d-266">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="69c3d-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





