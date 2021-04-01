---
title: Атрибут Site-List
description: Список сайтов, подключенных к этому объекту ссылки.
ms.assetid: c27dece1-513d-450e-b777-6fc7172d970a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Site-List
- Схема AD атрибута Сителист
topic_type:
- apiref
api_name:
- Site-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3be0fcdc67fc07693a1354e589f67b7efe3f00a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138458"
---
# <a name="site-list-attribute"></a><span data-ttu-id="3d6ec-105">Атрибут Site-List</span><span class="sxs-lookup"><span data-stu-id="3d6ec-105">Site-List attribute</span></span>

<span data-ttu-id="3d6ec-106">Список сайтов, подключенных к этому объекту ссылки.</span><span class="sxs-lookup"><span data-stu-id="3d6ec-106">List of sites connected to this link object.</span></span>



| <span data-ttu-id="3d6ec-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-107">Entry</span></span> | <span data-ttu-id="3d6ec-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="3d6ec-109">CN</span><span class="sxs-lookup"><span data-stu-id="3d6ec-109">CN</span></span>                | <span data-ttu-id="3d6ec-110">Site-List</span><span class="sxs-lookup"><span data-stu-id="3d6ec-110">Site-List</span></span>                                    |
| <span data-ttu-id="3d6ec-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3d6ec-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3d6ec-112">сителист</span><span class="sxs-lookup"><span data-stu-id="3d6ec-112">siteList</span></span>                                     |
| <span data-ttu-id="3d6ec-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3d6ec-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="3d6ec-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3d6ec-114">Update Privilege</span></span>  | <span data-ttu-id="3d6ec-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="3d6ec-115">Domain administrator</span></span>                         |
| <span data-ttu-id="3d6ec-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3d6ec-116">Update Frequency</span></span>  | <span data-ttu-id="3d6ec-117">При каждом добавлении или удалении сайта из.</span><span class="sxs-lookup"><span data-stu-id="3d6ec-117">Whenever a site is added to or removed from.</span></span> |
| <span data-ttu-id="3d6ec-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-118">Attribute-Id</span></span>      | <span data-ttu-id="3d6ec-119">1.2.840.113556.1.4.821</span><span class="sxs-lookup"><span data-stu-id="3d6ec-119">1.2.840.113556.1.4.821</span></span>                       |
| <span data-ttu-id="3d6ec-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3d6ec-120">System-Id-Guid</span></span>    | <span data-ttu-id="3d6ec-121">d50c2cdc-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3d6ec-121">d50c2cdc-8951-11d1-aebc-0000f80367c1</span></span>         |
| <span data-ttu-id="3d6ec-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d6ec-122">Syntax</span></span>            | [<span data-ttu-id="3d6ec-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="3d6ec-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3d6ec-124">Implementations</span></span>

-   [<span data-ttu-id="3d6ec-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d6ec-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d6ec-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3d6ec-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d6ec-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d6ec-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d6ec-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d6ec-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d6ec-132">Windows 2000 Server</span></span>



| <span data-ttu-id="3d6ec-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-133">Entry</span></span> | <span data-ttu-id="3d6ec-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-135">Link-Id</span></span>                | <span data-ttu-id="3d6ec-136">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-136">144</span></span>                                        |
| <span data-ttu-id="3d6ec-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-137">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-138">System-Only</span></span>            | <span data-ttu-id="3d6ec-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-139">False</span></span>                                      |
| <span data-ttu-id="3d6ec-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-141">False</span></span>                                      |
| <span data-ttu-id="3d6ec-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-142">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-143">False</span></span>                                      |
| <span data-ttu-id="3d6ec-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-144">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-145">False</span></span>                                      |
| <span data-ttu-id="3d6ec-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-147">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-148">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-149">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-150">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-151">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-152">System-Flags</span></span>           | <span data-ttu-id="3d6ec-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-153">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-154">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-155">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-155">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d6ec-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d6ec-156">Windows Server 2003</span></span>



| <span data-ttu-id="3d6ec-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-157">Entry</span></span> | <span data-ttu-id="3d6ec-158">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-158">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-159">Link-Id</span></span>                | <span data-ttu-id="3d6ec-160">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-160">144</span></span>                                        |
| <span data-ttu-id="3d6ec-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-162">System-Only</span></span>            | <span data-ttu-id="3d6ec-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-163">False</span></span>                                      |
| <span data-ttu-id="3d6ec-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-164">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-165">False</span></span>                                      |
| <span data-ttu-id="3d6ec-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-166">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-167">False</span></span>                                      |
| <span data-ttu-id="3d6ec-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-168">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-169">False</span></span>                                      |
| <span data-ttu-id="3d6ec-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-172">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-173">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-174">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-175">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-176">System-Flags</span></span>           | <span data-ttu-id="3d6ec-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-177">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-178">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-179">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-179">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3d6ec-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="3d6ec-180">ADAM</span></span>



| <span data-ttu-id="3d6ec-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-181">Entry</span></span> | <span data-ttu-id="3d6ec-182">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-182">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-183">Link-Id</span></span>                | <span data-ttu-id="3d6ec-184">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-184">144</span></span>                                        |
| <span data-ttu-id="3d6ec-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-185">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-186">System-Only</span></span>            | <span data-ttu-id="3d6ec-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-187">False</span></span>                                      |
| <span data-ttu-id="3d6ec-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-189">False</span></span>                                      |
| <span data-ttu-id="3d6ec-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-190">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-191">False</span></span>                                      |
| <span data-ttu-id="3d6ec-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-192">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-193">False</span></span>                                      |
| <span data-ttu-id="3d6ec-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-195">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-196">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-197">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-198">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-199">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-200">System-Flags</span></span>           | <span data-ttu-id="3d6ec-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-201">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-202">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-203">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-203">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d6ec-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d6ec-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d6ec-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-205">Entry</span></span> | <span data-ttu-id="3d6ec-206">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-206">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-207">Link-Id</span></span>                | <span data-ttu-id="3d6ec-208">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-208">144</span></span>                                        |
| <span data-ttu-id="3d6ec-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-209">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-210">System-Only</span></span>            | <span data-ttu-id="3d6ec-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-211">False</span></span>                                      |
| <span data-ttu-id="3d6ec-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-212">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-213">False</span></span>                                      |
| <span data-ttu-id="3d6ec-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-214">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-215">False</span></span>                                      |
| <span data-ttu-id="3d6ec-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-216">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-217">False</span></span>                                      |
| <span data-ttu-id="3d6ec-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-219">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-220">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-221">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-222">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-223">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-224">System-Flags</span></span>           | <span data-ttu-id="3d6ec-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-225">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-226">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-227">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-227">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d6ec-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d6ec-228">Windows Server 2008</span></span>



| <span data-ttu-id="3d6ec-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-229">Entry</span></span> | <span data-ttu-id="3d6ec-230">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-230">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-231">Link-Id</span></span>                | <span data-ttu-id="3d6ec-232">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-232">144</span></span>                                        |
| <span data-ttu-id="3d6ec-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-233">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-234">System-Only</span></span>            | <span data-ttu-id="3d6ec-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-235">False</span></span>                                      |
| <span data-ttu-id="3d6ec-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-236">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-237">False</span></span>                                      |
| <span data-ttu-id="3d6ec-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-238">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-239">False</span></span>                                      |
| <span data-ttu-id="3d6ec-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-240">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-241">False</span></span>                                      |
| <span data-ttu-id="3d6ec-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-243">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-244">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-245">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-246">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-247">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-248">System-Flags</span></span>           | <span data-ttu-id="3d6ec-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-249">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-250">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-251">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-251">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d6ec-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d6ec-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d6ec-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-253">Entry</span></span> | <span data-ttu-id="3d6ec-254">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-254">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-255">Link-Id</span></span>                | <span data-ttu-id="3d6ec-256">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-256">144</span></span>                                        |
| <span data-ttu-id="3d6ec-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-257">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-258">System-Only</span></span>            | <span data-ttu-id="3d6ec-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-259">False</span></span>                                      |
| <span data-ttu-id="3d6ec-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-260">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-261">False</span></span>                                      |
| <span data-ttu-id="3d6ec-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-262">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-263">False</span></span>                                      |
| <span data-ttu-id="3d6ec-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-264">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-265">False</span></span>                                      |
| <span data-ttu-id="3d6ec-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-267">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-268">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-269">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-270">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-271">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-272">System-Flags</span></span>           | <span data-ttu-id="3d6ec-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-273">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-274">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-275">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-275">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d6ec-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d6ec-276">Windows Server 2012</span></span>



| <span data-ttu-id="3d6ec-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d6ec-277">Entry</span></span> | <span data-ttu-id="3d6ec-278">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6ec-278">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3d6ec-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d6ec-279">Link-Id</span></span>                | <span data-ttu-id="3d6ec-280">144</span><span class="sxs-lookup"><span data-stu-id="3d6ec-280">144</span></span>                                        |
| <span data-ttu-id="3d6ec-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d6ec-281">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3d6ec-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d6ec-282">System-Only</span></span>            | <span data-ttu-id="3d6ec-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-283">False</span></span>                                      |
| <span data-ttu-id="3d6ec-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d6ec-284">Is-Single-Valued</span></span>       | <span data-ttu-id="3d6ec-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-285">False</span></span>                                      |
| <span data-ttu-id="3d6ec-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d6ec-286">Is Indexed</span></span>             | <span data-ttu-id="3d6ec-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-287">False</span></span>                                      |
| <span data-ttu-id="3d6ec-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d6ec-288">In Global Catalog</span></span>      | <span data-ttu-id="3d6ec-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d6ec-289">False</span></span>                                      |
| <span data-ttu-id="3d6ec-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d6ec-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d6ec-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d6ec-291">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3d6ec-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d6ec-292">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d6ec-293">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="3d6ec-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-294">Search-Flags</span></span>           | <span data-ttu-id="3d6ec-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d6ec-295">0x00000000</span></span>                                 |
| <span data-ttu-id="3d6ec-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d6ec-296">System-Flags</span></span>           | <span data-ttu-id="3d6ec-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d6ec-297">0x00000010</span></span>                                 |
| <span data-ttu-id="3d6ec-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d6ec-298">Classes used in</span></span>        | [<span data-ttu-id="3d6ec-299">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="3d6ec-299">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





