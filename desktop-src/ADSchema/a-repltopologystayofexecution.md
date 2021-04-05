---
title: REPL-топология-сохранение атрибута выполнения
description: Задержка между удалением объекта сервера и его окончательной удалением из топологии репликации.
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- REPL-топология-схема AD атрибута, которая остается в процессе выполнения
- Схема AD атрибута Реплтопологистайофексекутион
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804565"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="6708b-105">REPL-топология-сохранение атрибута выполнения</span><span class="sxs-lookup"><span data-stu-id="6708b-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="6708b-106">Задержка между удалением объекта сервера и его окончательной удалением из топологии репликации.</span><span class="sxs-lookup"><span data-stu-id="6708b-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="6708b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-107">Entry</span></span> | <span data-ttu-id="6708b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6708b-109">CN</span><span class="sxs-lookup"><span data-stu-id="6708b-109">CN</span></span>                | <span data-ttu-id="6708b-110">REPL-топология-продолжение выполнения</span><span class="sxs-lookup"><span data-stu-id="6708b-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="6708b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6708b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6708b-112">реплтопологистайофексекутион</span><span class="sxs-lookup"><span data-stu-id="6708b-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="6708b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6708b-113">Size</span></span>              | <span data-ttu-id="6708b-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="6708b-114">4 bytes</span></span>                              |
| <span data-ttu-id="6708b-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6708b-115">Update Privilege</span></span>  | <span data-ttu-id="6708b-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="6708b-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="6708b-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6708b-117">Update Frequency</span></span>  | <span data-ttu-id="6708b-118">При каждом удалении объекта сервера.</span><span class="sxs-lookup"><span data-stu-id="6708b-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="6708b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-119">Attribute-Id</span></span>      | <span data-ttu-id="6708b-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="6708b-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="6708b-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6708b-121">System-Id-Guid</span></span>    | <span data-ttu-id="6708b-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6708b-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="6708b-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6708b-123">Syntax</span></span>            | [<span data-ttu-id="6708b-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="6708b-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6708b-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6708b-125">Implementations</span></span>

-   [<span data-ttu-id="6708b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6708b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6708b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6708b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6708b-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6708b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6708b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6708b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6708b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6708b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6708b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6708b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6708b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6708b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6708b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6708b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6708b-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-134">Entry</span></span> | <span data-ttu-id="6708b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-138">System-Only</span></span>            | <span data-ttu-id="6708b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-139">False</span></span>                                            |
| <span data-ttu-id="6708b-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-141">True</span><span class="sxs-lookup"><span data-stu-id="6708b-141">True</span></span>                                             |
| <span data-ttu-id="6708b-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-142">Is Indexed</span></span>             | <span data-ttu-id="6708b-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-143">False</span></span>                                            |
| <span data-ttu-id="6708b-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-144">In Global Catalog</span></span>      | <span data-ttu-id="6708b-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-145">False</span></span>                                            |
| <span data-ttu-id="6708b-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-150">Search-Flags</span></span>           | <span data-ttu-id="6708b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-151">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-152">System-Flags</span></span>           | <span data-ttu-id="6708b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-153">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-154">Classes used in</span></span>        | [<span data-ttu-id="6708b-155">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6708b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6708b-156">Windows Server 2003</span></span>



| <span data-ttu-id="6708b-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-157">Entry</span></span> | <span data-ttu-id="6708b-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-161">System-Only</span></span>            | <span data-ttu-id="6708b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-162">False</span></span>                                            |
| <span data-ttu-id="6708b-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-164">True</span><span class="sxs-lookup"><span data-stu-id="6708b-164">True</span></span>                                             |
| <span data-ttu-id="6708b-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-165">Is Indexed</span></span>             | <span data-ttu-id="6708b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-166">False</span></span>                                            |
| <span data-ttu-id="6708b-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-167">In Global Catalog</span></span>      | <span data-ttu-id="6708b-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-168">False</span></span>                                            |
| <span data-ttu-id="6708b-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-173">Search-Flags</span></span>           | <span data-ttu-id="6708b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-174">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-175">System-Flags</span></span>           | <span data-ttu-id="6708b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-176">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-177">Classes used in</span></span>        | [<span data-ttu-id="6708b-178">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6708b-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="6708b-179">ADAM</span></span>



| <span data-ttu-id="6708b-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-180">Entry</span></span> | <span data-ttu-id="6708b-181">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-184">System-Only</span></span>            | <span data-ttu-id="6708b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-185">False</span></span>                                            |
| <span data-ttu-id="6708b-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-187">True</span><span class="sxs-lookup"><span data-stu-id="6708b-187">True</span></span>                                             |
| <span data-ttu-id="6708b-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-188">Is Indexed</span></span>             | <span data-ttu-id="6708b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-189">False</span></span>                                            |
| <span data-ttu-id="6708b-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-190">In Global Catalog</span></span>      | <span data-ttu-id="6708b-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-191">False</span></span>                                            |
| <span data-ttu-id="6708b-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-196">Search-Flags</span></span>           | <span data-ttu-id="6708b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-197">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-198">System-Flags</span></span>           | <span data-ttu-id="6708b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-199">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-200">Classes used in</span></span>        | [<span data-ttu-id="6708b-201">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6708b-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6708b-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6708b-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-203">Entry</span></span> | <span data-ttu-id="6708b-204">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-207">System-Only</span></span>            | <span data-ttu-id="6708b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-208">False</span></span>                                            |
| <span data-ttu-id="6708b-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-210">True</span><span class="sxs-lookup"><span data-stu-id="6708b-210">True</span></span>                                             |
| <span data-ttu-id="6708b-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-211">Is Indexed</span></span>             | <span data-ttu-id="6708b-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-212">False</span></span>                                            |
| <span data-ttu-id="6708b-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-213">In Global Catalog</span></span>      | <span data-ttu-id="6708b-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-214">False</span></span>                                            |
| <span data-ttu-id="6708b-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-219">Search-Flags</span></span>           | <span data-ttu-id="6708b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-220">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-221">System-Flags</span></span>           | <span data-ttu-id="6708b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-222">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-223">Classes used in</span></span>        | [<span data-ttu-id="6708b-224">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6708b-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6708b-225">Windows Server 2008</span></span>



| <span data-ttu-id="6708b-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-226">Entry</span></span> | <span data-ttu-id="6708b-227">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-230">System-Only</span></span>            | <span data-ttu-id="6708b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-231">False</span></span>                                            |
| <span data-ttu-id="6708b-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-233">True</span><span class="sxs-lookup"><span data-stu-id="6708b-233">True</span></span>                                             |
| <span data-ttu-id="6708b-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-234">Is Indexed</span></span>             | <span data-ttu-id="6708b-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-235">False</span></span>                                            |
| <span data-ttu-id="6708b-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-236">In Global Catalog</span></span>      | <span data-ttu-id="6708b-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-237">False</span></span>                                            |
| <span data-ttu-id="6708b-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-242">Search-Flags</span></span>           | <span data-ttu-id="6708b-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-243">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-244">System-Flags</span></span>           | <span data-ttu-id="6708b-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-245">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-246">Classes used in</span></span>        | [<span data-ttu-id="6708b-247">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6708b-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6708b-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6708b-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-249">Entry</span></span> | <span data-ttu-id="6708b-250">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-253">System-Only</span></span>            | <span data-ttu-id="6708b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-254">False</span></span>                                            |
| <span data-ttu-id="6708b-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-256">True</span><span class="sxs-lookup"><span data-stu-id="6708b-256">True</span></span>                                             |
| <span data-ttu-id="6708b-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-257">Is Indexed</span></span>             | <span data-ttu-id="6708b-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-258">False</span></span>                                            |
| <span data-ttu-id="6708b-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-259">In Global Catalog</span></span>      | <span data-ttu-id="6708b-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-260">False</span></span>                                            |
| <span data-ttu-id="6708b-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-265">Search-Flags</span></span>           | <span data-ttu-id="6708b-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-266">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-267">System-Flags</span></span>           | <span data-ttu-id="6708b-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-268">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-269">Classes used in</span></span>        | [<span data-ttu-id="6708b-270">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6708b-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6708b-271">Windows Server 2012</span></span>



| <span data-ttu-id="6708b-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="6708b-272">Entry</span></span> | <span data-ttu-id="6708b-273">Значение</span><span class="sxs-lookup"><span data-stu-id="6708b-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6708b-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6708b-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6708b-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6708b-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="6708b-276">System-Only</span></span>            | <span data-ttu-id="6708b-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-277">False</span></span>                                            |
| <span data-ttu-id="6708b-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6708b-278">Is-Single-Valued</span></span>       | <span data-ttu-id="6708b-279">True</span><span class="sxs-lookup"><span data-stu-id="6708b-279">True</span></span>                                             |
| <span data-ttu-id="6708b-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6708b-280">Is Indexed</span></span>             | <span data-ttu-id="6708b-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-281">False</span></span>                                            |
| <span data-ttu-id="6708b-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6708b-282">In Global Catalog</span></span>      | <span data-ttu-id="6708b-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="6708b-283">False</span></span>                                            |
| <span data-ttu-id="6708b-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6708b-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="6708b-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6708b-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6708b-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6708b-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6708b-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6708b-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6708b-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-288">Search-Flags</span></span>           | <span data-ttu-id="6708b-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6708b-289">0x00000000</span></span>                                       |
| <span data-ttu-id="6708b-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6708b-290">System-Flags</span></span>           | <span data-ttu-id="6708b-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6708b-291">0x00000010</span></span>                                       |
| <span data-ttu-id="6708b-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6708b-292">Classes used in</span></span>        | [<span data-ttu-id="6708b-293">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="6708b-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





