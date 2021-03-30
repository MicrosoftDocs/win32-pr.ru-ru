---
title: Атрибут Admin-Count
description: Указывает, что списки ACL для данного объекта изменились на более безопасное значение системой, так как он был членом одной из административных групп (напрямую или транзитно).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Admin-Count
- Схема AD атрибута Админкаунт
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805129"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="a2c95-105">Атрибут Admin-Count</span><span class="sxs-lookup"><span data-stu-id="a2c95-105">Admin-Count attribute</span></span>

<span data-ttu-id="a2c95-106">Указывает, что списки ACL для данного объекта изменились на более безопасное значение системой, так как он был членом одной из административных групп (напрямую или транзитно).</span><span class="sxs-lookup"><span data-stu-id="a2c95-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="a2c95-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-107">Entry</span></span> | <span data-ttu-id="a2c95-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="a2c95-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2c95-109">CN</span></span>                | <span data-ttu-id="a2c95-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="a2c95-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="a2c95-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a2c95-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2c95-112">админкаунт</span><span class="sxs-lookup"><span data-stu-id="a2c95-112">adminCount</span></span>                                          |
| <span data-ttu-id="a2c95-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a2c95-113">Size</span></span>              | <span data-ttu-id="a2c95-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="a2c95-114">4 bytes</span></span>                                             |
| <span data-ttu-id="a2c95-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a2c95-115">Update Privilege</span></span>  | <span data-ttu-id="a2c95-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="a2c95-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="a2c95-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a2c95-117">Update Frequency</span></span>  | <span data-ttu-id="a2c95-118">При добавлении объекта в административную группу.</span><span class="sxs-lookup"><span data-stu-id="a2c95-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="a2c95-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-119">Attribute-Id</span></span>      | <span data-ttu-id="a2c95-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="a2c95-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="a2c95-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a2c95-121">System-Id-Guid</span></span>    | <span data-ttu-id="a2c95-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a2c95-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="a2c95-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2c95-123">Syntax</span></span>            | [<span data-ttu-id="a2c95-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a2c95-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="a2c95-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a2c95-125">Implementations</span></span>

-   [<span data-ttu-id="a2c95-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2c95-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2c95-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2c95-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2c95-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2c95-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2c95-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2c95-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2c95-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2c95-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2c95-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2c95-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2c95-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2c95-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a2c95-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-133">Entry</span></span> | <span data-ttu-id="a2c95-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2c95-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2c95-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c95-137">System-Only</span></span>            | <span data-ttu-id="a2c95-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-138">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2c95-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c95-140">True</span><span class="sxs-lookup"><span data-stu-id="a2c95-140">True</span></span>                                                                  |
| <span data-ttu-id="a2c95-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2c95-141">Is Indexed</span></span>             | <span data-ttu-id="a2c95-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-142">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2c95-143">In Global Catalog</span></span>      | <span data-ttu-id="a2c95-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-144">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2c95-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c95-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2c95-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="a2c95-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c95-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c95-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-149">Search-Flags</span></span>           | <span data-ttu-id="a2c95-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c95-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="a2c95-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-151">System-Flags</span></span>           | <span data-ttu-id="a2c95-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c95-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="a2c95-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2c95-153">Classes used in</span></span>        | [<span data-ttu-id="a2c95-154">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2c95-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a2c95-155">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="a2c95-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2c95-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2c95-156">Windows Server 2003</span></span>



| <span data-ttu-id="a2c95-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-157">Entry</span></span> | <span data-ttu-id="a2c95-158">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2c95-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2c95-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c95-161">System-Only</span></span>            | <span data-ttu-id="a2c95-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-162">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2c95-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c95-164">True</span><span class="sxs-lookup"><span data-stu-id="a2c95-164">True</span></span>                                                                  |
| <span data-ttu-id="a2c95-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2c95-165">Is Indexed</span></span>             | <span data-ttu-id="a2c95-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-166">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2c95-167">In Global Catalog</span></span>      | <span data-ttu-id="a2c95-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-168">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2c95-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c95-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2c95-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="a2c95-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c95-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c95-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-173">Search-Flags</span></span>           | <span data-ttu-id="a2c95-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c95-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="a2c95-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-175">System-Flags</span></span>           | <span data-ttu-id="a2c95-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c95-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="a2c95-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2c95-177">Classes used in</span></span>        | [<span data-ttu-id="a2c95-178">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2c95-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a2c95-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="a2c95-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2c95-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2c95-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2c95-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-181">Entry</span></span> | <span data-ttu-id="a2c95-182">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2c95-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2c95-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c95-185">System-Only</span></span>            | <span data-ttu-id="a2c95-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-186">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2c95-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c95-188">True</span><span class="sxs-lookup"><span data-stu-id="a2c95-188">True</span></span>                                                                  |
| <span data-ttu-id="a2c95-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2c95-189">Is Indexed</span></span>             | <span data-ttu-id="a2c95-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-190">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2c95-191">In Global Catalog</span></span>      | <span data-ttu-id="a2c95-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-192">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2c95-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c95-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2c95-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="a2c95-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c95-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c95-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-197">Search-Flags</span></span>           | <span data-ttu-id="a2c95-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c95-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="a2c95-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-199">System-Flags</span></span>           | <span data-ttu-id="a2c95-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c95-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="a2c95-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2c95-201">Classes used in</span></span>        | [<span data-ttu-id="a2c95-202">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2c95-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a2c95-203">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="a2c95-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2c95-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2c95-204">Windows Server 2008</span></span>



| <span data-ttu-id="a2c95-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-205">Entry</span></span> | <span data-ttu-id="a2c95-206">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2c95-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2c95-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c95-209">System-Only</span></span>            | <span data-ttu-id="a2c95-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-210">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2c95-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c95-212">True</span><span class="sxs-lookup"><span data-stu-id="a2c95-212">True</span></span>                                                                  |
| <span data-ttu-id="a2c95-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2c95-213">Is Indexed</span></span>             | <span data-ttu-id="a2c95-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-214">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2c95-215">In Global Catalog</span></span>      | <span data-ttu-id="a2c95-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-216">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2c95-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c95-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2c95-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="a2c95-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c95-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c95-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-221">Search-Flags</span></span>           | <span data-ttu-id="a2c95-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c95-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="a2c95-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-223">System-Flags</span></span>           | <span data-ttu-id="a2c95-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c95-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="a2c95-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2c95-225">Classes used in</span></span>        | [<span data-ttu-id="a2c95-226">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2c95-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a2c95-227">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="a2c95-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2c95-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2c95-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2c95-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-229">Entry</span></span> | <span data-ttu-id="a2c95-230">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2c95-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2c95-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c95-233">System-Only</span></span>            | <span data-ttu-id="a2c95-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-234">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2c95-235">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c95-236">True</span><span class="sxs-lookup"><span data-stu-id="a2c95-236">True</span></span>                                                                  |
| <span data-ttu-id="a2c95-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2c95-237">Is Indexed</span></span>             | <span data-ttu-id="a2c95-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-238">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2c95-239">In Global Catalog</span></span>      | <span data-ttu-id="a2c95-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-240">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2c95-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c95-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2c95-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="a2c95-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c95-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c95-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-245">Search-Flags</span></span>           | <span data-ttu-id="a2c95-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c95-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="a2c95-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-247">System-Flags</span></span>           | <span data-ttu-id="a2c95-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c95-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="a2c95-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2c95-249">Classes used in</span></span>        | [<span data-ttu-id="a2c95-250">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2c95-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a2c95-251">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="a2c95-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2c95-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2c95-252">Windows Server 2012</span></span>



| <span data-ttu-id="a2c95-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2c95-253">Entry</span></span> | <span data-ttu-id="a2c95-254">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c95-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2c95-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2c95-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c95-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="a2c95-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c95-257">System-Only</span></span>            | <span data-ttu-id="a2c95-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-258">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2c95-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c95-260">True</span><span class="sxs-lookup"><span data-stu-id="a2c95-260">True</span></span>                                                                  |
| <span data-ttu-id="a2c95-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2c95-261">Is Indexed</span></span>             | <span data-ttu-id="a2c95-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-262">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2c95-263">In Global Catalog</span></span>      | <span data-ttu-id="a2c95-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2c95-264">False</span></span>                                                                 |
| <span data-ttu-id="a2c95-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2c95-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c95-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2c95-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="a2c95-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c95-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c95-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="a2c95-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-269">Search-Flags</span></span>           | <span data-ttu-id="a2c95-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c95-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="a2c95-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c95-271">System-Flags</span></span>           | <span data-ttu-id="a2c95-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c95-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="a2c95-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2c95-273">Classes used in</span></span>        | [<span data-ttu-id="a2c95-274">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2c95-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a2c95-275">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="a2c95-275">**User**</span></span>](c-user.md)<br/> |



 

 





