---
title: Атрибут Volume-Count
description: Квота на записанные тома для данного компьютера.
ms.assetid: a764a650-2cce-4df4-9a5e-d5fc8de196cb
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Volume-Count
- Схема AD атрибута Волумекаунт
topic_type:
- apiref
api_name:
- Volume-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2242926ce379cdba9a19ae1ad0dc2612a3375f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989617"
---
# <a name="volume-count-attribute"></a><span data-ttu-id="7a0b8-105">Атрибут Volume-Count</span><span class="sxs-lookup"><span data-stu-id="7a0b8-105">Volume-Count attribute</span></span>

<span data-ttu-id="7a0b8-106">Квота на записанные тома для данного компьютера.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-106">The tracked volume quota for a given computer.</span></span>



| <span data-ttu-id="7a0b8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-107">Entry</span></span> | <span data-ttu-id="7a0b8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7a0b8-109">CN</span><span class="sxs-lookup"><span data-stu-id="7a0b8-109">CN</span></span>                | <span data-ttu-id="7a0b8-110">Volume-Count</span><span class="sxs-lookup"><span data-stu-id="7a0b8-110">Volume-Count</span></span>                         |
| <span data-ttu-id="7a0b8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7a0b8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7a0b8-112">волумекаунт</span><span class="sxs-lookup"><span data-stu-id="7a0b8-112">volumeCount</span></span>                          |
| <span data-ttu-id="7a0b8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7a0b8-113">Size</span></span>              | <span data-ttu-id="7a0b8-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="7a0b8-114">4 bytes</span></span>                              |
| <span data-ttu-id="7a0b8-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7a0b8-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7a0b8-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7a0b8-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7a0b8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-117">Attribute-Id</span></span>      | <span data-ttu-id="7a0b8-118">1.2.840.113556.1.4.507</span><span class="sxs-lookup"><span data-stu-id="7a0b8-118">1.2.840.113556.1.4.507</span></span>               |
| <span data-ttu-id="7a0b8-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7a0b8-119">System-Id-Guid</span></span>    | <span data-ttu-id="7a0b8-120">34aaa217-b699-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7a0b8-120">34aaa217-b699-11d0-afee-0000f80367c1</span></span> |
| <span data-ttu-id="7a0b8-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a0b8-121">Syntax</span></span>            | [<span data-ttu-id="7a0b8-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7a0b8-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7a0b8-123">Implementations</span></span>

-   [<span data-ttu-id="7a0b8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7a0b8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a0b8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a0b8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a0b8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a0b8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7a0b8-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a0b8-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7a0b8-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-131">Entry</span></span> | <span data-ttu-id="7a0b8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="7a0b8-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a0b8-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a0b8-135">System-Only</span></span>            | <span data-ttu-id="7a0b8-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-136">False</span></span>                                     |
| <span data-ttu-id="7a0b8-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a0b8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7a0b8-138">True</span><span class="sxs-lookup"><span data-stu-id="7a0b8-138">True</span></span>                                      |
| <span data-ttu-id="7a0b8-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a0b8-139">Is Indexed</span></span>             | <span data-ttu-id="7a0b8-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-140">False</span></span>                                     |
| <span data-ttu-id="7a0b8-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a0b8-141">In Global Catalog</span></span>      | <span data-ttu-id="7a0b8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-142">False</span></span>                                     |
| <span data-ttu-id="7a0b8-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a0b8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a0b8-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a0b8-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="7a0b8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a0b8-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a0b8-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-147">Search-Flags</span></span>           | <span data-ttu-id="7a0b8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a0b8-148">0x00000000</span></span>                                |
| <span data-ttu-id="7a0b8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-149">System-Flags</span></span>           | <span data-ttu-id="7a0b8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a0b8-150">0x00000010</span></span>                                |
| <span data-ttu-id="7a0b8-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a0b8-151">Classes used in</span></span>        | [<span data-ttu-id="7a0b8-152">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7a0b8-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a0b8-153">Windows Server 2003</span></span>



| <span data-ttu-id="7a0b8-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-154">Entry</span></span> | <span data-ttu-id="7a0b8-155">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="7a0b8-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a0b8-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a0b8-158">System-Only</span></span>            | <span data-ttu-id="7a0b8-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-159">False</span></span>                                     |
| <span data-ttu-id="7a0b8-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a0b8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7a0b8-161">True</span><span class="sxs-lookup"><span data-stu-id="7a0b8-161">True</span></span>                                      |
| <span data-ttu-id="7a0b8-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a0b8-162">Is Indexed</span></span>             | <span data-ttu-id="7a0b8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-163">False</span></span>                                     |
| <span data-ttu-id="7a0b8-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a0b8-164">In Global Catalog</span></span>      | <span data-ttu-id="7a0b8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-165">False</span></span>                                     |
| <span data-ttu-id="7a0b8-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a0b8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a0b8-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a0b8-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="7a0b8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a0b8-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a0b8-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-170">Search-Flags</span></span>           | <span data-ttu-id="7a0b8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a0b8-171">0x00000000</span></span>                                |
| <span data-ttu-id="7a0b8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-172">System-Flags</span></span>           | <span data-ttu-id="7a0b8-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a0b8-173">0x00000010</span></span>                                |
| <span data-ttu-id="7a0b8-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a0b8-174">Classes used in</span></span>        | [<span data-ttu-id="7a0b8-175">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a0b8-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a0b8-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a0b8-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-177">Entry</span></span> | <span data-ttu-id="7a0b8-178">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="7a0b8-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a0b8-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a0b8-181">System-Only</span></span>            | <span data-ttu-id="7a0b8-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-182">False</span></span>                                     |
| <span data-ttu-id="7a0b8-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a0b8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7a0b8-184">True</span><span class="sxs-lookup"><span data-stu-id="7a0b8-184">True</span></span>                                      |
| <span data-ttu-id="7a0b8-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a0b8-185">Is Indexed</span></span>             | <span data-ttu-id="7a0b8-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-186">False</span></span>                                     |
| <span data-ttu-id="7a0b8-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a0b8-187">In Global Catalog</span></span>      | <span data-ttu-id="7a0b8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-188">False</span></span>                                     |
| <span data-ttu-id="7a0b8-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a0b8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a0b8-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a0b8-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="7a0b8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a0b8-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a0b8-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-193">Search-Flags</span></span>           | <span data-ttu-id="7a0b8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a0b8-194">0x00000000</span></span>                                |
| <span data-ttu-id="7a0b8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-195">System-Flags</span></span>           | <span data-ttu-id="7a0b8-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a0b8-196">0x00000010</span></span>                                |
| <span data-ttu-id="7a0b8-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a0b8-197">Classes used in</span></span>        | [<span data-ttu-id="7a0b8-198">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a0b8-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a0b8-199">Windows Server 2008</span></span>



| <span data-ttu-id="7a0b8-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-200">Entry</span></span> | <span data-ttu-id="7a0b8-201">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="7a0b8-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a0b8-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a0b8-204">System-Only</span></span>            | <span data-ttu-id="7a0b8-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-205">False</span></span>                                     |
| <span data-ttu-id="7a0b8-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a0b8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7a0b8-207">True</span><span class="sxs-lookup"><span data-stu-id="7a0b8-207">True</span></span>                                      |
| <span data-ttu-id="7a0b8-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a0b8-208">Is Indexed</span></span>             | <span data-ttu-id="7a0b8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-209">False</span></span>                                     |
| <span data-ttu-id="7a0b8-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a0b8-210">In Global Catalog</span></span>      | <span data-ttu-id="7a0b8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-211">False</span></span>                                     |
| <span data-ttu-id="7a0b8-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a0b8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a0b8-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a0b8-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="7a0b8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a0b8-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a0b8-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-216">Search-Flags</span></span>           | <span data-ttu-id="7a0b8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a0b8-217">0x00000000</span></span>                                |
| <span data-ttu-id="7a0b8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-218">System-Flags</span></span>           | <span data-ttu-id="7a0b8-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a0b8-219">0x00000010</span></span>                                |
| <span data-ttu-id="7a0b8-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a0b8-220">Classes used in</span></span>        | [<span data-ttu-id="7a0b8-221">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a0b8-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a0b8-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a0b8-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-223">Entry</span></span> | <span data-ttu-id="7a0b8-224">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="7a0b8-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a0b8-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a0b8-227">System-Only</span></span>            | <span data-ttu-id="7a0b8-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-228">False</span></span>                                     |
| <span data-ttu-id="7a0b8-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a0b8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7a0b8-230">True</span><span class="sxs-lookup"><span data-stu-id="7a0b8-230">True</span></span>                                      |
| <span data-ttu-id="7a0b8-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a0b8-231">Is Indexed</span></span>             | <span data-ttu-id="7a0b8-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-232">False</span></span>                                     |
| <span data-ttu-id="7a0b8-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a0b8-233">In Global Catalog</span></span>      | <span data-ttu-id="7a0b8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-234">False</span></span>                                     |
| <span data-ttu-id="7a0b8-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a0b8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a0b8-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a0b8-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="7a0b8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a0b8-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a0b8-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-239">Search-Flags</span></span>           | <span data-ttu-id="7a0b8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a0b8-240">0x00000000</span></span>                                |
| <span data-ttu-id="7a0b8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-241">System-Flags</span></span>           | <span data-ttu-id="7a0b8-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a0b8-242">0x00000010</span></span>                                |
| <span data-ttu-id="7a0b8-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a0b8-243">Classes used in</span></span>        | [<span data-ttu-id="7a0b8-244">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a0b8-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a0b8-245">Windows Server 2012</span></span>



| <span data-ttu-id="7a0b8-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a0b8-246">Entry</span></span> | <span data-ttu-id="7a0b8-247">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0b8-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="7a0b8-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a0b8-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a0b8-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="7a0b8-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a0b8-250">System-Only</span></span>            | <span data-ttu-id="7a0b8-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-251">False</span></span>                                     |
| <span data-ttu-id="7a0b8-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a0b8-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7a0b8-253">True</span><span class="sxs-lookup"><span data-stu-id="7a0b8-253">True</span></span>                                      |
| <span data-ttu-id="7a0b8-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a0b8-254">Is Indexed</span></span>             | <span data-ttu-id="7a0b8-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-255">False</span></span>                                     |
| <span data-ttu-id="7a0b8-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a0b8-256">In Global Catalog</span></span>      | <span data-ttu-id="7a0b8-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a0b8-257">False</span></span>                                     |
| <span data-ttu-id="7a0b8-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a0b8-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a0b8-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a0b8-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="7a0b8-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a0b8-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a0b8-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="7a0b8-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-262">Search-Flags</span></span>           | <span data-ttu-id="7a0b8-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a0b8-263">0x00000000</span></span>                                |
| <span data-ttu-id="7a0b8-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a0b8-264">System-Flags</span></span>           | <span data-ttu-id="7a0b8-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a0b8-265">0x00000010</span></span>                                |
| <span data-ttu-id="7a0b8-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a0b8-266">Classes used in</span></span>        | [<span data-ttu-id="7a0b8-267">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





