---
title: Phone-IP — другой атрибут
description: Список альтернативных TCP/IP-адресов для телефона. Используется телефонией.
ms.assetid: 3689c561-6dc1-4d73-adec-01c4ebdb5e47
ms.tgt_platform: multiple
keywords:
- Phone-IP — другая схема AD атрибутов
- Схема AD атрибута Осерипфоне
topic_type:
- apiref
api_name:
- Phone-Ip-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7955b4fb80d46c19e5536517b53eb419e6de9ec6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655321"
---
# <a name="phone-ip-other-attribute"></a><span data-ttu-id="acb9b-106">Phone-IP — другой атрибут</span><span class="sxs-lookup"><span data-stu-id="acb9b-106">Phone-Ip-Other attribute</span></span>

<span data-ttu-id="acb9b-107">Список альтернативных TCP/IP-адресов для телефона.</span><span class="sxs-lookup"><span data-stu-id="acb9b-107">The list of alternate TCP/IP addresses for the phone.</span></span> <span data-ttu-id="acb9b-108">Используется телефонией.</span><span class="sxs-lookup"><span data-stu-id="acb9b-108">Used by Telephony.</span></span>



| <span data-ttu-id="acb9b-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-109">Entry</span></span> | <span data-ttu-id="acb9b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="acb9b-111">CN</span><span class="sxs-lookup"><span data-stu-id="acb9b-111">CN</span></span>                | <span data-ttu-id="acb9b-112">Phone — IP — другие</span><span class="sxs-lookup"><span data-stu-id="acb9b-112">Phone-Ip-Other</span></span>                                                                   |
| <span data-ttu-id="acb9b-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="acb9b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="acb9b-114">otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="acb9b-114">otherIpPhone</span></span>                                                                     |
| <span data-ttu-id="acb9b-115">Размер</span><span class="sxs-lookup"><span data-stu-id="acb9b-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="acb9b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="acb9b-116">Update Privilege</span></span>  | <span data-ttu-id="acb9b-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="acb9b-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="acb9b-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="acb9b-118">Update Frequency</span></span>  | <span data-ttu-id="acb9b-119">При создании записи пользователя и при необходимости изменения номера телефона.</span><span class="sxs-lookup"><span data-stu-id="acb9b-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="acb9b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-120">Attribute-Id</span></span>      | <span data-ttu-id="acb9b-121">1.2.840.113556.1.4.722</span><span class="sxs-lookup"><span data-stu-id="acb9b-121">1.2.840.113556.1.4.722</span></span>                                                           |
| <span data-ttu-id="acb9b-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="acb9b-122">System-Id-Guid</span></span>    | <span data-ttu-id="acb9b-123">4d146e4b-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="acb9b-123">4d146e4b-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="acb9b-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acb9b-124">Syntax</span></span>            | [<span data-ttu-id="acb9b-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="acb9b-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="acb9b-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="acb9b-126">Implementations</span></span>

