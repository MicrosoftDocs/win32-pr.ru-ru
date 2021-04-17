---
title: Атрибут "ACS" — "Статистическая обработка"-частота "на пользователя"
description: Максимальная частота маркеров, которую любой пользователь может иметь для всех потоков.
ms.assetid: a617dce4-bade-40bb-ad99-6025e85bfac5
ms.tgt_platform: multiple
keywords:
- ACS-Статистическая обработка-токен-Rate-схема AD атрибута на пользователя
- Схема AD атрибута Аксаггрегатетокенратеперусер
topic_type:
- apiref
api_name:
- ACS-Aggregate-Token-Rate-Per-User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db1a614e4e2a547d7922bcf47d026337b5e1ba94
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655516"
---
# <a name="acs-aggregate-token-rate-per-user-attribute"></a><span data-ttu-id="91ffc-105">Атрибут "ACS" — "Статистическая обработка"-частота "на пользователя"</span><span class="sxs-lookup"><span data-stu-id="91ffc-105">ACS-Aggregate-Token-Rate-Per-User attribute</span></span>

<span data-ttu-id="91ffc-106">Максимальная частота маркеров, которую любой пользователь может иметь для всех потоков.</span><span class="sxs-lookup"><span data-stu-id="91ffc-106">The maximum token rate any user may have for all flows.</span></span>



| <span data-ttu-id="91ffc-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-107">Entry</span></span> | <span data-ttu-id="91ffc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="91ffc-109">CN</span><span class="sxs-lookup"><span data-stu-id="91ffc-109">CN</span></span>                | <span data-ttu-id="91ffc-110">ACS-агрегирование-частота маркеров на пользователя</span><span class="sxs-lookup"><span data-stu-id="91ffc-110">ACS-Aggregate-Token-Rate-Per-User</span></span>    |
| <span data-ttu-id="91ffc-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="91ffc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="91ffc-112">аксаггрегатетокенратеперусер</span><span class="sxs-lookup"><span data-stu-id="91ffc-112">aCSAggregateTokenRatePerUser</span></span>         |
| <span data-ttu-id="91ffc-113">Размер</span><span class="sxs-lookup"><span data-stu-id="91ffc-113">Size</span></span>              | <span data-ttu-id="91ffc-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="91ffc-114">8 bytes</span></span>                              |
| <span data-ttu-id="91ffc-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="91ffc-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="91ffc-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="91ffc-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="91ffc-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-117">Attribute-Id</span></span>      | <span data-ttu-id="91ffc-118">1.2.840.113556.1.4.760</span><span class="sxs-lookup"><span data-stu-id="91ffc-118">1.2.840.113556.1.4.760</span></span>               |
| <span data-ttu-id="91ffc-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="91ffc-119">System-Id-Guid</span></span>    | <span data-ttu-id="91ffc-120">7f56127d-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="91ffc-120">7f56127d-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="91ffc-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91ffc-121">Syntax</span></span>            | [<span data-ttu-id="91ffc-122">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="91ffc-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="91ffc-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="91ffc-123">Implementations</span></span>

