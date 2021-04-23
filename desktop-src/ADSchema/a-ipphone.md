---
title: Phone-IP-первичный атрибут
description: Адрес TCP/IP для телефона. Используется телефонией.
ms.assetid: b51f28e4-4677-4798-87f1-2bd952a528ea
ms.tgt_platform: multiple
keywords:
- Phone-IP — первичная схема AD атрибутов
- Схема AD атрибута Ипфоне
topic_type:
- apiref
api_name:
- Phone-Ip-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4f16d29f6b3f45c5a229d76ec30c0dd7efdea2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138127"
---
# <a name="phone-ip-primary-attribute"></a><span data-ttu-id="78856-106">Phone-IP-первичный атрибут</span><span class="sxs-lookup"><span data-stu-id="78856-106">Phone-Ip-Primary attribute</span></span>

<span data-ttu-id="78856-107">Адрес TCP/IP для телефона.</span><span class="sxs-lookup"><span data-stu-id="78856-107">The TCP/IP address for the phone.</span></span> <span data-ttu-id="78856-108">Используется телефонией.</span><span class="sxs-lookup"><span data-stu-id="78856-108">Used by Telephony.</span></span>



| <span data-ttu-id="78856-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-109">Entry</span></span> | <span data-ttu-id="78856-110">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78856-111">CN</span><span class="sxs-lookup"><span data-stu-id="78856-111">CN</span></span>                | <span data-ttu-id="78856-112">Телефон — IP-адрес — основной</span><span class="sxs-lookup"><span data-stu-id="78856-112">Phone-Ip-Primary</span></span>                                                                 |
| <span data-ttu-id="78856-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="78856-113">Ldap-Display-Name</span></span> | <span data-ttu-id="78856-114">ipPhone</span><span class="sxs-lookup"><span data-stu-id="78856-114">ipPhone</span></span>                                                                          |
| <span data-ttu-id="78856-115">Размер</span><span class="sxs-lookup"><span data-stu-id="78856-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="78856-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="78856-116">Update Privilege</span></span>  | <span data-ttu-id="78856-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78856-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="78856-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="78856-118">Update Frequency</span></span>  | <span data-ttu-id="78856-119">При создании записи пользователя и при необходимости изменения номера телефона.</span><span class="sxs-lookup"><span data-stu-id="78856-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="78856-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78856-120">Attribute-Id</span></span>      | <span data-ttu-id="78856-121">1.2.840.113556.1.4.721</span><span class="sxs-lookup"><span data-stu-id="78856-121">1.2.840.113556.1.4.721</span></span>                                                           |
| <span data-ttu-id="78856-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="78856-122">System-Id-Guid</span></span>    | <span data-ttu-id="78856-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="78856-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="78856-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78856-124">Syntax</span></span>            | [<span data-ttu-id="78856-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="78856-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="78856-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="78856-126">Implementations</span></span>

