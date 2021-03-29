---
title: Атрибут Mscope-Id
description: Указывает, что на указанном DHCP-сервере присутствует многоадресная область.
ms.assetid: 376e3699-d261-4278-a073-0cf2e5b8193b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Mscope-Id
- Схема AD атрибута Мскопеид
topic_type:
- apiref
api_name:
- Mscope-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6437e273fdc93137c7fe99047524e6b2475265d7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535771"
---
# <a name="mscope-id-attribute"></a><span data-ttu-id="56c1c-105">Атрибут Mscope-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-105">Mscope-Id attribute</span></span>

<span data-ttu-id="56c1c-106">Указывает, что на указанном DHCP-сервере присутствует многоадресная область.</span><span class="sxs-lookup"><span data-stu-id="56c1c-106">Indicates that there is a multicast scope on the specified DHCP server.</span></span>



| <span data-ttu-id="56c1c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-107">Entry</span></span> | <span data-ttu-id="56c1c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="56c1c-109">CN</span><span class="sxs-lookup"><span data-stu-id="56c1c-109">CN</span></span>                | <span data-ttu-id="56c1c-110">Mscope-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-110">Mscope-Id</span></span>                            |
| <span data-ttu-id="56c1c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="56c1c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="56c1c-112">мскопеид</span><span class="sxs-lookup"><span data-stu-id="56c1c-112">mscopeId</span></span>                             |
| <span data-ttu-id="56c1c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="56c1c-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="56c1c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="56c1c-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="56c1c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="56c1c-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="56c1c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-116">Attribute-Id</span></span>      | <span data-ttu-id="56c1c-117">1.2.840.113556.1.4.716</span><span class="sxs-lookup"><span data-stu-id="56c1c-117">1.2.840.113556.1.4.716</span></span>               |
| <span data-ttu-id="56c1c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="56c1c-118">System-Id-Guid</span></span>    | <span data-ttu-id="56c1c-119">963d2751-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="56c1c-119">963d2751-48be-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="56c1c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56c1c-120">Syntax</span></span>            | [<span data-ttu-id="56c1c-121">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="56c1c-121">**String(IA5)**</span></span>](s-string-ia5.md)  |



## <a name="implementations"></a><span data-ttu-id="56c1c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="56c1c-122">Implementations</span></span>

