---
title: Атрибут Last-Logon
description: Время последнего входа пользователя в систему.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Last-Logon
- Схема AD атрибута Ластлогон
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893586"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="2b9bf-105">Атрибут Last-Logon</span><span class="sxs-lookup"><span data-stu-id="2b9bf-105">Last-Logon attribute</span></span>

<span data-ttu-id="2b9bf-106">Время последнего входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-106">The last time the user logged on.</span></span> <span data-ttu-id="2b9bf-107">Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="2b9bf-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="2b9bf-108">Нулевое значение означает, что время последнего входа неизвестно.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="2b9bf-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-109">Entry</span></span> | <span data-ttu-id="2b9bf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2b9bf-111">CN</span><span class="sxs-lookup"><span data-stu-id="2b9bf-111">CN</span></span>                | <span data-ttu-id="2b9bf-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="2b9bf-112">Last-Logon</span></span>                           |
| <span data-ttu-id="2b9bf-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2b9bf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2b9bf-114">ластлогон</span><span class="sxs-lookup"><span data-stu-id="2b9bf-114">lastLogon</span></span>                            |
| <span data-ttu-id="2b9bf-115">Размер</span><span class="sxs-lookup"><span data-stu-id="2b9bf-115">Size</span></span>              | <span data-ttu-id="2b9bf-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="2b9bf-116">8 bytes</span></span>                              |
| <span data-ttu-id="2b9bf-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2b9bf-117">Update Privilege</span></span>  | <span data-ttu-id="2b9bf-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="2b9bf-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2b9bf-119">Update Frequency</span></span>  | <span data-ttu-id="2b9bf-120">Каждый раз при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="2b9bf-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-121">Attribute-Id</span></span>      | <span data-ttu-id="2b9bf-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="2b9bf-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="2b9bf-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2b9bf-123">System-Id-Guid</span></span>    | <span data-ttu-id="2b9bf-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2b9bf-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2b9bf-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b9bf-125">Syntax</span></span>            | [<span data-ttu-id="2b9bf-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2b9bf-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2b9bf-127">Implementations</span></span>

