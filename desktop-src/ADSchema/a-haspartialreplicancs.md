---
title: Атрибут WITH-PARTIAL-реплики NC
description: Одноуровневый элемент с атрибутом-Master-NC. Имеет-partial-реплика-NCS отражает различающееся имя всех контекстов именования других доменов, которые были реплицированы в глобальный каталог.
ms.assetid: 2501bbb3-74b5-4604-b0c0-8653fc092e1c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "содержит-partial-реплика-NC"
- Схема AD атрибута Хаспартиалрепликанкс
topic_type:
- apiref
api_name:
- Has-Partial-Replica-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f284df094c909b01b88a4853ed7c4a41dee9f31a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804313"
---
# <a name="has-partial-replica-ncs-attribute"></a><span data-ttu-id="56b11-106">Атрибут WITH-PARTIAL-реплики NC</span><span class="sxs-lookup"><span data-stu-id="56b11-106">Has-Partial-Replica-NCs attribute</span></span>

<span data-ttu-id="56b11-107">Одноуровневый элемент с атрибутом-Master-NC.</span><span class="sxs-lookup"><span data-stu-id="56b11-107">Sibling to Has-Master-NCs.</span></span> <span data-ttu-id="56b11-108">Имеет-partial-реплика-NCS отражает различающееся имя всех контекстов именования других доменов, которые были реплицированы в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="56b11-108">Has-Partial-Replica-NCs reflects the distinguished name for all other-domain NCs that have been replicated into a global catalog.</span></span>



| <span data-ttu-id="56b11-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-109">Entry</span></span> | <span data-ttu-id="56b11-110">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="56b11-111">CN</span><span class="sxs-lookup"><span data-stu-id="56b11-111">CN</span></span>                | <span data-ttu-id="56b11-112">Имеет-partial-реплика-NC</span><span class="sxs-lookup"><span data-stu-id="56b11-112">Has-Partial-Replica-NCs</span></span>                 |
| <span data-ttu-id="56b11-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="56b11-113">Ldap-Display-Name</span></span> | <span data-ttu-id="56b11-114">хаспартиалрепликанкс</span><span class="sxs-lookup"><span data-stu-id="56b11-114">hasPartialReplicaNCs</span></span>                    |
| <span data-ttu-id="56b11-115">Размер</span><span class="sxs-lookup"><span data-stu-id="56b11-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="56b11-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="56b11-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="56b11-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="56b11-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="56b11-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-118">Attribute-Id</span></span>      | <span data-ttu-id="56b11-119">1.2.840.113556.1.2.15</span><span class="sxs-lookup"><span data-stu-id="56b11-119">1.2.840.113556.1.2.15</span></span>                   |
| <span data-ttu-id="56b11-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="56b11-120">System-Id-Guid</span></span>    | <span data-ttu-id="56b11-121">bf967981-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="56b11-121">bf967981-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="56b11-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56b11-122">Syntax</span></span>            | [<span data-ttu-id="56b11-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="56b11-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="56b11-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="56b11-124">Implementations</span></span>

