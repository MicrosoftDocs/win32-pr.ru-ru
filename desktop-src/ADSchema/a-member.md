---
title: Атрибут элемента
description: Список пользователей, принадлежащих группе.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута элемента
- Схема AD атрибута элемента
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654912"
---
# <a name="member-attribute"></a><span data-ttu-id="50b9f-105">Атрибут элемента</span><span class="sxs-lookup"><span data-stu-id="50b9f-105">Member attribute</span></span>

<span data-ttu-id="50b9f-106">Список пользователей, принадлежащих группе.</span><span class="sxs-lookup"><span data-stu-id="50b9f-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="50b9f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-107">Entry</span></span> | <span data-ttu-id="50b9f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="50b9f-109">CN</span><span class="sxs-lookup"><span data-stu-id="50b9f-109">CN</span></span>                | <span data-ttu-id="50b9f-110">Член</span><span class="sxs-lookup"><span data-stu-id="50b9f-110">Member</span></span>                                                |
| <span data-ttu-id="50b9f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="50b9f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="50b9f-112">член</span><span class="sxs-lookup"><span data-stu-id="50b9f-112">member</span></span>                                                |
| <span data-ttu-id="50b9f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="50b9f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="50b9f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="50b9f-114">Update Privilege</span></span>  | <span data-ttu-id="50b9f-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="50b9f-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="50b9f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="50b9f-116">Update Frequency</span></span>  | <span data-ttu-id="50b9f-117">Каждый раз, когда пользователь добавляется в группу или удаляется из нее.</span><span class="sxs-lookup"><span data-stu-id="50b9f-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="50b9f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-118">Attribute-Id</span></span>      | <span data-ttu-id="50b9f-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="50b9f-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="50b9f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="50b9f-120">System-Id-Guid</span></span>    | <span data-ttu-id="50b9f-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="50b9f-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="50b9f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50b9f-122">Syntax</span></span>            | [<span data-ttu-id="50b9f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="50b9f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="50b9f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="50b9f-124">Implementations</span></span>

-   [<span data-ttu-id="50b9f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="50b9f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="50b9f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50b9f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50b9f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="50b9f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="50b9f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50b9f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50b9f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50b9f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50b9f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50b9f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50b9f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50b9f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="50b9f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50b9f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="50b9f-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-133">Entry</span></span> | <span data-ttu-id="50b9f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50b9f-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-135">Link-Id</span></span>                | <span data-ttu-id="50b9f-136">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-136">2</span></span>                                                                                       |
| <span data-ttu-id="50b9f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-137">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="50b9f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-139">System-Only</span></span>            | <span data-ttu-id="50b9f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-140">False</span></span>                                                                                   |
| <span data-ttu-id="50b9f-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-142">False</span></span>                                                                                   |
| <span data-ttu-id="50b9f-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-143">Is Indexed</span></span>             | <span data-ttu-id="50b9f-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-144">False</span></span>                                                                                   |
| <span data-ttu-id="50b9f-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-145">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-146">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-146">True</span></span>                                                                                    |
| <span data-ttu-id="50b9f-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="50b9f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="50b9f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="50b9f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-151">Search-Flags</span></span>           | <span data-ttu-id="50b9f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="50b9f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-153">System-Flags</span></span>           | <span data-ttu-id="50b9f-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="50b9f-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-155">Classes used in</span></span>        | [<span data-ttu-id="50b9f-156">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="50b9f-157">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="50b9f-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="50b9f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50b9f-158">Windows Server 2003</span></span>



| <span data-ttu-id="50b9f-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-159">Entry</span></span> | <span data-ttu-id="50b9f-160">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b9f-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-161">Link-Id</span></span>                | <span data-ttu-id="50b9f-162">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="50b9f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-163">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="50b9f-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-165">System-Only</span></span>            | <span data-ttu-id="50b9f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-167">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-169">Is Indexed</span></span>             | <span data-ttu-id="50b9f-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-171">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-172">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="50b9f-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="50b9f-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-177">Search-Flags</span></span>           | <span data-ttu-id="50b9f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-179">System-Flags</span></span>           | <span data-ttu-id="50b9f-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-181">Classes used in</span></span>        | [<span data-ttu-id="50b9f-182">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="50b9f-183">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="50b9f-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="50b9f-184">**Группа MSMQ**</span><span class="sxs-lookup"><span data-stu-id="50b9f-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="50b9f-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="50b9f-185">ADAM</span></span>



| <span data-ttu-id="50b9f-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-186">Entry</span></span> | <span data-ttu-id="50b9f-187">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="50b9f-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-188">Link-Id</span></span>                | <span data-ttu-id="50b9f-189">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-189">2</span></span>                                   |
| <span data-ttu-id="50b9f-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-190">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-191">0x8009</span></span>                              |
| <span data-ttu-id="50b9f-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-192">System-Only</span></span>            | <span data-ttu-id="50b9f-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-193">False</span></span>                               |
| <span data-ttu-id="50b9f-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-194">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-195">False</span></span>                               |
| <span data-ttu-id="50b9f-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-196">Is Indexed</span></span>             | <span data-ttu-id="50b9f-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-197">False</span></span>                               |
| <span data-ttu-id="50b9f-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-198">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-199">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-199">True</span></span>                                |
| <span data-ttu-id="50b9f-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="50b9f-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="50b9f-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="50b9f-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-204">Search-Flags</span></span>           | <span data-ttu-id="50b9f-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-205">0x00000000</span></span>                          |
| <span data-ttu-id="50b9f-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-206">System-Flags</span></span>           | <span data-ttu-id="50b9f-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-207">0x00000012</span></span>                          |
| <span data-ttu-id="50b9f-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-208">Classes used in</span></span>        | [<span data-ttu-id="50b9f-209">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50b9f-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50b9f-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50b9f-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-211">Entry</span></span> | <span data-ttu-id="50b9f-212">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b9f-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-213">Link-Id</span></span>                | <span data-ttu-id="50b9f-214">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="50b9f-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-215">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="50b9f-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-217">System-Only</span></span>            | <span data-ttu-id="50b9f-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-219">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-221">Is Indexed</span></span>             | <span data-ttu-id="50b9f-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-223">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-224">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="50b9f-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="50b9f-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-229">Search-Flags</span></span>           | <span data-ttu-id="50b9f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-231">System-Flags</span></span>           | <span data-ttu-id="50b9f-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-233">Classes used in</span></span>        | [<span data-ttu-id="50b9f-234">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="50b9f-235">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="50b9f-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="50b9f-236">**Группа MSMQ**</span><span class="sxs-lookup"><span data-stu-id="50b9f-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50b9f-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50b9f-237">Windows Server 2008</span></span>



| <span data-ttu-id="50b9f-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-238">Entry</span></span> | <span data-ttu-id="50b9f-239">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b9f-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-240">Link-Id</span></span>                | <span data-ttu-id="50b9f-241">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="50b9f-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-242">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="50b9f-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-244">System-Only</span></span>            | <span data-ttu-id="50b9f-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-246">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-248">Is Indexed</span></span>             | <span data-ttu-id="50b9f-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-250">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-251">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="50b9f-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="50b9f-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-256">Search-Flags</span></span>           | <span data-ttu-id="50b9f-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-258">System-Flags</span></span>           | <span data-ttu-id="50b9f-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-260">Classes used in</span></span>        | [<span data-ttu-id="50b9f-261">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="50b9f-262">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="50b9f-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="50b9f-263">**Группа MSMQ**</span><span class="sxs-lookup"><span data-stu-id="50b9f-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50b9f-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50b9f-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50b9f-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-265">Entry</span></span> | <span data-ttu-id="50b9f-266">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b9f-267">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-267">Link-Id</span></span>                | <span data-ttu-id="50b9f-268">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="50b9f-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-269">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="50b9f-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-271">System-Only</span></span>            | <span data-ttu-id="50b9f-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-273">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-273">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-275">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-275">Is Indexed</span></span>             | <span data-ttu-id="50b9f-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-277">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-277">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-278">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="50b9f-279">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-280">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="50b9f-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-283">Search-Flags</span></span>           | <span data-ttu-id="50b9f-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-285">System-Flags</span></span>           | <span data-ttu-id="50b9f-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-287">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-287">Classes used in</span></span>        | [<span data-ttu-id="50b9f-288">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="50b9f-289">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="50b9f-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="50b9f-290">**Группа MSMQ**</span><span class="sxs-lookup"><span data-stu-id="50b9f-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50b9f-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50b9f-291">Windows Server 2012</span></span>



| <span data-ttu-id="50b9f-292">Ввод</span><span class="sxs-lookup"><span data-stu-id="50b9f-292">Entry</span></span> | <span data-ttu-id="50b9f-293">Значение</span><span class="sxs-lookup"><span data-stu-id="50b9f-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b9f-294">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="50b9f-294">Link-Id</span></span>                | <span data-ttu-id="50b9f-295">2</span><span class="sxs-lookup"><span data-stu-id="50b9f-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="50b9f-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50b9f-296">MAPI-Id</span></span>                | <span data-ttu-id="50b9f-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="50b9f-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="50b9f-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="50b9f-298">System-Only</span></span>            | <span data-ttu-id="50b9f-299">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-300">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="50b9f-300">Is-Single-Valued</span></span>       | <span data-ttu-id="50b9f-301">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-302">Индексируется</span><span class="sxs-lookup"><span data-stu-id="50b9f-302">Is Indexed</span></span>             | <span data-ttu-id="50b9f-303">Неверно</span><span class="sxs-lookup"><span data-stu-id="50b9f-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="50b9f-304">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="50b9f-304">In Global Catalog</span></span>      | <span data-ttu-id="50b9f-305">True</span><span class="sxs-lookup"><span data-stu-id="50b9f-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="50b9f-306">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="50b9f-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="50b9f-307">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="50b9f-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="50b9f-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50b9f-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50b9f-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="50b9f-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-310">Search-Flags</span></span>           | <span data-ttu-id="50b9f-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50b9f-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50b9f-312">System-Flags</span></span>           | <span data-ttu-id="50b9f-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50b9f-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="50b9f-314">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="50b9f-314">Classes used in</span></span>        | [<span data-ttu-id="50b9f-315">**Группа**</span><span class="sxs-lookup"><span data-stu-id="50b9f-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="50b9f-316">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="50b9f-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="50b9f-317">**Группа MSMQ**</span><span class="sxs-lookup"><span data-stu-id="50b9f-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





