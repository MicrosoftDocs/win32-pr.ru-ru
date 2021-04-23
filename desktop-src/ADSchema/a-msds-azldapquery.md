---
title: Атрибут ms-DS-AZ-LDAP-Query
description: Строка, определяющая запрос LDAP (максимальная длина 4096), который определяет членство объекта-пользователя в группе.
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута запроса MS-DS-AZ-LDAP
- Схема AD атрибута msDS-Азлдапкуери
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138674"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="a3563-105">Атрибут ms-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="a3563-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="a3563-106">Строка, определяющая запрос LDAP (максимальная длина 4096), который определяет членство объекта-пользователя в группе.</span><span class="sxs-lookup"><span data-stu-id="a3563-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="a3563-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a3563-107">Entry</span></span> | <span data-ttu-id="a3563-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a3563-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a3563-109">CN</span><span class="sxs-lookup"><span data-stu-id="a3563-109">CN</span></span>                | <span data-ttu-id="a3563-110">MS-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="a3563-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="a3563-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a3563-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a3563-112">msDS-Азлдапкуери</span><span class="sxs-lookup"><span data-stu-id="a3563-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="a3563-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a3563-113">Size</span></span>              | <span data-ttu-id="a3563-114">4096 символов</span><span class="sxs-lookup"><span data-stu-id="a3563-114">4096 characters</span></span>                             |
| <span data-ttu-id="a3563-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a3563-115">Update Privilege</span></span>  | <span data-ttu-id="a3563-116">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="a3563-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="a3563-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a3563-117">Update Frequency</span></span>  | <span data-ttu-id="a3563-118">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="a3563-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="a3563-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3563-119">Attribute-Id</span></span>      | <span data-ttu-id="a3563-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="a3563-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="a3563-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a3563-121">System-Id-Guid</span></span>    | <span data-ttu-id="a3563-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="a3563-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="a3563-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3563-123">Syntax</span></span>            | [<span data-ttu-id="a3563-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="a3563-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a3563-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a3563-125">Implementations</span></span>

-   [<span data-ttu-id="a3563-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3563-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3563-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3563-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3563-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3563-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3563-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3563-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3563-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3563-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a3563-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3563-131">Windows Server 2003</span></span>



| <span data-ttu-id="a3563-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="a3563-132">Entry</span></span> | <span data-ttu-id="a3563-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a3563-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="a3563-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a3563-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3563-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3563-136">System-Only</span></span>            | <span data-ttu-id="a3563-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-137">False</span></span>                               |
| <span data-ttu-id="a3563-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a3563-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a3563-139">True</span><span class="sxs-lookup"><span data-stu-id="a3563-139">True</span></span>                                |
| <span data-ttu-id="a3563-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a3563-140">Is Indexed</span></span>             | <span data-ttu-id="a3563-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-141">False</span></span>                               |
| <span data-ttu-id="a3563-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a3563-142">In Global Catalog</span></span>      | <span data-ttu-id="a3563-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-143">False</span></span>                               |
| <span data-ttu-id="a3563-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a3563-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3563-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3563-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="a3563-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3563-146">Range-Lower</span></span>            | <span data-ttu-id="a3563-147">0</span><span class="sxs-lookup"><span data-stu-id="a3563-147">0</span></span>                                   |
| <span data-ttu-id="a3563-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3563-148">Range-Upper</span></span>            | <span data-ttu-id="a3563-149">4096</span><span class="sxs-lookup"><span data-stu-id="a3563-149">4096</span></span>                                |
| <span data-ttu-id="a3563-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-150">Search-Flags</span></span>           | <span data-ttu-id="a3563-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3563-151">0x00000000</span></span>                          |
| <span data-ttu-id="a3563-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-152">System-Flags</span></span>           | <span data-ttu-id="a3563-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3563-153">0x00000010</span></span>                          |
| <span data-ttu-id="a3563-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a3563-154">Classes used in</span></span>        | [<span data-ttu-id="a3563-155">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a3563-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3563-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3563-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3563-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="a3563-157">Entry</span></span> | <span data-ttu-id="a3563-158">Значение</span><span class="sxs-lookup"><span data-stu-id="a3563-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="a3563-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a3563-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3563-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3563-161">System-Only</span></span>            | <span data-ttu-id="a3563-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-162">False</span></span>                               |
| <span data-ttu-id="a3563-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a3563-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a3563-164">True</span><span class="sxs-lookup"><span data-stu-id="a3563-164">True</span></span>                                |
| <span data-ttu-id="a3563-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a3563-165">Is Indexed</span></span>             | <span data-ttu-id="a3563-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-166">False</span></span>                               |
| <span data-ttu-id="a3563-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a3563-167">In Global Catalog</span></span>      | <span data-ttu-id="a3563-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-168">False</span></span>                               |
| <span data-ttu-id="a3563-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a3563-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3563-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3563-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="a3563-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3563-171">Range-Lower</span></span>            | <span data-ttu-id="a3563-172">0</span><span class="sxs-lookup"><span data-stu-id="a3563-172">0</span></span>                                   |
| <span data-ttu-id="a3563-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3563-173">Range-Upper</span></span>            | <span data-ttu-id="a3563-174">4096</span><span class="sxs-lookup"><span data-stu-id="a3563-174">4096</span></span>                                |
| <span data-ttu-id="a3563-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-175">Search-Flags</span></span>           | <span data-ttu-id="a3563-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3563-176">0x00000000</span></span>                          |
| <span data-ttu-id="a3563-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-177">System-Flags</span></span>           | <span data-ttu-id="a3563-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3563-178">0x00000010</span></span>                          |
| <span data-ttu-id="a3563-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a3563-179">Classes used in</span></span>        | [<span data-ttu-id="a3563-180">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a3563-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3563-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3563-181">Windows Server 2008</span></span>



| <span data-ttu-id="a3563-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="a3563-182">Entry</span></span> | <span data-ttu-id="a3563-183">Значение</span><span class="sxs-lookup"><span data-stu-id="a3563-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="a3563-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a3563-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3563-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3563-186">System-Only</span></span>            | <span data-ttu-id="a3563-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-187">False</span></span>                               |
| <span data-ttu-id="a3563-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a3563-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a3563-189">True</span><span class="sxs-lookup"><span data-stu-id="a3563-189">True</span></span>                                |
| <span data-ttu-id="a3563-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a3563-190">Is Indexed</span></span>             | <span data-ttu-id="a3563-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-191">False</span></span>                               |
| <span data-ttu-id="a3563-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a3563-192">In Global Catalog</span></span>      | <span data-ttu-id="a3563-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-193">False</span></span>                               |
| <span data-ttu-id="a3563-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a3563-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3563-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3563-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="a3563-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3563-196">Range-Lower</span></span>            | <span data-ttu-id="a3563-197">0</span><span class="sxs-lookup"><span data-stu-id="a3563-197">0</span></span>                                   |
| <span data-ttu-id="a3563-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3563-198">Range-Upper</span></span>            | <span data-ttu-id="a3563-199">4096</span><span class="sxs-lookup"><span data-stu-id="a3563-199">4096</span></span>                                |
| <span data-ttu-id="a3563-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-200">Search-Flags</span></span>           | <span data-ttu-id="a3563-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3563-201">0x00000000</span></span>                          |
| <span data-ttu-id="a3563-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-202">System-Flags</span></span>           | <span data-ttu-id="a3563-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3563-203">0x00000010</span></span>                          |
| <span data-ttu-id="a3563-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a3563-204">Classes used in</span></span>        | [<span data-ttu-id="a3563-205">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a3563-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3563-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3563-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3563-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="a3563-207">Entry</span></span> | <span data-ttu-id="a3563-208">Значение</span><span class="sxs-lookup"><span data-stu-id="a3563-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="a3563-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a3563-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3563-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3563-211">System-Only</span></span>            | <span data-ttu-id="a3563-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-212">False</span></span>                               |
| <span data-ttu-id="a3563-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a3563-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a3563-214">True</span><span class="sxs-lookup"><span data-stu-id="a3563-214">True</span></span>                                |
| <span data-ttu-id="a3563-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a3563-215">Is Indexed</span></span>             | <span data-ttu-id="a3563-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-216">False</span></span>                               |
| <span data-ttu-id="a3563-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a3563-217">In Global Catalog</span></span>      | <span data-ttu-id="a3563-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-218">False</span></span>                               |
| <span data-ttu-id="a3563-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a3563-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3563-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3563-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="a3563-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3563-221">Range-Lower</span></span>            | <span data-ttu-id="a3563-222">0</span><span class="sxs-lookup"><span data-stu-id="a3563-222">0</span></span>                                   |
| <span data-ttu-id="a3563-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3563-223">Range-Upper</span></span>            | <span data-ttu-id="a3563-224">4096</span><span class="sxs-lookup"><span data-stu-id="a3563-224">4096</span></span>                                |
| <span data-ttu-id="a3563-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-225">Search-Flags</span></span>           | <span data-ttu-id="a3563-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3563-226">0x00000000</span></span>                          |
| <span data-ttu-id="a3563-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-227">System-Flags</span></span>           | <span data-ttu-id="a3563-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3563-228">0x00000010</span></span>                          |
| <span data-ttu-id="a3563-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a3563-229">Classes used in</span></span>        | [<span data-ttu-id="a3563-230">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a3563-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3563-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3563-231">Windows Server 2012</span></span>



| <span data-ttu-id="a3563-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="a3563-232">Entry</span></span> | <span data-ttu-id="a3563-233">Значение</span><span class="sxs-lookup"><span data-stu-id="a3563-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="a3563-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a3563-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3563-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="a3563-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3563-236">System-Only</span></span>            | <span data-ttu-id="a3563-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-237">False</span></span>                               |
| <span data-ttu-id="a3563-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a3563-238">Is-Single-Valued</span></span>       | <span data-ttu-id="a3563-239">True</span><span class="sxs-lookup"><span data-stu-id="a3563-239">True</span></span>                                |
| <span data-ttu-id="a3563-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a3563-240">Is Indexed</span></span>             | <span data-ttu-id="a3563-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-241">False</span></span>                               |
| <span data-ttu-id="a3563-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a3563-242">In Global Catalog</span></span>      | <span data-ttu-id="a3563-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="a3563-243">False</span></span>                               |
| <span data-ttu-id="a3563-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a3563-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3563-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3563-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="a3563-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3563-246">Range-Lower</span></span>            | <span data-ttu-id="a3563-247">0</span><span class="sxs-lookup"><span data-stu-id="a3563-247">0</span></span>                                   |
| <span data-ttu-id="a3563-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3563-248">Range-Upper</span></span>            | <span data-ttu-id="a3563-249">4096</span><span class="sxs-lookup"><span data-stu-id="a3563-249">4096</span></span>                                |
| <span data-ttu-id="a3563-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-250">Search-Flags</span></span>           | <span data-ttu-id="a3563-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3563-251">0x00000000</span></span>                          |
| <span data-ttu-id="a3563-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3563-252">System-Flags</span></span>           | <span data-ttu-id="a3563-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3563-253">0x00000010</span></span>                          |
| <span data-ttu-id="a3563-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a3563-254">Classes used in</span></span>        | [<span data-ttu-id="a3563-255">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a3563-255">**Group**</span></span>](c-group.md)<br/> |



 

 





