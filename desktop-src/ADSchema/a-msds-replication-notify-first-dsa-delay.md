---
title: Атрибут ms-DS-Replication-notify-First-DSA-Delay
description: Этот атрибут управляет задержкой между изменениями в DS и уведомлением первого участника реплики для NC.
ms.assetid: 58474bf9-9069-402a-a94b-4d1b6df0810e
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута "MS-DS-Replication-уведомлять-First-DSA — задержка"
- msDS-Replication-Schema-First-DSA-схема AD атрибута с задержкой
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-First-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a981ff257562e701b12e3855b279b7995721e39
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893485"
---
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="a0e00-105">Атрибут ms-DS-Replication-notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="a0e00-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="a0e00-106">Этот атрибут управляет задержкой между изменениями в DS и уведомлением первого участника реплики для NC.</span><span class="sxs-lookup"><span data-stu-id="a0e00-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="a0e00-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-107">Entry</span></span> | <span data-ttu-id="a0e00-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="a0e00-109">CN</span><span class="sxs-lookup"><span data-stu-id="a0e00-109">CN</span></span>                | <span data-ttu-id="a0e00-110">MS-DS-Replication-уведомлять-First-DSA — задержка</span><span class="sxs-lookup"><span data-stu-id="a0e00-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="a0e00-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a0e00-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a0e00-112">msDS-Replication-уведомлять-First-DSA — задержка</span><span class="sxs-lookup"><span data-stu-id="a0e00-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="a0e00-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a0e00-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="a0e00-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a0e00-114">Update Privilege</span></span>  | <span data-ttu-id="a0e00-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="a0e00-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="a0e00-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a0e00-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="a0e00-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-117">Attribute-Id</span></span>      | <span data-ttu-id="a0e00-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="a0e00-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="a0e00-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a0e00-119">System-Id-Guid</span></span>    | <span data-ttu-id="a0e00-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="a0e00-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="a0e00-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e00-121">Syntax</span></span>            | [<span data-ttu-id="a0e00-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a0e00-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="a0e00-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a0e00-123">Implementations</span></span>

