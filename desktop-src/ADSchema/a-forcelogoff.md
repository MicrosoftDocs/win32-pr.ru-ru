---
title: Атрибут Force-Logoff
description: Используется для вычисления времени запуска в Самижетаккаунтрестриктионс. Время выхода из системы минус принудительное завершение сеанса равно времени запуска.
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Force-Logoff
- Схема AD атрибута Форцелогофф
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e31cb241cde4deb40d5978594b4354fbcc564b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138170"
---
# <a name="force-logoff-attribute"></a><span data-ttu-id="80b0e-106">Атрибут Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="80b0e-106">Force-Logoff attribute</span></span>

<span data-ttu-id="80b0e-107">Используется для вычисления времени запуска в Самижетаккаунтрестриктионс.</span><span class="sxs-lookup"><span data-stu-id="80b0e-107">Used in computing the kick off time in SamIGetAccountRestrictions.</span></span> <span data-ttu-id="80b0e-108">Время выхода из системы минус принудительное завершение сеанса равно времени запуска.</span><span class="sxs-lookup"><span data-stu-id="80b0e-108">Logoff time minus Force Log off equals kick off time.</span></span>



| <span data-ttu-id="80b0e-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-109">Entry</span></span> | <span data-ttu-id="80b0e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="80b0e-111">CN</span><span class="sxs-lookup"><span data-stu-id="80b0e-111">CN</span></span>                | <span data-ttu-id="80b0e-112">Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="80b0e-112">Force-Logoff</span></span>                         |
| <span data-ttu-id="80b0e-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="80b0e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="80b0e-114">форцелогофф</span><span class="sxs-lookup"><span data-stu-id="80b0e-114">forceLogoff</span></span>                          |
| <span data-ttu-id="80b0e-115">Размер</span><span class="sxs-lookup"><span data-stu-id="80b0e-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="80b0e-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="80b0e-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="80b0e-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="80b0e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="80b0e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-118">Attribute-Id</span></span>      | <span data-ttu-id="80b0e-119">1.2.840.113556.1.4.39</span><span class="sxs-lookup"><span data-stu-id="80b0e-119">1.2.840.113556.1.4.39</span></span>                |
| <span data-ttu-id="80b0e-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="80b0e-120">System-Id-Guid</span></span>    | <span data-ttu-id="80b0e-121">bf967977-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="80b0e-121">bf967977-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="80b0e-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80b0e-122">Syntax</span></span>            | [<span data-ttu-id="80b0e-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="80b0e-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="80b0e-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="80b0e-124">Implementations</span></span>

