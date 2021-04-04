---
title: Атрибут имени пользователя-участника
description: Этот атрибут содержит имя входа в Интернет для пользователя, основанного на стандарте RFC 822 в формате Интернета.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Имя пользователя-субъекта-схема атрибута AD
- Схема AD атрибута userPrincipalName
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989619"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="17748-105">Атрибут имени пользователя-участника</span><span class="sxs-lookup"><span data-stu-id="17748-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="17748-106">Этот атрибут содержит имя входа в Интернет для пользователя, основанного на стандарте [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)в формате Интернета.</span><span class="sxs-lookup"><span data-stu-id="17748-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="17748-107">Имя участника-пользователя короче различающегося имени и проще запомнить.</span><span class="sxs-lookup"><span data-stu-id="17748-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="17748-108">По соглашению оно должно сопоставляться с именем электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="17748-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="17748-109">Значение, заданное для этого атрибута, равно длине идентификатора пользователя и имени домена.</span><span class="sxs-lookup"><span data-stu-id="17748-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="17748-110">Дополнительные сведения об этом атрибуте см. в разделе [атрибуты именования пользователей](/windows/desktop/AD/naming-properties).</span><span class="sxs-lookup"><span data-stu-id="17748-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="17748-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-111">Entry</span></span> | <span data-ttu-id="17748-112">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="17748-113">CN</span><span class="sxs-lookup"><span data-stu-id="17748-113">CN</span></span>                | <span data-ttu-id="17748-114">User-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="17748-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="17748-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="17748-115">Ldap-Display-Name</span></span> | <span data-ttu-id="17748-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="17748-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="17748-117">Размер</span><span class="sxs-lookup"><span data-stu-id="17748-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="17748-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="17748-118">Update Privilege</span></span>  | <span data-ttu-id="17748-119">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="17748-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="17748-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="17748-120">Update Frequency</span></span>  | <span data-ttu-id="17748-121">Теоретически это не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="17748-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="17748-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17748-122">Attribute-Id</span></span>      | <span data-ttu-id="17748-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="17748-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="17748-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="17748-124">System-Id-Guid</span></span>    | <span data-ttu-id="17748-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="17748-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="17748-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17748-126">Syntax</span></span>            | [<span data-ttu-id="17748-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="17748-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="17748-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="17748-128">Implementations</span></span>

