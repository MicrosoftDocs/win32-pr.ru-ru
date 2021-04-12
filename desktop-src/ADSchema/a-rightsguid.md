---
title: Атрибут Rights-Guid
description: Идентификатор GUID, используемый для представления расширенного права в записи управления доступом.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Rights-Guid
- Схема AD атрибута Ригхтсгуид
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138779"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="b1247-105">Атрибут Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="b1247-105">Rights-Guid attribute</span></span>

<span data-ttu-id="b1247-106">Идентификатор GUID, используемый для представления расширенного права в записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="b1247-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="b1247-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-107">Entry</span></span> | <span data-ttu-id="b1247-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b1247-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1247-109">CN</span></span>                | <span data-ttu-id="b1247-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="b1247-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="b1247-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b1247-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1247-112">ригхтсгуид</span><span class="sxs-lookup"><span data-stu-id="b1247-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="b1247-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b1247-113">Size</span></span>              | <span data-ttu-id="b1247-114">16 байт</span><span class="sxs-lookup"><span data-stu-id="b1247-114">16 bytes</span></span>                                    |
| <span data-ttu-id="b1247-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b1247-115">Update Privilege</span></span>  | <span data-ttu-id="b1247-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b1247-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="b1247-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b1247-117">Update Frequency</span></span>  | <span data-ttu-id="b1247-118">Когда создается новое расширенное право.</span><span class="sxs-lookup"><span data-stu-id="b1247-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="b1247-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-119">Attribute-Id</span></span>      | <span data-ttu-id="b1247-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="b1247-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="b1247-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b1247-121">System-Id-Guid</span></span>    | <span data-ttu-id="b1247-122">8297931c-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b1247-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="b1247-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1247-123">Syntax</span></span>            | [<span data-ttu-id="b1247-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b1247-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b1247-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b1247-125">Implementations</span></span>

-   [<span data-ttu-id="b1247-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b1247-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b1247-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1247-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1247-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b1247-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b1247-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1247-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1247-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1247-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1247-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1247-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1247-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1247-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b1247-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1247-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b1247-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-134">Entry</span></span> | <span data-ttu-id="b1247-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-138">System-Only</span></span>            | <span data-ttu-id="b1247-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-139">False</span></span>                                                           |
| <span data-ttu-id="b1247-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-141">True</span><span class="sxs-lookup"><span data-stu-id="b1247-141">True</span></span>                                                            |
| <span data-ttu-id="b1247-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-142">Is Indexed</span></span>             | <span data-ttu-id="b1247-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-143">False</span></span>                                                           |
| <span data-ttu-id="b1247-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-144">In Global Catalog</span></span>      | <span data-ttu-id="b1247-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-145">False</span></span>                                                           |
| <span data-ttu-id="b1247-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-148">Range-Lower</span></span>            | <span data-ttu-id="b1247-149">36</span><span class="sxs-lookup"><span data-stu-id="b1247-149">36</span></span>                                                              |
| <span data-ttu-id="b1247-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-150">Range-Upper</span></span>            | <span data-ttu-id="b1247-151">36</span><span class="sxs-lookup"><span data-stu-id="b1247-151">36</span></span>                                                              |
| <span data-ttu-id="b1247-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-152">Search-Flags</span></span>           | <span data-ttu-id="b1247-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-154">System-Flags</span></span>           | <span data-ttu-id="b1247-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-156">Classes used in</span></span>        | [<span data-ttu-id="b1247-157">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b1247-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1247-158">Windows Server 2003</span></span>



| <span data-ttu-id="b1247-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-159">Entry</span></span> | <span data-ttu-id="b1247-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-163">System-Only</span></span>            | <span data-ttu-id="b1247-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-164">False</span></span>                                                           |
| <span data-ttu-id="b1247-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-166">True</span><span class="sxs-lookup"><span data-stu-id="b1247-166">True</span></span>                                                            |
| <span data-ttu-id="b1247-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-167">Is Indexed</span></span>             | <span data-ttu-id="b1247-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-168">False</span></span>                                                           |
| <span data-ttu-id="b1247-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-169">In Global Catalog</span></span>      | <span data-ttu-id="b1247-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-170">False</span></span>                                                           |
| <span data-ttu-id="b1247-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-173">Range-Lower</span></span>            | <span data-ttu-id="b1247-174">36</span><span class="sxs-lookup"><span data-stu-id="b1247-174">36</span></span>                                                              |
| <span data-ttu-id="b1247-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-175">Range-Upper</span></span>            | <span data-ttu-id="b1247-176">36</span><span class="sxs-lookup"><span data-stu-id="b1247-176">36</span></span>                                                              |
| <span data-ttu-id="b1247-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-177">Search-Flags</span></span>           | <span data-ttu-id="b1247-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-179">System-Flags</span></span>           | <span data-ttu-id="b1247-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-181">Classes used in</span></span>        | [<span data-ttu-id="b1247-182">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b1247-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="b1247-183">ADAM</span></span>



| <span data-ttu-id="b1247-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-184">Entry</span></span> | <span data-ttu-id="b1247-185">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-188">System-Only</span></span>            | <span data-ttu-id="b1247-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-189">False</span></span>                                                           |
| <span data-ttu-id="b1247-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-190">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-191">True</span><span class="sxs-lookup"><span data-stu-id="b1247-191">True</span></span>                                                            |
| <span data-ttu-id="b1247-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-192">Is Indexed</span></span>             | <span data-ttu-id="b1247-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-193">False</span></span>                                                           |
| <span data-ttu-id="b1247-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-194">In Global Catalog</span></span>      | <span data-ttu-id="b1247-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-195">False</span></span>                                                           |
| <span data-ttu-id="b1247-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-198">Range-Lower</span></span>            | <span data-ttu-id="b1247-199">36</span><span class="sxs-lookup"><span data-stu-id="b1247-199">36</span></span>                                                              |
| <span data-ttu-id="b1247-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-200">Range-Upper</span></span>            | <span data-ttu-id="b1247-201">36</span><span class="sxs-lookup"><span data-stu-id="b1247-201">36</span></span>                                                              |
| <span data-ttu-id="b1247-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-202">Search-Flags</span></span>           | <span data-ttu-id="b1247-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-204">System-Flags</span></span>           | <span data-ttu-id="b1247-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-206">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-206">Classes used in</span></span>        | [<span data-ttu-id="b1247-207">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1247-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1247-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1247-209">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-209">Entry</span></span> | <span data-ttu-id="b1247-210">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-211">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-213">System-Only</span></span>            | <span data-ttu-id="b1247-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-214">False</span></span>                                                           |
| <span data-ttu-id="b1247-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-215">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-216">True</span><span class="sxs-lookup"><span data-stu-id="b1247-216">True</span></span>                                                            |
| <span data-ttu-id="b1247-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-217">Is Indexed</span></span>             | <span data-ttu-id="b1247-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-218">False</span></span>                                                           |
| <span data-ttu-id="b1247-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-219">In Global Catalog</span></span>      | <span data-ttu-id="b1247-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-220">False</span></span>                                                           |
| <span data-ttu-id="b1247-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-223">Range-Lower</span></span>            | <span data-ttu-id="b1247-224">36</span><span class="sxs-lookup"><span data-stu-id="b1247-224">36</span></span>                                                              |
| <span data-ttu-id="b1247-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-225">Range-Upper</span></span>            | <span data-ttu-id="b1247-226">36</span><span class="sxs-lookup"><span data-stu-id="b1247-226">36</span></span>                                                              |
| <span data-ttu-id="b1247-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-227">Search-Flags</span></span>           | <span data-ttu-id="b1247-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-229">System-Flags</span></span>           | <span data-ttu-id="b1247-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-231">Classes used in</span></span>        | [<span data-ttu-id="b1247-232">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1247-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1247-233">Windows Server 2008</span></span>



| <span data-ttu-id="b1247-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-234">Entry</span></span> | <span data-ttu-id="b1247-235">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-238">System-Only</span></span>            | <span data-ttu-id="b1247-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-239">False</span></span>                                                           |
| <span data-ttu-id="b1247-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-240">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-241">True</span><span class="sxs-lookup"><span data-stu-id="b1247-241">True</span></span>                                                            |
| <span data-ttu-id="b1247-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-242">Is Indexed</span></span>             | <span data-ttu-id="b1247-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-243">False</span></span>                                                           |
| <span data-ttu-id="b1247-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-244">In Global Catalog</span></span>      | <span data-ttu-id="b1247-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-245">False</span></span>                                                           |
| <span data-ttu-id="b1247-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-248">Range-Lower</span></span>            | <span data-ttu-id="b1247-249">36</span><span class="sxs-lookup"><span data-stu-id="b1247-249">36</span></span>                                                              |
| <span data-ttu-id="b1247-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-250">Range-Upper</span></span>            | <span data-ttu-id="b1247-251">36</span><span class="sxs-lookup"><span data-stu-id="b1247-251">36</span></span>                                                              |
| <span data-ttu-id="b1247-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-252">Search-Flags</span></span>           | <span data-ttu-id="b1247-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-254">System-Flags</span></span>           | <span data-ttu-id="b1247-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-256">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-256">Classes used in</span></span>        | [<span data-ttu-id="b1247-257">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1247-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1247-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1247-259">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-259">Entry</span></span> | <span data-ttu-id="b1247-260">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-261">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-263">System-Only</span></span>            | <span data-ttu-id="b1247-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-264">False</span></span>                                                           |
| <span data-ttu-id="b1247-265">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-265">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-266">True</span><span class="sxs-lookup"><span data-stu-id="b1247-266">True</span></span>                                                            |
| <span data-ttu-id="b1247-267">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-267">Is Indexed</span></span>             | <span data-ttu-id="b1247-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-268">False</span></span>                                                           |
| <span data-ttu-id="b1247-269">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-269">In Global Catalog</span></span>      | <span data-ttu-id="b1247-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-270">False</span></span>                                                           |
| <span data-ttu-id="b1247-271">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-272">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-273">Range-Lower</span></span>            | <span data-ttu-id="b1247-274">36</span><span class="sxs-lookup"><span data-stu-id="b1247-274">36</span></span>                                                              |
| <span data-ttu-id="b1247-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-275">Range-Upper</span></span>            | <span data-ttu-id="b1247-276">36</span><span class="sxs-lookup"><span data-stu-id="b1247-276">36</span></span>                                                              |
| <span data-ttu-id="b1247-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-277">Search-Flags</span></span>           | <span data-ttu-id="b1247-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-279">System-Flags</span></span>           | <span data-ttu-id="b1247-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-281">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-281">Classes used in</span></span>        | [<span data-ttu-id="b1247-282">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1247-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1247-283">Windows Server 2012</span></span>



| <span data-ttu-id="b1247-284">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1247-284">Entry</span></span> | <span data-ttu-id="b1247-285">Значение</span><span class="sxs-lookup"><span data-stu-id="b1247-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1247-286">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1247-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1247-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b1247-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1247-288">System-Only</span></span>            | <span data-ttu-id="b1247-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-289">False</span></span>                                                           |
| <span data-ttu-id="b1247-290">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1247-290">Is-Single-Valued</span></span>       | <span data-ttu-id="b1247-291">True</span><span class="sxs-lookup"><span data-stu-id="b1247-291">True</span></span>                                                            |
| <span data-ttu-id="b1247-292">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1247-292">Is Indexed</span></span>             | <span data-ttu-id="b1247-293">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-293">False</span></span>                                                           |
| <span data-ttu-id="b1247-294">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1247-294">In Global Catalog</span></span>      | <span data-ttu-id="b1247-295">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1247-295">False</span></span>                                                           |
| <span data-ttu-id="b1247-296">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1247-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1247-297">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1247-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b1247-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1247-298">Range-Lower</span></span>            | <span data-ttu-id="b1247-299">36</span><span class="sxs-lookup"><span data-stu-id="b1247-299">36</span></span>                                                              |
| <span data-ttu-id="b1247-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1247-300">Range-Upper</span></span>            | <span data-ttu-id="b1247-301">36</span><span class="sxs-lookup"><span data-stu-id="b1247-301">36</span></span>                                                              |
| <span data-ttu-id="b1247-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-302">Search-Flags</span></span>           | <span data-ttu-id="b1247-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1247-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="b1247-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1247-304">System-Flags</span></span>           | <span data-ttu-id="b1247-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1247-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="b1247-306">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1247-306">Classes used in</span></span>        | [<span data-ttu-id="b1247-307">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="b1247-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





