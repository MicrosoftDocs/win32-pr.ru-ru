---
title: REPL-свойство-мета-атрибут данных
description: Отслеживает сведения о состоянии внутренней репликации для объектов DS. Сведения, которые можно извлечь в общедоступной форме через общедоступный API Дсрепликажетинфо (). Имеется во всех объектах DS.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- REPL-свойство-мета-схема атрибута метаданных AD
- Схема AD атрибута Реплпропертиметадата
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804829"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="af205-107">REPL-свойство-мета-атрибут данных</span><span class="sxs-lookup"><span data-stu-id="af205-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="af205-108">Отслеживает сведения о состоянии внутренней репликации для объектов DS.</span><span class="sxs-lookup"><span data-stu-id="af205-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="af205-109">Сведения, которые можно извлечь в общедоступной форме через общедоступный API Дсрепликажетинфо ().</span><span class="sxs-lookup"><span data-stu-id="af205-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="af205-110">Имеется во всех объектах DS.</span><span class="sxs-lookup"><span data-stu-id="af205-110">Present on all DS objects.</span></span>



| <span data-ttu-id="af205-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-111">Entry</span></span> | <span data-ttu-id="af205-112">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="af205-113">CN</span><span class="sxs-lookup"><span data-stu-id="af205-113">CN</span></span>                | <span data-ttu-id="af205-114">REPL-Property-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="af205-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="af205-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="af205-115">Ldap-Display-Name</span></span> | <span data-ttu-id="af205-116">реплпропертиметадата</span><span class="sxs-lookup"><span data-stu-id="af205-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="af205-117">Размер</span><span class="sxs-lookup"><span data-stu-id="af205-117">Size</span></span>              | <span data-ttu-id="af205-118">Длина пропорциональна количеству реплицируемых атрибутов объекта.</span><span class="sxs-lookup"><span data-stu-id="af205-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="af205-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="af205-119">Update Privilege</span></span>  | <span data-ttu-id="af205-120">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="af205-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="af205-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="af205-121">Update Frequency</span></span>  | <span data-ttu-id="af205-122">Изменения в ответ на любые реплицируемые изменения в объекте.</span><span class="sxs-lookup"><span data-stu-id="af205-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="af205-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af205-123">Attribute-Id</span></span>      | <span data-ttu-id="af205-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="af205-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="af205-125">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="af205-125">System-Id-Guid</span></span>    | <span data-ttu-id="af205-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="af205-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="af205-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af205-127">Syntax</span></span>            | [<span data-ttu-id="af205-128">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="af205-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="af205-129">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="af205-129">Implementations</span></span>

-   [<span data-ttu-id="af205-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af205-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af205-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af205-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af205-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="af205-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="af205-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af205-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af205-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af205-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af205-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af205-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af205-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af205-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af205-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af205-137">Windows 2000 Server</span></span>



| <span data-ttu-id="af205-138">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-138">Entry</span></span> | <span data-ttu-id="af205-139">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-140">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-142">System-Only</span></span>            | <span data-ttu-id="af205-143">True</span><span class="sxs-lookup"><span data-stu-id="af205-143">True</span></span>                            |
| <span data-ttu-id="af205-144">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-144">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-145">True</span><span class="sxs-lookup"><span data-stu-id="af205-145">True</span></span>                            |
| <span data-ttu-id="af205-146">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-146">Is Indexed</span></span>             | <span data-ttu-id="af205-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-147">False</span></span>                           |
| <span data-ttu-id="af205-148">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-148">In Global Catalog</span></span>      | <span data-ttu-id="af205-149">True</span><span class="sxs-lookup"><span data-stu-id="af205-149">True</span></span>                            |
| <span data-ttu-id="af205-150">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-151">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-154">Search-Flags</span></span>           | <span data-ttu-id="af205-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-155">0x00000008</span></span>                      |
| <span data-ttu-id="af205-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-156">System-Flags</span></span>           | <span data-ttu-id="af205-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="af205-157">0x00000013</span></span>                      |
| <span data-ttu-id="af205-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-158">Classes used in</span></span>        | [<span data-ttu-id="af205-159">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af205-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af205-160">Windows Server 2003</span></span>



| <span data-ttu-id="af205-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-161">Entry</span></span> | <span data-ttu-id="af205-162">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-165">System-Only</span></span>            | <span data-ttu-id="af205-166">True</span><span class="sxs-lookup"><span data-stu-id="af205-166">True</span></span>                            |
| <span data-ttu-id="af205-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-167">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-168">True</span><span class="sxs-lookup"><span data-stu-id="af205-168">True</span></span>                            |
| <span data-ttu-id="af205-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-169">Is Indexed</span></span>             | <span data-ttu-id="af205-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-170">False</span></span>                           |
| <span data-ttu-id="af205-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-171">In Global Catalog</span></span>      | <span data-ttu-id="af205-172">True</span><span class="sxs-lookup"><span data-stu-id="af205-172">True</span></span>                            |
| <span data-ttu-id="af205-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-177">Search-Flags</span></span>           | <span data-ttu-id="af205-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-178">0x00000008</span></span>                      |
| <span data-ttu-id="af205-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-179">System-Flags</span></span>           | <span data-ttu-id="af205-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="af205-180">0x0000001B</span></span>                      |
| <span data-ttu-id="af205-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-181">Classes used in</span></span>        | [<span data-ttu-id="af205-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="af205-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="af205-183">ADAM</span></span>



| <span data-ttu-id="af205-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-184">Entry</span></span> | <span data-ttu-id="af205-185">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-188">System-Only</span></span>            | <span data-ttu-id="af205-189">True</span><span class="sxs-lookup"><span data-stu-id="af205-189">True</span></span>                            |
| <span data-ttu-id="af205-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-190">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-191">True</span><span class="sxs-lookup"><span data-stu-id="af205-191">True</span></span>                            |
| <span data-ttu-id="af205-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-192">Is Indexed</span></span>             | <span data-ttu-id="af205-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-193">False</span></span>                           |
| <span data-ttu-id="af205-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-194">In Global Catalog</span></span>      | <span data-ttu-id="af205-195">True</span><span class="sxs-lookup"><span data-stu-id="af205-195">True</span></span>                            |
| <span data-ttu-id="af205-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-200">Search-Flags</span></span>           | <span data-ttu-id="af205-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-201">0x00000008</span></span>                      |
| <span data-ttu-id="af205-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-202">System-Flags</span></span>           | <span data-ttu-id="af205-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="af205-203">0x0000001B</span></span>                      |
| <span data-ttu-id="af205-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-204">Classes used in</span></span>        | [<span data-ttu-id="af205-205">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af205-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af205-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af205-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-207">Entry</span></span> | <span data-ttu-id="af205-208">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-211">System-Only</span></span>            | <span data-ttu-id="af205-212">True</span><span class="sxs-lookup"><span data-stu-id="af205-212">True</span></span>                            |
| <span data-ttu-id="af205-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-213">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-214">True</span><span class="sxs-lookup"><span data-stu-id="af205-214">True</span></span>                            |
| <span data-ttu-id="af205-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-215">Is Indexed</span></span>             | <span data-ttu-id="af205-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-216">False</span></span>                           |
| <span data-ttu-id="af205-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-217">In Global Catalog</span></span>      | <span data-ttu-id="af205-218">True</span><span class="sxs-lookup"><span data-stu-id="af205-218">True</span></span>                            |
| <span data-ttu-id="af205-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-223">Search-Flags</span></span>           | <span data-ttu-id="af205-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-224">0x00000008</span></span>                      |
| <span data-ttu-id="af205-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-225">System-Flags</span></span>           | <span data-ttu-id="af205-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="af205-226">0x0000001B</span></span>                      |
| <span data-ttu-id="af205-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-227">Classes used in</span></span>        | [<span data-ttu-id="af205-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af205-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af205-229">Windows Server 2008</span></span>



| <span data-ttu-id="af205-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-230">Entry</span></span> | <span data-ttu-id="af205-231">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-234">System-Only</span></span>            | <span data-ttu-id="af205-235">True</span><span class="sxs-lookup"><span data-stu-id="af205-235">True</span></span>                            |
| <span data-ttu-id="af205-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-236">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-237">True</span><span class="sxs-lookup"><span data-stu-id="af205-237">True</span></span>                            |
| <span data-ttu-id="af205-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-238">Is Indexed</span></span>             | <span data-ttu-id="af205-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-239">False</span></span>                           |
| <span data-ttu-id="af205-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-240">In Global Catalog</span></span>      | <span data-ttu-id="af205-241">True</span><span class="sxs-lookup"><span data-stu-id="af205-241">True</span></span>                            |
| <span data-ttu-id="af205-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-246">Search-Flags</span></span>           | <span data-ttu-id="af205-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-247">0x00000008</span></span>                      |
| <span data-ttu-id="af205-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-248">System-Flags</span></span>           | <span data-ttu-id="af205-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="af205-249">0x0000001B</span></span>                      |
| <span data-ttu-id="af205-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-250">Classes used in</span></span>        | [<span data-ttu-id="af205-251">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af205-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af205-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af205-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-253">Entry</span></span> | <span data-ttu-id="af205-254">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-257">System-Only</span></span>            | <span data-ttu-id="af205-258">True</span><span class="sxs-lookup"><span data-stu-id="af205-258">True</span></span>                            |
| <span data-ttu-id="af205-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-259">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-260">True</span><span class="sxs-lookup"><span data-stu-id="af205-260">True</span></span>                            |
| <span data-ttu-id="af205-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-261">Is Indexed</span></span>             | <span data-ttu-id="af205-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-262">False</span></span>                           |
| <span data-ttu-id="af205-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-263">In Global Catalog</span></span>      | <span data-ttu-id="af205-264">True</span><span class="sxs-lookup"><span data-stu-id="af205-264">True</span></span>                            |
| <span data-ttu-id="af205-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-269">Search-Flags</span></span>           | <span data-ttu-id="af205-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-270">0x00000008</span></span>                      |
| <span data-ttu-id="af205-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-271">System-Flags</span></span>           | <span data-ttu-id="af205-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="af205-272">0x0000001B</span></span>                      |
| <span data-ttu-id="af205-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-273">Classes used in</span></span>        | [<span data-ttu-id="af205-274">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af205-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af205-275">Windows Server 2012</span></span>



| <span data-ttu-id="af205-276">Ввод</span><span class="sxs-lookup"><span data-stu-id="af205-276">Entry</span></span> | <span data-ttu-id="af205-277">Значение</span><span class="sxs-lookup"><span data-stu-id="af205-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af205-278">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af205-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af205-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af205-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="af205-280">System-Only</span></span>            | <span data-ttu-id="af205-281">True</span><span class="sxs-lookup"><span data-stu-id="af205-281">True</span></span>                            |
| <span data-ttu-id="af205-282">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af205-282">Is-Single-Valued</span></span>       | <span data-ttu-id="af205-283">True</span><span class="sxs-lookup"><span data-stu-id="af205-283">True</span></span>                            |
| <span data-ttu-id="af205-284">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af205-284">Is Indexed</span></span>             | <span data-ttu-id="af205-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="af205-285">False</span></span>                           |
| <span data-ttu-id="af205-286">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af205-286">In Global Catalog</span></span>      | <span data-ttu-id="af205-287">True</span><span class="sxs-lookup"><span data-stu-id="af205-287">True</span></span>                            |
| <span data-ttu-id="af205-288">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af205-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="af205-289">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af205-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af205-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af205-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af205-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af205-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af205-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-292">Search-Flags</span></span>           | <span data-ttu-id="af205-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af205-293">0x00000008</span></span>                      |
| <span data-ttu-id="af205-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af205-294">System-Flags</span></span>           | <span data-ttu-id="af205-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="af205-295">0x0000001B</span></span>                      |
| <span data-ttu-id="af205-296">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af205-296">Classes used in</span></span>        | [<span data-ttu-id="af205-297">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="af205-297">**Top**</span></span>](c-top.md)<br/> |



 

 





