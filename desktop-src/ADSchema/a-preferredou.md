---
title: Атрибут предпочитаемого подразделения
description: Подразделение, отображаемое по умолчанию на рабочем столе пользователя.
ms.assetid: e6f0d6df-0353-4626-8b1b-fa5f99f5ef58
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута предпочитаемого подразделения
- Схема AD атрибута Преферредау
topic_type:
- apiref
api_name:
- Preferred-OU
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b4e2bc2d125524934fa629c0a42121875d14c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535753"
---
# <a name="preferred-ou-attribute"></a><span data-ttu-id="cd0df-105">Атрибут предпочитаемого подразделения</span><span class="sxs-lookup"><span data-stu-id="cd0df-105">Preferred-OU attribute</span></span>

<span data-ttu-id="cd0df-106">Подразделение, отображаемое по умолчанию на рабочем столе пользователя.</span><span class="sxs-lookup"><span data-stu-id="cd0df-106">The Organizational Unit to show by default on user' s desktop.</span></span>



| <span data-ttu-id="cd0df-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-107">Entry</span></span> | <span data-ttu-id="cd0df-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="cd0df-109">CN</span><span class="sxs-lookup"><span data-stu-id="cd0df-109">CN</span></span>                | <span data-ttu-id="cd0df-110">Предпочитаемое подразделение</span><span class="sxs-lookup"><span data-stu-id="cd0df-110">Preferred-OU</span></span>                            |
| <span data-ttu-id="cd0df-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cd0df-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cd0df-112">преферредау</span><span class="sxs-lookup"><span data-stu-id="cd0df-112">preferredOU</span></span>                             |
| <span data-ttu-id="cd0df-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cd0df-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="cd0df-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cd0df-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="cd0df-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cd0df-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="cd0df-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-116">Attribute-Id</span></span>      | <span data-ttu-id="cd0df-117">1.2.840.113556.1.4.97</span><span class="sxs-lookup"><span data-stu-id="cd0df-117">1.2.840.113556.1.4.97</span></span>                   |
| <span data-ttu-id="cd0df-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cd0df-118">System-Id-Guid</span></span>    | <span data-ttu-id="cd0df-119">bf9679ff-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cd0df-119">bf9679ff-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="cd0df-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd0df-120">Syntax</span></span>            | [<span data-ttu-id="cd0df-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="cd0df-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="cd0df-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cd0df-122">Implementations</span></span>

