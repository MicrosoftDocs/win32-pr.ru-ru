---
title: Атрибут MS-DS-replicate-NC-Reason
description: Атрибут объекта Нтдсконнектион, указывающий, как (или в этом случае) показывается, что соединение будет использоваться в топологии репликации. Параметр имеет несколько значений и имеет синтаксис Дистнаме + binary, где двоичная часть является битовым значением целого размера.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-replicate-NC-Reason
- Схема AD атрибута mS-DS-Репликатеснкреасон
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416213"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="d567c-106">Атрибут MS-DS-replicate-NC-Reason</span><span class="sxs-lookup"><span data-stu-id="d567c-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="d567c-107">Атрибут объекта Нтдсконнектион, указывающий, как (или в этом случае) показывается, что соединение будет использоваться в топологии репликации.</span><span class="sxs-lookup"><span data-stu-id="d567c-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="d567c-108">Параметр имеет несколько значений и имеет синтаксис Дистнаме + binary, где двоичная часть является битовым значением целого размера.</span><span class="sxs-lookup"><span data-stu-id="d567c-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="d567c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-109">Entry</span></span> | <span data-ttu-id="d567c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d567c-111">CN</span><span class="sxs-lookup"><span data-stu-id="d567c-111">CN</span></span>                | <span data-ttu-id="d567c-112">MS-DS-replicate-NC-причина</span><span class="sxs-lookup"><span data-stu-id="d567c-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="d567c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d567c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d567c-114">mS-DS-Репликатеснкреасон</span><span class="sxs-lookup"><span data-stu-id="d567c-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="d567c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="d567c-115">Size</span></span>              | <span data-ttu-id="d567c-116">Значение для двоичной части: 0 = нет \_ причины, 1 = \_ топология сборки мусора, 2 = Кольцевая \_ топология, 4 = сокращение \_ \_ ТОПОЛОГИИ прыжков, 8 = устаревшая \_ \_ топология серверов.</span><span class="sxs-lookup"><span data-stu-id="d567c-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="d567c-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d567c-117">Update Privilege</span></span>  | <span data-ttu-id="d567c-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="d567c-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="d567c-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d567c-119">Update Frequency</span></span>  | <span data-ttu-id="d567c-120">Может измениться в ответ на изменения в топологии сети.</span><span class="sxs-lookup"><span data-stu-id="d567c-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="d567c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-121">Attribute-Id</span></span>      | <span data-ttu-id="d567c-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="d567c-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="d567c-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d567c-123">System-Id-Guid</span></span>    | <span data-ttu-id="d567c-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d567c-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="d567c-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d567c-125">Syntax</span></span>            | [<span data-ttu-id="d567c-126">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="d567c-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="d567c-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d567c-127">Implementations</span></span>

-   [<span data-ttu-id="d567c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d567c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d567c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d567c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d567c-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d567c-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d567c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d567c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d567c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d567c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d567c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d567c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d567c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d567c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d567c-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d567c-135">Windows 2000 Server</span></span>



| <span data-ttu-id="d567c-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-136">Entry</span></span> | <span data-ttu-id="d567c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-140">System-Only</span></span>            | <span data-ttu-id="d567c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-141">False</span></span>                                                  |
| <span data-ttu-id="d567c-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-143">False</span></span>                                                  |
| <span data-ttu-id="d567c-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-144">Is Indexed</span></span>             | <span data-ttu-id="d567c-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-145">False</span></span>                                                  |
| <span data-ttu-id="d567c-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-146">In Global Catalog</span></span>      | <span data-ttu-id="d567c-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-147">False</span></span>                                                  |
| <span data-ttu-id="d567c-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-152">Search-Flags</span></span>           | <span data-ttu-id="d567c-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-153">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-154">System-Flags</span></span>           | <span data-ttu-id="d567c-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-155">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-156">Classes used in</span></span>        | [<span data-ttu-id="d567c-157">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d567c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d567c-158">Windows Server 2003</span></span>



| <span data-ttu-id="d567c-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-159">Entry</span></span> | <span data-ttu-id="d567c-160">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-163">System-Only</span></span>            | <span data-ttu-id="d567c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-164">False</span></span>                                                  |
| <span data-ttu-id="d567c-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-166">False</span></span>                                                  |
| <span data-ttu-id="d567c-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-167">Is Indexed</span></span>             | <span data-ttu-id="d567c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-168">False</span></span>                                                  |
| <span data-ttu-id="d567c-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-169">In Global Catalog</span></span>      | <span data-ttu-id="d567c-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-170">False</span></span>                                                  |
| <span data-ttu-id="d567c-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-175">Search-Flags</span></span>           | <span data-ttu-id="d567c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-176">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-177">System-Flags</span></span>           | <span data-ttu-id="d567c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-178">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-179">Classes used in</span></span>        | [<span data-ttu-id="d567c-180">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d567c-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="d567c-181">ADAM</span></span>



| <span data-ttu-id="d567c-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-182">Entry</span></span> | <span data-ttu-id="d567c-183">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-186">System-Only</span></span>            | <span data-ttu-id="d567c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-187">False</span></span>                                                  |
| <span data-ttu-id="d567c-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-189">False</span></span>                                                  |
| <span data-ttu-id="d567c-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-190">Is Indexed</span></span>             | <span data-ttu-id="d567c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-191">False</span></span>                                                  |
| <span data-ttu-id="d567c-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-192">In Global Catalog</span></span>      | <span data-ttu-id="d567c-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-193">False</span></span>                                                  |
| <span data-ttu-id="d567c-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-198">Search-Flags</span></span>           | <span data-ttu-id="d567c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-199">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-200">System-Flags</span></span>           | <span data-ttu-id="d567c-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-201">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-202">Classes used in</span></span>        | [<span data-ttu-id="d567c-203">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d567c-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d567c-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d567c-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-205">Entry</span></span> | <span data-ttu-id="d567c-206">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-209">System-Only</span></span>            | <span data-ttu-id="d567c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-210">False</span></span>                                                  |
| <span data-ttu-id="d567c-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-212">False</span></span>                                                  |
| <span data-ttu-id="d567c-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-213">Is Indexed</span></span>             | <span data-ttu-id="d567c-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-214">False</span></span>                                                  |
| <span data-ttu-id="d567c-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-215">In Global Catalog</span></span>      | <span data-ttu-id="d567c-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-216">False</span></span>                                                  |
| <span data-ttu-id="d567c-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-221">Search-Flags</span></span>           | <span data-ttu-id="d567c-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-222">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-223">System-Flags</span></span>           | <span data-ttu-id="d567c-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-224">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-225">Classes used in</span></span>        | [<span data-ttu-id="d567c-226">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d567c-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d567c-227">Windows Server 2008</span></span>



| <span data-ttu-id="d567c-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-228">Entry</span></span> | <span data-ttu-id="d567c-229">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-232">System-Only</span></span>            | <span data-ttu-id="d567c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-233">False</span></span>                                                  |
| <span data-ttu-id="d567c-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-235">False</span></span>                                                  |
| <span data-ttu-id="d567c-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-236">Is Indexed</span></span>             | <span data-ttu-id="d567c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-237">False</span></span>                                                  |
| <span data-ttu-id="d567c-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-238">In Global Catalog</span></span>      | <span data-ttu-id="d567c-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-239">False</span></span>                                                  |
| <span data-ttu-id="d567c-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-244">Search-Flags</span></span>           | <span data-ttu-id="d567c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-245">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-246">System-Flags</span></span>           | <span data-ttu-id="d567c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-247">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-248">Classes used in</span></span>        | [<span data-ttu-id="d567c-249">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d567c-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d567c-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d567c-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-251">Entry</span></span> | <span data-ttu-id="d567c-252">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-255">System-Only</span></span>            | <span data-ttu-id="d567c-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-256">False</span></span>                                                  |
| <span data-ttu-id="d567c-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-257">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-258">False</span></span>                                                  |
| <span data-ttu-id="d567c-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-259">Is Indexed</span></span>             | <span data-ttu-id="d567c-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-260">False</span></span>                                                  |
| <span data-ttu-id="d567c-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-261">In Global Catalog</span></span>      | <span data-ttu-id="d567c-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-262">False</span></span>                                                  |
| <span data-ttu-id="d567c-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-267">Search-Flags</span></span>           | <span data-ttu-id="d567c-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-268">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-269">System-Flags</span></span>           | <span data-ttu-id="d567c-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-270">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-271">Classes used in</span></span>        | [<span data-ttu-id="d567c-272">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d567c-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d567c-273">Windows Server 2012</span></span>



| <span data-ttu-id="d567c-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="d567c-274">Entry</span></span> | <span data-ttu-id="d567c-275">Значение</span><span class="sxs-lookup"><span data-stu-id="d567c-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d567c-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d567c-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d567c-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d567c-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="d567c-278">System-Only</span></span>            | <span data-ttu-id="d567c-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-279">False</span></span>                                                  |
| <span data-ttu-id="d567c-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d567c-280">Is-Single-Valued</span></span>       | <span data-ttu-id="d567c-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-281">False</span></span>                                                  |
| <span data-ttu-id="d567c-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d567c-282">Is Indexed</span></span>             | <span data-ttu-id="d567c-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-283">False</span></span>                                                  |
| <span data-ttu-id="d567c-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d567c-284">In Global Catalog</span></span>      | <span data-ttu-id="d567c-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="d567c-285">False</span></span>                                                  |
| <span data-ttu-id="d567c-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d567c-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="d567c-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d567c-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d567c-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d567c-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d567c-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d567c-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-290">Search-Flags</span></span>           | <span data-ttu-id="d567c-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d567c-291">0x00000000</span></span>                                             |
| <span data-ttu-id="d567c-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d567c-292">System-Flags</span></span>           | <span data-ttu-id="d567c-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d567c-293">0x00000010</span></span>                                             |
| <span data-ttu-id="d567c-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d567c-294">Classes used in</span></span>        | [<span data-ttu-id="d567c-295">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="d567c-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





