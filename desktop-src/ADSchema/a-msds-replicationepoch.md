---
title: Атрибут ms-DS-Репликатионепоч
description: Он используется для хранения эпохи, при которой реплицируются все контроллеры домена. Эпоха — это период времени, в течение которого домен имеет определенное имя. Новый эпоха начинается, когда происходит изменение доменного имени.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-Репликатионепоч
- Схема AD атрибута msDS-Репликатионепоч
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536005"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="1c965-107">Атрибут ms-DS-Репликатионепоч</span><span class="sxs-lookup"><span data-stu-id="1c965-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="1c965-108">Он используется для хранения эпохи, при которой реплицируются все контроллеры домена.</span><span class="sxs-lookup"><span data-stu-id="1c965-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="1c965-109">Эпоха — это период времени, в течение которого домен имеет определенное имя.</span><span class="sxs-lookup"><span data-stu-id="1c965-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="1c965-110">Новый эпоха начинается, когда происходит изменение доменного имени.</span><span class="sxs-lookup"><span data-stu-id="1c965-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="1c965-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-111">Entry</span></span> | <span data-ttu-id="1c965-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1c965-113">CN</span><span class="sxs-lookup"><span data-stu-id="1c965-113">CN</span></span>                | <span data-ttu-id="1c965-114">MS-DS-Репликатионепоч</span><span class="sxs-lookup"><span data-stu-id="1c965-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="1c965-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1c965-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1c965-116">msDS-Репликатионепоч</span><span class="sxs-lookup"><span data-stu-id="1c965-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="1c965-117">Размер</span><span class="sxs-lookup"><span data-stu-id="1c965-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="1c965-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1c965-118">Update Privilege</span></span>  | <span data-ttu-id="1c965-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="1c965-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="1c965-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1c965-120">Update Frequency</span></span>  | <span data-ttu-id="1c965-121">Только во время реструктуризации домена.</span><span class="sxs-lookup"><span data-stu-id="1c965-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="1c965-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-122">Attribute-Id</span></span>      | <span data-ttu-id="1c965-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="1c965-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="1c965-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1c965-124">System-Id-Guid</span></span>    | <span data-ttu-id="1c965-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span><span class="sxs-lookup"><span data-stu-id="1c965-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="1c965-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c965-126">Syntax</span></span>            | [<span data-ttu-id="1c965-127">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="1c965-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1c965-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1c965-128">Implementations</span></span>

