---
title: Атрибут Given-Name
description: Содержит заданное имя (имя) пользователя.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Given-Name
- Схема AD атрибута givenName
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893601"
---
# <a name="given-name-attribute"></a><span data-ttu-id="11f2b-105">Атрибут Given-Name</span><span class="sxs-lookup"><span data-stu-id="11f2b-105">Given-Name attribute</span></span>

<span data-ttu-id="11f2b-106">Содержит заданное имя (имя) пользователя.</span><span class="sxs-lookup"><span data-stu-id="11f2b-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="11f2b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-107">Entry</span></span> | <span data-ttu-id="11f2b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="11f2b-109">CN</span><span class="sxs-lookup"><span data-stu-id="11f2b-109">CN</span></span>                | <span data-ttu-id="11f2b-110">Given-Name</span><span class="sxs-lookup"><span data-stu-id="11f2b-110">Given-Name</span></span>                                  |
| <span data-ttu-id="11f2b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="11f2b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="11f2b-112">givenName</span><span class="sxs-lookup"><span data-stu-id="11f2b-112">givenName</span></span>                                   |
| <span data-ttu-id="11f2b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="11f2b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="11f2b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="11f2b-114">Update Privilege</span></span>  | <span data-ttu-id="11f2b-115">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="11f2b-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="11f2b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="11f2b-116">Update Frequency</span></span>  | <span data-ttu-id="11f2b-117">При создании записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="11f2b-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="11f2b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-118">Attribute-Id</span></span>      | <span data-ttu-id="11f2b-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="11f2b-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="11f2b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="11f2b-120">System-Id-Guid</span></span>    | <span data-ttu-id="11f2b-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="11f2b-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="11f2b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11f2b-122">Syntax</span></span>            | [<span data-ttu-id="11f2b-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="11f2b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="11f2b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="11f2b-124">Implementations</span></span>

