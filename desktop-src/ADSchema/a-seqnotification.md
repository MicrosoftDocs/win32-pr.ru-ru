---
title: Атрибут Seq-Notification
description: Этот атрибут содержит счетчик, который увеличивается ежедневно. Это значение счетчика передается службе отслеживания ссылок, которая добавляет значение к его томам и связывает исходные файлы при их обновлении. Этот параметр поддерживается контроллером домена.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Seq-Notification
- Схема AD атрибута Секнотификатион
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138470"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="3cae9-107">Атрибут Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="3cae9-107">Seq-Notification attribute</span></span>

<span data-ttu-id="3cae9-108">Этот атрибут содержит счетчик, который увеличивается ежедневно.</span><span class="sxs-lookup"><span data-stu-id="3cae9-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="3cae9-109">Это значение счетчика передается службе отслеживания ссылок, которая добавляет значение к его томам и связывает исходные файлы при их обновлении.</span><span class="sxs-lookup"><span data-stu-id="3cae9-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="3cae9-110">Этот параметр поддерживается контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="3cae9-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="3cae9-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-111">Entry</span></span> | <span data-ttu-id="3cae9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3cae9-113">CN</span><span class="sxs-lookup"><span data-stu-id="3cae9-113">CN</span></span>                | <span data-ttu-id="3cae9-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="3cae9-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="3cae9-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3cae9-115">Ldap-Display-Name</span></span> | <span data-ttu-id="3cae9-116">секнотификатион</span><span class="sxs-lookup"><span data-stu-id="3cae9-116">seqNotification</span></span>                      |
| <span data-ttu-id="3cae9-117">Размер</span><span class="sxs-lookup"><span data-stu-id="3cae9-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="3cae9-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3cae9-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3cae9-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3cae9-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3cae9-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-120">Attribute-Id</span></span>      | <span data-ttu-id="3cae9-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="3cae9-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="3cae9-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3cae9-122">System-Id-Guid</span></span>    | <span data-ttu-id="3cae9-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="3cae9-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="3cae9-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cae9-124">Syntax</span></span>            | [<span data-ttu-id="3cae9-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="3cae9-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3cae9-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3cae9-126">Implementations</span></span>

