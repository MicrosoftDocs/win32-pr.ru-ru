---
title: Атрибут max-продлить возраст
description: Этот атрибут определяет период времени (в днях), в течение которого можно продлить билет предоставления билета (TGT) для проверки подлинности Kerberos. Значение по умолчанию — 7 дней в объекте групповая политика домена по умолчанию (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Max-продлить Age
- Схема AD атрибута Максреневаже
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654927"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="cfc71-106">Атрибут max-продлить возраст</span><span class="sxs-lookup"><span data-stu-id="cfc71-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="cfc71-107">Этот атрибут определяет период времени (в днях), в течение которого можно продлить билет предоставления билета (TGT) для проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="cfc71-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="cfc71-108">Значение по умолчанию — 7 дней в объекте групповая политика домена по умолчанию (GPO).</span><span class="sxs-lookup"><span data-stu-id="cfc71-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="cfc71-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-109">Entry</span></span> | <span data-ttu-id="cfc71-110">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cfc71-111">CN</span><span class="sxs-lookup"><span data-stu-id="cfc71-111">CN</span></span>                | <span data-ttu-id="cfc71-112">Max-продление — возраст</span><span class="sxs-lookup"><span data-stu-id="cfc71-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="cfc71-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cfc71-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cfc71-114">максреневаже</span><span class="sxs-lookup"><span data-stu-id="cfc71-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="cfc71-115">Размер</span><span class="sxs-lookup"><span data-stu-id="cfc71-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="cfc71-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cfc71-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cfc71-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cfc71-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cfc71-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-118">Attribute-Id</span></span>      | <span data-ttu-id="cfc71-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="cfc71-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="cfc71-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cfc71-120">System-Id-Guid</span></span>    | <span data-ttu-id="cfc71-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cfc71-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="cfc71-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfc71-122">Syntax</span></span>            | [<span data-ttu-id="cfc71-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="cfc71-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="cfc71-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cfc71-124">Implementations</span></span>

-   [<span data-ttu-id="cfc71-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cfc71-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cfc71-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cfc71-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cfc71-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cfc71-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cfc71-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cfc71-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cfc71-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cfc71-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cfc71-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cfc71-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cfc71-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cfc71-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cfc71-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-132">Entry</span></span> | <span data-ttu-id="cfc71-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cfc71-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cfc71-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfc71-136">System-Only</span></span>            | <span data-ttu-id="cfc71-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-137">False</span></span>                                              |
| <span data-ttu-id="cfc71-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cfc71-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cfc71-139">True</span><span class="sxs-lookup"><span data-stu-id="cfc71-139">True</span></span>                                               |
| <span data-ttu-id="cfc71-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cfc71-140">Is Indexed</span></span>             | <span data-ttu-id="cfc71-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-141">False</span></span>                                              |
| <span data-ttu-id="cfc71-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cfc71-142">In Global Catalog</span></span>      | <span data-ttu-id="cfc71-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-143">False</span></span>                                              |
| <span data-ttu-id="cfc71-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfc71-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfc71-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfc71-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cfc71-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfc71-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfc71-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-148">Search-Flags</span></span>           | <span data-ttu-id="cfc71-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfc71-149">0x00000000</span></span>                                         |
| <span data-ttu-id="cfc71-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-150">System-Flags</span></span>           | <span data-ttu-id="cfc71-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfc71-151">0x00000010</span></span>                                         |
| <span data-ttu-id="cfc71-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cfc71-152">Classes used in</span></span>        | [<span data-ttu-id="cfc71-153">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cfc71-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cfc71-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfc71-154">Windows Server 2003</span></span>



| <span data-ttu-id="cfc71-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-155">Entry</span></span> | <span data-ttu-id="cfc71-156">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cfc71-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cfc71-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfc71-159">System-Only</span></span>            | <span data-ttu-id="cfc71-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-160">False</span></span>                                              |
| <span data-ttu-id="cfc71-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cfc71-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cfc71-162">True</span><span class="sxs-lookup"><span data-stu-id="cfc71-162">True</span></span>                                               |
| <span data-ttu-id="cfc71-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cfc71-163">Is Indexed</span></span>             | <span data-ttu-id="cfc71-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-164">False</span></span>                                              |
| <span data-ttu-id="cfc71-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cfc71-165">In Global Catalog</span></span>      | <span data-ttu-id="cfc71-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-166">False</span></span>                                              |
| <span data-ttu-id="cfc71-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfc71-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfc71-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfc71-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cfc71-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfc71-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfc71-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-171">Search-Flags</span></span>           | <span data-ttu-id="cfc71-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfc71-172">0x00000000</span></span>                                         |
| <span data-ttu-id="cfc71-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-173">System-Flags</span></span>           | <span data-ttu-id="cfc71-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfc71-174">0x00000010</span></span>                                         |
| <span data-ttu-id="cfc71-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cfc71-175">Classes used in</span></span>        | [<span data-ttu-id="cfc71-176">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cfc71-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cfc71-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfc71-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cfc71-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-178">Entry</span></span> | <span data-ttu-id="cfc71-179">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cfc71-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cfc71-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfc71-182">System-Only</span></span>            | <span data-ttu-id="cfc71-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-183">False</span></span>                                              |
| <span data-ttu-id="cfc71-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cfc71-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cfc71-185">True</span><span class="sxs-lookup"><span data-stu-id="cfc71-185">True</span></span>                                               |
| <span data-ttu-id="cfc71-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cfc71-186">Is Indexed</span></span>             | <span data-ttu-id="cfc71-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-187">False</span></span>                                              |
| <span data-ttu-id="cfc71-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cfc71-188">In Global Catalog</span></span>      | <span data-ttu-id="cfc71-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-189">False</span></span>                                              |
| <span data-ttu-id="cfc71-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfc71-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfc71-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfc71-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cfc71-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfc71-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfc71-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-194">Search-Flags</span></span>           | <span data-ttu-id="cfc71-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfc71-195">0x00000000</span></span>                                         |
| <span data-ttu-id="cfc71-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-196">System-Flags</span></span>           | <span data-ttu-id="cfc71-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfc71-197">0x00000010</span></span>                                         |
| <span data-ttu-id="cfc71-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cfc71-198">Classes used in</span></span>        | [<span data-ttu-id="cfc71-199">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cfc71-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cfc71-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfc71-200">Windows Server 2008</span></span>



| <span data-ttu-id="cfc71-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-201">Entry</span></span> | <span data-ttu-id="cfc71-202">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cfc71-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cfc71-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfc71-205">System-Only</span></span>            | <span data-ttu-id="cfc71-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-206">False</span></span>                                              |
| <span data-ttu-id="cfc71-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cfc71-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cfc71-208">True</span><span class="sxs-lookup"><span data-stu-id="cfc71-208">True</span></span>                                               |
| <span data-ttu-id="cfc71-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cfc71-209">Is Indexed</span></span>             | <span data-ttu-id="cfc71-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-210">False</span></span>                                              |
| <span data-ttu-id="cfc71-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cfc71-211">In Global Catalog</span></span>      | <span data-ttu-id="cfc71-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-212">False</span></span>                                              |
| <span data-ttu-id="cfc71-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfc71-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfc71-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfc71-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cfc71-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfc71-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfc71-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-217">Search-Flags</span></span>           | <span data-ttu-id="cfc71-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfc71-218">0x00000000</span></span>                                         |
| <span data-ttu-id="cfc71-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-219">System-Flags</span></span>           | <span data-ttu-id="cfc71-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfc71-220">0x00000010</span></span>                                         |
| <span data-ttu-id="cfc71-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cfc71-221">Classes used in</span></span>        | [<span data-ttu-id="cfc71-222">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cfc71-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cfc71-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfc71-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cfc71-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-224">Entry</span></span> | <span data-ttu-id="cfc71-225">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cfc71-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cfc71-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfc71-228">System-Only</span></span>            | <span data-ttu-id="cfc71-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-229">False</span></span>                                              |
| <span data-ttu-id="cfc71-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cfc71-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cfc71-231">True</span><span class="sxs-lookup"><span data-stu-id="cfc71-231">True</span></span>                                               |
| <span data-ttu-id="cfc71-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cfc71-232">Is Indexed</span></span>             | <span data-ttu-id="cfc71-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-233">False</span></span>                                              |
| <span data-ttu-id="cfc71-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cfc71-234">In Global Catalog</span></span>      | <span data-ttu-id="cfc71-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-235">False</span></span>                                              |
| <span data-ttu-id="cfc71-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfc71-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfc71-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfc71-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cfc71-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfc71-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfc71-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-240">Search-Flags</span></span>           | <span data-ttu-id="cfc71-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfc71-241">0x00000000</span></span>                                         |
| <span data-ttu-id="cfc71-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-242">System-Flags</span></span>           | <span data-ttu-id="cfc71-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfc71-243">0x00000010</span></span>                                         |
| <span data-ttu-id="cfc71-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cfc71-244">Classes used in</span></span>        | [<span data-ttu-id="cfc71-245">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cfc71-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cfc71-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfc71-246">Windows Server 2012</span></span>



| <span data-ttu-id="cfc71-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="cfc71-247">Entry</span></span> | <span data-ttu-id="cfc71-248">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc71-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cfc71-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cfc71-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfc71-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cfc71-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfc71-251">System-Only</span></span>            | <span data-ttu-id="cfc71-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-252">False</span></span>                                              |
| <span data-ttu-id="cfc71-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cfc71-253">Is-Single-Valued</span></span>       | <span data-ttu-id="cfc71-254">True</span><span class="sxs-lookup"><span data-stu-id="cfc71-254">True</span></span>                                               |
| <span data-ttu-id="cfc71-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cfc71-255">Is Indexed</span></span>             | <span data-ttu-id="cfc71-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-256">False</span></span>                                              |
| <span data-ttu-id="cfc71-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cfc71-257">In Global Catalog</span></span>      | <span data-ttu-id="cfc71-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="cfc71-258">False</span></span>                                              |
| <span data-ttu-id="cfc71-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfc71-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfc71-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfc71-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cfc71-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfc71-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfc71-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cfc71-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-263">Search-Flags</span></span>           | <span data-ttu-id="cfc71-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfc71-264">0x00000000</span></span>                                         |
| <span data-ttu-id="cfc71-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfc71-265">System-Flags</span></span>           | <span data-ttu-id="cfc71-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfc71-266">0x00000010</span></span>                                         |
| <span data-ttu-id="cfc71-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cfc71-267">Classes used in</span></span>        | [<span data-ttu-id="cfc71-268">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cfc71-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





