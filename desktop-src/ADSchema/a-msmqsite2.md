---
title: Атрибут MSMQ-Site-2
description: Различающееся имя второго сайта подключенной пары.
ms.assetid: 41d8246e-c713-41c3-a570-f906ba0ab857
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MSMQ-Site-2
- Схема AD атрибута mSMQSite2
topic_type:
- apiref
api_name:
- MSMQ-Site-2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4f852750cf7d7566e3106e24062ec1234ba0ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138603"
---
# <a name="msmq-site-2-attribute"></a><span data-ttu-id="e9aef-105">Атрибут MSMQ-Site-2</span><span class="sxs-lookup"><span data-stu-id="e9aef-105">MSMQ-Site-2 attribute</span></span>

<span data-ttu-id="e9aef-106">Различающееся имя второго сайта подключенной пары.</span><span class="sxs-lookup"><span data-stu-id="e9aef-106">The DN of the second site of a pair that are connected.</span></span>



| <span data-ttu-id="e9aef-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-107">Entry</span></span> | <span data-ttu-id="e9aef-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e9aef-109">CN</span><span class="sxs-lookup"><span data-stu-id="e9aef-109">CN</span></span>                | <span data-ttu-id="e9aef-110">MSMQ-Site-2</span><span class="sxs-lookup"><span data-stu-id="e9aef-110">MSMQ-Site-2</span></span>                             |
| <span data-ttu-id="e9aef-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e9aef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e9aef-112">mSMQSite2</span><span class="sxs-lookup"><span data-stu-id="e9aef-112">mSMQSite2</span></span>                               |
| <span data-ttu-id="e9aef-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e9aef-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e9aef-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e9aef-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="e9aef-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e9aef-115">Update Frequency</span></span>  | <span data-ttu-id="e9aef-116">При каждом создании строки MSMQ-site-Line.</span><span class="sxs-lookup"><span data-stu-id="e9aef-116">Each time an MSMQ-Site-Line is created.</span></span> |
| <span data-ttu-id="e9aef-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-117">Attribute-Id</span></span>      | <span data-ttu-id="e9aef-118">1.2.840.113556.1.4.944</span><span class="sxs-lookup"><span data-stu-id="e9aef-118">1.2.840.113556.1.4.944</span></span>                  |
| <span data-ttu-id="e9aef-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e9aef-119">System-Id-Guid</span></span>    | <span data-ttu-id="e9aef-120">9a0dc338-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="e9aef-120">9a0dc338-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="e9aef-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9aef-121">Syntax</span></span>            | [<span data-ttu-id="e9aef-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e9aef-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e9aef-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e9aef-123">Implementations</span></span>

-   [<span data-ttu-id="e9aef-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9aef-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9aef-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9aef-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9aef-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9aef-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9aef-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9aef-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9aef-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9aef-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9aef-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9aef-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9aef-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9aef-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e9aef-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-131">Entry</span></span> | <span data-ttu-id="e9aef-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9aef-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9aef-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9aef-135">System-Only</span></span>            | <span data-ttu-id="e9aef-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-136">False</span></span>                                               |
| <span data-ttu-id="e9aef-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9aef-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e9aef-138">True</span><span class="sxs-lookup"><span data-stu-id="e9aef-138">True</span></span>                                                |
| <span data-ttu-id="e9aef-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9aef-139">Is Indexed</span></span>             | <span data-ttu-id="e9aef-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-140">False</span></span>                                               |
| <span data-ttu-id="e9aef-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9aef-141">In Global Catalog</span></span>      | <span data-ttu-id="e9aef-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-142">False</span></span>                                               |
| <span data-ttu-id="e9aef-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9aef-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9aef-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9aef-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="e9aef-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9aef-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9aef-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-147">Search-Flags</span></span>           | <span data-ttu-id="e9aef-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9aef-148">0x00000000</span></span>                                          |
| <span data-ttu-id="e9aef-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-149">System-Flags</span></span>           | <span data-ttu-id="e9aef-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9aef-150">0x00000010</span></span>                                          |
| <span data-ttu-id="e9aef-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9aef-151">Classes used in</span></span>        | [<span data-ttu-id="e9aef-152">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="e9aef-152">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9aef-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9aef-153">Windows Server 2003</span></span>



| <span data-ttu-id="e9aef-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-154">Entry</span></span> | <span data-ttu-id="e9aef-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9aef-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9aef-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9aef-158">System-Only</span></span>            | <span data-ttu-id="e9aef-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-159">False</span></span>                                               |
| <span data-ttu-id="e9aef-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9aef-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e9aef-161">True</span><span class="sxs-lookup"><span data-stu-id="e9aef-161">True</span></span>                                                |
| <span data-ttu-id="e9aef-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9aef-162">Is Indexed</span></span>             | <span data-ttu-id="e9aef-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-163">False</span></span>                                               |
| <span data-ttu-id="e9aef-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9aef-164">In Global Catalog</span></span>      | <span data-ttu-id="e9aef-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-165">False</span></span>                                               |
| <span data-ttu-id="e9aef-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9aef-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9aef-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9aef-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="e9aef-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9aef-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9aef-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-170">Search-Flags</span></span>           | <span data-ttu-id="e9aef-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9aef-171">0x00000000</span></span>                                          |
| <span data-ttu-id="e9aef-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-172">System-Flags</span></span>           | <span data-ttu-id="e9aef-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9aef-173">0x00000010</span></span>                                          |
| <span data-ttu-id="e9aef-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9aef-174">Classes used in</span></span>        | [<span data-ttu-id="e9aef-175">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="e9aef-175">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9aef-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9aef-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9aef-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-177">Entry</span></span> | <span data-ttu-id="e9aef-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9aef-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9aef-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9aef-181">System-Only</span></span>            | <span data-ttu-id="e9aef-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-182">False</span></span>                                               |
| <span data-ttu-id="e9aef-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9aef-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e9aef-184">True</span><span class="sxs-lookup"><span data-stu-id="e9aef-184">True</span></span>                                                |
| <span data-ttu-id="e9aef-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9aef-185">Is Indexed</span></span>             | <span data-ttu-id="e9aef-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-186">False</span></span>                                               |
| <span data-ttu-id="e9aef-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9aef-187">In Global Catalog</span></span>      | <span data-ttu-id="e9aef-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-188">False</span></span>                                               |
| <span data-ttu-id="e9aef-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9aef-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9aef-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9aef-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="e9aef-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9aef-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9aef-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-193">Search-Flags</span></span>           | <span data-ttu-id="e9aef-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9aef-194">0x00000000</span></span>                                          |
| <span data-ttu-id="e9aef-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-195">System-Flags</span></span>           | <span data-ttu-id="e9aef-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9aef-196">0x00000010</span></span>                                          |
| <span data-ttu-id="e9aef-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9aef-197">Classes used in</span></span>        | [<span data-ttu-id="e9aef-198">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="e9aef-198">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9aef-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9aef-199">Windows Server 2008</span></span>



| <span data-ttu-id="e9aef-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-200">Entry</span></span> | <span data-ttu-id="e9aef-201">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9aef-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9aef-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9aef-204">System-Only</span></span>            | <span data-ttu-id="e9aef-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-205">False</span></span>                                               |
| <span data-ttu-id="e9aef-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9aef-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e9aef-207">True</span><span class="sxs-lookup"><span data-stu-id="e9aef-207">True</span></span>                                                |
| <span data-ttu-id="e9aef-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9aef-208">Is Indexed</span></span>             | <span data-ttu-id="e9aef-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-209">False</span></span>                                               |
| <span data-ttu-id="e9aef-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9aef-210">In Global Catalog</span></span>      | <span data-ttu-id="e9aef-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-211">False</span></span>                                               |
| <span data-ttu-id="e9aef-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9aef-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9aef-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9aef-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="e9aef-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9aef-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9aef-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-216">Search-Flags</span></span>           | <span data-ttu-id="e9aef-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9aef-217">0x00000000</span></span>                                          |
| <span data-ttu-id="e9aef-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-218">System-Flags</span></span>           | <span data-ttu-id="e9aef-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9aef-219">0x00000010</span></span>                                          |
| <span data-ttu-id="e9aef-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9aef-220">Classes used in</span></span>        | [<span data-ttu-id="e9aef-221">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="e9aef-221">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9aef-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9aef-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9aef-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-223">Entry</span></span> | <span data-ttu-id="e9aef-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9aef-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9aef-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9aef-227">System-Only</span></span>            | <span data-ttu-id="e9aef-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-228">False</span></span>                                               |
| <span data-ttu-id="e9aef-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9aef-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e9aef-230">True</span><span class="sxs-lookup"><span data-stu-id="e9aef-230">True</span></span>                                                |
| <span data-ttu-id="e9aef-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9aef-231">Is Indexed</span></span>             | <span data-ttu-id="e9aef-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-232">False</span></span>                                               |
| <span data-ttu-id="e9aef-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9aef-233">In Global Catalog</span></span>      | <span data-ttu-id="e9aef-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-234">False</span></span>                                               |
| <span data-ttu-id="e9aef-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9aef-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9aef-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9aef-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="e9aef-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9aef-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9aef-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-239">Search-Flags</span></span>           | <span data-ttu-id="e9aef-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9aef-240">0x00000000</span></span>                                          |
| <span data-ttu-id="e9aef-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-241">System-Flags</span></span>           | <span data-ttu-id="e9aef-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9aef-242">0x00000010</span></span>                                          |
| <span data-ttu-id="e9aef-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9aef-243">Classes used in</span></span>        | [<span data-ttu-id="e9aef-244">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="e9aef-244">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9aef-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9aef-245">Windows Server 2012</span></span>



| <span data-ttu-id="e9aef-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9aef-246">Entry</span></span> | <span data-ttu-id="e9aef-247">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aef-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9aef-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9aef-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9aef-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="e9aef-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9aef-250">System-Only</span></span>            | <span data-ttu-id="e9aef-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-251">False</span></span>                                               |
| <span data-ttu-id="e9aef-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9aef-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e9aef-253">True</span><span class="sxs-lookup"><span data-stu-id="e9aef-253">True</span></span>                                                |
| <span data-ttu-id="e9aef-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9aef-254">Is Indexed</span></span>             | <span data-ttu-id="e9aef-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-255">False</span></span>                                               |
| <span data-ttu-id="e9aef-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9aef-256">In Global Catalog</span></span>      | <span data-ttu-id="e9aef-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9aef-257">False</span></span>                                               |
| <span data-ttu-id="e9aef-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9aef-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9aef-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9aef-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="e9aef-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9aef-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9aef-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="e9aef-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-262">Search-Flags</span></span>           | <span data-ttu-id="e9aef-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9aef-263">0x00000000</span></span>                                          |
| <span data-ttu-id="e9aef-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9aef-264">System-Flags</span></span>           | <span data-ttu-id="e9aef-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9aef-265">0x00000010</span></span>                                          |
| <span data-ttu-id="e9aef-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9aef-266">Classes used in</span></span>        | [<span data-ttu-id="e9aef-267">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="e9aef-267">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



 

 





