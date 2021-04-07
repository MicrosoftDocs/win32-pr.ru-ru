---
title: Другие атрибуты имени входа и рабочих станций
description: Не \ 8211; Рабочие станции Windows NT или LAN Manager, с которых пользователь может войти в систему.
ms.assetid: feaa1ade-f340-4bca-8787-5ae5aa10d51c
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибутов других имен входа и рабочих станций
- Схема AD атрибута Осерлогинворкстатионс
topic_type:
- apiref
api_name:
- Other-Login-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b71032e96de9ac8d323da8a94e4c50c5cace27c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893325"
---
# <a name="other-login-workstations-attribute"></a><span data-ttu-id="46bf1-105">Другие атрибуты имени входа и рабочих станций</span><span class="sxs-lookup"><span data-stu-id="46bf1-105">Other-Login-Workstations attribute</span></span>

<span data-ttu-id="46bf1-106">Пользователи, не являющиеся рабочими станциями Windows NT или LAN Manager, с которых пользователь может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="46bf1-106">Non Windows NT or LAN Manager workstations from which a user can log on.</span></span>

> [!Note]  
> <span data-ttu-id="46bf1-107">Active Directory не использует или не заполняет это поле.</span><span class="sxs-lookup"><span data-stu-id="46bf1-107">Active Directory does not use or populate this field.</span></span>

 



| <span data-ttu-id="46bf1-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-108">Entry</span></span> | <span data-ttu-id="46bf1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="46bf1-110">CN</span><span class="sxs-lookup"><span data-stu-id="46bf1-110">CN</span></span>                | <span data-ttu-id="46bf1-111">Другие-входные рабочие станции</span><span class="sxs-lookup"><span data-stu-id="46bf1-111">Other-Login-Workstations</span></span>                    |
| <span data-ttu-id="46bf1-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="46bf1-112">Ldap-Display-Name</span></span> | <span data-ttu-id="46bf1-113">осерлогинворкстатионс</span><span class="sxs-lookup"><span data-stu-id="46bf1-113">otherLoginWorkstations</span></span>                      |
| <span data-ttu-id="46bf1-114">Размер</span><span class="sxs-lookup"><span data-stu-id="46bf1-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="46bf1-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="46bf1-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="46bf1-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="46bf1-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="46bf1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-117">Attribute-Id</span></span>      | <span data-ttu-id="46bf1-118">1.2.840.113556.1.4.91</span><span class="sxs-lookup"><span data-stu-id="46bf1-118">1.2.840.113556.1.4.91</span></span>                       |
| <span data-ttu-id="46bf1-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="46bf1-119">System-Id-Guid</span></span>    | <span data-ttu-id="46bf1-120">bf9679f1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="46bf1-120">bf9679f1-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="46bf1-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46bf1-121">Syntax</span></span>            | [<span data-ttu-id="46bf1-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="46bf1-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="46bf1-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="46bf1-123">Implementations</span></span>

