---
title: Атрибут политики на уровне домена
description: Это предназначено для репликации пользовательской политики на клиентах.
ms.assetid: 930a2733-31c4-45de-a611-437e3d61d304
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута политики на уровне домена
- Схема AD атрибута Домаинвидеполици
topic_type:
- apiref
api_name:
- Domain-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc732ee761ee6c294ffb14dac832c36d5821927
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804337"
---
# <a name="domain-wide-policy-attribute"></a><span data-ttu-id="c9db9-105">Атрибут политики на уровне домена</span><span class="sxs-lookup"><span data-stu-id="c9db9-105">Domain-Wide-Policy attribute</span></span>

<span data-ttu-id="c9db9-106">Это предназначено для репликации пользовательской политики на клиентах.</span><span class="sxs-lookup"><span data-stu-id="c9db9-106">This is for user extensible policy to be replicated to the clients.</span></span>



| <span data-ttu-id="c9db9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-107">Entry</span></span> | <span data-ttu-id="c9db9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c9db9-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9db9-109">CN</span></span>                | <span data-ttu-id="c9db9-110">Политика на уровне домена</span><span class="sxs-lookup"><span data-stu-id="c9db9-110">Domain-Wide-Policy</span></span>                                    |
| <span data-ttu-id="c9db9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c9db9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9db9-112">домаинвидеполици</span><span class="sxs-lookup"><span data-stu-id="c9db9-112">domainWidePolicy</span></span>                                      |
| <span data-ttu-id="c9db9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c9db9-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c9db9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c9db9-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c9db9-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c9db9-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c9db9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-116">Attribute-Id</span></span>      | <span data-ttu-id="c9db9-117">1.2.840.113556.1.4.421</span><span class="sxs-lookup"><span data-stu-id="c9db9-117">1.2.840.113556.1.4.421</span></span>                                |
| <span data-ttu-id="c9db9-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c9db9-118">System-Id-Guid</span></span>    | <span data-ttu-id="c9db9-119">80a67e29-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c9db9-119">80a67e29-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="c9db9-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9db9-120">Syntax</span></span>            | [<span data-ttu-id="c9db9-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="c9db9-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c9db9-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c9db9-122">Implementations</span></span>

