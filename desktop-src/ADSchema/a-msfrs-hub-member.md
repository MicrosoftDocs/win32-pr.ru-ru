---
title: MS-FRS-Hub-атрибут члена
description: Для записи предпочтительных параметров топологии NTFRS используется атрибут MS-FRS-Hub-Member.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута членства MS-FRS-HUB
- Мсфрс-Hub-схема AD атрибута Member
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655160"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="9aa2e-105">MS-FRS-Hub-атрибут члена</span><span class="sxs-lookup"><span data-stu-id="9aa2e-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="9aa2e-106">Для записи предпочтительных параметров топологии NTFRS используется атрибут **MS-FRS-Hub-Member** .</span><span class="sxs-lookup"><span data-stu-id="9aa2e-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="9aa2e-107">Когда член FRS добавляется в набор реплик или удаляется из него, эти атрибуты называются, и в подключения между остальными членами FRS в наборе реплик устанавливаются соответствующие изменения.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="9aa2e-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="9aa2e-108">Entry</span></span> | <span data-ttu-id="9aa2e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa2e-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9aa2e-110">CN</span><span class="sxs-lookup"><span data-stu-id="9aa2e-110">CN</span></span>                | <span data-ttu-id="9aa2e-111">MS-FRS-Hub-член</span><span class="sxs-lookup"><span data-stu-id="9aa2e-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="9aa2e-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9aa2e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="9aa2e-113">Мсфрс-Hub-член</span><span class="sxs-lookup"><span data-stu-id="9aa2e-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="9aa2e-114">Размер</span><span class="sxs-lookup"><span data-stu-id="9aa2e-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="9aa2e-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9aa2e-115">Update Privilege</span></span>  | <span data-ttu-id="9aa2e-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="9aa2e-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="9aa2e-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9aa2e-117">Update Frequency</span></span>  | <span data-ttu-id="9aa2e-118">При создании набора реплик или изменении предпочтительной топологии.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="9aa2e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9aa2e-119">Attribute-Id</span></span>      | <span data-ttu-id="9aa2e-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="9aa2e-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="9aa2e-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9aa2e-121">System-Id-Guid</span></span>    | <span data-ttu-id="9aa2e-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="9aa2e-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="9aa2e-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aa2e-123">Syntax</span></span>            | [<span data-ttu-id="9aa2e-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="9aa2e-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9aa2e-125">Implementations</span></span>

-   [<span data-ttu-id="9aa2e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9aa2e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9aa2e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9aa2e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9aa2e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9aa2e-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9aa2e-131">Windows Server 2003</span></span>



| <span data-ttu-id="9aa2e-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="9aa2e-132">Entry</span></span> | <span data-ttu-id="9aa2e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa2e-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9aa2e-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9aa2e-134">Link-Id</span></span>                | <span data-ttu-id="9aa2e-135">1046</span><span class="sxs-lookup"><span data-stu-id="9aa2e-135">1046</span></span>                                                      |
| <span data-ttu-id="9aa2e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa2e-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9aa2e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa2e-137">System-Only</span></span>            | <span data-ttu-id="9aa2e-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-138">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9aa2e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa2e-140">True</span><span class="sxs-lookup"><span data-stu-id="9aa2e-140">True</span></span>                                                      |
| <span data-ttu-id="9aa2e-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9aa2e-141">Is Indexed</span></span>             | <span data-ttu-id="9aa2e-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-142">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9aa2e-143">In Global Catalog</span></span>      | <span data-ttu-id="9aa2e-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-144">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9aa2e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa2e-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa2e-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9aa2e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa2e-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa2e-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-149">Search-Flags</span></span>           | <span data-ttu-id="9aa2e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-150">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-151">System-Flags</span></span>           | <span data-ttu-id="9aa2e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-152">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9aa2e-153">Classes used in</span></span>        | [<span data-ttu-id="9aa2e-154">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9aa2e-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9aa2e-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9aa2e-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="9aa2e-156">Entry</span></span> | <span data-ttu-id="9aa2e-157">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa2e-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9aa2e-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9aa2e-158">Link-Id</span></span>                | <span data-ttu-id="9aa2e-159">1046</span><span class="sxs-lookup"><span data-stu-id="9aa2e-159">1046</span></span>                                                      |
| <span data-ttu-id="9aa2e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa2e-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9aa2e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa2e-161">System-Only</span></span>            | <span data-ttu-id="9aa2e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-162">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9aa2e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa2e-164">True</span><span class="sxs-lookup"><span data-stu-id="9aa2e-164">True</span></span>                                                      |
| <span data-ttu-id="9aa2e-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9aa2e-165">Is Indexed</span></span>             | <span data-ttu-id="9aa2e-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-166">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9aa2e-167">In Global Catalog</span></span>      | <span data-ttu-id="9aa2e-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-168">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9aa2e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa2e-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa2e-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9aa2e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa2e-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa2e-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-173">Search-Flags</span></span>           | <span data-ttu-id="9aa2e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-174">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-175">System-Flags</span></span>           | <span data-ttu-id="9aa2e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-176">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9aa2e-177">Classes used in</span></span>        | [<span data-ttu-id="9aa2e-178">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9aa2e-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aa2e-179">Windows Server 2008</span></span>



| <span data-ttu-id="9aa2e-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="9aa2e-180">Entry</span></span> | <span data-ttu-id="9aa2e-181">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa2e-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9aa2e-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9aa2e-182">Link-Id</span></span>                | <span data-ttu-id="9aa2e-183">1046</span><span class="sxs-lookup"><span data-stu-id="9aa2e-183">1046</span></span>                                                      |
| <span data-ttu-id="9aa2e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa2e-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9aa2e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa2e-185">System-Only</span></span>            | <span data-ttu-id="9aa2e-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-186">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9aa2e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa2e-188">True</span><span class="sxs-lookup"><span data-stu-id="9aa2e-188">True</span></span>                                                      |
| <span data-ttu-id="9aa2e-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9aa2e-189">Is Indexed</span></span>             | <span data-ttu-id="9aa2e-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-190">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9aa2e-191">In Global Catalog</span></span>      | <span data-ttu-id="9aa2e-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-192">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9aa2e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa2e-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa2e-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9aa2e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa2e-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa2e-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-197">Search-Flags</span></span>           | <span data-ttu-id="9aa2e-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-198">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-199">System-Flags</span></span>           | <span data-ttu-id="9aa2e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-200">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9aa2e-201">Classes used in</span></span>        | [<span data-ttu-id="9aa2e-202">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9aa2e-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9aa2e-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9aa2e-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="9aa2e-204">Entry</span></span> | <span data-ttu-id="9aa2e-205">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa2e-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9aa2e-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9aa2e-206">Link-Id</span></span>                | <span data-ttu-id="9aa2e-207">1046</span><span class="sxs-lookup"><span data-stu-id="9aa2e-207">1046</span></span>                                                      |
| <span data-ttu-id="9aa2e-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa2e-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9aa2e-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa2e-209">System-Only</span></span>            | <span data-ttu-id="9aa2e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-210">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9aa2e-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa2e-212">True</span><span class="sxs-lookup"><span data-stu-id="9aa2e-212">True</span></span>                                                      |
| <span data-ttu-id="9aa2e-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9aa2e-213">Is Indexed</span></span>             | <span data-ttu-id="9aa2e-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-214">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9aa2e-215">In Global Catalog</span></span>      | <span data-ttu-id="9aa2e-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-216">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9aa2e-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa2e-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa2e-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9aa2e-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa2e-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa2e-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-221">Search-Flags</span></span>           | <span data-ttu-id="9aa2e-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-222">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-223">System-Flags</span></span>           | <span data-ttu-id="9aa2e-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-224">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9aa2e-225">Classes used in</span></span>        | [<span data-ttu-id="9aa2e-226">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9aa2e-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9aa2e-227">Windows Server 2012</span></span>



| <span data-ttu-id="9aa2e-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="9aa2e-228">Entry</span></span> | <span data-ttu-id="9aa2e-229">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa2e-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9aa2e-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9aa2e-230">Link-Id</span></span>                | <span data-ttu-id="9aa2e-231">1046</span><span class="sxs-lookup"><span data-stu-id="9aa2e-231">1046</span></span>                                                      |
| <span data-ttu-id="9aa2e-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa2e-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9aa2e-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa2e-233">System-Only</span></span>            | <span data-ttu-id="9aa2e-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-234">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9aa2e-235">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa2e-236">True</span><span class="sxs-lookup"><span data-stu-id="9aa2e-236">True</span></span>                                                      |
| <span data-ttu-id="9aa2e-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9aa2e-237">Is Indexed</span></span>             | <span data-ttu-id="9aa2e-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-238">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9aa2e-239">In Global Catalog</span></span>      | <span data-ttu-id="9aa2e-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="9aa2e-240">False</span></span>                                                     |
| <span data-ttu-id="9aa2e-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9aa2e-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa2e-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa2e-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9aa2e-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa2e-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa2e-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9aa2e-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-245">Search-Flags</span></span>           | <span data-ttu-id="9aa2e-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-246">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa2e-247">System-Flags</span></span>           | <span data-ttu-id="9aa2e-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9aa2e-248">0x00000000</span></span>                                                |
| <span data-ttu-id="9aa2e-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9aa2e-249">Classes used in</span></span>        | [<span data-ttu-id="9aa2e-250">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9aa2e-251">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9aa2e-251">Remarks</span></span>

<span data-ttu-id="9aa2e-252">Это полное различающееся имя объекта [**члена NTFRS**](c-ntfrsmember.md) .</span><span class="sxs-lookup"><span data-stu-id="9aa2e-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="9aa2e-253">Различающееся имя имеет формат "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = тома DFS, CN = служба репликации файлов, CN = System, DC =..."</span><span class="sxs-lookup"><span data-stu-id="9aa2e-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 





