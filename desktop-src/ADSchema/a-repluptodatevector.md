---
title: REPL-Уптодате-атрибут Vector
description: Отслеживает сведения о состоянии внутренней репликации для всего NC. Сведения можно извлечь в общедоступной форме через API Дсрепликажетинфо (). Имеется во всех корневых объектах NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- REPL-схема AD атрибута Уптодате-Vector
- Схема AD атрибута Реплуптодатевектор
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655301"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="357af-107">REPL-Уптодате-атрибут Vector</span><span class="sxs-lookup"><span data-stu-id="357af-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="357af-108">Отслеживает сведения о состоянии внутренней репликации для всего NC.</span><span class="sxs-lookup"><span data-stu-id="357af-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="357af-109">Сведения можно извлечь в общедоступной форме через API Дсрепликажетинфо ().</span><span class="sxs-lookup"><span data-stu-id="357af-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="357af-110">Имеется во всех корневых объектах NC.</span><span class="sxs-lookup"><span data-stu-id="357af-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="357af-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-111">Entry</span></span> | <span data-ttu-id="357af-112">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="357af-113">CN</span><span class="sxs-lookup"><span data-stu-id="357af-113">CN</span></span>                | <span data-ttu-id="357af-114">REPL-Уптодате-Vector</span><span class="sxs-lookup"><span data-stu-id="357af-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="357af-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="357af-115">Ldap-Display-Name</span></span> | <span data-ttu-id="357af-116">реплуптодатевектор</span><span class="sxs-lookup"><span data-stu-id="357af-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="357af-117">Размер</span><span class="sxs-lookup"><span data-stu-id="357af-117">Size</span></span>              | <span data-ttu-id="357af-118">Длина пропорциональна количеству реплик (прошлых и существующих) NC.</span><span class="sxs-lookup"><span data-stu-id="357af-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="357af-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="357af-119">Update Privilege</span></span>  | <span data-ttu-id="357af-120">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="357af-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="357af-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="357af-121">Update Frequency</span></span>  | <span data-ttu-id="357af-122">Изменения в ответ на завершенные циклы входящей репликации.</span><span class="sxs-lookup"><span data-stu-id="357af-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="357af-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="357af-123">Attribute-Id</span></span>      | <span data-ttu-id="357af-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="357af-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="357af-125">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="357af-125">System-Id-Guid</span></span>    | <span data-ttu-id="357af-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="357af-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="357af-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="357af-127">Syntax</span></span>            | [<span data-ttu-id="357af-128">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="357af-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="357af-129">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="357af-129">Implementations</span></span>

