---
title: Атрибут Lockout-Time
description: Дата и время блокировки этой учетной записи (в формате UTC).
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Lockout-Time
- Схема AD атрибута lockoutTime
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655242"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="36eea-105">Атрибут Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="36eea-105">Lockout-Time attribute</span></span>

<span data-ttu-id="36eea-106">Дата и время блокировки этой учетной записи (в формате UTC). Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="36eea-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="36eea-107">Нулевое значение означает, что учетная запись в настоящее время не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="36eea-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="36eea-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-108">Entry</span></span> | <span data-ttu-id="36eea-109">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36eea-110">CN</span><span class="sxs-lookup"><span data-stu-id="36eea-110">CN</span></span>                | <span data-ttu-id="36eea-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="36eea-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="36eea-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="36eea-112">Ldap-Display-Name</span></span> | <span data-ttu-id="36eea-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="36eea-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="36eea-114">Размер</span><span class="sxs-lookup"><span data-stu-id="36eea-114">Size</span></span>              | <span data-ttu-id="36eea-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="36eea-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="36eea-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="36eea-116">Update Privilege</span></span>  | <span data-ttu-id="36eea-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="36eea-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="36eea-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="36eea-118">Update Frequency</span></span>  | <span data-ttu-id="36eea-119">При создании записи пользователя и при необходимости изменения времени блокировки.</span><span class="sxs-lookup"><span data-stu-id="36eea-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="36eea-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-120">Attribute-Id</span></span>      | <span data-ttu-id="36eea-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="36eea-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="36eea-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="36eea-122">System-Id-Guid</span></span>    | <span data-ttu-id="36eea-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="36eea-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="36eea-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36eea-124">Syntax</span></span>            | [<span data-ttu-id="36eea-125">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="36eea-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="36eea-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="36eea-126">Implementations</span></span>

-   [<span data-ttu-id="36eea-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36eea-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36eea-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36eea-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36eea-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="36eea-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="36eea-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36eea-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36eea-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36eea-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36eea-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36eea-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36eea-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36eea-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36eea-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36eea-134">Windows 2000 Server</span></span>



| <span data-ttu-id="36eea-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-135">Entry</span></span> | <span data-ttu-id="36eea-136">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="36eea-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-139">System-Only</span></span>            | <span data-ttu-id="36eea-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-140">False</span></span>                             |
| <span data-ttu-id="36eea-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-141">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-142">True</span><span class="sxs-lookup"><span data-stu-id="36eea-142">True</span></span>                              |
| <span data-ttu-id="36eea-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-143">Is Indexed</span></span>             | <span data-ttu-id="36eea-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-144">False</span></span>                             |
| <span data-ttu-id="36eea-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-145">In Global Catalog</span></span>      | <span data-ttu-id="36eea-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-146">False</span></span>                             |
| <span data-ttu-id="36eea-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="36eea-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="36eea-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="36eea-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-151">Search-Flags</span></span>           | <span data-ttu-id="36eea-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-152">0x00000000</span></span>                        |
| <span data-ttu-id="36eea-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-153">System-Flags</span></span>           | <span data-ttu-id="36eea-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-154">0x00000010</span></span>                        |
| <span data-ttu-id="36eea-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-155">Classes used in</span></span>        | [<span data-ttu-id="36eea-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="36eea-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36eea-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36eea-157">Windows Server 2003</span></span>



| <span data-ttu-id="36eea-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-158">Entry</span></span> | <span data-ttu-id="36eea-159">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="36eea-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-162">System-Only</span></span>            | <span data-ttu-id="36eea-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-163">False</span></span>                             |
| <span data-ttu-id="36eea-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-164">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-165">True</span><span class="sxs-lookup"><span data-stu-id="36eea-165">True</span></span>                              |
| <span data-ttu-id="36eea-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-166">Is Indexed</span></span>             | <span data-ttu-id="36eea-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-167">False</span></span>                             |
| <span data-ttu-id="36eea-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-168">In Global Catalog</span></span>      | <span data-ttu-id="36eea-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-169">False</span></span>                             |
| <span data-ttu-id="36eea-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="36eea-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="36eea-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="36eea-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-174">Search-Flags</span></span>           | <span data-ttu-id="36eea-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-175">0x00000000</span></span>                        |
| <span data-ttu-id="36eea-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-176">System-Flags</span></span>           | <span data-ttu-id="36eea-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-177">0x00000010</span></span>                        |
| <span data-ttu-id="36eea-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-178">Classes used in</span></span>        | [<span data-ttu-id="36eea-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="36eea-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="36eea-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="36eea-180">ADAM</span></span>



| <span data-ttu-id="36eea-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-181">Entry</span></span> | <span data-ttu-id="36eea-182">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="36eea-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="36eea-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="36eea-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-185">System-Only</span></span>            | <span data-ttu-id="36eea-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-186">False</span></span>                                                             |
| <span data-ttu-id="36eea-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-187">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-188">True</span><span class="sxs-lookup"><span data-stu-id="36eea-188">True</span></span>                                                              |
| <span data-ttu-id="36eea-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-189">Is Indexed</span></span>             | <span data-ttu-id="36eea-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-190">False</span></span>                                                             |
| <span data-ttu-id="36eea-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-191">In Global Catalog</span></span>      | <span data-ttu-id="36eea-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-192">False</span></span>                                                             |
| <span data-ttu-id="36eea-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="36eea-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="36eea-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="36eea-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-197">Search-Flags</span></span>           | <span data-ttu-id="36eea-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="36eea-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-199">System-Flags</span></span>           | <span data-ttu-id="36eea-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="36eea-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-201">Classes used in</span></span>        | [<span data-ttu-id="36eea-202">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="36eea-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36eea-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36eea-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36eea-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-204">Entry</span></span> | <span data-ttu-id="36eea-205">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="36eea-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-208">System-Only</span></span>            | <span data-ttu-id="36eea-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-209">False</span></span>                             |
| <span data-ttu-id="36eea-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-210">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-211">True</span><span class="sxs-lookup"><span data-stu-id="36eea-211">True</span></span>                              |
| <span data-ttu-id="36eea-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-212">Is Indexed</span></span>             | <span data-ttu-id="36eea-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-213">False</span></span>                             |
| <span data-ttu-id="36eea-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-214">In Global Catalog</span></span>      | <span data-ttu-id="36eea-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-215">False</span></span>                             |
| <span data-ttu-id="36eea-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="36eea-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="36eea-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="36eea-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-220">Search-Flags</span></span>           | <span data-ttu-id="36eea-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-221">0x00000000</span></span>                        |
| <span data-ttu-id="36eea-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-222">System-Flags</span></span>           | <span data-ttu-id="36eea-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-223">0x00000010</span></span>                        |
| <span data-ttu-id="36eea-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-224">Classes used in</span></span>        | [<span data-ttu-id="36eea-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="36eea-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36eea-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36eea-226">Windows Server 2008</span></span>



| <span data-ttu-id="36eea-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-227">Entry</span></span> | <span data-ttu-id="36eea-228">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="36eea-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-231">System-Only</span></span>            | <span data-ttu-id="36eea-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-232">False</span></span>                             |
| <span data-ttu-id="36eea-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-233">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-234">True</span><span class="sxs-lookup"><span data-stu-id="36eea-234">True</span></span>                              |
| <span data-ttu-id="36eea-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-235">Is Indexed</span></span>             | <span data-ttu-id="36eea-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-236">False</span></span>                             |
| <span data-ttu-id="36eea-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-237">In Global Catalog</span></span>      | <span data-ttu-id="36eea-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-238">False</span></span>                             |
| <span data-ttu-id="36eea-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="36eea-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="36eea-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="36eea-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-243">Search-Flags</span></span>           | <span data-ttu-id="36eea-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-244">0x00000000</span></span>                        |
| <span data-ttu-id="36eea-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-245">System-Flags</span></span>           | <span data-ttu-id="36eea-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-246">0x00000010</span></span>                        |
| <span data-ttu-id="36eea-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-247">Classes used in</span></span>        | [<span data-ttu-id="36eea-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="36eea-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36eea-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36eea-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36eea-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-250">Entry</span></span> | <span data-ttu-id="36eea-251">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="36eea-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-254">System-Only</span></span>            | <span data-ttu-id="36eea-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-255">False</span></span>                             |
| <span data-ttu-id="36eea-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-256">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-257">True</span><span class="sxs-lookup"><span data-stu-id="36eea-257">True</span></span>                              |
| <span data-ttu-id="36eea-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-258">Is Indexed</span></span>             | <span data-ttu-id="36eea-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-259">False</span></span>                             |
| <span data-ttu-id="36eea-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-260">In Global Catalog</span></span>      | <span data-ttu-id="36eea-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-261">False</span></span>                             |
| <span data-ttu-id="36eea-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="36eea-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="36eea-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="36eea-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-266">Search-Flags</span></span>           | <span data-ttu-id="36eea-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-267">0x00000000</span></span>                        |
| <span data-ttu-id="36eea-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-268">System-Flags</span></span>           | <span data-ttu-id="36eea-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-269">0x00000010</span></span>                        |
| <span data-ttu-id="36eea-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-270">Classes used in</span></span>        | [<span data-ttu-id="36eea-271">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="36eea-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36eea-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36eea-272">Windows Server 2012</span></span>



| <span data-ttu-id="36eea-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="36eea-273">Entry</span></span> | <span data-ttu-id="36eea-274">Значение</span><span class="sxs-lookup"><span data-stu-id="36eea-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="36eea-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36eea-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36eea-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="36eea-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="36eea-277">System-Only</span></span>            | <span data-ttu-id="36eea-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-278">False</span></span>                             |
| <span data-ttu-id="36eea-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36eea-279">Is-Single-Valued</span></span>       | <span data-ttu-id="36eea-280">True</span><span class="sxs-lookup"><span data-stu-id="36eea-280">True</span></span>                              |
| <span data-ttu-id="36eea-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36eea-281">Is Indexed</span></span>             | <span data-ttu-id="36eea-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-282">False</span></span>                             |
| <span data-ttu-id="36eea-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36eea-283">In Global Catalog</span></span>      | <span data-ttu-id="36eea-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="36eea-284">False</span></span>                             |
| <span data-ttu-id="36eea-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36eea-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="36eea-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36eea-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="36eea-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36eea-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="36eea-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36eea-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="36eea-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-289">Search-Flags</span></span>           | <span data-ttu-id="36eea-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36eea-290">0x00000000</span></span>                        |
| <span data-ttu-id="36eea-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36eea-291">System-Flags</span></span>           | <span data-ttu-id="36eea-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36eea-292">0x00000010</span></span>                        |
| <span data-ttu-id="36eea-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36eea-293">Classes used in</span></span>        | [<span data-ttu-id="36eea-294">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="36eea-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="36eea-295">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36eea-295">Remarks</span></span>

<span data-ttu-id="36eea-296">Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="36eea-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="36eea-297">Значение этого атрибута сбрасывается только при успешном входе в учетную запись.</span><span class="sxs-lookup"><span data-stu-id="36eea-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="36eea-298">Это означает, что это значение может быть не нулевым, но учетная запись не заблокирована. Чтобы точно определить, заблокирована ли учетная запись, необходимо добавить [**длительность блокировки**](a-lockoutduration.md) в это время и сравнить результат с текущим временем, учитывая местные Часовые пояса и летнее время.</span><span class="sxs-lookup"><span data-stu-id="36eea-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="36eea-299">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36eea-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36eea-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="36eea-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="36eea-301">**Продолжительность блокировки**</span><span class="sxs-lookup"><span data-stu-id="36eea-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

