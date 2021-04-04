---
title: Атрибут FRS-worked Path
description: Путь к базе данных репликации файлов.
ms.assetid: 43db1214-17a3-4458-b082-1cf69d06384c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active Path для службы FRS
- Схема AD атрибута Фрсворкингпас
topic_type:
- apiref
api_name:
- FRS-Working-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e86603b9e0c63645d7253e017619c53d763d138
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138158"
---
# <a name="frs-working-path-attribute"></a><span data-ttu-id="e6ff6-105">Атрибут FRS-worked Path</span><span class="sxs-lookup"><span data-stu-id="e6ff6-105">FRS-Working-Path attribute</span></span>

<span data-ttu-id="e6ff6-106">Путь к базе данных репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="e6ff6-106">The path to the file replication database.</span></span>



| <span data-ttu-id="e6ff6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-107">Entry</span></span> | <span data-ttu-id="e6ff6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e6ff6-109">CN</span><span class="sxs-lookup"><span data-stu-id="e6ff6-109">CN</span></span>                | <span data-ttu-id="e6ff6-110">FRS-Working-Path</span><span class="sxs-lookup"><span data-stu-id="e6ff6-110">FRS-Working-Path</span></span>                            |
| <span data-ttu-id="e6ff6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e6ff6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e6ff6-112">фрсворкингпас</span><span class="sxs-lookup"><span data-stu-id="e6ff6-112">fRSWorkingPath</span></span>                              |
| <span data-ttu-id="e6ff6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e6ff6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e6ff6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e6ff6-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e6ff6-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e6ff6-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e6ff6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-116">Attribute-Id</span></span>      | <span data-ttu-id="e6ff6-117">1.2.840.113556.1.4.486</span><span class="sxs-lookup"><span data-stu-id="e6ff6-117">1.2.840.113556.1.4.486</span></span>                      |
| <span data-ttu-id="e6ff6-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e6ff6-118">System-Id-Guid</span></span>    | <span data-ttu-id="e6ff6-119">1be8f173-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="e6ff6-119">1be8f173-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="e6ff6-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6ff6-120">Syntax</span></span>            | [<span data-ttu-id="e6ff6-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e6ff6-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e6ff6-122">Implementations</span></span>

-   [<span data-ttu-id="e6ff6-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e6ff6-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e6ff6-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e6ff6-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6ff6-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6ff6-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e6ff6-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6ff6-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e6ff6-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-130">Entry</span></span> | <span data-ttu-id="e6ff6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6ff6-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff6-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff6-134">System-Only</span></span>            | <span data-ttu-id="e6ff6-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-135">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff6-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff6-137">True</span><span class="sxs-lookup"><span data-stu-id="e6ff6-137">True</span></span>                                                           |
| <span data-ttu-id="e6ff6-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff6-138">Is Indexed</span></span>             | <span data-ttu-id="e6ff6-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-139">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff6-140">In Global Catalog</span></span>      | <span data-ttu-id="e6ff6-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-141">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff6-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff6-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff6-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e6ff6-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff6-144">Range-Lower</span></span>            | <span data-ttu-id="e6ff6-145">0</span><span class="sxs-lookup"><span data-stu-id="e6ff6-145">0</span></span>                                                              |
| <span data-ttu-id="e6ff6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff6-146">Range-Upper</span></span>            | <span data-ttu-id="e6ff6-147">2048</span><span class="sxs-lookup"><span data-stu-id="e6ff6-147">2048</span></span>                                                           |
| <span data-ttu-id="e6ff6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-148">Search-Flags</span></span>           | <span data-ttu-id="e6ff6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff6-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="e6ff6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-150">System-Flags</span></span>           | <span data-ttu-id="e6ff6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff6-151">0x00000010</span></span>                                                     |
| <span data-ttu-id="e6ff6-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff6-152">Classes used in</span></span>        | [<span data-ttu-id="e6ff6-153">**NTFRS-Subscriptions**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-153">**NTFRS-Subscriptions**</span></span>](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e6ff6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6ff6-154">Windows Server 2003</span></span>



| <span data-ttu-id="e6ff6-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-155">Entry</span></span> | <span data-ttu-id="e6ff6-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-156">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6ff6-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff6-157">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-158">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff6-159">System-Only</span></span>            | <span data-ttu-id="e6ff6-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-160">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff6-162">True</span><span class="sxs-lookup"><span data-stu-id="e6ff6-162">True</span></span>                                                           |
| <span data-ttu-id="e6ff6-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff6-163">Is Indexed</span></span>             | <span data-ttu-id="e6ff6-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-164">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff6-165">In Global Catalog</span></span>      | <span data-ttu-id="e6ff6-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-166">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff6-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff6-168">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e6ff6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff6-169">Range-Lower</span></span>            | <span data-ttu-id="e6ff6-170">0</span><span class="sxs-lookup"><span data-stu-id="e6ff6-170">0</span></span>                                                              |
| <span data-ttu-id="e6ff6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff6-171">Range-Upper</span></span>            | <span data-ttu-id="e6ff6-172">2048</span><span class="sxs-lookup"><span data-stu-id="e6ff6-172">2048</span></span>                                                           |
| <span data-ttu-id="e6ff6-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-173">Search-Flags</span></span>           | <span data-ttu-id="e6ff6-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff6-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="e6ff6-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-175">System-Flags</span></span>           | <span data-ttu-id="e6ff6-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff6-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="e6ff6-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff6-177">Classes used in</span></span>        | [<span data-ttu-id="e6ff6-178">**NTFRS-Subscriptions**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-178">**NTFRS-Subscriptions**</span></span>](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e6ff6-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e6ff6-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e6ff6-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-180">Entry</span></span> | <span data-ttu-id="e6ff6-181">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6ff6-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff6-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff6-184">System-Only</span></span>            | <span data-ttu-id="e6ff6-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-185">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff6-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff6-187">True</span><span class="sxs-lookup"><span data-stu-id="e6ff6-187">True</span></span>                                                           |
| <span data-ttu-id="e6ff6-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff6-188">Is Indexed</span></span>             | <span data-ttu-id="e6ff6-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-189">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff6-190">In Global Catalog</span></span>      | <span data-ttu-id="e6ff6-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-191">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff6-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff6-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff6-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e6ff6-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff6-194">Range-Lower</span></span>            | <span data-ttu-id="e6ff6-195">0</span><span class="sxs-lookup"><span data-stu-id="e6ff6-195">0</span></span>                                                              |
| <span data-ttu-id="e6ff6-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff6-196">Range-Upper</span></span>            | <span data-ttu-id="e6ff6-197">2048</span><span class="sxs-lookup"><span data-stu-id="e6ff6-197">2048</span></span>                                                           |
| <span data-ttu-id="e6ff6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-198">Search-Flags</span></span>           | <span data-ttu-id="e6ff6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff6-199">0x00000000</span></span>                                                     |
| <span data-ttu-id="e6ff6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-200">System-Flags</span></span>           | <span data-ttu-id="e6ff6-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff6-201">0x00000010</span></span>                                                     |
| <span data-ttu-id="e6ff6-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff6-202">Classes used in</span></span>        | [<span data-ttu-id="e6ff6-203">**NTFRS-Subscriptions**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-203">**NTFRS-Subscriptions**</span></span>](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e6ff6-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ff6-204">Windows Server 2008</span></span>



| <span data-ttu-id="e6ff6-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-205">Entry</span></span> | <span data-ttu-id="e6ff6-206">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-206">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6ff6-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff6-207">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-208">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff6-209">System-Only</span></span>            | <span data-ttu-id="e6ff6-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-210">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff6-212">True</span><span class="sxs-lookup"><span data-stu-id="e6ff6-212">True</span></span>                                                           |
| <span data-ttu-id="e6ff6-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff6-213">Is Indexed</span></span>             | <span data-ttu-id="e6ff6-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-214">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff6-215">In Global Catalog</span></span>      | <span data-ttu-id="e6ff6-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-216">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff6-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff6-218">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e6ff6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff6-219">Range-Lower</span></span>            | <span data-ttu-id="e6ff6-220">0</span><span class="sxs-lookup"><span data-stu-id="e6ff6-220">0</span></span>                                                              |
| <span data-ttu-id="e6ff6-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff6-221">Range-Upper</span></span>            | <span data-ttu-id="e6ff6-222">2048</span><span class="sxs-lookup"><span data-stu-id="e6ff6-222">2048</span></span>                                                           |
| <span data-ttu-id="e6ff6-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-223">Search-Flags</span></span>           | <span data-ttu-id="e6ff6-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff6-224">0x00000000</span></span>                                                     |
| <span data-ttu-id="e6ff6-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-225">System-Flags</span></span>           | <span data-ttu-id="e6ff6-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff6-226">0x00000010</span></span>                                                     |
| <span data-ttu-id="e6ff6-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff6-227">Classes used in</span></span>        | [<span data-ttu-id="e6ff6-228">**NTFRS-Subscriptions**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-228">**NTFRS-Subscriptions**</span></span>](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6ff6-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6ff6-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6ff6-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-230">Entry</span></span> | <span data-ttu-id="e6ff6-231">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-231">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6ff6-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff6-232">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-233">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff6-234">System-Only</span></span>            | <span data-ttu-id="e6ff6-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-235">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff6-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff6-237">True</span><span class="sxs-lookup"><span data-stu-id="e6ff6-237">True</span></span>                                                           |
| <span data-ttu-id="e6ff6-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff6-238">Is Indexed</span></span>             | <span data-ttu-id="e6ff6-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-239">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff6-240">In Global Catalog</span></span>      | <span data-ttu-id="e6ff6-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-241">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff6-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff6-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff6-243">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e6ff6-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff6-244">Range-Lower</span></span>            | <span data-ttu-id="e6ff6-245">0</span><span class="sxs-lookup"><span data-stu-id="e6ff6-245">0</span></span>                                                              |
| <span data-ttu-id="e6ff6-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff6-246">Range-Upper</span></span>            | <span data-ttu-id="e6ff6-247">2048</span><span class="sxs-lookup"><span data-stu-id="e6ff6-247">2048</span></span>                                                           |
| <span data-ttu-id="e6ff6-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-248">Search-Flags</span></span>           | <span data-ttu-id="e6ff6-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff6-249">0x00000000</span></span>                                                     |
| <span data-ttu-id="e6ff6-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-250">System-Flags</span></span>           | <span data-ttu-id="e6ff6-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff6-251">0x00000010</span></span>                                                     |
| <span data-ttu-id="e6ff6-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff6-252">Classes used in</span></span>        | [<span data-ttu-id="e6ff6-253">**NTFRS-Subscriptions**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-253">**NTFRS-Subscriptions**</span></span>](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6ff6-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6ff6-254">Windows Server 2012</span></span>



| <span data-ttu-id="e6ff6-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6ff6-255">Entry</span></span> | <span data-ttu-id="e6ff6-256">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ff6-256">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6ff6-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6ff6-257">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ff6-258">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e6ff6-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ff6-259">System-Only</span></span>            | <span data-ttu-id="e6ff6-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-260">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6ff6-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ff6-262">True</span><span class="sxs-lookup"><span data-stu-id="e6ff6-262">True</span></span>                                                           |
| <span data-ttu-id="e6ff6-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6ff6-263">Is Indexed</span></span>             | <span data-ttu-id="e6ff6-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-264">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6ff6-265">In Global Catalog</span></span>      | <span data-ttu-id="e6ff6-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6ff6-266">False</span></span>                                                          |
| <span data-ttu-id="e6ff6-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6ff6-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ff6-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6ff6-268">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e6ff6-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ff6-269">Range-Lower</span></span>            | <span data-ttu-id="e6ff6-270">0</span><span class="sxs-lookup"><span data-stu-id="e6ff6-270">0</span></span>                                                              |
| <span data-ttu-id="e6ff6-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ff6-271">Range-Upper</span></span>            | <span data-ttu-id="e6ff6-272">2048</span><span class="sxs-lookup"><span data-stu-id="e6ff6-272">2048</span></span>                                                           |
| <span data-ttu-id="e6ff6-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-273">Search-Flags</span></span>           | <span data-ttu-id="e6ff6-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ff6-274">0x00000000</span></span>                                                     |
| <span data-ttu-id="e6ff6-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ff6-275">System-Flags</span></span>           | <span data-ttu-id="e6ff6-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ff6-276">0x00000010</span></span>                                                     |
| <span data-ttu-id="e6ff6-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6ff6-277">Classes used in</span></span>        | [<span data-ttu-id="e6ff6-278">**NTFRS-Subscriptions**</span><span class="sxs-lookup"><span data-stu-id="e6ff6-278">**NTFRS-Subscriptions**</span></span>](c-ntfrssubscriptions.md)<br/> |



 

 





