---
title: Атрибут Logon-Count
description: Количество раз, когда учетная запись была успешно зарегистрирована. Значение 0 указывает, что значение неизвестно.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Logon-Count
- Схема AD атрибута Логонкаунт
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893578"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="23e93-106">Атрибут Logon-Count</span><span class="sxs-lookup"><span data-stu-id="23e93-106">Logon-Count attribute</span></span>

<span data-ttu-id="23e93-107">Количество раз, когда учетная запись была успешно зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="23e93-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="23e93-108">Значение 0 указывает, что значение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="23e93-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="23e93-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-109">Entry</span></span> | <span data-ttu-id="23e93-110">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="23e93-111">CN</span><span class="sxs-lookup"><span data-stu-id="23e93-111">CN</span></span>                | <span data-ttu-id="23e93-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="23e93-112">Logon-Count</span></span>                          |
| <span data-ttu-id="23e93-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="23e93-113">Ldap-Display-Name</span></span> | <span data-ttu-id="23e93-114">логонкаунт</span><span class="sxs-lookup"><span data-stu-id="23e93-114">logonCount</span></span>                           |
| <span data-ttu-id="23e93-115">Размер</span><span class="sxs-lookup"><span data-stu-id="23e93-115">Size</span></span>              | <span data-ttu-id="23e93-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="23e93-116">4 bytes</span></span>                              |
| <span data-ttu-id="23e93-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="23e93-117">Update Privilege</span></span>  | <span data-ttu-id="23e93-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="23e93-118">Domain administrator</span></span>                 |
| <span data-ttu-id="23e93-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="23e93-119">Update Frequency</span></span>  | <span data-ttu-id="23e93-120">Каждый раз при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="23e93-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="23e93-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-121">Attribute-Id</span></span>      | <span data-ttu-id="23e93-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="23e93-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="23e93-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="23e93-123">System-Id-Guid</span></span>    | <span data-ttu-id="23e93-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="23e93-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="23e93-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23e93-125">Syntax</span></span>            | [<span data-ttu-id="23e93-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="23e93-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="23e93-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="23e93-127">Implementations</span></span>

