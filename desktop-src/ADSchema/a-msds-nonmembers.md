---
title: Атрибут ms-DS-non-members
description: Этот атрибут служит той же цели, что и атрибут, не относящийся к безопасности, но с применением правил области.
ms.assetid: 11d3d030-3643-4ed2-a52e-a57f32e9597f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-non-members
- msDS-схема AD атрибутов, не входящих в состав
topic_type:
- apiref
api_name:
- ms-DS-Non-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8ca19af90f2f534f974863aa7d766f6be4624b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893505"
---
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="de444-105">Атрибут ms-DS-non-members</span><span class="sxs-lookup"><span data-stu-id="de444-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="de444-106">Этот атрибут служит той же цели, что и атрибут, не относящийся к безопасности, но с применением правил области.</span><span class="sxs-lookup"><span data-stu-id="de444-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="de444-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="de444-107">Entry</span></span> | <span data-ttu-id="de444-108">Значение</span><span class="sxs-lookup"><span data-stu-id="de444-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="de444-109">CN</span><span class="sxs-lookup"><span data-stu-id="de444-109">CN</span></span>                | <span data-ttu-id="de444-110">MS-DS-не-члены</span><span class="sxs-lookup"><span data-stu-id="de444-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="de444-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="de444-111">Ldap-Display-Name</span></span> | <span data-ttu-id="de444-112">msDS — не члены</span><span class="sxs-lookup"><span data-stu-id="de444-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="de444-113">Размер</span><span class="sxs-lookup"><span data-stu-id="de444-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="de444-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="de444-114">Update Privilege</span></span>  | <span data-ttu-id="de444-115">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="de444-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="de444-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="de444-116">Update Frequency</span></span>  | <span data-ttu-id="de444-117">При инициализации и изменении политики.</span><span class="sxs-lookup"><span data-stu-id="de444-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="de444-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de444-118">Attribute-Id</span></span>      | <span data-ttu-id="de444-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="de444-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="de444-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="de444-120">System-Id-Guid</span></span>    | <span data-ttu-id="de444-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="de444-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="de444-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de444-122">Syntax</span></span>            | [<span data-ttu-id="de444-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="de444-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="de444-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="de444-124">Implementations</span></span>