-   [<span data-ttu-id="46bf1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46bf1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46bf1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46bf1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46bf1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46bf1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46bf1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46bf1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46bf1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46bf1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46bf1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46bf1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46bf1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46bf1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="46bf1-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-131">Entry</span></span> | <span data-ttu-id="46bf1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46bf1-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46bf1-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="46bf1-135">System-Only</span></span>            | <span data-ttu-id="46bf1-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-136">False</span></span>                             |
| <span data-ttu-id="46bf1-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46bf1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="46bf1-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-138">False</span></span>                             |
| <span data-ttu-id="46bf1-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46bf1-139">Is Indexed</span></span>             | <span data-ttu-id="46bf1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-140">False</span></span>                             |
| <span data-ttu-id="46bf1-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46bf1-141">In Global Catalog</span></span>      | <span data-ttu-id="46bf1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-142">False</span></span>                             |
| <span data-ttu-id="46bf1-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46bf1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="46bf1-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46bf1-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46bf1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46bf1-145">Range-Lower</span></span>            | <span data-ttu-id="46bf1-146">0</span><span class="sxs-lookup"><span data-stu-id="46bf1-146">0</span></span>                                 |
| <span data-ttu-id="46bf1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46bf1-147">Range-Upper</span></span>            | <span data-ttu-id="46bf1-148">1024</span><span class="sxs-lookup"><span data-stu-id="46bf1-148">1024</span></span>                              |
| <span data-ttu-id="46bf1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-149">Search-Flags</span></span>           | <span data-ttu-id="46bf1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-150">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-151">System-Flags</span></span>           | <span data-ttu-id="46bf1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-152">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46bf1-153">Classes used in</span></span>        | [<span data-ttu-id="46bf1-154">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="46bf1-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46bf1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46bf1-155">Windows Server 2003</span></span>



| <span data-ttu-id="46bf1-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-156">Entry</span></span> | <span data-ttu-id="46bf1-157">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46bf1-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46bf1-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="46bf1-160">System-Only</span></span>            | <span data-ttu-id="46bf1-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-161">False</span></span>                             |
| <span data-ttu-id="46bf1-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46bf1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="46bf1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-163">False</span></span>                             |
| <span data-ttu-id="46bf1-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46bf1-164">Is Indexed</span></span>             | <span data-ttu-id="46bf1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-165">False</span></span>                             |
| <span data-ttu-id="46bf1-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46bf1-166">In Global Catalog</span></span>      | <span data-ttu-id="46bf1-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-167">False</span></span>                             |
| <span data-ttu-id="46bf1-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46bf1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="46bf1-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46bf1-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46bf1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46bf1-170">Range-Lower</span></span>            | <span data-ttu-id="46bf1-171">0</span><span class="sxs-lookup"><span data-stu-id="46bf1-171">0</span></span>                                 |
| <span data-ttu-id="46bf1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46bf1-172">Range-Upper</span></span>            | <span data-ttu-id="46bf1-173">1024</span><span class="sxs-lookup"><span data-stu-id="46bf1-173">1024</span></span>                              |
| <span data-ttu-id="46bf1-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-174">Search-Flags</span></span>           | <span data-ttu-id="46bf1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-175">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-176">System-Flags</span></span>           | <span data-ttu-id="46bf1-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-177">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46bf1-178">Classes used in</span></span>        | [<span data-ttu-id="46bf1-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="46bf1-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46bf1-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46bf1-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46bf1-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-181">Entry</span></span> | <span data-ttu-id="46bf1-182">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46bf1-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46bf1-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="46bf1-185">System-Only</span></span>            | <span data-ttu-id="46bf1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-186">False</span></span>                             |
| <span data-ttu-id="46bf1-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46bf1-187">Is-Single-Valued</span></span>       | <span data-ttu-id="46bf1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-188">False</span></span>                             |
| <span data-ttu-id="46bf1-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46bf1-189">Is Indexed</span></span>             | <span data-ttu-id="46bf1-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-190">False</span></span>                             |
| <span data-ttu-id="46bf1-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46bf1-191">In Global Catalog</span></span>      | <span data-ttu-id="46bf1-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-192">False</span></span>                             |
| <span data-ttu-id="46bf1-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46bf1-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="46bf1-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46bf1-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46bf1-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46bf1-195">Range-Lower</span></span>            | <span data-ttu-id="46bf1-196">0</span><span class="sxs-lookup"><span data-stu-id="46bf1-196">0</span></span>                                 |
| <span data-ttu-id="46bf1-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46bf1-197">Range-Upper</span></span>            | <span data-ttu-id="46bf1-198">1024</span><span class="sxs-lookup"><span data-stu-id="46bf1-198">1024</span></span>                              |
| <span data-ttu-id="46bf1-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-199">Search-Flags</span></span>           | <span data-ttu-id="46bf1-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-200">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-201">System-Flags</span></span>           | <span data-ttu-id="46bf1-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-202">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46bf1-203">Classes used in</span></span>        | [<span data-ttu-id="46bf1-204">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="46bf1-204">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46bf1-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46bf1-205">Windows Server 2008</span></span>



| <span data-ttu-id="46bf1-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-206">Entry</span></span> | <span data-ttu-id="46bf1-207">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-207">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46bf1-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46bf1-208">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-209">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="46bf1-210">System-Only</span></span>            | <span data-ttu-id="46bf1-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-211">False</span></span>                             |
| <span data-ttu-id="46bf1-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46bf1-212">Is-Single-Valued</span></span>       | <span data-ttu-id="46bf1-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-213">False</span></span>                             |
| <span data-ttu-id="46bf1-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46bf1-214">Is Indexed</span></span>             | <span data-ttu-id="46bf1-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-215">False</span></span>                             |
| <span data-ttu-id="46bf1-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46bf1-216">In Global Catalog</span></span>      | <span data-ttu-id="46bf1-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-217">False</span></span>                             |
| <span data-ttu-id="46bf1-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46bf1-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="46bf1-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46bf1-219">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46bf1-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46bf1-220">Range-Lower</span></span>            | <span data-ttu-id="46bf1-221">0</span><span class="sxs-lookup"><span data-stu-id="46bf1-221">0</span></span>                                 |
| <span data-ttu-id="46bf1-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46bf1-222">Range-Upper</span></span>            | <span data-ttu-id="46bf1-223">1024</span><span class="sxs-lookup"><span data-stu-id="46bf1-223">1024</span></span>                              |
| <span data-ttu-id="46bf1-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-224">Search-Flags</span></span>           | <span data-ttu-id="46bf1-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-225">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-226">System-Flags</span></span>           | <span data-ttu-id="46bf1-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-227">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46bf1-228">Classes used in</span></span>        | [<span data-ttu-id="46bf1-229">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="46bf1-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46bf1-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46bf1-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46bf1-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-231">Entry</span></span> | <span data-ttu-id="46bf1-232">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46bf1-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46bf1-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="46bf1-235">System-Only</span></span>            | <span data-ttu-id="46bf1-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-236">False</span></span>                             |
| <span data-ttu-id="46bf1-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46bf1-237">Is-Single-Valued</span></span>       | <span data-ttu-id="46bf1-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-238">False</span></span>                             |
| <span data-ttu-id="46bf1-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46bf1-239">Is Indexed</span></span>             | <span data-ttu-id="46bf1-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-240">False</span></span>                             |
| <span data-ttu-id="46bf1-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46bf1-241">In Global Catalog</span></span>      | <span data-ttu-id="46bf1-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-242">False</span></span>                             |
| <span data-ttu-id="46bf1-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46bf1-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="46bf1-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46bf1-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46bf1-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46bf1-245">Range-Lower</span></span>            | <span data-ttu-id="46bf1-246">0</span><span class="sxs-lookup"><span data-stu-id="46bf1-246">0</span></span>                                 |
| <span data-ttu-id="46bf1-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46bf1-247">Range-Upper</span></span>            | <span data-ttu-id="46bf1-248">1024</span><span class="sxs-lookup"><span data-stu-id="46bf1-248">1024</span></span>                              |
| <span data-ttu-id="46bf1-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-249">Search-Flags</span></span>           | <span data-ttu-id="46bf1-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-250">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-251">System-Flags</span></span>           | <span data-ttu-id="46bf1-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-252">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46bf1-253">Classes used in</span></span>        | [<span data-ttu-id="46bf1-254">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="46bf1-254">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46bf1-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46bf1-255">Windows Server 2012</span></span>



| <span data-ttu-id="46bf1-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="46bf1-256">Entry</span></span> | <span data-ttu-id="46bf1-257">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf1-257">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46bf1-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="46bf1-258">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46bf1-259">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46bf1-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="46bf1-260">System-Only</span></span>            | <span data-ttu-id="46bf1-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-261">False</span></span>                             |
| <span data-ttu-id="46bf1-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="46bf1-262">Is-Single-Valued</span></span>       | <span data-ttu-id="46bf1-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-263">False</span></span>                             |
| <span data-ttu-id="46bf1-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="46bf1-264">Is Indexed</span></span>             | <span data-ttu-id="46bf1-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-265">False</span></span>                             |
| <span data-ttu-id="46bf1-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="46bf1-266">In Global Catalog</span></span>      | <span data-ttu-id="46bf1-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="46bf1-267">False</span></span>                             |
| <span data-ttu-id="46bf1-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="46bf1-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="46bf1-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46bf1-269">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46bf1-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46bf1-270">Range-Lower</span></span>            | <span data-ttu-id="46bf1-271">0</span><span class="sxs-lookup"><span data-stu-id="46bf1-271">0</span></span>                                 |
| <span data-ttu-id="46bf1-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46bf1-272">Range-Upper</span></span>            | <span data-ttu-id="46bf1-273">1024</span><span class="sxs-lookup"><span data-stu-id="46bf1-273">1024</span></span>                              |
| <span data-ttu-id="46bf1-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-274">Search-Flags</span></span>           | <span data-ttu-id="46bf1-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-275">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46bf1-276">System-Flags</span></span>           | <span data-ttu-id="46bf1-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46bf1-277">0x00000010</span></span>                        |
| <span data-ttu-id="46bf1-278">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="46bf1-278">Classes used in</span></span>        | [<span data-ttu-id="46bf1-279">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="46bf1-279">**User**</span></span>](c-user.md)<br/> |



 

 





