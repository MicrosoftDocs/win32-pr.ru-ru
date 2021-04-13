---
title: Атрибут Logon-Hours
description: Часы, в которые пользователю разрешено выполнять вход в домен.
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Logon-Hours
- Схема AD атрибута Логонхаурс
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493578"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="eecba-105">Атрибут Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="eecba-105">Logon-Hours attribute</span></span>

<span data-ttu-id="eecba-106">Часы, в которые пользователю разрешено выполнять вход в домен.</span><span class="sxs-lookup"><span data-stu-id="eecba-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="eecba-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-107">Entry</span></span> | <span data-ttu-id="eecba-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="eecba-109">CN</span><span class="sxs-lookup"><span data-stu-id="eecba-109">CN</span></span>                | <span data-ttu-id="eecba-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="eecba-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="eecba-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="eecba-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eecba-112">логонхаурс</span><span class="sxs-lookup"><span data-stu-id="eecba-112">logonHours</span></span>                                            |
| <span data-ttu-id="eecba-113">Размер</span><span class="sxs-lookup"><span data-stu-id="eecba-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="eecba-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="eecba-114">Update Privilege</span></span>  | <span data-ttu-id="eecba-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="eecba-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="eecba-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="eecba-116">Update Frequency</span></span>  | <span data-ttu-id="eecba-117">Каждый раз, когда необходимо изменить время входа в учетную запись.</span><span class="sxs-lookup"><span data-stu-id="eecba-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="eecba-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-118">Attribute-Id</span></span>      | <span data-ttu-id="eecba-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="eecba-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="eecba-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="eecba-120">System-Id-Guid</span></span>    | <span data-ttu-id="eecba-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="eecba-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="eecba-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eecba-122">Syntax</span></span>            | [<span data-ttu-id="eecba-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="eecba-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="eecba-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="eecba-124">Implementations</span></span>

