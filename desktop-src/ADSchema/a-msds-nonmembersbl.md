---
title: Атрибут ms-DS-non-members-BL
description: Обратная ссылка из группы или пользователя, не являющегося членом, в AZ Groups, которые связываются с ним (те же функциональные возможности, что и не-Security-Member-BL).
ms.assetid: 51725a95-a9c0-4c88-a390-b8e35b8fd3e1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-non-members-BL
- Схема AD атрибута msDS-Нонмемберсбл
topic_type:
- apiref
api_name:
- ms-DS-Non-Members-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88483757e5c9f87771ce8d71f21d26ea3154f975
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655437"
---
# <a name="ms-ds-non-members-bl-attribute"></a><span data-ttu-id="f2e5b-105">Атрибут ms-DS-non-members-BL</span><span class="sxs-lookup"><span data-stu-id="f2e5b-105">ms-DS-Non-Members-BL attribute</span></span>

<span data-ttu-id="f2e5b-106">Обратная ссылка из группы или пользователя, не являющегося членом, в AZ Groups, которые связываются с ним (те же функциональные возможности, что и не-Security-Member-BL).</span><span class="sxs-lookup"><span data-stu-id="f2e5b-106">Backward link from non-member group or user to Az groups that link to it (same functionality as Non-Security-Member-BL).</span></span>