-   [<span data-ttu-id="78856-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78856-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78856-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78856-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78856-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78856-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78856-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78856-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78856-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78856-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78856-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78856-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78856-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78856-133">Windows 2000 Server</span></span>



| <span data-ttu-id="78856-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-134">Entry</span></span> | <span data-ttu-id="78856-135">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78856-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="78856-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78856-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="78856-138">System-Only</span></span>            | <span data-ttu-id="78856-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-139">False</span></span>                                                              |
| <span data-ttu-id="78856-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="78856-140">Is-Single-Valued</span></span>       | <span data-ttu-id="78856-141">True</span><span class="sxs-lookup"><span data-stu-id="78856-141">True</span></span>                                                               |
| <span data-ttu-id="78856-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="78856-142">Is Indexed</span></span>             | <span data-ttu-id="78856-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-143">False</span></span>                                                              |
| <span data-ttu-id="78856-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="78856-144">In Global Catalog</span></span>      | <span data-ttu-id="78856-145">True</span><span class="sxs-lookup"><span data-stu-id="78856-145">True</span></span>                                                               |
| <span data-ttu-id="78856-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="78856-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="78856-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78856-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="78856-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78856-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78856-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-150">Search-Flags</span></span>           | <span data-ttu-id="78856-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78856-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="78856-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-152">System-Flags</span></span>           | <span data-ttu-id="78856-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78856-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="78856-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="78856-154">Classes used in</span></span>        | [<span data-ttu-id="78856-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="78856-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78856-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78856-156">Windows Server 2003</span></span>



| <span data-ttu-id="78856-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-157">Entry</span></span> | <span data-ttu-id="78856-158">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78856-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="78856-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78856-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="78856-161">System-Only</span></span>            | <span data-ttu-id="78856-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-162">False</span></span>                                                              |
| <span data-ttu-id="78856-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="78856-163">Is-Single-Valued</span></span>       | <span data-ttu-id="78856-164">True</span><span class="sxs-lookup"><span data-stu-id="78856-164">True</span></span>                                                               |
| <span data-ttu-id="78856-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="78856-165">Is Indexed</span></span>             | <span data-ttu-id="78856-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-166">False</span></span>                                                              |
| <span data-ttu-id="78856-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="78856-167">In Global Catalog</span></span>      | <span data-ttu-id="78856-168">True</span><span class="sxs-lookup"><span data-stu-id="78856-168">True</span></span>                                                               |
| <span data-ttu-id="78856-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="78856-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="78856-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78856-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="78856-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78856-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78856-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-173">Search-Flags</span></span>           | <span data-ttu-id="78856-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78856-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="78856-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-175">System-Flags</span></span>           | <span data-ttu-id="78856-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78856-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="78856-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="78856-177">Classes used in</span></span>        | [<span data-ttu-id="78856-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="78856-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78856-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78856-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78856-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-180">Entry</span></span> | <span data-ttu-id="78856-181">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78856-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="78856-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78856-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="78856-184">System-Only</span></span>            | <span data-ttu-id="78856-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-185">False</span></span>                                                              |
| <span data-ttu-id="78856-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="78856-186">Is-Single-Valued</span></span>       | <span data-ttu-id="78856-187">True</span><span class="sxs-lookup"><span data-stu-id="78856-187">True</span></span>                                                               |
| <span data-ttu-id="78856-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="78856-188">Is Indexed</span></span>             | <span data-ttu-id="78856-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-189">False</span></span>                                                              |
| <span data-ttu-id="78856-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="78856-190">In Global Catalog</span></span>      | <span data-ttu-id="78856-191">True</span><span class="sxs-lookup"><span data-stu-id="78856-191">True</span></span>                                                               |
| <span data-ttu-id="78856-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="78856-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="78856-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78856-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="78856-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78856-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78856-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-196">Search-Flags</span></span>           | <span data-ttu-id="78856-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78856-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="78856-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-198">System-Flags</span></span>           | <span data-ttu-id="78856-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78856-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="78856-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="78856-200">Classes used in</span></span>        | [<span data-ttu-id="78856-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="78856-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78856-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78856-202">Windows Server 2008</span></span>



| <span data-ttu-id="78856-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-203">Entry</span></span> | <span data-ttu-id="78856-204">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78856-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="78856-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78856-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="78856-207">System-Only</span></span>            | <span data-ttu-id="78856-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-208">False</span></span>                                                              |
| <span data-ttu-id="78856-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="78856-209">Is-Single-Valued</span></span>       | <span data-ttu-id="78856-210">True</span><span class="sxs-lookup"><span data-stu-id="78856-210">True</span></span>                                                               |
| <span data-ttu-id="78856-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="78856-211">Is Indexed</span></span>             | <span data-ttu-id="78856-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-212">False</span></span>                                                              |
| <span data-ttu-id="78856-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="78856-213">In Global Catalog</span></span>      | <span data-ttu-id="78856-214">True</span><span class="sxs-lookup"><span data-stu-id="78856-214">True</span></span>                                                               |
| <span data-ttu-id="78856-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="78856-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="78856-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78856-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="78856-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78856-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78856-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-219">Search-Flags</span></span>           | <span data-ttu-id="78856-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78856-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="78856-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-221">System-Flags</span></span>           | <span data-ttu-id="78856-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78856-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="78856-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="78856-223">Classes used in</span></span>        | [<span data-ttu-id="78856-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="78856-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78856-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78856-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78856-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-226">Entry</span></span> | <span data-ttu-id="78856-227">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78856-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="78856-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78856-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="78856-230">System-Only</span></span>            | <span data-ttu-id="78856-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-231">False</span></span>                                                              |
| <span data-ttu-id="78856-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="78856-232">Is-Single-Valued</span></span>       | <span data-ttu-id="78856-233">True</span><span class="sxs-lookup"><span data-stu-id="78856-233">True</span></span>                                                               |
| <span data-ttu-id="78856-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="78856-234">Is Indexed</span></span>             | <span data-ttu-id="78856-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-235">False</span></span>                                                              |
| <span data-ttu-id="78856-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="78856-236">In Global Catalog</span></span>      | <span data-ttu-id="78856-237">True</span><span class="sxs-lookup"><span data-stu-id="78856-237">True</span></span>                                                               |
| <span data-ttu-id="78856-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="78856-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="78856-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78856-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="78856-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78856-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78856-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-242">Search-Flags</span></span>           | <span data-ttu-id="78856-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78856-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="78856-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-244">System-Flags</span></span>           | <span data-ttu-id="78856-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78856-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="78856-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="78856-246">Classes used in</span></span>        | [<span data-ttu-id="78856-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="78856-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78856-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78856-248">Windows Server 2012</span></span>



| <span data-ttu-id="78856-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="78856-249">Entry</span></span> | <span data-ttu-id="78856-250">Значение</span><span class="sxs-lookup"><span data-stu-id="78856-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78856-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="78856-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78856-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="78856-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="78856-253">System-Only</span></span>            | <span data-ttu-id="78856-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-254">False</span></span>                                                              |
| <span data-ttu-id="78856-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="78856-255">Is-Single-Valued</span></span>       | <span data-ttu-id="78856-256">True</span><span class="sxs-lookup"><span data-stu-id="78856-256">True</span></span>                                                               |
| <span data-ttu-id="78856-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="78856-257">Is Indexed</span></span>             | <span data-ttu-id="78856-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="78856-258">False</span></span>                                                              |
| <span data-ttu-id="78856-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="78856-259">In Global Catalog</span></span>      | <span data-ttu-id="78856-260">True</span><span class="sxs-lookup"><span data-stu-id="78856-260">True</span></span>                                                               |
| <span data-ttu-id="78856-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="78856-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="78856-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78856-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="78856-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78856-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78856-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="78856-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-265">Search-Flags</span></span>           | <span data-ttu-id="78856-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78856-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="78856-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78856-267">System-Flags</span></span>           | <span data-ttu-id="78856-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78856-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="78856-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="78856-269">Classes used in</span></span>        | [<span data-ttu-id="78856-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="78856-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





