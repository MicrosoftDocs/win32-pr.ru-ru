---
title: Атрибут LM-PWD-History
description: Журнал паролей пользователя в одностороннем формате LAN Manager (LM). LM OWF используется для обеспечения совместимости с клиентами LAN Manager 2. x, Windows 95 и Windows 98.
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута LM-PWD-History
- Схема AD атрибута Лмпвдхистори
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893582"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="96710-106">Атрибут LM-PWD-History</span><span class="sxs-lookup"><span data-stu-id="96710-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="96710-107">Журнал паролей пользователя в одностороннем формате LAN Manager (LM).</span><span class="sxs-lookup"><span data-stu-id="96710-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="96710-108">Протокол LM OWF используется для обеспечения совместимости с LAN Manager 2. *x* клиентов, Windows 95 и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="96710-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="96710-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-109">Entry</span></span> | <span data-ttu-id="96710-110">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="96710-111">CN</span><span class="sxs-lookup"><span data-stu-id="96710-111">CN</span></span>                | <span data-ttu-id="96710-112">LM-PWD-History</span><span class="sxs-lookup"><span data-stu-id="96710-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="96710-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="96710-113">Ldap-Display-Name</span></span> | <span data-ttu-id="96710-114">лмпвдхистори</span><span class="sxs-lookup"><span data-stu-id="96710-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="96710-115">Размер</span><span class="sxs-lookup"><span data-stu-id="96710-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="96710-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="96710-116">Update Privilege</span></span>  | <span data-ttu-id="96710-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="96710-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="96710-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="96710-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="96710-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96710-119">Attribute-Id</span></span>      | <span data-ttu-id="96710-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="96710-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="96710-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="96710-121">System-Id-Guid</span></span>    | <span data-ttu-id="96710-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="96710-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="96710-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96710-123">Syntax</span></span>            | [<span data-ttu-id="96710-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="96710-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="96710-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="96710-125">Implementations</span></span>

-   [<span data-ttu-id="96710-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="96710-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="96710-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96710-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96710-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96710-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96710-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96710-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96710-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96710-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96710-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96710-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="96710-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96710-132">Windows 2000 Server</span></span>



| <span data-ttu-id="96710-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-133">Entry</span></span> | <span data-ttu-id="96710-134">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96710-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="96710-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96710-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="96710-137">System-Only</span></span>            | <span data-ttu-id="96710-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-138">False</span></span>                             |
| <span data-ttu-id="96710-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="96710-139">Is-Single-Valued</span></span>       | <span data-ttu-id="96710-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-140">False</span></span>                             |
| <span data-ttu-id="96710-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="96710-141">Is Indexed</span></span>             | <span data-ttu-id="96710-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-142">False</span></span>                             |
| <span data-ttu-id="96710-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="96710-143">In Global Catalog</span></span>      | <span data-ttu-id="96710-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-144">False</span></span>                             |
| <span data-ttu-id="96710-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="96710-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="96710-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96710-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96710-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96710-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="96710-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96710-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="96710-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-149">Search-Flags</span></span>           | <span data-ttu-id="96710-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96710-150">0x00000000</span></span>                        |
| <span data-ttu-id="96710-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-151">System-Flags</span></span>           | <span data-ttu-id="96710-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96710-152">0x00000010</span></span>                        |
| <span data-ttu-id="96710-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="96710-153">Classes used in</span></span>        | [<span data-ttu-id="96710-154">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="96710-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="96710-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96710-155">Windows Server 2003</span></span>



| <span data-ttu-id="96710-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-156">Entry</span></span> | <span data-ttu-id="96710-157">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96710-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="96710-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96710-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="96710-160">System-Only</span></span>            | <span data-ttu-id="96710-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-161">False</span></span>                             |
| <span data-ttu-id="96710-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="96710-162">Is-Single-Valued</span></span>       | <span data-ttu-id="96710-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-163">False</span></span>                             |
| <span data-ttu-id="96710-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="96710-164">Is Indexed</span></span>             | <span data-ttu-id="96710-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-165">False</span></span>                             |
| <span data-ttu-id="96710-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="96710-166">In Global Catalog</span></span>      | <span data-ttu-id="96710-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-167">False</span></span>                             |
| <span data-ttu-id="96710-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="96710-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="96710-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96710-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96710-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96710-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="96710-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96710-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="96710-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-172">Search-Flags</span></span>           | <span data-ttu-id="96710-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96710-173">0x00000000</span></span>                        |
| <span data-ttu-id="96710-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-174">System-Flags</span></span>           | <span data-ttu-id="96710-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96710-175">0x00000010</span></span>                        |
| <span data-ttu-id="96710-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="96710-176">Classes used in</span></span>        | [<span data-ttu-id="96710-177">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="96710-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96710-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96710-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96710-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-179">Entry</span></span> | <span data-ttu-id="96710-180">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96710-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="96710-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96710-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="96710-183">System-Only</span></span>            | <span data-ttu-id="96710-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-184">False</span></span>                             |
| <span data-ttu-id="96710-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="96710-185">Is-Single-Valued</span></span>       | <span data-ttu-id="96710-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-186">False</span></span>                             |
| <span data-ttu-id="96710-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="96710-187">Is Indexed</span></span>             | <span data-ttu-id="96710-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-188">False</span></span>                             |
| <span data-ttu-id="96710-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="96710-189">In Global Catalog</span></span>      | <span data-ttu-id="96710-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-190">False</span></span>                             |
| <span data-ttu-id="96710-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="96710-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="96710-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96710-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96710-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96710-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="96710-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96710-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="96710-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-195">Search-Flags</span></span>           | <span data-ttu-id="96710-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96710-196">0x00000000</span></span>                        |
| <span data-ttu-id="96710-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-197">System-Flags</span></span>           | <span data-ttu-id="96710-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96710-198">0x00000010</span></span>                        |
| <span data-ttu-id="96710-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="96710-199">Classes used in</span></span>        | [<span data-ttu-id="96710-200">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="96710-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="96710-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96710-201">Windows Server 2008</span></span>



| <span data-ttu-id="96710-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-202">Entry</span></span> | <span data-ttu-id="96710-203">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96710-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="96710-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96710-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="96710-206">System-Only</span></span>            | <span data-ttu-id="96710-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-207">False</span></span>                             |
| <span data-ttu-id="96710-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="96710-208">Is-Single-Valued</span></span>       | <span data-ttu-id="96710-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-209">False</span></span>                             |
| <span data-ttu-id="96710-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="96710-210">Is Indexed</span></span>             | <span data-ttu-id="96710-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-211">False</span></span>                             |
| <span data-ttu-id="96710-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="96710-212">In Global Catalog</span></span>      | <span data-ttu-id="96710-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-213">False</span></span>                             |
| <span data-ttu-id="96710-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="96710-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="96710-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96710-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96710-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96710-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="96710-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96710-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="96710-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-218">Search-Flags</span></span>           | <span data-ttu-id="96710-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96710-219">0x00000000</span></span>                        |
| <span data-ttu-id="96710-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-220">System-Flags</span></span>           | <span data-ttu-id="96710-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96710-221">0x00000010</span></span>                        |
| <span data-ttu-id="96710-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="96710-222">Classes used in</span></span>        | [<span data-ttu-id="96710-223">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="96710-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96710-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96710-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96710-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-225">Entry</span></span> | <span data-ttu-id="96710-226">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96710-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="96710-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96710-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="96710-229">System-Only</span></span>            | <span data-ttu-id="96710-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-230">False</span></span>                             |
| <span data-ttu-id="96710-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="96710-231">Is-Single-Valued</span></span>       | <span data-ttu-id="96710-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-232">False</span></span>                             |
| <span data-ttu-id="96710-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="96710-233">Is Indexed</span></span>             | <span data-ttu-id="96710-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-234">False</span></span>                             |
| <span data-ttu-id="96710-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="96710-235">In Global Catalog</span></span>      | <span data-ttu-id="96710-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-236">False</span></span>                             |
| <span data-ttu-id="96710-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="96710-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="96710-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96710-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96710-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96710-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="96710-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96710-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="96710-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-241">Search-Flags</span></span>           | <span data-ttu-id="96710-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96710-242">0x00000000</span></span>                        |
| <span data-ttu-id="96710-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-243">System-Flags</span></span>           | <span data-ttu-id="96710-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96710-244">0x00000010</span></span>                        |
| <span data-ttu-id="96710-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="96710-245">Classes used in</span></span>        | [<span data-ttu-id="96710-246">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="96710-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="96710-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96710-247">Windows Server 2012</span></span>



| <span data-ttu-id="96710-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="96710-248">Entry</span></span> | <span data-ttu-id="96710-249">Значение</span><span class="sxs-lookup"><span data-stu-id="96710-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96710-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="96710-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96710-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96710-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="96710-252">System-Only</span></span>            | <span data-ttu-id="96710-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-253">False</span></span>                             |
| <span data-ttu-id="96710-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="96710-254">Is-Single-Valued</span></span>       | <span data-ttu-id="96710-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-255">False</span></span>                             |
| <span data-ttu-id="96710-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="96710-256">Is Indexed</span></span>             | <span data-ttu-id="96710-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-257">False</span></span>                             |
| <span data-ttu-id="96710-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="96710-258">In Global Catalog</span></span>      | <span data-ttu-id="96710-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="96710-259">False</span></span>                             |
| <span data-ttu-id="96710-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="96710-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="96710-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96710-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96710-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96710-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="96710-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96710-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="96710-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-264">Search-Flags</span></span>           | <span data-ttu-id="96710-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96710-265">0x00000000</span></span>                        |
| <span data-ttu-id="96710-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96710-266">System-Flags</span></span>           | <span data-ttu-id="96710-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96710-267">0x00000010</span></span>                        |
| <span data-ttu-id="96710-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="96710-268">Classes used in</span></span>        | [<span data-ttu-id="96710-269">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="96710-269">**User**</span></span>](c-user.md)<br/> |



 

 