-   [<span data-ttu-id="3cae9-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3cae9-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3cae9-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3cae9-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3cae9-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3cae9-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3cae9-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3cae9-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3cae9-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3cae9-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3cae9-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3cae9-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3cae9-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3cae9-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3cae9-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-134">Entry</span></span> | <span data-ttu-id="3cae9-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3cae9-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3cae9-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cae9-138">System-Only</span></span>            | <span data-ttu-id="3cae9-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-139">False</span></span>                                                          |
| <span data-ttu-id="3cae9-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3cae9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3cae9-141">True</span><span class="sxs-lookup"><span data-stu-id="3cae9-141">True</span></span>                                                           |
| <span data-ttu-id="3cae9-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3cae9-142">Is Indexed</span></span>             | <span data-ttu-id="3cae9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-143">False</span></span>                                                          |
| <span data-ttu-id="3cae9-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3cae9-144">In Global Catalog</span></span>      | <span data-ttu-id="3cae9-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-145">False</span></span>                                                          |
| <span data-ttu-id="3cae9-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3cae9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cae9-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3cae9-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="3cae9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cae9-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cae9-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-150">Search-Flags</span></span>           | <span data-ttu-id="3cae9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cae9-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="3cae9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-152">System-Flags</span></span>           | <span data-ttu-id="3cae9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cae9-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="3cae9-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3cae9-154">Classes used in</span></span>        | [<span data-ttu-id="3cae9-155">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="3cae9-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3cae9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3cae9-156">Windows Server 2003</span></span>



| <span data-ttu-id="3cae9-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-157">Entry</span></span> | <span data-ttu-id="3cae9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3cae9-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3cae9-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cae9-161">System-Only</span></span>            | <span data-ttu-id="3cae9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-162">False</span></span>                                                          |
| <span data-ttu-id="3cae9-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3cae9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3cae9-164">True</span><span class="sxs-lookup"><span data-stu-id="3cae9-164">True</span></span>                                                           |
| <span data-ttu-id="3cae9-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3cae9-165">Is Indexed</span></span>             | <span data-ttu-id="3cae9-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-166">False</span></span>                                                          |
| <span data-ttu-id="3cae9-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3cae9-167">In Global Catalog</span></span>      | <span data-ttu-id="3cae9-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-168">False</span></span>                                                          |
| <span data-ttu-id="3cae9-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3cae9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cae9-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3cae9-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="3cae9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cae9-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cae9-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-173">Search-Flags</span></span>           | <span data-ttu-id="3cae9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cae9-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="3cae9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-175">System-Flags</span></span>           | <span data-ttu-id="3cae9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cae9-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="3cae9-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3cae9-177">Classes used in</span></span>        | [<span data-ttu-id="3cae9-178">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="3cae9-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3cae9-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3cae9-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3cae9-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-180">Entry</span></span> | <span data-ttu-id="3cae9-181">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3cae9-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3cae9-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cae9-184">System-Only</span></span>            | <span data-ttu-id="3cae9-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-185">False</span></span>                                                          |
| <span data-ttu-id="3cae9-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3cae9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3cae9-187">True</span><span class="sxs-lookup"><span data-stu-id="3cae9-187">True</span></span>                                                           |
| <span data-ttu-id="3cae9-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3cae9-188">Is Indexed</span></span>             | <span data-ttu-id="3cae9-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-189">False</span></span>                                                          |
| <span data-ttu-id="3cae9-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3cae9-190">In Global Catalog</span></span>      | <span data-ttu-id="3cae9-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-191">False</span></span>                                                          |
| <span data-ttu-id="3cae9-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3cae9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cae9-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3cae9-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="3cae9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cae9-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cae9-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-196">Search-Flags</span></span>           | <span data-ttu-id="3cae9-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cae9-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="3cae9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-198">System-Flags</span></span>           | <span data-ttu-id="3cae9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cae9-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="3cae9-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3cae9-200">Classes used in</span></span>        | [<span data-ttu-id="3cae9-201">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="3cae9-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3cae9-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cae9-202">Windows Server 2008</span></span>



| <span data-ttu-id="3cae9-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-203">Entry</span></span> | <span data-ttu-id="3cae9-204">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3cae9-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3cae9-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cae9-207">System-Only</span></span>            | <span data-ttu-id="3cae9-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-208">False</span></span>                                                          |
| <span data-ttu-id="3cae9-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3cae9-209">Is-Single-Valued</span></span>       | <span data-ttu-id="3cae9-210">True</span><span class="sxs-lookup"><span data-stu-id="3cae9-210">True</span></span>                                                           |
| <span data-ttu-id="3cae9-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3cae9-211">Is Indexed</span></span>             | <span data-ttu-id="3cae9-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-212">False</span></span>                                                          |
| <span data-ttu-id="3cae9-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3cae9-213">In Global Catalog</span></span>      | <span data-ttu-id="3cae9-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-214">False</span></span>                                                          |
| <span data-ttu-id="3cae9-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3cae9-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cae9-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3cae9-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="3cae9-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cae9-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cae9-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-219">Search-Flags</span></span>           | <span data-ttu-id="3cae9-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cae9-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="3cae9-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-221">System-Flags</span></span>           | <span data-ttu-id="3cae9-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cae9-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="3cae9-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3cae9-223">Classes used in</span></span>        | [<span data-ttu-id="3cae9-224">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="3cae9-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3cae9-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3cae9-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3cae9-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-226">Entry</span></span> | <span data-ttu-id="3cae9-227">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3cae9-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3cae9-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cae9-230">System-Only</span></span>            | <span data-ttu-id="3cae9-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-231">False</span></span>                                                          |
| <span data-ttu-id="3cae9-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3cae9-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3cae9-233">True</span><span class="sxs-lookup"><span data-stu-id="3cae9-233">True</span></span>                                                           |
| <span data-ttu-id="3cae9-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3cae9-234">Is Indexed</span></span>             | <span data-ttu-id="3cae9-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-235">False</span></span>                                                          |
| <span data-ttu-id="3cae9-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3cae9-236">In Global Catalog</span></span>      | <span data-ttu-id="3cae9-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-237">False</span></span>                                                          |
| <span data-ttu-id="3cae9-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3cae9-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cae9-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3cae9-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="3cae9-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cae9-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cae9-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-242">Search-Flags</span></span>           | <span data-ttu-id="3cae9-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cae9-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="3cae9-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-244">System-Flags</span></span>           | <span data-ttu-id="3cae9-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cae9-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="3cae9-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3cae9-246">Classes used in</span></span>        | [<span data-ttu-id="3cae9-247">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="3cae9-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3cae9-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3cae9-248">Windows Server 2012</span></span>



| <span data-ttu-id="3cae9-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="3cae9-249">Entry</span></span> | <span data-ttu-id="3cae9-250">Значение</span><span class="sxs-lookup"><span data-stu-id="3cae9-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3cae9-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3cae9-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cae9-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="3cae9-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cae9-253">System-Only</span></span>            | <span data-ttu-id="3cae9-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-254">False</span></span>                                                          |
| <span data-ttu-id="3cae9-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3cae9-255">Is-Single-Valued</span></span>       | <span data-ttu-id="3cae9-256">True</span><span class="sxs-lookup"><span data-stu-id="3cae9-256">True</span></span>                                                           |
| <span data-ttu-id="3cae9-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3cae9-257">Is Indexed</span></span>             | <span data-ttu-id="3cae9-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-258">False</span></span>                                                          |
| <span data-ttu-id="3cae9-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3cae9-259">In Global Catalog</span></span>      | <span data-ttu-id="3cae9-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="3cae9-260">False</span></span>                                                          |
| <span data-ttu-id="3cae9-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3cae9-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cae9-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3cae9-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="3cae9-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cae9-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cae9-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="3cae9-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-265">Search-Flags</span></span>           | <span data-ttu-id="3cae9-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cae9-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="3cae9-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cae9-267">System-Flags</span></span>           | <span data-ttu-id="3cae9-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cae9-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="3cae9-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3cae9-269">Classes used in</span></span>        | [<span data-ttu-id="3cae9-270">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="3cae9-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





