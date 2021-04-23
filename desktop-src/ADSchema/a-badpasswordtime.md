---
title: Недопустимый атрибут времени с паролем
description: Последнее время и дата, когда попытка входа в эту учетную запись была выполнена с недопустимым паролем.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Неправильная схема AD атрибута времени пароля
- Схема AD атрибута аргументы badPasswordTime
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494103"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="38ca5-105">Недопустимый атрибут времени с паролем</span><span class="sxs-lookup"><span data-stu-id="38ca5-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="38ca5-106">Последнее время и дата, когда попытка входа в эту учетную запись была выполнена с недопустимым паролем.</span><span class="sxs-lookup"><span data-stu-id="38ca5-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="38ca5-107">Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="38ca5-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="38ca5-108">Нулевое значение означает, что при последнем использовании неверного пароля неизвестно.</span><span class="sxs-lookup"><span data-stu-id="38ca5-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="38ca5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-109">Entry</span></span> | <span data-ttu-id="38ca5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="38ca5-111">CN</span><span class="sxs-lookup"><span data-stu-id="38ca5-111">CN</span></span>                | <span data-ttu-id="38ca5-112">Ошибка-пароль-время</span><span class="sxs-lookup"><span data-stu-id="38ca5-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="38ca5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="38ca5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="38ca5-114">Аргументы badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="38ca5-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="38ca5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="38ca5-115">Size</span></span>              | <span data-ttu-id="38ca5-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="38ca5-116">8 bytes</span></span>                                   |
| <span data-ttu-id="38ca5-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="38ca5-117">Update Privilege</span></span>  | <span data-ttu-id="38ca5-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="38ca5-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="38ca5-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="38ca5-119">Update Frequency</span></span>  | <span data-ttu-id="38ca5-120">Каждый раз, когда пользователь вводит неправильный пароль.</span><span class="sxs-lookup"><span data-stu-id="38ca5-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="38ca5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-121">Attribute-Id</span></span>      | <span data-ttu-id="38ca5-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="38ca5-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="38ca5-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="38ca5-123">System-Id-Guid</span></span>    | <span data-ttu-id="38ca5-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="38ca5-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="38ca5-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38ca5-125">Syntax</span></span>            | [<span data-ttu-id="38ca5-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="38ca5-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="38ca5-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="38ca5-127">Implementations</span></span>

-   [<span data-ttu-id="38ca5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38ca5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38ca5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38ca5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38ca5-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="38ca5-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="38ca5-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38ca5-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38ca5-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38ca5-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38ca5-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38ca5-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38ca5-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38ca5-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38ca5-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38ca5-135">Windows 2000 Server</span></span>



| <span data-ttu-id="38ca5-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-136">Entry</span></span> | <span data-ttu-id="38ca5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38ca5-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-140">System-Only</span></span>            | <span data-ttu-id="38ca5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-141">False</span></span>                             |
| <span data-ttu-id="38ca5-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-143">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-143">True</span></span>                              |
| <span data-ttu-id="38ca5-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-144">Is Indexed</span></span>             | <span data-ttu-id="38ca5-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-145">False</span></span>                             |
| <span data-ttu-id="38ca5-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-146">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-147">False</span></span>                             |
| <span data-ttu-id="38ca5-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38ca5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38ca5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38ca5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-152">Search-Flags</span></span>           | <span data-ttu-id="38ca5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-153">0x00000000</span></span>                        |
| <span data-ttu-id="38ca5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-154">System-Flags</span></span>           | <span data-ttu-id="38ca5-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-155">0x00000011</span></span>                        |
| <span data-ttu-id="38ca5-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-156">Classes used in</span></span>        | [<span data-ttu-id="38ca5-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="38ca5-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38ca5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38ca5-158">Windows Server 2003</span></span>



| <span data-ttu-id="38ca5-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-159">Entry</span></span> | <span data-ttu-id="38ca5-160">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38ca5-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-163">System-Only</span></span>            | <span data-ttu-id="38ca5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-164">False</span></span>                             |
| <span data-ttu-id="38ca5-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-166">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-166">True</span></span>                              |
| <span data-ttu-id="38ca5-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-167">Is Indexed</span></span>             | <span data-ttu-id="38ca5-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-168">False</span></span>                             |
| <span data-ttu-id="38ca5-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-169">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-170">False</span></span>                             |
| <span data-ttu-id="38ca5-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38ca5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38ca5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38ca5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-175">Search-Flags</span></span>           | <span data-ttu-id="38ca5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-176">0x00000000</span></span>                        |
| <span data-ttu-id="38ca5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-177">System-Flags</span></span>           | <span data-ttu-id="38ca5-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-178">0x00000011</span></span>                        |
| <span data-ttu-id="38ca5-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-179">Classes used in</span></span>        | [<span data-ttu-id="38ca5-180">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="38ca5-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="38ca5-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="38ca5-181">ADAM</span></span>



| <span data-ttu-id="38ca5-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-182">Entry</span></span> | <span data-ttu-id="38ca5-183">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="38ca5-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="38ca5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="38ca5-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-186">System-Only</span></span>            | <span data-ttu-id="38ca5-187">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-187">True</span></span>                                                              |
| <span data-ttu-id="38ca5-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-188">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-189">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-189">True</span></span>                                                              |
| <span data-ttu-id="38ca5-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-190">Is Indexed</span></span>             | <span data-ttu-id="38ca5-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-191">False</span></span>                                                             |
| <span data-ttu-id="38ca5-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-192">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-193">False</span></span>                                                             |
| <span data-ttu-id="38ca5-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="38ca5-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="38ca5-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="38ca5-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-198">Search-Flags</span></span>           | <span data-ttu-id="38ca5-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="38ca5-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-200">System-Flags</span></span>           | <span data-ttu-id="38ca5-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="38ca5-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-202">Classes used in</span></span>        | [<span data-ttu-id="38ca5-203">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="38ca5-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38ca5-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38ca5-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38ca5-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-205">Entry</span></span> | <span data-ttu-id="38ca5-206">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38ca5-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-209">System-Only</span></span>            | <span data-ttu-id="38ca5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-210">False</span></span>                             |
| <span data-ttu-id="38ca5-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-211">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-212">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-212">True</span></span>                              |
| <span data-ttu-id="38ca5-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-213">Is Indexed</span></span>             | <span data-ttu-id="38ca5-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-214">False</span></span>                             |
| <span data-ttu-id="38ca5-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-215">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-216">False</span></span>                             |
| <span data-ttu-id="38ca5-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38ca5-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38ca5-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38ca5-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-221">Search-Flags</span></span>           | <span data-ttu-id="38ca5-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-222">0x00000000</span></span>                        |
| <span data-ttu-id="38ca5-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-223">System-Flags</span></span>           | <span data-ttu-id="38ca5-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-224">0x00000011</span></span>                        |
| <span data-ttu-id="38ca5-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-225">Classes used in</span></span>        | [<span data-ttu-id="38ca5-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="38ca5-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38ca5-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38ca5-227">Windows Server 2008</span></span>



| <span data-ttu-id="38ca5-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-228">Entry</span></span> | <span data-ttu-id="38ca5-229">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38ca5-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-232">System-Only</span></span>            | <span data-ttu-id="38ca5-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-233">False</span></span>                             |
| <span data-ttu-id="38ca5-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-234">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-235">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-235">True</span></span>                              |
| <span data-ttu-id="38ca5-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-236">Is Indexed</span></span>             | <span data-ttu-id="38ca5-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-237">False</span></span>                             |
| <span data-ttu-id="38ca5-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-238">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-239">False</span></span>                             |
| <span data-ttu-id="38ca5-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38ca5-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38ca5-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38ca5-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-244">Search-Flags</span></span>           | <span data-ttu-id="38ca5-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-245">0x00000000</span></span>                        |
| <span data-ttu-id="38ca5-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-246">System-Flags</span></span>           | <span data-ttu-id="38ca5-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-247">0x00000011</span></span>                        |
| <span data-ttu-id="38ca5-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-248">Classes used in</span></span>        | [<span data-ttu-id="38ca5-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="38ca5-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38ca5-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38ca5-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38ca5-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-251">Entry</span></span> | <span data-ttu-id="38ca5-252">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38ca5-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-255">System-Only</span></span>            | <span data-ttu-id="38ca5-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-256">False</span></span>                             |
| <span data-ttu-id="38ca5-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-257">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-258">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-258">True</span></span>                              |
| <span data-ttu-id="38ca5-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-259">Is Indexed</span></span>             | <span data-ttu-id="38ca5-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-260">False</span></span>                             |
| <span data-ttu-id="38ca5-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-261">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-262">False</span></span>                             |
| <span data-ttu-id="38ca5-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38ca5-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38ca5-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38ca5-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-267">Search-Flags</span></span>           | <span data-ttu-id="38ca5-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-268">0x00000000</span></span>                        |
| <span data-ttu-id="38ca5-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-269">System-Flags</span></span>           | <span data-ttu-id="38ca5-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-270">0x00000011</span></span>                        |
| <span data-ttu-id="38ca5-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-271">Classes used in</span></span>        | [<span data-ttu-id="38ca5-272">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="38ca5-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38ca5-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38ca5-273">Windows Server 2012</span></span>



| <span data-ttu-id="38ca5-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="38ca5-274">Entry</span></span> | <span data-ttu-id="38ca5-275">Значение</span><span class="sxs-lookup"><span data-stu-id="38ca5-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38ca5-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38ca5-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38ca5-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38ca5-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="38ca5-278">System-Only</span></span>            | <span data-ttu-id="38ca5-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-279">False</span></span>                             |
| <span data-ttu-id="38ca5-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38ca5-280">Is-Single-Valued</span></span>       | <span data-ttu-id="38ca5-281">True</span><span class="sxs-lookup"><span data-stu-id="38ca5-281">True</span></span>                              |
| <span data-ttu-id="38ca5-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38ca5-282">Is Indexed</span></span>             | <span data-ttu-id="38ca5-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-283">False</span></span>                             |
| <span data-ttu-id="38ca5-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38ca5-284">In Global Catalog</span></span>      | <span data-ttu-id="38ca5-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="38ca5-285">False</span></span>                             |
| <span data-ttu-id="38ca5-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38ca5-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="38ca5-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38ca5-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38ca5-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38ca5-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38ca5-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38ca5-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38ca5-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-290">Search-Flags</span></span>           | <span data-ttu-id="38ca5-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38ca5-291">0x00000000</span></span>                        |
| <span data-ttu-id="38ca5-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38ca5-292">System-Flags</span></span>           | <span data-ttu-id="38ca5-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="38ca5-293">0x00000011</span></span>                        |
| <span data-ttu-id="38ca5-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38ca5-294">Classes used in</span></span>        | [<span data-ttu-id="38ca5-295">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="38ca5-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="38ca5-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38ca5-296">Remarks</span></span>

<span data-ttu-id="38ca5-297">Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="38ca5-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="38ca5-298">Этот атрибут не реплицируется и хранится отдельно на каждом контроллере домена в домене.</span><span class="sxs-lookup"><span data-stu-id="38ca5-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="38ca5-299">Чтобы получить точное значение времени последнего неправильного пароля пользователя в домене, необходимо выполнить запрос к каждому контроллеру домена в домене.</span><span class="sxs-lookup"><span data-stu-id="38ca5-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="38ca5-300">Полученное максимальное значение представляет собой истинное время неправильного пароля.</span><span class="sxs-lookup"><span data-stu-id="38ca5-300">The largest value that is obtained represents the true bad password time.</span></span>

 

