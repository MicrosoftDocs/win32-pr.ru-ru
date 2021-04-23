---
title: атрибут типа DHCP
description: Тип DHCP-сервера.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута типа DHCP
- Схема AD атрибута Дхкптипе
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989538"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="a529f-105">атрибут типа DHCP</span><span class="sxs-lookup"><span data-stu-id="a529f-105">dhcp-Type attribute</span></span>

<span data-ttu-id="a529f-106">Тип DHCP-сервера.</span><span class="sxs-lookup"><span data-stu-id="a529f-106">The type of DHCP server.</span></span> <span data-ttu-id="a529f-107">Этот атрибут задается для всех объектов класса objectClass [**дхкпкласс**](c-dhcpclass.md).</span><span class="sxs-lookup"><span data-stu-id="a529f-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="a529f-108">Его значение определяет тип объекта:</span><span class="sxs-lookup"><span data-stu-id="a529f-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="a529f-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-109">Entry</span></span> | <span data-ttu-id="a529f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="a529f-111">CN</span><span class="sxs-lookup"><span data-stu-id="a529f-111">CN</span></span>                | <span data-ttu-id="a529f-112">Тип DHCP</span><span class="sxs-lookup"><span data-stu-id="a529f-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="a529f-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a529f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a529f-114">дхкптипе</span><span class="sxs-lookup"><span data-stu-id="a529f-114">dhcpType</span></span>                                               |
| <span data-ttu-id="a529f-115">Размер</span><span class="sxs-lookup"><span data-stu-id="a529f-115">Size</span></span>              | <span data-ttu-id="a529f-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="a529f-116">4 bytes</span></span>                                                |
| <span data-ttu-id="a529f-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a529f-117">Update Privilege</span></span>  | <span data-ttu-id="a529f-118">Администратор домена.</span><span class="sxs-lookup"><span data-stu-id="a529f-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="a529f-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a529f-119">Update Frequency</span></span>  | <span data-ttu-id="a529f-120">При добавлении или удалении нового сервера из леса.</span><span class="sxs-lookup"><span data-stu-id="a529f-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="a529f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-121">Attribute-Id</span></span>      | <span data-ttu-id="a529f-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="a529f-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="a529f-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a529f-123">System-Id-Guid</span></span>    | <span data-ttu-id="a529f-124">963d273b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a529f-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="a529f-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a529f-125">Syntax</span></span>            | [<span data-ttu-id="a529f-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a529f-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="a529f-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a529f-127">Implementations</span></span>

-   [<span data-ttu-id="a529f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a529f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a529f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a529f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a529f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a529f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a529f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a529f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a529f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a529f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a529f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a529f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a529f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a529f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a529f-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-135">Entry</span></span> | <span data-ttu-id="a529f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a529f-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a529f-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a529f-139">System-Only</span></span>            | <span data-ttu-id="a529f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-140">False</span></span>                                        |
| <span data-ttu-id="a529f-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a529f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a529f-142">True</span><span class="sxs-lookup"><span data-stu-id="a529f-142">True</span></span>                                         |
| <span data-ttu-id="a529f-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a529f-143">Is Indexed</span></span>             | <span data-ttu-id="a529f-144">True</span><span class="sxs-lookup"><span data-stu-id="a529f-144">True</span></span>                                         |
| <span data-ttu-id="a529f-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a529f-145">In Global Catalog</span></span>      | <span data-ttu-id="a529f-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-146">False</span></span>                                        |
| <span data-ttu-id="a529f-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a529f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a529f-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a529f-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a529f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a529f-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a529f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a529f-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a529f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-151">Search-Flags</span></span>           | <span data-ttu-id="a529f-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a529f-152">0x00000001</span></span>                                   |
| <span data-ttu-id="a529f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-153">System-Flags</span></span>           | <span data-ttu-id="a529f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a529f-154">0x00000010</span></span>                                   |
| <span data-ttu-id="a529f-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a529f-155">Classes used in</span></span>        | [<span data-ttu-id="a529f-156">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="a529f-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a529f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a529f-157">Windows Server 2003</span></span>



| <span data-ttu-id="a529f-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-158">Entry</span></span> | <span data-ttu-id="a529f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a529f-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a529f-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a529f-162">System-Only</span></span>            | <span data-ttu-id="a529f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-163">False</span></span>                                        |
| <span data-ttu-id="a529f-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a529f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a529f-165">True</span><span class="sxs-lookup"><span data-stu-id="a529f-165">True</span></span>                                         |
| <span data-ttu-id="a529f-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a529f-166">Is Indexed</span></span>             | <span data-ttu-id="a529f-167">True</span><span class="sxs-lookup"><span data-stu-id="a529f-167">True</span></span>                                         |
| <span data-ttu-id="a529f-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a529f-168">In Global Catalog</span></span>      | <span data-ttu-id="a529f-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-169">False</span></span>                                        |
| <span data-ttu-id="a529f-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a529f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a529f-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a529f-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a529f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a529f-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a529f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a529f-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a529f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-174">Search-Flags</span></span>           | <span data-ttu-id="a529f-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a529f-175">0x00000001</span></span>                                   |
| <span data-ttu-id="a529f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-176">System-Flags</span></span>           | <span data-ttu-id="a529f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a529f-177">0x00000010</span></span>                                   |
| <span data-ttu-id="a529f-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a529f-178">Classes used in</span></span>        | [<span data-ttu-id="a529f-179">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="a529f-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a529f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a529f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a529f-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-181">Entry</span></span> | <span data-ttu-id="a529f-182">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a529f-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a529f-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a529f-185">System-Only</span></span>            | <span data-ttu-id="a529f-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-186">False</span></span>                                        |
| <span data-ttu-id="a529f-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a529f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a529f-188">True</span><span class="sxs-lookup"><span data-stu-id="a529f-188">True</span></span>                                         |
| <span data-ttu-id="a529f-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a529f-189">Is Indexed</span></span>             | <span data-ttu-id="a529f-190">True</span><span class="sxs-lookup"><span data-stu-id="a529f-190">True</span></span>                                         |
| <span data-ttu-id="a529f-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a529f-191">In Global Catalog</span></span>      | <span data-ttu-id="a529f-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-192">False</span></span>                                        |
| <span data-ttu-id="a529f-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a529f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a529f-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a529f-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a529f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a529f-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a529f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a529f-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a529f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-197">Search-Flags</span></span>           | <span data-ttu-id="a529f-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a529f-198">0x00000001</span></span>                                   |
| <span data-ttu-id="a529f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-199">System-Flags</span></span>           | <span data-ttu-id="a529f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a529f-200">0x00000010</span></span>                                   |
| <span data-ttu-id="a529f-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a529f-201">Classes used in</span></span>        | [<span data-ttu-id="a529f-202">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="a529f-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a529f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a529f-203">Windows Server 2008</span></span>



| <span data-ttu-id="a529f-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-204">Entry</span></span> | <span data-ttu-id="a529f-205">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a529f-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a529f-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="a529f-208">System-Only</span></span>            | <span data-ttu-id="a529f-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-209">False</span></span>                                        |
| <span data-ttu-id="a529f-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a529f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="a529f-211">True</span><span class="sxs-lookup"><span data-stu-id="a529f-211">True</span></span>                                         |
| <span data-ttu-id="a529f-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a529f-212">Is Indexed</span></span>             | <span data-ttu-id="a529f-213">True</span><span class="sxs-lookup"><span data-stu-id="a529f-213">True</span></span>                                         |
| <span data-ttu-id="a529f-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a529f-214">In Global Catalog</span></span>      | <span data-ttu-id="a529f-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-215">False</span></span>                                        |
| <span data-ttu-id="a529f-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a529f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="a529f-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a529f-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a529f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a529f-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a529f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a529f-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a529f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-220">Search-Flags</span></span>           | <span data-ttu-id="a529f-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a529f-221">0x00000001</span></span>                                   |
| <span data-ttu-id="a529f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-222">System-Flags</span></span>           | <span data-ttu-id="a529f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a529f-223">0x00000010</span></span>                                   |
| <span data-ttu-id="a529f-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a529f-224">Classes used in</span></span>        | [<span data-ttu-id="a529f-225">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="a529f-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a529f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a529f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a529f-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-227">Entry</span></span> | <span data-ttu-id="a529f-228">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a529f-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a529f-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="a529f-231">System-Only</span></span>            | <span data-ttu-id="a529f-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-232">False</span></span>                                        |
| <span data-ttu-id="a529f-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a529f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="a529f-234">True</span><span class="sxs-lookup"><span data-stu-id="a529f-234">True</span></span>                                         |
| <span data-ttu-id="a529f-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a529f-235">Is Indexed</span></span>             | <span data-ttu-id="a529f-236">True</span><span class="sxs-lookup"><span data-stu-id="a529f-236">True</span></span>                                         |
| <span data-ttu-id="a529f-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a529f-237">In Global Catalog</span></span>      | <span data-ttu-id="a529f-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-238">False</span></span>                                        |
| <span data-ttu-id="a529f-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a529f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="a529f-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a529f-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a529f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a529f-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a529f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a529f-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a529f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-243">Search-Flags</span></span>           | <span data-ttu-id="a529f-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a529f-244">0x00000001</span></span>                                   |
| <span data-ttu-id="a529f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-245">System-Flags</span></span>           | <span data-ttu-id="a529f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a529f-246">0x00000010</span></span>                                   |
| <span data-ttu-id="a529f-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a529f-247">Classes used in</span></span>        | [<span data-ttu-id="a529f-248">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="a529f-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a529f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a529f-249">Windows Server 2012</span></span>



| <span data-ttu-id="a529f-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="a529f-250">Entry</span></span> | <span data-ttu-id="a529f-251">Значение</span><span class="sxs-lookup"><span data-stu-id="a529f-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a529f-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a529f-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a529f-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a529f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="a529f-254">System-Only</span></span>            | <span data-ttu-id="a529f-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-255">False</span></span>                                        |
| <span data-ttu-id="a529f-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a529f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="a529f-257">True</span><span class="sxs-lookup"><span data-stu-id="a529f-257">True</span></span>                                         |
| <span data-ttu-id="a529f-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a529f-258">Is Indexed</span></span>             | <span data-ttu-id="a529f-259">True</span><span class="sxs-lookup"><span data-stu-id="a529f-259">True</span></span>                                         |
| <span data-ttu-id="a529f-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a529f-260">In Global Catalog</span></span>      | <span data-ttu-id="a529f-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="a529f-261">False</span></span>                                        |
| <span data-ttu-id="a529f-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a529f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="a529f-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a529f-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a529f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a529f-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a529f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a529f-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a529f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-266">Search-Flags</span></span>           | <span data-ttu-id="a529f-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a529f-267">0x00000001</span></span>                                   |
| <span data-ttu-id="a529f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a529f-268">System-Flags</span></span>           | <span data-ttu-id="a529f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a529f-269">0x00000010</span></span>                                   |
| <span data-ttu-id="a529f-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a529f-270">Classes used in</span></span>        | [<span data-ttu-id="a529f-271">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="a529f-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





