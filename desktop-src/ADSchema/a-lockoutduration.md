---
title: Атрибут Lockout-Duration
description: Время, в течение которого учетная запись блокируется из-за превышения Lockout-Threshold.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Lockout-Duration
- Схема AD атрибута Локкаутдуратион
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654938"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="e0881-105">Атрибут Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="e0881-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="e0881-106">Время, в течение которого учетная запись блокируется из-за превышения [**порога блокировки**](a-lockoutthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="e0881-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="e0881-107">Это значение хранится в виде большого целого числа, представляющего отрицательное число интервалов 100-наносекундных с момента превышения [**порога блокировки**](a-lockoutthreshold.md) , который должен пройти до разблокировки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e0881-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="e0881-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-108">Entry</span></span> | <span data-ttu-id="e0881-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e0881-110">CN</span><span class="sxs-lookup"><span data-stu-id="e0881-110">CN</span></span>                | <span data-ttu-id="e0881-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="e0881-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="e0881-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e0881-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e0881-113">локкаутдуратион</span><span class="sxs-lookup"><span data-stu-id="e0881-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="e0881-114">Размер</span><span class="sxs-lookup"><span data-stu-id="e0881-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="e0881-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e0881-115">Update Privilege</span></span>  | <span data-ttu-id="e0881-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="e0881-116">Domain administrator</span></span>                 |
| <span data-ttu-id="e0881-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e0881-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e0881-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-118">Attribute-Id</span></span>      | <span data-ttu-id="e0881-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="e0881-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="e0881-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e0881-120">System-Id-Guid</span></span>    | <span data-ttu-id="e0881-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e0881-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e0881-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0881-122">Syntax</span></span>            | [<span data-ttu-id="e0881-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="e0881-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e0881-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e0881-124">Implementations</span></span>

-   [<span data-ttu-id="e0881-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e0881-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e0881-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0881-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0881-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0881-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0881-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0881-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0881-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0881-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0881-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0881-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e0881-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0881-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e0881-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-132">Entry</span></span> | <span data-ttu-id="e0881-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0881-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0881-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0881-136">System-Only</span></span>            | <span data-ttu-id="e0881-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0881-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e0881-139">True</span><span class="sxs-lookup"><span data-stu-id="e0881-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="e0881-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0881-140">Is Indexed</span></span>             | <span data-ttu-id="e0881-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0881-142">In Global Catalog</span></span>      | <span data-ttu-id="e0881-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0881-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0881-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0881-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="e0881-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0881-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0881-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-148">Search-Flags</span></span>           | <span data-ttu-id="e0881-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0881-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-150">System-Flags</span></span>           | <span data-ttu-id="e0881-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0881-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0881-152">Classes used in</span></span>        | [<span data-ttu-id="e0881-153">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="e0881-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="e0881-154">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e0881-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="e0881-155">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="e0881-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e0881-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0881-156">Windows Server 2003</span></span>



| <span data-ttu-id="e0881-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-157">Entry</span></span> | <span data-ttu-id="e0881-158">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0881-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0881-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0881-161">System-Only</span></span>            | <span data-ttu-id="e0881-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0881-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e0881-164">True</span><span class="sxs-lookup"><span data-stu-id="e0881-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="e0881-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0881-165">Is Indexed</span></span>             | <span data-ttu-id="e0881-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0881-167">In Global Catalog</span></span>      | <span data-ttu-id="e0881-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0881-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0881-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0881-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="e0881-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0881-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0881-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-173">Search-Flags</span></span>           | <span data-ttu-id="e0881-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0881-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-175">System-Flags</span></span>           | <span data-ttu-id="e0881-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0881-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0881-177">Classes used in</span></span>        | [<span data-ttu-id="e0881-178">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="e0881-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="e0881-179">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e0881-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="e0881-180">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="e0881-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0881-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0881-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0881-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-182">Entry</span></span> | <span data-ttu-id="e0881-183">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0881-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0881-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0881-186">System-Only</span></span>            | <span data-ttu-id="e0881-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0881-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e0881-189">True</span><span class="sxs-lookup"><span data-stu-id="e0881-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="e0881-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0881-190">Is Indexed</span></span>             | <span data-ttu-id="e0881-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0881-192">In Global Catalog</span></span>      | <span data-ttu-id="e0881-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0881-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0881-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0881-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="e0881-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0881-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0881-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-198">Search-Flags</span></span>           | <span data-ttu-id="e0881-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0881-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-200">System-Flags</span></span>           | <span data-ttu-id="e0881-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0881-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0881-202">Classes used in</span></span>        | [<span data-ttu-id="e0881-203">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="e0881-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="e0881-204">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e0881-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="e0881-205">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="e0881-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0881-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0881-206">Windows Server 2008</span></span>



| <span data-ttu-id="e0881-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-207">Entry</span></span> | <span data-ttu-id="e0881-208">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0881-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0881-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0881-211">System-Only</span></span>            | <span data-ttu-id="e0881-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0881-213">Is-Single-Valued</span></span>       | <span data-ttu-id="e0881-214">True</span><span class="sxs-lookup"><span data-stu-id="e0881-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="e0881-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0881-215">Is Indexed</span></span>             | <span data-ttu-id="e0881-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0881-217">In Global Catalog</span></span>      | <span data-ttu-id="e0881-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0881-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0881-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0881-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="e0881-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0881-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0881-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-223">Search-Flags</span></span>           | <span data-ttu-id="e0881-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0881-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-225">System-Flags</span></span>           | <span data-ttu-id="e0881-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0881-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0881-227">Classes used in</span></span>        | [<span data-ttu-id="e0881-228">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="e0881-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="e0881-229">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e0881-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="e0881-230">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="e0881-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0881-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0881-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0881-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-232">Entry</span></span> | <span data-ttu-id="e0881-233">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0881-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0881-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0881-236">System-Only</span></span>            | <span data-ttu-id="e0881-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0881-238">Is-Single-Valued</span></span>       | <span data-ttu-id="e0881-239">True</span><span class="sxs-lookup"><span data-stu-id="e0881-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="e0881-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0881-240">Is Indexed</span></span>             | <span data-ttu-id="e0881-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0881-242">In Global Catalog</span></span>      | <span data-ttu-id="e0881-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0881-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0881-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0881-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="e0881-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0881-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0881-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-248">Search-Flags</span></span>           | <span data-ttu-id="e0881-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0881-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-250">System-Flags</span></span>           | <span data-ttu-id="e0881-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0881-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0881-252">Classes used in</span></span>        | [<span data-ttu-id="e0881-253">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="e0881-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="e0881-254">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e0881-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="e0881-255">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="e0881-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0881-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0881-256">Windows Server 2012</span></span>



| <span data-ttu-id="e0881-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0881-257">Entry</span></span> | <span data-ttu-id="e0881-258">Значение</span><span class="sxs-lookup"><span data-stu-id="e0881-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0881-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0881-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0881-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0881-261">System-Only</span></span>            | <span data-ttu-id="e0881-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0881-263">Is-Single-Valued</span></span>       | <span data-ttu-id="e0881-264">True</span><span class="sxs-lookup"><span data-stu-id="e0881-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="e0881-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0881-265">Is Indexed</span></span>             | <span data-ttu-id="e0881-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0881-267">In Global Catalog</span></span>      | <span data-ttu-id="e0881-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0881-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="e0881-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0881-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0881-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0881-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="e0881-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0881-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0881-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="e0881-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-273">Search-Flags</span></span>           | <span data-ttu-id="e0881-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0881-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0881-275">System-Flags</span></span>           | <span data-ttu-id="e0881-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0881-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="e0881-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0881-277">Classes used in</span></span>        | [<span data-ttu-id="e0881-278">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="e0881-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="e0881-279">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e0881-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="e0881-280">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="e0881-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="e0881-281">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0881-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0881-282">**Порог блокировки**</span><span class="sxs-lookup"><span data-stu-id="e0881-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





