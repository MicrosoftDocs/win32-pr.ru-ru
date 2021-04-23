---
title: Атрибут Account-Expires
description: Дата истечения срока действия учетной записи.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Account-Expires
- Схема AD атрибута accountExpires
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655517"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="8f851-105">Атрибут Account-Expires</span><span class="sxs-lookup"><span data-stu-id="8f851-105">Account-Expires attribute</span></span>

<span data-ttu-id="8f851-106">Дата истечения срока действия учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f851-106">The date when the account expires.</span></span> <span data-ttu-id="8f851-107">Это значение представляет число 100-наносекундных интервалов с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="8f851-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="8f851-108">Значение 0 или 0x7FFFFFFFFFFFFFFF (9223372036854775807) указывает, что срок действия учетной записи никогда не истекает.</span><span class="sxs-lookup"><span data-stu-id="8f851-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="8f851-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-109">Entry</span></span> | <span data-ttu-id="8f851-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="8f851-111">CN</span><span class="sxs-lookup"><span data-stu-id="8f851-111">CN</span></span>                | <span data-ttu-id="8f851-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="8f851-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="8f851-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8f851-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8f851-114">accountExpires</span><span class="sxs-lookup"><span data-stu-id="8f851-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="8f851-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8f851-115">Size</span></span>              | <span data-ttu-id="8f851-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="8f851-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="8f851-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8f851-117">Update Privilege</span></span>  | <span data-ttu-id="8f851-118">Этот атрибут устанавливается администратором домена.</span><span class="sxs-lookup"><span data-stu-id="8f851-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="8f851-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8f851-119">Update Frequency</span></span>  | <span data-ttu-id="8f851-120">Каждый раз, когда срок действия предыдущей даты истекает и необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="8f851-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="8f851-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-121">Attribute-Id</span></span>      | <span data-ttu-id="8f851-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="8f851-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="8f851-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8f851-123">System-Id-Guid</span></span>    | <span data-ttu-id="8f851-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8f851-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="8f851-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f851-125">Syntax</span></span>            | [<span data-ttu-id="8f851-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="8f851-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="8f851-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8f851-127">Implementations</span></span>

-   [<span data-ttu-id="8f851-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f851-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f851-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f851-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f851-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8f851-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8f851-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f851-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f851-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f851-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f851-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f851-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f851-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f851-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f851-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f851-135">Windows 2000 Server</span></span>



| <span data-ttu-id="8f851-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-136">Entry</span></span> | <span data-ttu-id="8f851-137">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f851-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-140">System-Only</span></span>            | <span data-ttu-id="8f851-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-141">False</span></span>                             |
| <span data-ttu-id="8f851-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-142">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-143">True</span><span class="sxs-lookup"><span data-stu-id="8f851-143">True</span></span>                              |
| <span data-ttu-id="8f851-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-144">Is Indexed</span></span>             | <span data-ttu-id="8f851-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-145">False</span></span>                             |
| <span data-ttu-id="8f851-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-146">In Global Catalog</span></span>      | <span data-ttu-id="8f851-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-147">False</span></span>                             |
| <span data-ttu-id="8f851-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f851-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f851-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f851-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-152">Search-Flags</span></span>           | <span data-ttu-id="8f851-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-153">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-154">System-Flags</span></span>           | <span data-ttu-id="8f851-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-155">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-156">Classes used in</span></span>        | [<span data-ttu-id="8f851-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f851-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8f851-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f851-158">Windows Server 2003</span></span>



| <span data-ttu-id="8f851-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-159">Entry</span></span> | <span data-ttu-id="8f851-160">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f851-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-163">System-Only</span></span>            | <span data-ttu-id="8f851-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-164">False</span></span>                             |
| <span data-ttu-id="8f851-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-166">True</span><span class="sxs-lookup"><span data-stu-id="8f851-166">True</span></span>                              |
| <span data-ttu-id="8f851-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-167">Is Indexed</span></span>             | <span data-ttu-id="8f851-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-168">False</span></span>                             |
| <span data-ttu-id="8f851-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-169">In Global Catalog</span></span>      | <span data-ttu-id="8f851-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-170">False</span></span>                             |
| <span data-ttu-id="8f851-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f851-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f851-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f851-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-175">Search-Flags</span></span>           | <span data-ttu-id="8f851-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-176">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-177">System-Flags</span></span>           | <span data-ttu-id="8f851-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-178">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-179">Classes used in</span></span>        | [<span data-ttu-id="8f851-180">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f851-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8f851-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="8f851-181">ADAM</span></span>



| <span data-ttu-id="8f851-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-182">Entry</span></span> | <span data-ttu-id="8f851-183">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8f851-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8f851-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8f851-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-186">System-Only</span></span>            | <span data-ttu-id="8f851-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-187">False</span></span>                                                             |
| <span data-ttu-id="8f851-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-188">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-189">True</span><span class="sxs-lookup"><span data-stu-id="8f851-189">True</span></span>                                                              |
| <span data-ttu-id="8f851-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-190">Is Indexed</span></span>             | <span data-ttu-id="8f851-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-191">False</span></span>                                                             |
| <span data-ttu-id="8f851-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-192">In Global Catalog</span></span>      | <span data-ttu-id="8f851-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-193">False</span></span>                                                             |
| <span data-ttu-id="8f851-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8f851-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8f851-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8f851-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-198">Search-Flags</span></span>           | <span data-ttu-id="8f851-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="8f851-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-200">System-Flags</span></span>           | <span data-ttu-id="8f851-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="8f851-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-202">Classes used in</span></span>        | [<span data-ttu-id="8f851-203">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="8f851-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f851-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f851-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f851-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-205">Entry</span></span> | <span data-ttu-id="8f851-206">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f851-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-209">System-Only</span></span>            | <span data-ttu-id="8f851-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-210">False</span></span>                             |
| <span data-ttu-id="8f851-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-211">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-212">True</span><span class="sxs-lookup"><span data-stu-id="8f851-212">True</span></span>                              |
| <span data-ttu-id="8f851-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-213">Is Indexed</span></span>             | <span data-ttu-id="8f851-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-214">False</span></span>                             |
| <span data-ttu-id="8f851-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-215">In Global Catalog</span></span>      | <span data-ttu-id="8f851-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-216">False</span></span>                             |
| <span data-ttu-id="8f851-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f851-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f851-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f851-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-221">Search-Flags</span></span>           | <span data-ttu-id="8f851-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-222">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-223">System-Flags</span></span>           | <span data-ttu-id="8f851-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-224">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-225">Classes used in</span></span>        | [<span data-ttu-id="8f851-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f851-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8f851-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f851-227">Windows Server 2008</span></span>



| <span data-ttu-id="8f851-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-228">Entry</span></span> | <span data-ttu-id="8f851-229">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f851-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-232">System-Only</span></span>            | <span data-ttu-id="8f851-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-233">False</span></span>                             |
| <span data-ttu-id="8f851-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-234">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-235">True</span><span class="sxs-lookup"><span data-stu-id="8f851-235">True</span></span>                              |
| <span data-ttu-id="8f851-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-236">Is Indexed</span></span>             | <span data-ttu-id="8f851-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-237">False</span></span>                             |
| <span data-ttu-id="8f851-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-238">In Global Catalog</span></span>      | <span data-ttu-id="8f851-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-239">False</span></span>                             |
| <span data-ttu-id="8f851-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f851-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f851-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f851-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-244">Search-Flags</span></span>           | <span data-ttu-id="8f851-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-245">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-246">System-Flags</span></span>           | <span data-ttu-id="8f851-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-247">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-248">Classes used in</span></span>        | [<span data-ttu-id="8f851-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f851-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f851-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f851-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f851-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-251">Entry</span></span> | <span data-ttu-id="8f851-252">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f851-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-255">System-Only</span></span>            | <span data-ttu-id="8f851-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-256">False</span></span>                             |
| <span data-ttu-id="8f851-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-257">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-258">True</span><span class="sxs-lookup"><span data-stu-id="8f851-258">True</span></span>                              |
| <span data-ttu-id="8f851-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-259">Is Indexed</span></span>             | <span data-ttu-id="8f851-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-260">False</span></span>                             |
| <span data-ttu-id="8f851-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-261">In Global Catalog</span></span>      | <span data-ttu-id="8f851-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-262">False</span></span>                             |
| <span data-ttu-id="8f851-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f851-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f851-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f851-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-267">Search-Flags</span></span>           | <span data-ttu-id="8f851-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-268">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-269">System-Flags</span></span>           | <span data-ttu-id="8f851-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-270">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-271">Classes used in</span></span>        | [<span data-ttu-id="8f851-272">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f851-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8f851-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f851-273">Windows Server 2012</span></span>



| <span data-ttu-id="8f851-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f851-274">Entry</span></span> | <span data-ttu-id="8f851-275">Значение</span><span class="sxs-lookup"><span data-stu-id="8f851-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f851-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f851-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f851-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f851-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f851-278">System-Only</span></span>            | <span data-ttu-id="8f851-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-279">False</span></span>                             |
| <span data-ttu-id="8f851-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f851-280">Is-Single-Valued</span></span>       | <span data-ttu-id="8f851-281">True</span><span class="sxs-lookup"><span data-stu-id="8f851-281">True</span></span>                              |
| <span data-ttu-id="8f851-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f851-282">Is Indexed</span></span>             | <span data-ttu-id="8f851-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-283">False</span></span>                             |
| <span data-ttu-id="8f851-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f851-284">In Global Catalog</span></span>      | <span data-ttu-id="8f851-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f851-285">False</span></span>                             |
| <span data-ttu-id="8f851-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f851-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f851-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f851-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f851-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f851-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f851-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f851-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f851-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-290">Search-Flags</span></span>           | <span data-ttu-id="8f851-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-291">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f851-292">System-Flags</span></span>           | <span data-ttu-id="8f851-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f851-293">0x00000010</span></span>                        |
| <span data-ttu-id="8f851-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f851-294">Classes used in</span></span>        | [<span data-ttu-id="8f851-295">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f851-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8f851-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f851-296">Remarks</span></span>

<span data-ttu-id="8f851-297">Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="8f851-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 

