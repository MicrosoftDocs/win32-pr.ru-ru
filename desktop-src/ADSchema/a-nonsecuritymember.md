---
title: Атрибут элемента, не относящегося к безопасности
description: Члены группы, не являющиеся безопасностью. Используется для списков рассылки Exchange.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов элементов, не связанных с безопасностью
- Схема AD атрибута Нонсекуритимембер
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989788"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="8fd89-106">Атрибут элемента, не относящегося к безопасности</span><span class="sxs-lookup"><span data-stu-id="8fd89-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="8fd89-107">Члены группы, не являющиеся безопасностью.</span><span class="sxs-lookup"><span data-stu-id="8fd89-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="8fd89-108">Используется для списков рассылки Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fd89-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="8fd89-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-109">Entry</span></span> | <span data-ttu-id="8fd89-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="8fd89-111">CN</span><span class="sxs-lookup"><span data-stu-id="8fd89-111">CN</span></span>                | <span data-ttu-id="8fd89-112">Не-Security-Member</span><span class="sxs-lookup"><span data-stu-id="8fd89-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="8fd89-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8fd89-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8fd89-114">нонсекуритимембер</span><span class="sxs-lookup"><span data-stu-id="8fd89-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="8fd89-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8fd89-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="8fd89-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8fd89-116">Update Privilege</span></span>  | <span data-ttu-id="8fd89-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="8fd89-117">Domain administrator</span></span>                             |
| <span data-ttu-id="8fd89-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8fd89-118">Update Frequency</span></span>  | <span data-ttu-id="8fd89-119">Каждый раз, когда пользователь добавляется или удаляется из списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="8fd89-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="8fd89-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-120">Attribute-Id</span></span>      | <span data-ttu-id="8fd89-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="8fd89-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="8fd89-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8fd89-122">System-Id-Guid</span></span>    | <span data-ttu-id="8fd89-123">52458018-ca6a-11D0-аффф-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8fd89-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="8fd89-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fd89-124">Syntax</span></span>            | [<span data-ttu-id="8fd89-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8fd89-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="8fd89-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8fd89-126">Implementations</span></span>