-   [<span data-ttu-id="1c965-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1c965-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1c965-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1c965-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1c965-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1c965-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1c965-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1c965-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1c965-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1c965-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1c965-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1c965-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1c965-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1c965-135">Windows Server 2003</span></span>



| <span data-ttu-id="1c965-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-136">Entry</span></span> | <span data-ttu-id="1c965-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1c965-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c965-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c965-140">System-Only</span></span>            | <span data-ttu-id="1c965-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-141">False</span></span>                                    |
| <span data-ttu-id="1c965-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c965-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1c965-143">True</span><span class="sxs-lookup"><span data-stu-id="1c965-143">True</span></span>                                     |
| <span data-ttu-id="1c965-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c965-144">Is Indexed</span></span>             | <span data-ttu-id="1c965-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-145">False</span></span>                                    |
| <span data-ttu-id="1c965-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c965-146">In Global Catalog</span></span>      | <span data-ttu-id="1c965-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-147">False</span></span>                                    |
| <span data-ttu-id="1c965-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c965-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c965-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c965-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1c965-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c965-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1c965-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c965-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1c965-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-152">Search-Flags</span></span>           | <span data-ttu-id="1c965-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c965-153">0x00000000</span></span>                               |
| <span data-ttu-id="1c965-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-154">System-Flags</span></span>           | <span data-ttu-id="1c965-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1c965-155">0x00000011</span></span>                               |
| <span data-ttu-id="1c965-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c965-156">Classes used in</span></span>        | [<span data-ttu-id="1c965-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1c965-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1c965-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="1c965-158">ADAM</span></span>



| <span data-ttu-id="1c965-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-159">Entry</span></span> | <span data-ttu-id="1c965-160">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1c965-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c965-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c965-163">System-Only</span></span>            | <span data-ttu-id="1c965-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-164">False</span></span>                                    |
| <span data-ttu-id="1c965-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c965-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1c965-166">True</span><span class="sxs-lookup"><span data-stu-id="1c965-166">True</span></span>                                     |
| <span data-ttu-id="1c965-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c965-167">Is Indexed</span></span>             | <span data-ttu-id="1c965-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-168">False</span></span>                                    |
| <span data-ttu-id="1c965-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c965-169">In Global Catalog</span></span>      | <span data-ttu-id="1c965-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-170">False</span></span>                                    |
| <span data-ttu-id="1c965-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c965-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c965-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c965-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1c965-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c965-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1c965-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c965-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1c965-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-175">Search-Flags</span></span>           | <span data-ttu-id="1c965-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c965-176">0x00000000</span></span>                               |
| <span data-ttu-id="1c965-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-177">System-Flags</span></span>           | <span data-ttu-id="1c965-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1c965-178">0x00000011</span></span>                               |
| <span data-ttu-id="1c965-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c965-179">Classes used in</span></span>        | [<span data-ttu-id="1c965-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1c965-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1c965-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1c965-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1c965-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-182">Entry</span></span> | <span data-ttu-id="1c965-183">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1c965-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c965-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c965-186">System-Only</span></span>            | <span data-ttu-id="1c965-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-187">False</span></span>                                    |
| <span data-ttu-id="1c965-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c965-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1c965-189">True</span><span class="sxs-lookup"><span data-stu-id="1c965-189">True</span></span>                                     |
| <span data-ttu-id="1c965-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c965-190">Is Indexed</span></span>             | <span data-ttu-id="1c965-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-191">False</span></span>                                    |
| <span data-ttu-id="1c965-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c965-192">In Global Catalog</span></span>      | <span data-ttu-id="1c965-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-193">False</span></span>                                    |
| <span data-ttu-id="1c965-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c965-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c965-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c965-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1c965-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c965-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1c965-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c965-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1c965-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-198">Search-Flags</span></span>           | <span data-ttu-id="1c965-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c965-199">0x00000000</span></span>                               |
| <span data-ttu-id="1c965-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-200">System-Flags</span></span>           | <span data-ttu-id="1c965-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1c965-201">0x00000011</span></span>                               |
| <span data-ttu-id="1c965-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c965-202">Classes used in</span></span>        | [<span data-ttu-id="1c965-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1c965-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1c965-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c965-204">Windows Server 2008</span></span>



| <span data-ttu-id="1c965-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-205">Entry</span></span> | <span data-ttu-id="1c965-206">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1c965-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c965-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c965-209">System-Only</span></span>            | <span data-ttu-id="1c965-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-210">False</span></span>                                    |
| <span data-ttu-id="1c965-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c965-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1c965-212">True</span><span class="sxs-lookup"><span data-stu-id="1c965-212">True</span></span>                                     |
| <span data-ttu-id="1c965-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c965-213">Is Indexed</span></span>             | <span data-ttu-id="1c965-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-214">False</span></span>                                    |
| <span data-ttu-id="1c965-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c965-215">In Global Catalog</span></span>      | <span data-ttu-id="1c965-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-216">False</span></span>                                    |
| <span data-ttu-id="1c965-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c965-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c965-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c965-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1c965-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c965-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1c965-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c965-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1c965-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-221">Search-Flags</span></span>           | <span data-ttu-id="1c965-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c965-222">0x00000000</span></span>                               |
| <span data-ttu-id="1c965-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-223">System-Flags</span></span>           | <span data-ttu-id="1c965-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1c965-224">0x00000011</span></span>                               |
| <span data-ttu-id="1c965-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c965-225">Classes used in</span></span>        | [<span data-ttu-id="1c965-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1c965-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1c965-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c965-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1c965-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-228">Entry</span></span> | <span data-ttu-id="1c965-229">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1c965-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c965-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c965-232">System-Only</span></span>            | <span data-ttu-id="1c965-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-233">False</span></span>                                    |
| <span data-ttu-id="1c965-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c965-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1c965-235">True</span><span class="sxs-lookup"><span data-stu-id="1c965-235">True</span></span>                                     |
| <span data-ttu-id="1c965-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c965-236">Is Indexed</span></span>             | <span data-ttu-id="1c965-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-237">False</span></span>                                    |
| <span data-ttu-id="1c965-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c965-238">In Global Catalog</span></span>      | <span data-ttu-id="1c965-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-239">False</span></span>                                    |
| <span data-ttu-id="1c965-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c965-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c965-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c965-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1c965-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c965-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1c965-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c965-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1c965-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-244">Search-Flags</span></span>           | <span data-ttu-id="1c965-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c965-245">0x00000000</span></span>                               |
| <span data-ttu-id="1c965-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-246">System-Flags</span></span>           | <span data-ttu-id="1c965-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1c965-247">0x00000011</span></span>                               |
| <span data-ttu-id="1c965-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c965-248">Classes used in</span></span>        | [<span data-ttu-id="1c965-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1c965-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1c965-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c965-250">Windows Server 2012</span></span>



| <span data-ttu-id="1c965-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c965-251">Entry</span></span> | <span data-ttu-id="1c965-252">Значение</span><span class="sxs-lookup"><span data-stu-id="1c965-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1c965-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c965-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c965-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="1c965-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c965-255">System-Only</span></span>            | <span data-ttu-id="1c965-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-256">False</span></span>                                    |
| <span data-ttu-id="1c965-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c965-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1c965-258">True</span><span class="sxs-lookup"><span data-stu-id="1c965-258">True</span></span>                                     |
| <span data-ttu-id="1c965-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c965-259">Is Indexed</span></span>             | <span data-ttu-id="1c965-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-260">False</span></span>                                    |
| <span data-ttu-id="1c965-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c965-261">In Global Catalog</span></span>      | <span data-ttu-id="1c965-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c965-262">False</span></span>                                    |
| <span data-ttu-id="1c965-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c965-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c965-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c965-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1c965-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c965-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1c965-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c965-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1c965-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-267">Search-Flags</span></span>           | <span data-ttu-id="1c965-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c965-268">0x00000000</span></span>                               |
| <span data-ttu-id="1c965-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c965-269">System-Flags</span></span>           | <span data-ttu-id="1c965-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1c965-270">0x00000011</span></span>                               |
| <span data-ttu-id="1c965-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c965-271">Classes used in</span></span>        | [<span data-ttu-id="1c965-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1c965-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





