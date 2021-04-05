---
title: атрибут DHCP-Servers
description: Содержит список серверов, разрешенных на предприятии.
ms.assetid: f712b2d2-ff9c-4ee2-aede-b68023e3e6b6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "DHCP-серверы"
- Схема AD атрибута Дхкпсерверс
topic_type:
- apiref
api_name:
- dhcp-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e43018c91e5bb495ee39476f07f40756cfcf097
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989540"
---
# <a name="dhcp-servers-attribute"></a><span data-ttu-id="b2dc0-105">атрибут DHCP-Servers</span><span class="sxs-lookup"><span data-stu-id="b2dc0-105">dhcp-Servers attribute</span></span>

<span data-ttu-id="b2dc0-106">Содержит список серверов, разрешенных на предприятии.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-106">Contains a list of servers that are authorized in the enterprise.</span></span>



| <span data-ttu-id="b2dc0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-107">Entry</span></span> | <span data-ttu-id="b2dc0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-108">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="b2dc0-109">CN</span><span class="sxs-lookup"><span data-stu-id="b2dc0-109">CN</span></span>                | <span data-ttu-id="b2dc0-110">DHCP-серверы</span><span class="sxs-lookup"><span data-stu-id="b2dc0-110">dhcp-Servers</span></span>                                           |
| <span data-ttu-id="b2dc0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b2dc0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b2dc0-112">дхкпсерверс</span><span class="sxs-lookup"><span data-stu-id="b2dc0-112">dhcpServers</span></span>                                            |
| <span data-ttu-id="b2dc0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b2dc0-113">Size</span></span>              | \-                                                     |
| <span data-ttu-id="b2dc0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b2dc0-114">Update Privilege</span></span>  | <span data-ttu-id="b2dc0-115">Администратор домена.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-115">Domain administrator.</span></span>                                  |
| <span data-ttu-id="b2dc0-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b2dc0-116">Update Frequency</span></span>  | <span data-ttu-id="b2dc0-117">При добавлении или удалении нового сервера из леса.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-117">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="b2dc0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-118">Attribute-Id</span></span>      | <span data-ttu-id="b2dc0-119">1.2.840.113556.1.4.704</span><span class="sxs-lookup"><span data-stu-id="b2dc0-119">1.2.840.113556.1.4.704</span></span>                                 |
| <span data-ttu-id="b2dc0-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b2dc0-120">System-Id-Guid</span></span>    | <span data-ttu-id="b2dc0-121">963d2745-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b2dc0-121">963d2745-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="b2dc0-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2dc0-122">Syntax</span></span>            | [<span data-ttu-id="b2dc0-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-123">**String(IA5)**</span></span>](s-string-ia5.md)                    |



## <a name="implementations"></a><span data-ttu-id="b2dc0-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b2dc0-124">Implementations</span></span>

