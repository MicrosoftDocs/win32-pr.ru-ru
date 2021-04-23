---
title: Атрибут ms-DS-Replication-notify-последующего-DSA-Delay
description: Этот атрибут управляет задержкой между уведомлениями каждого последующего участника реплики для NC.
ms.assetid: 6bd9fed7-2003-4156-b1a0-da8622dc2ca8
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Replication-notify-последующего-DSA-Delay
- Схема AD атрибута msDS-Replication-notify-последующего-DSA-Delay
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-Subsequent-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd8b267309fa8d017ace926f7497ca210fb2b00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536257"
---
# <a name="ms-ds-replication-notify-subsequent-dsa-delay-attribute"></a><span data-ttu-id="ad685-105">Атрибут ms-DS-Replication-notify-последующего-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="ad685-105">ms-DS-Replication-Notify-Subsequent-DSA-Delay attribute</span></span>

<span data-ttu-id="ad685-106">Этот атрибут управляет задержкой между уведомлениями каждого последующего участника реплики для NC.</span><span class="sxs-lookup"><span data-stu-id="ad685-106">This attribute controls the delay in time between notification of each subsequent replica partner for an NC.</span></span>



| <span data-ttu-id="ad685-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-107">Entry</span></span> | <span data-ttu-id="ad685-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-108">Value</span></span> |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="ad685-109">CN</span><span class="sxs-lookup"><span data-stu-id="ad685-109">CN</span></span>                | <span data-ttu-id="ad685-110">MS-DS-Replication-notify-последующий-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="ad685-110">ms-DS-Replication-Notify-Subsequent-DSA-Delay</span></span> |
| <span data-ttu-id="ad685-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ad685-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ad685-112">msDS-Replication-notify-последующий-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="ad685-112">msDS-Replication-Notify-Subsequent-DSA-Delay</span></span>  |
| <span data-ttu-id="ad685-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ad685-113">Size</span></span>              | \-                                            |
| <span data-ttu-id="ad685-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ad685-114">Update Privilege</span></span>  | <span data-ttu-id="ad685-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="ad685-115">This value is set by the system.</span></span>              |
| <span data-ttu-id="ad685-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ad685-116">Update Frequency</span></span>  | \-                                            |
| <span data-ttu-id="ad685-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-117">Attribute-Id</span></span>      | <span data-ttu-id="ad685-118">1.2.840.113556.1.4.1664</span><span class="sxs-lookup"><span data-stu-id="ad685-118">1.2.840.113556.1.4.1664</span></span>                       |
| <span data-ttu-id="ad685-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ad685-119">System-Id-Guid</span></span>    | <span data-ttu-id="ad685-120">d63db385-dd92-4b52-b1d8-0d3ecc0e86b6</span><span class="sxs-lookup"><span data-stu-id="ad685-120">d63db385-dd92-4b52-b1d8-0d3ecc0e86b6</span></span>          |
| <span data-ttu-id="ad685-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad685-121">Syntax</span></span>            | [<span data-ttu-id="ad685-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ad685-122">**Enumeration**</span></span>](s-enumeration.md)          |



## <a name="implementations"></a><span data-ttu-id="ad685-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ad685-123">Implementations</span></span>

