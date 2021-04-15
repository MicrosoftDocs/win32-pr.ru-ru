---
title: Атрибут прокси — object-name
description: Этот атрибут используется внутренне Active Directory для наблюдения за перемещением между доменами.
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- Прокси-объект — имя схемы AD атрибута
- Схема AD атрибута Проксиедобжектнаме
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654788"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="ddc9b-105">Атрибут прокси — object-name</span><span class="sxs-lookup"><span data-stu-id="ddc9b-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="ddc9b-106">Этот атрибут используется внутренне Active Directory для наблюдения за перемещением между доменами.</span><span class="sxs-lookup"><span data-stu-id="ddc9b-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="ddc9b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-107">Entry</span></span> | <span data-ttu-id="ddc9b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="ddc9b-109">CN</span><span class="sxs-lookup"><span data-stu-id="ddc9b-109">CN</span></span>                | <span data-ttu-id="ddc9b-110">Прокси-объект-имя</span><span class="sxs-lookup"><span data-stu-id="ddc9b-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="ddc9b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ddc9b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ddc9b-112">проксиедобжектнаме</span><span class="sxs-lookup"><span data-stu-id="ddc9b-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="ddc9b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ddc9b-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="ddc9b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ddc9b-114">Update Privilege</span></span>  | <span data-ttu-id="ddc9b-115">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="ddc9b-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="ddc9b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ddc9b-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="ddc9b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-117">Attribute-Id</span></span>      | <span data-ttu-id="ddc9b-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="ddc9b-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="ddc9b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ddc9b-119">System-Id-Guid</span></span>    | <span data-ttu-id="ddc9b-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ddc9b-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="ddc9b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddc9b-121">Syntax</span></span>            | [<span data-ttu-id="ddc9b-122">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="ddc9b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ddc9b-123">Implementations</span></span>

-   [<span data-ttu-id="ddc9b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ddc9b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ddc9b-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ddc9b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ddc9b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ddc9b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ddc9b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ddc9b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddc9b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ddc9b-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-132">Entry</span></span> | <span data-ttu-id="ddc9b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-136">System-Only</span></span>            | <span data-ttu-id="ddc9b-137">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-137">True</span></span>                            |
| <span data-ttu-id="ddc9b-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-139">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-139">True</span></span>                            |
| <span data-ttu-id="ddc9b-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-140">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-141">False</span></span>                           |
| <span data-ttu-id="ddc9b-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-142">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-143">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-143">True</span></span>                            |
| <span data-ttu-id="ddc9b-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-148">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-149">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-150">System-Flags</span></span>           | <span data-ttu-id="ddc9b-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-151">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-152">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-153">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ddc9b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddc9b-154">Windows Server 2003</span></span>



| <span data-ttu-id="ddc9b-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-155">Entry</span></span> | <span data-ttu-id="ddc9b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-159">System-Only</span></span>            | <span data-ttu-id="ddc9b-160">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-160">True</span></span>                            |
| <span data-ttu-id="ddc9b-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-162">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-162">True</span></span>                            |
| <span data-ttu-id="ddc9b-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-163">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-164">False</span></span>                           |
| <span data-ttu-id="ddc9b-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-165">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-166">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-166">True</span></span>                            |
| <span data-ttu-id="ddc9b-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-171">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-172">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-173">System-Flags</span></span>           | <span data-ttu-id="ddc9b-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-174">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-175">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-176">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ddc9b-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="ddc9b-177">ADAM</span></span>



| <span data-ttu-id="ddc9b-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-178">Entry</span></span> | <span data-ttu-id="ddc9b-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-182">System-Only</span></span>            | <span data-ttu-id="ddc9b-183">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-183">True</span></span>                            |
| <span data-ttu-id="ddc9b-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-185">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-185">True</span></span>                            |
| <span data-ttu-id="ddc9b-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-186">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-187">False</span></span>                           |
| <span data-ttu-id="ddc9b-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-188">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-189">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-189">True</span></span>                            |
| <span data-ttu-id="ddc9b-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-194">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-195">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-196">System-Flags</span></span>           | <span data-ttu-id="ddc9b-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-197">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-198">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-199">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ddc9b-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ddc9b-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ddc9b-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-201">Entry</span></span> | <span data-ttu-id="ddc9b-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-205">System-Only</span></span>            | <span data-ttu-id="ddc9b-206">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-206">True</span></span>                            |
| <span data-ttu-id="ddc9b-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-208">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-208">True</span></span>                            |
| <span data-ttu-id="ddc9b-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-209">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-210">False</span></span>                           |
| <span data-ttu-id="ddc9b-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-211">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-212">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-212">True</span></span>                            |
| <span data-ttu-id="ddc9b-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-217">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-218">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-219">System-Flags</span></span>           | <span data-ttu-id="ddc9b-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-220">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-221">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-222">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ddc9b-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddc9b-223">Windows Server 2008</span></span>



| <span data-ttu-id="ddc9b-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-224">Entry</span></span> | <span data-ttu-id="ddc9b-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-228">System-Only</span></span>            | <span data-ttu-id="ddc9b-229">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-229">True</span></span>                            |
| <span data-ttu-id="ddc9b-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-231">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-231">True</span></span>                            |
| <span data-ttu-id="ddc9b-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-232">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-233">False</span></span>                           |
| <span data-ttu-id="ddc9b-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-234">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-235">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-235">True</span></span>                            |
| <span data-ttu-id="ddc9b-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-240">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-241">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-242">System-Flags</span></span>           | <span data-ttu-id="ddc9b-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-243">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-244">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-245">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ddc9b-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ddc9b-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ddc9b-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-247">Entry</span></span> | <span data-ttu-id="ddc9b-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-251">System-Only</span></span>            | <span data-ttu-id="ddc9b-252">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-252">True</span></span>                            |
| <span data-ttu-id="ddc9b-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-254">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-254">True</span></span>                            |
| <span data-ttu-id="ddc9b-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-255">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-256">False</span></span>                           |
| <span data-ttu-id="ddc9b-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-257">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-258">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-258">True</span></span>                            |
| <span data-ttu-id="ddc9b-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-263">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-264">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-265">System-Flags</span></span>           | <span data-ttu-id="ddc9b-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-266">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-267">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-268">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ddc9b-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-269">Windows Server 2012</span></span>



| <span data-ttu-id="ddc9b-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="ddc9b-270">Entry</span></span> | <span data-ttu-id="ddc9b-271">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc9b-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ddc9b-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ddc9b-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddc9b-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ddc9b-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddc9b-274">System-Only</span></span>            | <span data-ttu-id="ddc9b-275">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-275">True</span></span>                            |
| <span data-ttu-id="ddc9b-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ddc9b-276">Is-Single-Valued</span></span>       | <span data-ttu-id="ddc9b-277">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-277">True</span></span>                            |
| <span data-ttu-id="ddc9b-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ddc9b-278">Is Indexed</span></span>             | <span data-ttu-id="ddc9b-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="ddc9b-279">False</span></span>                           |
| <span data-ttu-id="ddc9b-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ddc9b-280">In Global Catalog</span></span>      | <span data-ttu-id="ddc9b-281">True</span><span class="sxs-lookup"><span data-stu-id="ddc9b-281">True</span></span>                            |
| <span data-ttu-id="ddc9b-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ddc9b-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddc9b-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddc9b-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ddc9b-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddc9b-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddc9b-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ddc9b-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-286">Search-Flags</span></span>           | <span data-ttu-id="ddc9b-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddc9b-287">0x00000000</span></span>                      |
| <span data-ttu-id="ddc9b-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddc9b-288">System-Flags</span></span>           | <span data-ttu-id="ddc9b-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ddc9b-289">0x00000012</span></span>                      |
| <span data-ttu-id="ddc9b-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ddc9b-290">Classes used in</span></span>        | [<span data-ttu-id="ddc9b-291">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="ddc9b-291">**Top**</span></span>](c-top.md)<br/> |



 

 





