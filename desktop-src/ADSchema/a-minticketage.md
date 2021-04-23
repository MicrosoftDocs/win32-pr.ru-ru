---
title: Атрибут min-Ticket-Age
description: Этот атрибут определяет минимальный период времени (в часах), в течение которого можно использовать билет предоставления билета (TGT) для проверки подлинности Kerberos, прежде чем можно будет запросить продление билета.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута min-Ticket-Age
- Схема AD атрибута Минтиккетаже
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138246"
---
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="46843-105">Атрибут min-Ticket-Age</span><span class="sxs-lookup"><span data-stu-id="46843-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="46843-106">Этот атрибут определяет минимальный период времени (в часах), в течение которого можно использовать билет предоставления билета (TGT) для проверки подлинности Kerberos, прежде чем можно будет запросить продление билета.</span><span class="sxs-lookup"><span data-stu-id="46843-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="46843-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-107">Entry</span></span> | <span data-ttu-id="46843-108">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="46843-109">CN</span><span class="sxs-lookup"><span data-stu-id="46843-109">CN</span></span>                | <span data-ttu-id="46843-110">Min-Ticket-Age</span><span class="sxs-lookup"><span data-stu-id="46843-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="46843-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="46843-111">Ldap-Display-Name</span></span> | <span data-ttu-id="46843-112">минтиккетаже</span><span class="sxs-lookup"><span data-stu-id="46843-112">minTicketAge</span></span>                         |
| <span data-ttu-id="46843-113">Размер</span><span class="sxs-lookup"><span data-stu-id="46843-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="46843-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="46843-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="46843-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="46843-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="46843-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46843-116">Attribute-Id</span></span>      | <span data-ttu-id="46843-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="46843-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="46843-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="46843-118">System-Id-Guid</span></span>    | <span data-ttu-id="46843-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="46843-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="46843-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46843-120">Syntax</span></span>            | [<span data-ttu-id="46843-121">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="46843-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="46843-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="46843-122">Implementations</span></span>

-   [<span data-ttu-id="46843-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46843-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46843-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46843-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46843-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46843-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46843-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46843-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46843-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46843-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46843-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46843-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46843-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46843-129">Windows 2000 Server</span></span>



| <span data-ttu-id="46843-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-130">Entry</span></span> | <span data-ttu-id="46843-131">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="46843-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46843-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46843-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="46843-134">System-Only</span></span>            | <span data-ttu-id="46843-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-135">False</span></span>                                              |
| <span data-ttu-id="46843-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46843-136">Is-Single-Valued</span></span>       | <span data-ttu-id="46843-137">True</span><span class="sxs-lookup"><span data-stu-id="46843-137">True</span></span>                                               |
| <span data-ttu-id="46843-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46843-138">Is Indexed</span></span>             | <span data-ttu-id="46843-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-139">False</span></span>                                              |
| <span data-ttu-id="46843-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46843-140">In Global Catalog</span></span>      | <span data-ttu-id="46843-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-141">False</span></span>                                              |
| <span data-ttu-id="46843-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46843-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="46843-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46843-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="46843-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46843-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="46843-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46843-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="46843-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-146">Search-Flags</span></span>           | <span data-ttu-id="46843-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46843-147">0x00000000</span></span>                                         |
| <span data-ttu-id="46843-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-148">System-Flags</span></span>           | <span data-ttu-id="46843-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46843-149">0x00000010</span></span>                                         |
| <span data-ttu-id="46843-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46843-150">Classes used in</span></span>        | [<span data-ttu-id="46843-151">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="46843-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46843-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46843-152">Windows Server 2003</span></span>



| <span data-ttu-id="46843-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-153">Entry</span></span> | <span data-ttu-id="46843-154">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="46843-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46843-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46843-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="46843-157">System-Only</span></span>            | <span data-ttu-id="46843-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-158">False</span></span>                                              |
| <span data-ttu-id="46843-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46843-159">Is-Single-Valued</span></span>       | <span data-ttu-id="46843-160">True</span><span class="sxs-lookup"><span data-stu-id="46843-160">True</span></span>                                               |
| <span data-ttu-id="46843-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46843-161">Is Indexed</span></span>             | <span data-ttu-id="46843-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-162">False</span></span>                                              |
| <span data-ttu-id="46843-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46843-163">In Global Catalog</span></span>      | <span data-ttu-id="46843-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-164">False</span></span>                                              |
| <span data-ttu-id="46843-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46843-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="46843-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46843-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="46843-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46843-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="46843-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46843-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="46843-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-169">Search-Flags</span></span>           | <span data-ttu-id="46843-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46843-170">0x00000000</span></span>                                         |
| <span data-ttu-id="46843-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-171">System-Flags</span></span>           | <span data-ttu-id="46843-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46843-172">0x00000010</span></span>                                         |
| <span data-ttu-id="46843-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46843-173">Classes used in</span></span>        | [<span data-ttu-id="46843-174">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="46843-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46843-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46843-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46843-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-176">Entry</span></span> | <span data-ttu-id="46843-177">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="46843-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46843-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46843-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="46843-180">System-Only</span></span>            | <span data-ttu-id="46843-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-181">False</span></span>                                              |
| <span data-ttu-id="46843-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46843-182">Is-Single-Valued</span></span>       | <span data-ttu-id="46843-183">True</span><span class="sxs-lookup"><span data-stu-id="46843-183">True</span></span>                                               |
| <span data-ttu-id="46843-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46843-184">Is Indexed</span></span>             | <span data-ttu-id="46843-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-185">False</span></span>                                              |
| <span data-ttu-id="46843-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46843-186">In Global Catalog</span></span>      | <span data-ttu-id="46843-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-187">False</span></span>                                              |
| <span data-ttu-id="46843-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46843-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="46843-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46843-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="46843-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46843-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="46843-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46843-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="46843-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-192">Search-Flags</span></span>           | <span data-ttu-id="46843-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46843-193">0x00000000</span></span>                                         |
| <span data-ttu-id="46843-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-194">System-Flags</span></span>           | <span data-ttu-id="46843-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46843-195">0x00000010</span></span>                                         |
| <span data-ttu-id="46843-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46843-196">Classes used in</span></span>        | [<span data-ttu-id="46843-197">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="46843-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46843-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46843-198">Windows Server 2008</span></span>



| <span data-ttu-id="46843-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-199">Entry</span></span> | <span data-ttu-id="46843-200">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="46843-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46843-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46843-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="46843-203">System-Only</span></span>            | <span data-ttu-id="46843-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-204">False</span></span>                                              |
| <span data-ttu-id="46843-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46843-205">Is-Single-Valued</span></span>       | <span data-ttu-id="46843-206">True</span><span class="sxs-lookup"><span data-stu-id="46843-206">True</span></span>                                               |
| <span data-ttu-id="46843-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46843-207">Is Indexed</span></span>             | <span data-ttu-id="46843-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-208">False</span></span>                                              |
| <span data-ttu-id="46843-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46843-209">In Global Catalog</span></span>      | <span data-ttu-id="46843-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-210">False</span></span>                                              |
| <span data-ttu-id="46843-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46843-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="46843-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46843-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="46843-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46843-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="46843-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46843-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="46843-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-215">Search-Flags</span></span>           | <span data-ttu-id="46843-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46843-216">0x00000000</span></span>                                         |
| <span data-ttu-id="46843-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-217">System-Flags</span></span>           | <span data-ttu-id="46843-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46843-218">0x00000010</span></span>                                         |
| <span data-ttu-id="46843-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46843-219">Classes used in</span></span>        | [<span data-ttu-id="46843-220">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="46843-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46843-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46843-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46843-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-222">Entry</span></span> | <span data-ttu-id="46843-223">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="46843-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46843-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46843-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="46843-226">System-Only</span></span>            | <span data-ttu-id="46843-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-227">False</span></span>                                              |
| <span data-ttu-id="46843-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46843-228">Is-Single-Valued</span></span>       | <span data-ttu-id="46843-229">True</span><span class="sxs-lookup"><span data-stu-id="46843-229">True</span></span>                                               |
| <span data-ttu-id="46843-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46843-230">Is Indexed</span></span>             | <span data-ttu-id="46843-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-231">False</span></span>                                              |
| <span data-ttu-id="46843-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46843-232">In Global Catalog</span></span>      | <span data-ttu-id="46843-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-233">False</span></span>                                              |
| <span data-ttu-id="46843-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46843-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="46843-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46843-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="46843-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46843-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="46843-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46843-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="46843-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-238">Search-Flags</span></span>           | <span data-ttu-id="46843-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46843-239">0x00000000</span></span>                                         |
| <span data-ttu-id="46843-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-240">System-Flags</span></span>           | <span data-ttu-id="46843-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46843-241">0x00000010</span></span>                                         |
| <span data-ttu-id="46843-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46843-242">Classes used in</span></span>        | [<span data-ttu-id="46843-243">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="46843-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46843-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46843-244">Windows Server 2012</span></span>



| <span data-ttu-id="46843-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="46843-245">Entry</span></span> | <span data-ttu-id="46843-246">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="46843-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46843-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46843-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="46843-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="46843-249">System-Only</span></span>            | <span data-ttu-id="46843-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-250">False</span></span>                                              |
| <span data-ttu-id="46843-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46843-251">Is-Single-Valued</span></span>       | <span data-ttu-id="46843-252">True</span><span class="sxs-lookup"><span data-stu-id="46843-252">True</span></span>                                               |
| <span data-ttu-id="46843-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46843-253">Is Indexed</span></span>             | <span data-ttu-id="46843-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-254">False</span></span>                                              |
| <span data-ttu-id="46843-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46843-255">In Global Catalog</span></span>      | <span data-ttu-id="46843-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="46843-256">False</span></span>                                              |
| <span data-ttu-id="46843-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46843-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="46843-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46843-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="46843-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46843-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="46843-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46843-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="46843-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-261">Search-Flags</span></span>           | <span data-ttu-id="46843-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46843-262">0x00000000</span></span>                                         |
| <span data-ttu-id="46843-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46843-263">System-Flags</span></span>           | <span data-ttu-id="46843-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46843-264">0x00000010</span></span>                                         |
| <span data-ttu-id="46843-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46843-265">Classes used in</span></span>        | [<span data-ttu-id="46843-266">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="46843-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