-   [<span data-ttu-id="a0e00-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0e00-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0e00-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a0e00-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a0e00-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0e00-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0e00-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0e00-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0e00-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0e00-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0e00-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0e00-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a0e00-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0e00-130">Windows Server 2003</span></span>



| <span data-ttu-id="a0e00-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-131">Entry</span></span> | <span data-ttu-id="a0e00-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a0e00-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a0e00-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0e00-135">System-Only</span></span>            | <span data-ttu-id="a0e00-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-136">False</span></span>                                      |
| <span data-ttu-id="a0e00-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a0e00-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a0e00-138">True</span><span class="sxs-lookup"><span data-stu-id="a0e00-138">True</span></span>                                       |
| <span data-ttu-id="a0e00-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a0e00-139">Is Indexed</span></span>             | <span data-ttu-id="a0e00-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-140">False</span></span>                                      |
| <span data-ttu-id="a0e00-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a0e00-141">In Global Catalog</span></span>      | <span data-ttu-id="a0e00-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-142">False</span></span>                                      |
| <span data-ttu-id="a0e00-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a0e00-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0e00-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0e00-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a0e00-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0e00-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0e00-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-147">Search-Flags</span></span>           | <span data-ttu-id="a0e00-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0e00-148">0x00000000</span></span>                                 |
| <span data-ttu-id="a0e00-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-149">System-Flags</span></span>           | <span data-ttu-id="a0e00-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0e00-150">0x00000010</span></span>                                 |
| <span data-ttu-id="a0e00-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a0e00-151">Classes used in</span></span>        | [<span data-ttu-id="a0e00-152">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a0e00-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a0e00-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="a0e00-153">ADAM</span></span>



| <span data-ttu-id="a0e00-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-154">Entry</span></span> | <span data-ttu-id="a0e00-155">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a0e00-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a0e00-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0e00-158">System-Only</span></span>            | <span data-ttu-id="a0e00-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-159">False</span></span>                                      |
| <span data-ttu-id="a0e00-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a0e00-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a0e00-161">True</span><span class="sxs-lookup"><span data-stu-id="a0e00-161">True</span></span>                                       |
| <span data-ttu-id="a0e00-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a0e00-162">Is Indexed</span></span>             | <span data-ttu-id="a0e00-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-163">False</span></span>                                      |
| <span data-ttu-id="a0e00-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a0e00-164">In Global Catalog</span></span>      | <span data-ttu-id="a0e00-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-165">False</span></span>                                      |
| <span data-ttu-id="a0e00-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a0e00-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0e00-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0e00-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a0e00-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0e00-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0e00-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-170">Search-Flags</span></span>           | <span data-ttu-id="a0e00-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0e00-171">0x00000000</span></span>                                 |
| <span data-ttu-id="a0e00-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-172">System-Flags</span></span>           | <span data-ttu-id="a0e00-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0e00-173">0x00000010</span></span>                                 |
| <span data-ttu-id="a0e00-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a0e00-174">Classes used in</span></span>        | [<span data-ttu-id="a0e00-175">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a0e00-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0e00-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0e00-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0e00-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-177">Entry</span></span> | <span data-ttu-id="a0e00-178">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a0e00-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a0e00-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0e00-181">System-Only</span></span>            | <span data-ttu-id="a0e00-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-182">False</span></span>                                      |
| <span data-ttu-id="a0e00-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a0e00-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a0e00-184">True</span><span class="sxs-lookup"><span data-stu-id="a0e00-184">True</span></span>                                       |
| <span data-ttu-id="a0e00-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a0e00-185">Is Indexed</span></span>             | <span data-ttu-id="a0e00-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-186">False</span></span>                                      |
| <span data-ttu-id="a0e00-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a0e00-187">In Global Catalog</span></span>      | <span data-ttu-id="a0e00-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-188">False</span></span>                                      |
| <span data-ttu-id="a0e00-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a0e00-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0e00-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0e00-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a0e00-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0e00-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0e00-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-193">Search-Flags</span></span>           | <span data-ttu-id="a0e00-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0e00-194">0x00000000</span></span>                                 |
| <span data-ttu-id="a0e00-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-195">System-Flags</span></span>           | <span data-ttu-id="a0e00-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0e00-196">0x00000010</span></span>                                 |
| <span data-ttu-id="a0e00-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a0e00-197">Classes used in</span></span>        | [<span data-ttu-id="a0e00-198">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a0e00-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0e00-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0e00-199">Windows Server 2008</span></span>



| <span data-ttu-id="a0e00-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-200">Entry</span></span> | <span data-ttu-id="a0e00-201">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a0e00-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a0e00-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0e00-204">System-Only</span></span>            | <span data-ttu-id="a0e00-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-205">False</span></span>                                      |
| <span data-ttu-id="a0e00-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a0e00-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a0e00-207">True</span><span class="sxs-lookup"><span data-stu-id="a0e00-207">True</span></span>                                       |
| <span data-ttu-id="a0e00-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a0e00-208">Is Indexed</span></span>             | <span data-ttu-id="a0e00-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-209">False</span></span>                                      |
| <span data-ttu-id="a0e00-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a0e00-210">In Global Catalog</span></span>      | <span data-ttu-id="a0e00-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-211">False</span></span>                                      |
| <span data-ttu-id="a0e00-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a0e00-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0e00-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0e00-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a0e00-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0e00-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0e00-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-216">Search-Flags</span></span>           | <span data-ttu-id="a0e00-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0e00-217">0x00000000</span></span>                                 |
| <span data-ttu-id="a0e00-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-218">System-Flags</span></span>           | <span data-ttu-id="a0e00-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0e00-219">0x00000010</span></span>                                 |
| <span data-ttu-id="a0e00-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a0e00-220">Classes used in</span></span>        | [<span data-ttu-id="a0e00-221">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a0e00-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0e00-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0e00-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0e00-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-223">Entry</span></span> | <span data-ttu-id="a0e00-224">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a0e00-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a0e00-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0e00-227">System-Only</span></span>            | <span data-ttu-id="a0e00-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-228">False</span></span>                                      |
| <span data-ttu-id="a0e00-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a0e00-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a0e00-230">True</span><span class="sxs-lookup"><span data-stu-id="a0e00-230">True</span></span>                                       |
| <span data-ttu-id="a0e00-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a0e00-231">Is Indexed</span></span>             | <span data-ttu-id="a0e00-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-232">False</span></span>                                      |
| <span data-ttu-id="a0e00-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a0e00-233">In Global Catalog</span></span>      | <span data-ttu-id="a0e00-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-234">False</span></span>                                      |
| <span data-ttu-id="a0e00-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a0e00-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0e00-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0e00-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a0e00-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0e00-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0e00-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-239">Search-Flags</span></span>           | <span data-ttu-id="a0e00-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0e00-240">0x00000000</span></span>                                 |
| <span data-ttu-id="a0e00-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-241">System-Flags</span></span>           | <span data-ttu-id="a0e00-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0e00-242">0x00000010</span></span>                                 |
| <span data-ttu-id="a0e00-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a0e00-243">Classes used in</span></span>        | [<span data-ttu-id="a0e00-244">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a0e00-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0e00-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0e00-245">Windows Server 2012</span></span>



| <span data-ttu-id="a0e00-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="a0e00-246">Entry</span></span> | <span data-ttu-id="a0e00-247">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e00-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a0e00-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a0e00-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0e00-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a0e00-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0e00-250">System-Only</span></span>            | <span data-ttu-id="a0e00-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-251">False</span></span>                                      |
| <span data-ttu-id="a0e00-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a0e00-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a0e00-253">True</span><span class="sxs-lookup"><span data-stu-id="a0e00-253">True</span></span>                                       |
| <span data-ttu-id="a0e00-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a0e00-254">Is Indexed</span></span>             | <span data-ttu-id="a0e00-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-255">False</span></span>                                      |
| <span data-ttu-id="a0e00-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a0e00-256">In Global Catalog</span></span>      | <span data-ttu-id="a0e00-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="a0e00-257">False</span></span>                                      |
| <span data-ttu-id="a0e00-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a0e00-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0e00-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0e00-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a0e00-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0e00-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0e00-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a0e00-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-262">Search-Flags</span></span>           | <span data-ttu-id="a0e00-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0e00-263">0x00000000</span></span>                                 |
| <span data-ttu-id="a0e00-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0e00-264">System-Flags</span></span>           | <span data-ttu-id="a0e00-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0e00-265">0x00000010</span></span>                                 |
| <span data-ttu-id="a0e00-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a0e00-266">Classes used in</span></span>        | [<span data-ttu-id="a0e00-267">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="a0e00-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





