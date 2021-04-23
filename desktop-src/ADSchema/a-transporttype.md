---
title: Атрибут Transport-Type
description: Различающееся имя для типа транспорта, используемого для объединения сайтов. Это значение может указывать на транспорт IP или SMTP.
ms.assetid: aed18e69-3118-4cb8-b959-829106602f95
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Transport-Type
- Схема AD атрибута transportType
topic_type:
- apiref
api_name:
- Transport-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28c68347deb83d52b78564688a563431609fb81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893253"
---
# <a name="transport-type-attribute"></a><span data-ttu-id="c9734-106">Атрибут Transport-Type</span><span class="sxs-lookup"><span data-stu-id="c9734-106">Transport-Type attribute</span></span>

<span data-ttu-id="c9734-107">Различающееся имя для типа транспорта, используемого для объединения сайтов.</span><span class="sxs-lookup"><span data-stu-id="c9734-107">The distinguished name for a type of transport being used to connect sites together.</span></span> <span data-ttu-id="c9734-108">Это значение может указывать на транспорт IP или SMTP.</span><span class="sxs-lookup"><span data-stu-id="c9734-108">This value can point to an IP or SMTP transport.</span></span>



| <span data-ttu-id="c9734-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-109">Entry</span></span> | <span data-ttu-id="c9734-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c9734-111">CN</span><span class="sxs-lookup"><span data-stu-id="c9734-111">CN</span></span>                | <span data-ttu-id="c9734-112">Transport-Type</span><span class="sxs-lookup"><span data-stu-id="c9734-112">Transport-Type</span></span>                          |
| <span data-ttu-id="c9734-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c9734-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c9734-114">transportType</span><span class="sxs-lookup"><span data-stu-id="c9734-114">transportType</span></span>                           |
| <span data-ttu-id="c9734-115">Размер</span><span class="sxs-lookup"><span data-stu-id="c9734-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="c9734-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c9734-116">Update Privilege</span></span>  | <span data-ttu-id="c9734-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c9734-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="c9734-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c9734-118">Update Frequency</span></span>  | <span data-ttu-id="c9734-119">При подключении сайтов.</span><span class="sxs-lookup"><span data-stu-id="c9734-119">When connecting sites.</span></span>                  |
| <span data-ttu-id="c9734-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-120">Attribute-Id</span></span>      | <span data-ttu-id="c9734-121">1.2.840.113556.1.4.791</span><span class="sxs-lookup"><span data-stu-id="c9734-121">1.2.840.113556.1.4.791</span></span>                  |
| <span data-ttu-id="c9734-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c9734-122">System-Id-Guid</span></span>    | <span data-ttu-id="c9734-123">26d97374-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c9734-123">26d97374-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="c9734-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9734-124">Syntax</span></span>            | [<span data-ttu-id="c9734-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c9734-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c9734-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c9734-126">Implementations</span></span>