-   [<span data-ttu-id="80b0e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80b0e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80b0e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80b0e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80b0e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80b0e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80b0e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80b0e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80b0e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80b0e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80b0e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80b0e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80b0e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80b0e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="80b0e-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-132">Entry</span></span> | <span data-ttu-id="80b0e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-133">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b0e-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80b0e-134">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-135">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="80b0e-136">System-Only</span></span>            | <span data-ttu-id="80b0e-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-137">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80b0e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="80b0e-139">True</span><span class="sxs-lookup"><span data-stu-id="80b0e-139">True</span></span>                                                                                                     |
| <span data-ttu-id="80b0e-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80b0e-140">Is Indexed</span></span>             | <span data-ttu-id="80b0e-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-141">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80b0e-142">In Global Catalog</span></span>      | <span data-ttu-id="80b0e-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-143">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80b0e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="80b0e-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80b0e-145">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="80b0e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80b0e-146">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80b0e-147">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-148">Search-Flags</span></span>           | <span data-ttu-id="80b0e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b0e-149">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="80b0e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-150">System-Flags</span></span>           | <span data-ttu-id="80b0e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80b0e-151">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="80b0e-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80b0e-152">Classes used in</span></span>        | [<span data-ttu-id="80b0e-153">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="80b0e-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="80b0e-154">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="80b0e-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80b0e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80b0e-155">Windows Server 2003</span></span>



| <span data-ttu-id="80b0e-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-156">Entry</span></span> | <span data-ttu-id="80b0e-157">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-157">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b0e-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80b0e-158">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-159">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="80b0e-160">System-Only</span></span>            | <span data-ttu-id="80b0e-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-161">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80b0e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="80b0e-163">True</span><span class="sxs-lookup"><span data-stu-id="80b0e-163">True</span></span>                                                                                                     |
| <span data-ttu-id="80b0e-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80b0e-164">Is Indexed</span></span>             | <span data-ttu-id="80b0e-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-165">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80b0e-166">In Global Catalog</span></span>      | <span data-ttu-id="80b0e-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-167">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80b0e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="80b0e-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80b0e-169">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="80b0e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80b0e-170">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80b0e-171">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-172">Search-Flags</span></span>           | <span data-ttu-id="80b0e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b0e-173">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="80b0e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-174">System-Flags</span></span>           | <span data-ttu-id="80b0e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80b0e-175">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="80b0e-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80b0e-176">Classes used in</span></span>        | [<span data-ttu-id="80b0e-177">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="80b0e-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="80b0e-178">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="80b0e-178">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80b0e-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80b0e-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80b0e-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-180">Entry</span></span> | <span data-ttu-id="80b0e-181">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-181">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b0e-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80b0e-182">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-183">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="80b0e-184">System-Only</span></span>            | <span data-ttu-id="80b0e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-185">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80b0e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="80b0e-187">True</span><span class="sxs-lookup"><span data-stu-id="80b0e-187">True</span></span>                                                                                                     |
| <span data-ttu-id="80b0e-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80b0e-188">Is Indexed</span></span>             | <span data-ttu-id="80b0e-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-189">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80b0e-190">In Global Catalog</span></span>      | <span data-ttu-id="80b0e-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-191">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80b0e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="80b0e-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80b0e-193">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="80b0e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80b0e-194">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80b0e-195">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-196">Search-Flags</span></span>           | <span data-ttu-id="80b0e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b0e-197">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="80b0e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-198">System-Flags</span></span>           | <span data-ttu-id="80b0e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80b0e-199">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="80b0e-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80b0e-200">Classes used in</span></span>        | [<span data-ttu-id="80b0e-201">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="80b0e-201">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="80b0e-202">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="80b0e-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80b0e-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80b0e-203">Windows Server 2008</span></span>



| <span data-ttu-id="80b0e-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-204">Entry</span></span> | <span data-ttu-id="80b0e-205">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-205">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b0e-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80b0e-206">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-207">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="80b0e-208">System-Only</span></span>            | <span data-ttu-id="80b0e-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-209">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80b0e-210">Is-Single-Valued</span></span>       | <span data-ttu-id="80b0e-211">True</span><span class="sxs-lookup"><span data-stu-id="80b0e-211">True</span></span>                                                                                                     |
| <span data-ttu-id="80b0e-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80b0e-212">Is Indexed</span></span>             | <span data-ttu-id="80b0e-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-213">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80b0e-214">In Global Catalog</span></span>      | <span data-ttu-id="80b0e-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-215">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80b0e-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="80b0e-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80b0e-217">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="80b0e-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80b0e-218">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80b0e-219">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-220">Search-Flags</span></span>           | <span data-ttu-id="80b0e-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b0e-221">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="80b0e-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-222">System-Flags</span></span>           | <span data-ttu-id="80b0e-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80b0e-223">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="80b0e-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80b0e-224">Classes used in</span></span>        | [<span data-ttu-id="80b0e-225">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="80b0e-225">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="80b0e-226">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="80b0e-226">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80b0e-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80b0e-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80b0e-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-228">Entry</span></span> | <span data-ttu-id="80b0e-229">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-229">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b0e-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80b0e-230">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-231">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="80b0e-232">System-Only</span></span>            | <span data-ttu-id="80b0e-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-233">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80b0e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="80b0e-235">True</span><span class="sxs-lookup"><span data-stu-id="80b0e-235">True</span></span>                                                                                                     |
| <span data-ttu-id="80b0e-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80b0e-236">Is Indexed</span></span>             | <span data-ttu-id="80b0e-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-237">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80b0e-238">In Global Catalog</span></span>      | <span data-ttu-id="80b0e-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-239">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80b0e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="80b0e-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80b0e-241">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="80b0e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80b0e-242">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80b0e-243">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-244">Search-Flags</span></span>           | <span data-ttu-id="80b0e-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b0e-245">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="80b0e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-246">System-Flags</span></span>           | <span data-ttu-id="80b0e-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80b0e-247">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="80b0e-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80b0e-248">Classes used in</span></span>        | [<span data-ttu-id="80b0e-249">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="80b0e-249">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="80b0e-250">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="80b0e-250">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80b0e-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80b0e-251">Windows Server 2012</span></span>



| <span data-ttu-id="80b0e-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="80b0e-252">Entry</span></span> | <span data-ttu-id="80b0e-253">Значение</span><span class="sxs-lookup"><span data-stu-id="80b0e-253">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b0e-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80b0e-254">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80b0e-255">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="80b0e-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="80b0e-256">System-Only</span></span>            | <span data-ttu-id="80b0e-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-257">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80b0e-258">Is-Single-Valued</span></span>       | <span data-ttu-id="80b0e-259">True</span><span class="sxs-lookup"><span data-stu-id="80b0e-259">True</span></span>                                                                                                     |
| <span data-ttu-id="80b0e-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80b0e-260">Is Indexed</span></span>             | <span data-ttu-id="80b0e-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-261">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80b0e-262">In Global Catalog</span></span>      | <span data-ttu-id="80b0e-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="80b0e-263">False</span></span>                                                                                                    |
| <span data-ttu-id="80b0e-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80b0e-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="80b0e-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80b0e-265">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="80b0e-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80b0e-266">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80b0e-267">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="80b0e-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-268">Search-Flags</span></span>           | <span data-ttu-id="80b0e-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b0e-269">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="80b0e-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80b0e-270">System-Flags</span></span>           | <span data-ttu-id="80b0e-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80b0e-271">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="80b0e-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80b0e-272">Classes used in</span></span>        | [<span data-ttu-id="80b0e-273">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="80b0e-273">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="80b0e-274">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="80b0e-274">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





