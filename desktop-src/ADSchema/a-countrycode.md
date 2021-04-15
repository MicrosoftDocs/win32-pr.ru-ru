---
title: Атрибут Country-Code
description: Указывает код страны или региона для выбранного языка пользователя. Это значение не используется в Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Country-Code
- Схема AD атрибута Каунтрикоде
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655528"
---
# <a name="country-code-attribute"></a><span data-ttu-id="b7f79-106">Атрибут Country-Code</span><span class="sxs-lookup"><span data-stu-id="b7f79-106">Country-Code attribute</span></span>

<span data-ttu-id="b7f79-107">Указывает код страны или региона для выбранного языка пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7f79-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="b7f79-108">Это значение не используется в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b7f79-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="b7f79-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-109">Entry</span></span> | <span data-ttu-id="b7f79-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b7f79-111">CN</span><span class="sxs-lookup"><span data-stu-id="b7f79-111">CN</span></span>                | <span data-ttu-id="b7f79-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="b7f79-112">Country-Code</span></span>                            |
| <span data-ttu-id="b7f79-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b7f79-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b7f79-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="b7f79-114">countryCode</span></span>                             |
| <span data-ttu-id="b7f79-115">Размер</span><span class="sxs-lookup"><span data-stu-id="b7f79-115">Size</span></span>              | <span data-ttu-id="b7f79-116">2 байта</span><span class="sxs-lookup"><span data-stu-id="b7f79-116">2 bytes</span></span>                                 |
| <span data-ttu-id="b7f79-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b7f79-117">Update Privilege</span></span>  | <span data-ttu-id="b7f79-118">Владелец учетной записи или администратор домена</span><span class="sxs-lookup"><span data-stu-id="b7f79-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="b7f79-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b7f79-119">Update Frequency</span></span>  | <span data-ttu-id="b7f79-120">При изменении страны или региона пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7f79-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="b7f79-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-121">Attribute-Id</span></span>      | <span data-ttu-id="b7f79-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="b7f79-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="b7f79-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b7f79-123">System-Id-Guid</span></span>    | <span data-ttu-id="b7f79-124">5fd42471-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="b7f79-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="b7f79-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7f79-125">Syntax</span></span>            | [<span data-ttu-id="b7f79-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b7f79-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="b7f79-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b7f79-127">Implementations</span></span>

-   [<span data-ttu-id="b7f79-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7f79-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7f79-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7f79-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7f79-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b7f79-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b7f79-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7f79-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7f79-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7f79-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7f79-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7f79-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7f79-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7f79-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7f79-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7f79-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b7f79-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-136">Entry</span></span> | <span data-ttu-id="b7f79-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f79-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-140">System-Only</span></span>            | <span data-ttu-id="b7f79-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-143">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="b7f79-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-144">Is Indexed</span></span>             | <span data-ttu-id="b7f79-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-146">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="b7f79-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="b7f79-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="b7f79-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-152">Search-Flags</span></span>           | <span data-ttu-id="b7f79-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-154">System-Flags</span></span>           | <span data-ttu-id="b7f79-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-156">Classes used in</span></span>        | [<span data-ttu-id="b7f79-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="b7f79-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="b7f79-158">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7f79-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7f79-159">Windows Server 2003</span></span>



| <span data-ttu-id="b7f79-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-160">Entry</span></span> | <span data-ttu-id="b7f79-161">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f79-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-164">System-Only</span></span>            | <span data-ttu-id="b7f79-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-166">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-167">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="b7f79-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-168">Is Indexed</span></span>             | <span data-ttu-id="b7f79-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-170">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="b7f79-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-174">Range-Lower</span></span>            | <span data-ttu-id="b7f79-175">0</span><span class="sxs-lookup"><span data-stu-id="b7f79-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="b7f79-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-176">Range-Upper</span></span>            | <span data-ttu-id="b7f79-177">65535</span><span class="sxs-lookup"><span data-stu-id="b7f79-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-178">Search-Flags</span></span>           | <span data-ttu-id="b7f79-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-180">System-Flags</span></span>           | <span data-ttu-id="b7f79-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-182">Classes used in</span></span>        | [<span data-ttu-id="b7f79-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="b7f79-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="b7f79-184">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b7f79-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="b7f79-185">ADAM</span></span>



| <span data-ttu-id="b7f79-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-186">Entry</span></span> | <span data-ttu-id="b7f79-187">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b7f79-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7f79-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7f79-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-190">System-Only</span></span>            | <span data-ttu-id="b7f79-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-191">False</span></span>                                                          |
| <span data-ttu-id="b7f79-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-192">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-193">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-193">True</span></span>                                                           |
| <span data-ttu-id="b7f79-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-194">Is Indexed</span></span>             | <span data-ttu-id="b7f79-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-195">False</span></span>                                                          |
| <span data-ttu-id="b7f79-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-196">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-197">False</span></span>                                                          |
| <span data-ttu-id="b7f79-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b7f79-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-200">Range-Lower</span></span>            | <span data-ttu-id="b7f79-201">0</span><span class="sxs-lookup"><span data-stu-id="b7f79-201">0</span></span>                                                              |
| <span data-ttu-id="b7f79-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-202">Range-Upper</span></span>            | <span data-ttu-id="b7f79-203">65535</span><span class="sxs-lookup"><span data-stu-id="b7f79-203">65535</span></span>                                                          |
| <span data-ttu-id="b7f79-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-204">Search-Flags</span></span>           | <span data-ttu-id="b7f79-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="b7f79-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-206">System-Flags</span></span>           | <span data-ttu-id="b7f79-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="b7f79-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-208">Classes used in</span></span>        | [<span data-ttu-id="b7f79-209">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7f79-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7f79-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7f79-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-211">Entry</span></span> | <span data-ttu-id="b7f79-212">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f79-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-215">System-Only</span></span>            | <span data-ttu-id="b7f79-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-217">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-218">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="b7f79-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-219">Is Indexed</span></span>             | <span data-ttu-id="b7f79-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-221">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="b7f79-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-225">Range-Lower</span></span>            | <span data-ttu-id="b7f79-226">0</span><span class="sxs-lookup"><span data-stu-id="b7f79-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="b7f79-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-227">Range-Upper</span></span>            | <span data-ttu-id="b7f79-228">65535</span><span class="sxs-lookup"><span data-stu-id="b7f79-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-229">Search-Flags</span></span>           | <span data-ttu-id="b7f79-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-231">System-Flags</span></span>           | <span data-ttu-id="b7f79-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-233">Classes used in</span></span>        | [<span data-ttu-id="b7f79-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="b7f79-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="b7f79-235">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7f79-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7f79-236">Windows Server 2008</span></span>



| <span data-ttu-id="b7f79-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-237">Entry</span></span> | <span data-ttu-id="b7f79-238">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f79-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-241">System-Only</span></span>            | <span data-ttu-id="b7f79-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-243">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-244">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="b7f79-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-245">Is Indexed</span></span>             | <span data-ttu-id="b7f79-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-247">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="b7f79-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-251">Range-Lower</span></span>            | <span data-ttu-id="b7f79-252">0</span><span class="sxs-lookup"><span data-stu-id="b7f79-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="b7f79-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-253">Range-Upper</span></span>            | <span data-ttu-id="b7f79-254">65535</span><span class="sxs-lookup"><span data-stu-id="b7f79-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-255">Search-Flags</span></span>           | <span data-ttu-id="b7f79-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-257">System-Flags</span></span>           | <span data-ttu-id="b7f79-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-259">Classes used in</span></span>        | [<span data-ttu-id="b7f79-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="b7f79-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="b7f79-261">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7f79-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7f79-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7f79-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-263">Entry</span></span> | <span data-ttu-id="b7f79-264">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f79-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-267">System-Only</span></span>            | <span data-ttu-id="b7f79-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-269">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-270">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="b7f79-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-271">Is Indexed</span></span>             | <span data-ttu-id="b7f79-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-273">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="b7f79-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-277">Range-Lower</span></span>            | <span data-ttu-id="b7f79-278">0</span><span class="sxs-lookup"><span data-stu-id="b7f79-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="b7f79-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-279">Range-Upper</span></span>            | <span data-ttu-id="b7f79-280">65535</span><span class="sxs-lookup"><span data-stu-id="b7f79-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-281">Search-Flags</span></span>           | <span data-ttu-id="b7f79-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-283">System-Flags</span></span>           | <span data-ttu-id="b7f79-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-285">Classes used in</span></span>        | [<span data-ttu-id="b7f79-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="b7f79-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="b7f79-287">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7f79-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7f79-288">Windows Server 2012</span></span>



| <span data-ttu-id="b7f79-289">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7f79-289">Entry</span></span> | <span data-ttu-id="b7f79-290">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f79-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f79-291">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7f79-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7f79-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="b7f79-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7f79-293">System-Only</span></span>            | <span data-ttu-id="b7f79-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-295">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7f79-295">Is-Single-Valued</span></span>       | <span data-ttu-id="b7f79-296">True</span><span class="sxs-lookup"><span data-stu-id="b7f79-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="b7f79-297">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7f79-297">Is Indexed</span></span>             | <span data-ttu-id="b7f79-298">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-299">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7f79-299">In Global Catalog</span></span>      | <span data-ttu-id="b7f79-300">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7f79-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-301">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7f79-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7f79-302">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7f79-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="b7f79-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7f79-303">Range-Lower</span></span>            | <span data-ttu-id="b7f79-304">0</span><span class="sxs-lookup"><span data-stu-id="b7f79-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="b7f79-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7f79-305">Range-Upper</span></span>            | <span data-ttu-id="b7f79-306">65535</span><span class="sxs-lookup"><span data-stu-id="b7f79-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="b7f79-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-307">Search-Flags</span></span>           | <span data-ttu-id="b7f79-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7f79-309">System-Flags</span></span>           | <span data-ttu-id="b7f79-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7f79-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="b7f79-311">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7f79-311">Classes used in</span></span>        | [<span data-ttu-id="b7f79-312">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="b7f79-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="b7f79-313">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="b7f79-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