-   [<span data-ttu-id="acb9b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="acb9b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="acb9b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="acb9b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="acb9b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="acb9b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="acb9b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="acb9b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="acb9b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="acb9b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="acb9b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="acb9b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="acb9b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="acb9b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="acb9b-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-134">Entry</span></span> | <span data-ttu-id="acb9b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb9b-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="acb9b-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="acb9b-138">System-Only</span></span>            | <span data-ttu-id="acb9b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-139">False</span></span>                                                              |
| <span data-ttu-id="acb9b-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="acb9b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="acb9b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-141">False</span></span>                                                              |
| <span data-ttu-id="acb9b-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="acb9b-142">Is Indexed</span></span>             | <span data-ttu-id="acb9b-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-143">False</span></span>                                                              |
| <span data-ttu-id="acb9b-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="acb9b-144">In Global Catalog</span></span>      | <span data-ttu-id="acb9b-145">True</span><span class="sxs-lookup"><span data-stu-id="acb9b-145">True</span></span>                                                               |
| <span data-ttu-id="acb9b-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="acb9b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="acb9b-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="acb9b-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="acb9b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acb9b-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acb9b-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-150">Search-Flags</span></span>           | <span data-ttu-id="acb9b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acb9b-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="acb9b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-152">System-Flags</span></span>           | <span data-ttu-id="acb9b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acb9b-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="acb9b-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="acb9b-154">Classes used in</span></span>        | [<span data-ttu-id="acb9b-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="acb9b-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="acb9b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acb9b-156">Windows Server 2003</span></span>



| <span data-ttu-id="acb9b-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-157">Entry</span></span> | <span data-ttu-id="acb9b-158">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb9b-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="acb9b-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="acb9b-161">System-Only</span></span>            | <span data-ttu-id="acb9b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-162">False</span></span>                                                              |
| <span data-ttu-id="acb9b-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="acb9b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="acb9b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-164">False</span></span>                                                              |
| <span data-ttu-id="acb9b-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="acb9b-165">Is Indexed</span></span>             | <span data-ttu-id="acb9b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-166">False</span></span>                                                              |
| <span data-ttu-id="acb9b-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="acb9b-167">In Global Catalog</span></span>      | <span data-ttu-id="acb9b-168">True</span><span class="sxs-lookup"><span data-stu-id="acb9b-168">True</span></span>                                                               |
| <span data-ttu-id="acb9b-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="acb9b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="acb9b-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="acb9b-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="acb9b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acb9b-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acb9b-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-173">Search-Flags</span></span>           | <span data-ttu-id="acb9b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acb9b-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="acb9b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-175">System-Flags</span></span>           | <span data-ttu-id="acb9b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acb9b-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="acb9b-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="acb9b-177">Classes used in</span></span>        | [<span data-ttu-id="acb9b-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="acb9b-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="acb9b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="acb9b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="acb9b-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-180">Entry</span></span> | <span data-ttu-id="acb9b-181">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb9b-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="acb9b-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="acb9b-184">System-Only</span></span>            | <span data-ttu-id="acb9b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-185">False</span></span>                                                              |
| <span data-ttu-id="acb9b-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="acb9b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="acb9b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-187">False</span></span>                                                              |
| <span data-ttu-id="acb9b-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="acb9b-188">Is Indexed</span></span>             | <span data-ttu-id="acb9b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-189">False</span></span>                                                              |
| <span data-ttu-id="acb9b-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="acb9b-190">In Global Catalog</span></span>      | <span data-ttu-id="acb9b-191">True</span><span class="sxs-lookup"><span data-stu-id="acb9b-191">True</span></span>                                                               |
| <span data-ttu-id="acb9b-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="acb9b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="acb9b-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="acb9b-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="acb9b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acb9b-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acb9b-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-196">Search-Flags</span></span>           | <span data-ttu-id="acb9b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acb9b-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="acb9b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-198">System-Flags</span></span>           | <span data-ttu-id="acb9b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acb9b-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="acb9b-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="acb9b-200">Classes used in</span></span>        | [<span data-ttu-id="acb9b-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="acb9b-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="acb9b-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acb9b-202">Windows Server 2008</span></span>



| <span data-ttu-id="acb9b-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-203">Entry</span></span> | <span data-ttu-id="acb9b-204">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb9b-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="acb9b-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="acb9b-207">System-Only</span></span>            | <span data-ttu-id="acb9b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-208">False</span></span>                                                              |
| <span data-ttu-id="acb9b-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="acb9b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="acb9b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-210">False</span></span>                                                              |
| <span data-ttu-id="acb9b-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="acb9b-211">Is Indexed</span></span>             | <span data-ttu-id="acb9b-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-212">False</span></span>                                                              |
| <span data-ttu-id="acb9b-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="acb9b-213">In Global Catalog</span></span>      | <span data-ttu-id="acb9b-214">True</span><span class="sxs-lookup"><span data-stu-id="acb9b-214">True</span></span>                                                               |
| <span data-ttu-id="acb9b-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="acb9b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="acb9b-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="acb9b-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="acb9b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acb9b-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acb9b-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-219">Search-Flags</span></span>           | <span data-ttu-id="acb9b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acb9b-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="acb9b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-221">System-Flags</span></span>           | <span data-ttu-id="acb9b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acb9b-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="acb9b-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="acb9b-223">Classes used in</span></span>        | [<span data-ttu-id="acb9b-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="acb9b-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="acb9b-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="acb9b-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="acb9b-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-226">Entry</span></span> | <span data-ttu-id="acb9b-227">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb9b-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="acb9b-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="acb9b-230">System-Only</span></span>            | <span data-ttu-id="acb9b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-231">False</span></span>                                                              |
| <span data-ttu-id="acb9b-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="acb9b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="acb9b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-233">False</span></span>                                                              |
| <span data-ttu-id="acb9b-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="acb9b-234">Is Indexed</span></span>             | <span data-ttu-id="acb9b-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-235">False</span></span>                                                              |
| <span data-ttu-id="acb9b-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="acb9b-236">In Global Catalog</span></span>      | <span data-ttu-id="acb9b-237">True</span><span class="sxs-lookup"><span data-stu-id="acb9b-237">True</span></span>                                                               |
| <span data-ttu-id="acb9b-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="acb9b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="acb9b-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="acb9b-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="acb9b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acb9b-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acb9b-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-242">Search-Flags</span></span>           | <span data-ttu-id="acb9b-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acb9b-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="acb9b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-244">System-Flags</span></span>           | <span data-ttu-id="acb9b-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acb9b-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="acb9b-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="acb9b-246">Classes used in</span></span>        | [<span data-ttu-id="acb9b-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="acb9b-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="acb9b-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acb9b-248">Windows Server 2012</span></span>



| <span data-ttu-id="acb9b-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="acb9b-249">Entry</span></span> | <span data-ttu-id="acb9b-250">Значение</span><span class="sxs-lookup"><span data-stu-id="acb9b-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb9b-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="acb9b-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acb9b-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="acb9b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="acb9b-253">System-Only</span></span>            | <span data-ttu-id="acb9b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-254">False</span></span>                                                              |
| <span data-ttu-id="acb9b-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="acb9b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="acb9b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-256">False</span></span>                                                              |
| <span data-ttu-id="acb9b-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="acb9b-257">Is Indexed</span></span>             | <span data-ttu-id="acb9b-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="acb9b-258">False</span></span>                                                              |
| <span data-ttu-id="acb9b-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="acb9b-259">In Global Catalog</span></span>      | <span data-ttu-id="acb9b-260">True</span><span class="sxs-lookup"><span data-stu-id="acb9b-260">True</span></span>                                                               |
| <span data-ttu-id="acb9b-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="acb9b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="acb9b-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="acb9b-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="acb9b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acb9b-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acb9b-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="acb9b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-265">Search-Flags</span></span>           | <span data-ttu-id="acb9b-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acb9b-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="acb9b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acb9b-267">System-Flags</span></span>           | <span data-ttu-id="acb9b-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acb9b-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="acb9b-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="acb9b-269">Classes used in</span></span>        | [<span data-ttu-id="acb9b-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="acb9b-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





