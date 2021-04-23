---
title: FRS-Control-Outbound-атрибут невыполненной работы
description: Пара "предупреждение" или "уровень ошибки" для исходящей невыполненной работы (число файлов).
ms.assetid: d35b4605-c336-4ed0-af8c-da5c9534e5c2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута невыполненной работы FRS-Control-Outbound
- Схема AD атрибута Фрсконтролаутбаундбакклог
topic_type:
- apiref
api_name:
- FRS-Control-Outbound-Backlog
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b3201f782735658a53dcb0e802106c86267df4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804421"
---
# <a name="frs-control-outbound-backlog-attribute"></a><span data-ttu-id="de4fa-105">FRS-Control-Outbound-атрибут невыполненной работы</span><span class="sxs-lookup"><span data-stu-id="de4fa-105">FRS-Control-Outbound-Backlog attribute</span></span>

<span data-ttu-id="de4fa-106">Пара "предупреждение" или "уровень ошибки" для исходящей невыполненной работы (число файлов).</span><span class="sxs-lookup"><span data-stu-id="de4fa-106">Warning/Error level pair for outbound backlog (number of files).</span></span>



| <span data-ttu-id="de4fa-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-107">Entry</span></span> | <span data-ttu-id="de4fa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="de4fa-109">CN</span><span class="sxs-lookup"><span data-stu-id="de4fa-109">CN</span></span>                | <span data-ttu-id="de4fa-110">FRS-Control-Outbound-невыполненная работа</span><span class="sxs-lookup"><span data-stu-id="de4fa-110">FRS-Control-Outbound-Backlog</span></span>                |
| <span data-ttu-id="de4fa-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="de4fa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="de4fa-112">фрсконтролаутбаундбакклог</span><span class="sxs-lookup"><span data-stu-id="de4fa-112">fRSControlOutboundBacklog</span></span>                   |
| <span data-ttu-id="de4fa-113">Размер</span><span class="sxs-lookup"><span data-stu-id="de4fa-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="de4fa-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="de4fa-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="de4fa-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="de4fa-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="de4fa-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-116">Attribute-Id</span></span>      | <span data-ttu-id="de4fa-117">1.2.840.113556.1.4.873</span><span class="sxs-lookup"><span data-stu-id="de4fa-117">1.2.840.113556.1.4.873</span></span>                      |
| <span data-ttu-id="de4fa-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="de4fa-118">System-Id-Guid</span></span>    | <span data-ttu-id="de4fa-119">2a13257c-9373-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="de4fa-119">2a13257c-9373-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="de4fa-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de4fa-120">Syntax</span></span>            | [<span data-ttu-id="de4fa-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="de4fa-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="de4fa-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="de4fa-122">Implementations</span></span>

