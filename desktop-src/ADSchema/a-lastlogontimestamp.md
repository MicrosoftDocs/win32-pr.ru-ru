---
title: Атрибут метки времени последнего входа
description: Время последнего входа пользователя в домен.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута метки времени последнего входа
- Схема AD атрибута lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138271"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="114d3-105">Атрибут метки времени последнего входа</span><span class="sxs-lookup"><span data-stu-id="114d3-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="114d3-106">Время последнего входа пользователя в домен.</span><span class="sxs-lookup"><span data-stu-id="114d3-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="114d3-107">Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="114d3-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="114d3-108">При каждом входе пользователя в систему значение этого атрибута считывается с контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="114d3-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="114d3-109">Если значение старше \[ `current_time - msDS-LogonTimeSyncInterval` \] , значение обновляется.</span><span class="sxs-lookup"><span data-stu-id="114d3-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="114d3-110">Начальное обновление после повышения функционального уровня домена вычисляется в течение 14 дней минус случайный процент от 5 дней.</span><span class="sxs-lookup"><span data-stu-id="114d3-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="114d3-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-111">Entry</span></span> | <span data-ttu-id="114d3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114d3-113">CN</span><span class="sxs-lookup"><span data-stu-id="114d3-113">CN</span></span>                | <span data-ttu-id="114d3-114">Метка времени последнего входа</span><span class="sxs-lookup"><span data-stu-id="114d3-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="114d3-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="114d3-115">Ldap-Display-Name</span></span> | <span data-ttu-id="114d3-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="114d3-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="114d3-117">Размер</span><span class="sxs-lookup"><span data-stu-id="114d3-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="114d3-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="114d3-118">Update Privilege</span></span>  | <span data-ttu-id="114d3-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="114d3-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="114d3-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="114d3-120">Update Frequency</span></span>  | <span data-ttu-id="114d3-121">При входе пользователя в систему и если это значение старше текущего времени минус значение msDS-ЛогонтимесинЦинтервал.</span><span class="sxs-lookup"><span data-stu-id="114d3-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="114d3-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-122">Attribute-Id</span></span>      | <span data-ttu-id="114d3-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="114d3-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="114d3-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="114d3-124">System-Id-Guid</span></span>    | <span data-ttu-id="114d3-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="114d3-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="114d3-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="114d3-126">Syntax</span></span>            | [<span data-ttu-id="114d3-127">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="114d3-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="114d3-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="114d3-128">Implementations</span></span>

