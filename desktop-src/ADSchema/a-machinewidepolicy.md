---
title: Атрибут политики на уровне компьютера
description: Используется для репликации расширяемой политики пользователя на клиентах.
ms.assetid: e8ce40b8-7658-4e4b-b0e1-b68031811dd1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута политики на уровне компьютера
- Схема AD атрибута Мачиневидеполици
topic_type:
- apiref
api_name:
- Machine-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd3af77dfb501000369b3c4ae23b3f5f64f0da9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989561"
---
# <a name="machine-wide-policy-attribute"></a><span data-ttu-id="c5563-105">Атрибут политики на уровне компьютера</span><span class="sxs-lookup"><span data-stu-id="c5563-105">Machine-Wide-Policy attribute</span></span>

<span data-ttu-id="c5563-106">Используется для репликации расширяемой политики пользователя на клиентах.</span><span class="sxs-lookup"><span data-stu-id="c5563-106">Used to replicate the user-extensible policy to the clients.</span></span>



| <span data-ttu-id="c5563-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-107">Entry</span></span> | <span data-ttu-id="c5563-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c5563-109">CN</span><span class="sxs-lookup"><span data-stu-id="c5563-109">CN</span></span>                | <span data-ttu-id="c5563-110">Политика на уровне компьютера</span><span class="sxs-lookup"><span data-stu-id="c5563-110">Machine-Wide-Policy</span></span>                                   |
| <span data-ttu-id="c5563-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c5563-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c5563-112">мачиневидеполици</span><span class="sxs-lookup"><span data-stu-id="c5563-112">machineWidePolicy</span></span>                                     |
| <span data-ttu-id="c5563-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c5563-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c5563-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c5563-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c5563-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c5563-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c5563-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-116">Attribute-Id</span></span>      | <span data-ttu-id="c5563-117">1.2.840.113556.1.4.459</span><span class="sxs-lookup"><span data-stu-id="c5563-117">1.2.840.113556.1.4.459</span></span>                                |
| <span data-ttu-id="c5563-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c5563-118">System-Id-Guid</span></span>    | <span data-ttu-id="c5563-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c5563-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="c5563-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5563-120">Syntax</span></span>            | [<span data-ttu-id="c5563-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="c5563-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c5563-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c5563-122">Implementations</span></span>