-   [<span data-ttu-id="b2dc0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b2dc0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2dc0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2dc0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2dc0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2dc0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b2dc0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2dc0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b2dc0-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-132">Entry</span></span> | <span data-ttu-id="b2dc0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2dc0-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2dc0-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2dc0-136">System-Only</span></span>            | <span data-ttu-id="b2dc0-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-137">False</span></span>                                        |
| <span data-ttu-id="b2dc0-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2dc0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b2dc0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-139">False</span></span>                                        |
| <span data-ttu-id="b2dc0-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2dc0-140">Is Indexed</span></span>             | <span data-ttu-id="b2dc0-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-141">False</span></span>                                        |
| <span data-ttu-id="b2dc0-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2dc0-142">In Global Catalog</span></span>      | <span data-ttu-id="b2dc0-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-143">False</span></span>                                        |
| <span data-ttu-id="b2dc0-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2dc0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2dc0-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2dc0-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2dc0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2dc0-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2dc0-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-148">Search-Flags</span></span>           | <span data-ttu-id="b2dc0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2dc0-149">0x00000000</span></span>                                   |
| <span data-ttu-id="b2dc0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-150">System-Flags</span></span>           | <span data-ttu-id="b2dc0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2dc0-151">0x00000010</span></span>                                   |
| <span data-ttu-id="b2dc0-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2dc0-152">Classes used in</span></span>        | [<span data-ttu-id="b2dc0-153">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-153">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b2dc0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2dc0-154">Windows Server 2003</span></span>



| <span data-ttu-id="b2dc0-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-155">Entry</span></span> | <span data-ttu-id="b2dc0-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2dc0-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2dc0-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2dc0-159">System-Only</span></span>            | <span data-ttu-id="b2dc0-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-160">False</span></span>                                        |
| <span data-ttu-id="b2dc0-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2dc0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b2dc0-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-162">False</span></span>                                        |
| <span data-ttu-id="b2dc0-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2dc0-163">Is Indexed</span></span>             | <span data-ttu-id="b2dc0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-164">False</span></span>                                        |
| <span data-ttu-id="b2dc0-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2dc0-165">In Global Catalog</span></span>      | <span data-ttu-id="b2dc0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-166">False</span></span>                                        |
| <span data-ttu-id="b2dc0-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2dc0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2dc0-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2dc0-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2dc0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2dc0-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2dc0-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-171">Search-Flags</span></span>           | <span data-ttu-id="b2dc0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2dc0-172">0x00000000</span></span>                                   |
| <span data-ttu-id="b2dc0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-173">System-Flags</span></span>           | <span data-ttu-id="b2dc0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2dc0-174">0x00000010</span></span>                                   |
| <span data-ttu-id="b2dc0-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2dc0-175">Classes used in</span></span>        | [<span data-ttu-id="b2dc0-176">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-176">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2dc0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2dc0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2dc0-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-178">Entry</span></span> | <span data-ttu-id="b2dc0-179">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2dc0-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2dc0-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2dc0-182">System-Only</span></span>            | <span data-ttu-id="b2dc0-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-183">False</span></span>                                        |
| <span data-ttu-id="b2dc0-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2dc0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b2dc0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-185">False</span></span>                                        |
| <span data-ttu-id="b2dc0-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2dc0-186">Is Indexed</span></span>             | <span data-ttu-id="b2dc0-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-187">False</span></span>                                        |
| <span data-ttu-id="b2dc0-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2dc0-188">In Global Catalog</span></span>      | <span data-ttu-id="b2dc0-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-189">False</span></span>                                        |
| <span data-ttu-id="b2dc0-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2dc0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2dc0-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2dc0-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2dc0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2dc0-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2dc0-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-194">Search-Flags</span></span>           | <span data-ttu-id="b2dc0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2dc0-195">0x00000000</span></span>                                   |
| <span data-ttu-id="b2dc0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-196">System-Flags</span></span>           | <span data-ttu-id="b2dc0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2dc0-197">0x00000010</span></span>                                   |
| <span data-ttu-id="b2dc0-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2dc0-198">Classes used in</span></span>        | [<span data-ttu-id="b2dc0-199">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-199">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2dc0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2dc0-200">Windows Server 2008</span></span>



| <span data-ttu-id="b2dc0-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-201">Entry</span></span> | <span data-ttu-id="b2dc0-202">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2dc0-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2dc0-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2dc0-205">System-Only</span></span>            | <span data-ttu-id="b2dc0-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-206">False</span></span>                                        |
| <span data-ttu-id="b2dc0-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2dc0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b2dc0-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-208">False</span></span>                                        |
| <span data-ttu-id="b2dc0-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2dc0-209">Is Indexed</span></span>             | <span data-ttu-id="b2dc0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-210">False</span></span>                                        |
| <span data-ttu-id="b2dc0-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2dc0-211">In Global Catalog</span></span>      | <span data-ttu-id="b2dc0-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-212">False</span></span>                                        |
| <span data-ttu-id="b2dc0-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2dc0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2dc0-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2dc0-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2dc0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2dc0-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2dc0-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-217">Search-Flags</span></span>           | <span data-ttu-id="b2dc0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2dc0-218">0x00000000</span></span>                                   |
| <span data-ttu-id="b2dc0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-219">System-Flags</span></span>           | <span data-ttu-id="b2dc0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2dc0-220">0x00000010</span></span>                                   |
| <span data-ttu-id="b2dc0-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2dc0-221">Classes used in</span></span>        | [<span data-ttu-id="b2dc0-222">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-222">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2dc0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2dc0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2dc0-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-224">Entry</span></span> | <span data-ttu-id="b2dc0-225">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2dc0-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2dc0-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2dc0-228">System-Only</span></span>            | <span data-ttu-id="b2dc0-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-229">False</span></span>                                        |
| <span data-ttu-id="b2dc0-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2dc0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b2dc0-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-231">False</span></span>                                        |
| <span data-ttu-id="b2dc0-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2dc0-232">Is Indexed</span></span>             | <span data-ttu-id="b2dc0-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-233">False</span></span>                                        |
| <span data-ttu-id="b2dc0-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2dc0-234">In Global Catalog</span></span>      | <span data-ttu-id="b2dc0-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-235">False</span></span>                                        |
| <span data-ttu-id="b2dc0-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2dc0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2dc0-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2dc0-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2dc0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2dc0-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2dc0-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-240">Search-Flags</span></span>           | <span data-ttu-id="b2dc0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2dc0-241">0x00000000</span></span>                                   |
| <span data-ttu-id="b2dc0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-242">System-Flags</span></span>           | <span data-ttu-id="b2dc0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2dc0-243">0x00000010</span></span>                                   |
| <span data-ttu-id="b2dc0-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2dc0-244">Classes used in</span></span>        | [<span data-ttu-id="b2dc0-245">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-245">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2dc0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2dc0-246">Windows Server 2012</span></span>



| <span data-ttu-id="b2dc0-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2dc0-247">Entry</span></span> | <span data-ttu-id="b2dc0-248">Значение</span><span class="sxs-lookup"><span data-stu-id="b2dc0-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2dc0-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2dc0-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2dc0-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2dc0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2dc0-251">System-Only</span></span>            | <span data-ttu-id="b2dc0-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-252">False</span></span>                                        |
| <span data-ttu-id="b2dc0-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2dc0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b2dc0-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-254">False</span></span>                                        |
| <span data-ttu-id="b2dc0-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2dc0-255">Is Indexed</span></span>             | <span data-ttu-id="b2dc0-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-256">False</span></span>                                        |
| <span data-ttu-id="b2dc0-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2dc0-257">In Global Catalog</span></span>      | <span data-ttu-id="b2dc0-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2dc0-258">False</span></span>                                        |
| <span data-ttu-id="b2dc0-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2dc0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2dc0-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2dc0-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2dc0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2dc0-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2dc0-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2dc0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-263">Search-Flags</span></span>           | <span data-ttu-id="b2dc0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2dc0-264">0x00000000</span></span>                                   |
| <span data-ttu-id="b2dc0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2dc0-265">System-Flags</span></span>           | <span data-ttu-id="b2dc0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2dc0-266">0x00000010</span></span>                                   |
| <span data-ttu-id="b2dc0-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2dc0-267">Classes used in</span></span>        | [<span data-ttu-id="b2dc0-268">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="b2dc0-268">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





