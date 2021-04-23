---
title: Group-Membership-SAM, атрибут
description: Безопасность Windows NT. Поддержка Windows NT нижнего уровня.
ms.assetid: 14e2f7c1-4d2b-4c0d-bf13-9abb576cd931
ms.tgt_platform: multiple
keywords:
- Group-Membership-SAM, схема AD
- Схема AD атрибута Граупмембершипсам
topic_type:
- apiref
api_name:
- Group-Membership-SAM
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fe8a9ff92077d22a628c9a85b942382cbb2034
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138726"
---
# <a name="group-membership-sam-attribute"></a><span data-ttu-id="27114-106">Group-Membership-SAM, атрибут</span><span class="sxs-lookup"><span data-stu-id="27114-106">Group-Membership-SAM attribute</span></span>

<span data-ttu-id="27114-107">Безопасность Windows NT.</span><span class="sxs-lookup"><span data-stu-id="27114-107">Windows NT Security.</span></span> <span data-ttu-id="27114-108">Поддержка Windows NT нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="27114-108">Down level Windows NT support.</span></span>



| <span data-ttu-id="27114-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-109">Entry</span></span> | <span data-ttu-id="27114-110">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="27114-111">CN</span><span class="sxs-lookup"><span data-stu-id="27114-111">CN</span></span>                | <span data-ttu-id="27114-112">Group-Membership-SAM</span><span class="sxs-lookup"><span data-stu-id="27114-112">Group-Membership-SAM</span></span>                                  |
| <span data-ttu-id="27114-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="27114-113">Ldap-Display-Name</span></span> | <span data-ttu-id="27114-114">граупмембершипсам</span><span class="sxs-lookup"><span data-stu-id="27114-114">groupMembershipSAM</span></span>                                    |
| <span data-ttu-id="27114-115">Размер</span><span class="sxs-lookup"><span data-stu-id="27114-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="27114-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="27114-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="27114-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="27114-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="27114-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27114-118">Attribute-Id</span></span>      | <span data-ttu-id="27114-119">1.2.840.113556.1.4.166</span><span class="sxs-lookup"><span data-stu-id="27114-119">1.2.840.113556.1.4.166</span></span>                                |
| <span data-ttu-id="27114-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="27114-120">System-Id-Guid</span></span>    | <span data-ttu-id="27114-121">bf967980-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="27114-121">bf967980-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="27114-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27114-122">Syntax</span></span>            | [<span data-ttu-id="27114-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="27114-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="27114-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="27114-124">Implementations</span></span>

