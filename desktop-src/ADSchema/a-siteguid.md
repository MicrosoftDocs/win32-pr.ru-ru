---
title: Атрибут site-GUID
description: Уникальный идентификатор для сайта.
ms.assetid: 1baa967e-5aa3-495f-aa4f-14eac74f70e4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута site-GUID
- Схема AD атрибута Ситегуид
topic_type:
- apiref
api_name:
- Site-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3932eb2ced2fe14480010c1120266619cc34456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989628"
---
# <a name="site-guid-attribute"></a><span data-ttu-id="5c4ce-105">Атрибут site-GUID</span><span class="sxs-lookup"><span data-stu-id="5c4ce-105">Site-GUID attribute</span></span>

<span data-ttu-id="5c4ce-106">Уникальный идентификатор для сайта.</span><span class="sxs-lookup"><span data-stu-id="5c4ce-106">The unique identifier for a site.</span></span>



| <span data-ttu-id="5c4ce-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-107">Entry</span></span> | <span data-ttu-id="5c4ce-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5c4ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="5c4ce-109">CN</span></span>                | <span data-ttu-id="5c4ce-110">Сайт — GUID</span><span class="sxs-lookup"><span data-stu-id="5c4ce-110">Site-GUID</span></span>                                             |
| <span data-ttu-id="5c4ce-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5c4ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5c4ce-112">ситегуид</span><span class="sxs-lookup"><span data-stu-id="5c4ce-112">siteGUID</span></span>                                              |
| <span data-ttu-id="5c4ce-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5c4ce-113">Size</span></span>              | <span data-ttu-id="5c4ce-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="5c4ce-114">16 bytes</span></span>                                              |
| <span data-ttu-id="5c4ce-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5c4ce-115">Update Privilege</span></span>  | <span data-ttu-id="5c4ce-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="5c4ce-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="5c4ce-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5c4ce-117">Update Frequency</span></span>  | <span data-ttu-id="5c4ce-118">При создании нового сайта.</span><span class="sxs-lookup"><span data-stu-id="5c4ce-118">Whenever a new site is created.</span></span>                       |
| <span data-ttu-id="5c4ce-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-119">Attribute-Id</span></span>      | <span data-ttu-id="5c4ce-120">1.2.840.113556.1.4.362</span><span class="sxs-lookup"><span data-stu-id="5c4ce-120">1.2.840.113556.1.4.362</span></span>                                |
| <span data-ttu-id="5c4ce-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5c4ce-121">System-Id-Guid</span></span>    | <span data-ttu-id="5c4ce-122">3e978924-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="5c4ce-122">3e978924-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="5c4ce-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c4ce-123">Syntax</span></span>            | [<span data-ttu-id="5c4ce-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5c4ce-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5c4ce-125">Implementations</span></span>

-   [<span data-ttu-id="5c4ce-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c4ce-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c4ce-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c4ce-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c4ce-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c4ce-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c4ce-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c4ce-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5c4ce-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-133">Entry</span></span> | <span data-ttu-id="5c4ce-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4ce-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c4ce-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4ce-137">System-Only</span></span>            | <span data-ttu-id="5c4ce-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-138">False</span></span>                                     |
| <span data-ttu-id="5c4ce-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c4ce-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4ce-140">True</span><span class="sxs-lookup"><span data-stu-id="5c4ce-140">True</span></span>                                      |
| <span data-ttu-id="5c4ce-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c4ce-141">Is Indexed</span></span>             | <span data-ttu-id="5c4ce-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-142">False</span></span>                                     |
| <span data-ttu-id="5c4ce-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c4ce-143">In Global Catalog</span></span>      | <span data-ttu-id="5c4ce-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-144">False</span></span>                                     |
| <span data-ttu-id="5c4ce-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c4ce-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4ce-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c4ce-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4ce-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4ce-147">Range-Lower</span></span>            | <span data-ttu-id="5c4ce-148">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-148">16</span></span>                                        |
| <span data-ttu-id="5c4ce-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4ce-149">Range-Upper</span></span>            | <span data-ttu-id="5c4ce-150">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-150">16</span></span>                                        |
| <span data-ttu-id="5c4ce-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-151">Search-Flags</span></span>           | <span data-ttu-id="5c4ce-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4ce-152">0x00000000</span></span>                                |
| <span data-ttu-id="5c4ce-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-153">System-Flags</span></span>           | <span data-ttu-id="5c4ce-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4ce-154">0x00000010</span></span>                                |
| <span data-ttu-id="5c4ce-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c4ce-155">Classes used in</span></span>        | [<span data-ttu-id="5c4ce-156">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c4ce-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c4ce-157">Windows Server 2003</span></span>



| <span data-ttu-id="5c4ce-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-158">Entry</span></span> | <span data-ttu-id="5c4ce-159">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4ce-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c4ce-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4ce-162">System-Only</span></span>            | <span data-ttu-id="5c4ce-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-163">False</span></span>                                     |
| <span data-ttu-id="5c4ce-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c4ce-164">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4ce-165">True</span><span class="sxs-lookup"><span data-stu-id="5c4ce-165">True</span></span>                                      |
| <span data-ttu-id="5c4ce-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c4ce-166">Is Indexed</span></span>             | <span data-ttu-id="5c4ce-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-167">False</span></span>                                     |
| <span data-ttu-id="5c4ce-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c4ce-168">In Global Catalog</span></span>      | <span data-ttu-id="5c4ce-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-169">False</span></span>                                     |
| <span data-ttu-id="5c4ce-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c4ce-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4ce-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c4ce-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4ce-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4ce-172">Range-Lower</span></span>            | <span data-ttu-id="5c4ce-173">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-173">16</span></span>                                        |
| <span data-ttu-id="5c4ce-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4ce-174">Range-Upper</span></span>            | <span data-ttu-id="5c4ce-175">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-175">16</span></span>                                        |
| <span data-ttu-id="5c4ce-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-176">Search-Flags</span></span>           | <span data-ttu-id="5c4ce-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4ce-177">0x00000000</span></span>                                |
| <span data-ttu-id="5c4ce-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-178">System-Flags</span></span>           | <span data-ttu-id="5c4ce-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4ce-179">0x00000010</span></span>                                |
| <span data-ttu-id="5c4ce-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c4ce-180">Classes used in</span></span>        | [<span data-ttu-id="5c4ce-181">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c4ce-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c4ce-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c4ce-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-183">Entry</span></span> | <span data-ttu-id="5c4ce-184">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4ce-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c4ce-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4ce-187">System-Only</span></span>            | <span data-ttu-id="5c4ce-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-188">False</span></span>                                     |
| <span data-ttu-id="5c4ce-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c4ce-189">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4ce-190">True</span><span class="sxs-lookup"><span data-stu-id="5c4ce-190">True</span></span>                                      |
| <span data-ttu-id="5c4ce-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c4ce-191">Is Indexed</span></span>             | <span data-ttu-id="5c4ce-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-192">False</span></span>                                     |
| <span data-ttu-id="5c4ce-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c4ce-193">In Global Catalog</span></span>      | <span data-ttu-id="5c4ce-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-194">False</span></span>                                     |
| <span data-ttu-id="5c4ce-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c4ce-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4ce-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c4ce-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4ce-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4ce-197">Range-Lower</span></span>            | <span data-ttu-id="5c4ce-198">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-198">16</span></span>                                        |
| <span data-ttu-id="5c4ce-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4ce-199">Range-Upper</span></span>            | <span data-ttu-id="5c4ce-200">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-200">16</span></span>                                        |
| <span data-ttu-id="5c4ce-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-201">Search-Flags</span></span>           | <span data-ttu-id="5c4ce-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4ce-202">0x00000000</span></span>                                |
| <span data-ttu-id="5c4ce-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-203">System-Flags</span></span>           | <span data-ttu-id="5c4ce-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4ce-204">0x00000010</span></span>                                |
| <span data-ttu-id="5c4ce-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c4ce-205">Classes used in</span></span>        | [<span data-ttu-id="5c4ce-206">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c4ce-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c4ce-207">Windows Server 2008</span></span>



| <span data-ttu-id="5c4ce-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-208">Entry</span></span> | <span data-ttu-id="5c4ce-209">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4ce-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c4ce-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4ce-212">System-Only</span></span>            | <span data-ttu-id="5c4ce-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-213">False</span></span>                                     |
| <span data-ttu-id="5c4ce-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c4ce-214">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4ce-215">True</span><span class="sxs-lookup"><span data-stu-id="5c4ce-215">True</span></span>                                      |
| <span data-ttu-id="5c4ce-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c4ce-216">Is Indexed</span></span>             | <span data-ttu-id="5c4ce-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-217">False</span></span>                                     |
| <span data-ttu-id="5c4ce-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c4ce-218">In Global Catalog</span></span>      | <span data-ttu-id="5c4ce-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-219">False</span></span>                                     |
| <span data-ttu-id="5c4ce-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c4ce-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4ce-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c4ce-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4ce-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4ce-222">Range-Lower</span></span>            | <span data-ttu-id="5c4ce-223">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-223">16</span></span>                                        |
| <span data-ttu-id="5c4ce-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4ce-224">Range-Upper</span></span>            | <span data-ttu-id="5c4ce-225">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-225">16</span></span>                                        |
| <span data-ttu-id="5c4ce-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-226">Search-Flags</span></span>           | <span data-ttu-id="5c4ce-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4ce-227">0x00000000</span></span>                                |
| <span data-ttu-id="5c4ce-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-228">System-Flags</span></span>           | <span data-ttu-id="5c4ce-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4ce-229">0x00000010</span></span>                                |
| <span data-ttu-id="5c4ce-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c4ce-230">Classes used in</span></span>        | [<span data-ttu-id="5c4ce-231">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c4ce-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c4ce-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c4ce-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-233">Entry</span></span> | <span data-ttu-id="5c4ce-234">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4ce-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c4ce-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4ce-237">System-Only</span></span>            | <span data-ttu-id="5c4ce-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-238">False</span></span>                                     |
| <span data-ttu-id="5c4ce-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c4ce-239">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4ce-240">True</span><span class="sxs-lookup"><span data-stu-id="5c4ce-240">True</span></span>                                      |
| <span data-ttu-id="5c4ce-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c4ce-241">Is Indexed</span></span>             | <span data-ttu-id="5c4ce-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-242">False</span></span>                                     |
| <span data-ttu-id="5c4ce-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c4ce-243">In Global Catalog</span></span>      | <span data-ttu-id="5c4ce-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-244">False</span></span>                                     |
| <span data-ttu-id="5c4ce-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c4ce-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4ce-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c4ce-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4ce-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4ce-247">Range-Lower</span></span>            | <span data-ttu-id="5c4ce-248">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-248">16</span></span>                                        |
| <span data-ttu-id="5c4ce-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4ce-249">Range-Upper</span></span>            | <span data-ttu-id="5c4ce-250">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-250">16</span></span>                                        |
| <span data-ttu-id="5c4ce-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-251">Search-Flags</span></span>           | <span data-ttu-id="5c4ce-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4ce-252">0x00000000</span></span>                                |
| <span data-ttu-id="5c4ce-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-253">System-Flags</span></span>           | <span data-ttu-id="5c4ce-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4ce-254">0x00000010</span></span>                                |
| <span data-ttu-id="5c4ce-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c4ce-255">Classes used in</span></span>        | [<span data-ttu-id="5c4ce-256">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c4ce-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c4ce-257">Windows Server 2012</span></span>



| <span data-ttu-id="5c4ce-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c4ce-258">Entry</span></span> | <span data-ttu-id="5c4ce-259">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4ce-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4ce-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c4ce-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4ce-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4ce-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4ce-262">System-Only</span></span>            | <span data-ttu-id="5c4ce-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-263">False</span></span>                                     |
| <span data-ttu-id="5c4ce-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c4ce-264">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4ce-265">True</span><span class="sxs-lookup"><span data-stu-id="5c4ce-265">True</span></span>                                      |
| <span data-ttu-id="5c4ce-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c4ce-266">Is Indexed</span></span>             | <span data-ttu-id="5c4ce-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-267">False</span></span>                                     |
| <span data-ttu-id="5c4ce-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c4ce-268">In Global Catalog</span></span>      | <span data-ttu-id="5c4ce-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c4ce-269">False</span></span>                                     |
| <span data-ttu-id="5c4ce-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c4ce-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4ce-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c4ce-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4ce-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4ce-272">Range-Lower</span></span>            | <span data-ttu-id="5c4ce-273">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-273">16</span></span>                                        |
| <span data-ttu-id="5c4ce-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4ce-274">Range-Upper</span></span>            | <span data-ttu-id="5c4ce-275">16</span><span class="sxs-lookup"><span data-stu-id="5c4ce-275">16</span></span>                                        |
| <span data-ttu-id="5c4ce-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-276">Search-Flags</span></span>           | <span data-ttu-id="5c4ce-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4ce-277">0x00000000</span></span>                                |
| <span data-ttu-id="5c4ce-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4ce-278">System-Flags</span></span>           | <span data-ttu-id="5c4ce-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4ce-279">0x00000010</span></span>                                |
| <span data-ttu-id="5c4ce-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c4ce-280">Classes used in</span></span>        | [<span data-ttu-id="5c4ce-281">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="5c4ce-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