-   [<span data-ttu-id="ad685-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad685-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad685-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ad685-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ad685-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad685-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad685-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad685-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad685-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad685-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad685-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad685-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ad685-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad685-130">Windows Server 2003</span></span>



| <span data-ttu-id="ad685-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-131">Entry</span></span> | <span data-ttu-id="ad685-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ad685-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad685-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad685-135">System-Only</span></span>            | <span data-ttu-id="ad685-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-136">False</span></span>                                      |
| <span data-ttu-id="ad685-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad685-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ad685-138">True</span><span class="sxs-lookup"><span data-stu-id="ad685-138">True</span></span>                                       |
| <span data-ttu-id="ad685-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad685-139">Is Indexed</span></span>             | <span data-ttu-id="ad685-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-140">False</span></span>                                      |
| <span data-ttu-id="ad685-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad685-141">In Global Catalog</span></span>      | <span data-ttu-id="ad685-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-142">False</span></span>                                      |
| <span data-ttu-id="ad685-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad685-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad685-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad685-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ad685-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad685-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="ad685-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad685-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="ad685-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-147">Search-Flags</span></span>           | <span data-ttu-id="ad685-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad685-148">0x00000000</span></span>                                 |
| <span data-ttu-id="ad685-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-149">System-Flags</span></span>           | <span data-ttu-id="ad685-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad685-150">0x00000010</span></span>                                 |
| <span data-ttu-id="ad685-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad685-151">Classes used in</span></span>        | [<span data-ttu-id="ad685-152">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="ad685-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ad685-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="ad685-153">ADAM</span></span>



| <span data-ttu-id="ad685-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-154">Entry</span></span> | <span data-ttu-id="ad685-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ad685-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad685-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad685-158">System-Only</span></span>            | <span data-ttu-id="ad685-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-159">False</span></span>                                      |
| <span data-ttu-id="ad685-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad685-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ad685-161">True</span><span class="sxs-lookup"><span data-stu-id="ad685-161">True</span></span>                                       |
| <span data-ttu-id="ad685-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad685-162">Is Indexed</span></span>             | <span data-ttu-id="ad685-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-163">False</span></span>                                      |
| <span data-ttu-id="ad685-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad685-164">In Global Catalog</span></span>      | <span data-ttu-id="ad685-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-165">False</span></span>                                      |
| <span data-ttu-id="ad685-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad685-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad685-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad685-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ad685-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad685-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="ad685-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad685-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="ad685-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-170">Search-Flags</span></span>           | <span data-ttu-id="ad685-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad685-171">0x00000000</span></span>                                 |
| <span data-ttu-id="ad685-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-172">System-Flags</span></span>           | <span data-ttu-id="ad685-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad685-173">0x00000010</span></span>                                 |
| <span data-ttu-id="ad685-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad685-174">Classes used in</span></span>        | [<span data-ttu-id="ad685-175">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="ad685-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad685-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad685-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad685-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-177">Entry</span></span> | <span data-ttu-id="ad685-178">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ad685-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad685-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad685-181">System-Only</span></span>            | <span data-ttu-id="ad685-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-182">False</span></span>                                      |
| <span data-ttu-id="ad685-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad685-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ad685-184">True</span><span class="sxs-lookup"><span data-stu-id="ad685-184">True</span></span>                                       |
| <span data-ttu-id="ad685-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad685-185">Is Indexed</span></span>             | <span data-ttu-id="ad685-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-186">False</span></span>                                      |
| <span data-ttu-id="ad685-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad685-187">In Global Catalog</span></span>      | <span data-ttu-id="ad685-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-188">False</span></span>                                      |
| <span data-ttu-id="ad685-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad685-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad685-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad685-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ad685-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad685-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="ad685-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad685-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="ad685-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-193">Search-Flags</span></span>           | <span data-ttu-id="ad685-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad685-194">0x00000000</span></span>                                 |
| <span data-ttu-id="ad685-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-195">System-Flags</span></span>           | <span data-ttu-id="ad685-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad685-196">0x00000010</span></span>                                 |
| <span data-ttu-id="ad685-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad685-197">Classes used in</span></span>        | [<span data-ttu-id="ad685-198">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="ad685-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad685-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad685-199">Windows Server 2008</span></span>



| <span data-ttu-id="ad685-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-200">Entry</span></span> | <span data-ttu-id="ad685-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ad685-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad685-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad685-204">System-Only</span></span>            | <span data-ttu-id="ad685-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-205">False</span></span>                                      |
| <span data-ttu-id="ad685-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad685-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ad685-207">True</span><span class="sxs-lookup"><span data-stu-id="ad685-207">True</span></span>                                       |
| <span data-ttu-id="ad685-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad685-208">Is Indexed</span></span>             | <span data-ttu-id="ad685-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-209">False</span></span>                                      |
| <span data-ttu-id="ad685-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad685-210">In Global Catalog</span></span>      | <span data-ttu-id="ad685-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-211">False</span></span>                                      |
| <span data-ttu-id="ad685-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad685-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad685-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad685-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ad685-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad685-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="ad685-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad685-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="ad685-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-216">Search-Flags</span></span>           | <span data-ttu-id="ad685-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad685-217">0x00000000</span></span>                                 |
| <span data-ttu-id="ad685-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-218">System-Flags</span></span>           | <span data-ttu-id="ad685-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad685-219">0x00000010</span></span>                                 |
| <span data-ttu-id="ad685-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad685-220">Classes used in</span></span>        | [<span data-ttu-id="ad685-221">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="ad685-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad685-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad685-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad685-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-223">Entry</span></span> | <span data-ttu-id="ad685-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ad685-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad685-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad685-227">System-Only</span></span>            | <span data-ttu-id="ad685-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-228">False</span></span>                                      |
| <span data-ttu-id="ad685-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad685-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ad685-230">True</span><span class="sxs-lookup"><span data-stu-id="ad685-230">True</span></span>                                       |
| <span data-ttu-id="ad685-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad685-231">Is Indexed</span></span>             | <span data-ttu-id="ad685-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-232">False</span></span>                                      |
| <span data-ttu-id="ad685-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad685-233">In Global Catalog</span></span>      | <span data-ttu-id="ad685-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-234">False</span></span>                                      |
| <span data-ttu-id="ad685-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad685-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad685-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad685-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ad685-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad685-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="ad685-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad685-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="ad685-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-239">Search-Flags</span></span>           | <span data-ttu-id="ad685-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad685-240">0x00000000</span></span>                                 |
| <span data-ttu-id="ad685-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-241">System-Flags</span></span>           | <span data-ttu-id="ad685-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad685-242">0x00000010</span></span>                                 |
| <span data-ttu-id="ad685-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad685-243">Classes used in</span></span>        | [<span data-ttu-id="ad685-244">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="ad685-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad685-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad685-245">Windows Server 2012</span></span>



| <span data-ttu-id="ad685-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad685-246">Entry</span></span> | <span data-ttu-id="ad685-247">Значение</span><span class="sxs-lookup"><span data-stu-id="ad685-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ad685-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad685-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad685-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ad685-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad685-250">System-Only</span></span>            | <span data-ttu-id="ad685-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-251">False</span></span>                                      |
| <span data-ttu-id="ad685-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad685-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ad685-253">True</span><span class="sxs-lookup"><span data-stu-id="ad685-253">True</span></span>                                       |
| <span data-ttu-id="ad685-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad685-254">Is Indexed</span></span>             | <span data-ttu-id="ad685-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-255">False</span></span>                                      |
| <span data-ttu-id="ad685-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad685-256">In Global Catalog</span></span>      | <span data-ttu-id="ad685-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad685-257">False</span></span>                                      |
| <span data-ttu-id="ad685-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad685-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad685-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad685-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ad685-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad685-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="ad685-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad685-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="ad685-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-262">Search-Flags</span></span>           | <span data-ttu-id="ad685-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad685-263">0x00000000</span></span>                                 |
| <span data-ttu-id="ad685-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad685-264">System-Flags</span></span>           | <span data-ttu-id="ad685-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad685-265">0x00000010</span></span>                                 |
| <span data-ttu-id="ad685-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad685-266">Classes used in</span></span>        | [<span data-ttu-id="ad685-267">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="ad685-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





