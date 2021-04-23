---
title: Атрибут MSMQ-Authenticate
description: Указывает, принимает ли очередь только сообщения, прошедшие проверку подлинности.
ms.assetid: f03316e3-daae-4d1e-b135-8b4c3c2765b2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MSMQ-Authenticate
- Схема AD атрибута Мсмкаусентикате
topic_type:
- apiref
api_name:
- MSMQ-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a2d3744a01834cde181f5cfcf3804a0c765415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536242"
---
# <a name="msmq-authenticate-attribute"></a><span data-ttu-id="c822c-105">Атрибут MSMQ-Authenticate</span><span class="sxs-lookup"><span data-stu-id="c822c-105">MSMQ-Authenticate attribute</span></span>

<span data-ttu-id="c822c-106">Указывает, принимает ли очередь только сообщения, прошедшие проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="c822c-106">Indicates whether the queue accepts only authenticated messages.</span></span>



| <span data-ttu-id="c822c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-107">Entry</span></span> | <span data-ttu-id="c822c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c822c-109">CN</span><span class="sxs-lookup"><span data-stu-id="c822c-109">CN</span></span>                | <span data-ttu-id="c822c-110">MSMQ-Authenticate</span><span class="sxs-lookup"><span data-stu-id="c822c-110">MSMQ-Authenticate</span></span>                    |
| <span data-ttu-id="c822c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c822c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c822c-112">мсмкаусентикате</span><span class="sxs-lookup"><span data-stu-id="c822c-112">mSMQAuthenticate</span></span>                     |
| <span data-ttu-id="c822c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c822c-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="c822c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c822c-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c822c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c822c-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c822c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-116">Attribute-Id</span></span>      | <span data-ttu-id="c822c-117">1.2.840.113556.1.4.923</span><span class="sxs-lookup"><span data-stu-id="c822c-117">1.2.840.113556.1.4.923</span></span>               |
| <span data-ttu-id="c822c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c822c-118">System-Id-Guid</span></span>    | <span data-ttu-id="c822c-119">9a0dc326-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c822c-119">9a0dc326-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="c822c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c822c-120">Syntax</span></span>            | [<span data-ttu-id="c822c-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="c822c-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c822c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c822c-122">Implementations</span></span>