| <span data-ttu-id="f2e5b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2e5b-107">Entry</span></span> | <span data-ttu-id="f2e5b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e5b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f2e5b-109">CN</span><span class="sxs-lookup"><span data-stu-id="f2e5b-109">CN</span></span>                | <span data-ttu-id="f2e5b-110">MS-DS-не-Members-BL</span><span class="sxs-lookup"><span data-stu-id="f2e5b-110">ms-DS-Non-Members-BL</span></span>                    |
| <span data-ttu-id="f2e5b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f2e5b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f2e5b-112">msDS-Нонмемберсбл</span><span class="sxs-lookup"><span data-stu-id="f2e5b-112">msDS-NonMembersBL</span></span>                       |
| <span data-ttu-id="f2e5b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f2e5b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f2e5b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f2e5b-114">Update Privilege</span></span>  | <span data-ttu-id="f2e5b-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="f2e5b-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="f2e5b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f2e5b-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f2e5b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2e5b-117">Attribute-Id</span></span>      | <span data-ttu-id="f2e5b-118">1.2.840.113556.1.4.1794</span><span class="sxs-lookup"><span data-stu-id="f2e5b-118">1.2.840.113556.1.4.1794</span></span>                 |
| <span data-ttu-id="f2e5b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f2e5b-119">System-Id-Guid</span></span>    | <span data-ttu-id="f2e5b-120">2a8c68fc-3a7a-4e87-8720-fe77c51cbe74</span><span class="sxs-lookup"><span data-stu-id="f2e5b-120">2a8c68fc-3a7a-4e87-8720-fe77c51cbe74</span></span>    |
| <span data-ttu-id="f2e5b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2e5b-121">Syntax</span></span>            | [<span data-ttu-id="f2e5b-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f2e5b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f2e5b-123">Implementations</span></span>

-   [<span data-ttu-id="f2e5b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f2e5b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f2e5b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2e5b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2e5b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f2e5b-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2e5b-129">Windows Server 2003</span></span>



| <span data-ttu-id="f2e5b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2e5b-130">Entry</span></span> | <span data-ttu-id="f2e5b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e5b-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f2e5b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2e5b-132">Link-Id</span></span>                | <span data-ttu-id="f2e5b-133">2015</span><span class="sxs-lookup"><span data-stu-id="f2e5b-133">2015</span></span>                            |
| <span data-ttu-id="f2e5b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e5b-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f2e5b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e5b-135">System-Only</span></span>            | <span data-ttu-id="f2e5b-136">True</span><span class="sxs-lookup"><span data-stu-id="f2e5b-136">True</span></span>                            |
| <span data-ttu-id="f2e5b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2e5b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e5b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-138">False</span></span>                           |
| <span data-ttu-id="f2e5b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2e5b-139">Is Indexed</span></span>             | <span data-ttu-id="f2e5b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-140">False</span></span>                           |
| <span data-ttu-id="f2e5b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2e5b-141">In Global Catalog</span></span>      | <span data-ttu-id="f2e5b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-142">False</span></span>                           |
| <span data-ttu-id="f2e5b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2e5b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e5b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2e5b-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f2e5b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e5b-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e5b-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-147">Search-Flags</span></span>           | <span data-ttu-id="f2e5b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e5b-148">0x00000000</span></span>                      |
| <span data-ttu-id="f2e5b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-149">System-Flags</span></span>           | <span data-ttu-id="f2e5b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e5b-150">0x00000010</span></span>                      |
| <span data-ttu-id="f2e5b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2e5b-151">Classes used in</span></span>        | [<span data-ttu-id="f2e5b-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f2e5b-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2e5b-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f2e5b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2e5b-154">Entry</span></span> | <span data-ttu-id="f2e5b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e5b-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f2e5b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2e5b-156">Link-Id</span></span>                | <span data-ttu-id="f2e5b-157">2015</span><span class="sxs-lookup"><span data-stu-id="f2e5b-157">2015</span></span>                            |
| <span data-ttu-id="f2e5b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e5b-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f2e5b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e5b-159">System-Only</span></span>            | <span data-ttu-id="f2e5b-160">True</span><span class="sxs-lookup"><span data-stu-id="f2e5b-160">True</span></span>                            |
| <span data-ttu-id="f2e5b-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2e5b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e5b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-162">False</span></span>                           |
| <span data-ttu-id="f2e5b-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2e5b-163">Is Indexed</span></span>             | <span data-ttu-id="f2e5b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-164">False</span></span>                           |
| <span data-ttu-id="f2e5b-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2e5b-165">In Global Catalog</span></span>      | <span data-ttu-id="f2e5b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-166">False</span></span>                           |
| <span data-ttu-id="f2e5b-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2e5b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e5b-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2e5b-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f2e5b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e5b-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e5b-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-171">Search-Flags</span></span>           | <span data-ttu-id="f2e5b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e5b-172">0x00000000</span></span>                      |
| <span data-ttu-id="f2e5b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-173">System-Flags</span></span>           | <span data-ttu-id="f2e5b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e5b-174">0x00000010</span></span>                      |
| <span data-ttu-id="f2e5b-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2e5b-175">Classes used in</span></span>        | [<span data-ttu-id="f2e5b-176">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f2e5b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2e5b-177">Windows Server 2008</span></span>



| <span data-ttu-id="f2e5b-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2e5b-178">Entry</span></span> | <span data-ttu-id="f2e5b-179">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e5b-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f2e5b-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2e5b-180">Link-Id</span></span>                | <span data-ttu-id="f2e5b-181">2015</span><span class="sxs-lookup"><span data-stu-id="f2e5b-181">2015</span></span>                            |
| <span data-ttu-id="f2e5b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e5b-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f2e5b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e5b-183">System-Only</span></span>            | <span data-ttu-id="f2e5b-184">True</span><span class="sxs-lookup"><span data-stu-id="f2e5b-184">True</span></span>                            |
| <span data-ttu-id="f2e5b-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2e5b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e5b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-186">False</span></span>                           |
| <span data-ttu-id="f2e5b-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2e5b-187">Is Indexed</span></span>             | <span data-ttu-id="f2e5b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-188">False</span></span>                           |
| <span data-ttu-id="f2e5b-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2e5b-189">In Global Catalog</span></span>      | <span data-ttu-id="f2e5b-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-190">False</span></span>                           |
| <span data-ttu-id="f2e5b-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2e5b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e5b-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2e5b-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f2e5b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e5b-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e5b-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-195">Search-Flags</span></span>           | <span data-ttu-id="f2e5b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e5b-196">0x00000000</span></span>                      |
| <span data-ttu-id="f2e5b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-197">System-Flags</span></span>           | <span data-ttu-id="f2e5b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e5b-198">0x00000010</span></span>                      |
| <span data-ttu-id="f2e5b-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2e5b-199">Classes used in</span></span>        | [<span data-ttu-id="f2e5b-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2e5b-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2e5b-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2e5b-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2e5b-202">Entry</span></span> | <span data-ttu-id="f2e5b-203">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e5b-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f2e5b-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2e5b-204">Link-Id</span></span>                | <span data-ttu-id="f2e5b-205">2015</span><span class="sxs-lookup"><span data-stu-id="f2e5b-205">2015</span></span>                            |
| <span data-ttu-id="f2e5b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e5b-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f2e5b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e5b-207">System-Only</span></span>            | <span data-ttu-id="f2e5b-208">True</span><span class="sxs-lookup"><span data-stu-id="f2e5b-208">True</span></span>                            |
| <span data-ttu-id="f2e5b-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2e5b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e5b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-210">False</span></span>                           |
| <span data-ttu-id="f2e5b-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2e5b-211">Is Indexed</span></span>             | <span data-ttu-id="f2e5b-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-212">False</span></span>                           |
| <span data-ttu-id="f2e5b-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2e5b-213">In Global Catalog</span></span>      | <span data-ttu-id="f2e5b-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-214">False</span></span>                           |
| <span data-ttu-id="f2e5b-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2e5b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e5b-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2e5b-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f2e5b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e5b-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e5b-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-219">Search-Flags</span></span>           | <span data-ttu-id="f2e5b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e5b-220">0x00000000</span></span>                      |
| <span data-ttu-id="f2e5b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-221">System-Flags</span></span>           | <span data-ttu-id="f2e5b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e5b-222">0x00000010</span></span>                      |
| <span data-ttu-id="f2e5b-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2e5b-223">Classes used in</span></span>        | [<span data-ttu-id="f2e5b-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2e5b-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2e5b-225">Windows Server 2012</span></span>



| <span data-ttu-id="f2e5b-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2e5b-226">Entry</span></span> | <span data-ttu-id="f2e5b-227">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e5b-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f2e5b-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2e5b-228">Link-Id</span></span>                | <span data-ttu-id="f2e5b-229">2015</span><span class="sxs-lookup"><span data-stu-id="f2e5b-229">2015</span></span>                            |
| <span data-ttu-id="f2e5b-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e5b-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f2e5b-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e5b-231">System-Only</span></span>            | <span data-ttu-id="f2e5b-232">True</span><span class="sxs-lookup"><span data-stu-id="f2e5b-232">True</span></span>                            |
| <span data-ttu-id="f2e5b-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2e5b-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e5b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-234">False</span></span>                           |
| <span data-ttu-id="f2e5b-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2e5b-235">Is Indexed</span></span>             | <span data-ttu-id="f2e5b-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-236">False</span></span>                           |
| <span data-ttu-id="f2e5b-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2e5b-237">In Global Catalog</span></span>      | <span data-ttu-id="f2e5b-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2e5b-238">False</span></span>                           |
| <span data-ttu-id="f2e5b-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2e5b-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e5b-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2e5b-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f2e5b-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e5b-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e5b-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f2e5b-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-243">Search-Flags</span></span>           | <span data-ttu-id="f2e5b-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e5b-244">0x00000000</span></span>                      |
| <span data-ttu-id="f2e5b-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e5b-245">System-Flags</span></span>           | <span data-ttu-id="f2e5b-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e5b-246">0x00000010</span></span>                      |
| <span data-ttu-id="f2e5b-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2e5b-247">Classes used in</span></span>        | [<span data-ttu-id="f2e5b-248">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f2e5b-248">**Top**</span></span>](c-top.md)<br/> |



 

 





