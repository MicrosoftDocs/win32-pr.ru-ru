---
title: Атрибут Lockout-Threshold
description: Число недопустимых попыток входа в систему, которые разрешены до блокировки учетной записи.
ms.assetid: c4dcbbb6-0680-45f3-9b0b-f9c4bbf2b349
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Lockout-Threshold
- Схема AD атрибута lockoutThreshold
topic_type:
- apiref
api_name:
- Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345977055597c48d70e30a20ce9bfbc9f07f3929
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893081"
---
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="51fc5-105">Атрибут Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="51fc5-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="51fc5-106">Число недопустимых попыток входа в систему, которые разрешены до блокировки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="51fc5-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="51fc5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-107">Entry</span></span> | <span data-ttu-id="51fc5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="51fc5-109">CN</span><span class="sxs-lookup"><span data-stu-id="51fc5-109">CN</span></span>                | <span data-ttu-id="51fc5-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="51fc5-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="51fc5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="51fc5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="51fc5-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="51fc5-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="51fc5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="51fc5-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="51fc5-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="51fc5-114">Update Privilege</span></span>  | <span data-ttu-id="51fc5-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="51fc5-115">Domain administrator</span></span>                 |
| <span data-ttu-id="51fc5-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="51fc5-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="51fc5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-117">Attribute-Id</span></span>      | <span data-ttu-id="51fc5-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="51fc5-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="51fc5-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="51fc5-119">System-Id-Guid</span></span>    | <span data-ttu-id="51fc5-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="51fc5-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="51fc5-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51fc5-121">Syntax</span></span>            | [<span data-ttu-id="51fc5-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="51fc5-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="51fc5-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="51fc5-123">Implementations</span></span>

