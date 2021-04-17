---
title: MS-IEEE-80211-атрибут данных
description: Содержит список предпочитаемых конфигураций сети в групповая политика для беспроводных сетей.
ms.assetid: 8e5ae2c6-c048-419d-a684-e450a2445a0e
ms.tgt_platform: multiple
keywords:
- MS-IEEE-80211 — схема AD атрибутов данных
- msieee80211 — схема AD атрибутов данных
topic_type:
- apiref
api_name:
- ms-ieee-80211-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a53138e15a15e4fafecb998b87ef8b4df71fb2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535990"
---
# <a name="ms-ieee-80211-data-attribute"></a><span data-ttu-id="2f46b-105">MS-IEEE-80211-атрибут данных</span><span class="sxs-lookup"><span data-stu-id="2f46b-105">ms-ieee-80211-Data attribute</span></span>

<span data-ttu-id="2f46b-106">Содержит список предпочитаемых конфигураций сети в групповая политика для беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="2f46b-106">Stores a list of preferred network configurations in Group Policy for wireless networks.</span></span>



| <span data-ttu-id="2f46b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2f46b-107">Entry</span></span> | <span data-ttu-id="2f46b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2f46b-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2f46b-109">CN</span><span class="sxs-lookup"><span data-stu-id="2f46b-109">CN</span></span>                | <span data-ttu-id="2f46b-110">MS-IEEE-80211-Data</span><span class="sxs-lookup"><span data-stu-id="2f46b-110">ms-ieee-80211-Data</span></span>                                                               |
| <span data-ttu-id="2f46b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2f46b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2f46b-112">msieee80211 — данные</span><span class="sxs-lookup"><span data-stu-id="2f46b-112">msieee80211-Data</span></span>                                                                 |
| <span data-ttu-id="2f46b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2f46b-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="2f46b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2f46b-114">Update Privilege</span></span>  | <span data-ttu-id="2f46b-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="2f46b-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="2f46b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2f46b-116">Update Frequency</span></span>  | <span data-ttu-id="2f46b-117">Каждый раз, когда администратор домена изменяет политику беспроводной сети для домена или подразделения.</span><span class="sxs-lookup"><span data-stu-id="2f46b-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="2f46b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2f46b-118">Attribute-Id</span></span>      | <span data-ttu-id="2f46b-119">1.2.840.113556.1.4.1821</span><span class="sxs-lookup"><span data-stu-id="2f46b-119">1.2.840.113556.1.4.1821</span></span>                                                          |
| <span data-ttu-id="2f46b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2f46b-120">System-Id-Guid</span></span>    | <span data-ttu-id="2f46b-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span><span class="sxs-lookup"><span data-stu-id="2f46b-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span></span>                                             |
| <span data-ttu-id="2f46b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f46b-122">Syntax</span></span>            | [<span data-ttu-id="2f46b-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="2f46b-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                            |



## <a name="implementations"></a><span data-ttu-id="2f46b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2f46b-124">Implementations</span></span>

-   [<span data-ttu-id="2f46b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2f46b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2f46b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2f46b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2f46b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2f46b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2f46b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f46b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2f46b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2f46b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2f46b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f46b-130">Windows Server 2003</span></span>



| <span data-ttu-id="2f46b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2f46b-131">Entry</span></span> | <span data-ttu-id="2f46b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2f46b-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2f46b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2f46b-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f46b-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f46b-135">System-Only</span></span>            | <span data-ttu-id="2f46b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-136">False</span></span>                                                           |
| <span data-ttu-id="2f46b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2f46b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2f46b-138">True</span><span class="sxs-lookup"><span data-stu-id="2f46b-138">True</span></span>                                                            |
| <span data-ttu-id="2f46b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2f46b-139">Is Indexed</span></span>             | <span data-ttu-id="2f46b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-140">False</span></span>                                                           |
| <span data-ttu-id="2f46b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2f46b-141">In Global Catalog</span></span>      | <span data-ttu-id="2f46b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-142">False</span></span>                                                           |
| <span data-ttu-id="2f46b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2f46b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f46b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f46b-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2f46b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f46b-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f46b-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-147">Search-Flags</span></span>           | <span data-ttu-id="2f46b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f46b-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="2f46b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-149">System-Flags</span></span>           | <span data-ttu-id="2f46b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f46b-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="2f46b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2f46b-151">Classes used in</span></span>        | [<span data-ttu-id="2f46b-152">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="2f46b-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2f46b-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2f46b-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2f46b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2f46b-154">Entry</span></span> | <span data-ttu-id="2f46b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2f46b-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2f46b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2f46b-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f46b-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f46b-158">System-Only</span></span>            | <span data-ttu-id="2f46b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-159">False</span></span>                                                           |
| <span data-ttu-id="2f46b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2f46b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2f46b-161">True</span><span class="sxs-lookup"><span data-stu-id="2f46b-161">True</span></span>                                                            |
| <span data-ttu-id="2f46b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2f46b-162">Is Indexed</span></span>             | <span data-ttu-id="2f46b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-163">False</span></span>                                                           |
| <span data-ttu-id="2f46b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2f46b-164">In Global Catalog</span></span>      | <span data-ttu-id="2f46b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-165">False</span></span>                                                           |
| <span data-ttu-id="2f46b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2f46b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f46b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f46b-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2f46b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f46b-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f46b-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-170">Search-Flags</span></span>           | <span data-ttu-id="2f46b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f46b-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="2f46b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-172">System-Flags</span></span>           | <span data-ttu-id="2f46b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f46b-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="2f46b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2f46b-174">Classes used in</span></span>        | [<span data-ttu-id="2f46b-175">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="2f46b-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2f46b-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f46b-176">Windows Server 2008</span></span>



| <span data-ttu-id="2f46b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2f46b-177">Entry</span></span> | <span data-ttu-id="2f46b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2f46b-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2f46b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2f46b-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f46b-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f46b-181">System-Only</span></span>            | <span data-ttu-id="2f46b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-182">False</span></span>                                                           |
| <span data-ttu-id="2f46b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2f46b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2f46b-184">True</span><span class="sxs-lookup"><span data-stu-id="2f46b-184">True</span></span>                                                            |
| <span data-ttu-id="2f46b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2f46b-185">Is Indexed</span></span>             | <span data-ttu-id="2f46b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-186">False</span></span>                                                           |
| <span data-ttu-id="2f46b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2f46b-187">In Global Catalog</span></span>      | <span data-ttu-id="2f46b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-188">False</span></span>                                                           |
| <span data-ttu-id="2f46b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2f46b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f46b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f46b-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2f46b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f46b-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f46b-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-193">Search-Flags</span></span>           | <span data-ttu-id="2f46b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f46b-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="2f46b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-195">System-Flags</span></span>           | <span data-ttu-id="2f46b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f46b-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="2f46b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2f46b-197">Classes used in</span></span>        | [<span data-ttu-id="2f46b-198">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="2f46b-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2f46b-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f46b-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2f46b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="2f46b-200">Entry</span></span> | <span data-ttu-id="2f46b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2f46b-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2f46b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2f46b-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f46b-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f46b-204">System-Only</span></span>            | <span data-ttu-id="2f46b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-205">False</span></span>                                                           |
| <span data-ttu-id="2f46b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2f46b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2f46b-207">True</span><span class="sxs-lookup"><span data-stu-id="2f46b-207">True</span></span>                                                            |
| <span data-ttu-id="2f46b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2f46b-208">Is Indexed</span></span>             | <span data-ttu-id="2f46b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-209">False</span></span>                                                           |
| <span data-ttu-id="2f46b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2f46b-210">In Global Catalog</span></span>      | <span data-ttu-id="2f46b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-211">False</span></span>                                                           |
| <span data-ttu-id="2f46b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2f46b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f46b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f46b-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2f46b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f46b-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f46b-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-216">Search-Flags</span></span>           | <span data-ttu-id="2f46b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f46b-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="2f46b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-218">System-Flags</span></span>           | <span data-ttu-id="2f46b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f46b-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="2f46b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2f46b-220">Classes used in</span></span>        | [<span data-ttu-id="2f46b-221">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="2f46b-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2f46b-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f46b-222">Windows Server 2012</span></span>



| <span data-ttu-id="2f46b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="2f46b-223">Entry</span></span> | <span data-ttu-id="2f46b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="2f46b-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2f46b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2f46b-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f46b-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2f46b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f46b-227">System-Only</span></span>            | <span data-ttu-id="2f46b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-228">False</span></span>                                                           |
| <span data-ttu-id="2f46b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2f46b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2f46b-230">True</span><span class="sxs-lookup"><span data-stu-id="2f46b-230">True</span></span>                                                            |
| <span data-ttu-id="2f46b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2f46b-231">Is Indexed</span></span>             | <span data-ttu-id="2f46b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-232">False</span></span>                                                           |
| <span data-ttu-id="2f46b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2f46b-233">In Global Catalog</span></span>      | <span data-ttu-id="2f46b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2f46b-234">False</span></span>                                                           |
| <span data-ttu-id="2f46b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2f46b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f46b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f46b-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2f46b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f46b-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f46b-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2f46b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-239">Search-Flags</span></span>           | <span data-ttu-id="2f46b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f46b-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="2f46b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f46b-241">System-Flags</span></span>           | <span data-ttu-id="2f46b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f46b-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="2f46b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2f46b-243">Classes used in</span></span>        | [<span data-ttu-id="2f46b-244">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="2f46b-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 