-   [<span data-ttu-id="de4fa-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="de4fa-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="de4fa-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de4fa-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de4fa-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de4fa-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de4fa-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de4fa-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de4fa-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de4fa-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de4fa-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de4fa-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="de4fa-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de4fa-129">Windows 2000 Server</span></span>



| <span data-ttu-id="de4fa-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-130">Entry</span></span> | <span data-ttu-id="de4fa-131">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-131">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="de4fa-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de4fa-132">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-133">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="de4fa-134">System-Only</span></span>            | <span data-ttu-id="de4fa-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-135">False</span></span>                                            |
| <span data-ttu-id="de4fa-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de4fa-136">Is-Single-Valued</span></span>       | <span data-ttu-id="de4fa-137">True</span><span class="sxs-lookup"><span data-stu-id="de4fa-137">True</span></span>                                             |
| <span data-ttu-id="de4fa-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de4fa-138">Is Indexed</span></span>             | <span data-ttu-id="de4fa-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-139">False</span></span>                                            |
| <span data-ttu-id="de4fa-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de4fa-140">In Global Catalog</span></span>      | <span data-ttu-id="de4fa-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-141">False</span></span>                                            |
| <span data-ttu-id="de4fa-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de4fa-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="de4fa-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de4fa-143">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="de4fa-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de4fa-144">Range-Lower</span></span>            | <span data-ttu-id="de4fa-145">0</span><span class="sxs-lookup"><span data-stu-id="de4fa-145">0</span></span>                                                |
| <span data-ttu-id="de4fa-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de4fa-146">Range-Upper</span></span>            | <span data-ttu-id="de4fa-147">32</span><span class="sxs-lookup"><span data-stu-id="de4fa-147">32</span></span>                                               |
| <span data-ttu-id="de4fa-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-148">Search-Flags</span></span>           | <span data-ttu-id="de4fa-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de4fa-149">0x00000000</span></span>                                       |
| <span data-ttu-id="de4fa-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-150">System-Flags</span></span>           | <span data-ttu-id="de4fa-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de4fa-151">0x00000010</span></span>                                       |
| <span data-ttu-id="de4fa-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de4fa-152">Classes used in</span></span>        | [<span data-ttu-id="de4fa-153">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="de4fa-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="de4fa-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de4fa-154">Windows Server 2003</span></span>



| <span data-ttu-id="de4fa-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-155">Entry</span></span> | <span data-ttu-id="de4fa-156">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="de4fa-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de4fa-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="de4fa-159">System-Only</span></span>            | <span data-ttu-id="de4fa-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-160">False</span></span>                                            |
| <span data-ttu-id="de4fa-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de4fa-161">Is-Single-Valued</span></span>       | <span data-ttu-id="de4fa-162">True</span><span class="sxs-lookup"><span data-stu-id="de4fa-162">True</span></span>                                             |
| <span data-ttu-id="de4fa-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de4fa-163">Is Indexed</span></span>             | <span data-ttu-id="de4fa-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-164">False</span></span>                                            |
| <span data-ttu-id="de4fa-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de4fa-165">In Global Catalog</span></span>      | <span data-ttu-id="de4fa-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-166">False</span></span>                                            |
| <span data-ttu-id="de4fa-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de4fa-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="de4fa-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de4fa-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="de4fa-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de4fa-169">Range-Lower</span></span>            | <span data-ttu-id="de4fa-170">0</span><span class="sxs-lookup"><span data-stu-id="de4fa-170">0</span></span>                                                |
| <span data-ttu-id="de4fa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de4fa-171">Range-Upper</span></span>            | <span data-ttu-id="de4fa-172">32</span><span class="sxs-lookup"><span data-stu-id="de4fa-172">32</span></span>                                               |
| <span data-ttu-id="de4fa-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-173">Search-Flags</span></span>           | <span data-ttu-id="de4fa-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de4fa-174">0x00000000</span></span>                                       |
| <span data-ttu-id="de4fa-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-175">System-Flags</span></span>           | <span data-ttu-id="de4fa-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de4fa-176">0x00000010</span></span>                                       |
| <span data-ttu-id="de4fa-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de4fa-177">Classes used in</span></span>        | [<span data-ttu-id="de4fa-178">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="de4fa-178">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de4fa-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de4fa-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de4fa-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-180">Entry</span></span> | <span data-ttu-id="de4fa-181">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="de4fa-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de4fa-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="de4fa-184">System-Only</span></span>            | <span data-ttu-id="de4fa-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-185">False</span></span>                                            |
| <span data-ttu-id="de4fa-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de4fa-186">Is-Single-Valued</span></span>       | <span data-ttu-id="de4fa-187">True</span><span class="sxs-lookup"><span data-stu-id="de4fa-187">True</span></span>                                             |
| <span data-ttu-id="de4fa-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de4fa-188">Is Indexed</span></span>             | <span data-ttu-id="de4fa-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-189">False</span></span>                                            |
| <span data-ttu-id="de4fa-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de4fa-190">In Global Catalog</span></span>      | <span data-ttu-id="de4fa-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-191">False</span></span>                                            |
| <span data-ttu-id="de4fa-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de4fa-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="de4fa-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de4fa-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="de4fa-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de4fa-194">Range-Lower</span></span>            | <span data-ttu-id="de4fa-195">0</span><span class="sxs-lookup"><span data-stu-id="de4fa-195">0</span></span>                                                |
| <span data-ttu-id="de4fa-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de4fa-196">Range-Upper</span></span>            | <span data-ttu-id="de4fa-197">32</span><span class="sxs-lookup"><span data-stu-id="de4fa-197">32</span></span>                                               |
| <span data-ttu-id="de4fa-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-198">Search-Flags</span></span>           | <span data-ttu-id="de4fa-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de4fa-199">0x00000000</span></span>                                       |
| <span data-ttu-id="de4fa-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-200">System-Flags</span></span>           | <span data-ttu-id="de4fa-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de4fa-201">0x00000010</span></span>                                       |
| <span data-ttu-id="de4fa-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de4fa-202">Classes used in</span></span>        | [<span data-ttu-id="de4fa-203">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="de4fa-203">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de4fa-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de4fa-204">Windows Server 2008</span></span>



| <span data-ttu-id="de4fa-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-205">Entry</span></span> | <span data-ttu-id="de4fa-206">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="de4fa-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de4fa-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="de4fa-209">System-Only</span></span>            | <span data-ttu-id="de4fa-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-210">False</span></span>                                            |
| <span data-ttu-id="de4fa-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de4fa-211">Is-Single-Valued</span></span>       | <span data-ttu-id="de4fa-212">True</span><span class="sxs-lookup"><span data-stu-id="de4fa-212">True</span></span>                                             |
| <span data-ttu-id="de4fa-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de4fa-213">Is Indexed</span></span>             | <span data-ttu-id="de4fa-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-214">False</span></span>                                            |
| <span data-ttu-id="de4fa-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de4fa-215">In Global Catalog</span></span>      | <span data-ttu-id="de4fa-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-216">False</span></span>                                            |
| <span data-ttu-id="de4fa-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de4fa-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="de4fa-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de4fa-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="de4fa-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de4fa-219">Range-Lower</span></span>            | <span data-ttu-id="de4fa-220">0</span><span class="sxs-lookup"><span data-stu-id="de4fa-220">0</span></span>                                                |
| <span data-ttu-id="de4fa-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de4fa-221">Range-Upper</span></span>            | <span data-ttu-id="de4fa-222">32</span><span class="sxs-lookup"><span data-stu-id="de4fa-222">32</span></span>                                               |
| <span data-ttu-id="de4fa-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-223">Search-Flags</span></span>           | <span data-ttu-id="de4fa-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de4fa-224">0x00000000</span></span>                                       |
| <span data-ttu-id="de4fa-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-225">System-Flags</span></span>           | <span data-ttu-id="de4fa-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de4fa-226">0x00000010</span></span>                                       |
| <span data-ttu-id="de4fa-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de4fa-227">Classes used in</span></span>        | [<span data-ttu-id="de4fa-228">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="de4fa-228">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de4fa-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de4fa-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de4fa-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-230">Entry</span></span> | <span data-ttu-id="de4fa-231">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-231">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="de4fa-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de4fa-232">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-233">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="de4fa-234">System-Only</span></span>            | <span data-ttu-id="de4fa-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-235">False</span></span>                                            |
| <span data-ttu-id="de4fa-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de4fa-236">Is-Single-Valued</span></span>       | <span data-ttu-id="de4fa-237">True</span><span class="sxs-lookup"><span data-stu-id="de4fa-237">True</span></span>                                             |
| <span data-ttu-id="de4fa-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de4fa-238">Is Indexed</span></span>             | <span data-ttu-id="de4fa-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-239">False</span></span>                                            |
| <span data-ttu-id="de4fa-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de4fa-240">In Global Catalog</span></span>      | <span data-ttu-id="de4fa-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-241">False</span></span>                                            |
| <span data-ttu-id="de4fa-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de4fa-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="de4fa-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de4fa-243">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="de4fa-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de4fa-244">Range-Lower</span></span>            | <span data-ttu-id="de4fa-245">0</span><span class="sxs-lookup"><span data-stu-id="de4fa-245">0</span></span>                                                |
| <span data-ttu-id="de4fa-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de4fa-246">Range-Upper</span></span>            | <span data-ttu-id="de4fa-247">32</span><span class="sxs-lookup"><span data-stu-id="de4fa-247">32</span></span>                                               |
| <span data-ttu-id="de4fa-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-248">Search-Flags</span></span>           | <span data-ttu-id="de4fa-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de4fa-249">0x00000000</span></span>                                       |
| <span data-ttu-id="de4fa-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-250">System-Flags</span></span>           | <span data-ttu-id="de4fa-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de4fa-251">0x00000010</span></span>                                       |
| <span data-ttu-id="de4fa-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de4fa-252">Classes used in</span></span>        | [<span data-ttu-id="de4fa-253">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="de4fa-253">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de4fa-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de4fa-254">Windows Server 2012</span></span>



| <span data-ttu-id="de4fa-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="de4fa-255">Entry</span></span> | <span data-ttu-id="de4fa-256">Значение</span><span class="sxs-lookup"><span data-stu-id="de4fa-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="de4fa-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de4fa-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de4fa-258">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="de4fa-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="de4fa-259">System-Only</span></span>            | <span data-ttu-id="de4fa-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-260">False</span></span>                                            |
| <span data-ttu-id="de4fa-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de4fa-261">Is-Single-Valued</span></span>       | <span data-ttu-id="de4fa-262">True</span><span class="sxs-lookup"><span data-stu-id="de4fa-262">True</span></span>                                             |
| <span data-ttu-id="de4fa-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de4fa-263">Is Indexed</span></span>             | <span data-ttu-id="de4fa-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-264">False</span></span>                                            |
| <span data-ttu-id="de4fa-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de4fa-265">In Global Catalog</span></span>      | <span data-ttu-id="de4fa-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="de4fa-266">False</span></span>                                            |
| <span data-ttu-id="de4fa-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de4fa-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="de4fa-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de4fa-268">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="de4fa-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de4fa-269">Range-Lower</span></span>            | <span data-ttu-id="de4fa-270">0</span><span class="sxs-lookup"><span data-stu-id="de4fa-270">0</span></span>                                                |
| <span data-ttu-id="de4fa-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de4fa-271">Range-Upper</span></span>            | <span data-ttu-id="de4fa-272">32</span><span class="sxs-lookup"><span data-stu-id="de4fa-272">32</span></span>                                               |
| <span data-ttu-id="de4fa-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-273">Search-Flags</span></span>           | <span data-ttu-id="de4fa-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de4fa-274">0x00000000</span></span>                                       |
| <span data-ttu-id="de4fa-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de4fa-275">System-Flags</span></span>           | <span data-ttu-id="de4fa-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de4fa-276">0x00000010</span></span>                                       |
| <span data-ttu-id="de4fa-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de4fa-277">Classes used in</span></span>        | [<span data-ttu-id="de4fa-278">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="de4fa-278">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



 

 





