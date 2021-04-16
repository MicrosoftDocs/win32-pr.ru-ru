---
title: Атрибут Server-State
description: Указывает, включен ли сервер или отключен.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Server-State
- Схема AD атрибута serverState
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655053"
---
# <a name="server-state-attribute"></a><span data-ttu-id="3af97-105">Атрибут Server-State</span><span class="sxs-lookup"><span data-stu-id="3af97-105">Server-State attribute</span></span>

<span data-ttu-id="3af97-106">Указывает, включен ли сервер или отключен.</span><span class="sxs-lookup"><span data-stu-id="3af97-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="3af97-107">Значение 1 указывает на то, что сервер включен.</span><span class="sxs-lookup"><span data-stu-id="3af97-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="3af97-108">Значение 2 указывает на то, что сервер отключен.</span><span class="sxs-lookup"><span data-stu-id="3af97-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="3af97-109">Все остальные значения недопустимы.</span><span class="sxs-lookup"><span data-stu-id="3af97-109">All other values are invalid.</span></span>



| <span data-ttu-id="3af97-110">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-110">Entry</span></span> | <span data-ttu-id="3af97-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3af97-112">CN</span><span class="sxs-lookup"><span data-stu-id="3af97-112">CN</span></span>                | <span data-ttu-id="3af97-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="3af97-113">Server-State</span></span>                         |
| <span data-ttu-id="3af97-114">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3af97-114">Ldap-Display-Name</span></span> | <span data-ttu-id="3af97-115">serverState</span><span class="sxs-lookup"><span data-stu-id="3af97-115">serverState</span></span>                          |
| <span data-ttu-id="3af97-116">Размер</span><span class="sxs-lookup"><span data-stu-id="3af97-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="3af97-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3af97-117">Update Privilege</span></span>  | <span data-ttu-id="3af97-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="3af97-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="3af97-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3af97-119">Update Frequency</span></span>  | <span data-ttu-id="3af97-120">При изменении политики для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3af97-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="3af97-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-121">Attribute-Id</span></span>      | <span data-ttu-id="3af97-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="3af97-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="3af97-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3af97-123">System-Id-Guid</span></span>    | <span data-ttu-id="3af97-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3af97-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3af97-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3af97-125">Syntax</span></span>            | [<span data-ttu-id="3af97-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="3af97-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3af97-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3af97-127">Implementations</span></span>