-   [<span data-ttu-id="11f2b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="11f2b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="11f2b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="11f2b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="11f2b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="11f2b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="11f2b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="11f2b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="11f2b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="11f2b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="11f2b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="11f2b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="11f2b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11f2b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="11f2b-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-132">Entry</span></span> | <span data-ttu-id="11f2b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="11f2b-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="11f2b-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="11f2b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-135">MAPI-Id</span></span>                | <span data-ttu-id="11f2b-136">0x3A06</span><span class="sxs-lookup"><span data-stu-id="11f2b-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="11f2b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="11f2b-137">System-Only</span></span>            | <span data-ttu-id="11f2b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="11f2b-138">False</span></span>                                                              |
| <span data-ttu-id="11f2b-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="11f2b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="11f2b-140">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-140">True</span></span>                                                               |
| <span data-ttu-id="11f2b-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="11f2b-141">Is Indexed</span></span>             | <span data-ttu-id="11f2b-142">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-142">True</span></span>                                                               |
| <span data-ttu-id="11f2b-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="11f2b-143">In Global Catalog</span></span>      | <span data-ttu-id="11f2b-144">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-144">True</span></span>                                                               |
| <span data-ttu-id="11f2b-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="11f2b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="11f2b-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11f2b-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="11f2b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11f2b-147">Range-Lower</span></span>            | <span data-ttu-id="11f2b-148">1</span><span class="sxs-lookup"><span data-stu-id="11f2b-148">1</span></span>                                                                  |
| <span data-ttu-id="11f2b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11f2b-149">Range-Upper</span></span>            | <span data-ttu-id="11f2b-150">64</span><span class="sxs-lookup"><span data-stu-id="11f2b-150">64</span></span>                                                                 |
| <span data-ttu-id="11f2b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-151">Search-Flags</span></span>           | <span data-ttu-id="11f2b-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="11f2b-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="11f2b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-153">System-Flags</span></span>           | <span data-ttu-id="11f2b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11f2b-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="11f2b-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="11f2b-155">Classes used in</span></span>        | [<span data-ttu-id="11f2b-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="11f2b-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="11f2b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11f2b-157">Windows Server 2003</span></span>



| <span data-ttu-id="11f2b-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-158">Entry</span></span> | <span data-ttu-id="11f2b-159">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f2b-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="11f2b-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="11f2b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-161">MAPI-Id</span></span>                | <span data-ttu-id="11f2b-162">0x3A06</span><span class="sxs-lookup"><span data-stu-id="11f2b-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="11f2b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="11f2b-163">System-Only</span></span>            | <span data-ttu-id="11f2b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="11f2b-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="11f2b-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="11f2b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="11f2b-166">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="11f2b-167">Is Indexed</span></span>             | <span data-ttu-id="11f2b-168">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="11f2b-169">In Global Catalog</span></span>      | <span data-ttu-id="11f2b-170">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="11f2b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="11f2b-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11f2b-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="11f2b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11f2b-173">Range-Lower</span></span>            | <span data-ttu-id="11f2b-174">1</span><span class="sxs-lookup"><span data-stu-id="11f2b-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="11f2b-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11f2b-175">Range-Upper</span></span>            | <span data-ttu-id="11f2b-176">64</span><span class="sxs-lookup"><span data-stu-id="11f2b-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="11f2b-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-177">Search-Flags</span></span>           | <span data-ttu-id="11f2b-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="11f2b-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-179">System-Flags</span></span>           | <span data-ttu-id="11f2b-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11f2b-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="11f2b-181">Classes used in</span></span>        | [<span data-ttu-id="11f2b-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="11f2b-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="11f2b-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="11f2b-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="11f2b-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="11f2b-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="11f2b-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-185">Entry</span></span> | <span data-ttu-id="11f2b-186">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f2b-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="11f2b-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="11f2b-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-188">MAPI-Id</span></span>                | <span data-ttu-id="11f2b-189">0x3A06</span><span class="sxs-lookup"><span data-stu-id="11f2b-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="11f2b-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="11f2b-190">System-Only</span></span>            | <span data-ttu-id="11f2b-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="11f2b-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="11f2b-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="11f2b-192">Is-Single-Valued</span></span>       | <span data-ttu-id="11f2b-193">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="11f2b-194">Is Indexed</span></span>             | <span data-ttu-id="11f2b-195">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="11f2b-196">In Global Catalog</span></span>      | <span data-ttu-id="11f2b-197">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="11f2b-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="11f2b-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11f2b-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="11f2b-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11f2b-200">Range-Lower</span></span>            | <span data-ttu-id="11f2b-201">1</span><span class="sxs-lookup"><span data-stu-id="11f2b-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="11f2b-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11f2b-202">Range-Upper</span></span>            | <span data-ttu-id="11f2b-203">64</span><span class="sxs-lookup"><span data-stu-id="11f2b-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="11f2b-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-204">Search-Flags</span></span>           | <span data-ttu-id="11f2b-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="11f2b-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-206">System-Flags</span></span>           | <span data-ttu-id="11f2b-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11f2b-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="11f2b-208">Classes used in</span></span>        | [<span data-ttu-id="11f2b-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="11f2b-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="11f2b-210">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="11f2b-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="11f2b-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11f2b-211">Windows Server 2008</span></span>



| <span data-ttu-id="11f2b-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-212">Entry</span></span> | <span data-ttu-id="11f2b-213">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f2b-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="11f2b-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="11f2b-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-215">MAPI-Id</span></span>                | <span data-ttu-id="11f2b-216">0x3A06</span><span class="sxs-lookup"><span data-stu-id="11f2b-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="11f2b-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="11f2b-217">System-Only</span></span>            | <span data-ttu-id="11f2b-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="11f2b-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="11f2b-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="11f2b-219">Is-Single-Valued</span></span>       | <span data-ttu-id="11f2b-220">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="11f2b-221">Is Indexed</span></span>             | <span data-ttu-id="11f2b-222">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="11f2b-223">In Global Catalog</span></span>      | <span data-ttu-id="11f2b-224">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="11f2b-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="11f2b-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11f2b-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="11f2b-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11f2b-227">Range-Lower</span></span>            | <span data-ttu-id="11f2b-228">1</span><span class="sxs-lookup"><span data-stu-id="11f2b-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="11f2b-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11f2b-229">Range-Upper</span></span>            | <span data-ttu-id="11f2b-230">64</span><span class="sxs-lookup"><span data-stu-id="11f2b-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="11f2b-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-231">Search-Flags</span></span>           | <span data-ttu-id="11f2b-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="11f2b-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-233">System-Flags</span></span>           | <span data-ttu-id="11f2b-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11f2b-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-235">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="11f2b-235">Classes used in</span></span>        | [<span data-ttu-id="11f2b-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="11f2b-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="11f2b-237">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="11f2b-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="11f2b-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11f2b-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="11f2b-239">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-239">Entry</span></span> | <span data-ttu-id="11f2b-240">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f2b-241">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="11f2b-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="11f2b-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-242">MAPI-Id</span></span>                | <span data-ttu-id="11f2b-243">0x3A06</span><span class="sxs-lookup"><span data-stu-id="11f2b-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="11f2b-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="11f2b-244">System-Only</span></span>            | <span data-ttu-id="11f2b-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="11f2b-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="11f2b-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="11f2b-246">Is-Single-Valued</span></span>       | <span data-ttu-id="11f2b-247">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="11f2b-248">Is Indexed</span></span>             | <span data-ttu-id="11f2b-249">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="11f2b-250">In Global Catalog</span></span>      | <span data-ttu-id="11f2b-251">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="11f2b-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="11f2b-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11f2b-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="11f2b-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11f2b-254">Range-Lower</span></span>            | <span data-ttu-id="11f2b-255">1</span><span class="sxs-lookup"><span data-stu-id="11f2b-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="11f2b-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11f2b-256">Range-Upper</span></span>            | <span data-ttu-id="11f2b-257">64</span><span class="sxs-lookup"><span data-stu-id="11f2b-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="11f2b-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-258">Search-Flags</span></span>           | <span data-ttu-id="11f2b-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="11f2b-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-260">System-Flags</span></span>           | <span data-ttu-id="11f2b-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11f2b-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-262">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="11f2b-262">Classes used in</span></span>        | [<span data-ttu-id="11f2b-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="11f2b-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="11f2b-264">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="11f2b-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="11f2b-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11f2b-265">Windows Server 2012</span></span>



| <span data-ttu-id="11f2b-266">Ввод</span><span class="sxs-lookup"><span data-stu-id="11f2b-266">Entry</span></span> | <span data-ttu-id="11f2b-267">Значение</span><span class="sxs-lookup"><span data-stu-id="11f2b-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f2b-268">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="11f2b-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="11f2b-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11f2b-269">MAPI-Id</span></span>                | <span data-ttu-id="11f2b-270">0x3A06</span><span class="sxs-lookup"><span data-stu-id="11f2b-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="11f2b-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="11f2b-271">System-Only</span></span>            | <span data-ttu-id="11f2b-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="11f2b-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="11f2b-273">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="11f2b-273">Is-Single-Valued</span></span>       | <span data-ttu-id="11f2b-274">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-275">Индексируется</span><span class="sxs-lookup"><span data-stu-id="11f2b-275">Is Indexed</span></span>             | <span data-ttu-id="11f2b-276">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-277">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="11f2b-277">In Global Catalog</span></span>      | <span data-ttu-id="11f2b-278">True</span><span class="sxs-lookup"><span data-stu-id="11f2b-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="11f2b-279">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="11f2b-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="11f2b-280">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11f2b-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="11f2b-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11f2b-281">Range-Lower</span></span>            | <span data-ttu-id="11f2b-282">1</span><span class="sxs-lookup"><span data-stu-id="11f2b-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="11f2b-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11f2b-283">Range-Upper</span></span>            | <span data-ttu-id="11f2b-284">64</span><span class="sxs-lookup"><span data-stu-id="11f2b-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="11f2b-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-285">Search-Flags</span></span>           | <span data-ttu-id="11f2b-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="11f2b-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11f2b-287">System-Flags</span></span>           | <span data-ttu-id="11f2b-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11f2b-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="11f2b-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="11f2b-289">Classes used in</span></span>        | [<span data-ttu-id="11f2b-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="11f2b-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="11f2b-291">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="11f2b-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





