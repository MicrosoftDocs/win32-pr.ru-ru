---
title: Атрибут разделяемого атрибута-удаления списка
description: Отслеживает состояние внутренней репликации частичных реплик (то есть в глобальных каталогах). Атрибут объекта NC частичной реплики. Используется, когда сборщик мусора находится в процессе удаления атрибутов из объектов в контекстах именования частичной реплики.
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута разделяемого атрибута-удаления-списка
- Схема AD атрибута Партиалаттрибутеделетионлист
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655092"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="bc472-107">Атрибут разделяемого атрибута-удаления списка</span><span class="sxs-lookup"><span data-stu-id="bc472-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="bc472-108">Отслеживает состояние внутренней репликации частичных реплик (то есть в глобальных каталогах).</span><span class="sxs-lookup"><span data-stu-id="bc472-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="bc472-109">Атрибут объекта NC частичной реплики.</span><span class="sxs-lookup"><span data-stu-id="bc472-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="bc472-110">Используется, когда сборщик мусора находится в процессе удаления атрибутов из объектов в контекстах именования частичной реплики.</span><span class="sxs-lookup"><span data-stu-id="bc472-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="bc472-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-111">Entry</span></span> | <span data-ttu-id="bc472-112">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bc472-113">CN</span><span class="sxs-lookup"><span data-stu-id="bc472-113">CN</span></span>                | <span data-ttu-id="bc472-114">Разделяемый атрибут-удаление-список</span><span class="sxs-lookup"><span data-stu-id="bc472-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="bc472-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bc472-115">Ldap-Display-Name</span></span> | <span data-ttu-id="bc472-116">партиалаттрибутеделетионлист</span><span class="sxs-lookup"><span data-stu-id="bc472-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="bc472-117">Размер</span><span class="sxs-lookup"><span data-stu-id="bc472-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bc472-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bc472-118">Update Privilege</span></span>  | <span data-ttu-id="bc472-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="bc472-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="bc472-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bc472-120">Update Frequency</span></span>  | <span data-ttu-id="bc472-121">Во время репликации</span><span class="sxs-lookup"><span data-stu-id="bc472-121">During replication</span></span>                                    |
| <span data-ttu-id="bc472-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-122">Attribute-Id</span></span>      | <span data-ttu-id="bc472-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="bc472-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="bc472-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bc472-124">System-Id-Guid</span></span>    | <span data-ttu-id="bc472-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bc472-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="bc472-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc472-126">Syntax</span></span>            | [<span data-ttu-id="bc472-127">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="bc472-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bc472-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bc472-128">Implementations</span></span>

