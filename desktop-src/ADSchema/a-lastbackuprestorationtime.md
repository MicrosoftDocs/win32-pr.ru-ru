---
title: Последний-резервный — атрибут времени восстановления
description: Когда произошло последнее восстановление системы.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "Последняя архивация-время восстановления"
- Схема AD атрибута Ластбаккупресторатионтиме
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072052"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="0af5d-105">Последний-резервный — атрибут времени восстановления</span><span class="sxs-lookup"><span data-stu-id="0af5d-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="0af5d-106">Когда произошло последнее восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="0af5d-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="0af5d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-107">Entry</span></span> | <span data-ttu-id="0af5d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0af5d-109">CN</span><span class="sxs-lookup"><span data-stu-id="0af5d-109">CN</span></span>                | <span data-ttu-id="0af5d-110">Последнее резервное копирование — время восстановления</span><span class="sxs-lookup"><span data-stu-id="0af5d-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="0af5d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0af5d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0af5d-112">ластбаккупресторатионтиме</span><span class="sxs-lookup"><span data-stu-id="0af5d-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="0af5d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="0af5d-113">Size</span></span>              | <span data-ttu-id="0af5d-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="0af5d-114">8 bytes</span></span>                              |
| <span data-ttu-id="0af5d-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0af5d-115">Update Privilege</span></span>  | <span data-ttu-id="0af5d-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="0af5d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="0af5d-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0af5d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0af5d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-118">Attribute-Id</span></span>      | <span data-ttu-id="0af5d-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="0af5d-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="0af5d-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0af5d-120">System-Id-Guid</span></span>    | <span data-ttu-id="0af5d-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0af5d-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="0af5d-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0af5d-122">Syntax</span></span>            | [<span data-ttu-id="0af5d-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="0af5d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0af5d-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0af5d-124">Implementations</span></span>

