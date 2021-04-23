---
title: атрибут отметки времени членства MS-DS-Cache-Membership
description: Атрибут "MS-DS-Cache-Time-меткой" используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута метки времени членства MS-DS-Cache-Membership
- msDS-схема AD атрибута-отметки времени членства в кэше
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655205"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="be129-105">атрибут отметки времени членства MS-DS-Cache-Membership</span><span class="sxs-lookup"><span data-stu-id="be129-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="be129-106">Атрибут " **MS-DS-Cache-Time-меткой** " используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.</span><span class="sxs-lookup"><span data-stu-id="be129-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="be129-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="be129-107">Entry</span></span> | <span data-ttu-id="be129-108">Значение</span><span class="sxs-lookup"><span data-stu-id="be129-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="be129-109">CN</span><span class="sxs-lookup"><span data-stu-id="be129-109">CN</span></span>                | <span data-ttu-id="be129-110">Метка времени членства MS-DS-Cache-Membership</span><span class="sxs-lookup"><span data-stu-id="be129-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="be129-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="be129-111">Ldap-Display-Name</span></span> | <span data-ttu-id="be129-112">msDS — метка времени членства в кэше</span><span class="sxs-lookup"><span data-stu-id="be129-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="be129-113">Размер</span><span class="sxs-lookup"><span data-stu-id="be129-113">Size</span></span>              | <span data-ttu-id="be129-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="be129-114">8 bytes</span></span>                              |
| <span data-ttu-id="be129-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="be129-115">Update Privilege</span></span>  | <span data-ttu-id="be129-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="be129-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="be129-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="be129-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="be129-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be129-118">Attribute-Id</span></span>      | <span data-ttu-id="be129-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="be129-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="be129-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="be129-120">System-Id-Guid</span></span>    | <span data-ttu-id="be129-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="be129-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="be129-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be129-122">Syntax</span></span>            | [<span data-ttu-id="be129-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="be129-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="be129-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="be129-124">Implementations</span></span>

-   [<span data-ttu-id="be129-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be129-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be129-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be129-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be129-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be129-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be129-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be129-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be129-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be129-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="be129-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be129-130">Windows Server 2003</span></span>



| <span data-ttu-id="be129-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="be129-131">Entry</span></span> | <span data-ttu-id="be129-132">Значение</span><span class="sxs-lookup"><span data-stu-id="be129-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="be129-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be129-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be129-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="be129-135">System-Only</span></span>            | <span data-ttu-id="be129-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-136">False</span></span>                             |
| <span data-ttu-id="be129-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be129-137">Is-Single-Valued</span></span>       | <span data-ttu-id="be129-138">True</span><span class="sxs-lookup"><span data-stu-id="be129-138">True</span></span>                              |
| <span data-ttu-id="be129-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be129-139">Is Indexed</span></span>             | <span data-ttu-id="be129-140">True</span><span class="sxs-lookup"><span data-stu-id="be129-140">True</span></span>                              |
| <span data-ttu-id="be129-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be129-141">In Global Catalog</span></span>      | <span data-ttu-id="be129-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-142">False</span></span>                             |
| <span data-ttu-id="be129-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be129-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="be129-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be129-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="be129-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be129-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="be129-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be129-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="be129-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-147">Search-Flags</span></span>           | <span data-ttu-id="be129-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be129-148">0x00000001</span></span>                        |
| <span data-ttu-id="be129-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-149">System-Flags</span></span>           | <span data-ttu-id="be129-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="be129-150">0x00000011</span></span>                        |
| <span data-ttu-id="be129-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be129-151">Classes used in</span></span>        | [<span data-ttu-id="be129-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="be129-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be129-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be129-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be129-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="be129-154">Entry</span></span> | <span data-ttu-id="be129-155">Значение</span><span class="sxs-lookup"><span data-stu-id="be129-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="be129-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be129-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be129-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="be129-158">System-Only</span></span>            | <span data-ttu-id="be129-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-159">False</span></span>                             |
| <span data-ttu-id="be129-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be129-160">Is-Single-Valued</span></span>       | <span data-ttu-id="be129-161">True</span><span class="sxs-lookup"><span data-stu-id="be129-161">True</span></span>                              |
| <span data-ttu-id="be129-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be129-162">Is Indexed</span></span>             | <span data-ttu-id="be129-163">True</span><span class="sxs-lookup"><span data-stu-id="be129-163">True</span></span>                              |
| <span data-ttu-id="be129-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be129-164">In Global Catalog</span></span>      | <span data-ttu-id="be129-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-165">False</span></span>                             |
| <span data-ttu-id="be129-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be129-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="be129-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be129-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="be129-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be129-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="be129-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be129-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="be129-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-170">Search-Flags</span></span>           | <span data-ttu-id="be129-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be129-171">0x00000001</span></span>                        |
| <span data-ttu-id="be129-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-172">System-Flags</span></span>           | <span data-ttu-id="be129-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="be129-173">0x00000011</span></span>                        |
| <span data-ttu-id="be129-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be129-174">Classes used in</span></span>        | [<span data-ttu-id="be129-175">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="be129-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be129-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be129-176">Windows Server 2008</span></span>



| <span data-ttu-id="be129-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="be129-177">Entry</span></span> | <span data-ttu-id="be129-178">Значение</span><span class="sxs-lookup"><span data-stu-id="be129-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="be129-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be129-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be129-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="be129-181">System-Only</span></span>            | <span data-ttu-id="be129-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-182">False</span></span>                             |
| <span data-ttu-id="be129-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be129-183">Is-Single-Valued</span></span>       | <span data-ttu-id="be129-184">True</span><span class="sxs-lookup"><span data-stu-id="be129-184">True</span></span>                              |
| <span data-ttu-id="be129-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be129-185">Is Indexed</span></span>             | <span data-ttu-id="be129-186">True</span><span class="sxs-lookup"><span data-stu-id="be129-186">True</span></span>                              |
| <span data-ttu-id="be129-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be129-187">In Global Catalog</span></span>      | <span data-ttu-id="be129-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-188">False</span></span>                             |
| <span data-ttu-id="be129-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be129-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="be129-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be129-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="be129-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be129-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="be129-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be129-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="be129-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-193">Search-Flags</span></span>           | <span data-ttu-id="be129-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be129-194">0x00000001</span></span>                        |
| <span data-ttu-id="be129-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-195">System-Flags</span></span>           | <span data-ttu-id="be129-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="be129-196">0x00000011</span></span>                        |
| <span data-ttu-id="be129-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be129-197">Classes used in</span></span>        | [<span data-ttu-id="be129-198">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="be129-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be129-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be129-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be129-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="be129-200">Entry</span></span> | <span data-ttu-id="be129-201">Значение</span><span class="sxs-lookup"><span data-stu-id="be129-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="be129-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be129-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be129-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="be129-204">System-Only</span></span>            | <span data-ttu-id="be129-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-205">False</span></span>                             |
| <span data-ttu-id="be129-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be129-206">Is-Single-Valued</span></span>       | <span data-ttu-id="be129-207">True</span><span class="sxs-lookup"><span data-stu-id="be129-207">True</span></span>                              |
| <span data-ttu-id="be129-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be129-208">Is Indexed</span></span>             | <span data-ttu-id="be129-209">True</span><span class="sxs-lookup"><span data-stu-id="be129-209">True</span></span>                              |
| <span data-ttu-id="be129-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be129-210">In Global Catalog</span></span>      | <span data-ttu-id="be129-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-211">False</span></span>                             |
| <span data-ttu-id="be129-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be129-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="be129-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be129-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="be129-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be129-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="be129-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be129-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="be129-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-216">Search-Flags</span></span>           | <span data-ttu-id="be129-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be129-217">0x00000001</span></span>                        |
| <span data-ttu-id="be129-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-218">System-Flags</span></span>           | <span data-ttu-id="be129-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="be129-219">0x00000011</span></span>                        |
| <span data-ttu-id="be129-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be129-220">Classes used in</span></span>        | [<span data-ttu-id="be129-221">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="be129-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be129-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be129-222">Windows Server 2012</span></span>



| <span data-ttu-id="be129-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="be129-223">Entry</span></span> | <span data-ttu-id="be129-224">Значение</span><span class="sxs-lookup"><span data-stu-id="be129-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="be129-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="be129-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be129-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="be129-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="be129-227">System-Only</span></span>            | <span data-ttu-id="be129-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-228">False</span></span>                             |
| <span data-ttu-id="be129-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="be129-229">Is-Single-Valued</span></span>       | <span data-ttu-id="be129-230">True</span><span class="sxs-lookup"><span data-stu-id="be129-230">True</span></span>                              |
| <span data-ttu-id="be129-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="be129-231">Is Indexed</span></span>             | <span data-ttu-id="be129-232">True</span><span class="sxs-lookup"><span data-stu-id="be129-232">True</span></span>                              |
| <span data-ttu-id="be129-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="be129-233">In Global Catalog</span></span>      | <span data-ttu-id="be129-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="be129-234">False</span></span>                             |
| <span data-ttu-id="be129-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="be129-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="be129-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="be129-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="be129-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be129-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="be129-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be129-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="be129-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-239">Search-Flags</span></span>           | <span data-ttu-id="be129-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be129-240">0x00000001</span></span>                        |
| <span data-ttu-id="be129-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be129-241">System-Flags</span></span>           | <span data-ttu-id="be129-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="be129-242">0x00000011</span></span>                        |
| <span data-ttu-id="be129-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="be129-243">Classes used in</span></span>        | [<span data-ttu-id="be129-244">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="be129-244">**User**</span></span>](c-user.md)<br/> |



 

 