-   [<span data-ttu-id="bc472-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bc472-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bc472-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc472-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc472-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bc472-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bc472-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc472-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc472-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc472-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc472-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc472-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc472-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc472-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bc472-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc472-136">Windows 2000 Server</span></span>



| <span data-ttu-id="bc472-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-137">Entry</span></span> | <span data-ttu-id="bc472-138">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-141">System-Only</span></span>            | <span data-ttu-id="bc472-142">True</span><span class="sxs-lookup"><span data-stu-id="bc472-142">True</span></span>                            |
| <span data-ttu-id="bc472-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-143">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-144">True</span><span class="sxs-lookup"><span data-stu-id="bc472-144">True</span></span>                            |
| <span data-ttu-id="bc472-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-145">Is Indexed</span></span>             | <span data-ttu-id="bc472-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-146">False</span></span>                           |
| <span data-ttu-id="bc472-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-147">In Global Catalog</span></span>      | <span data-ttu-id="bc472-148">True</span><span class="sxs-lookup"><span data-stu-id="bc472-148">True</span></span>                            |
| <span data-ttu-id="bc472-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-153">Search-Flags</span></span>           | <span data-ttu-id="bc472-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-154">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-155">System-Flags</span></span>           | <span data-ttu-id="bc472-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-156">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-157">Classes used in</span></span>        | [<span data-ttu-id="bc472-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bc472-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc472-159">Windows Server 2003</span></span>



| <span data-ttu-id="bc472-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-160">Entry</span></span> | <span data-ttu-id="bc472-161">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-164">System-Only</span></span>            | <span data-ttu-id="bc472-165">True</span><span class="sxs-lookup"><span data-stu-id="bc472-165">True</span></span>                            |
| <span data-ttu-id="bc472-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-166">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-167">True</span><span class="sxs-lookup"><span data-stu-id="bc472-167">True</span></span>                            |
| <span data-ttu-id="bc472-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-168">Is Indexed</span></span>             | <span data-ttu-id="bc472-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-169">False</span></span>                           |
| <span data-ttu-id="bc472-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-170">In Global Catalog</span></span>      | <span data-ttu-id="bc472-171">True</span><span class="sxs-lookup"><span data-stu-id="bc472-171">True</span></span>                            |
| <span data-ttu-id="bc472-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-176">Search-Flags</span></span>           | <span data-ttu-id="bc472-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-177">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-178">System-Flags</span></span>           | <span data-ttu-id="bc472-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-179">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-180">Classes used in</span></span>        | [<span data-ttu-id="bc472-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bc472-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="bc472-182">ADAM</span></span>



| <span data-ttu-id="bc472-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-183">Entry</span></span> | <span data-ttu-id="bc472-184">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-187">System-Only</span></span>            | <span data-ttu-id="bc472-188">True</span><span class="sxs-lookup"><span data-stu-id="bc472-188">True</span></span>                            |
| <span data-ttu-id="bc472-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-189">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-190">True</span><span class="sxs-lookup"><span data-stu-id="bc472-190">True</span></span>                            |
| <span data-ttu-id="bc472-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-191">Is Indexed</span></span>             | <span data-ttu-id="bc472-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-192">False</span></span>                           |
| <span data-ttu-id="bc472-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-193">In Global Catalog</span></span>      | <span data-ttu-id="bc472-194">True</span><span class="sxs-lookup"><span data-stu-id="bc472-194">True</span></span>                            |
| <span data-ttu-id="bc472-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-199">Search-Flags</span></span>           | <span data-ttu-id="bc472-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-200">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-201">System-Flags</span></span>           | <span data-ttu-id="bc472-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-202">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-203">Classes used in</span></span>        | [<span data-ttu-id="bc472-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc472-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc472-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc472-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-206">Entry</span></span> | <span data-ttu-id="bc472-207">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-210">System-Only</span></span>            | <span data-ttu-id="bc472-211">True</span><span class="sxs-lookup"><span data-stu-id="bc472-211">True</span></span>                            |
| <span data-ttu-id="bc472-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-212">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-213">True</span><span class="sxs-lookup"><span data-stu-id="bc472-213">True</span></span>                            |
| <span data-ttu-id="bc472-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-214">Is Indexed</span></span>             | <span data-ttu-id="bc472-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-215">False</span></span>                           |
| <span data-ttu-id="bc472-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-216">In Global Catalog</span></span>      | <span data-ttu-id="bc472-217">True</span><span class="sxs-lookup"><span data-stu-id="bc472-217">True</span></span>                            |
| <span data-ttu-id="bc472-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-222">Search-Flags</span></span>           | <span data-ttu-id="bc472-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-223">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-224">System-Flags</span></span>           | <span data-ttu-id="bc472-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-225">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-226">Classes used in</span></span>        | [<span data-ttu-id="bc472-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc472-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc472-228">Windows Server 2008</span></span>



| <span data-ttu-id="bc472-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-229">Entry</span></span> | <span data-ttu-id="bc472-230">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-233">System-Only</span></span>            | <span data-ttu-id="bc472-234">True</span><span class="sxs-lookup"><span data-stu-id="bc472-234">True</span></span>                            |
| <span data-ttu-id="bc472-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-235">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-236">True</span><span class="sxs-lookup"><span data-stu-id="bc472-236">True</span></span>                            |
| <span data-ttu-id="bc472-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-237">Is Indexed</span></span>             | <span data-ttu-id="bc472-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-238">False</span></span>                           |
| <span data-ttu-id="bc472-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-239">In Global Catalog</span></span>      | <span data-ttu-id="bc472-240">True</span><span class="sxs-lookup"><span data-stu-id="bc472-240">True</span></span>                            |
| <span data-ttu-id="bc472-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-245">Search-Flags</span></span>           | <span data-ttu-id="bc472-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-246">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-247">System-Flags</span></span>           | <span data-ttu-id="bc472-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-248">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-249">Classes used in</span></span>        | [<span data-ttu-id="bc472-250">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc472-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc472-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc472-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-252">Entry</span></span> | <span data-ttu-id="bc472-253">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-256">System-Only</span></span>            | <span data-ttu-id="bc472-257">True</span><span class="sxs-lookup"><span data-stu-id="bc472-257">True</span></span>                            |
| <span data-ttu-id="bc472-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-258">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-259">True</span><span class="sxs-lookup"><span data-stu-id="bc472-259">True</span></span>                            |
| <span data-ttu-id="bc472-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-260">Is Indexed</span></span>             | <span data-ttu-id="bc472-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-261">False</span></span>                           |
| <span data-ttu-id="bc472-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-262">In Global Catalog</span></span>      | <span data-ttu-id="bc472-263">True</span><span class="sxs-lookup"><span data-stu-id="bc472-263">True</span></span>                            |
| <span data-ttu-id="bc472-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-268">Search-Flags</span></span>           | <span data-ttu-id="bc472-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-269">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-270">System-Flags</span></span>           | <span data-ttu-id="bc472-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-271">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-272">Classes used in</span></span>        | [<span data-ttu-id="bc472-273">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc472-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc472-274">Windows Server 2012</span></span>



| <span data-ttu-id="bc472-275">Ввод</span><span class="sxs-lookup"><span data-stu-id="bc472-275">Entry</span></span> | <span data-ttu-id="bc472-276">Значение</span><span class="sxs-lookup"><span data-stu-id="bc472-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc472-277">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bc472-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc472-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bc472-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc472-279">System-Only</span></span>            | <span data-ttu-id="bc472-280">True</span><span class="sxs-lookup"><span data-stu-id="bc472-280">True</span></span>                            |
| <span data-ttu-id="bc472-281">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bc472-281">Is-Single-Valued</span></span>       | <span data-ttu-id="bc472-282">True</span><span class="sxs-lookup"><span data-stu-id="bc472-282">True</span></span>                            |
| <span data-ttu-id="bc472-283">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bc472-283">Is Indexed</span></span>             | <span data-ttu-id="bc472-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="bc472-284">False</span></span>                           |
| <span data-ttu-id="bc472-285">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bc472-285">In Global Catalog</span></span>      | <span data-ttu-id="bc472-286">True</span><span class="sxs-lookup"><span data-stu-id="bc472-286">True</span></span>                            |
| <span data-ttu-id="bc472-287">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bc472-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc472-288">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bc472-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc472-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc472-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc472-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc472-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc472-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-291">Search-Flags</span></span>           | <span data-ttu-id="bc472-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc472-292">0x00000000</span></span>                      |
| <span data-ttu-id="bc472-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc472-293">System-Flags</span></span>           | <span data-ttu-id="bc472-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc472-294">0x00000013</span></span>                      |
| <span data-ttu-id="bc472-295">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bc472-295">Classes used in</span></span>        | [<span data-ttu-id="bc472-296">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bc472-296">**Top**</span></span>](c-top.md)<br/> |



 

 





