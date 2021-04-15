---
title: Атрибут Server-Role
description: Для совместимости с серверами пред-Windows 2000 Server. Компьютер под управлением Windows NT Server может быть автономным сервером, основным контроллером домена (PDC) или резервным контроллером домена (BDC).
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Server-Role
- Схема AD атрибута serverRole
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655289"
---
# <a name="server-role-attribute"></a><span data-ttu-id="21ef4-106">Атрибут Server-Role</span><span class="sxs-lookup"><span data-stu-id="21ef4-106">Server-Role attribute</span></span>

<span data-ttu-id="21ef4-107">Для совместимости с серверами пред-Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="21ef4-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="21ef4-108">Компьютер под управлением Windows NT Server может быть автономным сервером, основным контроллером домена (PDC) или резервным контроллером домена (BDC).</span><span class="sxs-lookup"><span data-stu-id="21ef4-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="21ef4-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-109">Entry</span></span> | <span data-ttu-id="21ef4-110">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="21ef4-111">CN</span><span class="sxs-lookup"><span data-stu-id="21ef4-111">CN</span></span>                | <span data-ttu-id="21ef4-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="21ef4-112">Server-Role</span></span>                          |
| <span data-ttu-id="21ef4-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="21ef4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="21ef4-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="21ef4-114">serverRole</span></span>                           |
| <span data-ttu-id="21ef4-115">Размер</span><span class="sxs-lookup"><span data-stu-id="21ef4-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="21ef4-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="21ef4-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="21ef4-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="21ef4-117">Update Frequency</span></span>  | <span data-ttu-id="21ef4-118">4 байта</span><span class="sxs-lookup"><span data-stu-id="21ef4-118">4 bytes</span></span>                              |
| <span data-ttu-id="21ef4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-119">Attribute-Id</span></span>      | <span data-ttu-id="21ef4-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="21ef4-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="21ef4-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="21ef4-121">System-Id-Guid</span></span>    | <span data-ttu-id="21ef4-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="21ef4-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="21ef4-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21ef4-123">Syntax</span></span>            | [<span data-ttu-id="21ef4-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="21ef4-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="21ef4-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="21ef4-125">Implementations</span></span>

