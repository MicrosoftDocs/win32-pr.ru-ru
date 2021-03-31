---
title: Атрибут списка LDAP-Ипдени-List
description: Содержит список двоичных IP-адресов, которым запрещен доступ к серверу LDAP.
ms.assetid: 7d554d49-8934-4d71-b32f-8e59c22faf8c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "LDAP-Ипдени-List"
- Схема AD атрибута Лдапипденилист
topic_type:
- apiref
api_name:
- LDAP-IPDeny-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43246b5bb5786eefafc8598e9d729d9a2f308e08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138711"
---
# <a name="ldap-ipdeny-list-attribute"></a><span data-ttu-id="a9722-105">Атрибут списка LDAP-Ипдени-List</span><span class="sxs-lookup"><span data-stu-id="a9722-105">LDAP-IPDeny-List attribute</span></span>

<span data-ttu-id="a9722-106">Содержит список двоичных IP-адресов, которым запрещен доступ к серверу LDAP.</span><span class="sxs-lookup"><span data-stu-id="a9722-106">Holds a list of binary IP addresses that are denied access to an LDAP server.</span></span>



| <span data-ttu-id="a9722-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-107">Entry</span></span> | <span data-ttu-id="a9722-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a9722-109">CN</span><span class="sxs-lookup"><span data-stu-id="a9722-109">CN</span></span>                | <span data-ttu-id="a9722-110">Список LDAP-Ипдени-List</span><span class="sxs-lookup"><span data-stu-id="a9722-110">LDAP-IPDeny-List</span></span>                                      |
| <span data-ttu-id="a9722-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a9722-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a9722-112">лдапипденилист</span><span class="sxs-lookup"><span data-stu-id="a9722-112">lDAPIPDenyList</span></span>                                        |
| <span data-ttu-id="a9722-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a9722-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a9722-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a9722-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="a9722-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a9722-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="a9722-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-116">Attribute-Id</span></span>      | <span data-ttu-id="a9722-117">1.2.840.113556.1.4.844</span><span class="sxs-lookup"><span data-stu-id="a9722-117">1.2.840.113556.1.4.844</span></span>                                |
| <span data-ttu-id="a9722-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a9722-118">System-Id-Guid</span></span>    | <span data-ttu-id="a9722-119">7359a353-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a9722-119">7359a353-90f7-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="a9722-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9722-120">Syntax</span></span>            | [<span data-ttu-id="a9722-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="a9722-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a9722-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a9722-122">Implementations</span></span>