-   [<span data-ttu-id="17748-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="17748-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="17748-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17748-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17748-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="17748-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="17748-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17748-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17748-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17748-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17748-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17748-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17748-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17748-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="17748-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17748-136">Windows 2000 Server</span></span>



| <span data-ttu-id="17748-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-137">Entry</span></span> | <span data-ttu-id="17748-138">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17748-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-141">System-Only</span></span>            | <span data-ttu-id="17748-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-142">False</span></span>                             |
| <span data-ttu-id="17748-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-143">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-144">True</span><span class="sxs-lookup"><span data-stu-id="17748-144">True</span></span>                              |
| <span data-ttu-id="17748-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-145">Is Indexed</span></span>             | <span data-ttu-id="17748-146">True</span><span class="sxs-lookup"><span data-stu-id="17748-146">True</span></span>                              |
| <span data-ttu-id="17748-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-147">In Global Catalog</span></span>      | <span data-ttu-id="17748-148">True</span><span class="sxs-lookup"><span data-stu-id="17748-148">True</span></span>                              |
| <span data-ttu-id="17748-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17748-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17748-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17748-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-153">Search-Flags</span></span>           | <span data-ttu-id="17748-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-154">0x00000001</span></span>                        |
| <span data-ttu-id="17748-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-155">System-Flags</span></span>           | <span data-ttu-id="17748-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-156">0x00000012</span></span>                        |
| <span data-ttu-id="17748-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-157">Classes used in</span></span>        | [<span data-ttu-id="17748-158">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="17748-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="17748-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17748-159">Windows Server 2003</span></span>



| <span data-ttu-id="17748-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-160">Entry</span></span> | <span data-ttu-id="17748-161">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17748-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-164">System-Only</span></span>            | <span data-ttu-id="17748-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-165">False</span></span>                             |
| <span data-ttu-id="17748-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-166">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-167">True</span><span class="sxs-lookup"><span data-stu-id="17748-167">True</span></span>                              |
| <span data-ttu-id="17748-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-168">Is Indexed</span></span>             | <span data-ttu-id="17748-169">True</span><span class="sxs-lookup"><span data-stu-id="17748-169">True</span></span>                              |
| <span data-ttu-id="17748-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-170">In Global Catalog</span></span>      | <span data-ttu-id="17748-171">True</span><span class="sxs-lookup"><span data-stu-id="17748-171">True</span></span>                              |
| <span data-ttu-id="17748-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17748-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17748-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17748-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-176">Search-Flags</span></span>           | <span data-ttu-id="17748-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-177">0x00000001</span></span>                        |
| <span data-ttu-id="17748-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-178">System-Flags</span></span>           | <span data-ttu-id="17748-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-179">0x00000012</span></span>                        |
| <span data-ttu-id="17748-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-180">Classes used in</span></span>        | [<span data-ttu-id="17748-181">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="17748-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="17748-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="17748-182">ADAM</span></span>



| <span data-ttu-id="17748-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-183">Entry</span></span> | <span data-ttu-id="17748-184">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="17748-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="17748-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="17748-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-187">System-Only</span></span>            | <span data-ttu-id="17748-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-188">False</span></span>        |
| <span data-ttu-id="17748-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-189">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-190">True</span><span class="sxs-lookup"><span data-stu-id="17748-190">True</span></span>         |
| <span data-ttu-id="17748-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-191">Is Indexed</span></span>             | <span data-ttu-id="17748-192">True</span><span class="sxs-lookup"><span data-stu-id="17748-192">True</span></span>         |
| <span data-ttu-id="17748-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-193">In Global Catalog</span></span>      | <span data-ttu-id="17748-194">True</span><span class="sxs-lookup"><span data-stu-id="17748-194">True</span></span>         |
| <span data-ttu-id="17748-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="17748-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="17748-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="17748-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-199">Search-Flags</span></span>           | <span data-ttu-id="17748-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-200">0x00000001</span></span>   |
| <span data-ttu-id="17748-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-201">System-Flags</span></span>           | <span data-ttu-id="17748-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-202">0x00000012</span></span>   |
| <span data-ttu-id="17748-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17748-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17748-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17748-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-205">Entry</span></span> | <span data-ttu-id="17748-206">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17748-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-209">System-Only</span></span>            | <span data-ttu-id="17748-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-210">False</span></span>                             |
| <span data-ttu-id="17748-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-211">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-212">True</span><span class="sxs-lookup"><span data-stu-id="17748-212">True</span></span>                              |
| <span data-ttu-id="17748-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-213">Is Indexed</span></span>             | <span data-ttu-id="17748-214">True</span><span class="sxs-lookup"><span data-stu-id="17748-214">True</span></span>                              |
| <span data-ttu-id="17748-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-215">In Global Catalog</span></span>      | <span data-ttu-id="17748-216">True</span><span class="sxs-lookup"><span data-stu-id="17748-216">True</span></span>                              |
| <span data-ttu-id="17748-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17748-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17748-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17748-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-221">Search-Flags</span></span>           | <span data-ttu-id="17748-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-222">0x00000001</span></span>                        |
| <span data-ttu-id="17748-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-223">System-Flags</span></span>           | <span data-ttu-id="17748-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-224">0x00000012</span></span>                        |
| <span data-ttu-id="17748-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-225">Classes used in</span></span>        | [<span data-ttu-id="17748-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="17748-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17748-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17748-227">Windows Server 2008</span></span>



| <span data-ttu-id="17748-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-228">Entry</span></span> | <span data-ttu-id="17748-229">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17748-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-232">System-Only</span></span>            | <span data-ttu-id="17748-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-233">False</span></span>                             |
| <span data-ttu-id="17748-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-234">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-235">True</span><span class="sxs-lookup"><span data-stu-id="17748-235">True</span></span>                              |
| <span data-ttu-id="17748-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-236">Is Indexed</span></span>             | <span data-ttu-id="17748-237">True</span><span class="sxs-lookup"><span data-stu-id="17748-237">True</span></span>                              |
| <span data-ttu-id="17748-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-238">In Global Catalog</span></span>      | <span data-ttu-id="17748-239">True</span><span class="sxs-lookup"><span data-stu-id="17748-239">True</span></span>                              |
| <span data-ttu-id="17748-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17748-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17748-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17748-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-244">Search-Flags</span></span>           | <span data-ttu-id="17748-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-245">0x00000001</span></span>                        |
| <span data-ttu-id="17748-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-246">System-Flags</span></span>           | <span data-ttu-id="17748-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-247">0x00000012</span></span>                        |
| <span data-ttu-id="17748-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-248">Classes used in</span></span>        | [<span data-ttu-id="17748-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="17748-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17748-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17748-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17748-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-251">Entry</span></span> | <span data-ttu-id="17748-252">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17748-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-255">System-Only</span></span>            | <span data-ttu-id="17748-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-256">False</span></span>                             |
| <span data-ttu-id="17748-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-257">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-258">True</span><span class="sxs-lookup"><span data-stu-id="17748-258">True</span></span>                              |
| <span data-ttu-id="17748-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-259">Is Indexed</span></span>             | <span data-ttu-id="17748-260">True</span><span class="sxs-lookup"><span data-stu-id="17748-260">True</span></span>                              |
| <span data-ttu-id="17748-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-261">In Global Catalog</span></span>      | <span data-ttu-id="17748-262">True</span><span class="sxs-lookup"><span data-stu-id="17748-262">True</span></span>                              |
| <span data-ttu-id="17748-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17748-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17748-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17748-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-267">Search-Flags</span></span>           | <span data-ttu-id="17748-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-268">0x00000001</span></span>                        |
| <span data-ttu-id="17748-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-269">System-Flags</span></span>           | <span data-ttu-id="17748-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-270">0x00000012</span></span>                        |
| <span data-ttu-id="17748-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-271">Classes used in</span></span>        | [<span data-ttu-id="17748-272">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="17748-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17748-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17748-273">Windows Server 2012</span></span>



| <span data-ttu-id="17748-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="17748-274">Entry</span></span> | <span data-ttu-id="17748-275">Значение</span><span class="sxs-lookup"><span data-stu-id="17748-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17748-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17748-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17748-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17748-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="17748-278">System-Only</span></span>            | <span data-ttu-id="17748-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="17748-279">False</span></span>                             |
| <span data-ttu-id="17748-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17748-280">Is-Single-Valued</span></span>       | <span data-ttu-id="17748-281">True</span><span class="sxs-lookup"><span data-stu-id="17748-281">True</span></span>                              |
| <span data-ttu-id="17748-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17748-282">Is Indexed</span></span>             | <span data-ttu-id="17748-283">True</span><span class="sxs-lookup"><span data-stu-id="17748-283">True</span></span>                              |
| <span data-ttu-id="17748-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17748-284">In Global Catalog</span></span>      | <span data-ttu-id="17748-285">True</span><span class="sxs-lookup"><span data-stu-id="17748-285">True</span></span>                              |
| <span data-ttu-id="17748-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17748-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="17748-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17748-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17748-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17748-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17748-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17748-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17748-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-290">Search-Flags</span></span>           | <span data-ttu-id="17748-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17748-291">0x00000001</span></span>                        |
| <span data-ttu-id="17748-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17748-292">System-Flags</span></span>           | <span data-ttu-id="17748-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="17748-293">0x00000012</span></span>                        |
| <span data-ttu-id="17748-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17748-294">Classes used in</span></span>        | [<span data-ttu-id="17748-295">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="17748-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="17748-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17748-296">Remarks</span></span>

<span data-ttu-id="17748-297">В ADAM этот атрибут не обязательно должен быть в стандартном формате RFC 822. Это может быть простое имя.</span><span class="sxs-lookup"><span data-stu-id="17748-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