-   [<span data-ttu-id="91ffc-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="91ffc-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="91ffc-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91ffc-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91ffc-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91ffc-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91ffc-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91ffc-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91ffc-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91ffc-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91ffc-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91ffc-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="91ffc-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91ffc-130">Windows 2000 Server</span></span>



| <span data-ttu-id="91ffc-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-131">Entry</span></span> | <span data-ttu-id="91ffc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="91ffc-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91ffc-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="91ffc-135">System-Only</span></span>            | <span data-ttu-id="91ffc-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-136">False</span></span>                                        |
| <span data-ttu-id="91ffc-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91ffc-137">Is-Single-Valued</span></span>       | <span data-ttu-id="91ffc-138">True</span><span class="sxs-lookup"><span data-stu-id="91ffc-138">True</span></span>                                         |
| <span data-ttu-id="91ffc-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91ffc-139">Is Indexed</span></span>             | <span data-ttu-id="91ffc-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-140">False</span></span>                                        |
| <span data-ttu-id="91ffc-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91ffc-141">In Global Catalog</span></span>      | <span data-ttu-id="91ffc-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-142">False</span></span>                                        |
| <span data-ttu-id="91ffc-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91ffc-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="91ffc-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91ffc-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="91ffc-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91ffc-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91ffc-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-147">Search-Flags</span></span>           | <span data-ttu-id="91ffc-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91ffc-148">0x00000000</span></span>                                   |
| <span data-ttu-id="91ffc-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-149">System-Flags</span></span>           | <span data-ttu-id="91ffc-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91ffc-150">0x00000010</span></span>                                   |
| <span data-ttu-id="91ffc-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91ffc-151">Classes used in</span></span>        | [<span data-ttu-id="91ffc-152">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="91ffc-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="91ffc-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91ffc-153">Windows Server 2003</span></span>



| <span data-ttu-id="91ffc-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-154">Entry</span></span> | <span data-ttu-id="91ffc-155">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="91ffc-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91ffc-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="91ffc-158">System-Only</span></span>            | <span data-ttu-id="91ffc-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-159">False</span></span>                                        |
| <span data-ttu-id="91ffc-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91ffc-160">Is-Single-Valued</span></span>       | <span data-ttu-id="91ffc-161">True</span><span class="sxs-lookup"><span data-stu-id="91ffc-161">True</span></span>                                         |
| <span data-ttu-id="91ffc-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91ffc-162">Is Indexed</span></span>             | <span data-ttu-id="91ffc-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-163">False</span></span>                                        |
| <span data-ttu-id="91ffc-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91ffc-164">In Global Catalog</span></span>      | <span data-ttu-id="91ffc-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-165">False</span></span>                                        |
| <span data-ttu-id="91ffc-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91ffc-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="91ffc-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91ffc-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="91ffc-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91ffc-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91ffc-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-170">Search-Flags</span></span>           | <span data-ttu-id="91ffc-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91ffc-171">0x00000000</span></span>                                   |
| <span data-ttu-id="91ffc-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-172">System-Flags</span></span>           | <span data-ttu-id="91ffc-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91ffc-173">0x00000010</span></span>                                   |
| <span data-ttu-id="91ffc-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91ffc-174">Classes used in</span></span>        | [<span data-ttu-id="91ffc-175">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="91ffc-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91ffc-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91ffc-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91ffc-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-177">Entry</span></span> | <span data-ttu-id="91ffc-178">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="91ffc-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91ffc-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="91ffc-181">System-Only</span></span>            | <span data-ttu-id="91ffc-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-182">False</span></span>                                        |
| <span data-ttu-id="91ffc-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91ffc-183">Is-Single-Valued</span></span>       | <span data-ttu-id="91ffc-184">True</span><span class="sxs-lookup"><span data-stu-id="91ffc-184">True</span></span>                                         |
| <span data-ttu-id="91ffc-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91ffc-185">Is Indexed</span></span>             | <span data-ttu-id="91ffc-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-186">False</span></span>                                        |
| <span data-ttu-id="91ffc-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91ffc-187">In Global Catalog</span></span>      | <span data-ttu-id="91ffc-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-188">False</span></span>                                        |
| <span data-ttu-id="91ffc-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91ffc-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="91ffc-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91ffc-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="91ffc-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91ffc-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91ffc-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-193">Search-Flags</span></span>           | <span data-ttu-id="91ffc-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91ffc-194">0x00000000</span></span>                                   |
| <span data-ttu-id="91ffc-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-195">System-Flags</span></span>           | <span data-ttu-id="91ffc-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91ffc-196">0x00000010</span></span>                                   |
| <span data-ttu-id="91ffc-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91ffc-197">Classes used in</span></span>        | [<span data-ttu-id="91ffc-198">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="91ffc-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91ffc-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91ffc-199">Windows Server 2008</span></span>



| <span data-ttu-id="91ffc-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-200">Entry</span></span> | <span data-ttu-id="91ffc-201">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="91ffc-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91ffc-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="91ffc-204">System-Only</span></span>            | <span data-ttu-id="91ffc-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-205">False</span></span>                                        |
| <span data-ttu-id="91ffc-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91ffc-206">Is-Single-Valued</span></span>       | <span data-ttu-id="91ffc-207">True</span><span class="sxs-lookup"><span data-stu-id="91ffc-207">True</span></span>                                         |
| <span data-ttu-id="91ffc-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91ffc-208">Is Indexed</span></span>             | <span data-ttu-id="91ffc-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-209">False</span></span>                                        |
| <span data-ttu-id="91ffc-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91ffc-210">In Global Catalog</span></span>      | <span data-ttu-id="91ffc-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-211">False</span></span>                                        |
| <span data-ttu-id="91ffc-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91ffc-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="91ffc-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91ffc-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="91ffc-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91ffc-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91ffc-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-216">Search-Flags</span></span>           | <span data-ttu-id="91ffc-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91ffc-217">0x00000000</span></span>                                   |
| <span data-ttu-id="91ffc-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-218">System-Flags</span></span>           | <span data-ttu-id="91ffc-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91ffc-219">0x00000010</span></span>                                   |
| <span data-ttu-id="91ffc-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91ffc-220">Classes used in</span></span>        | [<span data-ttu-id="91ffc-221">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="91ffc-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91ffc-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91ffc-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91ffc-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-223">Entry</span></span> | <span data-ttu-id="91ffc-224">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="91ffc-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91ffc-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="91ffc-227">System-Only</span></span>            | <span data-ttu-id="91ffc-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-228">False</span></span>                                        |
| <span data-ttu-id="91ffc-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91ffc-229">Is-Single-Valued</span></span>       | <span data-ttu-id="91ffc-230">True</span><span class="sxs-lookup"><span data-stu-id="91ffc-230">True</span></span>                                         |
| <span data-ttu-id="91ffc-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91ffc-231">Is Indexed</span></span>             | <span data-ttu-id="91ffc-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-232">False</span></span>                                        |
| <span data-ttu-id="91ffc-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91ffc-233">In Global Catalog</span></span>      | <span data-ttu-id="91ffc-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-234">False</span></span>                                        |
| <span data-ttu-id="91ffc-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91ffc-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="91ffc-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91ffc-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="91ffc-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91ffc-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91ffc-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-239">Search-Flags</span></span>           | <span data-ttu-id="91ffc-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91ffc-240">0x00000000</span></span>                                   |
| <span data-ttu-id="91ffc-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-241">System-Flags</span></span>           | <span data-ttu-id="91ffc-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91ffc-242">0x00000010</span></span>                                   |
| <span data-ttu-id="91ffc-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91ffc-243">Classes used in</span></span>        | [<span data-ttu-id="91ffc-244">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="91ffc-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91ffc-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91ffc-245">Windows Server 2012</span></span>



| <span data-ttu-id="91ffc-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="91ffc-246">Entry</span></span> | <span data-ttu-id="91ffc-247">Значение</span><span class="sxs-lookup"><span data-stu-id="91ffc-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="91ffc-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="91ffc-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91ffc-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="91ffc-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="91ffc-250">System-Only</span></span>            | <span data-ttu-id="91ffc-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-251">False</span></span>                                        |
| <span data-ttu-id="91ffc-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="91ffc-252">Is-Single-Valued</span></span>       | <span data-ttu-id="91ffc-253">True</span><span class="sxs-lookup"><span data-stu-id="91ffc-253">True</span></span>                                         |
| <span data-ttu-id="91ffc-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="91ffc-254">Is Indexed</span></span>             | <span data-ttu-id="91ffc-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-255">False</span></span>                                        |
| <span data-ttu-id="91ffc-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="91ffc-256">In Global Catalog</span></span>      | <span data-ttu-id="91ffc-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="91ffc-257">False</span></span>                                        |
| <span data-ttu-id="91ffc-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="91ffc-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="91ffc-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91ffc-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="91ffc-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91ffc-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91ffc-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="91ffc-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-262">Search-Flags</span></span>           | <span data-ttu-id="91ffc-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91ffc-263">0x00000000</span></span>                                   |
| <span data-ttu-id="91ffc-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91ffc-264">System-Flags</span></span>           | <span data-ttu-id="91ffc-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91ffc-265">0x00000010</span></span>                                   |
| <span data-ttu-id="91ffc-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="91ffc-266">Classes used in</span></span>        | [<span data-ttu-id="91ffc-267">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="91ffc-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