-   [<span data-ttu-id="eecba-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eecba-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eecba-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eecba-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eecba-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eecba-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eecba-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eecba-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eecba-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eecba-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eecba-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eecba-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eecba-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eecba-131">Windows 2000 Server</span></span>



| <span data-ttu-id="eecba-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-132">Entry</span></span> | <span data-ttu-id="eecba-133">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eecba-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eecba-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="eecba-136">System-Only</span></span>            | <span data-ttu-id="eecba-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-137">False</span></span>                             |
| <span data-ttu-id="eecba-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eecba-138">Is-Single-Valued</span></span>       | <span data-ttu-id="eecba-139">True</span><span class="sxs-lookup"><span data-stu-id="eecba-139">True</span></span>                              |
| <span data-ttu-id="eecba-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eecba-140">Is Indexed</span></span>             | <span data-ttu-id="eecba-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-141">False</span></span>                             |
| <span data-ttu-id="eecba-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eecba-142">In Global Catalog</span></span>      | <span data-ttu-id="eecba-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-143">False</span></span>                             |
| <span data-ttu-id="eecba-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eecba-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="eecba-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eecba-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eecba-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eecba-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eecba-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eecba-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eecba-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-148">Search-Flags</span></span>           | <span data-ttu-id="eecba-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-149">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-150">System-Flags</span></span>           | <span data-ttu-id="eecba-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-151">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eecba-152">Classes used in</span></span>        | [<span data-ttu-id="eecba-153">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="eecba-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eecba-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eecba-154">Windows Server 2003</span></span>



| <span data-ttu-id="eecba-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-155">Entry</span></span> | <span data-ttu-id="eecba-156">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eecba-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eecba-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="eecba-159">System-Only</span></span>            | <span data-ttu-id="eecba-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-160">False</span></span>                             |
| <span data-ttu-id="eecba-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eecba-161">Is-Single-Valued</span></span>       | <span data-ttu-id="eecba-162">True</span><span class="sxs-lookup"><span data-stu-id="eecba-162">True</span></span>                              |
| <span data-ttu-id="eecba-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eecba-163">Is Indexed</span></span>             | <span data-ttu-id="eecba-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-164">False</span></span>                             |
| <span data-ttu-id="eecba-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eecba-165">In Global Catalog</span></span>      | <span data-ttu-id="eecba-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-166">False</span></span>                             |
| <span data-ttu-id="eecba-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eecba-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="eecba-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eecba-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eecba-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eecba-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eecba-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eecba-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eecba-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-171">Search-Flags</span></span>           | <span data-ttu-id="eecba-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-172">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-173">System-Flags</span></span>           | <span data-ttu-id="eecba-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-174">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eecba-175">Classes used in</span></span>        | [<span data-ttu-id="eecba-176">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="eecba-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eecba-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eecba-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eecba-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-178">Entry</span></span> | <span data-ttu-id="eecba-179">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eecba-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eecba-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="eecba-182">System-Only</span></span>            | <span data-ttu-id="eecba-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-183">False</span></span>                             |
| <span data-ttu-id="eecba-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eecba-184">Is-Single-Valued</span></span>       | <span data-ttu-id="eecba-185">True</span><span class="sxs-lookup"><span data-stu-id="eecba-185">True</span></span>                              |
| <span data-ttu-id="eecba-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eecba-186">Is Indexed</span></span>             | <span data-ttu-id="eecba-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-187">False</span></span>                             |
| <span data-ttu-id="eecba-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eecba-188">In Global Catalog</span></span>      | <span data-ttu-id="eecba-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-189">False</span></span>                             |
| <span data-ttu-id="eecba-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eecba-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="eecba-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eecba-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eecba-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eecba-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eecba-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eecba-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eecba-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-194">Search-Flags</span></span>           | <span data-ttu-id="eecba-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-195">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-196">System-Flags</span></span>           | <span data-ttu-id="eecba-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-197">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eecba-198">Classes used in</span></span>        | [<span data-ttu-id="eecba-199">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="eecba-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eecba-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eecba-200">Windows Server 2008</span></span>



| <span data-ttu-id="eecba-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-201">Entry</span></span> | <span data-ttu-id="eecba-202">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eecba-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eecba-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="eecba-205">System-Only</span></span>            | <span data-ttu-id="eecba-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-206">False</span></span>                             |
| <span data-ttu-id="eecba-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eecba-207">Is-Single-Valued</span></span>       | <span data-ttu-id="eecba-208">True</span><span class="sxs-lookup"><span data-stu-id="eecba-208">True</span></span>                              |
| <span data-ttu-id="eecba-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eecba-209">Is Indexed</span></span>             | <span data-ttu-id="eecba-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-210">False</span></span>                             |
| <span data-ttu-id="eecba-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eecba-211">In Global Catalog</span></span>      | <span data-ttu-id="eecba-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-212">False</span></span>                             |
| <span data-ttu-id="eecba-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eecba-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="eecba-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eecba-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eecba-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eecba-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eecba-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eecba-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eecba-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-217">Search-Flags</span></span>           | <span data-ttu-id="eecba-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-218">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-219">System-Flags</span></span>           | <span data-ttu-id="eecba-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-220">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eecba-221">Classes used in</span></span>        | [<span data-ttu-id="eecba-222">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="eecba-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eecba-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eecba-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eecba-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-224">Entry</span></span> | <span data-ttu-id="eecba-225">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eecba-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eecba-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="eecba-228">System-Only</span></span>            | <span data-ttu-id="eecba-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-229">False</span></span>                             |
| <span data-ttu-id="eecba-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eecba-230">Is-Single-Valued</span></span>       | <span data-ttu-id="eecba-231">True</span><span class="sxs-lookup"><span data-stu-id="eecba-231">True</span></span>                              |
| <span data-ttu-id="eecba-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eecba-232">Is Indexed</span></span>             | <span data-ttu-id="eecba-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-233">False</span></span>                             |
| <span data-ttu-id="eecba-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eecba-234">In Global Catalog</span></span>      | <span data-ttu-id="eecba-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-235">False</span></span>                             |
| <span data-ttu-id="eecba-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eecba-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="eecba-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eecba-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eecba-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eecba-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eecba-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eecba-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eecba-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-240">Search-Flags</span></span>           | <span data-ttu-id="eecba-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-241">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-242">System-Flags</span></span>           | <span data-ttu-id="eecba-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-243">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eecba-244">Classes used in</span></span>        | [<span data-ttu-id="eecba-245">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="eecba-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eecba-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eecba-246">Windows Server 2012</span></span>



| <span data-ttu-id="eecba-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="eecba-247">Entry</span></span> | <span data-ttu-id="eecba-248">Значение</span><span class="sxs-lookup"><span data-stu-id="eecba-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eecba-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eecba-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eecba-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eecba-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="eecba-251">System-Only</span></span>            | <span data-ttu-id="eecba-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-252">False</span></span>                             |
| <span data-ttu-id="eecba-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eecba-253">Is-Single-Valued</span></span>       | <span data-ttu-id="eecba-254">True</span><span class="sxs-lookup"><span data-stu-id="eecba-254">True</span></span>                              |
| <span data-ttu-id="eecba-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eecba-255">Is Indexed</span></span>             | <span data-ttu-id="eecba-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-256">False</span></span>                             |
| <span data-ttu-id="eecba-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eecba-257">In Global Catalog</span></span>      | <span data-ttu-id="eecba-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="eecba-258">False</span></span>                             |
| <span data-ttu-id="eecba-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eecba-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="eecba-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eecba-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eecba-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eecba-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eecba-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eecba-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eecba-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-263">Search-Flags</span></span>           | <span data-ttu-id="eecba-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-264">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eecba-265">System-Flags</span></span>           | <span data-ttu-id="eecba-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eecba-266">0x00000010</span></span>                        |
| <span data-ttu-id="eecba-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eecba-267">Classes used in</span></span>        | [<span data-ttu-id="eecba-268">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="eecba-268">**User**</span></span>](c-user.md)<br/> |



 

 





