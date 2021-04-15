---
title: Атрибут Options-Location
description: Для DHCP расположение параметров содержит различающееся имя для альтернативных сайтов, содержащих сведения о параметрах.
ms.assetid: 2b357733-620f-4ad7-ba69-209095e98aa6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Options-Location
- Схема AD атрибута Оптионслокатион
topic_type:
- apiref
api_name:
- Options-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72b33089770d4d9b7cd869cb6375f6224ecd361a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493959"
---
# <a name="options-location-attribute"></a><span data-ttu-id="13a61-105">Атрибут Options-Location</span><span class="sxs-lookup"><span data-stu-id="13a61-105">Options-Location attribute</span></span>

<span data-ttu-id="13a61-106">Для DHCP расположение параметров содержит различающееся имя для альтернативных сайтов, содержащих сведения о параметрах.</span><span class="sxs-lookup"><span data-stu-id="13a61-106">For DHCP, the options location contains the DN for alternate sites that contain the options information.</span></span>



| <span data-ttu-id="13a61-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-107">Entry</span></span> | <span data-ttu-id="13a61-108">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="13a61-109">CN</span><span class="sxs-lookup"><span data-stu-id="13a61-109">CN</span></span>                | <span data-ttu-id="13a61-110">Options-Location</span><span class="sxs-lookup"><span data-stu-id="13a61-110">Options-Location</span></span>                     |
| <span data-ttu-id="13a61-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="13a61-111">Ldap-Display-Name</span></span> | <span data-ttu-id="13a61-112">оптионслокатион</span><span class="sxs-lookup"><span data-stu-id="13a61-112">optionsLocation</span></span>                      |
| <span data-ttu-id="13a61-113">Размер</span><span class="sxs-lookup"><span data-stu-id="13a61-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="13a61-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="13a61-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="13a61-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="13a61-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="13a61-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-116">Attribute-Id</span></span>      | <span data-ttu-id="13a61-117">1.2.840.113556.1.4.713</span><span class="sxs-lookup"><span data-stu-id="13a61-117">1.2.840.113556.1.4.713</span></span>               |
| <span data-ttu-id="13a61-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="13a61-118">System-Id-Guid</span></span>    | <span data-ttu-id="13a61-119">963d274e-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="13a61-119">963d274e-48be-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="13a61-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13a61-120">Syntax</span></span>            | [<span data-ttu-id="13a61-121">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="13a61-121">**String(IA5)**</span></span>](s-string-ia5.md)  |



## <a name="implementations"></a><span data-ttu-id="13a61-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="13a61-122">Implementations</span></span>

