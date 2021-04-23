---
title: Атрибут инициалов
description: Содержит инициалы для частей полного имени пользователя. Его можно использовать в качестве отчества в адресной книге Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Начальная схема атрибута AD
- начальная схема атрибута AD
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655267"
---
# <a name="initials-attribute"></a><span data-ttu-id="742a1-106">Атрибут инициалов</span><span class="sxs-lookup"><span data-stu-id="742a1-106">Initials attribute</span></span>

<span data-ttu-id="742a1-107">Содержит инициалы для частей полного имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="742a1-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="742a1-108">Его можно использовать в качестве отчества в адресной книге Windows.</span><span class="sxs-lookup"><span data-stu-id="742a1-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="742a1-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-109">Entry</span></span> | <span data-ttu-id="742a1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="742a1-111">CN</span><span class="sxs-lookup"><span data-stu-id="742a1-111">CN</span></span>                | <span data-ttu-id="742a1-112">Инициалы</span><span class="sxs-lookup"><span data-stu-id="742a1-112">Initials</span></span>                                    |
| <span data-ttu-id="742a1-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="742a1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="742a1-114">Initials</span><span class="sxs-lookup"><span data-stu-id="742a1-114">initials</span></span>                                    |
| <span data-ttu-id="742a1-115">Размер</span><span class="sxs-lookup"><span data-stu-id="742a1-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="742a1-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="742a1-116">Update Privilege</span></span>  | <span data-ttu-id="742a1-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="742a1-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="742a1-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="742a1-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="742a1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-119">Attribute-Id</span></span>      | <span data-ttu-id="742a1-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="742a1-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="742a1-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="742a1-121">System-Id-Guid</span></span>    | <span data-ttu-id="742a1-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="742a1-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="742a1-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="742a1-123">Syntax</span></span>            | [<span data-ttu-id="742a1-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="742a1-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="742a1-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="742a1-125">Implementations</span></span>

-   [<span data-ttu-id="742a1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="742a1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="742a1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="742a1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="742a1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="742a1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="742a1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="742a1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="742a1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="742a1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="742a1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="742a1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="742a1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="742a1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="742a1-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-133">Entry</span></span> | <span data-ttu-id="742a1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="742a1-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="742a1-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="742a1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-136">MAPI-Id</span></span>                | <span data-ttu-id="742a1-137">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="742a1-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="742a1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="742a1-138">System-Only</span></span>            | <span data-ttu-id="742a1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-139">False</span></span>                                                              |
| <span data-ttu-id="742a1-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="742a1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="742a1-141">True</span><span class="sxs-lookup"><span data-stu-id="742a1-141">True</span></span>                                                               |
| <span data-ttu-id="742a1-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="742a1-142">Is Indexed</span></span>             | <span data-ttu-id="742a1-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-143">False</span></span>                                                              |
| <span data-ttu-id="742a1-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="742a1-144">In Global Catalog</span></span>      | <span data-ttu-id="742a1-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-145">False</span></span>                                                              |
| <span data-ttu-id="742a1-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="742a1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="742a1-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="742a1-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="742a1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="742a1-148">Range-Lower</span></span>            | <span data-ttu-id="742a1-149">1</span><span class="sxs-lookup"><span data-stu-id="742a1-149">1</span></span>                                                                  |
| <span data-ttu-id="742a1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="742a1-150">Range-Upper</span></span>            | <span data-ttu-id="742a1-151">6</span><span class="sxs-lookup"><span data-stu-id="742a1-151">6</span></span>                                                                  |
| <span data-ttu-id="742a1-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-152">Search-Flags</span></span>           | <span data-ttu-id="742a1-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="742a1-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="742a1-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-154">System-Flags</span></span>           | <span data-ttu-id="742a1-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="742a1-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="742a1-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="742a1-156">Classes used in</span></span>        | [<span data-ttu-id="742a1-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="742a1-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="742a1-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="742a1-158">Windows Server 2003</span></span>



| <span data-ttu-id="742a1-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-159">Entry</span></span> | <span data-ttu-id="742a1-160">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742a1-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="742a1-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="742a1-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-162">MAPI-Id</span></span>                | <span data-ttu-id="742a1-163">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="742a1-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="742a1-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="742a1-164">System-Only</span></span>            | <span data-ttu-id="742a1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="742a1-166">Is-Single-Valued</span></span>       | <span data-ttu-id="742a1-167">True</span><span class="sxs-lookup"><span data-stu-id="742a1-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="742a1-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="742a1-168">Is Indexed</span></span>             | <span data-ttu-id="742a1-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="742a1-170">In Global Catalog</span></span>      | <span data-ttu-id="742a1-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="742a1-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="742a1-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="742a1-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="742a1-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="742a1-174">Range-Lower</span></span>            | <span data-ttu-id="742a1-175">1</span><span class="sxs-lookup"><span data-stu-id="742a1-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="742a1-176">Range-Upper</span></span>            | <span data-ttu-id="742a1-177">6</span><span class="sxs-lookup"><span data-stu-id="742a1-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-178">Search-Flags</span></span>           | <span data-ttu-id="742a1-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="742a1-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="742a1-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-180">System-Flags</span></span>           | <span data-ttu-id="742a1-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="742a1-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="742a1-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="742a1-182">Classes used in</span></span>        | [<span data-ttu-id="742a1-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="742a1-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="742a1-184">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="742a1-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="742a1-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="742a1-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="742a1-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-186">Entry</span></span> | <span data-ttu-id="742a1-187">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742a1-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="742a1-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="742a1-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-189">MAPI-Id</span></span>                | <span data-ttu-id="742a1-190">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="742a1-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="742a1-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="742a1-191">System-Only</span></span>            | <span data-ttu-id="742a1-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="742a1-193">Is-Single-Valued</span></span>       | <span data-ttu-id="742a1-194">True</span><span class="sxs-lookup"><span data-stu-id="742a1-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="742a1-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="742a1-195">Is Indexed</span></span>             | <span data-ttu-id="742a1-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="742a1-197">In Global Catalog</span></span>      | <span data-ttu-id="742a1-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="742a1-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="742a1-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="742a1-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="742a1-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="742a1-201">Range-Lower</span></span>            | <span data-ttu-id="742a1-202">1</span><span class="sxs-lookup"><span data-stu-id="742a1-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="742a1-203">Range-Upper</span></span>            | <span data-ttu-id="742a1-204">6</span><span class="sxs-lookup"><span data-stu-id="742a1-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-205">Search-Flags</span></span>           | <span data-ttu-id="742a1-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="742a1-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="742a1-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-207">System-Flags</span></span>           | <span data-ttu-id="742a1-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="742a1-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="742a1-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="742a1-209">Classes used in</span></span>        | [<span data-ttu-id="742a1-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="742a1-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="742a1-211">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="742a1-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="742a1-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="742a1-212">Windows Server 2008</span></span>



| <span data-ttu-id="742a1-213">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-213">Entry</span></span> | <span data-ttu-id="742a1-214">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742a1-215">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="742a1-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="742a1-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-216">MAPI-Id</span></span>                | <span data-ttu-id="742a1-217">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="742a1-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="742a1-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="742a1-218">System-Only</span></span>            | <span data-ttu-id="742a1-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-220">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="742a1-220">Is-Single-Valued</span></span>       | <span data-ttu-id="742a1-221">True</span><span class="sxs-lookup"><span data-stu-id="742a1-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="742a1-222">Индексируется</span><span class="sxs-lookup"><span data-stu-id="742a1-222">Is Indexed</span></span>             | <span data-ttu-id="742a1-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-224">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="742a1-224">In Global Catalog</span></span>      | <span data-ttu-id="742a1-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-226">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="742a1-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="742a1-227">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="742a1-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="742a1-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="742a1-228">Range-Lower</span></span>            | <span data-ttu-id="742a1-229">1</span><span class="sxs-lookup"><span data-stu-id="742a1-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="742a1-230">Range-Upper</span></span>            | <span data-ttu-id="742a1-231">6</span><span class="sxs-lookup"><span data-stu-id="742a1-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-232">Search-Flags</span></span>           | <span data-ttu-id="742a1-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="742a1-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="742a1-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-234">System-Flags</span></span>           | <span data-ttu-id="742a1-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="742a1-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="742a1-236">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="742a1-236">Classes used in</span></span>        | [<span data-ttu-id="742a1-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="742a1-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="742a1-238">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="742a1-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="742a1-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="742a1-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="742a1-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-240">Entry</span></span> | <span data-ttu-id="742a1-241">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742a1-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="742a1-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="742a1-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-243">MAPI-Id</span></span>                | <span data-ttu-id="742a1-244">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="742a1-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="742a1-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="742a1-245">System-Only</span></span>            | <span data-ttu-id="742a1-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-247">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="742a1-247">Is-Single-Valued</span></span>       | <span data-ttu-id="742a1-248">True</span><span class="sxs-lookup"><span data-stu-id="742a1-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="742a1-249">Индексируется</span><span class="sxs-lookup"><span data-stu-id="742a1-249">Is Indexed</span></span>             | <span data-ttu-id="742a1-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-251">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="742a1-251">In Global Catalog</span></span>      | <span data-ttu-id="742a1-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-253">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="742a1-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="742a1-254">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="742a1-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="742a1-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="742a1-255">Range-Lower</span></span>            | <span data-ttu-id="742a1-256">1</span><span class="sxs-lookup"><span data-stu-id="742a1-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="742a1-257">Range-Upper</span></span>            | <span data-ttu-id="742a1-258">6</span><span class="sxs-lookup"><span data-stu-id="742a1-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-259">Search-Flags</span></span>           | <span data-ttu-id="742a1-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="742a1-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="742a1-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-261">System-Flags</span></span>           | <span data-ttu-id="742a1-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="742a1-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="742a1-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="742a1-263">Classes used in</span></span>        | [<span data-ttu-id="742a1-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="742a1-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="742a1-265">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="742a1-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="742a1-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="742a1-266">Windows Server 2012</span></span>



| <span data-ttu-id="742a1-267">Ввод</span><span class="sxs-lookup"><span data-stu-id="742a1-267">Entry</span></span> | <span data-ttu-id="742a1-268">Значение</span><span class="sxs-lookup"><span data-stu-id="742a1-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742a1-269">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="742a1-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="742a1-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="742a1-270">MAPI-Id</span></span>                | <span data-ttu-id="742a1-271">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="742a1-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="742a1-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="742a1-272">System-Only</span></span>            | <span data-ttu-id="742a1-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-274">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="742a1-274">Is-Single-Valued</span></span>       | <span data-ttu-id="742a1-275">True</span><span class="sxs-lookup"><span data-stu-id="742a1-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="742a1-276">Индексируется</span><span class="sxs-lookup"><span data-stu-id="742a1-276">Is Indexed</span></span>             | <span data-ttu-id="742a1-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-278">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="742a1-278">In Global Catalog</span></span>      | <span data-ttu-id="742a1-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="742a1-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="742a1-280">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="742a1-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="742a1-281">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="742a1-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="742a1-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="742a1-282">Range-Lower</span></span>            | <span data-ttu-id="742a1-283">1</span><span class="sxs-lookup"><span data-stu-id="742a1-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="742a1-284">Range-Upper</span></span>            | <span data-ttu-id="742a1-285">6</span><span class="sxs-lookup"><span data-stu-id="742a1-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="742a1-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-286">Search-Flags</span></span>           | <span data-ttu-id="742a1-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="742a1-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="742a1-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="742a1-288">System-Flags</span></span>           | <span data-ttu-id="742a1-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="742a1-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="742a1-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="742a1-290">Classes used in</span></span>        | [<span data-ttu-id="742a1-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="742a1-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="742a1-292">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="742a1-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