-   [<span data-ttu-id="56b11-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="56b11-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="56b11-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56b11-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56b11-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="56b11-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="56b11-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56b11-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56b11-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56b11-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56b11-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56b11-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56b11-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56b11-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="56b11-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56b11-132">Windows 2000 Server</span></span>



| <span data-ttu-id="56b11-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-133">Entry</span></span> | <span data-ttu-id="56b11-134">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-135">Link-Id</span></span>                | <span data-ttu-id="56b11-136">74</span><span class="sxs-lookup"><span data-stu-id="56b11-136">74</span></span>                                       |
| <span data-ttu-id="56b11-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-137">MAPI-Id</span></span>                | <span data-ttu-id="56b11-138">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-138">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-139">System-Only</span></span>            | <span data-ttu-id="56b11-140">True</span><span class="sxs-lookup"><span data-stu-id="56b11-140">True</span></span>                                     |
| <span data-ttu-id="56b11-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-141">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-142">False</span></span>                                    |
| <span data-ttu-id="56b11-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-143">Is Indexed</span></span>             | <span data-ttu-id="56b11-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-144">False</span></span>                                    |
| <span data-ttu-id="56b11-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-145">In Global Catalog</span></span>      | <span data-ttu-id="56b11-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-146">False</span></span>                                    |
| <span data-ttu-id="56b11-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-151">Search-Flags</span></span>           | <span data-ttu-id="56b11-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-152">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-153">System-Flags</span></span>           | <span data-ttu-id="56b11-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-154">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-155">Classes used in</span></span>        | [<span data-ttu-id="56b11-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="56b11-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56b11-157">Windows Server 2003</span></span>



| <span data-ttu-id="56b11-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-158">Entry</span></span> | <span data-ttu-id="56b11-159">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-160">Link-Id</span></span>                | <span data-ttu-id="56b11-161">74</span><span class="sxs-lookup"><span data-stu-id="56b11-161">74</span></span>                                       |
| <span data-ttu-id="56b11-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-162">MAPI-Id</span></span>                | <span data-ttu-id="56b11-163">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-163">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-164">System-Only</span></span>            | <span data-ttu-id="56b11-165">True</span><span class="sxs-lookup"><span data-stu-id="56b11-165">True</span></span>                                     |
| <span data-ttu-id="56b11-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-166">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-167">False</span></span>                                    |
| <span data-ttu-id="56b11-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-168">Is Indexed</span></span>             | <span data-ttu-id="56b11-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-169">False</span></span>                                    |
| <span data-ttu-id="56b11-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-170">In Global Catalog</span></span>      | <span data-ttu-id="56b11-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-171">False</span></span>                                    |
| <span data-ttu-id="56b11-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-176">Search-Flags</span></span>           | <span data-ttu-id="56b11-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-177">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-178">System-Flags</span></span>           | <span data-ttu-id="56b11-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-179">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-180">Classes used in</span></span>        | [<span data-ttu-id="56b11-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="56b11-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="56b11-182">ADAM</span></span>



| <span data-ttu-id="56b11-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-183">Entry</span></span> | <span data-ttu-id="56b11-184">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-185">Link-Id</span></span>                | <span data-ttu-id="56b11-186">74</span><span class="sxs-lookup"><span data-stu-id="56b11-186">74</span></span>                                       |
| <span data-ttu-id="56b11-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-187">MAPI-Id</span></span>                | <span data-ttu-id="56b11-188">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-188">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-189">System-Only</span></span>            | <span data-ttu-id="56b11-190">True</span><span class="sxs-lookup"><span data-stu-id="56b11-190">True</span></span>                                     |
| <span data-ttu-id="56b11-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-191">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-192">False</span></span>                                    |
| <span data-ttu-id="56b11-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-193">Is Indexed</span></span>             | <span data-ttu-id="56b11-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-194">False</span></span>                                    |
| <span data-ttu-id="56b11-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-195">In Global Catalog</span></span>      | <span data-ttu-id="56b11-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-196">False</span></span>                                    |
| <span data-ttu-id="56b11-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-201">Search-Flags</span></span>           | <span data-ttu-id="56b11-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-202">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-203">System-Flags</span></span>           | <span data-ttu-id="56b11-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-204">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-205">Classes used in</span></span>        | [<span data-ttu-id="56b11-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56b11-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56b11-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56b11-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-208">Entry</span></span> | <span data-ttu-id="56b11-209">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-210">Link-Id</span></span>                | <span data-ttu-id="56b11-211">74</span><span class="sxs-lookup"><span data-stu-id="56b11-211">74</span></span>                                       |
| <span data-ttu-id="56b11-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-212">MAPI-Id</span></span>                | <span data-ttu-id="56b11-213">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-213">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-214">System-Only</span></span>            | <span data-ttu-id="56b11-215">True</span><span class="sxs-lookup"><span data-stu-id="56b11-215">True</span></span>                                     |
| <span data-ttu-id="56b11-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-216">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-217">False</span></span>                                    |
| <span data-ttu-id="56b11-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-218">Is Indexed</span></span>             | <span data-ttu-id="56b11-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-219">False</span></span>                                    |
| <span data-ttu-id="56b11-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-220">In Global Catalog</span></span>      | <span data-ttu-id="56b11-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-221">False</span></span>                                    |
| <span data-ttu-id="56b11-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-226">Search-Flags</span></span>           | <span data-ttu-id="56b11-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-227">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-228">System-Flags</span></span>           | <span data-ttu-id="56b11-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-229">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-230">Classes used in</span></span>        | [<span data-ttu-id="56b11-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56b11-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56b11-232">Windows Server 2008</span></span>



| <span data-ttu-id="56b11-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-233">Entry</span></span> | <span data-ttu-id="56b11-234">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-235">Link-Id</span></span>                | <span data-ttu-id="56b11-236">74</span><span class="sxs-lookup"><span data-stu-id="56b11-236">74</span></span>                                       |
| <span data-ttu-id="56b11-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-237">MAPI-Id</span></span>                | <span data-ttu-id="56b11-238">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-238">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-239">System-Only</span></span>            | <span data-ttu-id="56b11-240">True</span><span class="sxs-lookup"><span data-stu-id="56b11-240">True</span></span>                                     |
| <span data-ttu-id="56b11-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-241">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-242">False</span></span>                                    |
| <span data-ttu-id="56b11-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-243">Is Indexed</span></span>             | <span data-ttu-id="56b11-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-244">False</span></span>                                    |
| <span data-ttu-id="56b11-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-245">In Global Catalog</span></span>      | <span data-ttu-id="56b11-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-246">False</span></span>                                    |
| <span data-ttu-id="56b11-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-251">Search-Flags</span></span>           | <span data-ttu-id="56b11-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-252">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-253">System-Flags</span></span>           | <span data-ttu-id="56b11-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-254">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-255">Classes used in</span></span>        | [<span data-ttu-id="56b11-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56b11-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56b11-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56b11-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-258">Entry</span></span> | <span data-ttu-id="56b11-259">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-260">Link-Id</span></span>                | <span data-ttu-id="56b11-261">74</span><span class="sxs-lookup"><span data-stu-id="56b11-261">74</span></span>                                       |
| <span data-ttu-id="56b11-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-262">MAPI-Id</span></span>                | <span data-ttu-id="56b11-263">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-263">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-264">System-Only</span></span>            | <span data-ttu-id="56b11-265">True</span><span class="sxs-lookup"><span data-stu-id="56b11-265">True</span></span>                                     |
| <span data-ttu-id="56b11-266">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-266">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-267">False</span></span>                                    |
| <span data-ttu-id="56b11-268">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-268">Is Indexed</span></span>             | <span data-ttu-id="56b11-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-269">False</span></span>                                    |
| <span data-ttu-id="56b11-270">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-270">In Global Catalog</span></span>      | <span data-ttu-id="56b11-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-271">False</span></span>                                    |
| <span data-ttu-id="56b11-272">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-273">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-276">Search-Flags</span></span>           | <span data-ttu-id="56b11-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-277">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-278">System-Flags</span></span>           | <span data-ttu-id="56b11-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-279">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-280">Classes used in</span></span>        | [<span data-ttu-id="56b11-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56b11-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56b11-282">Windows Server 2012</span></span>



| <span data-ttu-id="56b11-283">Ввод</span><span class="sxs-lookup"><span data-stu-id="56b11-283">Entry</span></span> | <span data-ttu-id="56b11-284">Значение</span><span class="sxs-lookup"><span data-stu-id="56b11-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="56b11-285">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56b11-285">Link-Id</span></span>                | <span data-ttu-id="56b11-286">74</span><span class="sxs-lookup"><span data-stu-id="56b11-286">74</span></span>                                       |
| <span data-ttu-id="56b11-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56b11-287">MAPI-Id</span></span>                | <span data-ttu-id="56b11-288">0x80B5</span><span class="sxs-lookup"><span data-stu-id="56b11-288">0x80B5</span></span>                                   |
| <span data-ttu-id="56b11-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="56b11-289">System-Only</span></span>            | <span data-ttu-id="56b11-290">True</span><span class="sxs-lookup"><span data-stu-id="56b11-290">True</span></span>                                     |
| <span data-ttu-id="56b11-291">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56b11-291">Is-Single-Valued</span></span>       | <span data-ttu-id="56b11-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-292">False</span></span>                                    |
| <span data-ttu-id="56b11-293">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56b11-293">Is Indexed</span></span>             | <span data-ttu-id="56b11-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-294">False</span></span>                                    |
| <span data-ttu-id="56b11-295">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56b11-295">In Global Catalog</span></span>      | <span data-ttu-id="56b11-296">Неверно</span><span class="sxs-lookup"><span data-stu-id="56b11-296">False</span></span>                                    |
| <span data-ttu-id="56b11-297">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56b11-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="56b11-298">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56b11-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="56b11-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56b11-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="56b11-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56b11-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="56b11-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-301">Search-Flags</span></span>           | <span data-ttu-id="56b11-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56b11-302">0x00000000</span></span>                               |
| <span data-ttu-id="56b11-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56b11-303">System-Flags</span></span>           | <span data-ttu-id="56b11-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56b11-304">0x00000010</span></span>                               |
| <span data-ttu-id="56b11-305">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56b11-305">Classes used in</span></span>        | [<span data-ttu-id="56b11-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="56b11-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