-   [<span data-ttu-id="27114-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27114-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27114-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27114-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27114-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27114-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27114-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27114-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27114-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27114-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27114-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27114-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27114-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27114-131">Windows 2000 Server</span></span>



| <span data-ttu-id="27114-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-132">Entry</span></span> | <span data-ttu-id="27114-133">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="27114-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27114-134">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27114-135">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="27114-136">System-Only</span></span>            | <span data-ttu-id="27114-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-137">False</span></span>                                                                 |
| <span data-ttu-id="27114-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27114-138">Is-Single-Valued</span></span>       | <span data-ttu-id="27114-139">True</span><span class="sxs-lookup"><span data-stu-id="27114-139">True</span></span>                                                                  |
| <span data-ttu-id="27114-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27114-140">Is Indexed</span></span>             | <span data-ttu-id="27114-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-141">False</span></span>                                                                 |
| <span data-ttu-id="27114-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27114-142">In Global Catalog</span></span>      | <span data-ttu-id="27114-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-143">False</span></span>                                                                 |
| <span data-ttu-id="27114-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27114-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="27114-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27114-145">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="27114-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27114-146">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27114-147">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-148">Search-Flags</span></span>           | <span data-ttu-id="27114-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27114-149">0x00000000</span></span>                                                            |
| <span data-ttu-id="27114-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-150">System-Flags</span></span>           | <span data-ttu-id="27114-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27114-151">0x00000010</span></span>                                                            |
| <span data-ttu-id="27114-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27114-152">Classes used in</span></span>        | [<span data-ttu-id="27114-153">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="27114-153">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="27114-154">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="27114-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27114-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27114-155">Windows Server 2003</span></span>



| <span data-ttu-id="27114-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-156">Entry</span></span> | <span data-ttu-id="27114-157">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="27114-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27114-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27114-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="27114-160">System-Only</span></span>            | <span data-ttu-id="27114-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-161">False</span></span>                                                                 |
| <span data-ttu-id="27114-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27114-162">Is-Single-Valued</span></span>       | <span data-ttu-id="27114-163">True</span><span class="sxs-lookup"><span data-stu-id="27114-163">True</span></span>                                                                  |
| <span data-ttu-id="27114-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27114-164">Is Indexed</span></span>             | <span data-ttu-id="27114-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-165">False</span></span>                                                                 |
| <span data-ttu-id="27114-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27114-166">In Global Catalog</span></span>      | <span data-ttu-id="27114-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-167">False</span></span>                                                                 |
| <span data-ttu-id="27114-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27114-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="27114-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27114-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="27114-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27114-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27114-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-172">Search-Flags</span></span>           | <span data-ttu-id="27114-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27114-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="27114-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-174">System-Flags</span></span>           | <span data-ttu-id="27114-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27114-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="27114-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27114-176">Classes used in</span></span>        | [<span data-ttu-id="27114-177">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="27114-177">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="27114-178">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="27114-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27114-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27114-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27114-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-180">Entry</span></span> | <span data-ttu-id="27114-181">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="27114-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27114-182">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27114-183">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="27114-184">System-Only</span></span>            | <span data-ttu-id="27114-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-185">False</span></span>                                                                 |
| <span data-ttu-id="27114-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27114-186">Is-Single-Valued</span></span>       | <span data-ttu-id="27114-187">True</span><span class="sxs-lookup"><span data-stu-id="27114-187">True</span></span>                                                                  |
| <span data-ttu-id="27114-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27114-188">Is Indexed</span></span>             | <span data-ttu-id="27114-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-189">False</span></span>                                                                 |
| <span data-ttu-id="27114-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27114-190">In Global Catalog</span></span>      | <span data-ttu-id="27114-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-191">False</span></span>                                                                 |
| <span data-ttu-id="27114-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27114-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="27114-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27114-193">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="27114-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27114-194">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27114-195">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-196">Search-Flags</span></span>           | <span data-ttu-id="27114-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27114-197">0x00000000</span></span>                                                            |
| <span data-ttu-id="27114-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-198">System-Flags</span></span>           | <span data-ttu-id="27114-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27114-199">0x00000010</span></span>                                                            |
| <span data-ttu-id="27114-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27114-200">Classes used in</span></span>        | [<span data-ttu-id="27114-201">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="27114-201">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="27114-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="27114-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27114-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27114-203">Windows Server 2008</span></span>



| <span data-ttu-id="27114-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-204">Entry</span></span> | <span data-ttu-id="27114-205">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="27114-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27114-206">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27114-207">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="27114-208">System-Only</span></span>            | <span data-ttu-id="27114-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-209">False</span></span>                                                                 |
| <span data-ttu-id="27114-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27114-210">Is-Single-Valued</span></span>       | <span data-ttu-id="27114-211">True</span><span class="sxs-lookup"><span data-stu-id="27114-211">True</span></span>                                                                  |
| <span data-ttu-id="27114-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27114-212">Is Indexed</span></span>             | <span data-ttu-id="27114-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-213">False</span></span>                                                                 |
| <span data-ttu-id="27114-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27114-214">In Global Catalog</span></span>      | <span data-ttu-id="27114-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-215">False</span></span>                                                                 |
| <span data-ttu-id="27114-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27114-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="27114-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27114-217">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="27114-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27114-218">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27114-219">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-220">Search-Flags</span></span>           | <span data-ttu-id="27114-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27114-221">0x00000000</span></span>                                                            |
| <span data-ttu-id="27114-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-222">System-Flags</span></span>           | <span data-ttu-id="27114-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27114-223">0x00000010</span></span>                                                            |
| <span data-ttu-id="27114-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27114-224">Classes used in</span></span>        | [<span data-ttu-id="27114-225">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="27114-225">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="27114-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="27114-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27114-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27114-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27114-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-228">Entry</span></span> | <span data-ttu-id="27114-229">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="27114-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27114-230">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27114-231">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="27114-232">System-Only</span></span>            | <span data-ttu-id="27114-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-233">False</span></span>                                                                 |
| <span data-ttu-id="27114-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27114-234">Is-Single-Valued</span></span>       | <span data-ttu-id="27114-235">True</span><span class="sxs-lookup"><span data-stu-id="27114-235">True</span></span>                                                                  |
| <span data-ttu-id="27114-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27114-236">Is Indexed</span></span>             | <span data-ttu-id="27114-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-237">False</span></span>                                                                 |
| <span data-ttu-id="27114-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27114-238">In Global Catalog</span></span>      | <span data-ttu-id="27114-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-239">False</span></span>                                                                 |
| <span data-ttu-id="27114-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27114-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="27114-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27114-241">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="27114-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27114-242">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27114-243">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-244">Search-Flags</span></span>           | <span data-ttu-id="27114-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27114-245">0x00000000</span></span>                                                            |
| <span data-ttu-id="27114-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-246">System-Flags</span></span>           | <span data-ttu-id="27114-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27114-247">0x00000010</span></span>                                                            |
| <span data-ttu-id="27114-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27114-248">Classes used in</span></span>        | [<span data-ttu-id="27114-249">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="27114-249">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="27114-250">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="27114-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27114-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27114-251">Windows Server 2012</span></span>



| <span data-ttu-id="27114-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="27114-252">Entry</span></span> | <span data-ttu-id="27114-253">Значение</span><span class="sxs-lookup"><span data-stu-id="27114-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="27114-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27114-254">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27114-255">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="27114-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="27114-256">System-Only</span></span>            | <span data-ttu-id="27114-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-257">False</span></span>                                                                 |
| <span data-ttu-id="27114-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27114-258">Is-Single-Valued</span></span>       | <span data-ttu-id="27114-259">True</span><span class="sxs-lookup"><span data-stu-id="27114-259">True</span></span>                                                                  |
| <span data-ttu-id="27114-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27114-260">Is Indexed</span></span>             | <span data-ttu-id="27114-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-261">False</span></span>                                                                 |
| <span data-ttu-id="27114-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27114-262">In Global Catalog</span></span>      | <span data-ttu-id="27114-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="27114-263">False</span></span>                                                                 |
| <span data-ttu-id="27114-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27114-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="27114-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27114-265">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="27114-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27114-266">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27114-267">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="27114-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-268">Search-Flags</span></span>           | <span data-ttu-id="27114-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27114-269">0x00000000</span></span>                                                            |
| <span data-ttu-id="27114-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27114-270">System-Flags</span></span>           | <span data-ttu-id="27114-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27114-271">0x00000010</span></span>                                                            |
| <span data-ttu-id="27114-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27114-272">Classes used in</span></span>        | [<span data-ttu-id="27114-273">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="27114-273">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="27114-274">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="27114-274">**User**</span></span>](c-user.md)<br/> |



 

 





