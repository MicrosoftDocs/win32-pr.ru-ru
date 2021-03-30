---
title: Атрибут PRIMARY-Group-ID
description: Содержит относительный идентификатор (RID) для основной группы пользователя. По умолчанию это RID для группы "Пользователи домена".
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута PRIMARY-Group-ID
- Схема AD атрибута Примариграупид
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804870"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="67708-106">Атрибут PRIMARY-Group-ID</span><span class="sxs-lookup"><span data-stu-id="67708-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="67708-107">Содержит относительный идентификатор (RID) для основной группы пользователя.</span><span class="sxs-lookup"><span data-stu-id="67708-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="67708-108">По умолчанию это RID для группы "Пользователи домена".</span><span class="sxs-lookup"><span data-stu-id="67708-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="67708-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-109">Entry</span></span> | <span data-ttu-id="67708-110">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="67708-111">CN</span><span class="sxs-lookup"><span data-stu-id="67708-111">CN</span></span>                | <span data-ttu-id="67708-112">ИДЕНТИФИКАТОР первичной группы</span><span class="sxs-lookup"><span data-stu-id="67708-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="67708-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="67708-113">Ldap-Display-Name</span></span> | <span data-ttu-id="67708-114">примариграупид</span><span class="sxs-lookup"><span data-stu-id="67708-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="67708-115">Размер</span><span class="sxs-lookup"><span data-stu-id="67708-115">Size</span></span>              | <span data-ttu-id="67708-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="67708-116">4 bytes</span></span>                              |
| <span data-ttu-id="67708-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="67708-117">Update Privilege</span></span>  | <span data-ttu-id="67708-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="67708-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="67708-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="67708-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="67708-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="67708-120">Attribute-Id</span></span>      | <span data-ttu-id="67708-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="67708-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="67708-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="67708-122">System-Id-Guid</span></span>    | <span data-ttu-id="67708-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="67708-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="67708-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67708-124">Syntax</span></span>            | [<span data-ttu-id="67708-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="67708-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="67708-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="67708-126">Implementations</span></span>