-   [<span data-ttu-id="114d3-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="114d3-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="114d3-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="114d3-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="114d3-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="114d3-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="114d3-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="114d3-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="114d3-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="114d3-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="114d3-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="114d3-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="114d3-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="114d3-135">Windows Server 2003</span></span>



| <span data-ttu-id="114d3-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-136">Entry</span></span> | <span data-ttu-id="114d3-137">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="114d3-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="114d3-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d3-140">System-Only</span></span>            | <span data-ttu-id="114d3-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-141">False</span></span>                             |
| <span data-ttu-id="114d3-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="114d3-142">Is-Single-Valued</span></span>       | <span data-ttu-id="114d3-143">True</span><span class="sxs-lookup"><span data-stu-id="114d3-143">True</span></span>                              |
| <span data-ttu-id="114d3-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="114d3-144">Is Indexed</span></span>             | <span data-ttu-id="114d3-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-145">False</span></span>                             |
| <span data-ttu-id="114d3-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="114d3-146">In Global Catalog</span></span>      | <span data-ttu-id="114d3-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-147">False</span></span>                             |
| <span data-ttu-id="114d3-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="114d3-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d3-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="114d3-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="114d3-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d3-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="114d3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d3-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="114d3-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-152">Search-Flags</span></span>           | <span data-ttu-id="114d3-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d3-153">0x00000000</span></span>                        |
| <span data-ttu-id="114d3-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-154">System-Flags</span></span>           | <span data-ttu-id="114d3-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d3-155">0x00000010</span></span>                        |
| <span data-ttu-id="114d3-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="114d3-156">Classes used in</span></span>        | [<span data-ttu-id="114d3-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="114d3-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="114d3-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="114d3-158">ADAM</span></span>



| <span data-ttu-id="114d3-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-159">Entry</span></span> | <span data-ttu-id="114d3-160">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="114d3-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="114d3-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="114d3-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="114d3-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d3-163">System-Only</span></span>            | <span data-ttu-id="114d3-164">True</span><span class="sxs-lookup"><span data-stu-id="114d3-164">True</span></span>                                                              |
| <span data-ttu-id="114d3-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="114d3-165">Is-Single-Valued</span></span>       | <span data-ttu-id="114d3-166">True</span><span class="sxs-lookup"><span data-stu-id="114d3-166">True</span></span>                                                              |
| <span data-ttu-id="114d3-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="114d3-167">Is Indexed</span></span>             | <span data-ttu-id="114d3-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-168">False</span></span>                                                             |
| <span data-ttu-id="114d3-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="114d3-169">In Global Catalog</span></span>      | <span data-ttu-id="114d3-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-170">False</span></span>                                                             |
| <span data-ttu-id="114d3-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="114d3-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d3-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="114d3-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="114d3-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d3-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="114d3-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d3-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="114d3-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-175">Search-Flags</span></span>           | <span data-ttu-id="114d3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d3-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="114d3-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-177">System-Flags</span></span>           | <span data-ttu-id="114d3-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d3-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="114d3-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="114d3-179">Classes used in</span></span>        | [<span data-ttu-id="114d3-180">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="114d3-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="114d3-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="114d3-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="114d3-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-182">Entry</span></span> | <span data-ttu-id="114d3-183">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="114d3-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="114d3-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d3-186">System-Only</span></span>            | <span data-ttu-id="114d3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-187">False</span></span>                             |
| <span data-ttu-id="114d3-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="114d3-188">Is-Single-Valued</span></span>       | <span data-ttu-id="114d3-189">True</span><span class="sxs-lookup"><span data-stu-id="114d3-189">True</span></span>                              |
| <span data-ttu-id="114d3-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="114d3-190">Is Indexed</span></span>             | <span data-ttu-id="114d3-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-191">False</span></span>                             |
| <span data-ttu-id="114d3-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="114d3-192">In Global Catalog</span></span>      | <span data-ttu-id="114d3-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-193">False</span></span>                             |
| <span data-ttu-id="114d3-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="114d3-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d3-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="114d3-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="114d3-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d3-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="114d3-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d3-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="114d3-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-198">Search-Flags</span></span>           | <span data-ttu-id="114d3-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d3-199">0x00000000</span></span>                        |
| <span data-ttu-id="114d3-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-200">System-Flags</span></span>           | <span data-ttu-id="114d3-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d3-201">0x00000010</span></span>                        |
| <span data-ttu-id="114d3-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="114d3-202">Classes used in</span></span>        | [<span data-ttu-id="114d3-203">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="114d3-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="114d3-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="114d3-204">Windows Server 2008</span></span>



| <span data-ttu-id="114d3-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-205">Entry</span></span> | <span data-ttu-id="114d3-206">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="114d3-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="114d3-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d3-209">System-Only</span></span>            | <span data-ttu-id="114d3-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-210">False</span></span>                             |
| <span data-ttu-id="114d3-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="114d3-211">Is-Single-Valued</span></span>       | <span data-ttu-id="114d3-212">True</span><span class="sxs-lookup"><span data-stu-id="114d3-212">True</span></span>                              |
| <span data-ttu-id="114d3-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="114d3-213">Is Indexed</span></span>             | <span data-ttu-id="114d3-214">True</span><span class="sxs-lookup"><span data-stu-id="114d3-214">True</span></span>                              |
| <span data-ttu-id="114d3-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="114d3-215">In Global Catalog</span></span>      | <span data-ttu-id="114d3-216">True</span><span class="sxs-lookup"><span data-stu-id="114d3-216">True</span></span>                              |
| <span data-ttu-id="114d3-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="114d3-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d3-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="114d3-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="114d3-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d3-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="114d3-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d3-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="114d3-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-221">Search-Flags</span></span>           | <span data-ttu-id="114d3-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="114d3-222">0x00000001</span></span>                        |
| <span data-ttu-id="114d3-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-223">System-Flags</span></span>           | <span data-ttu-id="114d3-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d3-224">0x00000010</span></span>                        |
| <span data-ttu-id="114d3-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="114d3-225">Classes used in</span></span>        | [<span data-ttu-id="114d3-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="114d3-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="114d3-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="114d3-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="114d3-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-228">Entry</span></span> | <span data-ttu-id="114d3-229">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="114d3-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="114d3-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d3-232">System-Only</span></span>            | <span data-ttu-id="114d3-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-233">False</span></span>                             |
| <span data-ttu-id="114d3-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="114d3-234">Is-Single-Valued</span></span>       | <span data-ttu-id="114d3-235">True</span><span class="sxs-lookup"><span data-stu-id="114d3-235">True</span></span>                              |
| <span data-ttu-id="114d3-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="114d3-236">Is Indexed</span></span>             | <span data-ttu-id="114d3-237">True</span><span class="sxs-lookup"><span data-stu-id="114d3-237">True</span></span>                              |
| <span data-ttu-id="114d3-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="114d3-238">In Global Catalog</span></span>      | <span data-ttu-id="114d3-239">True</span><span class="sxs-lookup"><span data-stu-id="114d3-239">True</span></span>                              |
| <span data-ttu-id="114d3-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="114d3-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d3-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="114d3-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="114d3-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d3-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="114d3-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d3-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="114d3-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-244">Search-Flags</span></span>           | <span data-ttu-id="114d3-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="114d3-245">0x00000001</span></span>                        |
| <span data-ttu-id="114d3-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-246">System-Flags</span></span>           | <span data-ttu-id="114d3-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d3-247">0x00000010</span></span>                        |
| <span data-ttu-id="114d3-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="114d3-248">Classes used in</span></span>        | [<span data-ttu-id="114d3-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="114d3-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="114d3-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="114d3-250">Windows Server 2012</span></span>



| <span data-ttu-id="114d3-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="114d3-251">Entry</span></span> | <span data-ttu-id="114d3-252">Значение</span><span class="sxs-lookup"><span data-stu-id="114d3-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="114d3-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="114d3-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d3-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="114d3-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d3-255">System-Only</span></span>            | <span data-ttu-id="114d3-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="114d3-256">False</span></span>                             |
| <span data-ttu-id="114d3-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="114d3-257">Is-Single-Valued</span></span>       | <span data-ttu-id="114d3-258">True</span><span class="sxs-lookup"><span data-stu-id="114d3-258">True</span></span>                              |
| <span data-ttu-id="114d3-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="114d3-259">Is Indexed</span></span>             | <span data-ttu-id="114d3-260">True</span><span class="sxs-lookup"><span data-stu-id="114d3-260">True</span></span>                              |
| <span data-ttu-id="114d3-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="114d3-261">In Global Catalog</span></span>      | <span data-ttu-id="114d3-262">True</span><span class="sxs-lookup"><span data-stu-id="114d3-262">True</span></span>                              |
| <span data-ttu-id="114d3-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="114d3-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d3-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="114d3-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="114d3-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d3-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="114d3-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d3-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="114d3-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-267">Search-Flags</span></span>           | <span data-ttu-id="114d3-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="114d3-268">0x00000001</span></span>                        |
| <span data-ttu-id="114d3-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d3-269">System-Flags</span></span>           | <span data-ttu-id="114d3-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d3-270">0x00000010</span></span>                        |
| <span data-ttu-id="114d3-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="114d3-271">Classes used in</span></span>        | [<span data-ttu-id="114d3-272">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="114d3-272">**User**</span></span>](c-user.md)<br/> |



 

 