-   [<span data-ttu-id="c9734-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9734-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9734-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9734-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9734-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c9734-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c9734-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9734-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9734-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9734-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9734-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9734-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9734-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9734-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9734-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9734-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c9734-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-135">Entry</span></span> | <span data-ttu-id="c9734-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-136">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-137">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-138">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-139">System-Only</span></span>            | <span data-ttu-id="c9734-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-140">False</span></span>                                                  |
| <span data-ttu-id="c9734-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-142">True</span><span class="sxs-lookup"><span data-stu-id="c9734-142">True</span></span>                                                   |
| <span data-ttu-id="c9734-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-143">Is Indexed</span></span>             | <span data-ttu-id="c9734-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-144">False</span></span>                                                  |
| <span data-ttu-id="c9734-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-145">In Global Catalog</span></span>      | <span data-ttu-id="c9734-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-146">False</span></span>                                                  |
| <span data-ttu-id="c9734-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-148">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-149">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-150">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-151">Search-Flags</span></span>           | <span data-ttu-id="c9734-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-152">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-153">System-Flags</span></span>           | <span data-ttu-id="c9734-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-154">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-155">Classes used in</span></span>        | [<span data-ttu-id="c9734-156">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-156">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9734-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9734-157">Windows Server 2003</span></span>



| <span data-ttu-id="c9734-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-158">Entry</span></span> | <span data-ttu-id="c9734-159">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-159">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-160">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-161">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-162">System-Only</span></span>            | <span data-ttu-id="c9734-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-163">False</span></span>                                                  |
| <span data-ttu-id="c9734-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-165">True</span><span class="sxs-lookup"><span data-stu-id="c9734-165">True</span></span>                                                   |
| <span data-ttu-id="c9734-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-166">Is Indexed</span></span>             | <span data-ttu-id="c9734-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-167">False</span></span>                                                  |
| <span data-ttu-id="c9734-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-168">In Global Catalog</span></span>      | <span data-ttu-id="c9734-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-169">False</span></span>                                                  |
| <span data-ttu-id="c9734-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-171">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-172">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-173">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-174">Search-Flags</span></span>           | <span data-ttu-id="c9734-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-175">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-176">System-Flags</span></span>           | <span data-ttu-id="c9734-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-177">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-178">Classes used in</span></span>        | [<span data-ttu-id="c9734-179">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-179">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c9734-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="c9734-180">ADAM</span></span>



| <span data-ttu-id="c9734-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-181">Entry</span></span> | <span data-ttu-id="c9734-182">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-182">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-183">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-184">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-185">System-Only</span></span>            | <span data-ttu-id="c9734-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-186">False</span></span>                                                  |
| <span data-ttu-id="c9734-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-188">True</span><span class="sxs-lookup"><span data-stu-id="c9734-188">True</span></span>                                                   |
| <span data-ttu-id="c9734-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-189">Is Indexed</span></span>             | <span data-ttu-id="c9734-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-190">False</span></span>                                                  |
| <span data-ttu-id="c9734-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-191">In Global Catalog</span></span>      | <span data-ttu-id="c9734-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-192">False</span></span>                                                  |
| <span data-ttu-id="c9734-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-194">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-195">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-196">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-197">Search-Flags</span></span>           | <span data-ttu-id="c9734-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-198">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-199">System-Flags</span></span>           | <span data-ttu-id="c9734-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-200">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-201">Classes used in</span></span>        | [<span data-ttu-id="c9734-202">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-202">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9734-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9734-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9734-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-204">Entry</span></span> | <span data-ttu-id="c9734-205">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-205">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-206">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-207">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-208">System-Only</span></span>            | <span data-ttu-id="c9734-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-209">False</span></span>                                                  |
| <span data-ttu-id="c9734-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-211">True</span><span class="sxs-lookup"><span data-stu-id="c9734-211">True</span></span>                                                   |
| <span data-ttu-id="c9734-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-212">Is Indexed</span></span>             | <span data-ttu-id="c9734-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-213">False</span></span>                                                  |
| <span data-ttu-id="c9734-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-214">In Global Catalog</span></span>      | <span data-ttu-id="c9734-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-215">False</span></span>                                                  |
| <span data-ttu-id="c9734-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-217">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-218">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-219">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-220">Search-Flags</span></span>           | <span data-ttu-id="c9734-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-221">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-222">System-Flags</span></span>           | <span data-ttu-id="c9734-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-223">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-224">Classes used in</span></span>        | [<span data-ttu-id="c9734-225">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-225">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9734-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9734-226">Windows Server 2008</span></span>



| <span data-ttu-id="c9734-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-227">Entry</span></span> | <span data-ttu-id="c9734-228">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-228">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-229">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-230">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-231">System-Only</span></span>            | <span data-ttu-id="c9734-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-232">False</span></span>                                                  |
| <span data-ttu-id="c9734-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-234">True</span><span class="sxs-lookup"><span data-stu-id="c9734-234">True</span></span>                                                   |
| <span data-ttu-id="c9734-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-235">Is Indexed</span></span>             | <span data-ttu-id="c9734-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-236">False</span></span>                                                  |
| <span data-ttu-id="c9734-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-237">In Global Catalog</span></span>      | <span data-ttu-id="c9734-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-238">False</span></span>                                                  |
| <span data-ttu-id="c9734-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-240">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-241">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-242">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-243">Search-Flags</span></span>           | <span data-ttu-id="c9734-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-244">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-245">System-Flags</span></span>           | <span data-ttu-id="c9734-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-246">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-247">Classes used in</span></span>        | [<span data-ttu-id="c9734-248">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-248">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9734-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9734-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9734-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-250">Entry</span></span> | <span data-ttu-id="c9734-251">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-251">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-252">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-253">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-254">System-Only</span></span>            | <span data-ttu-id="c9734-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-255">False</span></span>                                                  |
| <span data-ttu-id="c9734-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-257">True</span><span class="sxs-lookup"><span data-stu-id="c9734-257">True</span></span>                                                   |
| <span data-ttu-id="c9734-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-258">Is Indexed</span></span>             | <span data-ttu-id="c9734-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-259">False</span></span>                                                  |
| <span data-ttu-id="c9734-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-260">In Global Catalog</span></span>      | <span data-ttu-id="c9734-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-261">False</span></span>                                                  |
| <span data-ttu-id="c9734-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-263">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-264">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-265">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-266">Search-Flags</span></span>           | <span data-ttu-id="c9734-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-267">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-268">System-Flags</span></span>           | <span data-ttu-id="c9734-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-269">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-270">Classes used in</span></span>        | [<span data-ttu-id="c9734-271">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-271">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9734-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9734-272">Windows Server 2012</span></span>



| <span data-ttu-id="c9734-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9734-273">Entry</span></span> | <span data-ttu-id="c9734-274">Значение</span><span class="sxs-lookup"><span data-stu-id="c9734-274">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="c9734-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9734-275">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9734-276">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="c9734-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9734-277">System-Only</span></span>            | <span data-ttu-id="c9734-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-278">False</span></span>                                                  |
| <span data-ttu-id="c9734-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9734-279">Is-Single-Valued</span></span>       | <span data-ttu-id="c9734-280">True</span><span class="sxs-lookup"><span data-stu-id="c9734-280">True</span></span>                                                   |
| <span data-ttu-id="c9734-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9734-281">Is Indexed</span></span>             | <span data-ttu-id="c9734-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-282">False</span></span>                                                  |
| <span data-ttu-id="c9734-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9734-283">In Global Catalog</span></span>      | <span data-ttu-id="c9734-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9734-284">False</span></span>                                                  |
| <span data-ttu-id="c9734-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9734-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9734-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9734-286">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="c9734-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9734-287">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9734-288">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="c9734-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-289">Search-Flags</span></span>           | <span data-ttu-id="c9734-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9734-290">0x00000000</span></span>                                             |
| <span data-ttu-id="c9734-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9734-291">System-Flags</span></span>           | <span data-ttu-id="c9734-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9734-292">0x00000010</span></span>                                             |
| <span data-ttu-id="c9734-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9734-293">Classes used in</span></span>        | [<span data-ttu-id="c9734-294">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="c9734-294">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





