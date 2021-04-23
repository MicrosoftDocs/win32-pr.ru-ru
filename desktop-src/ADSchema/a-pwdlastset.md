---
title: PWD-Last-Set, атрибут
description: Дата и время последнего изменения пароля для этой учетной записи.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- PWD-Last-Set схема AD атрибута
- Схема AD атрибута pwdLastSet
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655306"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="7ccad-105">PWD-Last-Set, атрибут</span><span class="sxs-lookup"><span data-stu-id="7ccad-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="7ccad-106">Дата и время последнего изменения пароля для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7ccad-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="7ccad-107">Это значение хранится в виде большого целого числа, представляющего количество интервалов в 100 нс, начиная с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="7ccad-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="7ccad-108">Если это значение равно 0, а атрибут [**User-Account-Control**](a-useraccountcontrol.md) не содержит флаг **УФ \_ не \_ Expires \_ PASSWD** , то пользователь должен задать пароль при следующем входе в систему.</span><span class="sxs-lookup"><span data-stu-id="7ccad-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="7ccad-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-109">Entry</span></span> | <span data-ttu-id="7ccad-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7ccad-111">CN</span><span class="sxs-lookup"><span data-stu-id="7ccad-111">CN</span></span>                | <span data-ttu-id="7ccad-112">PWD-Last-Set</span><span class="sxs-lookup"><span data-stu-id="7ccad-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="7ccad-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7ccad-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7ccad-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="7ccad-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="7ccad-115">Размер</span><span class="sxs-lookup"><span data-stu-id="7ccad-115">Size</span></span>              | <span data-ttu-id="7ccad-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="7ccad-116">8 bytes</span></span>                              |
| <span data-ttu-id="7ccad-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7ccad-117">Update Privilege</span></span>  | <span data-ttu-id="7ccad-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="7ccad-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="7ccad-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7ccad-119">Update Frequency</span></span>  | <span data-ttu-id="7ccad-120">При каждом изменении пароля.</span><span class="sxs-lookup"><span data-stu-id="7ccad-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="7ccad-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-121">Attribute-Id</span></span>      | <span data-ttu-id="7ccad-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="7ccad-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="7ccad-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7ccad-123">System-Id-Guid</span></span>    | <span data-ttu-id="7ccad-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7ccad-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7ccad-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ccad-125">Syntax</span></span>            | [<span data-ttu-id="7ccad-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="7ccad-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7ccad-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7ccad-127">Implementations</span></span>