-   [<span data-ttu-id="c5563-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c5563-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c5563-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c5563-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c5563-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c5563-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c5563-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c5563-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c5563-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c5563-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c5563-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c5563-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c5563-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5563-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c5563-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-130">Entry</span></span> | <span data-ttu-id="c5563-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c5563-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c5563-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5563-134">System-Only</span></span>            | <span data-ttu-id="c5563-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-135">False</span></span>        |
| <span data-ttu-id="c5563-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c5563-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c5563-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-137">False</span></span>        |
| <span data-ttu-id="c5563-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c5563-138">Is Indexed</span></span>             | <span data-ttu-id="c5563-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-139">False</span></span>        |
| <span data-ttu-id="c5563-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c5563-140">In Global Catalog</span></span>      | <span data-ttu-id="c5563-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-141">False</span></span>        |
| <span data-ttu-id="c5563-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c5563-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5563-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c5563-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c5563-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5563-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c5563-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5563-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c5563-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-146">Search-Flags</span></span>           | <span data-ttu-id="c5563-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5563-147">0x00000000</span></span>   |
| <span data-ttu-id="c5563-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-148">System-Flags</span></span>           | <span data-ttu-id="c5563-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5563-149">0x00000010</span></span>   |
| <span data-ttu-id="c5563-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c5563-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="c5563-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5563-151">Windows Server 2003</span></span>



| <span data-ttu-id="c5563-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-152">Entry</span></span> | <span data-ttu-id="c5563-153">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c5563-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c5563-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5563-156">System-Only</span></span>            | <span data-ttu-id="c5563-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-157">False</span></span>        |
| <span data-ttu-id="c5563-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c5563-158">Is-Single-Valued</span></span>       | <span data-ttu-id="c5563-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-159">False</span></span>        |
| <span data-ttu-id="c5563-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c5563-160">Is Indexed</span></span>             | <span data-ttu-id="c5563-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-161">False</span></span>        |
| <span data-ttu-id="c5563-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c5563-162">In Global Catalog</span></span>      | <span data-ttu-id="c5563-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-163">False</span></span>        |
| <span data-ttu-id="c5563-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c5563-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5563-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c5563-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c5563-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5563-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c5563-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5563-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c5563-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-168">Search-Flags</span></span>           | <span data-ttu-id="c5563-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5563-169">0x00000000</span></span>   |
| <span data-ttu-id="c5563-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-170">System-Flags</span></span>           | <span data-ttu-id="c5563-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5563-171">0x00000010</span></span>   |
| <span data-ttu-id="c5563-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c5563-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c5563-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c5563-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c5563-174">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-174">Entry</span></span> | <span data-ttu-id="c5563-175">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c5563-176">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c5563-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5563-178">System-Only</span></span>            | <span data-ttu-id="c5563-179">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-179">False</span></span>        |
| <span data-ttu-id="c5563-180">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c5563-180">Is-Single-Valued</span></span>       | <span data-ttu-id="c5563-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-181">False</span></span>        |
| <span data-ttu-id="c5563-182">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c5563-182">Is Indexed</span></span>             | <span data-ttu-id="c5563-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-183">False</span></span>        |
| <span data-ttu-id="c5563-184">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c5563-184">In Global Catalog</span></span>      | <span data-ttu-id="c5563-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-185">False</span></span>        |
| <span data-ttu-id="c5563-186">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c5563-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5563-187">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c5563-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c5563-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5563-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c5563-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5563-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c5563-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-190">Search-Flags</span></span>           | <span data-ttu-id="c5563-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5563-191">0x00000000</span></span>   |
| <span data-ttu-id="c5563-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-192">System-Flags</span></span>           | <span data-ttu-id="c5563-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5563-193">0x00000010</span></span>   |
| <span data-ttu-id="c5563-194">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c5563-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="c5563-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5563-195">Windows Server 2008</span></span>



| <span data-ttu-id="c5563-196">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-196">Entry</span></span> | <span data-ttu-id="c5563-197">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c5563-198">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c5563-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5563-200">System-Only</span></span>            | <span data-ttu-id="c5563-201">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-201">False</span></span>        |
| <span data-ttu-id="c5563-202">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c5563-202">Is-Single-Valued</span></span>       | <span data-ttu-id="c5563-203">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-203">False</span></span>        |
| <span data-ttu-id="c5563-204">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c5563-204">Is Indexed</span></span>             | <span data-ttu-id="c5563-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-205">False</span></span>        |
| <span data-ttu-id="c5563-206">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c5563-206">In Global Catalog</span></span>      | <span data-ttu-id="c5563-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-207">False</span></span>        |
| <span data-ttu-id="c5563-208">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c5563-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5563-209">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c5563-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c5563-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5563-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c5563-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5563-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c5563-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-212">Search-Flags</span></span>           | <span data-ttu-id="c5563-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5563-213">0x00000000</span></span>   |
| <span data-ttu-id="c5563-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-214">System-Flags</span></span>           | <span data-ttu-id="c5563-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5563-215">0x00000010</span></span>   |
| <span data-ttu-id="c5563-216">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c5563-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c5563-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5563-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c5563-218">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-218">Entry</span></span> | <span data-ttu-id="c5563-219">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c5563-220">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c5563-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5563-222">System-Only</span></span>            | <span data-ttu-id="c5563-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-223">False</span></span>        |
| <span data-ttu-id="c5563-224">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c5563-224">Is-Single-Valued</span></span>       | <span data-ttu-id="c5563-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-225">False</span></span>        |
| <span data-ttu-id="c5563-226">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c5563-226">Is Indexed</span></span>             | <span data-ttu-id="c5563-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-227">False</span></span>        |
| <span data-ttu-id="c5563-228">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c5563-228">In Global Catalog</span></span>      | <span data-ttu-id="c5563-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-229">False</span></span>        |
| <span data-ttu-id="c5563-230">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c5563-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5563-231">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c5563-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c5563-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5563-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c5563-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5563-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c5563-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-234">Search-Flags</span></span>           | <span data-ttu-id="c5563-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5563-235">0x00000000</span></span>   |
| <span data-ttu-id="c5563-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-236">System-Flags</span></span>           | <span data-ttu-id="c5563-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5563-237">0x00000010</span></span>   |
| <span data-ttu-id="c5563-238">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c5563-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="c5563-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5563-239">Windows Server 2012</span></span>



| <span data-ttu-id="c5563-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="c5563-240">Entry</span></span> | <span data-ttu-id="c5563-241">Значение</span><span class="sxs-lookup"><span data-stu-id="c5563-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c5563-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c5563-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5563-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c5563-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5563-244">System-Only</span></span>            | <span data-ttu-id="c5563-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-245">False</span></span>        |
| <span data-ttu-id="c5563-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c5563-246">Is-Single-Valued</span></span>       | <span data-ttu-id="c5563-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-247">False</span></span>        |
| <span data-ttu-id="c5563-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c5563-248">Is Indexed</span></span>             | <span data-ttu-id="c5563-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-249">False</span></span>        |
| <span data-ttu-id="c5563-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c5563-250">In Global Catalog</span></span>      | <span data-ttu-id="c5563-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="c5563-251">False</span></span>        |
| <span data-ttu-id="c5563-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c5563-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5563-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c5563-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c5563-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5563-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c5563-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5563-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c5563-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-256">Search-Flags</span></span>           | <span data-ttu-id="c5563-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5563-257">0x00000000</span></span>   |
| <span data-ttu-id="c5563-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5563-258">System-Flags</span></span>           | <span data-ttu-id="c5563-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5563-259">0x00000010</span></span>   |
| <span data-ttu-id="c5563-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c5563-260">Classes used in</span></span>        | \-           |



 

 