-   [<span data-ttu-id="3af97-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3af97-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3af97-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3af97-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3af97-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3af97-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3af97-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3af97-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3af97-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3af97-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3af97-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3af97-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3af97-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3af97-134">Windows 2000 Server</span></span>



| <span data-ttu-id="3af97-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-135">Entry</span></span> | <span data-ttu-id="3af97-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3af97-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3af97-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="3af97-139">System-Only</span></span>            | <span data-ttu-id="3af97-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-140">False</span></span>                                                 |
| <span data-ttu-id="3af97-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3af97-141">Is-Single-Valued</span></span>       | <span data-ttu-id="3af97-142">True</span><span class="sxs-lookup"><span data-stu-id="3af97-142">True</span></span>                                                  |
| <span data-ttu-id="3af97-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3af97-143">Is Indexed</span></span>             | <span data-ttu-id="3af97-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-144">False</span></span>                                                 |
| <span data-ttu-id="3af97-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3af97-145">In Global Catalog</span></span>      | <span data-ttu-id="3af97-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-146">False</span></span>                                                 |
| <span data-ttu-id="3af97-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3af97-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="3af97-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3af97-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3af97-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3af97-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3af97-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-151">Search-Flags</span></span>           | <span data-ttu-id="3af97-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3af97-152">0x00000000</span></span>                                            |
| <span data-ttu-id="3af97-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-153">System-Flags</span></span>           | <span data-ttu-id="3af97-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3af97-154">0x00000011</span></span>                                            |
| <span data-ttu-id="3af97-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3af97-155">Classes used in</span></span>        | [<span data-ttu-id="3af97-156">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="3af97-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3af97-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3af97-157">Windows Server 2003</span></span>



| <span data-ttu-id="3af97-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-158">Entry</span></span> | <span data-ttu-id="3af97-159">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3af97-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3af97-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="3af97-162">System-Only</span></span>            | <span data-ttu-id="3af97-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-163">False</span></span>                                                 |
| <span data-ttu-id="3af97-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3af97-164">Is-Single-Valued</span></span>       | <span data-ttu-id="3af97-165">True</span><span class="sxs-lookup"><span data-stu-id="3af97-165">True</span></span>                                                  |
| <span data-ttu-id="3af97-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3af97-166">Is Indexed</span></span>             | <span data-ttu-id="3af97-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-167">False</span></span>                                                 |
| <span data-ttu-id="3af97-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3af97-168">In Global Catalog</span></span>      | <span data-ttu-id="3af97-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-169">False</span></span>                                                 |
| <span data-ttu-id="3af97-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3af97-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="3af97-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3af97-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3af97-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3af97-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3af97-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-174">Search-Flags</span></span>           | <span data-ttu-id="3af97-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3af97-175">0x00000000</span></span>                                            |
| <span data-ttu-id="3af97-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-176">System-Flags</span></span>           | <span data-ttu-id="3af97-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3af97-177">0x00000011</span></span>                                            |
| <span data-ttu-id="3af97-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3af97-178">Classes used in</span></span>        | [<span data-ttu-id="3af97-179">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="3af97-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3af97-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3af97-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3af97-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-181">Entry</span></span> | <span data-ttu-id="3af97-182">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3af97-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3af97-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3af97-185">System-Only</span></span>            | <span data-ttu-id="3af97-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-186">False</span></span>                                                 |
| <span data-ttu-id="3af97-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3af97-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3af97-188">True</span><span class="sxs-lookup"><span data-stu-id="3af97-188">True</span></span>                                                  |
| <span data-ttu-id="3af97-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3af97-189">Is Indexed</span></span>             | <span data-ttu-id="3af97-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-190">False</span></span>                                                 |
| <span data-ttu-id="3af97-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3af97-191">In Global Catalog</span></span>      | <span data-ttu-id="3af97-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-192">False</span></span>                                                 |
| <span data-ttu-id="3af97-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3af97-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3af97-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3af97-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3af97-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3af97-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3af97-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-197">Search-Flags</span></span>           | <span data-ttu-id="3af97-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3af97-198">0x00000000</span></span>                                            |
| <span data-ttu-id="3af97-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-199">System-Flags</span></span>           | <span data-ttu-id="3af97-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3af97-200">0x00000011</span></span>                                            |
| <span data-ttu-id="3af97-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3af97-201">Classes used in</span></span>        | [<span data-ttu-id="3af97-202">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="3af97-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3af97-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3af97-203">Windows Server 2008</span></span>



| <span data-ttu-id="3af97-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-204">Entry</span></span> | <span data-ttu-id="3af97-205">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3af97-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3af97-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="3af97-208">System-Only</span></span>            | <span data-ttu-id="3af97-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-209">False</span></span>                                                 |
| <span data-ttu-id="3af97-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3af97-210">Is-Single-Valued</span></span>       | <span data-ttu-id="3af97-211">True</span><span class="sxs-lookup"><span data-stu-id="3af97-211">True</span></span>                                                  |
| <span data-ttu-id="3af97-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3af97-212">Is Indexed</span></span>             | <span data-ttu-id="3af97-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-213">False</span></span>                                                 |
| <span data-ttu-id="3af97-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3af97-214">In Global Catalog</span></span>      | <span data-ttu-id="3af97-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-215">False</span></span>                                                 |
| <span data-ttu-id="3af97-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3af97-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="3af97-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3af97-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3af97-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3af97-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3af97-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-220">Search-Flags</span></span>           | <span data-ttu-id="3af97-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3af97-221">0x00000000</span></span>                                            |
| <span data-ttu-id="3af97-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-222">System-Flags</span></span>           | <span data-ttu-id="3af97-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3af97-223">0x00000011</span></span>                                            |
| <span data-ttu-id="3af97-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3af97-224">Classes used in</span></span>        | [<span data-ttu-id="3af97-225">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="3af97-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3af97-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3af97-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3af97-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-227">Entry</span></span> | <span data-ttu-id="3af97-228">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3af97-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3af97-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="3af97-231">System-Only</span></span>            | <span data-ttu-id="3af97-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-232">False</span></span>                                                 |
| <span data-ttu-id="3af97-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3af97-233">Is-Single-Valued</span></span>       | <span data-ttu-id="3af97-234">True</span><span class="sxs-lookup"><span data-stu-id="3af97-234">True</span></span>                                                  |
| <span data-ttu-id="3af97-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3af97-235">Is Indexed</span></span>             | <span data-ttu-id="3af97-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-236">False</span></span>                                                 |
| <span data-ttu-id="3af97-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3af97-237">In Global Catalog</span></span>      | <span data-ttu-id="3af97-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-238">False</span></span>                                                 |
| <span data-ttu-id="3af97-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3af97-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="3af97-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3af97-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3af97-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3af97-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3af97-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-243">Search-Flags</span></span>           | <span data-ttu-id="3af97-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3af97-244">0x00000000</span></span>                                            |
| <span data-ttu-id="3af97-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-245">System-Flags</span></span>           | <span data-ttu-id="3af97-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3af97-246">0x00000011</span></span>                                            |
| <span data-ttu-id="3af97-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3af97-247">Classes used in</span></span>        | [<span data-ttu-id="3af97-248">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="3af97-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3af97-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3af97-249">Windows Server 2012</span></span>



| <span data-ttu-id="3af97-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="3af97-250">Entry</span></span> | <span data-ttu-id="3af97-251">Значение</span><span class="sxs-lookup"><span data-stu-id="3af97-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3af97-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3af97-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3af97-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3af97-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="3af97-254">System-Only</span></span>            | <span data-ttu-id="3af97-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-255">False</span></span>                                                 |
| <span data-ttu-id="3af97-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3af97-256">Is-Single-Valued</span></span>       | <span data-ttu-id="3af97-257">True</span><span class="sxs-lookup"><span data-stu-id="3af97-257">True</span></span>                                                  |
| <span data-ttu-id="3af97-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3af97-258">Is Indexed</span></span>             | <span data-ttu-id="3af97-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-259">False</span></span>                                                 |
| <span data-ttu-id="3af97-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3af97-260">In Global Catalog</span></span>      | <span data-ttu-id="3af97-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="3af97-261">False</span></span>                                                 |
| <span data-ttu-id="3af97-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3af97-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="3af97-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3af97-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3af97-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3af97-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3af97-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3af97-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-266">Search-Flags</span></span>           | <span data-ttu-id="3af97-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3af97-267">0x00000000</span></span>                                            |
| <span data-ttu-id="3af97-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3af97-268">System-Flags</span></span>           | <span data-ttu-id="3af97-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3af97-269">0x00000011</span></span>                                            |
| <span data-ttu-id="3af97-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3af97-270">Classes used in</span></span>        | [<span data-ttu-id="3af97-271">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="3af97-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