-   [<span data-ttu-id="0af5d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0af5d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0af5d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0af5d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0af5d-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0af5d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0af5d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0af5d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0af5d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0af5d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0af5d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0af5d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0af5d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0af5d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0af5d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0af5d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0af5d-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-133">Entry</span></span> | <span data-ttu-id="0af5d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-137">System-Only</span></span>            | <span data-ttu-id="0af5d-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-138">False</span></span>                                    |
| <span data-ttu-id="0af5d-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-140">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-140">True</span></span>                                     |
| <span data-ttu-id="0af5d-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-141">Is Indexed</span></span>             | <span data-ttu-id="0af5d-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-142">False</span></span>                                    |
| <span data-ttu-id="0af5d-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-143">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-144">False</span></span>                                    |
| <span data-ttu-id="0af5d-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-149">Search-Flags</span></span>           | <span data-ttu-id="0af5d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-150">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-151">System-Flags</span></span>           | <span data-ttu-id="0af5d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-152">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-153">Classes used in</span></span>        | [<span data-ttu-id="0af5d-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0af5d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0af5d-155">Windows Server 2003</span></span>



| <span data-ttu-id="0af5d-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-156">Entry</span></span> | <span data-ttu-id="0af5d-157">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-160">System-Only</span></span>            | <span data-ttu-id="0af5d-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-161">False</span></span>                                    |
| <span data-ttu-id="0af5d-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-163">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-163">True</span></span>                                     |
| <span data-ttu-id="0af5d-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-164">Is Indexed</span></span>             | <span data-ttu-id="0af5d-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-165">False</span></span>                                    |
| <span data-ttu-id="0af5d-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-166">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-167">False</span></span>                                    |
| <span data-ttu-id="0af5d-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-172">Search-Flags</span></span>           | <span data-ttu-id="0af5d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-173">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-174">System-Flags</span></span>           | <span data-ttu-id="0af5d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-175">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-176">Classes used in</span></span>        | [<span data-ttu-id="0af5d-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0af5d-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="0af5d-178">ADAM</span></span>



| <span data-ttu-id="0af5d-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-179">Entry</span></span> | <span data-ttu-id="0af5d-180">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-183">System-Only</span></span>            | <span data-ttu-id="0af5d-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-184">False</span></span>                                    |
| <span data-ttu-id="0af5d-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-186">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-186">True</span></span>                                     |
| <span data-ttu-id="0af5d-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-187">Is Indexed</span></span>             | <span data-ttu-id="0af5d-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-188">False</span></span>                                    |
| <span data-ttu-id="0af5d-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-189">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-190">False</span></span>                                    |
| <span data-ttu-id="0af5d-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-195">Search-Flags</span></span>           | <span data-ttu-id="0af5d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-196">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-197">System-Flags</span></span>           | <span data-ttu-id="0af5d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-198">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-199">Classes used in</span></span>        | [<span data-ttu-id="0af5d-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0af5d-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0af5d-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0af5d-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-202">Entry</span></span> | <span data-ttu-id="0af5d-203">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-206">System-Only</span></span>            | <span data-ttu-id="0af5d-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-207">False</span></span>                                    |
| <span data-ttu-id="0af5d-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-209">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-209">True</span></span>                                     |
| <span data-ttu-id="0af5d-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-210">Is Indexed</span></span>             | <span data-ttu-id="0af5d-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-211">False</span></span>                                    |
| <span data-ttu-id="0af5d-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-212">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-213">False</span></span>                                    |
| <span data-ttu-id="0af5d-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-218">Search-Flags</span></span>           | <span data-ttu-id="0af5d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-219">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-220">System-Flags</span></span>           | <span data-ttu-id="0af5d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-221">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-222">Classes used in</span></span>        | [<span data-ttu-id="0af5d-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0af5d-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0af5d-224">Windows Server 2008</span></span>



| <span data-ttu-id="0af5d-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-225">Entry</span></span> | <span data-ttu-id="0af5d-226">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-229">System-Only</span></span>            | <span data-ttu-id="0af5d-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-230">False</span></span>                                    |
| <span data-ttu-id="0af5d-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-232">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-232">True</span></span>                                     |
| <span data-ttu-id="0af5d-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-233">Is Indexed</span></span>             | <span data-ttu-id="0af5d-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-234">False</span></span>                                    |
| <span data-ttu-id="0af5d-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-235">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-236">False</span></span>                                    |
| <span data-ttu-id="0af5d-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-241">Search-Flags</span></span>           | <span data-ttu-id="0af5d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-242">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-243">System-Flags</span></span>           | <span data-ttu-id="0af5d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-244">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-245">Classes used in</span></span>        | [<span data-ttu-id="0af5d-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0af5d-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0af5d-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0af5d-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-248">Entry</span></span> | <span data-ttu-id="0af5d-249">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-252">System-Only</span></span>            | <span data-ttu-id="0af5d-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-253">False</span></span>                                    |
| <span data-ttu-id="0af5d-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-255">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-255">True</span></span>                                     |
| <span data-ttu-id="0af5d-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-256">Is Indexed</span></span>             | <span data-ttu-id="0af5d-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-257">False</span></span>                                    |
| <span data-ttu-id="0af5d-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-258">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-259">False</span></span>                                    |
| <span data-ttu-id="0af5d-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-264">Search-Flags</span></span>           | <span data-ttu-id="0af5d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-265">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-266">System-Flags</span></span>           | <span data-ttu-id="0af5d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-267">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-268">Classes used in</span></span>        | [<span data-ttu-id="0af5d-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0af5d-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0af5d-270">Windows Server 2012</span></span>



| <span data-ttu-id="0af5d-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="0af5d-271">Entry</span></span> | <span data-ttu-id="0af5d-272">Значение</span><span class="sxs-lookup"><span data-stu-id="0af5d-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0af5d-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0af5d-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af5d-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0af5d-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af5d-275">System-Only</span></span>            | <span data-ttu-id="0af5d-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-276">False</span></span>                                    |
| <span data-ttu-id="0af5d-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0af5d-277">Is-Single-Valued</span></span>       | <span data-ttu-id="0af5d-278">True</span><span class="sxs-lookup"><span data-stu-id="0af5d-278">True</span></span>                                     |
| <span data-ttu-id="0af5d-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0af5d-279">Is Indexed</span></span>             | <span data-ttu-id="0af5d-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-280">False</span></span>                                    |
| <span data-ttu-id="0af5d-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0af5d-281">In Global Catalog</span></span>      | <span data-ttu-id="0af5d-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="0af5d-282">False</span></span>                                    |
| <span data-ttu-id="0af5d-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0af5d-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af5d-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0af5d-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0af5d-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af5d-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af5d-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0af5d-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-287">Search-Flags</span></span>           | <span data-ttu-id="0af5d-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af5d-288">0x00000000</span></span>                               |
| <span data-ttu-id="0af5d-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af5d-289">System-Flags</span></span>           | <span data-ttu-id="0af5d-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af5d-290">0x00000010</span></span>                               |
| <span data-ttu-id="0af5d-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0af5d-291">Classes used in</span></span>        | [<span data-ttu-id="0af5d-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0af5d-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





