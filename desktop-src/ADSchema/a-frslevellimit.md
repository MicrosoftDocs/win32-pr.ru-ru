---
title: Атрибут ограничения уровня FRS
description: Ограничьте глубину дерева каталогов для репликации файлов.
ms.assetid: e2916cbd-1ce7-4ff7-82a2-5fbdae3c6a1b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ограничения на уровне FRS
- Схема AD атрибута Фрслевеллимит
topic_type:
- apiref
api_name:
- FRS-Level-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c587565eb10014ef638a2320dd9229d8409ba06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654846"
---
# <a name="frs-level-limit-attribute"></a><span data-ttu-id="8fbee-105">Атрибут ограничения уровня FRS</span><span class="sxs-lookup"><span data-stu-id="8fbee-105">FRS-Level-Limit attribute</span></span>

<span data-ttu-id="8fbee-106">Ограничьте глубину дерева каталогов для репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="8fbee-106">Limit depth of directory tree to replicate for file replication.</span></span>



| <span data-ttu-id="8fbee-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-107">Entry</span></span> | <span data-ttu-id="8fbee-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8fbee-109">CN</span><span class="sxs-lookup"><span data-stu-id="8fbee-109">CN</span></span>                | <span data-ttu-id="8fbee-110">Репликация на уровне FRS</span><span class="sxs-lookup"><span data-stu-id="8fbee-110">FRS-Level-Limit</span></span>                      |
| <span data-ttu-id="8fbee-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8fbee-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8fbee-112">фрслевеллимит</span><span class="sxs-lookup"><span data-stu-id="8fbee-112">fRSLevelLimit</span></span>                        |
| <span data-ttu-id="8fbee-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8fbee-113">Size</span></span>              | <span data-ttu-id="8fbee-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="8fbee-114">4 bytes</span></span>                              |
| <span data-ttu-id="8fbee-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8fbee-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8fbee-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8fbee-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8fbee-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-117">Attribute-Id</span></span>      | <span data-ttu-id="8fbee-118">1.2.840.113556.1.4.534</span><span class="sxs-lookup"><span data-stu-id="8fbee-118">1.2.840.113556.1.4.534</span></span>               |
| <span data-ttu-id="8fbee-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8fbee-119">System-Id-Guid</span></span>    | <span data-ttu-id="8fbee-120">5245801e-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8fbee-120">5245801e-ca6a-11d0-afff-0000f80367c1</span></span> |
| <span data-ttu-id="8fbee-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fbee-121">Syntax</span></span>            | [<span data-ttu-id="8fbee-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="8fbee-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8fbee-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8fbee-123">Implementations</span></span>

-   [<span data-ttu-id="8fbee-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8fbee-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8fbee-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8fbee-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8fbee-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8fbee-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8fbee-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8fbee-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8fbee-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8fbee-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8fbee-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8fbee-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8fbee-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8fbee-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8fbee-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-131">Entry</span></span> | <span data-ttu-id="8fbee-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fbee-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fbee-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fbee-135">System-Only</span></span>            | <span data-ttu-id="8fbee-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-136">False</span></span>                                                     |
| <span data-ttu-id="8fbee-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fbee-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8fbee-138">True</span><span class="sxs-lookup"><span data-stu-id="8fbee-138">True</span></span>                                                      |
| <span data-ttu-id="8fbee-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fbee-139">Is Indexed</span></span>             | <span data-ttu-id="8fbee-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-140">False</span></span>                                                     |
| <span data-ttu-id="8fbee-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fbee-141">In Global Catalog</span></span>      | <span data-ttu-id="8fbee-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-142">False</span></span>                                                     |
| <span data-ttu-id="8fbee-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fbee-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fbee-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fbee-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8fbee-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fbee-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fbee-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-147">Search-Flags</span></span>           | <span data-ttu-id="8fbee-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fbee-148">0x00000000</span></span>                                                |
| <span data-ttu-id="8fbee-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-149">System-Flags</span></span>           | <span data-ttu-id="8fbee-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fbee-150">0x00000010</span></span>                                                |
| <span data-ttu-id="8fbee-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fbee-151">Classes used in</span></span>        | [<span data-ttu-id="8fbee-152">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="8fbee-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8fbee-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8fbee-153">Windows Server 2003</span></span>



| <span data-ttu-id="8fbee-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-154">Entry</span></span> | <span data-ttu-id="8fbee-155">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fbee-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fbee-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fbee-158">System-Only</span></span>            | <span data-ttu-id="8fbee-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-159">False</span></span>                                                     |
| <span data-ttu-id="8fbee-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fbee-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8fbee-161">True</span><span class="sxs-lookup"><span data-stu-id="8fbee-161">True</span></span>                                                      |
| <span data-ttu-id="8fbee-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fbee-162">Is Indexed</span></span>             | <span data-ttu-id="8fbee-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-163">False</span></span>                                                     |
| <span data-ttu-id="8fbee-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fbee-164">In Global Catalog</span></span>      | <span data-ttu-id="8fbee-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-165">False</span></span>                                                     |
| <span data-ttu-id="8fbee-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fbee-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fbee-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fbee-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8fbee-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fbee-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fbee-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-170">Search-Flags</span></span>           | <span data-ttu-id="8fbee-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fbee-171">0x00000000</span></span>                                                |
| <span data-ttu-id="8fbee-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-172">System-Flags</span></span>           | <span data-ttu-id="8fbee-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fbee-173">0x00000010</span></span>                                                |
| <span data-ttu-id="8fbee-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fbee-174">Classes used in</span></span>        | [<span data-ttu-id="8fbee-175">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="8fbee-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8fbee-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8fbee-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8fbee-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-177">Entry</span></span> | <span data-ttu-id="8fbee-178">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fbee-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fbee-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fbee-181">System-Only</span></span>            | <span data-ttu-id="8fbee-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-182">False</span></span>                                                     |
| <span data-ttu-id="8fbee-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fbee-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8fbee-184">True</span><span class="sxs-lookup"><span data-stu-id="8fbee-184">True</span></span>                                                      |
| <span data-ttu-id="8fbee-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fbee-185">Is Indexed</span></span>             | <span data-ttu-id="8fbee-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-186">False</span></span>                                                     |
| <span data-ttu-id="8fbee-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fbee-187">In Global Catalog</span></span>      | <span data-ttu-id="8fbee-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-188">False</span></span>                                                     |
| <span data-ttu-id="8fbee-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fbee-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fbee-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fbee-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8fbee-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fbee-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fbee-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-193">Search-Flags</span></span>           | <span data-ttu-id="8fbee-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fbee-194">0x00000000</span></span>                                                |
| <span data-ttu-id="8fbee-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-195">System-Flags</span></span>           | <span data-ttu-id="8fbee-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fbee-196">0x00000010</span></span>                                                |
| <span data-ttu-id="8fbee-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fbee-197">Classes used in</span></span>        | [<span data-ttu-id="8fbee-198">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="8fbee-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8fbee-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fbee-199">Windows Server 2008</span></span>



| <span data-ttu-id="8fbee-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-200">Entry</span></span> | <span data-ttu-id="8fbee-201">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fbee-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fbee-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fbee-204">System-Only</span></span>            | <span data-ttu-id="8fbee-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-205">False</span></span>                                                     |
| <span data-ttu-id="8fbee-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fbee-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8fbee-207">True</span><span class="sxs-lookup"><span data-stu-id="8fbee-207">True</span></span>                                                      |
| <span data-ttu-id="8fbee-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fbee-208">Is Indexed</span></span>             | <span data-ttu-id="8fbee-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-209">False</span></span>                                                     |
| <span data-ttu-id="8fbee-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fbee-210">In Global Catalog</span></span>      | <span data-ttu-id="8fbee-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-211">False</span></span>                                                     |
| <span data-ttu-id="8fbee-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fbee-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fbee-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fbee-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8fbee-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fbee-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fbee-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-216">Search-Flags</span></span>           | <span data-ttu-id="8fbee-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fbee-217">0x00000000</span></span>                                                |
| <span data-ttu-id="8fbee-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-218">System-Flags</span></span>           | <span data-ttu-id="8fbee-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fbee-219">0x00000010</span></span>                                                |
| <span data-ttu-id="8fbee-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fbee-220">Classes used in</span></span>        | [<span data-ttu-id="8fbee-221">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="8fbee-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8fbee-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fbee-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8fbee-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-223">Entry</span></span> | <span data-ttu-id="8fbee-224">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fbee-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fbee-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fbee-227">System-Only</span></span>            | <span data-ttu-id="8fbee-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-228">False</span></span>                                                     |
| <span data-ttu-id="8fbee-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fbee-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8fbee-230">True</span><span class="sxs-lookup"><span data-stu-id="8fbee-230">True</span></span>                                                      |
| <span data-ttu-id="8fbee-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fbee-231">Is Indexed</span></span>             | <span data-ttu-id="8fbee-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-232">False</span></span>                                                     |
| <span data-ttu-id="8fbee-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fbee-233">In Global Catalog</span></span>      | <span data-ttu-id="8fbee-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-234">False</span></span>                                                     |
| <span data-ttu-id="8fbee-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fbee-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fbee-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fbee-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8fbee-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fbee-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fbee-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-239">Search-Flags</span></span>           | <span data-ttu-id="8fbee-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fbee-240">0x00000000</span></span>                                                |
| <span data-ttu-id="8fbee-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-241">System-Flags</span></span>           | <span data-ttu-id="8fbee-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fbee-242">0x00000010</span></span>                                                |
| <span data-ttu-id="8fbee-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fbee-243">Classes used in</span></span>        | [<span data-ttu-id="8fbee-244">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="8fbee-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8fbee-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fbee-245">Windows Server 2012</span></span>



| <span data-ttu-id="8fbee-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fbee-246">Entry</span></span> | <span data-ttu-id="8fbee-247">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbee-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fbee-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fbee-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fbee-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8fbee-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fbee-250">System-Only</span></span>            | <span data-ttu-id="8fbee-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-251">False</span></span>                                                     |
| <span data-ttu-id="8fbee-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fbee-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8fbee-253">True</span><span class="sxs-lookup"><span data-stu-id="8fbee-253">True</span></span>                                                      |
| <span data-ttu-id="8fbee-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fbee-254">Is Indexed</span></span>             | <span data-ttu-id="8fbee-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-255">False</span></span>                                                     |
| <span data-ttu-id="8fbee-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fbee-256">In Global Catalog</span></span>      | <span data-ttu-id="8fbee-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fbee-257">False</span></span>                                                     |
| <span data-ttu-id="8fbee-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fbee-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fbee-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fbee-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8fbee-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fbee-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fbee-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8fbee-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-262">Search-Flags</span></span>           | <span data-ttu-id="8fbee-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fbee-263">0x00000000</span></span>                                                |
| <span data-ttu-id="8fbee-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fbee-264">System-Flags</span></span>           | <span data-ttu-id="8fbee-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fbee-265">0x00000010</span></span>                                                |
| <span data-ttu-id="8fbee-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fbee-266">Classes used in</span></span>        | [<span data-ttu-id="8fbee-267">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="8fbee-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