-   [<span data-ttu-id="357af-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="357af-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="357af-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="357af-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="357af-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="357af-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="357af-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="357af-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="357af-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="357af-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="357af-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="357af-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="357af-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="357af-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="357af-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="357af-137">Windows 2000 Server</span></span>



| <span data-ttu-id="357af-138">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-138">Entry</span></span> | <span data-ttu-id="357af-139">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-140">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-142">System-Only</span></span>            | <span data-ttu-id="357af-143">True</span><span class="sxs-lookup"><span data-stu-id="357af-143">True</span></span>                            |
| <span data-ttu-id="357af-144">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-144">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-145">True</span><span class="sxs-lookup"><span data-stu-id="357af-145">True</span></span>                            |
| <span data-ttu-id="357af-146">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-146">Is Indexed</span></span>             | <span data-ttu-id="357af-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-147">False</span></span>                           |
| <span data-ttu-id="357af-148">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-148">In Global Catalog</span></span>      | <span data-ttu-id="357af-149">True</span><span class="sxs-lookup"><span data-stu-id="357af-149">True</span></span>                            |
| <span data-ttu-id="357af-150">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-151">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-154">Search-Flags</span></span>           | <span data-ttu-id="357af-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-155">0x00000000</span></span>                      |
| <span data-ttu-id="357af-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-156">System-Flags</span></span>           | <span data-ttu-id="357af-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-157">0x00000013</span></span>                      |
| <span data-ttu-id="357af-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-158">Classes used in</span></span>        | [<span data-ttu-id="357af-159">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="357af-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="357af-160">Windows Server 2003</span></span>



| <span data-ttu-id="357af-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-161">Entry</span></span> | <span data-ttu-id="357af-162">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-165">System-Only</span></span>            | <span data-ttu-id="357af-166">True</span><span class="sxs-lookup"><span data-stu-id="357af-166">True</span></span>                            |
| <span data-ttu-id="357af-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-167">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-168">True</span><span class="sxs-lookup"><span data-stu-id="357af-168">True</span></span>                            |
| <span data-ttu-id="357af-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-169">Is Indexed</span></span>             | <span data-ttu-id="357af-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-170">False</span></span>                           |
| <span data-ttu-id="357af-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-171">In Global Catalog</span></span>      | <span data-ttu-id="357af-172">True</span><span class="sxs-lookup"><span data-stu-id="357af-172">True</span></span>                            |
| <span data-ttu-id="357af-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-177">Search-Flags</span></span>           | <span data-ttu-id="357af-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-178">0x00000000</span></span>                      |
| <span data-ttu-id="357af-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-179">System-Flags</span></span>           | <span data-ttu-id="357af-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-180">0x00000013</span></span>                      |
| <span data-ttu-id="357af-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-181">Classes used in</span></span>        | [<span data-ttu-id="357af-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="357af-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="357af-183">ADAM</span></span>



| <span data-ttu-id="357af-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-184">Entry</span></span> | <span data-ttu-id="357af-185">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-188">System-Only</span></span>            | <span data-ttu-id="357af-189">True</span><span class="sxs-lookup"><span data-stu-id="357af-189">True</span></span>                            |
| <span data-ttu-id="357af-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-190">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-191">True</span><span class="sxs-lookup"><span data-stu-id="357af-191">True</span></span>                            |
| <span data-ttu-id="357af-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-192">Is Indexed</span></span>             | <span data-ttu-id="357af-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-193">False</span></span>                           |
| <span data-ttu-id="357af-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-194">In Global Catalog</span></span>      | <span data-ttu-id="357af-195">True</span><span class="sxs-lookup"><span data-stu-id="357af-195">True</span></span>                            |
| <span data-ttu-id="357af-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-200">Search-Flags</span></span>           | <span data-ttu-id="357af-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-201">0x00000000</span></span>                      |
| <span data-ttu-id="357af-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-202">System-Flags</span></span>           | <span data-ttu-id="357af-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-203">0x00000013</span></span>                      |
| <span data-ttu-id="357af-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-204">Classes used in</span></span>        | [<span data-ttu-id="357af-205">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="357af-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="357af-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="357af-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-207">Entry</span></span> | <span data-ttu-id="357af-208">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-211">System-Only</span></span>            | <span data-ttu-id="357af-212">True</span><span class="sxs-lookup"><span data-stu-id="357af-212">True</span></span>                            |
| <span data-ttu-id="357af-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-213">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-214">True</span><span class="sxs-lookup"><span data-stu-id="357af-214">True</span></span>                            |
| <span data-ttu-id="357af-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-215">Is Indexed</span></span>             | <span data-ttu-id="357af-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-216">False</span></span>                           |
| <span data-ttu-id="357af-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-217">In Global Catalog</span></span>      | <span data-ttu-id="357af-218">True</span><span class="sxs-lookup"><span data-stu-id="357af-218">True</span></span>                            |
| <span data-ttu-id="357af-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-223">Search-Flags</span></span>           | <span data-ttu-id="357af-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-224">0x00000000</span></span>                      |
| <span data-ttu-id="357af-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-225">System-Flags</span></span>           | <span data-ttu-id="357af-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-226">0x00000013</span></span>                      |
| <span data-ttu-id="357af-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-227">Classes used in</span></span>        | [<span data-ttu-id="357af-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="357af-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="357af-229">Windows Server 2008</span></span>



| <span data-ttu-id="357af-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-230">Entry</span></span> | <span data-ttu-id="357af-231">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-234">System-Only</span></span>            | <span data-ttu-id="357af-235">True</span><span class="sxs-lookup"><span data-stu-id="357af-235">True</span></span>                            |
| <span data-ttu-id="357af-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-236">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-237">True</span><span class="sxs-lookup"><span data-stu-id="357af-237">True</span></span>                            |
| <span data-ttu-id="357af-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-238">Is Indexed</span></span>             | <span data-ttu-id="357af-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-239">False</span></span>                           |
| <span data-ttu-id="357af-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-240">In Global Catalog</span></span>      | <span data-ttu-id="357af-241">True</span><span class="sxs-lookup"><span data-stu-id="357af-241">True</span></span>                            |
| <span data-ttu-id="357af-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-246">Search-Flags</span></span>           | <span data-ttu-id="357af-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-247">0x00000000</span></span>                      |
| <span data-ttu-id="357af-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-248">System-Flags</span></span>           | <span data-ttu-id="357af-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-249">0x00000013</span></span>                      |
| <span data-ttu-id="357af-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-250">Classes used in</span></span>        | [<span data-ttu-id="357af-251">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="357af-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="357af-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="357af-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-253">Entry</span></span> | <span data-ttu-id="357af-254">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-257">System-Only</span></span>            | <span data-ttu-id="357af-258">True</span><span class="sxs-lookup"><span data-stu-id="357af-258">True</span></span>                            |
| <span data-ttu-id="357af-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-259">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-260">True</span><span class="sxs-lookup"><span data-stu-id="357af-260">True</span></span>                            |
| <span data-ttu-id="357af-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-261">Is Indexed</span></span>             | <span data-ttu-id="357af-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-262">False</span></span>                           |
| <span data-ttu-id="357af-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-263">In Global Catalog</span></span>      | <span data-ttu-id="357af-264">True</span><span class="sxs-lookup"><span data-stu-id="357af-264">True</span></span>                            |
| <span data-ttu-id="357af-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-269">Search-Flags</span></span>           | <span data-ttu-id="357af-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-270">0x00000000</span></span>                      |
| <span data-ttu-id="357af-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-271">System-Flags</span></span>           | <span data-ttu-id="357af-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-272">0x00000013</span></span>                      |
| <span data-ttu-id="357af-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-273">Classes used in</span></span>        | [<span data-ttu-id="357af-274">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="357af-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="357af-275">Windows Server 2012</span></span>



| <span data-ttu-id="357af-276">Ввод</span><span class="sxs-lookup"><span data-stu-id="357af-276">Entry</span></span> | <span data-ttu-id="357af-277">Значение</span><span class="sxs-lookup"><span data-stu-id="357af-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="357af-278">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="357af-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="357af-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="357af-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="357af-280">System-Only</span></span>            | <span data-ttu-id="357af-281">True</span><span class="sxs-lookup"><span data-stu-id="357af-281">True</span></span>                            |
| <span data-ttu-id="357af-282">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="357af-282">Is-Single-Valued</span></span>       | <span data-ttu-id="357af-283">True</span><span class="sxs-lookup"><span data-stu-id="357af-283">True</span></span>                            |
| <span data-ttu-id="357af-284">Индексируется</span><span class="sxs-lookup"><span data-stu-id="357af-284">Is Indexed</span></span>             | <span data-ttu-id="357af-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="357af-285">False</span></span>                           |
| <span data-ttu-id="357af-286">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="357af-286">In Global Catalog</span></span>      | <span data-ttu-id="357af-287">True</span><span class="sxs-lookup"><span data-stu-id="357af-287">True</span></span>                            |
| <span data-ttu-id="357af-288">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="357af-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="357af-289">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="357af-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="357af-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="357af-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="357af-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="357af-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="357af-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-292">Search-Flags</span></span>           | <span data-ttu-id="357af-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="357af-293">0x00000000</span></span>                      |
| <span data-ttu-id="357af-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="357af-294">System-Flags</span></span>           | <span data-ttu-id="357af-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="357af-295">0x00000013</span></span>                      |
| <span data-ttu-id="357af-296">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="357af-296">Classes used in</span></span>        | [<span data-ttu-id="357af-297">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="357af-297">**Top**</span></span>](c-top.md)<br/> |



 

 





