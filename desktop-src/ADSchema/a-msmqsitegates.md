---
title: Атрибут MSMQ-site-Gates
description: Список DNs-серверов маршрутизации MSMQ, через который должен маршрутизироваться весь трафик между сайтами.
ms.assetid: 4c00553e-6439-4fad-974c-3bfbb61d8f2d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов Active Directory для службы "MSMQ-site-Gate"
- Схема AD атрибута Мсмкситегатес
topic_type:
- apiref
api_name:
- MSMQ-Site-Gates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b970c979bb34ef0854755e042b6d36457c999be0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893429"
---
# <a name="msmq-site-gates-attribute"></a><span data-ttu-id="5cd93-105">Атрибут MSMQ-site-Gates</span><span class="sxs-lookup"><span data-stu-id="5cd93-105">MSMQ-Site-Gates attribute</span></span>

<span data-ttu-id="5cd93-106">Список DNs-серверов маршрутизации MSMQ, через который должен маршрутизироваться весь трафик между сайтами.</span><span class="sxs-lookup"><span data-stu-id="5cd93-106">The list of DNs for MSMQ routing servers, through which all traffic between sites must be routed.</span></span>



| <span data-ttu-id="5cd93-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-107">Entry</span></span> | <span data-ttu-id="5cd93-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5cd93-109">CN</span><span class="sxs-lookup"><span data-stu-id="5cd93-109">CN</span></span>                | <span data-ttu-id="5cd93-110">MSMQ-site-Gates</span><span class="sxs-lookup"><span data-stu-id="5cd93-110">MSMQ-Site-Gates</span></span>                         |
| <span data-ttu-id="5cd93-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5cd93-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5cd93-112">мсмкситегатес</span><span class="sxs-lookup"><span data-stu-id="5cd93-112">mSMQSiteGates</span></span>                           |
| <span data-ttu-id="5cd93-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5cd93-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="5cd93-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5cd93-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="5cd93-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5cd93-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="5cd93-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-116">Attribute-Id</span></span>      | <span data-ttu-id="5cd93-117">1.2.840.113556.1.4.945</span><span class="sxs-lookup"><span data-stu-id="5cd93-117">1.2.840.113556.1.4.945</span></span>                  |
| <span data-ttu-id="5cd93-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5cd93-118">System-Id-Guid</span></span>    | <span data-ttu-id="5cd93-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="5cd93-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="5cd93-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cd93-120">Syntax</span></span>            | [<span data-ttu-id="5cd93-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5cd93-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5cd93-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5cd93-122">Implementations</span></span>

-   [<span data-ttu-id="5cd93-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5cd93-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5cd93-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5cd93-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5cd93-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5cd93-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5cd93-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5cd93-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5cd93-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5cd93-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5cd93-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5cd93-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5cd93-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5cd93-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5cd93-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-130">Entry</span></span> | <span data-ttu-id="5cd93-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd93-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5cd93-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cd93-134">System-Only</span></span>            | <span data-ttu-id="5cd93-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-135">False</span></span>                                               |
| <span data-ttu-id="5cd93-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5cd93-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5cd93-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-137">False</span></span>                                               |
| <span data-ttu-id="5cd93-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5cd93-138">Is Indexed</span></span>             | <span data-ttu-id="5cd93-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-139">False</span></span>                                               |
| <span data-ttu-id="5cd93-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5cd93-140">In Global Catalog</span></span>      | <span data-ttu-id="5cd93-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-141">False</span></span>                                               |
| <span data-ttu-id="5cd93-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5cd93-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cd93-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5cd93-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5cd93-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cd93-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cd93-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-146">Search-Flags</span></span>           | <span data-ttu-id="5cd93-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cd93-147">0x00000000</span></span>                                          |
| <span data-ttu-id="5cd93-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-148">System-Flags</span></span>           | <span data-ttu-id="5cd93-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cd93-149">0x00000010</span></span>                                          |
| <span data-ttu-id="5cd93-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5cd93-150">Classes used in</span></span>        | [<span data-ttu-id="5cd93-151">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="5cd93-151">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5cd93-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5cd93-152">Windows Server 2003</span></span>



| <span data-ttu-id="5cd93-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-153">Entry</span></span> | <span data-ttu-id="5cd93-154">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd93-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5cd93-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cd93-157">System-Only</span></span>            | <span data-ttu-id="5cd93-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-158">False</span></span>                                               |
| <span data-ttu-id="5cd93-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5cd93-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5cd93-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-160">False</span></span>                                               |
| <span data-ttu-id="5cd93-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5cd93-161">Is Indexed</span></span>             | <span data-ttu-id="5cd93-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-162">False</span></span>                                               |
| <span data-ttu-id="5cd93-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5cd93-163">In Global Catalog</span></span>      | <span data-ttu-id="5cd93-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-164">False</span></span>                                               |
| <span data-ttu-id="5cd93-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5cd93-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cd93-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5cd93-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5cd93-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cd93-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cd93-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-169">Search-Flags</span></span>           | <span data-ttu-id="5cd93-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cd93-170">0x00000000</span></span>                                          |
| <span data-ttu-id="5cd93-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-171">System-Flags</span></span>           | <span data-ttu-id="5cd93-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cd93-172">0x00000010</span></span>                                          |
| <span data-ttu-id="5cd93-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5cd93-173">Classes used in</span></span>        | [<span data-ttu-id="5cd93-174">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="5cd93-174">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5cd93-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5cd93-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5cd93-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-176">Entry</span></span> | <span data-ttu-id="5cd93-177">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd93-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5cd93-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cd93-180">System-Only</span></span>            | <span data-ttu-id="5cd93-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-181">False</span></span>                                               |
| <span data-ttu-id="5cd93-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5cd93-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5cd93-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-183">False</span></span>                                               |
| <span data-ttu-id="5cd93-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5cd93-184">Is Indexed</span></span>             | <span data-ttu-id="5cd93-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-185">False</span></span>                                               |
| <span data-ttu-id="5cd93-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5cd93-186">In Global Catalog</span></span>      | <span data-ttu-id="5cd93-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-187">False</span></span>                                               |
| <span data-ttu-id="5cd93-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5cd93-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cd93-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5cd93-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5cd93-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cd93-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cd93-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-192">Search-Flags</span></span>           | <span data-ttu-id="5cd93-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cd93-193">0x00000000</span></span>                                          |
| <span data-ttu-id="5cd93-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-194">System-Flags</span></span>           | <span data-ttu-id="5cd93-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cd93-195">0x00000010</span></span>                                          |
| <span data-ttu-id="5cd93-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5cd93-196">Classes used in</span></span>        | [<span data-ttu-id="5cd93-197">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="5cd93-197">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5cd93-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cd93-198">Windows Server 2008</span></span>



| <span data-ttu-id="5cd93-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-199">Entry</span></span> | <span data-ttu-id="5cd93-200">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd93-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5cd93-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cd93-203">System-Only</span></span>            | <span data-ttu-id="5cd93-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-204">False</span></span>                                               |
| <span data-ttu-id="5cd93-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5cd93-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5cd93-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-206">False</span></span>                                               |
| <span data-ttu-id="5cd93-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5cd93-207">Is Indexed</span></span>             | <span data-ttu-id="5cd93-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-208">False</span></span>                                               |
| <span data-ttu-id="5cd93-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5cd93-209">In Global Catalog</span></span>      | <span data-ttu-id="5cd93-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-210">False</span></span>                                               |
| <span data-ttu-id="5cd93-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5cd93-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cd93-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5cd93-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5cd93-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cd93-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cd93-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-215">Search-Flags</span></span>           | <span data-ttu-id="5cd93-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cd93-216">0x00000000</span></span>                                          |
| <span data-ttu-id="5cd93-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-217">System-Flags</span></span>           | <span data-ttu-id="5cd93-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cd93-218">0x00000010</span></span>                                          |
| <span data-ttu-id="5cd93-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5cd93-219">Classes used in</span></span>        | [<span data-ttu-id="5cd93-220">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="5cd93-220">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5cd93-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5cd93-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5cd93-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-222">Entry</span></span> | <span data-ttu-id="5cd93-223">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd93-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5cd93-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cd93-226">System-Only</span></span>            | <span data-ttu-id="5cd93-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-227">False</span></span>                                               |
| <span data-ttu-id="5cd93-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5cd93-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5cd93-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-229">False</span></span>                                               |
| <span data-ttu-id="5cd93-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5cd93-230">Is Indexed</span></span>             | <span data-ttu-id="5cd93-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-231">False</span></span>                                               |
| <span data-ttu-id="5cd93-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5cd93-232">In Global Catalog</span></span>      | <span data-ttu-id="5cd93-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-233">False</span></span>                                               |
| <span data-ttu-id="5cd93-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5cd93-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cd93-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5cd93-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5cd93-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cd93-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cd93-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-238">Search-Flags</span></span>           | <span data-ttu-id="5cd93-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cd93-239">0x00000000</span></span>                                          |
| <span data-ttu-id="5cd93-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-240">System-Flags</span></span>           | <span data-ttu-id="5cd93-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cd93-241">0x00000010</span></span>                                          |
| <span data-ttu-id="5cd93-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5cd93-242">Classes used in</span></span>        | [<span data-ttu-id="5cd93-243">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="5cd93-243">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5cd93-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cd93-244">Windows Server 2012</span></span>



| <span data-ttu-id="5cd93-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="5cd93-245">Entry</span></span> | <span data-ttu-id="5cd93-246">Значение</span><span class="sxs-lookup"><span data-stu-id="5cd93-246">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd93-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5cd93-247">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cd93-248">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5cd93-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cd93-249">System-Only</span></span>            | <span data-ttu-id="5cd93-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-250">False</span></span>                                               |
| <span data-ttu-id="5cd93-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5cd93-251">Is-Single-Valued</span></span>       | <span data-ttu-id="5cd93-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-252">False</span></span>                                               |
| <span data-ttu-id="5cd93-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5cd93-253">Is Indexed</span></span>             | <span data-ttu-id="5cd93-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-254">False</span></span>                                               |
| <span data-ttu-id="5cd93-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5cd93-255">In Global Catalog</span></span>      | <span data-ttu-id="5cd93-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="5cd93-256">False</span></span>                                               |
| <span data-ttu-id="5cd93-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5cd93-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cd93-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5cd93-258">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5cd93-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cd93-259">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cd93-260">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5cd93-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-261">Search-Flags</span></span>           | <span data-ttu-id="5cd93-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cd93-262">0x00000000</span></span>                                          |
| <span data-ttu-id="5cd93-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cd93-263">System-Flags</span></span>           | <span data-ttu-id="5cd93-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cd93-264">0x00000010</span></span>                                          |
| <span data-ttu-id="5cd93-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5cd93-265">Classes used in</span></span>        | [<span data-ttu-id="5cd93-266">**Очередь MSMQ-site-Link**</span><span class="sxs-lookup"><span data-stu-id="5cd93-266">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



 

 