-   [<span data-ttu-id="56c1c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="56c1c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="56c1c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56c1c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56c1c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56c1c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56c1c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56c1c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56c1c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56c1c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56c1c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56c1c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="56c1c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56c1c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="56c1c-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-130">Entry</span></span> | <span data-ttu-id="56c1c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="56c1c-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56c1c-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="56c1c-134">System-Only</span></span>            | <span data-ttu-id="56c1c-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-135">False</span></span>                                        |
| <span data-ttu-id="56c1c-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56c1c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="56c1c-137">True</span><span class="sxs-lookup"><span data-stu-id="56c1c-137">True</span></span>                                         |
| <span data-ttu-id="56c1c-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56c1c-138">Is Indexed</span></span>             | <span data-ttu-id="56c1c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-139">False</span></span>                                        |
| <span data-ttu-id="56c1c-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56c1c-140">In Global Catalog</span></span>      | <span data-ttu-id="56c1c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-141">False</span></span>                                        |
| <span data-ttu-id="56c1c-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56c1c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="56c1c-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56c1c-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="56c1c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56c1c-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56c1c-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-146">Search-Flags</span></span>           | <span data-ttu-id="56c1c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56c1c-147">0x00000000</span></span>                                   |
| <span data-ttu-id="56c1c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-148">System-Flags</span></span>           | <span data-ttu-id="56c1c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56c1c-149">0x00000010</span></span>                                   |
| <span data-ttu-id="56c1c-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56c1c-150">Classes used in</span></span>        | [<span data-ttu-id="56c1c-151">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="56c1c-151">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="56c1c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56c1c-152">Windows Server 2003</span></span>



| <span data-ttu-id="56c1c-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-153">Entry</span></span> | <span data-ttu-id="56c1c-154">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="56c1c-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56c1c-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="56c1c-157">System-Only</span></span>            | <span data-ttu-id="56c1c-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-158">False</span></span>                                        |
| <span data-ttu-id="56c1c-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56c1c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="56c1c-160">True</span><span class="sxs-lookup"><span data-stu-id="56c1c-160">True</span></span>                                         |
| <span data-ttu-id="56c1c-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56c1c-161">Is Indexed</span></span>             | <span data-ttu-id="56c1c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-162">False</span></span>                                        |
| <span data-ttu-id="56c1c-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56c1c-163">In Global Catalog</span></span>      | <span data-ttu-id="56c1c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-164">False</span></span>                                        |
| <span data-ttu-id="56c1c-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56c1c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="56c1c-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56c1c-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="56c1c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56c1c-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56c1c-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-169">Search-Flags</span></span>           | <span data-ttu-id="56c1c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56c1c-170">0x00000000</span></span>                                   |
| <span data-ttu-id="56c1c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-171">System-Flags</span></span>           | <span data-ttu-id="56c1c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56c1c-172">0x00000010</span></span>                                   |
| <span data-ttu-id="56c1c-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56c1c-173">Classes used in</span></span>        | [<span data-ttu-id="56c1c-174">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="56c1c-174">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56c1c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56c1c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56c1c-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-176">Entry</span></span> | <span data-ttu-id="56c1c-177">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="56c1c-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56c1c-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="56c1c-180">System-Only</span></span>            | <span data-ttu-id="56c1c-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-181">False</span></span>                                        |
| <span data-ttu-id="56c1c-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56c1c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="56c1c-183">True</span><span class="sxs-lookup"><span data-stu-id="56c1c-183">True</span></span>                                         |
| <span data-ttu-id="56c1c-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56c1c-184">Is Indexed</span></span>             | <span data-ttu-id="56c1c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-185">False</span></span>                                        |
| <span data-ttu-id="56c1c-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56c1c-186">In Global Catalog</span></span>      | <span data-ttu-id="56c1c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-187">False</span></span>                                        |
| <span data-ttu-id="56c1c-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56c1c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="56c1c-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56c1c-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="56c1c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56c1c-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56c1c-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-192">Search-Flags</span></span>           | <span data-ttu-id="56c1c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56c1c-193">0x00000000</span></span>                                   |
| <span data-ttu-id="56c1c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-194">System-Flags</span></span>           | <span data-ttu-id="56c1c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56c1c-195">0x00000010</span></span>                                   |
| <span data-ttu-id="56c1c-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56c1c-196">Classes used in</span></span>        | [<span data-ttu-id="56c1c-197">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="56c1c-197">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56c1c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56c1c-198">Windows Server 2008</span></span>



| <span data-ttu-id="56c1c-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-199">Entry</span></span> | <span data-ttu-id="56c1c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="56c1c-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56c1c-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="56c1c-203">System-Only</span></span>            | <span data-ttu-id="56c1c-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-204">False</span></span>                                        |
| <span data-ttu-id="56c1c-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56c1c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="56c1c-206">True</span><span class="sxs-lookup"><span data-stu-id="56c1c-206">True</span></span>                                         |
| <span data-ttu-id="56c1c-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56c1c-207">Is Indexed</span></span>             | <span data-ttu-id="56c1c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-208">False</span></span>                                        |
| <span data-ttu-id="56c1c-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56c1c-209">In Global Catalog</span></span>      | <span data-ttu-id="56c1c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-210">False</span></span>                                        |
| <span data-ttu-id="56c1c-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56c1c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="56c1c-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56c1c-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="56c1c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56c1c-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56c1c-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-215">Search-Flags</span></span>           | <span data-ttu-id="56c1c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56c1c-216">0x00000000</span></span>                                   |
| <span data-ttu-id="56c1c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-217">System-Flags</span></span>           | <span data-ttu-id="56c1c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56c1c-218">0x00000010</span></span>                                   |
| <span data-ttu-id="56c1c-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56c1c-219">Classes used in</span></span>        | [<span data-ttu-id="56c1c-220">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="56c1c-220">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56c1c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56c1c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56c1c-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-222">Entry</span></span> | <span data-ttu-id="56c1c-223">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="56c1c-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56c1c-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="56c1c-226">System-Only</span></span>            | <span data-ttu-id="56c1c-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-227">False</span></span>                                        |
| <span data-ttu-id="56c1c-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56c1c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="56c1c-229">True</span><span class="sxs-lookup"><span data-stu-id="56c1c-229">True</span></span>                                         |
| <span data-ttu-id="56c1c-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56c1c-230">Is Indexed</span></span>             | <span data-ttu-id="56c1c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-231">False</span></span>                                        |
| <span data-ttu-id="56c1c-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56c1c-232">In Global Catalog</span></span>      | <span data-ttu-id="56c1c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-233">False</span></span>                                        |
| <span data-ttu-id="56c1c-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56c1c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="56c1c-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56c1c-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="56c1c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56c1c-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56c1c-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-238">Search-Flags</span></span>           | <span data-ttu-id="56c1c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56c1c-239">0x00000000</span></span>                                   |
| <span data-ttu-id="56c1c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-240">System-Flags</span></span>           | <span data-ttu-id="56c1c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56c1c-241">0x00000010</span></span>                                   |
| <span data-ttu-id="56c1c-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56c1c-242">Classes used in</span></span>        | [<span data-ttu-id="56c1c-243">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="56c1c-243">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56c1c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56c1c-244">Windows Server 2012</span></span>



| <span data-ttu-id="56c1c-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="56c1c-245">Entry</span></span> | <span data-ttu-id="56c1c-246">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1c-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="56c1c-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="56c1c-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56c1c-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="56c1c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="56c1c-249">System-Only</span></span>            | <span data-ttu-id="56c1c-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-250">False</span></span>                                        |
| <span data-ttu-id="56c1c-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="56c1c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="56c1c-252">True</span><span class="sxs-lookup"><span data-stu-id="56c1c-252">True</span></span>                                         |
| <span data-ttu-id="56c1c-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="56c1c-253">Is Indexed</span></span>             | <span data-ttu-id="56c1c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-254">False</span></span>                                        |
| <span data-ttu-id="56c1c-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="56c1c-255">In Global Catalog</span></span>      | <span data-ttu-id="56c1c-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="56c1c-256">False</span></span>                                        |
| <span data-ttu-id="56c1c-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="56c1c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="56c1c-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="56c1c-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="56c1c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56c1c-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56c1c-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="56c1c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-261">Search-Flags</span></span>           | <span data-ttu-id="56c1c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56c1c-262">0x00000000</span></span>                                   |
| <span data-ttu-id="56c1c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56c1c-263">System-Flags</span></span>           | <span data-ttu-id="56c1c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56c1c-264">0x00000010</span></span>                                   |
| <span data-ttu-id="56c1c-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="56c1c-265">Classes used in</span></span>        | [<span data-ttu-id="56c1c-266">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="56c1c-266">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