-   [<span data-ttu-id="13a61-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13a61-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13a61-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13a61-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13a61-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13a61-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13a61-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13a61-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13a61-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13a61-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13a61-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13a61-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13a61-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13a61-129">Windows 2000 Server</span></span>



| <span data-ttu-id="13a61-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-130">Entry</span></span> | <span data-ttu-id="13a61-131">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a61-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13a61-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a61-134">System-Only</span></span>            | <span data-ttu-id="13a61-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-135">False</span></span>                                        |
| <span data-ttu-id="13a61-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13a61-136">Is-Single-Valued</span></span>       | <span data-ttu-id="13a61-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-137">False</span></span>                                        |
| <span data-ttu-id="13a61-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13a61-138">Is Indexed</span></span>             | <span data-ttu-id="13a61-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-139">False</span></span>                                        |
| <span data-ttu-id="13a61-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13a61-140">In Global Catalog</span></span>      | <span data-ttu-id="13a61-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-141">False</span></span>                                        |
| <span data-ttu-id="13a61-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13a61-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a61-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13a61-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a61-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a61-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a61-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a61-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a61-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-146">Search-Flags</span></span>           | <span data-ttu-id="13a61-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a61-147">0x00000000</span></span>                                   |
| <span data-ttu-id="13a61-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-148">System-Flags</span></span>           | <span data-ttu-id="13a61-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a61-149">0x00000010</span></span>                                   |
| <span data-ttu-id="13a61-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13a61-150">Classes used in</span></span>        | [<span data-ttu-id="13a61-151">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="13a61-151">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13a61-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13a61-152">Windows Server 2003</span></span>



| <span data-ttu-id="13a61-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-153">Entry</span></span> | <span data-ttu-id="13a61-154">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a61-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13a61-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a61-157">System-Only</span></span>            | <span data-ttu-id="13a61-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-158">False</span></span>                                        |
| <span data-ttu-id="13a61-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13a61-159">Is-Single-Valued</span></span>       | <span data-ttu-id="13a61-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-160">False</span></span>                                        |
| <span data-ttu-id="13a61-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13a61-161">Is Indexed</span></span>             | <span data-ttu-id="13a61-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-162">False</span></span>                                        |
| <span data-ttu-id="13a61-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13a61-163">In Global Catalog</span></span>      | <span data-ttu-id="13a61-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-164">False</span></span>                                        |
| <span data-ttu-id="13a61-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13a61-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a61-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13a61-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a61-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a61-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a61-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a61-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a61-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-169">Search-Flags</span></span>           | <span data-ttu-id="13a61-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a61-170">0x00000000</span></span>                                   |
| <span data-ttu-id="13a61-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-171">System-Flags</span></span>           | <span data-ttu-id="13a61-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a61-172">0x00000010</span></span>                                   |
| <span data-ttu-id="13a61-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13a61-173">Classes used in</span></span>        | [<span data-ttu-id="13a61-174">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="13a61-174">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13a61-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13a61-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13a61-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-176">Entry</span></span> | <span data-ttu-id="13a61-177">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a61-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13a61-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a61-180">System-Only</span></span>            | <span data-ttu-id="13a61-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-181">False</span></span>                                        |
| <span data-ttu-id="13a61-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13a61-182">Is-Single-Valued</span></span>       | <span data-ttu-id="13a61-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-183">False</span></span>                                        |
| <span data-ttu-id="13a61-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13a61-184">Is Indexed</span></span>             | <span data-ttu-id="13a61-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-185">False</span></span>                                        |
| <span data-ttu-id="13a61-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13a61-186">In Global Catalog</span></span>      | <span data-ttu-id="13a61-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-187">False</span></span>                                        |
| <span data-ttu-id="13a61-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13a61-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a61-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13a61-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a61-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a61-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a61-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a61-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a61-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-192">Search-Flags</span></span>           | <span data-ttu-id="13a61-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a61-193">0x00000000</span></span>                                   |
| <span data-ttu-id="13a61-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-194">System-Flags</span></span>           | <span data-ttu-id="13a61-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a61-195">0x00000010</span></span>                                   |
| <span data-ttu-id="13a61-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13a61-196">Classes used in</span></span>        | [<span data-ttu-id="13a61-197">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="13a61-197">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13a61-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13a61-198">Windows Server 2008</span></span>



| <span data-ttu-id="13a61-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-199">Entry</span></span> | <span data-ttu-id="13a61-200">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a61-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13a61-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a61-203">System-Only</span></span>            | <span data-ttu-id="13a61-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-204">False</span></span>                                        |
| <span data-ttu-id="13a61-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13a61-205">Is-Single-Valued</span></span>       | <span data-ttu-id="13a61-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-206">False</span></span>                                        |
| <span data-ttu-id="13a61-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13a61-207">Is Indexed</span></span>             | <span data-ttu-id="13a61-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-208">False</span></span>                                        |
| <span data-ttu-id="13a61-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13a61-209">In Global Catalog</span></span>      | <span data-ttu-id="13a61-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-210">False</span></span>                                        |
| <span data-ttu-id="13a61-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13a61-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a61-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13a61-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a61-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a61-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a61-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a61-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a61-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-215">Search-Flags</span></span>           | <span data-ttu-id="13a61-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a61-216">0x00000000</span></span>                                   |
| <span data-ttu-id="13a61-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-217">System-Flags</span></span>           | <span data-ttu-id="13a61-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a61-218">0x00000010</span></span>                                   |
| <span data-ttu-id="13a61-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13a61-219">Classes used in</span></span>        | [<span data-ttu-id="13a61-220">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="13a61-220">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13a61-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13a61-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13a61-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-222">Entry</span></span> | <span data-ttu-id="13a61-223">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a61-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13a61-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a61-226">System-Only</span></span>            | <span data-ttu-id="13a61-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-227">False</span></span>                                        |
| <span data-ttu-id="13a61-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13a61-228">Is-Single-Valued</span></span>       | <span data-ttu-id="13a61-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-229">False</span></span>                                        |
| <span data-ttu-id="13a61-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13a61-230">Is Indexed</span></span>             | <span data-ttu-id="13a61-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-231">False</span></span>                                        |
| <span data-ttu-id="13a61-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13a61-232">In Global Catalog</span></span>      | <span data-ttu-id="13a61-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-233">False</span></span>                                        |
| <span data-ttu-id="13a61-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13a61-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a61-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13a61-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a61-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a61-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a61-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a61-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a61-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-238">Search-Flags</span></span>           | <span data-ttu-id="13a61-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a61-239">0x00000000</span></span>                                   |
| <span data-ttu-id="13a61-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-240">System-Flags</span></span>           | <span data-ttu-id="13a61-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a61-241">0x00000010</span></span>                                   |
| <span data-ttu-id="13a61-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13a61-242">Classes used in</span></span>        | [<span data-ttu-id="13a61-243">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="13a61-243">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13a61-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13a61-244">Windows Server 2012</span></span>



| <span data-ttu-id="13a61-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="13a61-245">Entry</span></span> | <span data-ttu-id="13a61-246">Значение</span><span class="sxs-lookup"><span data-stu-id="13a61-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a61-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="13a61-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a61-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a61-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a61-249">System-Only</span></span>            | <span data-ttu-id="13a61-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-250">False</span></span>                                        |
| <span data-ttu-id="13a61-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="13a61-251">Is-Single-Valued</span></span>       | <span data-ttu-id="13a61-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-252">False</span></span>                                        |
| <span data-ttu-id="13a61-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="13a61-253">Is Indexed</span></span>             | <span data-ttu-id="13a61-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-254">False</span></span>                                        |
| <span data-ttu-id="13a61-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="13a61-255">In Global Catalog</span></span>      | <span data-ttu-id="13a61-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="13a61-256">False</span></span>                                        |
| <span data-ttu-id="13a61-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="13a61-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a61-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13a61-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a61-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a61-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a61-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a61-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a61-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-261">Search-Flags</span></span>           | <span data-ttu-id="13a61-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a61-262">0x00000000</span></span>                                   |
| <span data-ttu-id="13a61-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a61-263">System-Flags</span></span>           | <span data-ttu-id="13a61-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a61-264">0x00000010</span></span>                                   |
| <span data-ttu-id="13a61-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="13a61-265">Classes used in</span></span>        | [<span data-ttu-id="13a61-266">**DHCP-класс**</span><span class="sxs-lookup"><span data-stu-id="13a61-266">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





