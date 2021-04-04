---
title: FRS-Control-Inbound-атрибут невыполненной работы
description: Пара "предупреждение" или "уровень ошибки" для входящего невыполненной работы (число файлов).
ms.assetid: 4b3cc978-cdc5-4423-a78d-477e4bc5e489
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута невыполненной работы FRS-Control-Inbound
- Схема AD атрибута Фрсконтролинбаундбакклог
topic_type:
- apiref
api_name:
- FRS-Control-Inbound-Backlog
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e45a6b535c889d9482b78165a4317fb54826cf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989529"
---
# <a name="frs-control-inbound-backlog-attribute"></a><span data-ttu-id="58a59-105">FRS-Control-Inbound-атрибут невыполненной работы</span><span class="sxs-lookup"><span data-stu-id="58a59-105">FRS-Control-Inbound-Backlog attribute</span></span>

<span data-ttu-id="58a59-106">Пара "предупреждение" или "уровень ошибки" для входящего невыполненной работы (число файлов).</span><span class="sxs-lookup"><span data-stu-id="58a59-106">Warning/Error level pair for inbound backlog (number of files).</span></span>



| <span data-ttu-id="58a59-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-107">Entry</span></span> | <span data-ttu-id="58a59-108">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="58a59-109">CN</span><span class="sxs-lookup"><span data-stu-id="58a59-109">CN</span></span>                | <span data-ttu-id="58a59-110">Служба FRS-Control-Inbound-невыполненная работа</span><span class="sxs-lookup"><span data-stu-id="58a59-110">FRS-Control-Inbound-Backlog</span></span>                 |
| <span data-ttu-id="58a59-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="58a59-111">Ldap-Display-Name</span></span> | <span data-ttu-id="58a59-112">фрсконтролинбаундбакклог</span><span class="sxs-lookup"><span data-stu-id="58a59-112">fRSControlInboundBacklog</span></span>                    |
| <span data-ttu-id="58a59-113">Размер</span><span class="sxs-lookup"><span data-stu-id="58a59-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="58a59-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="58a59-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="58a59-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="58a59-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="58a59-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-116">Attribute-Id</span></span>      | <span data-ttu-id="58a59-117">1.2.840.113556.1.4.872</span><span class="sxs-lookup"><span data-stu-id="58a59-117">1.2.840.113556.1.4.872</span></span>                      |
| <span data-ttu-id="58a59-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="58a59-118">System-Id-Guid</span></span>    | <span data-ttu-id="58a59-119">2a13257b-9373-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="58a59-119">2a13257b-9373-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="58a59-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58a59-120">Syntax</span></span>            | [<span data-ttu-id="58a59-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="58a59-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="58a59-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="58a59-122">Implementations</span></span>