-   [<span data-ttu-id="de444-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de444-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de444-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de444-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de444-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de444-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de444-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de444-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de444-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de444-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="de444-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de444-130">Windows Server 2003</span></span>



| <span data-ttu-id="de444-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="de444-131">Entry</span></span> | <span data-ttu-id="de444-132">Значение</span><span class="sxs-lookup"><span data-stu-id="de444-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="de444-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de444-133">Link-Id</span></span>                | <span data-ttu-id="de444-134">2014</span><span class="sxs-lookup"><span data-stu-id="de444-134">2014</span></span>                                |
| <span data-ttu-id="de444-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de444-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="de444-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="de444-136">System-Only</span></span>            | <span data-ttu-id="de444-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-137">False</span></span>                               |
| <span data-ttu-id="de444-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de444-138">Is-Single-Valued</span></span>       | <span data-ttu-id="de444-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-139">False</span></span>                               |
| <span data-ttu-id="de444-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de444-140">Is Indexed</span></span>             | <span data-ttu-id="de444-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-141">False</span></span>                               |
| <span data-ttu-id="de444-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de444-142">In Global Catalog</span></span>      | <span data-ttu-id="de444-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-143">False</span></span>                               |
| <span data-ttu-id="de444-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de444-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="de444-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de444-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="de444-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de444-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="de444-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de444-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="de444-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-148">Search-Flags</span></span>           | <span data-ttu-id="de444-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de444-149">0x00000000</span></span>                          |
| <span data-ttu-id="de444-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-150">System-Flags</span></span>           | <span data-ttu-id="de444-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de444-151">0x00000010</span></span>                          |
| <span data-ttu-id="de444-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de444-152">Classes used in</span></span>        | [<span data-ttu-id="de444-153">**Группа**</span><span class="sxs-lookup"><span data-stu-id="de444-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de444-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de444-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de444-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="de444-155">Entry</span></span> | <span data-ttu-id="de444-156">Значение</span><span class="sxs-lookup"><span data-stu-id="de444-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="de444-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de444-157">Link-Id</span></span>                | <span data-ttu-id="de444-158">2014</span><span class="sxs-lookup"><span data-stu-id="de444-158">2014</span></span>                                |
| <span data-ttu-id="de444-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de444-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="de444-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="de444-160">System-Only</span></span>            | <span data-ttu-id="de444-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-161">False</span></span>                               |
| <span data-ttu-id="de444-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de444-162">Is-Single-Valued</span></span>       | <span data-ttu-id="de444-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-163">False</span></span>                               |
| <span data-ttu-id="de444-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de444-164">Is Indexed</span></span>             | <span data-ttu-id="de444-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-165">False</span></span>                               |
| <span data-ttu-id="de444-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de444-166">In Global Catalog</span></span>      | <span data-ttu-id="de444-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-167">False</span></span>                               |
| <span data-ttu-id="de444-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de444-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="de444-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de444-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="de444-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de444-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="de444-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de444-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="de444-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-172">Search-Flags</span></span>           | <span data-ttu-id="de444-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de444-173">0x00000000</span></span>                          |
| <span data-ttu-id="de444-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-174">System-Flags</span></span>           | <span data-ttu-id="de444-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de444-175">0x00000010</span></span>                          |
| <span data-ttu-id="de444-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de444-176">Classes used in</span></span>        | [<span data-ttu-id="de444-177">**Группа**</span><span class="sxs-lookup"><span data-stu-id="de444-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de444-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de444-178">Windows Server 2008</span></span>



| <span data-ttu-id="de444-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="de444-179">Entry</span></span> | <span data-ttu-id="de444-180">Значение</span><span class="sxs-lookup"><span data-stu-id="de444-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="de444-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de444-181">Link-Id</span></span>                | <span data-ttu-id="de444-182">2014</span><span class="sxs-lookup"><span data-stu-id="de444-182">2014</span></span>                                |
| <span data-ttu-id="de444-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de444-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="de444-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="de444-184">System-Only</span></span>            | <span data-ttu-id="de444-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-185">False</span></span>                               |
| <span data-ttu-id="de444-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de444-186">Is-Single-Valued</span></span>       | <span data-ttu-id="de444-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-187">False</span></span>                               |
| <span data-ttu-id="de444-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de444-188">Is Indexed</span></span>             | <span data-ttu-id="de444-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-189">False</span></span>                               |
| <span data-ttu-id="de444-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de444-190">In Global Catalog</span></span>      | <span data-ttu-id="de444-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-191">False</span></span>                               |
| <span data-ttu-id="de444-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de444-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="de444-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de444-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="de444-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de444-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="de444-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de444-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="de444-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-196">Search-Flags</span></span>           | <span data-ttu-id="de444-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de444-197">0x00000000</span></span>                          |
| <span data-ttu-id="de444-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-198">System-Flags</span></span>           | <span data-ttu-id="de444-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de444-199">0x00000010</span></span>                          |
| <span data-ttu-id="de444-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de444-200">Classes used in</span></span>        | [<span data-ttu-id="de444-201">**Группа**</span><span class="sxs-lookup"><span data-stu-id="de444-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de444-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de444-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de444-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="de444-203">Entry</span></span> | <span data-ttu-id="de444-204">Значение</span><span class="sxs-lookup"><span data-stu-id="de444-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="de444-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de444-205">Link-Id</span></span>                | <span data-ttu-id="de444-206">2014</span><span class="sxs-lookup"><span data-stu-id="de444-206">2014</span></span>                                |
| <span data-ttu-id="de444-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de444-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="de444-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="de444-208">System-Only</span></span>            | <span data-ttu-id="de444-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-209">False</span></span>                               |
| <span data-ttu-id="de444-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de444-210">Is-Single-Valued</span></span>       | <span data-ttu-id="de444-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-211">False</span></span>                               |
| <span data-ttu-id="de444-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de444-212">Is Indexed</span></span>             | <span data-ttu-id="de444-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-213">False</span></span>                               |
| <span data-ttu-id="de444-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de444-214">In Global Catalog</span></span>      | <span data-ttu-id="de444-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-215">False</span></span>                               |
| <span data-ttu-id="de444-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de444-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="de444-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de444-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="de444-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de444-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="de444-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de444-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="de444-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-220">Search-Flags</span></span>           | <span data-ttu-id="de444-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de444-221">0x00000000</span></span>                          |
| <span data-ttu-id="de444-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-222">System-Flags</span></span>           | <span data-ttu-id="de444-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de444-223">0x00000010</span></span>                          |
| <span data-ttu-id="de444-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de444-224">Classes used in</span></span>        | [<span data-ttu-id="de444-225">**Группа**</span><span class="sxs-lookup"><span data-stu-id="de444-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de444-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de444-226">Windows Server 2012</span></span>



| <span data-ttu-id="de444-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="de444-227">Entry</span></span> | <span data-ttu-id="de444-228">Значение</span><span class="sxs-lookup"><span data-stu-id="de444-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="de444-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de444-229">Link-Id</span></span>                | <span data-ttu-id="de444-230">2014</span><span class="sxs-lookup"><span data-stu-id="de444-230">2014</span></span>                                |
| <span data-ttu-id="de444-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de444-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="de444-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="de444-232">System-Only</span></span>            | <span data-ttu-id="de444-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-233">False</span></span>                               |
| <span data-ttu-id="de444-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de444-234">Is-Single-Valued</span></span>       | <span data-ttu-id="de444-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-235">False</span></span>                               |
| <span data-ttu-id="de444-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de444-236">Is Indexed</span></span>             | <span data-ttu-id="de444-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-237">False</span></span>                               |
| <span data-ttu-id="de444-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de444-238">In Global Catalog</span></span>      | <span data-ttu-id="de444-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="de444-239">False</span></span>                               |
| <span data-ttu-id="de444-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de444-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="de444-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de444-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="de444-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de444-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="de444-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de444-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="de444-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-244">Search-Flags</span></span>           | <span data-ttu-id="de444-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de444-245">0x00000000</span></span>                          |
| <span data-ttu-id="de444-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de444-246">System-Flags</span></span>           | <span data-ttu-id="de444-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de444-247">0x00000010</span></span>                          |
| <span data-ttu-id="de444-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de444-248">Classes used in</span></span>        | [<span data-ttu-id="de444-249">**Группа**</span><span class="sxs-lookup"><span data-stu-id="de444-249">**Group**</span></span>](c-group.md)<br/> |



 

 





