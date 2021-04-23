---
title: Атрибут разделяемого атрибута Set
description: Отслеживает состояние внутренней репликации частичных реплик (то есть в глобальных каталогах). Атрибут объекта NC частичной реплики. Определяет набор атрибутов, имеющихся в определенном NC частичной реплики.
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов с частичным атрибутом
- Схема AD атрибута Партиалаттрибутесет
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655317"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="99033-107">Атрибут разделяемого атрибута Set</span><span class="sxs-lookup"><span data-stu-id="99033-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="99033-108">Отслеживает состояние внутренней репликации частичных реплик (то есть в глобальных каталогах).</span><span class="sxs-lookup"><span data-stu-id="99033-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="99033-109">Атрибут объекта NC частичной реплики.</span><span class="sxs-lookup"><span data-stu-id="99033-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="99033-110">Определяет набор атрибутов, имеющихся в определенном NC частичной реплики.</span><span class="sxs-lookup"><span data-stu-id="99033-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="99033-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-111">Entry</span></span> | <span data-ttu-id="99033-112">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="99033-113">CN</span><span class="sxs-lookup"><span data-stu-id="99033-113">CN</span></span>                | <span data-ttu-id="99033-114">Разделяемый атрибут-set</span><span class="sxs-lookup"><span data-stu-id="99033-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="99033-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="99033-115">Ldap-Display-Name</span></span> | <span data-ttu-id="99033-116">партиалаттрибутесет</span><span class="sxs-lookup"><span data-stu-id="99033-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="99033-117">Размер</span><span class="sxs-lookup"><span data-stu-id="99033-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="99033-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="99033-118">Update Privilege</span></span>  | <span data-ttu-id="99033-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="99033-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="99033-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="99033-120">Update Frequency</span></span>  | <span data-ttu-id="99033-121">Во время репликации</span><span class="sxs-lookup"><span data-stu-id="99033-121">During replication</span></span>                                    |
| <span data-ttu-id="99033-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99033-122">Attribute-Id</span></span>      | <span data-ttu-id="99033-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="99033-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="99033-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="99033-124">System-Id-Guid</span></span>    | <span data-ttu-id="99033-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="99033-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="99033-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99033-126">Syntax</span></span>            | [<span data-ttu-id="99033-127">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="99033-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="99033-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="99033-128">Implementations</span></span>