-   [<span data-ttu-id="58a59-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="58a59-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="58a59-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58a59-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58a59-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58a59-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58a59-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58a59-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58a59-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58a59-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58a59-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58a59-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="58a59-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58a59-129">Windows 2000 Server</span></span>



| <span data-ttu-id="58a59-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-130">Entry</span></span> | <span data-ttu-id="58a59-131">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-131">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="58a59-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a59-132">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-133">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a59-134">System-Only</span></span>            | <span data-ttu-id="58a59-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-135">False</span></span>                                            |
| <span data-ttu-id="58a59-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a59-136">Is-Single-Valued</span></span>       | <span data-ttu-id="58a59-137">True</span><span class="sxs-lookup"><span data-stu-id="58a59-137">True</span></span>                                             |
| <span data-ttu-id="58a59-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a59-138">Is Indexed</span></span>             | <span data-ttu-id="58a59-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-139">False</span></span>                                            |
| <span data-ttu-id="58a59-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a59-140">In Global Catalog</span></span>      | <span data-ttu-id="58a59-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-141">False</span></span>                                            |
| <span data-ttu-id="58a59-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a59-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a59-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a59-143">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="58a59-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a59-144">Range-Lower</span></span>            | <span data-ttu-id="58a59-145">0</span><span class="sxs-lookup"><span data-stu-id="58a59-145">0</span></span>                                                |
| <span data-ttu-id="58a59-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a59-146">Range-Upper</span></span>            | <span data-ttu-id="58a59-147">32</span><span class="sxs-lookup"><span data-stu-id="58a59-147">32</span></span>                                               |
| <span data-ttu-id="58a59-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-148">Search-Flags</span></span>           | <span data-ttu-id="58a59-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a59-149">0x00000000</span></span>                                       |
| <span data-ttu-id="58a59-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-150">System-Flags</span></span>           | <span data-ttu-id="58a59-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a59-151">0x00000010</span></span>                                       |
| <span data-ttu-id="58a59-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a59-152">Classes used in</span></span>        | [<span data-ttu-id="58a59-153">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="58a59-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="58a59-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58a59-154">Windows Server 2003</span></span>



| <span data-ttu-id="58a59-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-155">Entry</span></span> | <span data-ttu-id="58a59-156">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="58a59-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a59-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a59-159">System-Only</span></span>            | <span data-ttu-id="58a59-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-160">False</span></span>                                            |
| <span data-ttu-id="58a59-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a59-161">Is-Single-Valued</span></span>       | <span data-ttu-id="58a59-162">True</span><span class="sxs-lookup"><span data-stu-id="58a59-162">True</span></span>                                             |
| <span data-ttu-id="58a59-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a59-163">Is Indexed</span></span>             | <span data-ttu-id="58a59-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-164">False</span></span>                                            |
| <span data-ttu-id="58a59-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a59-165">In Global Catalog</span></span>      | <span data-ttu-id="58a59-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-166">False</span></span>                                            |
| <span data-ttu-id="58a59-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a59-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a59-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a59-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="58a59-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a59-169">Range-Lower</span></span>            | <span data-ttu-id="58a59-170">0</span><span class="sxs-lookup"><span data-stu-id="58a59-170">0</span></span>                                                |
| <span data-ttu-id="58a59-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a59-171">Range-Upper</span></span>            | <span data-ttu-id="58a59-172">32</span><span class="sxs-lookup"><span data-stu-id="58a59-172">32</span></span>                                               |
| <span data-ttu-id="58a59-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-173">Search-Flags</span></span>           | <span data-ttu-id="58a59-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a59-174">0x00000000</span></span>                                       |
| <span data-ttu-id="58a59-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-175">System-Flags</span></span>           | <span data-ttu-id="58a59-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a59-176">0x00000010</span></span>                                       |
| <span data-ttu-id="58a59-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a59-177">Classes used in</span></span>        | [<span data-ttu-id="58a59-178">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="58a59-178">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58a59-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58a59-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58a59-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-180">Entry</span></span> | <span data-ttu-id="58a59-181">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="58a59-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a59-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a59-184">System-Only</span></span>            | <span data-ttu-id="58a59-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-185">False</span></span>                                            |
| <span data-ttu-id="58a59-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a59-186">Is-Single-Valued</span></span>       | <span data-ttu-id="58a59-187">True</span><span class="sxs-lookup"><span data-stu-id="58a59-187">True</span></span>                                             |
| <span data-ttu-id="58a59-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a59-188">Is Indexed</span></span>             | <span data-ttu-id="58a59-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-189">False</span></span>                                            |
| <span data-ttu-id="58a59-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a59-190">In Global Catalog</span></span>      | <span data-ttu-id="58a59-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-191">False</span></span>                                            |
| <span data-ttu-id="58a59-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a59-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a59-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a59-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="58a59-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a59-194">Range-Lower</span></span>            | <span data-ttu-id="58a59-195">0</span><span class="sxs-lookup"><span data-stu-id="58a59-195">0</span></span>                                                |
| <span data-ttu-id="58a59-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a59-196">Range-Upper</span></span>            | <span data-ttu-id="58a59-197">32</span><span class="sxs-lookup"><span data-stu-id="58a59-197">32</span></span>                                               |
| <span data-ttu-id="58a59-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-198">Search-Flags</span></span>           | <span data-ttu-id="58a59-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a59-199">0x00000000</span></span>                                       |
| <span data-ttu-id="58a59-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-200">System-Flags</span></span>           | <span data-ttu-id="58a59-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a59-201">0x00000010</span></span>                                       |
| <span data-ttu-id="58a59-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a59-202">Classes used in</span></span>        | [<span data-ttu-id="58a59-203">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="58a59-203">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58a59-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58a59-204">Windows Server 2008</span></span>



| <span data-ttu-id="58a59-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-205">Entry</span></span> | <span data-ttu-id="58a59-206">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="58a59-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a59-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a59-209">System-Only</span></span>            | <span data-ttu-id="58a59-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-210">False</span></span>                                            |
| <span data-ttu-id="58a59-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a59-211">Is-Single-Valued</span></span>       | <span data-ttu-id="58a59-212">True</span><span class="sxs-lookup"><span data-stu-id="58a59-212">True</span></span>                                             |
| <span data-ttu-id="58a59-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a59-213">Is Indexed</span></span>             | <span data-ttu-id="58a59-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-214">False</span></span>                                            |
| <span data-ttu-id="58a59-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a59-215">In Global Catalog</span></span>      | <span data-ttu-id="58a59-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-216">False</span></span>                                            |
| <span data-ttu-id="58a59-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a59-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a59-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a59-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="58a59-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a59-219">Range-Lower</span></span>            | <span data-ttu-id="58a59-220">0</span><span class="sxs-lookup"><span data-stu-id="58a59-220">0</span></span>                                                |
| <span data-ttu-id="58a59-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a59-221">Range-Upper</span></span>            | <span data-ttu-id="58a59-222">32</span><span class="sxs-lookup"><span data-stu-id="58a59-222">32</span></span>                                               |
| <span data-ttu-id="58a59-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-223">Search-Flags</span></span>           | <span data-ttu-id="58a59-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a59-224">0x00000000</span></span>                                       |
| <span data-ttu-id="58a59-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-225">System-Flags</span></span>           | <span data-ttu-id="58a59-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a59-226">0x00000010</span></span>                                       |
| <span data-ttu-id="58a59-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a59-227">Classes used in</span></span>        | [<span data-ttu-id="58a59-228">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="58a59-228">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58a59-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58a59-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58a59-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-230">Entry</span></span> | <span data-ttu-id="58a59-231">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-231">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="58a59-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a59-232">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-233">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a59-234">System-Only</span></span>            | <span data-ttu-id="58a59-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-235">False</span></span>                                            |
| <span data-ttu-id="58a59-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a59-236">Is-Single-Valued</span></span>       | <span data-ttu-id="58a59-237">True</span><span class="sxs-lookup"><span data-stu-id="58a59-237">True</span></span>                                             |
| <span data-ttu-id="58a59-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a59-238">Is Indexed</span></span>             | <span data-ttu-id="58a59-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-239">False</span></span>                                            |
| <span data-ttu-id="58a59-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a59-240">In Global Catalog</span></span>      | <span data-ttu-id="58a59-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-241">False</span></span>                                            |
| <span data-ttu-id="58a59-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a59-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a59-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a59-243">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="58a59-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a59-244">Range-Lower</span></span>            | <span data-ttu-id="58a59-245">0</span><span class="sxs-lookup"><span data-stu-id="58a59-245">0</span></span>                                                |
| <span data-ttu-id="58a59-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a59-246">Range-Upper</span></span>            | <span data-ttu-id="58a59-247">32</span><span class="sxs-lookup"><span data-stu-id="58a59-247">32</span></span>                                               |
| <span data-ttu-id="58a59-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-248">Search-Flags</span></span>           | <span data-ttu-id="58a59-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a59-249">0x00000000</span></span>                                       |
| <span data-ttu-id="58a59-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-250">System-Flags</span></span>           | <span data-ttu-id="58a59-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a59-251">0x00000010</span></span>                                       |
| <span data-ttu-id="58a59-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a59-252">Classes used in</span></span>        | [<span data-ttu-id="58a59-253">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="58a59-253">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58a59-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58a59-254">Windows Server 2012</span></span>



| <span data-ttu-id="58a59-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="58a59-255">Entry</span></span> | <span data-ttu-id="58a59-256">Значение</span><span class="sxs-lookup"><span data-stu-id="58a59-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="58a59-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58a59-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58a59-258">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="58a59-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="58a59-259">System-Only</span></span>            | <span data-ttu-id="58a59-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-260">False</span></span>                                            |
| <span data-ttu-id="58a59-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58a59-261">Is-Single-Valued</span></span>       | <span data-ttu-id="58a59-262">True</span><span class="sxs-lookup"><span data-stu-id="58a59-262">True</span></span>                                             |
| <span data-ttu-id="58a59-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58a59-263">Is Indexed</span></span>             | <span data-ttu-id="58a59-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-264">False</span></span>                                            |
| <span data-ttu-id="58a59-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58a59-265">In Global Catalog</span></span>      | <span data-ttu-id="58a59-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="58a59-266">False</span></span>                                            |
| <span data-ttu-id="58a59-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58a59-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="58a59-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58a59-268">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="58a59-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58a59-269">Range-Lower</span></span>            | <span data-ttu-id="58a59-270">0</span><span class="sxs-lookup"><span data-stu-id="58a59-270">0</span></span>                                                |
| <span data-ttu-id="58a59-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58a59-271">Range-Upper</span></span>            | <span data-ttu-id="58a59-272">32</span><span class="sxs-lookup"><span data-stu-id="58a59-272">32</span></span>                                               |
| <span data-ttu-id="58a59-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-273">Search-Flags</span></span>           | <span data-ttu-id="58a59-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58a59-274">0x00000000</span></span>                                       |
| <span data-ttu-id="58a59-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58a59-275">System-Flags</span></span>           | <span data-ttu-id="58a59-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58a59-276">0x00000010</span></span>                                       |
| <span data-ttu-id="58a59-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58a59-277">Classes used in</span></span>        | [<span data-ttu-id="58a59-278">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="58a59-278">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



 

 