-   [<span data-ttu-id="51fc5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51fc5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51fc5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51fc5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51fc5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51fc5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51fc5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51fc5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51fc5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51fc5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51fc5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51fc5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51fc5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51fc5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="51fc5-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-131">Entry</span></span> | <span data-ttu-id="51fc5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fc5-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51fc5-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="51fc5-135">System-Only</span></span>            | <span data-ttu-id="51fc5-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51fc5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="51fc5-138">True</span><span class="sxs-lookup"><span data-stu-id="51fc5-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="51fc5-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51fc5-139">Is Indexed</span></span>             | <span data-ttu-id="51fc5-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51fc5-141">In Global Catalog</span></span>      | <span data-ttu-id="51fc5-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51fc5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="51fc5-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51fc5-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="51fc5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51fc5-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51fc5-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-147">Search-Flags</span></span>           | <span data-ttu-id="51fc5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51fc5-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-149">System-Flags</span></span>           | <span data-ttu-id="51fc5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51fc5-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51fc5-151">Classes used in</span></span>        | [<span data-ttu-id="51fc5-152">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="51fc5-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="51fc5-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="51fc5-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="51fc5-154">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="51fc5-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51fc5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51fc5-155">Windows Server 2003</span></span>



| <span data-ttu-id="51fc5-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-156">Entry</span></span> | <span data-ttu-id="51fc5-157">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fc5-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51fc5-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="51fc5-160">System-Only</span></span>            | <span data-ttu-id="51fc5-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51fc5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="51fc5-163">True</span><span class="sxs-lookup"><span data-stu-id="51fc5-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="51fc5-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51fc5-164">Is Indexed</span></span>             | <span data-ttu-id="51fc5-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51fc5-166">In Global Catalog</span></span>      | <span data-ttu-id="51fc5-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51fc5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="51fc5-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51fc5-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="51fc5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51fc5-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51fc5-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-172">Search-Flags</span></span>           | <span data-ttu-id="51fc5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51fc5-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-174">System-Flags</span></span>           | <span data-ttu-id="51fc5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51fc5-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51fc5-176">Classes used in</span></span>        | [<span data-ttu-id="51fc5-177">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="51fc5-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="51fc5-178">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="51fc5-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="51fc5-179">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="51fc5-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51fc5-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51fc5-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51fc5-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-181">Entry</span></span> | <span data-ttu-id="51fc5-182">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fc5-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51fc5-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="51fc5-185">System-Only</span></span>            | <span data-ttu-id="51fc5-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51fc5-187">Is-Single-Valued</span></span>       | <span data-ttu-id="51fc5-188">True</span><span class="sxs-lookup"><span data-stu-id="51fc5-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="51fc5-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51fc5-189">Is Indexed</span></span>             | <span data-ttu-id="51fc5-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51fc5-191">In Global Catalog</span></span>      | <span data-ttu-id="51fc5-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51fc5-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="51fc5-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51fc5-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="51fc5-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51fc5-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51fc5-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-197">Search-Flags</span></span>           | <span data-ttu-id="51fc5-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51fc5-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-199">System-Flags</span></span>           | <span data-ttu-id="51fc5-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51fc5-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51fc5-201">Classes used in</span></span>        | [<span data-ttu-id="51fc5-202">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="51fc5-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="51fc5-203">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="51fc5-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="51fc5-204">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="51fc5-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51fc5-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51fc5-205">Windows Server 2008</span></span>



| <span data-ttu-id="51fc5-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-206">Entry</span></span> | <span data-ttu-id="51fc5-207">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fc5-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51fc5-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="51fc5-210">System-Only</span></span>            | <span data-ttu-id="51fc5-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51fc5-212">Is-Single-Valued</span></span>       | <span data-ttu-id="51fc5-213">True</span><span class="sxs-lookup"><span data-stu-id="51fc5-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="51fc5-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51fc5-214">Is Indexed</span></span>             | <span data-ttu-id="51fc5-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51fc5-216">In Global Catalog</span></span>      | <span data-ttu-id="51fc5-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51fc5-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="51fc5-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51fc5-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="51fc5-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51fc5-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51fc5-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-222">Search-Flags</span></span>           | <span data-ttu-id="51fc5-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51fc5-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-224">System-Flags</span></span>           | <span data-ttu-id="51fc5-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51fc5-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51fc5-226">Classes used in</span></span>        | [<span data-ttu-id="51fc5-227">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="51fc5-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="51fc5-228">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="51fc5-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="51fc5-229">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="51fc5-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51fc5-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51fc5-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51fc5-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-231">Entry</span></span> | <span data-ttu-id="51fc5-232">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fc5-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51fc5-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="51fc5-235">System-Only</span></span>            | <span data-ttu-id="51fc5-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51fc5-237">Is-Single-Valued</span></span>       | <span data-ttu-id="51fc5-238">True</span><span class="sxs-lookup"><span data-stu-id="51fc5-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="51fc5-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51fc5-239">Is Indexed</span></span>             | <span data-ttu-id="51fc5-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51fc5-241">In Global Catalog</span></span>      | <span data-ttu-id="51fc5-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51fc5-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="51fc5-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51fc5-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="51fc5-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51fc5-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51fc5-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-247">Search-Flags</span></span>           | <span data-ttu-id="51fc5-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51fc5-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-249">System-Flags</span></span>           | <span data-ttu-id="51fc5-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51fc5-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51fc5-251">Classes used in</span></span>        | [<span data-ttu-id="51fc5-252">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="51fc5-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="51fc5-253">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="51fc5-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="51fc5-254">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="51fc5-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51fc5-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51fc5-255">Windows Server 2012</span></span>



| <span data-ttu-id="51fc5-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="51fc5-256">Entry</span></span> | <span data-ttu-id="51fc5-257">Значение</span><span class="sxs-lookup"><span data-stu-id="51fc5-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fc5-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51fc5-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51fc5-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="51fc5-260">System-Only</span></span>            | <span data-ttu-id="51fc5-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51fc5-262">Is-Single-Valued</span></span>       | <span data-ttu-id="51fc5-263">True</span><span class="sxs-lookup"><span data-stu-id="51fc5-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="51fc5-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51fc5-264">Is Indexed</span></span>             | <span data-ttu-id="51fc5-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51fc5-266">In Global Catalog</span></span>      | <span data-ttu-id="51fc5-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="51fc5-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="51fc5-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51fc5-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="51fc5-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51fc5-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="51fc5-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51fc5-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51fc5-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="51fc5-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-272">Search-Flags</span></span>           | <span data-ttu-id="51fc5-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51fc5-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51fc5-274">System-Flags</span></span>           | <span data-ttu-id="51fc5-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51fc5-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="51fc5-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51fc5-276">Classes used in</span></span>        | [<span data-ttu-id="51fc5-277">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="51fc5-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="51fc5-278">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="51fc5-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="51fc5-279">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="51fc5-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="51fc5-280">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51fc5-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fc5-281">**Продолжительность блокировки**</span><span class="sxs-lookup"><span data-stu-id="51fc5-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





