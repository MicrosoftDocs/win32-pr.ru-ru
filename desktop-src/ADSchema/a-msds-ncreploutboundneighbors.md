---
title: Атрибут ms-DS-NC-REPL-Outbound-соседи
description: Партнеры репликации для этой секции. Этот сервер отправляет данные репликации на эти серверы, которые выступают в качестве назначений. Этот сервер будет уведомлять эти серверы о доступности новых данных.
ms.assetid: 9dcc7485-1999-47ff-bb57-8193768a15a9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-NC-REPL-Outbound-соседи
- Схема AD атрибута msDS-Нкреплаутбаунднеигхборс
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Outbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fd37ccab1b3faef6ca2c84a52c05249a52ff38a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893506"
---
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="039f8-107">Атрибут ms-DS-NC-REPL-Outbound-соседи</span><span class="sxs-lookup"><span data-stu-id="039f8-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="039f8-108">Партнеры репликации для этой секции.</span><span class="sxs-lookup"><span data-stu-id="039f8-108">Replication partners for this partition.</span></span> <span data-ttu-id="039f8-109">Этот сервер отправляет данные репликации на эти серверы, которые выступают в качестве назначений.</span><span class="sxs-lookup"><span data-stu-id="039f8-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="039f8-110">Этот сервер будет уведомлять эти серверы о доступности новых данных.</span><span class="sxs-lookup"><span data-stu-id="039f8-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="039f8-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-111">Entry</span></span> | <span data-ttu-id="039f8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="039f8-113">CN</span><span class="sxs-lookup"><span data-stu-id="039f8-113">CN</span></span>                | <span data-ttu-id="039f8-114">MS-DS-NC-REPL-Outbound-соседи</span><span class="sxs-lookup"><span data-stu-id="039f8-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="039f8-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="039f8-115">Ldap-Display-Name</span></span> | <span data-ttu-id="039f8-116">msDS-Нкреплаутбаунднеигхборс</span><span class="sxs-lookup"><span data-stu-id="039f8-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="039f8-117">Размер</span><span class="sxs-lookup"><span data-stu-id="039f8-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="039f8-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="039f8-118">Update Privilege</span></span>  | <span data-ttu-id="039f8-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="039f8-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="039f8-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="039f8-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="039f8-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-121">Attribute-Id</span></span>      | <span data-ttu-id="039f8-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="039f8-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="039f8-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="039f8-123">System-Id-Guid</span></span>    | <span data-ttu-id="039f8-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="039f8-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="039f8-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="039f8-125">Syntax</span></span>            | [<span data-ttu-id="039f8-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="039f8-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="039f8-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="039f8-127">Implementations</span></span>