-   [<span data-ttu-id="7ccad-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ccad-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ccad-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ccad-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ccad-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7ccad-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7ccad-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ccad-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ccad-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ccad-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ccad-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ccad-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ccad-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ccad-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ccad-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ccad-135">Windows 2000 Server</span></span>



| <span data-ttu-id="7ccad-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-136">Entry</span></span> | <span data-ttu-id="7ccad-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ccad-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-140">System-Only</span></span>            | <span data-ttu-id="7ccad-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-141">False</span></span>                             |
| <span data-ttu-id="7ccad-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-142">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-143">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-143">True</span></span>                              |
| <span data-ttu-id="7ccad-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-144">Is Indexed</span></span>             | <span data-ttu-id="7ccad-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-145">False</span></span>                             |
| <span data-ttu-id="7ccad-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-146">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-147">False</span></span>                             |
| <span data-ttu-id="7ccad-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ccad-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ccad-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ccad-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-152">Search-Flags</span></span>           | <span data-ttu-id="7ccad-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-153">0x00000000</span></span>                        |
| <span data-ttu-id="7ccad-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-154">System-Flags</span></span>           | <span data-ttu-id="7ccad-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-155">0x00000010</span></span>                        |
| <span data-ttu-id="7ccad-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-156">Classes used in</span></span>        | [<span data-ttu-id="7ccad-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="7ccad-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ccad-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ccad-158">Windows Server 2003</span></span>



| <span data-ttu-id="7ccad-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-159">Entry</span></span> | <span data-ttu-id="7ccad-160">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ccad-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-163">System-Only</span></span>            | <span data-ttu-id="7ccad-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-164">False</span></span>                             |
| <span data-ttu-id="7ccad-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-165">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-166">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-166">True</span></span>                              |
| <span data-ttu-id="7ccad-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-167">Is Indexed</span></span>             | <span data-ttu-id="7ccad-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-168">False</span></span>                             |
| <span data-ttu-id="7ccad-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-169">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-170">False</span></span>                             |
| <span data-ttu-id="7ccad-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ccad-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ccad-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ccad-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-175">Search-Flags</span></span>           | <span data-ttu-id="7ccad-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-176">0x00000000</span></span>                        |
| <span data-ttu-id="7ccad-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-177">System-Flags</span></span>           | <span data-ttu-id="7ccad-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-178">0x00000010</span></span>                        |
| <span data-ttu-id="7ccad-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-179">Classes used in</span></span>        | [<span data-ttu-id="7ccad-180">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="7ccad-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7ccad-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="7ccad-181">ADAM</span></span>



| <span data-ttu-id="7ccad-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-182">Entry</span></span> | <span data-ttu-id="7ccad-183">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7ccad-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7ccad-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7ccad-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-186">System-Only</span></span>            | <span data-ttu-id="7ccad-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-187">False</span></span>                                                             |
| <span data-ttu-id="7ccad-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-189">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-189">True</span></span>                                                              |
| <span data-ttu-id="7ccad-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-190">Is Indexed</span></span>             | <span data-ttu-id="7ccad-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-191">False</span></span>                                                             |
| <span data-ttu-id="7ccad-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-192">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-193">False</span></span>                                                             |
| <span data-ttu-id="7ccad-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7ccad-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7ccad-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7ccad-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-198">Search-Flags</span></span>           | <span data-ttu-id="7ccad-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="7ccad-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-200">System-Flags</span></span>           | <span data-ttu-id="7ccad-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="7ccad-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-202">Classes used in</span></span>        | [<span data-ttu-id="7ccad-203">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="7ccad-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ccad-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ccad-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ccad-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-205">Entry</span></span> | <span data-ttu-id="7ccad-206">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ccad-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-209">System-Only</span></span>            | <span data-ttu-id="7ccad-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-210">False</span></span>                             |
| <span data-ttu-id="7ccad-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-211">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-212">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-212">True</span></span>                              |
| <span data-ttu-id="7ccad-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-213">Is Indexed</span></span>             | <span data-ttu-id="7ccad-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-214">False</span></span>                             |
| <span data-ttu-id="7ccad-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-215">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-216">False</span></span>                             |
| <span data-ttu-id="7ccad-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ccad-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ccad-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ccad-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-221">Search-Flags</span></span>           | <span data-ttu-id="7ccad-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-222">0x00000000</span></span>                        |
| <span data-ttu-id="7ccad-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-223">System-Flags</span></span>           | <span data-ttu-id="7ccad-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-224">0x00000010</span></span>                        |
| <span data-ttu-id="7ccad-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-225">Classes used in</span></span>        | [<span data-ttu-id="7ccad-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="7ccad-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ccad-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ccad-227">Windows Server 2008</span></span>



| <span data-ttu-id="7ccad-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-228">Entry</span></span> | <span data-ttu-id="7ccad-229">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ccad-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-232">System-Only</span></span>            | <span data-ttu-id="7ccad-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-233">False</span></span>                             |
| <span data-ttu-id="7ccad-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-235">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-235">True</span></span>                              |
| <span data-ttu-id="7ccad-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-236">Is Indexed</span></span>             | <span data-ttu-id="7ccad-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-237">False</span></span>                             |
| <span data-ttu-id="7ccad-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-238">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-239">False</span></span>                             |
| <span data-ttu-id="7ccad-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ccad-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ccad-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ccad-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-244">Search-Flags</span></span>           | <span data-ttu-id="7ccad-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-245">0x00000000</span></span>                        |
| <span data-ttu-id="7ccad-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-246">System-Flags</span></span>           | <span data-ttu-id="7ccad-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-247">0x00000010</span></span>                        |
| <span data-ttu-id="7ccad-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-248">Classes used in</span></span>        | [<span data-ttu-id="7ccad-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="7ccad-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ccad-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ccad-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ccad-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-251">Entry</span></span> | <span data-ttu-id="7ccad-252">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ccad-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-255">System-Only</span></span>            | <span data-ttu-id="7ccad-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-256">False</span></span>                             |
| <span data-ttu-id="7ccad-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-257">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-258">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-258">True</span></span>                              |
| <span data-ttu-id="7ccad-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-259">Is Indexed</span></span>             | <span data-ttu-id="7ccad-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-260">False</span></span>                             |
| <span data-ttu-id="7ccad-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-261">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-262">False</span></span>                             |
| <span data-ttu-id="7ccad-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ccad-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ccad-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ccad-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-267">Search-Flags</span></span>           | <span data-ttu-id="7ccad-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-268">0x00000000</span></span>                        |
| <span data-ttu-id="7ccad-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-269">System-Flags</span></span>           | <span data-ttu-id="7ccad-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-270">0x00000010</span></span>                        |
| <span data-ttu-id="7ccad-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-271">Classes used in</span></span>        | [<span data-ttu-id="7ccad-272">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="7ccad-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ccad-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ccad-273">Windows Server 2012</span></span>



| <span data-ttu-id="7ccad-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ccad-274">Entry</span></span> | <span data-ttu-id="7ccad-275">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccad-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ccad-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ccad-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccad-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ccad-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccad-278">System-Only</span></span>            | <span data-ttu-id="7ccad-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-279">False</span></span>                             |
| <span data-ttu-id="7ccad-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ccad-280">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccad-281">True</span><span class="sxs-lookup"><span data-stu-id="7ccad-281">True</span></span>                              |
| <span data-ttu-id="7ccad-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ccad-282">Is Indexed</span></span>             | <span data-ttu-id="7ccad-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-283">False</span></span>                             |
| <span data-ttu-id="7ccad-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ccad-284">In Global Catalog</span></span>      | <span data-ttu-id="7ccad-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ccad-285">False</span></span>                             |
| <span data-ttu-id="7ccad-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ccad-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccad-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ccad-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ccad-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccad-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ccad-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccad-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ccad-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-290">Search-Flags</span></span>           | <span data-ttu-id="7ccad-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccad-291">0x00000000</span></span>                        |
| <span data-ttu-id="7ccad-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccad-292">System-Flags</span></span>           | <span data-ttu-id="7ccad-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccad-293">0x00000010</span></span>                        |
| <span data-ttu-id="7ccad-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ccad-294">Classes used in</span></span>        | [<span data-ttu-id="7ccad-295">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="7ccad-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7ccad-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ccad-296">Remarks</span></span>

<span data-ttu-id="7ccad-297">Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="7ccad-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ccad-298">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ccad-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccad-299">**Управление учетными записями пользователей**</span><span class="sxs-lookup"><span data-stu-id="7ccad-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