-   [<span data-ttu-id="2b9bf-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b9bf-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b9bf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b9bf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b9bf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b9bf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b9bf-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b9bf-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2b9bf-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-135">Entry</span></span> | <span data-ttu-id="2b9bf-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b9bf-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9bf-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9bf-139">System-Only</span></span>            | <span data-ttu-id="2b9bf-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-140">False</span></span>                             |
| <span data-ttu-id="2b9bf-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9bf-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9bf-142">True</span><span class="sxs-lookup"><span data-stu-id="2b9bf-142">True</span></span>                              |
| <span data-ttu-id="2b9bf-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9bf-143">Is Indexed</span></span>             | <span data-ttu-id="2b9bf-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-144">False</span></span>                             |
| <span data-ttu-id="2b9bf-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9bf-145">In Global Catalog</span></span>      | <span data-ttu-id="2b9bf-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-146">False</span></span>                             |
| <span data-ttu-id="2b9bf-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9bf-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9bf-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9bf-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b9bf-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9bf-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9bf-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-151">Search-Flags</span></span>           | <span data-ttu-id="2b9bf-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9bf-152">0x00000000</span></span>                        |
| <span data-ttu-id="2b9bf-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-153">System-Flags</span></span>           | <span data-ttu-id="2b9bf-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2b9bf-154">0x00000011</span></span>                        |
| <span data-ttu-id="2b9bf-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9bf-155">Classes used in</span></span>        | [<span data-ttu-id="2b9bf-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b9bf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b9bf-157">Windows Server 2003</span></span>



| <span data-ttu-id="2b9bf-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-158">Entry</span></span> | <span data-ttu-id="2b9bf-159">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b9bf-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9bf-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9bf-162">System-Only</span></span>            | <span data-ttu-id="2b9bf-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-163">False</span></span>                             |
| <span data-ttu-id="2b9bf-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9bf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9bf-165">True</span><span class="sxs-lookup"><span data-stu-id="2b9bf-165">True</span></span>                              |
| <span data-ttu-id="2b9bf-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9bf-166">Is Indexed</span></span>             | <span data-ttu-id="2b9bf-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-167">False</span></span>                             |
| <span data-ttu-id="2b9bf-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9bf-168">In Global Catalog</span></span>      | <span data-ttu-id="2b9bf-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-169">False</span></span>                             |
| <span data-ttu-id="2b9bf-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9bf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9bf-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9bf-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b9bf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9bf-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9bf-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-174">Search-Flags</span></span>           | <span data-ttu-id="2b9bf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9bf-175">0x00000000</span></span>                        |
| <span data-ttu-id="2b9bf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-176">System-Flags</span></span>           | <span data-ttu-id="2b9bf-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2b9bf-177">0x00000011</span></span>                        |
| <span data-ttu-id="2b9bf-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9bf-178">Classes used in</span></span>        | [<span data-ttu-id="2b9bf-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b9bf-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b9bf-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b9bf-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-181">Entry</span></span> | <span data-ttu-id="2b9bf-182">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b9bf-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9bf-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9bf-185">System-Only</span></span>            | <span data-ttu-id="2b9bf-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-186">False</span></span>                             |
| <span data-ttu-id="2b9bf-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9bf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9bf-188">True</span><span class="sxs-lookup"><span data-stu-id="2b9bf-188">True</span></span>                              |
| <span data-ttu-id="2b9bf-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9bf-189">Is Indexed</span></span>             | <span data-ttu-id="2b9bf-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-190">False</span></span>                             |
| <span data-ttu-id="2b9bf-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9bf-191">In Global Catalog</span></span>      | <span data-ttu-id="2b9bf-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-192">False</span></span>                             |
| <span data-ttu-id="2b9bf-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9bf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9bf-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9bf-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b9bf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9bf-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9bf-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-197">Search-Flags</span></span>           | <span data-ttu-id="2b9bf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9bf-198">0x00000000</span></span>                        |
| <span data-ttu-id="2b9bf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-199">System-Flags</span></span>           | <span data-ttu-id="2b9bf-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2b9bf-200">0x00000011</span></span>                        |
| <span data-ttu-id="2b9bf-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9bf-201">Classes used in</span></span>        | [<span data-ttu-id="2b9bf-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b9bf-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b9bf-203">Windows Server 2008</span></span>



| <span data-ttu-id="2b9bf-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-204">Entry</span></span> | <span data-ttu-id="2b9bf-205">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b9bf-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9bf-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9bf-208">System-Only</span></span>            | <span data-ttu-id="2b9bf-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-209">False</span></span>                             |
| <span data-ttu-id="2b9bf-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9bf-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9bf-211">True</span><span class="sxs-lookup"><span data-stu-id="2b9bf-211">True</span></span>                              |
| <span data-ttu-id="2b9bf-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9bf-212">Is Indexed</span></span>             | <span data-ttu-id="2b9bf-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-213">False</span></span>                             |
| <span data-ttu-id="2b9bf-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9bf-214">In Global Catalog</span></span>      | <span data-ttu-id="2b9bf-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-215">False</span></span>                             |
| <span data-ttu-id="2b9bf-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9bf-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9bf-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9bf-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b9bf-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9bf-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9bf-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-220">Search-Flags</span></span>           | <span data-ttu-id="2b9bf-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9bf-221">0x00000000</span></span>                        |
| <span data-ttu-id="2b9bf-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-222">System-Flags</span></span>           | <span data-ttu-id="2b9bf-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2b9bf-223">0x00000011</span></span>                        |
| <span data-ttu-id="2b9bf-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9bf-224">Classes used in</span></span>        | [<span data-ttu-id="2b9bf-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b9bf-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b9bf-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b9bf-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-227">Entry</span></span> | <span data-ttu-id="2b9bf-228">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b9bf-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9bf-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9bf-231">System-Only</span></span>            | <span data-ttu-id="2b9bf-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-232">False</span></span>                             |
| <span data-ttu-id="2b9bf-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9bf-233">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9bf-234">True</span><span class="sxs-lookup"><span data-stu-id="2b9bf-234">True</span></span>                              |
| <span data-ttu-id="2b9bf-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9bf-235">Is Indexed</span></span>             | <span data-ttu-id="2b9bf-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-236">False</span></span>                             |
| <span data-ttu-id="2b9bf-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9bf-237">In Global Catalog</span></span>      | <span data-ttu-id="2b9bf-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-238">False</span></span>                             |
| <span data-ttu-id="2b9bf-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9bf-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9bf-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9bf-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b9bf-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9bf-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9bf-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-243">Search-Flags</span></span>           | <span data-ttu-id="2b9bf-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9bf-244">0x00000000</span></span>                        |
| <span data-ttu-id="2b9bf-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-245">System-Flags</span></span>           | <span data-ttu-id="2b9bf-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2b9bf-246">0x00000011</span></span>                        |
| <span data-ttu-id="2b9bf-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9bf-247">Classes used in</span></span>        | [<span data-ttu-id="2b9bf-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b9bf-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b9bf-249">Windows Server 2012</span></span>



| <span data-ttu-id="2b9bf-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9bf-250">Entry</span></span> | <span data-ttu-id="2b9bf-251">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9bf-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b9bf-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9bf-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9bf-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b9bf-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9bf-254">System-Only</span></span>            | <span data-ttu-id="2b9bf-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-255">False</span></span>                             |
| <span data-ttu-id="2b9bf-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9bf-256">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9bf-257">True</span><span class="sxs-lookup"><span data-stu-id="2b9bf-257">True</span></span>                              |
| <span data-ttu-id="2b9bf-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9bf-258">Is Indexed</span></span>             | <span data-ttu-id="2b9bf-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-259">False</span></span>                             |
| <span data-ttu-id="2b9bf-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9bf-260">In Global Catalog</span></span>      | <span data-ttu-id="2b9bf-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9bf-261">False</span></span>                             |
| <span data-ttu-id="2b9bf-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9bf-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9bf-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9bf-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b9bf-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9bf-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9bf-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b9bf-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-266">Search-Flags</span></span>           | <span data-ttu-id="2b9bf-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9bf-267">0x00000000</span></span>                        |
| <span data-ttu-id="2b9bf-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9bf-268">System-Flags</span></span>           | <span data-ttu-id="2b9bf-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2b9bf-269">0x00000011</span></span>                        |
| <span data-ttu-id="2b9bf-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9bf-270">Classes used in</span></span>        | [<span data-ttu-id="2b9bf-271">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2b9bf-272">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b9bf-272">Remarks</span></span>

<span data-ttu-id="2b9bf-273">Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="2b9bf-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="2b9bf-274">Этот атрибут не реплицируется и хранится отдельно на каждом контроллере домена в домене.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="2b9bf-275">Чтобы получить точное значение для последнего входа пользователя в домен, атрибут **последнего входа** пользователя должен быть получен из каждого контроллера домена в домене.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="2b9bf-276">Максимальное получаемое значение — это истинное время последнего входа для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b9bf-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b9bf-277">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b9bf-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b9bf-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="2b9bf-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