-   [<span data-ttu-id="039f8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="039f8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="039f8-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="039f8-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="039f8-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="039f8-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="039f8-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="039f8-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="039f8-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="039f8-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="039f8-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="039f8-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="039f8-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="039f8-134">Windows Server 2003</span></span>



| <span data-ttu-id="039f8-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-135">Entry</span></span> | <span data-ttu-id="039f8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="039f8-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="039f8-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="039f8-139">System-Only</span></span>            | <span data-ttu-id="039f8-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-140">False</span></span>                           |
| <span data-ttu-id="039f8-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="039f8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="039f8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-142">False</span></span>                           |
| <span data-ttu-id="039f8-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="039f8-143">Is Indexed</span></span>             | <span data-ttu-id="039f8-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-144">False</span></span>                           |
| <span data-ttu-id="039f8-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="039f8-145">In Global Catalog</span></span>      | <span data-ttu-id="039f8-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-146">False</span></span>                           |
| <span data-ttu-id="039f8-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="039f8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="039f8-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="039f8-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="039f8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="039f8-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="039f8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="039f8-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="039f8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-151">Search-Flags</span></span>           | <span data-ttu-id="039f8-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="039f8-152">0x00000000</span></span>                      |
| <span data-ttu-id="039f8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-153">System-Flags</span></span>           | <span data-ttu-id="039f8-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="039f8-154">0x00000014</span></span>                      |
| <span data-ttu-id="039f8-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="039f8-155">Classes used in</span></span>        | [<span data-ttu-id="039f8-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="039f8-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="039f8-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="039f8-157">ADAM</span></span>



| <span data-ttu-id="039f8-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-158">Entry</span></span> | <span data-ttu-id="039f8-159">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="039f8-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="039f8-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="039f8-162">System-Only</span></span>            | <span data-ttu-id="039f8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-163">False</span></span>                           |
| <span data-ttu-id="039f8-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="039f8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="039f8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-165">False</span></span>                           |
| <span data-ttu-id="039f8-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="039f8-166">Is Indexed</span></span>             | <span data-ttu-id="039f8-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-167">False</span></span>                           |
| <span data-ttu-id="039f8-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="039f8-168">In Global Catalog</span></span>      | <span data-ttu-id="039f8-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-169">False</span></span>                           |
| <span data-ttu-id="039f8-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="039f8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="039f8-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="039f8-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="039f8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="039f8-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="039f8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="039f8-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="039f8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-174">Search-Flags</span></span>           | <span data-ttu-id="039f8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="039f8-175">0x00000000</span></span>                      |
| <span data-ttu-id="039f8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-176">System-Flags</span></span>           | <span data-ttu-id="039f8-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="039f8-177">0x00000014</span></span>                      |
| <span data-ttu-id="039f8-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="039f8-178">Classes used in</span></span>        | [<span data-ttu-id="039f8-179">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="039f8-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="039f8-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="039f8-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="039f8-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-181">Entry</span></span> | <span data-ttu-id="039f8-182">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="039f8-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="039f8-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="039f8-185">System-Only</span></span>            | <span data-ttu-id="039f8-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-186">False</span></span>                           |
| <span data-ttu-id="039f8-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="039f8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="039f8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-188">False</span></span>                           |
| <span data-ttu-id="039f8-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="039f8-189">Is Indexed</span></span>             | <span data-ttu-id="039f8-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-190">False</span></span>                           |
| <span data-ttu-id="039f8-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="039f8-191">In Global Catalog</span></span>      | <span data-ttu-id="039f8-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-192">False</span></span>                           |
| <span data-ttu-id="039f8-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="039f8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="039f8-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="039f8-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="039f8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="039f8-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="039f8-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="039f8-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="039f8-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-197">Search-Flags</span></span>           | <span data-ttu-id="039f8-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="039f8-198">0x00000000</span></span>                      |
| <span data-ttu-id="039f8-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-199">System-Flags</span></span>           | <span data-ttu-id="039f8-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="039f8-200">0x00000014</span></span>                      |
| <span data-ttu-id="039f8-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="039f8-201">Classes used in</span></span>        | [<span data-ttu-id="039f8-202">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="039f8-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="039f8-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="039f8-203">Windows Server 2008</span></span>



| <span data-ttu-id="039f8-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-204">Entry</span></span> | <span data-ttu-id="039f8-205">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="039f8-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="039f8-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="039f8-208">System-Only</span></span>            | <span data-ttu-id="039f8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-209">False</span></span>                           |
| <span data-ttu-id="039f8-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="039f8-210">Is-Single-Valued</span></span>       | <span data-ttu-id="039f8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-211">False</span></span>                           |
| <span data-ttu-id="039f8-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="039f8-212">Is Indexed</span></span>             | <span data-ttu-id="039f8-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-213">False</span></span>                           |
| <span data-ttu-id="039f8-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="039f8-214">In Global Catalog</span></span>      | <span data-ttu-id="039f8-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-215">False</span></span>                           |
| <span data-ttu-id="039f8-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="039f8-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="039f8-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="039f8-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="039f8-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="039f8-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="039f8-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="039f8-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="039f8-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-220">Search-Flags</span></span>           | <span data-ttu-id="039f8-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="039f8-221">0x00000000</span></span>                      |
| <span data-ttu-id="039f8-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-222">System-Flags</span></span>           | <span data-ttu-id="039f8-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="039f8-223">0x00000014</span></span>                      |
| <span data-ttu-id="039f8-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="039f8-224">Classes used in</span></span>        | [<span data-ttu-id="039f8-225">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="039f8-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="039f8-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="039f8-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="039f8-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-227">Entry</span></span> | <span data-ttu-id="039f8-228">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="039f8-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="039f8-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="039f8-231">System-Only</span></span>            | <span data-ttu-id="039f8-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-232">False</span></span>                           |
| <span data-ttu-id="039f8-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="039f8-233">Is-Single-Valued</span></span>       | <span data-ttu-id="039f8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-234">False</span></span>                           |
| <span data-ttu-id="039f8-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="039f8-235">Is Indexed</span></span>             | <span data-ttu-id="039f8-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-236">False</span></span>                           |
| <span data-ttu-id="039f8-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="039f8-237">In Global Catalog</span></span>      | <span data-ttu-id="039f8-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-238">False</span></span>                           |
| <span data-ttu-id="039f8-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="039f8-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="039f8-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="039f8-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="039f8-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="039f8-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="039f8-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="039f8-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="039f8-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-243">Search-Flags</span></span>           | <span data-ttu-id="039f8-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="039f8-244">0x00000000</span></span>                      |
| <span data-ttu-id="039f8-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-245">System-Flags</span></span>           | <span data-ttu-id="039f8-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="039f8-246">0x00000014</span></span>                      |
| <span data-ttu-id="039f8-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="039f8-247">Classes used in</span></span>        | [<span data-ttu-id="039f8-248">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="039f8-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="039f8-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="039f8-249">Windows Server 2012</span></span>



| <span data-ttu-id="039f8-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="039f8-250">Entry</span></span> | <span data-ttu-id="039f8-251">Значение</span><span class="sxs-lookup"><span data-stu-id="039f8-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="039f8-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="039f8-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="039f8-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="039f8-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="039f8-254">System-Only</span></span>            | <span data-ttu-id="039f8-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-255">False</span></span>                           |
| <span data-ttu-id="039f8-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="039f8-256">Is-Single-Valued</span></span>       | <span data-ttu-id="039f8-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-257">False</span></span>                           |
| <span data-ttu-id="039f8-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="039f8-258">Is Indexed</span></span>             | <span data-ttu-id="039f8-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-259">False</span></span>                           |
| <span data-ttu-id="039f8-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="039f8-260">In Global Catalog</span></span>      | <span data-ttu-id="039f8-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="039f8-261">False</span></span>                           |
| <span data-ttu-id="039f8-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="039f8-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="039f8-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="039f8-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="039f8-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="039f8-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="039f8-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="039f8-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="039f8-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-266">Search-Flags</span></span>           | <span data-ttu-id="039f8-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="039f8-267">0x00000000</span></span>                      |
| <span data-ttu-id="039f8-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="039f8-268">System-Flags</span></span>           | <span data-ttu-id="039f8-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="039f8-269">0x00000014</span></span>                      |
| <span data-ttu-id="039f8-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="039f8-270">Classes used in</span></span>        | [<span data-ttu-id="039f8-271">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="039f8-271">**Top**</span></span>](c-top.md)<br/> |



 

 





