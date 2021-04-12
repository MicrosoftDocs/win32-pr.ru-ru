---
title: Атрибут "сайт-ссылка-список"
description: Список связей сайтов, связанных с этим мостом.
ms.assetid: 79ec0ae2-ceb3-4321-8b6d-ce5c3bda667a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута списка связей сайтов
- Схема AD атрибута Сителинклист
topic_type:
- apiref
api_name:
- Site-Link-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e71284e4650a3cb146b1656c846483e33a6dd66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416297"
---
# <a name="site-link-list-attribute"></a><span data-ttu-id="d1a62-105">Атрибут "сайт-ссылка-список"</span><span class="sxs-lookup"><span data-stu-id="d1a62-105">Site-Link-List attribute</span></span>

<span data-ttu-id="d1a62-106">Список связей сайтов, связанных с этим мостом.</span><span class="sxs-lookup"><span data-stu-id="d1a62-106">List of site links that are associated with this bridge.</span></span>



| <span data-ttu-id="d1a62-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-107">Entry</span></span> | <span data-ttu-id="d1a62-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-108">Value</span></span> |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1a62-109">CN</span><span class="sxs-lookup"><span data-stu-id="d1a62-109">CN</span></span>                | <span data-ttu-id="d1a62-110">Site-Link-List</span><span class="sxs-lookup"><span data-stu-id="d1a62-110">Site-Link-List</span></span>                                               |
| <span data-ttu-id="d1a62-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d1a62-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d1a62-112">сителинклист</span><span class="sxs-lookup"><span data-stu-id="d1a62-112">siteLinkList</span></span>                                                 |
| <span data-ttu-id="d1a62-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d1a62-113">Size</span></span>              | \-                                                           |
| <span data-ttu-id="d1a62-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d1a62-114">Update Privilege</span></span>  | <span data-ttu-id="d1a62-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="d1a62-115">Domain administrator</span></span>                                         |
| <span data-ttu-id="d1a62-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d1a62-116">Update Frequency</span></span>  | <span data-ttu-id="d1a62-117">При добавлении или удалении связи сайтов из моста.</span><span class="sxs-lookup"><span data-stu-id="d1a62-117">Whenever a site link is added to or removed from the bridge.</span></span> |
| <span data-ttu-id="d1a62-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-118">Attribute-Id</span></span>      | <span data-ttu-id="d1a62-119">1.2.840.113556.1.4.822</span><span class="sxs-lookup"><span data-stu-id="d1a62-119">1.2.840.113556.1.4.822</span></span>                                       |
| <span data-ttu-id="d1a62-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d1a62-120">System-Id-Guid</span></span>    | <span data-ttu-id="d1a62-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d1a62-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span></span>                         |
| <span data-ttu-id="d1a62-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1a62-122">Syntax</span></span>            | [<span data-ttu-id="d1a62-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d1a62-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                      |



## <a name="implementations"></a><span data-ttu-id="d1a62-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d1a62-124">Implementations</span></span>

-   [<span data-ttu-id="d1a62-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d1a62-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d1a62-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1a62-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1a62-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d1a62-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d1a62-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1a62-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1a62-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1a62-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1a62-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1a62-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1a62-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1a62-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d1a62-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1a62-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d1a62-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-133">Entry</span></span> | <span data-ttu-id="d1a62-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-134">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-135">Link-Id</span></span>                | <span data-ttu-id="d1a62-136">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-136">142</span></span>                                                     |
| <span data-ttu-id="d1a62-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-137">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-138">System-Only</span></span>            | <span data-ttu-id="d1a62-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-139">False</span></span>                                                   |
| <span data-ttu-id="d1a62-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-141">False</span></span>                                                   |
| <span data-ttu-id="d1a62-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-142">Is Indexed</span></span>             | <span data-ttu-id="d1a62-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-143">False</span></span>                                                   |
| <span data-ttu-id="d1a62-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-144">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-145">False</span></span>                                                   |
| <span data-ttu-id="d1a62-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-147">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-148">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-149">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-150">Search-Flags</span></span>           | <span data-ttu-id="d1a62-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-151">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-152">System-Flags</span></span>           | <span data-ttu-id="d1a62-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-153">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-154">Classes used in</span></span>        | [<span data-ttu-id="d1a62-155">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-155">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d1a62-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1a62-156">Windows Server 2003</span></span>



| <span data-ttu-id="d1a62-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-157">Entry</span></span> | <span data-ttu-id="d1a62-158">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-158">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-159">Link-Id</span></span>                | <span data-ttu-id="d1a62-160">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-160">142</span></span>                                                     |
| <span data-ttu-id="d1a62-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-161">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-162">System-Only</span></span>            | <span data-ttu-id="d1a62-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-163">False</span></span>                                                   |
| <span data-ttu-id="d1a62-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-165">False</span></span>                                                   |
| <span data-ttu-id="d1a62-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-166">Is Indexed</span></span>             | <span data-ttu-id="d1a62-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-167">False</span></span>                                                   |
| <span data-ttu-id="d1a62-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-168">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-169">False</span></span>                                                   |
| <span data-ttu-id="d1a62-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-171">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-172">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-173">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-174">Search-Flags</span></span>           | <span data-ttu-id="d1a62-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-175">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-176">System-Flags</span></span>           | <span data-ttu-id="d1a62-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-177">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-178">Classes used in</span></span>        | [<span data-ttu-id="d1a62-179">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-179">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d1a62-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="d1a62-180">ADAM</span></span>



| <span data-ttu-id="d1a62-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-181">Entry</span></span> | <span data-ttu-id="d1a62-182">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-182">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-183">Link-Id</span></span>                | <span data-ttu-id="d1a62-184">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-184">142</span></span>                                                     |
| <span data-ttu-id="d1a62-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-185">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-186">System-Only</span></span>            | <span data-ttu-id="d1a62-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-187">False</span></span>                                                   |
| <span data-ttu-id="d1a62-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-189">False</span></span>                                                   |
| <span data-ttu-id="d1a62-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-190">Is Indexed</span></span>             | <span data-ttu-id="d1a62-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-191">False</span></span>                                                   |
| <span data-ttu-id="d1a62-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-192">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-193">False</span></span>                                                   |
| <span data-ttu-id="d1a62-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-195">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-196">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-197">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-198">Search-Flags</span></span>           | <span data-ttu-id="d1a62-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-199">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-200">System-Flags</span></span>           | <span data-ttu-id="d1a62-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-201">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-202">Classes used in</span></span>        | [<span data-ttu-id="d1a62-203">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-203">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1a62-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1a62-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1a62-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-205">Entry</span></span> | <span data-ttu-id="d1a62-206">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-206">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-207">Link-Id</span></span>                | <span data-ttu-id="d1a62-208">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-208">142</span></span>                                                     |
| <span data-ttu-id="d1a62-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-209">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-210">System-Only</span></span>            | <span data-ttu-id="d1a62-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-211">False</span></span>                                                   |
| <span data-ttu-id="d1a62-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-212">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-213">False</span></span>                                                   |
| <span data-ttu-id="d1a62-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-214">Is Indexed</span></span>             | <span data-ttu-id="d1a62-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-215">False</span></span>                                                   |
| <span data-ttu-id="d1a62-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-216">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-217">False</span></span>                                                   |
| <span data-ttu-id="d1a62-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-219">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-220">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-221">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-222">Search-Flags</span></span>           | <span data-ttu-id="d1a62-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-223">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-224">System-Flags</span></span>           | <span data-ttu-id="d1a62-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-225">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-226">Classes used in</span></span>        | [<span data-ttu-id="d1a62-227">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-227">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d1a62-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1a62-228">Windows Server 2008</span></span>



| <span data-ttu-id="d1a62-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-229">Entry</span></span> | <span data-ttu-id="d1a62-230">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-230">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-231">Link-Id</span></span>                | <span data-ttu-id="d1a62-232">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-232">142</span></span>                                                     |
| <span data-ttu-id="d1a62-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-233">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-234">System-Only</span></span>            | <span data-ttu-id="d1a62-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-235">False</span></span>                                                   |
| <span data-ttu-id="d1a62-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-236">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-237">False</span></span>                                                   |
| <span data-ttu-id="d1a62-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-238">Is Indexed</span></span>             | <span data-ttu-id="d1a62-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-239">False</span></span>                                                   |
| <span data-ttu-id="d1a62-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-240">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-241">False</span></span>                                                   |
| <span data-ttu-id="d1a62-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-243">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-244">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-245">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-246">Search-Flags</span></span>           | <span data-ttu-id="d1a62-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-247">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-248">System-Flags</span></span>           | <span data-ttu-id="d1a62-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-249">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-250">Classes used in</span></span>        | [<span data-ttu-id="d1a62-251">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-251">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1a62-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1a62-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1a62-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-253">Entry</span></span> | <span data-ttu-id="d1a62-254">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-254">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-255">Link-Id</span></span>                | <span data-ttu-id="d1a62-256">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-256">142</span></span>                                                     |
| <span data-ttu-id="d1a62-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-257">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-258">System-Only</span></span>            | <span data-ttu-id="d1a62-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-259">False</span></span>                                                   |
| <span data-ttu-id="d1a62-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-260">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-261">False</span></span>                                                   |
| <span data-ttu-id="d1a62-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-262">Is Indexed</span></span>             | <span data-ttu-id="d1a62-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-263">False</span></span>                                                   |
| <span data-ttu-id="d1a62-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-264">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-265">False</span></span>                                                   |
| <span data-ttu-id="d1a62-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-267">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-268">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-269">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-270">Search-Flags</span></span>           | <span data-ttu-id="d1a62-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-271">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-272">System-Flags</span></span>           | <span data-ttu-id="d1a62-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-273">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-274">Classes used in</span></span>        | [<span data-ttu-id="d1a62-275">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-275">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d1a62-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1a62-276">Windows Server 2012</span></span>



| <span data-ttu-id="d1a62-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="d1a62-277">Entry</span></span> | <span data-ttu-id="d1a62-278">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a62-278">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1a62-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d1a62-279">Link-Id</span></span>                | <span data-ttu-id="d1a62-280">142</span><span class="sxs-lookup"><span data-stu-id="d1a62-280">142</span></span>                                                     |
| <span data-ttu-id="d1a62-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1a62-281">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="d1a62-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1a62-282">System-Only</span></span>            | <span data-ttu-id="d1a62-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-283">False</span></span>                                                   |
| <span data-ttu-id="d1a62-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d1a62-284">Is-Single-Valued</span></span>       | <span data-ttu-id="d1a62-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-285">False</span></span>                                                   |
| <span data-ttu-id="d1a62-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d1a62-286">Is Indexed</span></span>             | <span data-ttu-id="d1a62-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-287">False</span></span>                                                   |
| <span data-ttu-id="d1a62-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d1a62-288">In Global Catalog</span></span>      | <span data-ttu-id="d1a62-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="d1a62-289">False</span></span>                                                   |
| <span data-ttu-id="d1a62-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d1a62-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1a62-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1a62-291">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="d1a62-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1a62-292">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1a62-293">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="d1a62-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-294">Search-Flags</span></span>           | <span data-ttu-id="d1a62-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1a62-295">0x00000000</span></span>                                              |
| <span data-ttu-id="d1a62-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1a62-296">System-Flags</span></span>           | <span data-ttu-id="d1a62-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1a62-297">0x00000010</span></span>                                              |
| <span data-ttu-id="d1a62-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d1a62-298">Classes used in</span></span>        | [<span data-ttu-id="d1a62-299">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="d1a62-299">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



 

 





