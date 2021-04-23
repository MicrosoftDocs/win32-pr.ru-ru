---
title: Атрибут RID
description: Относительный идентификатор объекта.
ms.assetid: 52110cac-033c-475c-84d7-aff631af3413
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута RID
- Схема AD атрибута RID
topic_type:
- apiref
api_name:
- Rid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ab6327fccf804b21a9ba7de6881f98ea4f97be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989776"
---
# <a name="rid-attribute"></a><span data-ttu-id="ffa23-105">Атрибут RID</span><span class="sxs-lookup"><span data-stu-id="ffa23-105">Rid attribute</span></span>

<span data-ttu-id="ffa23-106">Относительный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="ffa23-106">The relative Identifier of an object.</span></span>



| <span data-ttu-id="ffa23-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-107">Entry</span></span> | <span data-ttu-id="ffa23-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ffa23-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffa23-109">CN</span></span>                | <span data-ttu-id="ffa23-110">Избежать</span><span class="sxs-lookup"><span data-stu-id="ffa23-110">Rid</span></span>                                         |
| <span data-ttu-id="ffa23-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ffa23-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffa23-112">rid</span><span class="sxs-lookup"><span data-stu-id="ffa23-112">rid</span></span>                                         |
| <span data-ttu-id="ffa23-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ffa23-113">Size</span></span>              | <span data-ttu-id="ffa23-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="ffa23-114">4 bytes</span></span>                                     |
| <span data-ttu-id="ffa23-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ffa23-115">Update Privilege</span></span>  | <span data-ttu-id="ffa23-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="ffa23-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="ffa23-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ffa23-117">Update Frequency</span></span>  | <span data-ttu-id="ffa23-118">При создании объекта, которому требуется RID.</span><span class="sxs-lookup"><span data-stu-id="ffa23-118">When an object that needs a RID is created.</span></span> |
| <span data-ttu-id="ffa23-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-119">Attribute-Id</span></span>      | <span data-ttu-id="ffa23-120">1.2.840.113556.1.4.153</span><span class="sxs-lookup"><span data-stu-id="ffa23-120">1.2.840.113556.1.4.153</span></span>                      |
| <span data-ttu-id="ffa23-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ffa23-121">System-Id-Guid</span></span>    | <span data-ttu-id="ffa23-122">bf967a22-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ffa23-122">bf967a22-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="ffa23-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffa23-123">Syntax</span></span>            | [<span data-ttu-id="ffa23-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ffa23-124">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="ffa23-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ffa23-125">Implementations</span></span>

