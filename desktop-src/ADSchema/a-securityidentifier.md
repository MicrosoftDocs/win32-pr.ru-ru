---
title: Атрибут Security-Identifier
description: Уникальное значение переменной длины, используемое для указания учетной записи пользователя, учетной записи группы или сеанса входа в систему, к которому применяется ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Security-Identifier
- Схема AD атрибута securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804547"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="2c434-105">Атрибут Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="2c434-105">Security-Identifier attribute</span></span>

<span data-ttu-id="2c434-106">Уникальное значение переменной длины, используемое для указания учетной записи пользователя, учетной записи группы или сеанса входа в систему, к которому применяется ACE.</span><span class="sxs-lookup"><span data-stu-id="2c434-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="2c434-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-107">Entry</span></span> | <span data-ttu-id="2c434-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2c434-109">CN</span><span class="sxs-lookup"><span data-stu-id="2c434-109">CN</span></span>                | <span data-ttu-id="2c434-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="2c434-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="2c434-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2c434-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2c434-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="2c434-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="2c434-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2c434-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="2c434-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2c434-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2c434-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2c434-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2c434-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-116">Attribute-Id</span></span>      | <span data-ttu-id="2c434-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="2c434-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="2c434-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2c434-118">System-Id-Guid</span></span>    | <span data-ttu-id="2c434-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2c434-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2c434-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c434-120">Syntax</span></span>            | [<span data-ttu-id="2c434-121">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="2c434-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="2c434-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2c434-122">Implementations</span></span>

-   [<span data-ttu-id="2c434-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c434-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c434-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c434-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c434-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c434-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c434-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c434-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c434-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c434-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c434-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c434-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c434-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c434-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2c434-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-130">Entry</span></span> | <span data-ttu-id="2c434-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c434-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c434-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c434-134">System-Only</span></span>            | <span data-ttu-id="2c434-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-135">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c434-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2c434-137">True</span><span class="sxs-lookup"><span data-stu-id="2c434-137">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c434-138">Is Indexed</span></span>             | <span data-ttu-id="2c434-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-139">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c434-140">In Global Catalog</span></span>      | <span data-ttu-id="2c434-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-141">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c434-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c434-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c434-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="2c434-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c434-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c434-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-146">Search-Flags</span></span>           | <span data-ttu-id="2c434-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c434-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="2c434-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-148">System-Flags</span></span>           | <span data-ttu-id="2c434-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c434-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="2c434-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c434-150">Classes used in</span></span>        | [<span data-ttu-id="2c434-151">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="2c434-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="2c434-152">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c434-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c434-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c434-153">Windows Server 2003</span></span>



| <span data-ttu-id="2c434-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-154">Entry</span></span> | <span data-ttu-id="2c434-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c434-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c434-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c434-158">System-Only</span></span>            | <span data-ttu-id="2c434-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-159">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c434-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2c434-161">True</span><span class="sxs-lookup"><span data-stu-id="2c434-161">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c434-162">Is Indexed</span></span>             | <span data-ttu-id="2c434-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-163">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c434-164">In Global Catalog</span></span>      | <span data-ttu-id="2c434-165">True</span><span class="sxs-lookup"><span data-stu-id="2c434-165">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c434-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c434-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c434-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="2c434-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c434-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c434-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-170">Search-Flags</span></span>           | <span data-ttu-id="2c434-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c434-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="2c434-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-172">System-Flags</span></span>           | <span data-ttu-id="2c434-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c434-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="2c434-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c434-174">Classes used in</span></span>        | [<span data-ttu-id="2c434-175">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="2c434-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="2c434-176">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c434-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c434-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c434-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c434-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-178">Entry</span></span> | <span data-ttu-id="2c434-179">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c434-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c434-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c434-182">System-Only</span></span>            | <span data-ttu-id="2c434-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-183">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c434-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2c434-185">True</span><span class="sxs-lookup"><span data-stu-id="2c434-185">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c434-186">Is Indexed</span></span>             | <span data-ttu-id="2c434-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-187">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c434-188">In Global Catalog</span></span>      | <span data-ttu-id="2c434-189">True</span><span class="sxs-lookup"><span data-stu-id="2c434-189">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c434-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c434-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c434-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="2c434-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c434-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c434-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-194">Search-Flags</span></span>           | <span data-ttu-id="2c434-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c434-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="2c434-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-196">System-Flags</span></span>           | <span data-ttu-id="2c434-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c434-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="2c434-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c434-198">Classes used in</span></span>        | [<span data-ttu-id="2c434-199">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="2c434-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="2c434-200">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c434-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c434-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c434-201">Windows Server 2008</span></span>



| <span data-ttu-id="2c434-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-202">Entry</span></span> | <span data-ttu-id="2c434-203">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c434-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c434-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c434-206">System-Only</span></span>            | <span data-ttu-id="2c434-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-207">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c434-208">Is-Single-Valued</span></span>       | <span data-ttu-id="2c434-209">True</span><span class="sxs-lookup"><span data-stu-id="2c434-209">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c434-210">Is Indexed</span></span>             | <span data-ttu-id="2c434-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-211">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c434-212">In Global Catalog</span></span>      | <span data-ttu-id="2c434-213">True</span><span class="sxs-lookup"><span data-stu-id="2c434-213">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c434-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c434-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c434-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="2c434-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c434-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c434-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-218">Search-Flags</span></span>           | <span data-ttu-id="2c434-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c434-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="2c434-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-220">System-Flags</span></span>           | <span data-ttu-id="2c434-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c434-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="2c434-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c434-222">Classes used in</span></span>        | [<span data-ttu-id="2c434-223">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="2c434-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="2c434-224">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c434-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c434-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c434-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c434-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-226">Entry</span></span> | <span data-ttu-id="2c434-227">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c434-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c434-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c434-230">System-Only</span></span>            | <span data-ttu-id="2c434-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-231">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c434-232">Is-Single-Valued</span></span>       | <span data-ttu-id="2c434-233">True</span><span class="sxs-lookup"><span data-stu-id="2c434-233">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c434-234">Is Indexed</span></span>             | <span data-ttu-id="2c434-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-235">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c434-236">In Global Catalog</span></span>      | <span data-ttu-id="2c434-237">True</span><span class="sxs-lookup"><span data-stu-id="2c434-237">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c434-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c434-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c434-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="2c434-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c434-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c434-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-242">Search-Flags</span></span>           | <span data-ttu-id="2c434-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c434-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="2c434-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-244">System-Flags</span></span>           | <span data-ttu-id="2c434-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c434-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="2c434-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c434-246">Classes used in</span></span>        | [<span data-ttu-id="2c434-247">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="2c434-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="2c434-248">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c434-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c434-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c434-249">Windows Server 2012</span></span>



| <span data-ttu-id="2c434-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c434-250">Entry</span></span> | <span data-ttu-id="2c434-251">Значение</span><span class="sxs-lookup"><span data-stu-id="2c434-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c434-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c434-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c434-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="2c434-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c434-254">System-Only</span></span>            | <span data-ttu-id="2c434-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-255">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c434-256">Is-Single-Valued</span></span>       | <span data-ttu-id="2c434-257">True</span><span class="sxs-lookup"><span data-stu-id="2c434-257">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c434-258">Is Indexed</span></span>             | <span data-ttu-id="2c434-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c434-259">False</span></span>                                                                                                             |
| <span data-ttu-id="2c434-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c434-260">In Global Catalog</span></span>      | <span data-ttu-id="2c434-261">True</span><span class="sxs-lookup"><span data-stu-id="2c434-261">True</span></span>                                                                                                              |
| <span data-ttu-id="2c434-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c434-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c434-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c434-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="2c434-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c434-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c434-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="2c434-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-266">Search-Flags</span></span>           | <span data-ttu-id="2c434-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c434-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="2c434-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c434-268">System-Flags</span></span>           | <span data-ttu-id="2c434-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c434-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="2c434-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c434-270">Classes used in</span></span>        | [<span data-ttu-id="2c434-271">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="2c434-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="2c434-272">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c434-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





