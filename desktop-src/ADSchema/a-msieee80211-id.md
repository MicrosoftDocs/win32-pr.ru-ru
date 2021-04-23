---
title: MS-IEEE-80211-атрибут ID
description: Идентификатор, используемый для объекта политики беспроводной связи в AD.
ms.assetid: 751eb9e1-a97f-4a94-a726-151e85ae2dbf
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ID MS-IEEE-80211
- msieee80211 — схема AD атрибута ID
topic_type:
- apiref
api_name:
- ms-ieee-80211-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1b380617cadf5cfc8b5048e6c9513d40001504
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989687"
---
# <a name="ms-ieee-80211-id-attribute"></a><span data-ttu-id="b742f-105">MS-IEEE-80211-атрибут ID</span><span class="sxs-lookup"><span data-stu-id="b742f-105">ms-ieee-80211-ID attribute</span></span>

<span data-ttu-id="b742f-106">Идентификатор, используемый для объекта политики беспроводной связи в AD.</span><span class="sxs-lookup"><span data-stu-id="b742f-106">An identifier used for a wireless policy object on AD.</span></span>



| <span data-ttu-id="b742f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b742f-107">Entry</span></span> | <span data-ttu-id="b742f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b742f-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b742f-109">CN</span><span class="sxs-lookup"><span data-stu-id="b742f-109">CN</span></span>                | <span data-ttu-id="b742f-110">MS-IEEE-80211-ID</span><span class="sxs-lookup"><span data-stu-id="b742f-110">ms-ieee-80211-ID</span></span>                                                                 |
| <span data-ttu-id="b742f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b742f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b742f-112">msieee80211 — идентификатор</span><span class="sxs-lookup"><span data-stu-id="b742f-112">msieee80211-ID</span></span>                                                                   |
| <span data-ttu-id="b742f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b742f-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="b742f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b742f-114">Update Privilege</span></span>  | <span data-ttu-id="b742f-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="b742f-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="b742f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b742f-116">Update Frequency</span></span>  | <span data-ttu-id="b742f-117">Каждый раз, когда администратор домена изменяет политику беспроводной сети для домена или подразделения.</span><span class="sxs-lookup"><span data-stu-id="b742f-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="b742f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b742f-118">Attribute-Id</span></span>      | <span data-ttu-id="b742f-119">1.2.840.113556.1.4.1823</span><span class="sxs-lookup"><span data-stu-id="b742f-119">1.2.840.113556.1.4.1823</span></span>                                                          |
| <span data-ttu-id="b742f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b742f-120">System-Id-Guid</span></span>    | <span data-ttu-id="b742f-121">7f73ef75-14c9-4c23-81de-dd07a06f9e8b</span><span class="sxs-lookup"><span data-stu-id="b742f-121">7f73ef75-14c9-4c23-81de-dd07a06f9e8b</span></span>                                             |
| <span data-ttu-id="b742f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b742f-122">Syntax</span></span>            | [<span data-ttu-id="b742f-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b742f-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="b742f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b742f-124">Implementations</span></span>

-   [<span data-ttu-id="b742f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b742f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b742f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b742f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b742f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b742f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b742f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b742f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b742f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b742f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b742f-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b742f-130">Windows Server 2003</span></span>



| <span data-ttu-id="b742f-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="b742f-131">Entry</span></span> | <span data-ttu-id="b742f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b742f-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b742f-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b742f-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b742f-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b742f-135">System-Only</span></span>            | <span data-ttu-id="b742f-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-136">False</span></span>                                                           |
| <span data-ttu-id="b742f-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b742f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b742f-138">True</span><span class="sxs-lookup"><span data-stu-id="b742f-138">True</span></span>                                                            |
| <span data-ttu-id="b742f-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b742f-139">Is Indexed</span></span>             | <span data-ttu-id="b742f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-140">False</span></span>                                                           |
| <span data-ttu-id="b742f-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b742f-141">In Global Catalog</span></span>      | <span data-ttu-id="b742f-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-142">False</span></span>                                                           |
| <span data-ttu-id="b742f-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b742f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b742f-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b742f-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b742f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b742f-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b742f-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-147">Search-Flags</span></span>           | <span data-ttu-id="b742f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b742f-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="b742f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-149">System-Flags</span></span>           | <span data-ttu-id="b742f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b742f-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="b742f-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b742f-151">Classes used in</span></span>        | [<span data-ttu-id="b742f-152">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="b742f-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b742f-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b742f-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b742f-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="b742f-154">Entry</span></span> | <span data-ttu-id="b742f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="b742f-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b742f-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b742f-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b742f-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b742f-158">System-Only</span></span>            | <span data-ttu-id="b742f-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-159">False</span></span>                                                           |
| <span data-ttu-id="b742f-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b742f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b742f-161">True</span><span class="sxs-lookup"><span data-stu-id="b742f-161">True</span></span>                                                            |
| <span data-ttu-id="b742f-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b742f-162">Is Indexed</span></span>             | <span data-ttu-id="b742f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-163">False</span></span>                                                           |
| <span data-ttu-id="b742f-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b742f-164">In Global Catalog</span></span>      | <span data-ttu-id="b742f-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-165">False</span></span>                                                           |
| <span data-ttu-id="b742f-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b742f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b742f-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b742f-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b742f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b742f-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b742f-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-170">Search-Flags</span></span>           | <span data-ttu-id="b742f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b742f-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="b742f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-172">System-Flags</span></span>           | <span data-ttu-id="b742f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b742f-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="b742f-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b742f-174">Classes used in</span></span>        | [<span data-ttu-id="b742f-175">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="b742f-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b742f-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b742f-176">Windows Server 2008</span></span>



| <span data-ttu-id="b742f-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="b742f-177">Entry</span></span> | <span data-ttu-id="b742f-178">Значение</span><span class="sxs-lookup"><span data-stu-id="b742f-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b742f-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b742f-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b742f-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b742f-181">System-Only</span></span>            | <span data-ttu-id="b742f-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-182">False</span></span>                                                           |
| <span data-ttu-id="b742f-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b742f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b742f-184">True</span><span class="sxs-lookup"><span data-stu-id="b742f-184">True</span></span>                                                            |
| <span data-ttu-id="b742f-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b742f-185">Is Indexed</span></span>             | <span data-ttu-id="b742f-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-186">False</span></span>                                                           |
| <span data-ttu-id="b742f-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b742f-187">In Global Catalog</span></span>      | <span data-ttu-id="b742f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-188">False</span></span>                                                           |
| <span data-ttu-id="b742f-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b742f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b742f-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b742f-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b742f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b742f-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b742f-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-193">Search-Flags</span></span>           | <span data-ttu-id="b742f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b742f-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="b742f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-195">System-Flags</span></span>           | <span data-ttu-id="b742f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b742f-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="b742f-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b742f-197">Classes used in</span></span>        | [<span data-ttu-id="b742f-198">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="b742f-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b742f-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b742f-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b742f-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="b742f-200">Entry</span></span> | <span data-ttu-id="b742f-201">Значение</span><span class="sxs-lookup"><span data-stu-id="b742f-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b742f-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b742f-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b742f-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b742f-204">System-Only</span></span>            | <span data-ttu-id="b742f-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-205">False</span></span>                                                           |
| <span data-ttu-id="b742f-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b742f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b742f-207">True</span><span class="sxs-lookup"><span data-stu-id="b742f-207">True</span></span>                                                            |
| <span data-ttu-id="b742f-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b742f-208">Is Indexed</span></span>             | <span data-ttu-id="b742f-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-209">False</span></span>                                                           |
| <span data-ttu-id="b742f-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b742f-210">In Global Catalog</span></span>      | <span data-ttu-id="b742f-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-211">False</span></span>                                                           |
| <span data-ttu-id="b742f-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b742f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b742f-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b742f-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b742f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b742f-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b742f-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-216">Search-Flags</span></span>           | <span data-ttu-id="b742f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b742f-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="b742f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-218">System-Flags</span></span>           | <span data-ttu-id="b742f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b742f-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="b742f-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b742f-220">Classes used in</span></span>        | [<span data-ttu-id="b742f-221">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="b742f-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b742f-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b742f-222">Windows Server 2012</span></span>



| <span data-ttu-id="b742f-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="b742f-223">Entry</span></span> | <span data-ttu-id="b742f-224">Значение</span><span class="sxs-lookup"><span data-stu-id="b742f-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b742f-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b742f-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b742f-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b742f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b742f-227">System-Only</span></span>            | <span data-ttu-id="b742f-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-228">False</span></span>                                                           |
| <span data-ttu-id="b742f-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b742f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b742f-230">True</span><span class="sxs-lookup"><span data-stu-id="b742f-230">True</span></span>                                                            |
| <span data-ttu-id="b742f-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b742f-231">Is Indexed</span></span>             | <span data-ttu-id="b742f-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-232">False</span></span>                                                           |
| <span data-ttu-id="b742f-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b742f-233">In Global Catalog</span></span>      | <span data-ttu-id="b742f-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="b742f-234">False</span></span>                                                           |
| <span data-ttu-id="b742f-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b742f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b742f-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b742f-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b742f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b742f-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b742f-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="b742f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-239">Search-Flags</span></span>           | <span data-ttu-id="b742f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b742f-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="b742f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b742f-241">System-Flags</span></span>           | <span data-ttu-id="b742f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b742f-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="b742f-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b742f-243">Classes used in</span></span>        | [<span data-ttu-id="b742f-244">**MS-IEEE-80211 — политика**</span><span class="sxs-lookup"><span data-stu-id="b742f-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 