-   [<span data-ttu-id="23e93-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="23e93-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="23e93-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="23e93-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="23e93-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="23e93-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="23e93-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="23e93-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="23e93-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="23e93-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="23e93-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="23e93-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="23e93-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23e93-134">Windows 2000 Server</span></span>



| <span data-ttu-id="23e93-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-135">Entry</span></span> | <span data-ttu-id="23e93-136">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23e93-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="23e93-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="23e93-139">System-Only</span></span>            | <span data-ttu-id="23e93-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-140">False</span></span>                             |
| <span data-ttu-id="23e93-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="23e93-141">Is-Single-Valued</span></span>       | <span data-ttu-id="23e93-142">True</span><span class="sxs-lookup"><span data-stu-id="23e93-142">True</span></span>                              |
| <span data-ttu-id="23e93-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="23e93-143">Is Indexed</span></span>             | <span data-ttu-id="23e93-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-144">False</span></span>                             |
| <span data-ttu-id="23e93-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="23e93-145">In Global Catalog</span></span>      | <span data-ttu-id="23e93-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-146">False</span></span>                             |
| <span data-ttu-id="23e93-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="23e93-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="23e93-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="23e93-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23e93-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23e93-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23e93-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23e93-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23e93-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-151">Search-Flags</span></span>           | <span data-ttu-id="23e93-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23e93-152">0x00000000</span></span>                        |
| <span data-ttu-id="23e93-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-153">System-Flags</span></span>           | <span data-ttu-id="23e93-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="23e93-154">0x00000011</span></span>                        |
| <span data-ttu-id="23e93-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="23e93-155">Classes used in</span></span>        | [<span data-ttu-id="23e93-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="23e93-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="23e93-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="23e93-157">Windows Server 2003</span></span>



| <span data-ttu-id="23e93-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-158">Entry</span></span> | <span data-ttu-id="23e93-159">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23e93-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="23e93-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="23e93-162">System-Only</span></span>            | <span data-ttu-id="23e93-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-163">False</span></span>                             |
| <span data-ttu-id="23e93-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="23e93-164">Is-Single-Valued</span></span>       | <span data-ttu-id="23e93-165">True</span><span class="sxs-lookup"><span data-stu-id="23e93-165">True</span></span>                              |
| <span data-ttu-id="23e93-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="23e93-166">Is Indexed</span></span>             | <span data-ttu-id="23e93-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-167">False</span></span>                             |
| <span data-ttu-id="23e93-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="23e93-168">In Global Catalog</span></span>      | <span data-ttu-id="23e93-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-169">False</span></span>                             |
| <span data-ttu-id="23e93-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="23e93-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="23e93-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="23e93-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23e93-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23e93-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23e93-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23e93-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23e93-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-174">Search-Flags</span></span>           | <span data-ttu-id="23e93-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23e93-175">0x00000000</span></span>                        |
| <span data-ttu-id="23e93-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-176">System-Flags</span></span>           | <span data-ttu-id="23e93-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="23e93-177">0x00000011</span></span>                        |
| <span data-ttu-id="23e93-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="23e93-178">Classes used in</span></span>        | [<span data-ttu-id="23e93-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="23e93-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="23e93-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="23e93-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="23e93-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-181">Entry</span></span> | <span data-ttu-id="23e93-182">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23e93-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="23e93-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="23e93-185">System-Only</span></span>            | <span data-ttu-id="23e93-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-186">False</span></span>                             |
| <span data-ttu-id="23e93-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="23e93-187">Is-Single-Valued</span></span>       | <span data-ttu-id="23e93-188">True</span><span class="sxs-lookup"><span data-stu-id="23e93-188">True</span></span>                              |
| <span data-ttu-id="23e93-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="23e93-189">Is Indexed</span></span>             | <span data-ttu-id="23e93-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-190">False</span></span>                             |
| <span data-ttu-id="23e93-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="23e93-191">In Global Catalog</span></span>      | <span data-ttu-id="23e93-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-192">False</span></span>                             |
| <span data-ttu-id="23e93-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="23e93-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="23e93-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="23e93-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23e93-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23e93-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23e93-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23e93-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23e93-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-197">Search-Flags</span></span>           | <span data-ttu-id="23e93-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23e93-198">0x00000000</span></span>                        |
| <span data-ttu-id="23e93-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-199">System-Flags</span></span>           | <span data-ttu-id="23e93-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="23e93-200">0x00000011</span></span>                        |
| <span data-ttu-id="23e93-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="23e93-201">Classes used in</span></span>        | [<span data-ttu-id="23e93-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="23e93-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="23e93-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23e93-203">Windows Server 2008</span></span>



| <span data-ttu-id="23e93-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-204">Entry</span></span> | <span data-ttu-id="23e93-205">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23e93-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="23e93-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="23e93-208">System-Only</span></span>            | <span data-ttu-id="23e93-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-209">False</span></span>                             |
| <span data-ttu-id="23e93-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="23e93-210">Is-Single-Valued</span></span>       | <span data-ttu-id="23e93-211">True</span><span class="sxs-lookup"><span data-stu-id="23e93-211">True</span></span>                              |
| <span data-ttu-id="23e93-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="23e93-212">Is Indexed</span></span>             | <span data-ttu-id="23e93-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-213">False</span></span>                             |
| <span data-ttu-id="23e93-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="23e93-214">In Global Catalog</span></span>      | <span data-ttu-id="23e93-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-215">False</span></span>                             |
| <span data-ttu-id="23e93-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="23e93-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="23e93-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="23e93-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23e93-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23e93-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23e93-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23e93-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23e93-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-220">Search-Flags</span></span>           | <span data-ttu-id="23e93-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23e93-221">0x00000000</span></span>                        |
| <span data-ttu-id="23e93-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-222">System-Flags</span></span>           | <span data-ttu-id="23e93-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="23e93-223">0x00000011</span></span>                        |
| <span data-ttu-id="23e93-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="23e93-224">Classes used in</span></span>        | [<span data-ttu-id="23e93-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="23e93-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="23e93-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="23e93-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="23e93-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-227">Entry</span></span> | <span data-ttu-id="23e93-228">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23e93-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="23e93-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="23e93-231">System-Only</span></span>            | <span data-ttu-id="23e93-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-232">False</span></span>                             |
| <span data-ttu-id="23e93-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="23e93-233">Is-Single-Valued</span></span>       | <span data-ttu-id="23e93-234">True</span><span class="sxs-lookup"><span data-stu-id="23e93-234">True</span></span>                              |
| <span data-ttu-id="23e93-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="23e93-235">Is Indexed</span></span>             | <span data-ttu-id="23e93-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-236">False</span></span>                             |
| <span data-ttu-id="23e93-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="23e93-237">In Global Catalog</span></span>      | <span data-ttu-id="23e93-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-238">False</span></span>                             |
| <span data-ttu-id="23e93-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="23e93-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="23e93-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="23e93-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23e93-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23e93-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23e93-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23e93-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23e93-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-243">Search-Flags</span></span>           | <span data-ttu-id="23e93-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23e93-244">0x00000000</span></span>                        |
| <span data-ttu-id="23e93-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-245">System-Flags</span></span>           | <span data-ttu-id="23e93-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="23e93-246">0x00000011</span></span>                        |
| <span data-ttu-id="23e93-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="23e93-247">Classes used in</span></span>        | [<span data-ttu-id="23e93-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="23e93-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="23e93-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23e93-249">Windows Server 2012</span></span>



| <span data-ttu-id="23e93-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="23e93-250">Entry</span></span> | <span data-ttu-id="23e93-251">Значение</span><span class="sxs-lookup"><span data-stu-id="23e93-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23e93-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="23e93-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23e93-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23e93-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="23e93-254">System-Only</span></span>            | <span data-ttu-id="23e93-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-255">False</span></span>                             |
| <span data-ttu-id="23e93-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="23e93-256">Is-Single-Valued</span></span>       | <span data-ttu-id="23e93-257">True</span><span class="sxs-lookup"><span data-stu-id="23e93-257">True</span></span>                              |
| <span data-ttu-id="23e93-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="23e93-258">Is Indexed</span></span>             | <span data-ttu-id="23e93-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-259">False</span></span>                             |
| <span data-ttu-id="23e93-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="23e93-260">In Global Catalog</span></span>      | <span data-ttu-id="23e93-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="23e93-261">False</span></span>                             |
| <span data-ttu-id="23e93-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="23e93-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="23e93-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="23e93-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23e93-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23e93-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23e93-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23e93-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23e93-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-266">Search-Flags</span></span>           | <span data-ttu-id="23e93-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23e93-267">0x00000000</span></span>                        |
| <span data-ttu-id="23e93-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23e93-268">System-Flags</span></span>           | <span data-ttu-id="23e93-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="23e93-269">0x00000011</span></span>                        |
| <span data-ttu-id="23e93-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="23e93-270">Classes used in</span></span>        | [<span data-ttu-id="23e93-271">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="23e93-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="23e93-272">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23e93-272">Remarks</span></span>

<span data-ttu-id="23e93-273">Этот атрибут не реплицируется и поддерживается на каждом контроллере домена в домене.</span><span class="sxs-lookup"><span data-stu-id="23e93-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="23e93-274">Чтобы получить точное значение общего числа успешных попыток входа в домен, необходимо запрашивать каждый контроллер домена в домене и использовать сумму значений.</span><span class="sxs-lookup"><span data-stu-id="23e93-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="23e93-275">Помните, что атрибут не реплицируется, поэтому контроллеры домена, которые были удалены, могут подсчитать входные данные для пользователя, и они будут отсутствовать в счетчике.</span><span class="sxs-lookup"><span data-stu-id="23e93-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23e93-276">Из-за совместимости с 16-разрядными версиями диспетчера LAN атрибут имеет верхний предел 65535.</span><span class="sxs-lookup"><span data-stu-id="23e93-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="23e93-277">После достижения этого предела вы не сможете использовать его в качестве индикатора активности пользователей на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="23e93-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 





