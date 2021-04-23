---
title: атрибут роли MS-DS-Members-for-AZ-Role
description: Список групп приложений-участников или пользователей, связанных с AZ-Role.
ms.assetid: c1234443-fd25-4ed8-a8ee-9853810ebe7d
ms.tgt_platform: multiple
keywords:
- Active-DS-Members-for-AZ-схема AD атрибута role
- Схема AD атрибута msDS-Мемберсфоразроле
topic_type:
- apiref
api_name:
- ms-DS-Members-For-Az-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b19203e5c44d0389e64531867444d1bb2865196
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494031"
---
# <a name="ms-ds-members-for-az-role-attribute"></a><span data-ttu-id="2a8a8-105">атрибут роли MS-DS-Members-for-AZ-Role</span><span class="sxs-lookup"><span data-stu-id="2a8a8-105">ms-DS-Members-For-Az-Role attribute</span></span>

<span data-ttu-id="2a8a8-106">Список групп приложений-участников или пользователей, связанных с AZ-Role.</span><span class="sxs-lookup"><span data-stu-id="2a8a8-106">List of member application groups or users linked to Az-Role.</span></span>



| <span data-ttu-id="2a8a8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2a8a8-107">Entry</span></span> | <span data-ttu-id="2a8a8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8a8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2a8a8-109">CN</span><span class="sxs-lookup"><span data-stu-id="2a8a8-109">CN</span></span>                | <span data-ttu-id="2a8a8-110">MS-DS-Members-for-AZ-Role</span><span class="sxs-lookup"><span data-stu-id="2a8a8-110">ms-DS-Members-For-Az-Role</span></span>               |
| <span data-ttu-id="2a8a8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2a8a8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2a8a8-112">msDS-Мемберсфоразроле</span><span class="sxs-lookup"><span data-stu-id="2a8a8-112">msDS-MembersForAzRole</span></span>                   |
| <span data-ttu-id="2a8a8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2a8a8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2a8a8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2a8a8-114">Update Privilege</span></span>  | <span data-ttu-id="2a8a8-115">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="2a8a8-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="2a8a8-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2a8a8-116">Update Frequency</span></span>  | <span data-ttu-id="2a8a8-117">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="2a8a8-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="2a8a8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a8a8-118">Attribute-Id</span></span>      | <span data-ttu-id="2a8a8-119">1.2.840.113556.1.4.1806</span><span class="sxs-lookup"><span data-stu-id="2a8a8-119">1.2.840.113556.1.4.1806</span></span>                 |
| <span data-ttu-id="2a8a8-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2a8a8-120">System-Id-Guid</span></span>    | <span data-ttu-id="2a8a8-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span><span class="sxs-lookup"><span data-stu-id="2a8a8-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span></span>    |
| <span data-ttu-id="2a8a8-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a8a8-122">Syntax</span></span>            | [<span data-ttu-id="2a8a8-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2a8a8-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2a8a8-124">Implementations</span></span>

-   [<span data-ttu-id="2a8a8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a8a8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a8a8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a8a8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a8a8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2a8a8-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a8a8-130">Windows Server 2003</span></span>



| <span data-ttu-id="2a8a8-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2a8a8-131">Entry</span></span> | <span data-ttu-id="2a8a8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8a8-132">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="2a8a8-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2a8a8-133">Link-Id</span></span>                | <span data-ttu-id="2a8a8-134">2016</span><span class="sxs-lookup"><span data-stu-id="2a8a8-134">2016</span></span>                                              |
| <span data-ttu-id="2a8a8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8a8-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="2a8a8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8a8-136">System-Only</span></span>            | <span data-ttu-id="2a8a8-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-137">False</span></span>                                             |
| <span data-ttu-id="2a8a8-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2a8a8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8a8-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-139">False</span></span>                                             |
| <span data-ttu-id="2a8a8-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2a8a8-140">Is Indexed</span></span>             | <span data-ttu-id="2a8a8-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-141">False</span></span>                                             |
| <span data-ttu-id="2a8a8-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2a8a8-142">In Global Catalog</span></span>      | <span data-ttu-id="2a8a8-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-143">False</span></span>                                             |
| <span data-ttu-id="2a8a8-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2a8a8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8a8-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a8a8-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="2a8a8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8a8-146">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8a8-147">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-148">Search-Flags</span></span>           | <span data-ttu-id="2a8a8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8a8-149">0x00000000</span></span>                                        |
| <span data-ttu-id="2a8a8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-150">System-Flags</span></span>           | <span data-ttu-id="2a8a8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8a8-151">0x00000010</span></span>                                        |
| <span data-ttu-id="2a8a8-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2a8a8-152">Classes used in</span></span>        | [<span data-ttu-id="2a8a8-153">**MS-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-153">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a8a8-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a8a8-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a8a8-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="2a8a8-155">Entry</span></span> | <span data-ttu-id="2a8a8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8a8-156">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="2a8a8-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2a8a8-157">Link-Id</span></span>                | <span data-ttu-id="2a8a8-158">2016</span><span class="sxs-lookup"><span data-stu-id="2a8a8-158">2016</span></span>                                              |
| <span data-ttu-id="2a8a8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8a8-159">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="2a8a8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8a8-160">System-Only</span></span>            | <span data-ttu-id="2a8a8-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-161">False</span></span>                                             |
| <span data-ttu-id="2a8a8-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2a8a8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8a8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-163">False</span></span>                                             |
| <span data-ttu-id="2a8a8-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2a8a8-164">Is Indexed</span></span>             | <span data-ttu-id="2a8a8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-165">False</span></span>                                             |
| <span data-ttu-id="2a8a8-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2a8a8-166">In Global Catalog</span></span>      | <span data-ttu-id="2a8a8-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-167">False</span></span>                                             |
| <span data-ttu-id="2a8a8-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2a8a8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8a8-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a8a8-169">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="2a8a8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8a8-170">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8a8-171">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-172">Search-Flags</span></span>           | <span data-ttu-id="2a8a8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8a8-173">0x00000000</span></span>                                        |
| <span data-ttu-id="2a8a8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-174">System-Flags</span></span>           | <span data-ttu-id="2a8a8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8a8-175">0x00000010</span></span>                                        |
| <span data-ttu-id="2a8a8-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2a8a8-176">Classes used in</span></span>        | [<span data-ttu-id="2a8a8-177">**MS-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-177">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a8a8-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a8a8-178">Windows Server 2008</span></span>



| <span data-ttu-id="2a8a8-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="2a8a8-179">Entry</span></span> | <span data-ttu-id="2a8a8-180">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8a8-180">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="2a8a8-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2a8a8-181">Link-Id</span></span>                | <span data-ttu-id="2a8a8-182">2016</span><span class="sxs-lookup"><span data-stu-id="2a8a8-182">2016</span></span>                                              |
| <span data-ttu-id="2a8a8-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8a8-183">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="2a8a8-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8a8-184">System-Only</span></span>            | <span data-ttu-id="2a8a8-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-185">False</span></span>                                             |
| <span data-ttu-id="2a8a8-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2a8a8-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8a8-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-187">False</span></span>                                             |
| <span data-ttu-id="2a8a8-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2a8a8-188">Is Indexed</span></span>             | <span data-ttu-id="2a8a8-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-189">False</span></span>                                             |
| <span data-ttu-id="2a8a8-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2a8a8-190">In Global Catalog</span></span>      | <span data-ttu-id="2a8a8-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-191">False</span></span>                                             |
| <span data-ttu-id="2a8a8-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2a8a8-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8a8-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a8a8-193">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="2a8a8-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8a8-194">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8a8-195">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-196">Search-Flags</span></span>           | <span data-ttu-id="2a8a8-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8a8-197">0x00000000</span></span>                                        |
| <span data-ttu-id="2a8a8-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-198">System-Flags</span></span>           | <span data-ttu-id="2a8a8-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8a8-199">0x00000010</span></span>                                        |
| <span data-ttu-id="2a8a8-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2a8a8-200">Classes used in</span></span>        | [<span data-ttu-id="2a8a8-201">**MS-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-201">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a8a8-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a8a8-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a8a8-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="2a8a8-203">Entry</span></span> | <span data-ttu-id="2a8a8-204">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8a8-204">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="2a8a8-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2a8a8-205">Link-Id</span></span>                | <span data-ttu-id="2a8a8-206">2016</span><span class="sxs-lookup"><span data-stu-id="2a8a8-206">2016</span></span>                                              |
| <span data-ttu-id="2a8a8-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8a8-207">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="2a8a8-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8a8-208">System-Only</span></span>            | <span data-ttu-id="2a8a8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-209">False</span></span>                                             |
| <span data-ttu-id="2a8a8-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2a8a8-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8a8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-211">False</span></span>                                             |
| <span data-ttu-id="2a8a8-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2a8a8-212">Is Indexed</span></span>             | <span data-ttu-id="2a8a8-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-213">False</span></span>                                             |
| <span data-ttu-id="2a8a8-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2a8a8-214">In Global Catalog</span></span>      | <span data-ttu-id="2a8a8-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-215">False</span></span>                                             |
| <span data-ttu-id="2a8a8-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2a8a8-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8a8-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a8a8-217">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="2a8a8-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8a8-218">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8a8-219">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-220">Search-Flags</span></span>           | <span data-ttu-id="2a8a8-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8a8-221">0x00000000</span></span>                                        |
| <span data-ttu-id="2a8a8-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-222">System-Flags</span></span>           | <span data-ttu-id="2a8a8-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8a8-223">0x00000010</span></span>                                        |
| <span data-ttu-id="2a8a8-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2a8a8-224">Classes used in</span></span>        | [<span data-ttu-id="2a8a8-225">**MS-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-225">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a8a8-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a8a8-226">Windows Server 2012</span></span>



| <span data-ttu-id="2a8a8-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="2a8a8-227">Entry</span></span> | <span data-ttu-id="2a8a8-228">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8a8-228">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="2a8a8-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2a8a8-229">Link-Id</span></span>                | <span data-ttu-id="2a8a8-230">2016</span><span class="sxs-lookup"><span data-stu-id="2a8a8-230">2016</span></span>                                              |
| <span data-ttu-id="2a8a8-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8a8-231">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="2a8a8-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8a8-232">System-Only</span></span>            | <span data-ttu-id="2a8a8-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-233">False</span></span>                                             |
| <span data-ttu-id="2a8a8-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2a8a8-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8a8-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-235">False</span></span>                                             |
| <span data-ttu-id="2a8a8-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2a8a8-236">Is Indexed</span></span>             | <span data-ttu-id="2a8a8-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-237">False</span></span>                                             |
| <span data-ttu-id="2a8a8-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2a8a8-238">In Global Catalog</span></span>      | <span data-ttu-id="2a8a8-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="2a8a8-239">False</span></span>                                             |
| <span data-ttu-id="2a8a8-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2a8a8-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8a8-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a8a8-241">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="2a8a8-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8a8-242">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8a8-243">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="2a8a8-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-244">Search-Flags</span></span>           | <span data-ttu-id="2a8a8-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8a8-245">0x00000000</span></span>                                        |
| <span data-ttu-id="2a8a8-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8a8-246">System-Flags</span></span>           | <span data-ttu-id="2a8a8-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8a8-247">0x00000010</span></span>                                        |
| <span data-ttu-id="2a8a8-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2a8a8-248">Classes used in</span></span>        | [<span data-ttu-id="2a8a8-249">**MS-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="2a8a8-249">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



 

 