-   [<span data-ttu-id="8fd89-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8fd89-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8fd89-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8fd89-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8fd89-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8fd89-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8fd89-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8fd89-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8fd89-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8fd89-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8fd89-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8fd89-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8fd89-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8fd89-133">Windows 2000 Server</span></span>



| <span data-ttu-id="8fd89-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-134">Entry</span></span> | <span data-ttu-id="8fd89-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8fd89-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fd89-136">Link-Id</span></span>                | <span data-ttu-id="8fd89-137">50</span><span class="sxs-lookup"><span data-stu-id="8fd89-137">50</span></span>                                  |
| <span data-ttu-id="8fd89-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8fd89-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fd89-139">System-Only</span></span>            | <span data-ttu-id="8fd89-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-140">False</span></span>                               |
| <span data-ttu-id="8fd89-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fd89-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8fd89-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-142">False</span></span>                               |
| <span data-ttu-id="8fd89-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fd89-143">Is Indexed</span></span>             | <span data-ttu-id="8fd89-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-144">False</span></span>                               |
| <span data-ttu-id="8fd89-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fd89-145">In Global Catalog</span></span>      | <span data-ttu-id="8fd89-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-146">False</span></span>                               |
| <span data-ttu-id="8fd89-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fd89-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fd89-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fd89-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8fd89-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fd89-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fd89-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-151">Search-Flags</span></span>           | <span data-ttu-id="8fd89-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fd89-152">0x00000000</span></span>                          |
| <span data-ttu-id="8fd89-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-153">System-Flags</span></span>           | <span data-ttu-id="8fd89-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fd89-154">0x00000010</span></span>                          |
| <span data-ttu-id="8fd89-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fd89-155">Classes used in</span></span>        | [<span data-ttu-id="8fd89-156">**Группа**</span><span class="sxs-lookup"><span data-stu-id="8fd89-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8fd89-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8fd89-157">Windows Server 2003</span></span>



| <span data-ttu-id="8fd89-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-158">Entry</span></span> | <span data-ttu-id="8fd89-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8fd89-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fd89-160">Link-Id</span></span>                | <span data-ttu-id="8fd89-161">50</span><span class="sxs-lookup"><span data-stu-id="8fd89-161">50</span></span>                                  |
| <span data-ttu-id="8fd89-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8fd89-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fd89-163">System-Only</span></span>            | <span data-ttu-id="8fd89-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-164">False</span></span>                               |
| <span data-ttu-id="8fd89-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fd89-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8fd89-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-166">False</span></span>                               |
| <span data-ttu-id="8fd89-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fd89-167">Is Indexed</span></span>             | <span data-ttu-id="8fd89-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-168">False</span></span>                               |
| <span data-ttu-id="8fd89-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fd89-169">In Global Catalog</span></span>      | <span data-ttu-id="8fd89-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-170">False</span></span>                               |
| <span data-ttu-id="8fd89-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fd89-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fd89-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fd89-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8fd89-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fd89-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fd89-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-175">Search-Flags</span></span>           | <span data-ttu-id="8fd89-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fd89-176">0x00000000</span></span>                          |
| <span data-ttu-id="8fd89-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-177">System-Flags</span></span>           | <span data-ttu-id="8fd89-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fd89-178">0x00000010</span></span>                          |
| <span data-ttu-id="8fd89-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fd89-179">Classes used in</span></span>        | [<span data-ttu-id="8fd89-180">**Группа**</span><span class="sxs-lookup"><span data-stu-id="8fd89-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8fd89-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8fd89-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8fd89-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-182">Entry</span></span> | <span data-ttu-id="8fd89-183">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8fd89-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fd89-184">Link-Id</span></span>                | <span data-ttu-id="8fd89-185">50</span><span class="sxs-lookup"><span data-stu-id="8fd89-185">50</span></span>                                  |
| <span data-ttu-id="8fd89-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8fd89-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fd89-187">System-Only</span></span>            | <span data-ttu-id="8fd89-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-188">False</span></span>                               |
| <span data-ttu-id="8fd89-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fd89-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8fd89-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-190">False</span></span>                               |
| <span data-ttu-id="8fd89-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fd89-191">Is Indexed</span></span>             | <span data-ttu-id="8fd89-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-192">False</span></span>                               |
| <span data-ttu-id="8fd89-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fd89-193">In Global Catalog</span></span>      | <span data-ttu-id="8fd89-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-194">False</span></span>                               |
| <span data-ttu-id="8fd89-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fd89-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fd89-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fd89-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8fd89-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fd89-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fd89-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-199">Search-Flags</span></span>           | <span data-ttu-id="8fd89-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fd89-200">0x00000000</span></span>                          |
| <span data-ttu-id="8fd89-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-201">System-Flags</span></span>           | <span data-ttu-id="8fd89-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fd89-202">0x00000010</span></span>                          |
| <span data-ttu-id="8fd89-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fd89-203">Classes used in</span></span>        | [<span data-ttu-id="8fd89-204">**Группа**</span><span class="sxs-lookup"><span data-stu-id="8fd89-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8fd89-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fd89-205">Windows Server 2008</span></span>



| <span data-ttu-id="8fd89-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-206">Entry</span></span> | <span data-ttu-id="8fd89-207">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8fd89-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fd89-208">Link-Id</span></span>                | <span data-ttu-id="8fd89-209">50</span><span class="sxs-lookup"><span data-stu-id="8fd89-209">50</span></span>                                  |
| <span data-ttu-id="8fd89-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8fd89-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fd89-211">System-Only</span></span>            | <span data-ttu-id="8fd89-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-212">False</span></span>                               |
| <span data-ttu-id="8fd89-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fd89-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8fd89-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-214">False</span></span>                               |
| <span data-ttu-id="8fd89-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fd89-215">Is Indexed</span></span>             | <span data-ttu-id="8fd89-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-216">False</span></span>                               |
| <span data-ttu-id="8fd89-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fd89-217">In Global Catalog</span></span>      | <span data-ttu-id="8fd89-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-218">False</span></span>                               |
| <span data-ttu-id="8fd89-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fd89-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fd89-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fd89-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8fd89-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fd89-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fd89-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-223">Search-Flags</span></span>           | <span data-ttu-id="8fd89-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fd89-224">0x00000000</span></span>                          |
| <span data-ttu-id="8fd89-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-225">System-Flags</span></span>           | <span data-ttu-id="8fd89-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fd89-226">0x00000010</span></span>                          |
| <span data-ttu-id="8fd89-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fd89-227">Classes used in</span></span>        | [<span data-ttu-id="8fd89-228">**Группа**</span><span class="sxs-lookup"><span data-stu-id="8fd89-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8fd89-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fd89-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8fd89-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-230">Entry</span></span> | <span data-ttu-id="8fd89-231">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8fd89-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fd89-232">Link-Id</span></span>                | <span data-ttu-id="8fd89-233">50</span><span class="sxs-lookup"><span data-stu-id="8fd89-233">50</span></span>                                  |
| <span data-ttu-id="8fd89-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8fd89-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fd89-235">System-Only</span></span>            | <span data-ttu-id="8fd89-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-236">False</span></span>                               |
| <span data-ttu-id="8fd89-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fd89-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8fd89-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-238">False</span></span>                               |
| <span data-ttu-id="8fd89-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fd89-239">Is Indexed</span></span>             | <span data-ttu-id="8fd89-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-240">False</span></span>                               |
| <span data-ttu-id="8fd89-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fd89-241">In Global Catalog</span></span>      | <span data-ttu-id="8fd89-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-242">False</span></span>                               |
| <span data-ttu-id="8fd89-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fd89-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fd89-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fd89-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8fd89-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fd89-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fd89-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-247">Search-Flags</span></span>           | <span data-ttu-id="8fd89-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fd89-248">0x00000000</span></span>                          |
| <span data-ttu-id="8fd89-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-249">System-Flags</span></span>           | <span data-ttu-id="8fd89-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fd89-250">0x00000010</span></span>                          |
| <span data-ttu-id="8fd89-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fd89-251">Classes used in</span></span>        | [<span data-ttu-id="8fd89-252">**Группа**</span><span class="sxs-lookup"><span data-stu-id="8fd89-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8fd89-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fd89-253">Windows Server 2012</span></span>



| <span data-ttu-id="8fd89-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="8fd89-254">Entry</span></span> | <span data-ttu-id="8fd89-255">Значение</span><span class="sxs-lookup"><span data-stu-id="8fd89-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="8fd89-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8fd89-256">Link-Id</span></span>                | <span data-ttu-id="8fd89-257">50</span><span class="sxs-lookup"><span data-stu-id="8fd89-257">50</span></span>                                  |
| <span data-ttu-id="8fd89-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fd89-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="8fd89-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fd89-259">System-Only</span></span>            | <span data-ttu-id="8fd89-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-260">False</span></span>                               |
| <span data-ttu-id="8fd89-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8fd89-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8fd89-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-262">False</span></span>                               |
| <span data-ttu-id="8fd89-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8fd89-263">Is Indexed</span></span>             | <span data-ttu-id="8fd89-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-264">False</span></span>                               |
| <span data-ttu-id="8fd89-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8fd89-265">In Global Catalog</span></span>      | <span data-ttu-id="8fd89-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="8fd89-266">False</span></span>                               |
| <span data-ttu-id="8fd89-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8fd89-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fd89-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8fd89-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="8fd89-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fd89-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fd89-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="8fd89-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-271">Search-Flags</span></span>           | <span data-ttu-id="8fd89-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fd89-272">0x00000000</span></span>                          |
| <span data-ttu-id="8fd89-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fd89-273">System-Flags</span></span>           | <span data-ttu-id="8fd89-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fd89-274">0x00000010</span></span>                          |
| <span data-ttu-id="8fd89-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8fd89-275">Classes used in</span></span>        | [<span data-ttu-id="8fd89-276">**Группа**</span><span class="sxs-lookup"><span data-stu-id="8fd89-276">**Group**</span></span>](c-group.md)<br/> |



 

 