-   [<span data-ttu-id="ffa23-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ffa23-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ffa23-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffa23-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffa23-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffa23-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffa23-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffa23-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffa23-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffa23-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffa23-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffa23-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ffa23-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffa23-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ffa23-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-133">Entry</span></span> | <span data-ttu-id="ffa23-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ffa23-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffa23-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffa23-137">System-Only</span></span>            | <span data-ttu-id="ffa23-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-138">False</span></span>                                                        |
| <span data-ttu-id="ffa23-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffa23-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ffa23-140">True</span><span class="sxs-lookup"><span data-stu-id="ffa23-140">True</span></span>                                                         |
| <span data-ttu-id="ffa23-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffa23-141">Is Indexed</span></span>             | <span data-ttu-id="ffa23-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-142">False</span></span>                                                        |
| <span data-ttu-id="ffa23-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffa23-143">In Global Catalog</span></span>      | <span data-ttu-id="ffa23-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-144">False</span></span>                                                        |
| <span data-ttu-id="ffa23-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffa23-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffa23-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffa23-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ffa23-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffa23-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffa23-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-149">Search-Flags</span></span>           | <span data-ttu-id="ffa23-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffa23-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="ffa23-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-151">System-Flags</span></span>           | <span data-ttu-id="ffa23-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffa23-152">0x00000010</span></span>                                                   |
| <span data-ttu-id="ffa23-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffa23-153">Classes used in</span></span>        | [<span data-ttu-id="ffa23-154">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="ffa23-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ffa23-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffa23-155">Windows Server 2003</span></span>



| <span data-ttu-id="ffa23-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-156">Entry</span></span> | <span data-ttu-id="ffa23-157">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ffa23-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffa23-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffa23-160">System-Only</span></span>            | <span data-ttu-id="ffa23-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-161">False</span></span>                                                        |
| <span data-ttu-id="ffa23-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffa23-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ffa23-163">True</span><span class="sxs-lookup"><span data-stu-id="ffa23-163">True</span></span>                                                         |
| <span data-ttu-id="ffa23-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffa23-164">Is Indexed</span></span>             | <span data-ttu-id="ffa23-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-165">False</span></span>                                                        |
| <span data-ttu-id="ffa23-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffa23-166">In Global Catalog</span></span>      | <span data-ttu-id="ffa23-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-167">False</span></span>                                                        |
| <span data-ttu-id="ffa23-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffa23-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffa23-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffa23-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ffa23-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffa23-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffa23-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-172">Search-Flags</span></span>           | <span data-ttu-id="ffa23-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffa23-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="ffa23-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-174">System-Flags</span></span>           | <span data-ttu-id="ffa23-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffa23-175">0x00000010</span></span>                                                   |
| <span data-ttu-id="ffa23-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffa23-176">Classes used in</span></span>        | [<span data-ttu-id="ffa23-177">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="ffa23-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffa23-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffa23-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffa23-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-179">Entry</span></span> | <span data-ttu-id="ffa23-180">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ffa23-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffa23-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffa23-183">System-Only</span></span>            | <span data-ttu-id="ffa23-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-184">False</span></span>                                                        |
| <span data-ttu-id="ffa23-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffa23-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ffa23-186">True</span><span class="sxs-lookup"><span data-stu-id="ffa23-186">True</span></span>                                                         |
| <span data-ttu-id="ffa23-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffa23-187">Is Indexed</span></span>             | <span data-ttu-id="ffa23-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-188">False</span></span>                                                        |
| <span data-ttu-id="ffa23-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffa23-189">In Global Catalog</span></span>      | <span data-ttu-id="ffa23-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-190">False</span></span>                                                        |
| <span data-ttu-id="ffa23-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffa23-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffa23-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffa23-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ffa23-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffa23-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffa23-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-195">Search-Flags</span></span>           | <span data-ttu-id="ffa23-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffa23-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="ffa23-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-197">System-Flags</span></span>           | <span data-ttu-id="ffa23-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffa23-198">0x00000010</span></span>                                                   |
| <span data-ttu-id="ffa23-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffa23-199">Classes used in</span></span>        | [<span data-ttu-id="ffa23-200">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="ffa23-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffa23-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffa23-201">Windows Server 2008</span></span>



| <span data-ttu-id="ffa23-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-202">Entry</span></span> | <span data-ttu-id="ffa23-203">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ffa23-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffa23-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffa23-206">System-Only</span></span>            | <span data-ttu-id="ffa23-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-207">False</span></span>                                                        |
| <span data-ttu-id="ffa23-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffa23-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ffa23-209">True</span><span class="sxs-lookup"><span data-stu-id="ffa23-209">True</span></span>                                                         |
| <span data-ttu-id="ffa23-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffa23-210">Is Indexed</span></span>             | <span data-ttu-id="ffa23-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-211">False</span></span>                                                        |
| <span data-ttu-id="ffa23-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffa23-212">In Global Catalog</span></span>      | <span data-ttu-id="ffa23-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-213">False</span></span>                                                        |
| <span data-ttu-id="ffa23-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffa23-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffa23-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffa23-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ffa23-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffa23-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffa23-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-218">Search-Flags</span></span>           | <span data-ttu-id="ffa23-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffa23-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="ffa23-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-220">System-Flags</span></span>           | <span data-ttu-id="ffa23-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffa23-221">0x00000010</span></span>                                                   |
| <span data-ttu-id="ffa23-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffa23-222">Classes used in</span></span>        | [<span data-ttu-id="ffa23-223">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="ffa23-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffa23-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffa23-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffa23-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-225">Entry</span></span> | <span data-ttu-id="ffa23-226">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ffa23-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffa23-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffa23-229">System-Only</span></span>            | <span data-ttu-id="ffa23-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-230">False</span></span>                                                        |
| <span data-ttu-id="ffa23-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffa23-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ffa23-232">True</span><span class="sxs-lookup"><span data-stu-id="ffa23-232">True</span></span>                                                         |
| <span data-ttu-id="ffa23-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffa23-233">Is Indexed</span></span>             | <span data-ttu-id="ffa23-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-234">False</span></span>                                                        |
| <span data-ttu-id="ffa23-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffa23-235">In Global Catalog</span></span>      | <span data-ttu-id="ffa23-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-236">False</span></span>                                                        |
| <span data-ttu-id="ffa23-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffa23-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffa23-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffa23-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ffa23-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffa23-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffa23-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-241">Search-Flags</span></span>           | <span data-ttu-id="ffa23-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffa23-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="ffa23-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-243">System-Flags</span></span>           | <span data-ttu-id="ffa23-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffa23-244">0x00000010</span></span>                                                   |
| <span data-ttu-id="ffa23-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffa23-245">Classes used in</span></span>        | [<span data-ttu-id="ffa23-246">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="ffa23-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffa23-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffa23-247">Windows Server 2012</span></span>



| <span data-ttu-id="ffa23-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffa23-248">Entry</span></span> | <span data-ttu-id="ffa23-249">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa23-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ffa23-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffa23-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffa23-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ffa23-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffa23-252">System-Only</span></span>            | <span data-ttu-id="ffa23-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-253">False</span></span>                                                        |
| <span data-ttu-id="ffa23-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffa23-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ffa23-255">True</span><span class="sxs-lookup"><span data-stu-id="ffa23-255">True</span></span>                                                         |
| <span data-ttu-id="ffa23-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffa23-256">Is Indexed</span></span>             | <span data-ttu-id="ffa23-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-257">False</span></span>                                                        |
| <span data-ttu-id="ffa23-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffa23-258">In Global Catalog</span></span>      | <span data-ttu-id="ffa23-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffa23-259">False</span></span>                                                        |
| <span data-ttu-id="ffa23-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffa23-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffa23-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffa23-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ffa23-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffa23-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffa23-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="ffa23-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-264">Search-Flags</span></span>           | <span data-ttu-id="ffa23-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffa23-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="ffa23-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffa23-266">System-Flags</span></span>           | <span data-ttu-id="ffa23-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffa23-267">0x00000010</span></span>                                                   |
| <span data-ttu-id="ffa23-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffa23-268">Classes used in</span></span>        | [<span data-ttu-id="ffa23-269">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="ffa23-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