-   [<span data-ttu-id="67708-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="67708-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="67708-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="67708-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="67708-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="67708-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="67708-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="67708-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="67708-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="67708-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="67708-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="67708-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="67708-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67708-133">Windows 2000 Server</span></span>



| <span data-ttu-id="67708-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-134">Entry</span></span> | <span data-ttu-id="67708-135">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67708-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="67708-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67708-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="67708-138">System-Only</span></span>            | <span data-ttu-id="67708-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="67708-139">False</span></span>                             |
| <span data-ttu-id="67708-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="67708-140">Is-Single-Valued</span></span>       | <span data-ttu-id="67708-141">True</span><span class="sxs-lookup"><span data-stu-id="67708-141">True</span></span>                              |
| <span data-ttu-id="67708-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="67708-142">Is Indexed</span></span>             | <span data-ttu-id="67708-143">True</span><span class="sxs-lookup"><span data-stu-id="67708-143">True</span></span>                              |
| <span data-ttu-id="67708-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="67708-144">In Global Catalog</span></span>      | <span data-ttu-id="67708-145">True</span><span class="sxs-lookup"><span data-stu-id="67708-145">True</span></span>                              |
| <span data-ttu-id="67708-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="67708-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="67708-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="67708-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67708-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67708-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67708-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67708-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67708-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-150">Search-Flags</span></span>           | <span data-ttu-id="67708-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="67708-151">0x00000011</span></span>                        |
| <span data-ttu-id="67708-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-152">System-Flags</span></span>           | <span data-ttu-id="67708-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="67708-153">0x00000012</span></span>                        |
| <span data-ttu-id="67708-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="67708-154">Classes used in</span></span>        | [<span data-ttu-id="67708-155">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="67708-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="67708-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67708-156">Windows Server 2003</span></span>



| <span data-ttu-id="67708-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-157">Entry</span></span> | <span data-ttu-id="67708-158">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67708-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="67708-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67708-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="67708-161">System-Only</span></span>            | <span data-ttu-id="67708-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="67708-162">False</span></span>                             |
| <span data-ttu-id="67708-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="67708-163">Is-Single-Valued</span></span>       | <span data-ttu-id="67708-164">True</span><span class="sxs-lookup"><span data-stu-id="67708-164">True</span></span>                              |
| <span data-ttu-id="67708-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="67708-165">Is Indexed</span></span>             | <span data-ttu-id="67708-166">True</span><span class="sxs-lookup"><span data-stu-id="67708-166">True</span></span>                              |
| <span data-ttu-id="67708-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="67708-167">In Global Catalog</span></span>      | <span data-ttu-id="67708-168">True</span><span class="sxs-lookup"><span data-stu-id="67708-168">True</span></span>                              |
| <span data-ttu-id="67708-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="67708-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="67708-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="67708-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67708-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67708-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67708-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67708-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67708-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-173">Search-Flags</span></span>           | <span data-ttu-id="67708-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="67708-174">0x00000011</span></span>                        |
| <span data-ttu-id="67708-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-175">System-Flags</span></span>           | <span data-ttu-id="67708-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="67708-176">0x00000012</span></span>                        |
| <span data-ttu-id="67708-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="67708-177">Classes used in</span></span>        | [<span data-ttu-id="67708-178">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="67708-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="67708-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="67708-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="67708-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-180">Entry</span></span> | <span data-ttu-id="67708-181">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67708-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="67708-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67708-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="67708-184">System-Only</span></span>            | <span data-ttu-id="67708-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="67708-185">False</span></span>                             |
| <span data-ttu-id="67708-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="67708-186">Is-Single-Valued</span></span>       | <span data-ttu-id="67708-187">True</span><span class="sxs-lookup"><span data-stu-id="67708-187">True</span></span>                              |
| <span data-ttu-id="67708-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="67708-188">Is Indexed</span></span>             | <span data-ttu-id="67708-189">True</span><span class="sxs-lookup"><span data-stu-id="67708-189">True</span></span>                              |
| <span data-ttu-id="67708-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="67708-190">In Global Catalog</span></span>      | <span data-ttu-id="67708-191">True</span><span class="sxs-lookup"><span data-stu-id="67708-191">True</span></span>                              |
| <span data-ttu-id="67708-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="67708-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="67708-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="67708-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67708-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67708-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67708-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67708-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67708-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-196">Search-Flags</span></span>           | <span data-ttu-id="67708-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="67708-197">0x00000011</span></span>                        |
| <span data-ttu-id="67708-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-198">System-Flags</span></span>           | <span data-ttu-id="67708-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="67708-199">0x00000012</span></span>                        |
| <span data-ttu-id="67708-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="67708-200">Classes used in</span></span>        | [<span data-ttu-id="67708-201">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="67708-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="67708-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67708-202">Windows Server 2008</span></span>



| <span data-ttu-id="67708-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-203">Entry</span></span> | <span data-ttu-id="67708-204">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67708-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="67708-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67708-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="67708-207">System-Only</span></span>            | <span data-ttu-id="67708-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="67708-208">False</span></span>                             |
| <span data-ttu-id="67708-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="67708-209">Is-Single-Valued</span></span>       | <span data-ttu-id="67708-210">True</span><span class="sxs-lookup"><span data-stu-id="67708-210">True</span></span>                              |
| <span data-ttu-id="67708-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="67708-211">Is Indexed</span></span>             | <span data-ttu-id="67708-212">True</span><span class="sxs-lookup"><span data-stu-id="67708-212">True</span></span>                              |
| <span data-ttu-id="67708-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="67708-213">In Global Catalog</span></span>      | <span data-ttu-id="67708-214">True</span><span class="sxs-lookup"><span data-stu-id="67708-214">True</span></span>                              |
| <span data-ttu-id="67708-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="67708-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="67708-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="67708-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67708-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67708-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67708-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67708-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67708-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-219">Search-Flags</span></span>           | <span data-ttu-id="67708-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="67708-220">0x00000011</span></span>                        |
| <span data-ttu-id="67708-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-221">System-Flags</span></span>           | <span data-ttu-id="67708-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="67708-222">0x00000012</span></span>                        |
| <span data-ttu-id="67708-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="67708-223">Classes used in</span></span>        | [<span data-ttu-id="67708-224">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="67708-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="67708-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67708-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="67708-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-226">Entry</span></span> | <span data-ttu-id="67708-227">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67708-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="67708-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67708-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="67708-230">System-Only</span></span>            | <span data-ttu-id="67708-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="67708-231">False</span></span>                             |
| <span data-ttu-id="67708-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="67708-232">Is-Single-Valued</span></span>       | <span data-ttu-id="67708-233">True</span><span class="sxs-lookup"><span data-stu-id="67708-233">True</span></span>                              |
| <span data-ttu-id="67708-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="67708-234">Is Indexed</span></span>             | <span data-ttu-id="67708-235">True</span><span class="sxs-lookup"><span data-stu-id="67708-235">True</span></span>                              |
| <span data-ttu-id="67708-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="67708-236">In Global Catalog</span></span>      | <span data-ttu-id="67708-237">True</span><span class="sxs-lookup"><span data-stu-id="67708-237">True</span></span>                              |
| <span data-ttu-id="67708-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="67708-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="67708-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="67708-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67708-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67708-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67708-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67708-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67708-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-242">Search-Flags</span></span>           | <span data-ttu-id="67708-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="67708-243">0x00000011</span></span>                        |
| <span data-ttu-id="67708-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-244">System-Flags</span></span>           | <span data-ttu-id="67708-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="67708-245">0x00000012</span></span>                        |
| <span data-ttu-id="67708-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="67708-246">Classes used in</span></span>        | [<span data-ttu-id="67708-247">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="67708-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="67708-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67708-248">Windows Server 2012</span></span>



| <span data-ttu-id="67708-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="67708-249">Entry</span></span> | <span data-ttu-id="67708-250">Значение</span><span class="sxs-lookup"><span data-stu-id="67708-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="67708-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="67708-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67708-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="67708-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="67708-253">System-Only</span></span>            | <span data-ttu-id="67708-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="67708-254">False</span></span>                             |
| <span data-ttu-id="67708-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="67708-255">Is-Single-Valued</span></span>       | <span data-ttu-id="67708-256">True</span><span class="sxs-lookup"><span data-stu-id="67708-256">True</span></span>                              |
| <span data-ttu-id="67708-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="67708-257">Is Indexed</span></span>             | <span data-ttu-id="67708-258">True</span><span class="sxs-lookup"><span data-stu-id="67708-258">True</span></span>                              |
| <span data-ttu-id="67708-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="67708-259">In Global Catalog</span></span>      | <span data-ttu-id="67708-260">True</span><span class="sxs-lookup"><span data-stu-id="67708-260">True</span></span>                              |
| <span data-ttu-id="67708-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="67708-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="67708-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="67708-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="67708-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67708-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="67708-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67708-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="67708-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-265">Search-Flags</span></span>           | <span data-ttu-id="67708-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="67708-266">0x00000011</span></span>                        |
| <span data-ttu-id="67708-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67708-267">System-Flags</span></span>           | <span data-ttu-id="67708-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="67708-268">0x00000012</span></span>                        |
| <span data-ttu-id="67708-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="67708-269">Classes used in</span></span>        | [<span data-ttu-id="67708-270">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="67708-270">**User**</span></span>](c-user.md)<br/> |



 

 