-   [<span data-ttu-id="a9722-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a9722-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a9722-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9722-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9722-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a9722-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a9722-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9722-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9722-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9722-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9722-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9722-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9722-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9722-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a9722-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9722-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a9722-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-131">Entry</span></span> | <span data-ttu-id="a9722-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-135">System-Only</span></span>            | <span data-ttu-id="a9722-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-136">False</span></span>                                            |
| <span data-ttu-id="a9722-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-138">False</span></span>                                            |
| <span data-ttu-id="a9722-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-139">Is Indexed</span></span>             | <span data-ttu-id="a9722-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-140">False</span></span>                                            |
| <span data-ttu-id="a9722-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-141">In Global Catalog</span></span>      | <span data-ttu-id="a9722-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-142">False</span></span>                                            |
| <span data-ttu-id="a9722-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-147">Search-Flags</span></span>           | <span data-ttu-id="a9722-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-148">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-149">System-Flags</span></span>           | <span data-ttu-id="a9722-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-150">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-151">Classes used in</span></span>        | [<span data-ttu-id="a9722-152">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a9722-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9722-153">Windows Server 2003</span></span>



| <span data-ttu-id="a9722-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-154">Entry</span></span> | <span data-ttu-id="a9722-155">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-158">System-Only</span></span>            | <span data-ttu-id="a9722-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-159">False</span></span>                                            |
| <span data-ttu-id="a9722-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-161">False</span></span>                                            |
| <span data-ttu-id="a9722-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-162">Is Indexed</span></span>             | <span data-ttu-id="a9722-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-163">False</span></span>                                            |
| <span data-ttu-id="a9722-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-164">In Global Catalog</span></span>      | <span data-ttu-id="a9722-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-165">False</span></span>                                            |
| <span data-ttu-id="a9722-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-170">Search-Flags</span></span>           | <span data-ttu-id="a9722-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-171">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-172">System-Flags</span></span>           | <span data-ttu-id="a9722-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-173">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-174">Classes used in</span></span>        | [<span data-ttu-id="a9722-175">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a9722-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="a9722-176">ADAM</span></span>



| <span data-ttu-id="a9722-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-177">Entry</span></span> | <span data-ttu-id="a9722-178">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-181">System-Only</span></span>            | <span data-ttu-id="a9722-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-182">False</span></span>                                            |
| <span data-ttu-id="a9722-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-184">False</span></span>                                            |
| <span data-ttu-id="a9722-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-185">Is Indexed</span></span>             | <span data-ttu-id="a9722-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-186">False</span></span>                                            |
| <span data-ttu-id="a9722-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-187">In Global Catalog</span></span>      | <span data-ttu-id="a9722-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-188">False</span></span>                                            |
| <span data-ttu-id="a9722-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-193">Search-Flags</span></span>           | <span data-ttu-id="a9722-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-194">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-195">System-Flags</span></span>           | <span data-ttu-id="a9722-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-196">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-197">Classes used in</span></span>        | [<span data-ttu-id="a9722-198">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9722-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9722-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9722-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-200">Entry</span></span> | <span data-ttu-id="a9722-201">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-204">System-Only</span></span>            | <span data-ttu-id="a9722-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-205">False</span></span>                                            |
| <span data-ttu-id="a9722-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-207">False</span></span>                                            |
| <span data-ttu-id="a9722-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-208">Is Indexed</span></span>             | <span data-ttu-id="a9722-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-209">False</span></span>                                            |
| <span data-ttu-id="a9722-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-210">In Global Catalog</span></span>      | <span data-ttu-id="a9722-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-211">False</span></span>                                            |
| <span data-ttu-id="a9722-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-216">Search-Flags</span></span>           | <span data-ttu-id="a9722-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-217">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-218">System-Flags</span></span>           | <span data-ttu-id="a9722-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-219">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-220">Classes used in</span></span>        | [<span data-ttu-id="a9722-221">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9722-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9722-222">Windows Server 2008</span></span>



| <span data-ttu-id="a9722-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-223">Entry</span></span> | <span data-ttu-id="a9722-224">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-227">System-Only</span></span>            | <span data-ttu-id="a9722-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-228">False</span></span>                                            |
| <span data-ttu-id="a9722-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-230">False</span></span>                                            |
| <span data-ttu-id="a9722-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-231">Is Indexed</span></span>             | <span data-ttu-id="a9722-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-232">False</span></span>                                            |
| <span data-ttu-id="a9722-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-233">In Global Catalog</span></span>      | <span data-ttu-id="a9722-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-234">False</span></span>                                            |
| <span data-ttu-id="a9722-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-239">Search-Flags</span></span>           | <span data-ttu-id="a9722-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-240">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-241">System-Flags</span></span>           | <span data-ttu-id="a9722-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-242">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-243">Classes used in</span></span>        | [<span data-ttu-id="a9722-244">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9722-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9722-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9722-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-246">Entry</span></span> | <span data-ttu-id="a9722-247">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-250">System-Only</span></span>            | <span data-ttu-id="a9722-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-251">False</span></span>                                            |
| <span data-ttu-id="a9722-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-253">False</span></span>                                            |
| <span data-ttu-id="a9722-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-254">Is Indexed</span></span>             | <span data-ttu-id="a9722-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-255">False</span></span>                                            |
| <span data-ttu-id="a9722-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-256">In Global Catalog</span></span>      | <span data-ttu-id="a9722-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-257">False</span></span>                                            |
| <span data-ttu-id="a9722-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-262">Search-Flags</span></span>           | <span data-ttu-id="a9722-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-263">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-264">System-Flags</span></span>           | <span data-ttu-id="a9722-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-265">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-266">Classes used in</span></span>        | [<span data-ttu-id="a9722-267">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9722-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9722-268">Windows Server 2012</span></span>



| <span data-ttu-id="a9722-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9722-269">Entry</span></span> | <span data-ttu-id="a9722-270">Значение</span><span class="sxs-lookup"><span data-stu-id="a9722-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a9722-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9722-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9722-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a9722-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9722-273">System-Only</span></span>            | <span data-ttu-id="a9722-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-274">False</span></span>                                            |
| <span data-ttu-id="a9722-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9722-275">Is-Single-Valued</span></span>       | <span data-ttu-id="a9722-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-276">False</span></span>                                            |
| <span data-ttu-id="a9722-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9722-277">Is Indexed</span></span>             | <span data-ttu-id="a9722-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-278">False</span></span>                                            |
| <span data-ttu-id="a9722-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9722-279">In Global Catalog</span></span>      | <span data-ttu-id="a9722-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9722-280">False</span></span>                                            |
| <span data-ttu-id="a9722-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9722-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9722-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9722-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a9722-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9722-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a9722-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9722-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a9722-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-285">Search-Flags</span></span>           | <span data-ttu-id="a9722-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9722-286">0x00000000</span></span>                                       |
| <span data-ttu-id="a9722-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9722-287">System-Flags</span></span>           | <span data-ttu-id="a9722-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9722-288">0x00000010</span></span>                                       |
| <span data-ttu-id="a9722-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9722-289">Classes used in</span></span>        | [<span data-ttu-id="a9722-290">**Политика запроса**</span><span class="sxs-lookup"><span data-stu-id="a9722-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





