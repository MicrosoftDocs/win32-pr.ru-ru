---
title: Атрибут max-Ticket-Age
description: Этот атрибут определяет максимальное количество времени (в часах), в течение которого можно использовать билет предоставления билета (TGT) для проверки подлинности Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Max-Ticket-Age
- Схема AD атрибута Макстиккетаже
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804409"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="dad27-105">Атрибут max-Ticket-Age</span><span class="sxs-lookup"><span data-stu-id="dad27-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="dad27-106">Этот атрибут определяет максимальное количество времени (в часах), в течение которого можно использовать билет предоставления билета (TGT) для проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="dad27-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="dad27-107">По истечении срока действия TGT пользователя должен быть запрошен новый запрос, или должен быть обновлен существующий.</span><span class="sxs-lookup"><span data-stu-id="dad27-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="dad27-108">По умолчанию для этого параметра задано значение 10 часов в объекте групповая политика домена по умолчанию (GPO).</span><span class="sxs-lookup"><span data-stu-id="dad27-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="dad27-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-109">Entry</span></span> | <span data-ttu-id="dad27-110">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="dad27-111">CN</span><span class="sxs-lookup"><span data-stu-id="dad27-111">CN</span></span>                | <span data-ttu-id="dad27-112">Max-Ticket-Age</span><span class="sxs-lookup"><span data-stu-id="dad27-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="dad27-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="dad27-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dad27-114">макстиккетаже</span><span class="sxs-lookup"><span data-stu-id="dad27-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="dad27-115">Размер</span><span class="sxs-lookup"><span data-stu-id="dad27-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="dad27-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="dad27-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="dad27-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="dad27-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="dad27-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-118">Attribute-Id</span></span>      | <span data-ttu-id="dad27-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="dad27-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="dad27-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="dad27-120">System-Id-Guid</span></span>    | <span data-ttu-id="dad27-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dad27-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="dad27-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dad27-122">Syntax</span></span>            | [<span data-ttu-id="dad27-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="dad27-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="dad27-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="dad27-124">Implementations</span></span>

