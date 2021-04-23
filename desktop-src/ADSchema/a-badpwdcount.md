---
title: Недопустимый атрибут-PWD-Count
description: Число попыток входа пользователя в учетную запись с помощью неправильного пароля.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Неправильная схема AD атрибута-PWD-Count
- Схема AD атрибута badPwdCount
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138302"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="f4de4-105">Недопустимый атрибут-PWD-Count</span><span class="sxs-lookup"><span data-stu-id="f4de4-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="f4de4-106">Число попыток входа пользователя в учетную запись с помощью неправильного пароля.</span><span class="sxs-lookup"><span data-stu-id="f4de4-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="f4de4-107">Значение 0 указывает, что значение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f4de4-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="f4de4-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-108">Entry</span></span> | <span data-ttu-id="f4de4-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="f4de4-110">CN</span><span class="sxs-lookup"><span data-stu-id="f4de4-110">CN</span></span>                | <span data-ttu-id="f4de4-111">Bad-PWD-число</span><span class="sxs-lookup"><span data-stu-id="f4de4-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="f4de4-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f4de4-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f4de4-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="f4de4-113">badPwdCount</span></span>                               |
| <span data-ttu-id="f4de4-114">Размер</span><span class="sxs-lookup"><span data-stu-id="f4de4-114">Size</span></span>              | <span data-ttu-id="f4de4-115">4 байта</span><span class="sxs-lookup"><span data-stu-id="f4de4-115">4 bytes</span></span>                                   |
| <span data-ttu-id="f4de4-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f4de4-116">Update Privilege</span></span>  | <span data-ttu-id="f4de4-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="f4de4-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="f4de4-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f4de4-118">Update Frequency</span></span>  | <span data-ttu-id="f4de4-119">Каждый раз, когда пользователь вводит неправильный пароль.</span><span class="sxs-lookup"><span data-stu-id="f4de4-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="f4de4-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-120">Attribute-Id</span></span>      | <span data-ttu-id="f4de4-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="f4de4-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="f4de4-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f4de4-122">System-Id-Guid</span></span>    | <span data-ttu-id="f4de4-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f4de4-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="f4de4-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4de4-124">Syntax</span></span>            | [<span data-ttu-id="f4de4-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="f4de4-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="f4de4-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f4de4-126">Implementations</span></span>

-   [<span data-ttu-id="f4de4-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f4de4-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f4de4-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4de4-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4de4-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f4de4-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f4de4-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4de4-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4de4-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4de4-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4de4-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4de4-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4de4-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4de4-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f4de4-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4de4-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f4de4-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-135">Entry</span></span> | <span data-ttu-id="f4de4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4de4-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-139">System-Only</span></span>            | <span data-ttu-id="f4de4-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-140">False</span></span>                             |
| <span data-ttu-id="f4de4-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-142">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-142">True</span></span>                              |
| <span data-ttu-id="f4de4-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-143">Is Indexed</span></span>             | <span data-ttu-id="f4de4-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-144">False</span></span>                             |
| <span data-ttu-id="f4de4-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-145">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-146">False</span></span>                             |
| <span data-ttu-id="f4de4-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4de4-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4de4-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4de4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-151">Search-Flags</span></span>           | <span data-ttu-id="f4de4-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-152">0x00000000</span></span>                        |
| <span data-ttu-id="f4de4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-153">System-Flags</span></span>           | <span data-ttu-id="f4de4-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-154">0x00000011</span></span>                        |
| <span data-ttu-id="f4de4-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-155">Classes used in</span></span>        | [<span data-ttu-id="f4de4-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f4de4-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f4de4-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4de4-157">Windows Server 2003</span></span>



| <span data-ttu-id="f4de4-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-158">Entry</span></span> | <span data-ttu-id="f4de4-159">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4de4-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-162">System-Only</span></span>            | <span data-ttu-id="f4de4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-163">False</span></span>                             |
| <span data-ttu-id="f4de4-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-165">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-165">True</span></span>                              |
| <span data-ttu-id="f4de4-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-166">Is Indexed</span></span>             | <span data-ttu-id="f4de4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-167">False</span></span>                             |
| <span data-ttu-id="f4de4-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-168">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-169">False</span></span>                             |
| <span data-ttu-id="f4de4-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4de4-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4de4-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4de4-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-174">Search-Flags</span></span>           | <span data-ttu-id="f4de4-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-175">0x00000000</span></span>                        |
| <span data-ttu-id="f4de4-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-176">System-Flags</span></span>           | <span data-ttu-id="f4de4-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-177">0x00000011</span></span>                        |
| <span data-ttu-id="f4de4-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-178">Classes used in</span></span>        | [<span data-ttu-id="f4de4-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f4de4-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f4de4-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="f4de4-180">ADAM</span></span>



| <span data-ttu-id="f4de4-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-181">Entry</span></span> | <span data-ttu-id="f4de4-182">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4de4-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4de4-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4de4-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-185">System-Only</span></span>            | <span data-ttu-id="f4de4-186">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-186">True</span></span>                                                              |
| <span data-ttu-id="f4de4-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-188">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-188">True</span></span>                                                              |
| <span data-ttu-id="f4de4-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-189">Is Indexed</span></span>             | <span data-ttu-id="f4de4-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-190">False</span></span>                                                             |
| <span data-ttu-id="f4de4-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-191">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-192">False</span></span>                                                             |
| <span data-ttu-id="f4de4-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4de4-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4de4-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4de4-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-197">Search-Flags</span></span>           | <span data-ttu-id="f4de4-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4de4-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-199">System-Flags</span></span>           | <span data-ttu-id="f4de4-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="f4de4-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-201">Classes used in</span></span>        | [<span data-ttu-id="f4de4-202">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="f4de4-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4de4-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4de4-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4de4-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-204">Entry</span></span> | <span data-ttu-id="f4de4-205">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4de4-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-208">System-Only</span></span>            | <span data-ttu-id="f4de4-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-209">False</span></span>                             |
| <span data-ttu-id="f4de4-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-211">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-211">True</span></span>                              |
| <span data-ttu-id="f4de4-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-212">Is Indexed</span></span>             | <span data-ttu-id="f4de4-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-213">False</span></span>                             |
| <span data-ttu-id="f4de4-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-214">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-215">False</span></span>                             |
| <span data-ttu-id="f4de4-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4de4-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4de4-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4de4-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-220">Search-Flags</span></span>           | <span data-ttu-id="f4de4-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-221">0x00000000</span></span>                        |
| <span data-ttu-id="f4de4-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-222">System-Flags</span></span>           | <span data-ttu-id="f4de4-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-223">0x00000011</span></span>                        |
| <span data-ttu-id="f4de4-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-224">Classes used in</span></span>        | [<span data-ttu-id="f4de4-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f4de4-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4de4-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4de4-226">Windows Server 2008</span></span>



| <span data-ttu-id="f4de4-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-227">Entry</span></span> | <span data-ttu-id="f4de4-228">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4de4-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-231">System-Only</span></span>            | <span data-ttu-id="f4de4-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-232">False</span></span>                             |
| <span data-ttu-id="f4de4-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-234">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-234">True</span></span>                              |
| <span data-ttu-id="f4de4-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-235">Is Indexed</span></span>             | <span data-ttu-id="f4de4-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-236">False</span></span>                             |
| <span data-ttu-id="f4de4-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-237">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-238">False</span></span>                             |
| <span data-ttu-id="f4de4-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4de4-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4de4-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4de4-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-243">Search-Flags</span></span>           | <span data-ttu-id="f4de4-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-244">0x00000000</span></span>                        |
| <span data-ttu-id="f4de4-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-245">System-Flags</span></span>           | <span data-ttu-id="f4de4-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-246">0x00000011</span></span>                        |
| <span data-ttu-id="f4de4-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-247">Classes used in</span></span>        | [<span data-ttu-id="f4de4-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f4de4-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4de4-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4de4-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4de4-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-250">Entry</span></span> | <span data-ttu-id="f4de4-251">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4de4-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-254">System-Only</span></span>            | <span data-ttu-id="f4de4-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-255">False</span></span>                             |
| <span data-ttu-id="f4de4-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-257">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-257">True</span></span>                              |
| <span data-ttu-id="f4de4-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-258">Is Indexed</span></span>             | <span data-ttu-id="f4de4-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-259">False</span></span>                             |
| <span data-ttu-id="f4de4-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-260">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-261">False</span></span>                             |
| <span data-ttu-id="f4de4-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4de4-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4de4-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4de4-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-266">Search-Flags</span></span>           | <span data-ttu-id="f4de4-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-267">0x00000000</span></span>                        |
| <span data-ttu-id="f4de4-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-268">System-Flags</span></span>           | <span data-ttu-id="f4de4-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-269">0x00000011</span></span>                        |
| <span data-ttu-id="f4de4-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-270">Classes used in</span></span>        | [<span data-ttu-id="f4de4-271">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f4de4-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4de4-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4de4-272">Windows Server 2012</span></span>



| <span data-ttu-id="f4de4-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4de4-273">Entry</span></span> | <span data-ttu-id="f4de4-274">Значение</span><span class="sxs-lookup"><span data-stu-id="f4de4-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4de4-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4de4-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4de4-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4de4-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4de4-277">System-Only</span></span>            | <span data-ttu-id="f4de4-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-278">False</span></span>                             |
| <span data-ttu-id="f4de4-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4de4-279">Is-Single-Valued</span></span>       | <span data-ttu-id="f4de4-280">True</span><span class="sxs-lookup"><span data-stu-id="f4de4-280">True</span></span>                              |
| <span data-ttu-id="f4de4-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4de4-281">Is Indexed</span></span>             | <span data-ttu-id="f4de4-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-282">False</span></span>                             |
| <span data-ttu-id="f4de4-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4de4-283">In Global Catalog</span></span>      | <span data-ttu-id="f4de4-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4de4-284">False</span></span>                             |
| <span data-ttu-id="f4de4-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4de4-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4de4-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4de4-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4de4-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4de4-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4de4-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4de4-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4de4-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-289">Search-Flags</span></span>           | <span data-ttu-id="f4de4-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4de4-290">0x00000000</span></span>                        |
| <span data-ttu-id="f4de4-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4de4-291">System-Flags</span></span>           | <span data-ttu-id="f4de4-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f4de4-292">0x00000011</span></span>                        |
| <span data-ttu-id="f4de4-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4de4-293">Classes used in</span></span>        | [<span data-ttu-id="f4de4-294">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f4de4-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f4de4-295">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4de4-295">Remarks</span></span>

<span data-ttu-id="f4de4-296">Этот атрибут не реплицируется и хранится отдельно на каждом контроллере домена в домене.</span><span class="sxs-lookup"><span data-stu-id="f4de4-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="f4de4-297">Этот атрибут сбрасывается на конкретном контроллере домена, когда пользователь успешно входит в систему на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="f4de4-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 