-   [<span data-ttu-id="21ef4-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21ef4-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21ef4-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21ef4-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21ef4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21ef4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21ef4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21ef4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21ef4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21ef4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21ef4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21ef4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21ef4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21ef4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="21ef4-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-133">Entry</span></span> | <span data-ttu-id="21ef4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="21ef4-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21ef4-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="21ef4-137">System-Only</span></span>            | <span data-ttu-id="21ef4-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-138">False</span></span>                                                 |
| <span data-ttu-id="21ef4-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21ef4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="21ef4-140">True</span><span class="sxs-lookup"><span data-stu-id="21ef4-140">True</span></span>                                                  |
| <span data-ttu-id="21ef4-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21ef4-141">Is Indexed</span></span>             | <span data-ttu-id="21ef4-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-142">False</span></span>                                                 |
| <span data-ttu-id="21ef4-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21ef4-143">In Global Catalog</span></span>      | <span data-ttu-id="21ef4-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-144">False</span></span>                                                 |
| <span data-ttu-id="21ef4-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21ef4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="21ef4-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21ef4-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="21ef4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21ef4-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21ef4-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-149">Search-Flags</span></span>           | <span data-ttu-id="21ef4-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21ef4-150">0x00000000</span></span>                                            |
| <span data-ttu-id="21ef4-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-151">System-Flags</span></span>           | <span data-ttu-id="21ef4-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21ef4-152">0x00000010</span></span>                                            |
| <span data-ttu-id="21ef4-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21ef4-153">Classes used in</span></span>        | [<span data-ttu-id="21ef4-154">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="21ef4-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21ef4-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21ef4-155">Windows Server 2003</span></span>



| <span data-ttu-id="21ef4-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-156">Entry</span></span> | <span data-ttu-id="21ef4-157">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="21ef4-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21ef4-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="21ef4-160">System-Only</span></span>            | <span data-ttu-id="21ef4-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-161">False</span></span>                                                 |
| <span data-ttu-id="21ef4-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21ef4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="21ef4-163">True</span><span class="sxs-lookup"><span data-stu-id="21ef4-163">True</span></span>                                                  |
| <span data-ttu-id="21ef4-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21ef4-164">Is Indexed</span></span>             | <span data-ttu-id="21ef4-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-165">False</span></span>                                                 |
| <span data-ttu-id="21ef4-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21ef4-166">In Global Catalog</span></span>      | <span data-ttu-id="21ef4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-167">False</span></span>                                                 |
| <span data-ttu-id="21ef4-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21ef4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="21ef4-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21ef4-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="21ef4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21ef4-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21ef4-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-172">Search-Flags</span></span>           | <span data-ttu-id="21ef4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21ef4-173">0x00000000</span></span>                                            |
| <span data-ttu-id="21ef4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-174">System-Flags</span></span>           | <span data-ttu-id="21ef4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21ef4-175">0x00000010</span></span>                                            |
| <span data-ttu-id="21ef4-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21ef4-176">Classes used in</span></span>        | [<span data-ttu-id="21ef4-177">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="21ef4-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21ef4-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21ef4-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21ef4-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-179">Entry</span></span> | <span data-ttu-id="21ef4-180">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="21ef4-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21ef4-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="21ef4-183">System-Only</span></span>            | <span data-ttu-id="21ef4-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-184">False</span></span>                                                 |
| <span data-ttu-id="21ef4-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21ef4-185">Is-Single-Valued</span></span>       | <span data-ttu-id="21ef4-186">True</span><span class="sxs-lookup"><span data-stu-id="21ef4-186">True</span></span>                                                  |
| <span data-ttu-id="21ef4-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21ef4-187">Is Indexed</span></span>             | <span data-ttu-id="21ef4-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-188">False</span></span>                                                 |
| <span data-ttu-id="21ef4-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21ef4-189">In Global Catalog</span></span>      | <span data-ttu-id="21ef4-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-190">False</span></span>                                                 |
| <span data-ttu-id="21ef4-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21ef4-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="21ef4-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21ef4-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="21ef4-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21ef4-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21ef4-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-195">Search-Flags</span></span>           | <span data-ttu-id="21ef4-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21ef4-196">0x00000000</span></span>                                            |
| <span data-ttu-id="21ef4-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-197">System-Flags</span></span>           | <span data-ttu-id="21ef4-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21ef4-198">0x00000010</span></span>                                            |
| <span data-ttu-id="21ef4-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21ef4-199">Classes used in</span></span>        | [<span data-ttu-id="21ef4-200">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="21ef4-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21ef4-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21ef4-201">Windows Server 2008</span></span>



| <span data-ttu-id="21ef4-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-202">Entry</span></span> | <span data-ttu-id="21ef4-203">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="21ef4-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21ef4-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="21ef4-206">System-Only</span></span>            | <span data-ttu-id="21ef4-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-207">False</span></span>                                                 |
| <span data-ttu-id="21ef4-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21ef4-208">Is-Single-Valued</span></span>       | <span data-ttu-id="21ef4-209">True</span><span class="sxs-lookup"><span data-stu-id="21ef4-209">True</span></span>                                                  |
| <span data-ttu-id="21ef4-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21ef4-210">Is Indexed</span></span>             | <span data-ttu-id="21ef4-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-211">False</span></span>                                                 |
| <span data-ttu-id="21ef4-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21ef4-212">In Global Catalog</span></span>      | <span data-ttu-id="21ef4-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-213">False</span></span>                                                 |
| <span data-ttu-id="21ef4-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21ef4-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="21ef4-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21ef4-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="21ef4-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21ef4-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21ef4-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-218">Search-Flags</span></span>           | <span data-ttu-id="21ef4-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21ef4-219">0x00000000</span></span>                                            |
| <span data-ttu-id="21ef4-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-220">System-Flags</span></span>           | <span data-ttu-id="21ef4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21ef4-221">0x00000010</span></span>                                            |
| <span data-ttu-id="21ef4-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21ef4-222">Classes used in</span></span>        | [<span data-ttu-id="21ef4-223">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="21ef4-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21ef4-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21ef4-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21ef4-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-225">Entry</span></span> | <span data-ttu-id="21ef4-226">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="21ef4-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21ef4-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="21ef4-229">System-Only</span></span>            | <span data-ttu-id="21ef4-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-230">False</span></span>                                                 |
| <span data-ttu-id="21ef4-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21ef4-231">Is-Single-Valued</span></span>       | <span data-ttu-id="21ef4-232">True</span><span class="sxs-lookup"><span data-stu-id="21ef4-232">True</span></span>                                                  |
| <span data-ttu-id="21ef4-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21ef4-233">Is Indexed</span></span>             | <span data-ttu-id="21ef4-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-234">False</span></span>                                                 |
| <span data-ttu-id="21ef4-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21ef4-235">In Global Catalog</span></span>      | <span data-ttu-id="21ef4-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-236">False</span></span>                                                 |
| <span data-ttu-id="21ef4-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21ef4-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="21ef4-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21ef4-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="21ef4-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21ef4-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21ef4-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-241">Search-Flags</span></span>           | <span data-ttu-id="21ef4-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21ef4-242">0x00000000</span></span>                                            |
| <span data-ttu-id="21ef4-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-243">System-Flags</span></span>           | <span data-ttu-id="21ef4-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21ef4-244">0x00000010</span></span>                                            |
| <span data-ttu-id="21ef4-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21ef4-245">Classes used in</span></span>        | [<span data-ttu-id="21ef4-246">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="21ef4-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21ef4-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21ef4-247">Windows Server 2012</span></span>



| <span data-ttu-id="21ef4-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="21ef4-248">Entry</span></span> | <span data-ttu-id="21ef4-249">Значение</span><span class="sxs-lookup"><span data-stu-id="21ef4-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="21ef4-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21ef4-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21ef4-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="21ef4-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="21ef4-252">System-Only</span></span>            | <span data-ttu-id="21ef4-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-253">False</span></span>                                                 |
| <span data-ttu-id="21ef4-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21ef4-254">Is-Single-Valued</span></span>       | <span data-ttu-id="21ef4-255">True</span><span class="sxs-lookup"><span data-stu-id="21ef4-255">True</span></span>                                                  |
| <span data-ttu-id="21ef4-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21ef4-256">Is Indexed</span></span>             | <span data-ttu-id="21ef4-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-257">False</span></span>                                                 |
| <span data-ttu-id="21ef4-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21ef4-258">In Global Catalog</span></span>      | <span data-ttu-id="21ef4-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="21ef4-259">False</span></span>                                                 |
| <span data-ttu-id="21ef4-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21ef4-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="21ef4-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21ef4-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="21ef4-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21ef4-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21ef4-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="21ef4-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-264">Search-Flags</span></span>           | <span data-ttu-id="21ef4-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21ef4-265">0x00000000</span></span>                                            |
| <span data-ttu-id="21ef4-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21ef4-266">System-Flags</span></span>           | <span data-ttu-id="21ef4-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21ef4-267">0x00000010</span></span>                                            |
| <span data-ttu-id="21ef4-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21ef4-268">Classes used in</span></span>        | [<span data-ttu-id="21ef4-269">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="21ef4-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