-   [<span data-ttu-id="cd0df-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cd0df-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cd0df-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd0df-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd0df-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd0df-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd0df-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd0df-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd0df-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd0df-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd0df-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd0df-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cd0df-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd0df-129">Windows 2000 Server</span></span>



| <span data-ttu-id="cd0df-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-130">Entry</span></span> | <span data-ttu-id="cd0df-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cd0df-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd0df-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0df-134">System-Only</span></span>            | <span data-ttu-id="cd0df-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-135">False</span></span>                             |
| <span data-ttu-id="cd0df-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd0df-136">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0df-137">True</span><span class="sxs-lookup"><span data-stu-id="cd0df-137">True</span></span>                              |
| <span data-ttu-id="cd0df-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd0df-138">Is Indexed</span></span>             | <span data-ttu-id="cd0df-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-139">False</span></span>                             |
| <span data-ttu-id="cd0df-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd0df-140">In Global Catalog</span></span>      | <span data-ttu-id="cd0df-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-141">False</span></span>                             |
| <span data-ttu-id="cd0df-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd0df-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0df-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd0df-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cd0df-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0df-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cd0df-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0df-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cd0df-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-146">Search-Flags</span></span>           | <span data-ttu-id="cd0df-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-147">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-148">System-Flags</span></span>           | <span data-ttu-id="cd0df-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-149">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd0df-150">Classes used in</span></span>        | [<span data-ttu-id="cd0df-151">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="cd0df-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cd0df-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd0df-152">Windows Server 2003</span></span>



| <span data-ttu-id="cd0df-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-153">Entry</span></span> | <span data-ttu-id="cd0df-154">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cd0df-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd0df-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0df-157">System-Only</span></span>            | <span data-ttu-id="cd0df-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-158">False</span></span>                             |
| <span data-ttu-id="cd0df-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd0df-159">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0df-160">True</span><span class="sxs-lookup"><span data-stu-id="cd0df-160">True</span></span>                              |
| <span data-ttu-id="cd0df-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd0df-161">Is Indexed</span></span>             | <span data-ttu-id="cd0df-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-162">False</span></span>                             |
| <span data-ttu-id="cd0df-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd0df-163">In Global Catalog</span></span>      | <span data-ttu-id="cd0df-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-164">False</span></span>                             |
| <span data-ttu-id="cd0df-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd0df-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0df-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd0df-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cd0df-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0df-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cd0df-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0df-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cd0df-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-169">Search-Flags</span></span>           | <span data-ttu-id="cd0df-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-170">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-171">System-Flags</span></span>           | <span data-ttu-id="cd0df-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-172">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd0df-173">Classes used in</span></span>        | [<span data-ttu-id="cd0df-174">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="cd0df-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd0df-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd0df-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd0df-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-176">Entry</span></span> | <span data-ttu-id="cd0df-177">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cd0df-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd0df-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0df-180">System-Only</span></span>            | <span data-ttu-id="cd0df-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-181">False</span></span>                             |
| <span data-ttu-id="cd0df-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd0df-182">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0df-183">True</span><span class="sxs-lookup"><span data-stu-id="cd0df-183">True</span></span>                              |
| <span data-ttu-id="cd0df-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd0df-184">Is Indexed</span></span>             | <span data-ttu-id="cd0df-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-185">False</span></span>                             |
| <span data-ttu-id="cd0df-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd0df-186">In Global Catalog</span></span>      | <span data-ttu-id="cd0df-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-187">False</span></span>                             |
| <span data-ttu-id="cd0df-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd0df-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0df-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd0df-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cd0df-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0df-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cd0df-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0df-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cd0df-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-192">Search-Flags</span></span>           | <span data-ttu-id="cd0df-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-193">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-194">System-Flags</span></span>           | <span data-ttu-id="cd0df-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-195">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd0df-196">Classes used in</span></span>        | [<span data-ttu-id="cd0df-197">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="cd0df-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd0df-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd0df-198">Windows Server 2008</span></span>



| <span data-ttu-id="cd0df-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-199">Entry</span></span> | <span data-ttu-id="cd0df-200">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cd0df-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd0df-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0df-203">System-Only</span></span>            | <span data-ttu-id="cd0df-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-204">False</span></span>                             |
| <span data-ttu-id="cd0df-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd0df-205">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0df-206">True</span><span class="sxs-lookup"><span data-stu-id="cd0df-206">True</span></span>                              |
| <span data-ttu-id="cd0df-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd0df-207">Is Indexed</span></span>             | <span data-ttu-id="cd0df-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-208">False</span></span>                             |
| <span data-ttu-id="cd0df-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd0df-209">In Global Catalog</span></span>      | <span data-ttu-id="cd0df-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-210">False</span></span>                             |
| <span data-ttu-id="cd0df-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd0df-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0df-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd0df-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cd0df-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0df-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cd0df-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0df-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cd0df-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-215">Search-Flags</span></span>           | <span data-ttu-id="cd0df-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-216">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-217">System-Flags</span></span>           | <span data-ttu-id="cd0df-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-218">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd0df-219">Classes used in</span></span>        | [<span data-ttu-id="cd0df-220">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="cd0df-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd0df-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd0df-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd0df-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-222">Entry</span></span> | <span data-ttu-id="cd0df-223">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cd0df-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd0df-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0df-226">System-Only</span></span>            | <span data-ttu-id="cd0df-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-227">False</span></span>                             |
| <span data-ttu-id="cd0df-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd0df-228">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0df-229">True</span><span class="sxs-lookup"><span data-stu-id="cd0df-229">True</span></span>                              |
| <span data-ttu-id="cd0df-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd0df-230">Is Indexed</span></span>             | <span data-ttu-id="cd0df-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-231">False</span></span>                             |
| <span data-ttu-id="cd0df-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd0df-232">In Global Catalog</span></span>      | <span data-ttu-id="cd0df-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-233">False</span></span>                             |
| <span data-ttu-id="cd0df-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd0df-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0df-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd0df-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cd0df-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0df-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cd0df-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0df-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cd0df-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-238">Search-Flags</span></span>           | <span data-ttu-id="cd0df-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-239">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-240">System-Flags</span></span>           | <span data-ttu-id="cd0df-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-241">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd0df-242">Classes used in</span></span>        | [<span data-ttu-id="cd0df-243">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="cd0df-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd0df-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd0df-244">Windows Server 2012</span></span>



| <span data-ttu-id="cd0df-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd0df-245">Entry</span></span> | <span data-ttu-id="cd0df-246">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0df-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cd0df-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd0df-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd0df-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cd0df-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd0df-249">System-Only</span></span>            | <span data-ttu-id="cd0df-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-250">False</span></span>                             |
| <span data-ttu-id="cd0df-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd0df-251">Is-Single-Valued</span></span>       | <span data-ttu-id="cd0df-252">True</span><span class="sxs-lookup"><span data-stu-id="cd0df-252">True</span></span>                              |
| <span data-ttu-id="cd0df-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd0df-253">Is Indexed</span></span>             | <span data-ttu-id="cd0df-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-254">False</span></span>                             |
| <span data-ttu-id="cd0df-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd0df-255">In Global Catalog</span></span>      | <span data-ttu-id="cd0df-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd0df-256">False</span></span>                             |
| <span data-ttu-id="cd0df-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd0df-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd0df-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd0df-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cd0df-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd0df-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cd0df-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd0df-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cd0df-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-261">Search-Flags</span></span>           | <span data-ttu-id="cd0df-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-262">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd0df-263">System-Flags</span></span>           | <span data-ttu-id="cd0df-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd0df-264">0x00000010</span></span>                        |
| <span data-ttu-id="cd0df-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd0df-265">Classes used in</span></span>        | [<span data-ttu-id="cd0df-266">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="cd0df-266">**User**</span></span>](c-user.md)<br/> |



 

 