-   [<span data-ttu-id="dad27-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dad27-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dad27-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dad27-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dad27-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dad27-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dad27-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dad27-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dad27-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dad27-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dad27-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dad27-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dad27-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dad27-131">Windows 2000 Server</span></span>



| <span data-ttu-id="dad27-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-132">Entry</span></span> | <span data-ttu-id="dad27-133">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="dad27-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dad27-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="dad27-136">System-Only</span></span>            | <span data-ttu-id="dad27-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-137">False</span></span>                                              |
| <span data-ttu-id="dad27-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dad27-138">Is-Single-Valued</span></span>       | <span data-ttu-id="dad27-139">True</span><span class="sxs-lookup"><span data-stu-id="dad27-139">True</span></span>                                               |
| <span data-ttu-id="dad27-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dad27-140">Is Indexed</span></span>             | <span data-ttu-id="dad27-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-141">False</span></span>                                              |
| <span data-ttu-id="dad27-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dad27-142">In Global Catalog</span></span>      | <span data-ttu-id="dad27-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-143">False</span></span>                                              |
| <span data-ttu-id="dad27-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dad27-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="dad27-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dad27-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="dad27-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dad27-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dad27-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-148">Search-Flags</span></span>           | <span data-ttu-id="dad27-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dad27-149">0x00000000</span></span>                                         |
| <span data-ttu-id="dad27-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-150">System-Flags</span></span>           | <span data-ttu-id="dad27-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dad27-151">0x00000010</span></span>                                         |
| <span data-ttu-id="dad27-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dad27-152">Classes used in</span></span>        | [<span data-ttu-id="dad27-153">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="dad27-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dad27-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dad27-154">Windows Server 2003</span></span>



| <span data-ttu-id="dad27-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-155">Entry</span></span> | <span data-ttu-id="dad27-156">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="dad27-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dad27-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dad27-159">System-Only</span></span>            | <span data-ttu-id="dad27-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-160">False</span></span>                                              |
| <span data-ttu-id="dad27-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dad27-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dad27-162">True</span><span class="sxs-lookup"><span data-stu-id="dad27-162">True</span></span>                                               |
| <span data-ttu-id="dad27-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dad27-163">Is Indexed</span></span>             | <span data-ttu-id="dad27-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-164">False</span></span>                                              |
| <span data-ttu-id="dad27-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dad27-165">In Global Catalog</span></span>      | <span data-ttu-id="dad27-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-166">False</span></span>                                              |
| <span data-ttu-id="dad27-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dad27-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dad27-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dad27-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="dad27-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dad27-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dad27-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-171">Search-Flags</span></span>           | <span data-ttu-id="dad27-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dad27-172">0x00000000</span></span>                                         |
| <span data-ttu-id="dad27-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-173">System-Flags</span></span>           | <span data-ttu-id="dad27-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dad27-174">0x00000010</span></span>                                         |
| <span data-ttu-id="dad27-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dad27-175">Classes used in</span></span>        | [<span data-ttu-id="dad27-176">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="dad27-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dad27-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dad27-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dad27-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-178">Entry</span></span> | <span data-ttu-id="dad27-179">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="dad27-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dad27-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="dad27-182">System-Only</span></span>            | <span data-ttu-id="dad27-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-183">False</span></span>                                              |
| <span data-ttu-id="dad27-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dad27-184">Is-Single-Valued</span></span>       | <span data-ttu-id="dad27-185">True</span><span class="sxs-lookup"><span data-stu-id="dad27-185">True</span></span>                                               |
| <span data-ttu-id="dad27-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dad27-186">Is Indexed</span></span>             | <span data-ttu-id="dad27-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-187">False</span></span>                                              |
| <span data-ttu-id="dad27-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dad27-188">In Global Catalog</span></span>      | <span data-ttu-id="dad27-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-189">False</span></span>                                              |
| <span data-ttu-id="dad27-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dad27-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="dad27-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dad27-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="dad27-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dad27-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dad27-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-194">Search-Flags</span></span>           | <span data-ttu-id="dad27-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dad27-195">0x00000000</span></span>                                         |
| <span data-ttu-id="dad27-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-196">System-Flags</span></span>           | <span data-ttu-id="dad27-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dad27-197">0x00000010</span></span>                                         |
| <span data-ttu-id="dad27-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dad27-198">Classes used in</span></span>        | [<span data-ttu-id="dad27-199">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="dad27-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dad27-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dad27-200">Windows Server 2008</span></span>



| <span data-ttu-id="dad27-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-201">Entry</span></span> | <span data-ttu-id="dad27-202">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="dad27-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dad27-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="dad27-205">System-Only</span></span>            | <span data-ttu-id="dad27-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-206">False</span></span>                                              |
| <span data-ttu-id="dad27-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dad27-207">Is-Single-Valued</span></span>       | <span data-ttu-id="dad27-208">True</span><span class="sxs-lookup"><span data-stu-id="dad27-208">True</span></span>                                               |
| <span data-ttu-id="dad27-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dad27-209">Is Indexed</span></span>             | <span data-ttu-id="dad27-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-210">False</span></span>                                              |
| <span data-ttu-id="dad27-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dad27-211">In Global Catalog</span></span>      | <span data-ttu-id="dad27-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-212">False</span></span>                                              |
| <span data-ttu-id="dad27-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dad27-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="dad27-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dad27-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="dad27-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dad27-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dad27-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-217">Search-Flags</span></span>           | <span data-ttu-id="dad27-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dad27-218">0x00000000</span></span>                                         |
| <span data-ttu-id="dad27-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-219">System-Flags</span></span>           | <span data-ttu-id="dad27-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dad27-220">0x00000010</span></span>                                         |
| <span data-ttu-id="dad27-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dad27-221">Classes used in</span></span>        | [<span data-ttu-id="dad27-222">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="dad27-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dad27-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dad27-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dad27-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-224">Entry</span></span> | <span data-ttu-id="dad27-225">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="dad27-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dad27-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="dad27-228">System-Only</span></span>            | <span data-ttu-id="dad27-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-229">False</span></span>                                              |
| <span data-ttu-id="dad27-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dad27-230">Is-Single-Valued</span></span>       | <span data-ttu-id="dad27-231">True</span><span class="sxs-lookup"><span data-stu-id="dad27-231">True</span></span>                                               |
| <span data-ttu-id="dad27-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dad27-232">Is Indexed</span></span>             | <span data-ttu-id="dad27-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-233">False</span></span>                                              |
| <span data-ttu-id="dad27-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dad27-234">In Global Catalog</span></span>      | <span data-ttu-id="dad27-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-235">False</span></span>                                              |
| <span data-ttu-id="dad27-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dad27-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="dad27-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dad27-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="dad27-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dad27-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dad27-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-240">Search-Flags</span></span>           | <span data-ttu-id="dad27-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dad27-241">0x00000000</span></span>                                         |
| <span data-ttu-id="dad27-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-242">System-Flags</span></span>           | <span data-ttu-id="dad27-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dad27-243">0x00000010</span></span>                                         |
| <span data-ttu-id="dad27-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dad27-244">Classes used in</span></span>        | [<span data-ttu-id="dad27-245">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="dad27-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dad27-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dad27-246">Windows Server 2012</span></span>



| <span data-ttu-id="dad27-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="dad27-247">Entry</span></span> | <span data-ttu-id="dad27-248">Значение</span><span class="sxs-lookup"><span data-stu-id="dad27-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="dad27-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dad27-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dad27-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="dad27-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="dad27-251">System-Only</span></span>            | <span data-ttu-id="dad27-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-252">False</span></span>                                              |
| <span data-ttu-id="dad27-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dad27-253">Is-Single-Valued</span></span>       | <span data-ttu-id="dad27-254">True</span><span class="sxs-lookup"><span data-stu-id="dad27-254">True</span></span>                                               |
| <span data-ttu-id="dad27-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dad27-255">Is Indexed</span></span>             | <span data-ttu-id="dad27-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-256">False</span></span>                                              |
| <span data-ttu-id="dad27-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dad27-257">In Global Catalog</span></span>      | <span data-ttu-id="dad27-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="dad27-258">False</span></span>                                              |
| <span data-ttu-id="dad27-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dad27-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="dad27-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dad27-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="dad27-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dad27-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dad27-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="dad27-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-263">Search-Flags</span></span>           | <span data-ttu-id="dad27-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dad27-264">0x00000000</span></span>                                         |
| <span data-ttu-id="dad27-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dad27-265">System-Flags</span></span>           | <span data-ttu-id="dad27-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dad27-266">0x00000010</span></span>                                         |
| <span data-ttu-id="dad27-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dad27-267">Classes used in</span></span>        | [<span data-ttu-id="dad27-268">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="dad27-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