-   [<span data-ttu-id="c9db9-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9db9-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9db9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9db9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9db9-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9db9-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9db9-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9db9-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9db9-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9db9-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9db9-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9db9-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9db9-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9db9-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c9db9-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-130">Entry</span></span> | <span data-ttu-id="c9db9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="c9db9-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9db9-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9db9-134">System-Only</span></span>            | <span data-ttu-id="c9db9-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-135">False</span></span>                                              |
| <span data-ttu-id="c9db9-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9db9-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c9db9-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-137">False</span></span>                                              |
| <span data-ttu-id="c9db9-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9db9-138">Is Indexed</span></span>             | <span data-ttu-id="c9db9-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-139">False</span></span>                                              |
| <span data-ttu-id="c9db9-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9db9-140">In Global Catalog</span></span>      | <span data-ttu-id="c9db9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-141">False</span></span>                                              |
| <span data-ttu-id="c9db9-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9db9-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9db9-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9db9-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="c9db9-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9db9-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9db9-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-146">Search-Flags</span></span>           | <span data-ttu-id="c9db9-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9db9-147">0x00000000</span></span>                                         |
| <span data-ttu-id="c9db9-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-148">System-Flags</span></span>           | <span data-ttu-id="c9db9-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9db9-149">0x00000010</span></span>                                         |
| <span data-ttu-id="c9db9-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9db9-150">Classes used in</span></span>        | [<span data-ttu-id="c9db9-151">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c9db9-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9db9-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9db9-152">Windows Server 2003</span></span>



| <span data-ttu-id="c9db9-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-153">Entry</span></span> | <span data-ttu-id="c9db9-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="c9db9-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9db9-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9db9-157">System-Only</span></span>            | <span data-ttu-id="c9db9-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-158">False</span></span>                                              |
| <span data-ttu-id="c9db9-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9db9-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c9db9-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-160">False</span></span>                                              |
| <span data-ttu-id="c9db9-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9db9-161">Is Indexed</span></span>             | <span data-ttu-id="c9db9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-162">False</span></span>                                              |
| <span data-ttu-id="c9db9-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9db9-163">In Global Catalog</span></span>      | <span data-ttu-id="c9db9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-164">False</span></span>                                              |
| <span data-ttu-id="c9db9-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9db9-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9db9-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9db9-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="c9db9-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9db9-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9db9-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-169">Search-Flags</span></span>           | <span data-ttu-id="c9db9-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9db9-170">0x00000000</span></span>                                         |
| <span data-ttu-id="c9db9-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-171">System-Flags</span></span>           | <span data-ttu-id="c9db9-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9db9-172">0x00000010</span></span>                                         |
| <span data-ttu-id="c9db9-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9db9-173">Classes used in</span></span>        | [<span data-ttu-id="c9db9-174">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c9db9-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9db9-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9db9-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9db9-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-176">Entry</span></span> | <span data-ttu-id="c9db9-177">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="c9db9-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9db9-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9db9-180">System-Only</span></span>            | <span data-ttu-id="c9db9-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-181">False</span></span>                                              |
| <span data-ttu-id="c9db9-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9db9-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c9db9-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-183">False</span></span>                                              |
| <span data-ttu-id="c9db9-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9db9-184">Is Indexed</span></span>             | <span data-ttu-id="c9db9-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-185">False</span></span>                                              |
| <span data-ttu-id="c9db9-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9db9-186">In Global Catalog</span></span>      | <span data-ttu-id="c9db9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-187">False</span></span>                                              |
| <span data-ttu-id="c9db9-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9db9-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9db9-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9db9-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="c9db9-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9db9-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9db9-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-192">Search-Flags</span></span>           | <span data-ttu-id="c9db9-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9db9-193">0x00000000</span></span>                                         |
| <span data-ttu-id="c9db9-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-194">System-Flags</span></span>           | <span data-ttu-id="c9db9-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9db9-195">0x00000010</span></span>                                         |
| <span data-ttu-id="c9db9-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9db9-196">Classes used in</span></span>        | [<span data-ttu-id="c9db9-197">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c9db9-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9db9-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9db9-198">Windows Server 2008</span></span>



| <span data-ttu-id="c9db9-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-199">Entry</span></span> | <span data-ttu-id="c9db9-200">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="c9db9-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9db9-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9db9-203">System-Only</span></span>            | <span data-ttu-id="c9db9-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-204">False</span></span>                                              |
| <span data-ttu-id="c9db9-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9db9-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c9db9-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-206">False</span></span>                                              |
| <span data-ttu-id="c9db9-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9db9-207">Is Indexed</span></span>             | <span data-ttu-id="c9db9-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-208">False</span></span>                                              |
| <span data-ttu-id="c9db9-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9db9-209">In Global Catalog</span></span>      | <span data-ttu-id="c9db9-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-210">False</span></span>                                              |
| <span data-ttu-id="c9db9-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9db9-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9db9-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9db9-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="c9db9-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9db9-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9db9-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-215">Search-Flags</span></span>           | <span data-ttu-id="c9db9-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9db9-216">0x00000000</span></span>                                         |
| <span data-ttu-id="c9db9-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-217">System-Flags</span></span>           | <span data-ttu-id="c9db9-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9db9-218">0x00000010</span></span>                                         |
| <span data-ttu-id="c9db9-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9db9-219">Classes used in</span></span>        | [<span data-ttu-id="c9db9-220">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c9db9-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9db9-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9db9-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9db9-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-222">Entry</span></span> | <span data-ttu-id="c9db9-223">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="c9db9-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9db9-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9db9-226">System-Only</span></span>            | <span data-ttu-id="c9db9-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-227">False</span></span>                                              |
| <span data-ttu-id="c9db9-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9db9-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c9db9-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-229">False</span></span>                                              |
| <span data-ttu-id="c9db9-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9db9-230">Is Indexed</span></span>             | <span data-ttu-id="c9db9-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-231">False</span></span>                                              |
| <span data-ttu-id="c9db9-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9db9-232">In Global Catalog</span></span>      | <span data-ttu-id="c9db9-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-233">False</span></span>                                              |
| <span data-ttu-id="c9db9-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9db9-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9db9-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9db9-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="c9db9-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9db9-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9db9-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-238">Search-Flags</span></span>           | <span data-ttu-id="c9db9-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9db9-239">0x00000000</span></span>                                         |
| <span data-ttu-id="c9db9-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-240">System-Flags</span></span>           | <span data-ttu-id="c9db9-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9db9-241">0x00000010</span></span>                                         |
| <span data-ttu-id="c9db9-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9db9-242">Classes used in</span></span>        | [<span data-ttu-id="c9db9-243">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c9db9-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9db9-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9db9-244">Windows Server 2012</span></span>



| <span data-ttu-id="c9db9-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="c9db9-245">Entry</span></span> | <span data-ttu-id="c9db9-246">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db9-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="c9db9-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c9db9-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9db9-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="c9db9-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9db9-249">System-Only</span></span>            | <span data-ttu-id="c9db9-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-250">False</span></span>                                              |
| <span data-ttu-id="c9db9-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c9db9-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c9db9-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-252">False</span></span>                                              |
| <span data-ttu-id="c9db9-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c9db9-253">Is Indexed</span></span>             | <span data-ttu-id="c9db9-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-254">False</span></span>                                              |
| <span data-ttu-id="c9db9-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c9db9-255">In Global Catalog</span></span>      | <span data-ttu-id="c9db9-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="c9db9-256">False</span></span>                                              |
| <span data-ttu-id="c9db9-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c9db9-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9db9-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c9db9-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="c9db9-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9db9-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9db9-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="c9db9-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-261">Search-Flags</span></span>           | <span data-ttu-id="c9db9-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9db9-262">0x00000000</span></span>                                         |
| <span data-ttu-id="c9db9-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9db9-263">System-Flags</span></span>           | <span data-ttu-id="c9db9-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9db9-264">0x00000010</span></span>                                         |
| <span data-ttu-id="c9db9-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c9db9-265">Classes used in</span></span>        | [<span data-ttu-id="c9db9-266">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c9db9-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