-   [<span data-ttu-id="c822c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c822c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c822c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c822c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c822c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c822c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c822c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c822c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c822c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c822c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c822c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c822c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c822c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c822c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c822c-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-130">Entry</span></span> | <span data-ttu-id="c822c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c822c-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c822c-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c822c-134">System-Only</span></span>            | <span data-ttu-id="c822c-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-135">False</span></span>                                        |
| <span data-ttu-id="c822c-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c822c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c822c-137">True</span><span class="sxs-lookup"><span data-stu-id="c822c-137">True</span></span>                                         |
| <span data-ttu-id="c822c-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c822c-138">Is Indexed</span></span>             | <span data-ttu-id="c822c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-139">False</span></span>                                        |
| <span data-ttu-id="c822c-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c822c-140">In Global Catalog</span></span>      | <span data-ttu-id="c822c-141">True</span><span class="sxs-lookup"><span data-stu-id="c822c-141">True</span></span>                                         |
| <span data-ttu-id="c822c-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c822c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c822c-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c822c-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c822c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c822c-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c822c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c822c-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c822c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-146">Search-Flags</span></span>           | <span data-ttu-id="c822c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c822c-147">0x00000000</span></span>                                   |
| <span data-ttu-id="c822c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-148">System-Flags</span></span>           | <span data-ttu-id="c822c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c822c-149">0x00000010</span></span>                                   |
| <span data-ttu-id="c822c-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c822c-150">Classes used in</span></span>        | [<span data-ttu-id="c822c-151">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c822c-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c822c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c822c-152">Windows Server 2003</span></span>



| <span data-ttu-id="c822c-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-153">Entry</span></span> | <span data-ttu-id="c822c-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c822c-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c822c-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c822c-157">System-Only</span></span>            | <span data-ttu-id="c822c-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-158">False</span></span>                                        |
| <span data-ttu-id="c822c-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c822c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c822c-160">True</span><span class="sxs-lookup"><span data-stu-id="c822c-160">True</span></span>                                         |
| <span data-ttu-id="c822c-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c822c-161">Is Indexed</span></span>             | <span data-ttu-id="c822c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-162">False</span></span>                                        |
| <span data-ttu-id="c822c-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c822c-163">In Global Catalog</span></span>      | <span data-ttu-id="c822c-164">True</span><span class="sxs-lookup"><span data-stu-id="c822c-164">True</span></span>                                         |
| <span data-ttu-id="c822c-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c822c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c822c-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c822c-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c822c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c822c-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c822c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c822c-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c822c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-169">Search-Flags</span></span>           | <span data-ttu-id="c822c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c822c-170">0x00000000</span></span>                                   |
| <span data-ttu-id="c822c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-171">System-Flags</span></span>           | <span data-ttu-id="c822c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c822c-172">0x00000010</span></span>                                   |
| <span data-ttu-id="c822c-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c822c-173">Classes used in</span></span>        | [<span data-ttu-id="c822c-174">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c822c-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c822c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c822c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c822c-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-176">Entry</span></span> | <span data-ttu-id="c822c-177">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c822c-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c822c-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c822c-180">System-Only</span></span>            | <span data-ttu-id="c822c-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-181">False</span></span>                                        |
| <span data-ttu-id="c822c-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c822c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c822c-183">True</span><span class="sxs-lookup"><span data-stu-id="c822c-183">True</span></span>                                         |
| <span data-ttu-id="c822c-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c822c-184">Is Indexed</span></span>             | <span data-ttu-id="c822c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-185">False</span></span>                                        |
| <span data-ttu-id="c822c-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c822c-186">In Global Catalog</span></span>      | <span data-ttu-id="c822c-187">True</span><span class="sxs-lookup"><span data-stu-id="c822c-187">True</span></span>                                         |
| <span data-ttu-id="c822c-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c822c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c822c-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c822c-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c822c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c822c-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c822c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c822c-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c822c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-192">Search-Flags</span></span>           | <span data-ttu-id="c822c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c822c-193">0x00000000</span></span>                                   |
| <span data-ttu-id="c822c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-194">System-Flags</span></span>           | <span data-ttu-id="c822c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c822c-195">0x00000010</span></span>                                   |
| <span data-ttu-id="c822c-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c822c-196">Classes used in</span></span>        | [<span data-ttu-id="c822c-197">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c822c-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c822c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c822c-198">Windows Server 2008</span></span>



| <span data-ttu-id="c822c-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-199">Entry</span></span> | <span data-ttu-id="c822c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c822c-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c822c-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c822c-203">System-Only</span></span>            | <span data-ttu-id="c822c-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-204">False</span></span>                                        |
| <span data-ttu-id="c822c-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c822c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c822c-206">True</span><span class="sxs-lookup"><span data-stu-id="c822c-206">True</span></span>                                         |
| <span data-ttu-id="c822c-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c822c-207">Is Indexed</span></span>             | <span data-ttu-id="c822c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-208">False</span></span>                                        |
| <span data-ttu-id="c822c-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c822c-209">In Global Catalog</span></span>      | <span data-ttu-id="c822c-210">True</span><span class="sxs-lookup"><span data-stu-id="c822c-210">True</span></span>                                         |
| <span data-ttu-id="c822c-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c822c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c822c-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c822c-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c822c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c822c-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c822c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c822c-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c822c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-215">Search-Flags</span></span>           | <span data-ttu-id="c822c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c822c-216">0x00000000</span></span>                                   |
| <span data-ttu-id="c822c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-217">System-Flags</span></span>           | <span data-ttu-id="c822c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c822c-218">0x00000010</span></span>                                   |
| <span data-ttu-id="c822c-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c822c-219">Classes used in</span></span>        | [<span data-ttu-id="c822c-220">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c822c-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c822c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c822c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c822c-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-222">Entry</span></span> | <span data-ttu-id="c822c-223">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c822c-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c822c-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c822c-226">System-Only</span></span>            | <span data-ttu-id="c822c-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-227">False</span></span>                                        |
| <span data-ttu-id="c822c-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c822c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c822c-229">True</span><span class="sxs-lookup"><span data-stu-id="c822c-229">True</span></span>                                         |
| <span data-ttu-id="c822c-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c822c-230">Is Indexed</span></span>             | <span data-ttu-id="c822c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-231">False</span></span>                                        |
| <span data-ttu-id="c822c-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c822c-232">In Global Catalog</span></span>      | <span data-ttu-id="c822c-233">True</span><span class="sxs-lookup"><span data-stu-id="c822c-233">True</span></span>                                         |
| <span data-ttu-id="c822c-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c822c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c822c-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c822c-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c822c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c822c-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c822c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c822c-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c822c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-238">Search-Flags</span></span>           | <span data-ttu-id="c822c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c822c-239">0x00000000</span></span>                                   |
| <span data-ttu-id="c822c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-240">System-Flags</span></span>           | <span data-ttu-id="c822c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c822c-241">0x00000010</span></span>                                   |
| <span data-ttu-id="c822c-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c822c-242">Classes used in</span></span>        | [<span data-ttu-id="c822c-243">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c822c-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c822c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c822c-244">Windows Server 2012</span></span>



| <span data-ttu-id="c822c-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="c822c-245">Entry</span></span> | <span data-ttu-id="c822c-246">Значение</span><span class="sxs-lookup"><span data-stu-id="c822c-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c822c-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c822c-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c822c-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c822c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c822c-249">System-Only</span></span>            | <span data-ttu-id="c822c-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-250">False</span></span>                                        |
| <span data-ttu-id="c822c-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c822c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c822c-252">True</span><span class="sxs-lookup"><span data-stu-id="c822c-252">True</span></span>                                         |
| <span data-ttu-id="c822c-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c822c-253">Is Indexed</span></span>             | <span data-ttu-id="c822c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="c822c-254">False</span></span>                                        |
| <span data-ttu-id="c822c-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c822c-255">In Global Catalog</span></span>      | <span data-ttu-id="c822c-256">True</span><span class="sxs-lookup"><span data-stu-id="c822c-256">True</span></span>                                         |
| <span data-ttu-id="c822c-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c822c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c822c-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c822c-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c822c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c822c-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c822c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c822c-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c822c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-261">Search-Flags</span></span>           | <span data-ttu-id="c822c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c822c-262">0x00000000</span></span>                                   |
| <span data-ttu-id="c822c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c822c-263">System-Flags</span></span>           | <span data-ttu-id="c822c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c822c-264">0x00000010</span></span>                                   |
| <span data-ttu-id="c822c-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c822c-265">Classes used in</span></span>        | [<span data-ttu-id="c822c-266">**Очередь MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c822c-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