-   [<span data-ttu-id="99033-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="99033-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="99033-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99033-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99033-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="99033-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="99033-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99033-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99033-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99033-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99033-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99033-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99033-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99033-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="99033-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99033-136">Windows 2000 Server</span></span>



| <span data-ttu-id="99033-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-137">Entry</span></span> | <span data-ttu-id="99033-138">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-141">System-Only</span></span>            | <span data-ttu-id="99033-142">True</span><span class="sxs-lookup"><span data-stu-id="99033-142">True</span></span>                            |
| <span data-ttu-id="99033-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-143">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-144">True</span><span class="sxs-lookup"><span data-stu-id="99033-144">True</span></span>                            |
| <span data-ttu-id="99033-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-145">Is Indexed</span></span>             | <span data-ttu-id="99033-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-146">False</span></span>                           |
| <span data-ttu-id="99033-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-147">In Global Catalog</span></span>      | <span data-ttu-id="99033-148">True</span><span class="sxs-lookup"><span data-stu-id="99033-148">True</span></span>                            |
| <span data-ttu-id="99033-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-153">Search-Flags</span></span>           | <span data-ttu-id="99033-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-154">0x00000000</span></span>                      |
| <span data-ttu-id="99033-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-155">System-Flags</span></span>           | <span data-ttu-id="99033-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-156">0x00000013</span></span>                      |
| <span data-ttu-id="99033-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-157">Classes used in</span></span>        | [<span data-ttu-id="99033-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="99033-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99033-159">Windows Server 2003</span></span>



| <span data-ttu-id="99033-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-160">Entry</span></span> | <span data-ttu-id="99033-161">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-164">System-Only</span></span>            | <span data-ttu-id="99033-165">True</span><span class="sxs-lookup"><span data-stu-id="99033-165">True</span></span>                            |
| <span data-ttu-id="99033-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-166">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-167">True</span><span class="sxs-lookup"><span data-stu-id="99033-167">True</span></span>                            |
| <span data-ttu-id="99033-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-168">Is Indexed</span></span>             | <span data-ttu-id="99033-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-169">False</span></span>                           |
| <span data-ttu-id="99033-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-170">In Global Catalog</span></span>      | <span data-ttu-id="99033-171">True</span><span class="sxs-lookup"><span data-stu-id="99033-171">True</span></span>                            |
| <span data-ttu-id="99033-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-176">Search-Flags</span></span>           | <span data-ttu-id="99033-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-177">0x00000000</span></span>                      |
| <span data-ttu-id="99033-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-178">System-Flags</span></span>           | <span data-ttu-id="99033-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-179">0x00000013</span></span>                      |
| <span data-ttu-id="99033-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-180">Classes used in</span></span>        | [<span data-ttu-id="99033-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="99033-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="99033-182">ADAM</span></span>



| <span data-ttu-id="99033-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-183">Entry</span></span> | <span data-ttu-id="99033-184">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-187">System-Only</span></span>            | <span data-ttu-id="99033-188">True</span><span class="sxs-lookup"><span data-stu-id="99033-188">True</span></span>                            |
| <span data-ttu-id="99033-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-189">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-190">True</span><span class="sxs-lookup"><span data-stu-id="99033-190">True</span></span>                            |
| <span data-ttu-id="99033-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-191">Is Indexed</span></span>             | <span data-ttu-id="99033-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-192">False</span></span>                           |
| <span data-ttu-id="99033-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-193">In Global Catalog</span></span>      | <span data-ttu-id="99033-194">True</span><span class="sxs-lookup"><span data-stu-id="99033-194">True</span></span>                            |
| <span data-ttu-id="99033-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-199">Search-Flags</span></span>           | <span data-ttu-id="99033-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-200">0x00000000</span></span>                      |
| <span data-ttu-id="99033-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-201">System-Flags</span></span>           | <span data-ttu-id="99033-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-202">0x00000013</span></span>                      |
| <span data-ttu-id="99033-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-203">Classes used in</span></span>        | [<span data-ttu-id="99033-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99033-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99033-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99033-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-206">Entry</span></span> | <span data-ttu-id="99033-207">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-210">System-Only</span></span>            | <span data-ttu-id="99033-211">True</span><span class="sxs-lookup"><span data-stu-id="99033-211">True</span></span>                            |
| <span data-ttu-id="99033-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-212">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-213">True</span><span class="sxs-lookup"><span data-stu-id="99033-213">True</span></span>                            |
| <span data-ttu-id="99033-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-214">Is Indexed</span></span>             | <span data-ttu-id="99033-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-215">False</span></span>                           |
| <span data-ttu-id="99033-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-216">In Global Catalog</span></span>      | <span data-ttu-id="99033-217">True</span><span class="sxs-lookup"><span data-stu-id="99033-217">True</span></span>                            |
| <span data-ttu-id="99033-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-222">Search-Flags</span></span>           | <span data-ttu-id="99033-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-223">0x00000000</span></span>                      |
| <span data-ttu-id="99033-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-224">System-Flags</span></span>           | <span data-ttu-id="99033-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-225">0x00000013</span></span>                      |
| <span data-ttu-id="99033-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-226">Classes used in</span></span>        | [<span data-ttu-id="99033-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99033-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99033-228">Windows Server 2008</span></span>



| <span data-ttu-id="99033-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-229">Entry</span></span> | <span data-ttu-id="99033-230">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-233">System-Only</span></span>            | <span data-ttu-id="99033-234">True</span><span class="sxs-lookup"><span data-stu-id="99033-234">True</span></span>                            |
| <span data-ttu-id="99033-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-235">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-236">True</span><span class="sxs-lookup"><span data-stu-id="99033-236">True</span></span>                            |
| <span data-ttu-id="99033-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-237">Is Indexed</span></span>             | <span data-ttu-id="99033-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-238">False</span></span>                           |
| <span data-ttu-id="99033-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-239">In Global Catalog</span></span>      | <span data-ttu-id="99033-240">True</span><span class="sxs-lookup"><span data-stu-id="99033-240">True</span></span>                            |
| <span data-ttu-id="99033-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-245">Search-Flags</span></span>           | <span data-ttu-id="99033-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-246">0x00000000</span></span>                      |
| <span data-ttu-id="99033-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-247">System-Flags</span></span>           | <span data-ttu-id="99033-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-248">0x00000013</span></span>                      |
| <span data-ttu-id="99033-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-249">Classes used in</span></span>        | [<span data-ttu-id="99033-250">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99033-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99033-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99033-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-252">Entry</span></span> | <span data-ttu-id="99033-253">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-256">System-Only</span></span>            | <span data-ttu-id="99033-257">True</span><span class="sxs-lookup"><span data-stu-id="99033-257">True</span></span>                            |
| <span data-ttu-id="99033-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-258">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-259">True</span><span class="sxs-lookup"><span data-stu-id="99033-259">True</span></span>                            |
| <span data-ttu-id="99033-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-260">Is Indexed</span></span>             | <span data-ttu-id="99033-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-261">False</span></span>                           |
| <span data-ttu-id="99033-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-262">In Global Catalog</span></span>      | <span data-ttu-id="99033-263">True</span><span class="sxs-lookup"><span data-stu-id="99033-263">True</span></span>                            |
| <span data-ttu-id="99033-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-268">Search-Flags</span></span>           | <span data-ttu-id="99033-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-269">0x00000000</span></span>                      |
| <span data-ttu-id="99033-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-270">System-Flags</span></span>           | <span data-ttu-id="99033-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-271">0x00000013</span></span>                      |
| <span data-ttu-id="99033-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-272">Classes used in</span></span>        | [<span data-ttu-id="99033-273">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99033-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99033-274">Windows Server 2012</span></span>



| <span data-ttu-id="99033-275">Ввод</span><span class="sxs-lookup"><span data-stu-id="99033-275">Entry</span></span> | <span data-ttu-id="99033-276">Значение</span><span class="sxs-lookup"><span data-stu-id="99033-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="99033-277">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="99033-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99033-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="99033-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="99033-279">System-Only</span></span>            | <span data-ttu-id="99033-280">True</span><span class="sxs-lookup"><span data-stu-id="99033-280">True</span></span>                            |
| <span data-ttu-id="99033-281">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="99033-281">Is-Single-Valued</span></span>       | <span data-ttu-id="99033-282">True</span><span class="sxs-lookup"><span data-stu-id="99033-282">True</span></span>                            |
| <span data-ttu-id="99033-283">Индексируется</span><span class="sxs-lookup"><span data-stu-id="99033-283">Is Indexed</span></span>             | <span data-ttu-id="99033-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="99033-284">False</span></span>                           |
| <span data-ttu-id="99033-285">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="99033-285">In Global Catalog</span></span>      | <span data-ttu-id="99033-286">True</span><span class="sxs-lookup"><span data-stu-id="99033-286">True</span></span>                            |
| <span data-ttu-id="99033-287">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="99033-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="99033-288">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99033-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="99033-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99033-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="99033-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99033-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="99033-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-291">Search-Flags</span></span>           | <span data-ttu-id="99033-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99033-292">0x00000000</span></span>                      |
| <span data-ttu-id="99033-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99033-293">System-Flags</span></span>           | <span data-ttu-id="99033-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="99033-294">0x00000013</span></span>                      |
| <span data-ttu-id="99033-295">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="99033-295">Classes used in</span></span>        | [<span data-ttu-id="99033-296">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="99033-296">**Top**</span></span>](c-top.md)<br/> |



 

 





