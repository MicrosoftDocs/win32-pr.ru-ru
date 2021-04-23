---
title: Атрибут Manager
description: Содержит различающееся имя пользователя, который является руководителем пользователя. Объект-пользователь руководителя содержит свойство directReports, содержащее ссылки на все объекты user, для свойств диспетчера которых задано это различающееся имя.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута диспетчера
- Схема AD атрибута диспетчера
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416285"
---
# <a name="manager-attribute"></a><span data-ttu-id="a2927-106">Атрибут Manager</span><span class="sxs-lookup"><span data-stu-id="a2927-106">Manager attribute</span></span>

<span data-ttu-id="a2927-107">Содержит различающееся имя пользователя, который является руководителем пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2927-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="a2927-108">Объект-пользователь руководителя содержит свойство directReports, содержащее ссылки на все объекты user, для свойств диспетчера которых задано это различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="a2927-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="a2927-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-109">Entry</span></span> | <span data-ttu-id="a2927-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a2927-111">CN</span><span class="sxs-lookup"><span data-stu-id="a2927-111">CN</span></span>                | <span data-ttu-id="a2927-112">Manager</span><span class="sxs-lookup"><span data-stu-id="a2927-112">Manager</span></span>                                                                     |
| <span data-ttu-id="a2927-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a2927-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a2927-114">manager</span><span class="sxs-lookup"><span data-stu-id="a2927-114">manager</span></span>                                                                     |
| <span data-ttu-id="a2927-115">Размер</span><span class="sxs-lookup"><span data-stu-id="a2927-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="a2927-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a2927-116">Update Privilege</span></span>  | <span data-ttu-id="a2927-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a2927-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="a2927-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a2927-118">Update Frequency</span></span>  | <span data-ttu-id="a2927-119">При создании записи пользователя и при необходимости изменения руководителя.</span><span class="sxs-lookup"><span data-stu-id="a2927-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="a2927-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-120">Attribute-Id</span></span>      | <span data-ttu-id="a2927-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="a2927-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="a2927-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a2927-122">System-Id-Guid</span></span>    | <span data-ttu-id="a2927-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a2927-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="a2927-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2927-124">Syntax</span></span>            | [<span data-ttu-id="a2927-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a2927-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="a2927-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a2927-126">Implementations</span></span>

-   [<span data-ttu-id="a2927-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2927-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2927-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2927-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2927-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2927-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2927-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2927-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2927-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2927-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2927-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2927-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2927-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2927-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a2927-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-134">Entry</span></span> | <span data-ttu-id="a2927-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a2927-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2927-136">Link-Id</span></span>                | <span data-ttu-id="a2927-137">42</span><span class="sxs-lookup"><span data-stu-id="a2927-137">42</span></span>                                                                 |
| <span data-ttu-id="a2927-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-138">MAPI-Id</span></span>                | <span data-ttu-id="a2927-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="a2927-139">0x8005</span></span>                                                             |
| <span data-ttu-id="a2927-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2927-140">System-Only</span></span>            | <span data-ttu-id="a2927-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-141">False</span></span>                                                              |
| <span data-ttu-id="a2927-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2927-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a2927-143">True</span><span class="sxs-lookup"><span data-stu-id="a2927-143">True</span></span>                                                               |
| <span data-ttu-id="a2927-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2927-144">Is Indexed</span></span>             | <span data-ttu-id="a2927-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-145">False</span></span>                                                              |
| <span data-ttu-id="a2927-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2927-146">In Global Catalog</span></span>      | <span data-ttu-id="a2927-147">True</span><span class="sxs-lookup"><span data-stu-id="a2927-147">True</span></span>                                                               |
| <span data-ttu-id="a2927-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2927-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2927-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2927-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a2927-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2927-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a2927-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2927-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a2927-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-152">Search-Flags</span></span>           | <span data-ttu-id="a2927-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="a2927-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-154">System-Flags</span></span>           | <span data-ttu-id="a2927-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="a2927-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2927-156">Classes used in</span></span>        | [<span data-ttu-id="a2927-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a2927-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2927-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2927-158">Windows Server 2003</span></span>



| <span data-ttu-id="a2927-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-159">Entry</span></span> | <span data-ttu-id="a2927-160">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2927-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2927-161">Link-Id</span></span>                | <span data-ttu-id="a2927-162">42</span><span class="sxs-lookup"><span data-stu-id="a2927-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="a2927-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-163">MAPI-Id</span></span>                | <span data-ttu-id="a2927-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="a2927-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="a2927-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2927-165">System-Only</span></span>            | <span data-ttu-id="a2927-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2927-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a2927-168">True</span><span class="sxs-lookup"><span data-stu-id="a2927-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2927-169">Is Indexed</span></span>             | <span data-ttu-id="a2927-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2927-171">In Global Catalog</span></span>      | <span data-ttu-id="a2927-172">True</span><span class="sxs-lookup"><span data-stu-id="a2927-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2927-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2927-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2927-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a2927-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2927-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2927-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-177">Search-Flags</span></span>           | <span data-ttu-id="a2927-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-179">System-Flags</span></span>           | <span data-ttu-id="a2927-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2927-181">Classes used in</span></span>        | [<span data-ttu-id="a2927-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a2927-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="a2927-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a2927-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2927-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2927-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2927-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-185">Entry</span></span> | <span data-ttu-id="a2927-186">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2927-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2927-187">Link-Id</span></span>                | <span data-ttu-id="a2927-188">42</span><span class="sxs-lookup"><span data-stu-id="a2927-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="a2927-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-189">MAPI-Id</span></span>                | <span data-ttu-id="a2927-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="a2927-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="a2927-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2927-191">System-Only</span></span>            | <span data-ttu-id="a2927-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2927-193">Is-Single-Valued</span></span>       | <span data-ttu-id="a2927-194">True</span><span class="sxs-lookup"><span data-stu-id="a2927-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2927-195">Is Indexed</span></span>             | <span data-ttu-id="a2927-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2927-197">In Global Catalog</span></span>      | <span data-ttu-id="a2927-198">True</span><span class="sxs-lookup"><span data-stu-id="a2927-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2927-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2927-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2927-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a2927-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2927-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2927-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-203">Search-Flags</span></span>           | <span data-ttu-id="a2927-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-205">System-Flags</span></span>           | <span data-ttu-id="a2927-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2927-207">Classes used in</span></span>        | [<span data-ttu-id="a2927-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a2927-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="a2927-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a2927-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2927-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2927-210">Windows Server 2008</span></span>



| <span data-ttu-id="a2927-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-211">Entry</span></span> | <span data-ttu-id="a2927-212">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2927-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2927-213">Link-Id</span></span>                | <span data-ttu-id="a2927-214">42</span><span class="sxs-lookup"><span data-stu-id="a2927-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="a2927-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-215">MAPI-Id</span></span>                | <span data-ttu-id="a2927-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="a2927-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="a2927-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2927-217">System-Only</span></span>            | <span data-ttu-id="a2927-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2927-219">Is-Single-Valued</span></span>       | <span data-ttu-id="a2927-220">True</span><span class="sxs-lookup"><span data-stu-id="a2927-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2927-221">Is Indexed</span></span>             | <span data-ttu-id="a2927-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2927-223">In Global Catalog</span></span>      | <span data-ttu-id="a2927-224">True</span><span class="sxs-lookup"><span data-stu-id="a2927-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2927-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2927-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2927-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a2927-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2927-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2927-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-229">Search-Flags</span></span>           | <span data-ttu-id="a2927-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-231">System-Flags</span></span>           | <span data-ttu-id="a2927-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2927-233">Classes used in</span></span>        | [<span data-ttu-id="a2927-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a2927-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="a2927-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a2927-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2927-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2927-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2927-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-237">Entry</span></span> | <span data-ttu-id="a2927-238">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2927-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2927-239">Link-Id</span></span>                | <span data-ttu-id="a2927-240">42</span><span class="sxs-lookup"><span data-stu-id="a2927-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="a2927-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-241">MAPI-Id</span></span>                | <span data-ttu-id="a2927-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="a2927-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="a2927-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2927-243">System-Only</span></span>            | <span data-ttu-id="a2927-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2927-245">Is-Single-Valued</span></span>       | <span data-ttu-id="a2927-246">True</span><span class="sxs-lookup"><span data-stu-id="a2927-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2927-247">Is Indexed</span></span>             | <span data-ttu-id="a2927-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2927-249">In Global Catalog</span></span>      | <span data-ttu-id="a2927-250">True</span><span class="sxs-lookup"><span data-stu-id="a2927-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2927-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2927-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2927-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a2927-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2927-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2927-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-255">Search-Flags</span></span>           | <span data-ttu-id="a2927-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-257">System-Flags</span></span>           | <span data-ttu-id="a2927-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2927-259">Classes used in</span></span>        | [<span data-ttu-id="a2927-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a2927-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="a2927-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a2927-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2927-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2927-262">Windows Server 2012</span></span>



| <span data-ttu-id="a2927-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="a2927-263">Entry</span></span> | <span data-ttu-id="a2927-264">Значение</span><span class="sxs-lookup"><span data-stu-id="a2927-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2927-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a2927-265">Link-Id</span></span>                | <span data-ttu-id="a2927-266">42</span><span class="sxs-lookup"><span data-stu-id="a2927-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="a2927-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2927-267">MAPI-Id</span></span>                | <span data-ttu-id="a2927-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="a2927-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="a2927-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2927-269">System-Only</span></span>            | <span data-ttu-id="a2927-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-271">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a2927-271">Is-Single-Valued</span></span>       | <span data-ttu-id="a2927-272">True</span><span class="sxs-lookup"><span data-stu-id="a2927-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-273">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a2927-273">Is Indexed</span></span>             | <span data-ttu-id="a2927-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="a2927-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="a2927-275">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a2927-275">In Global Catalog</span></span>      | <span data-ttu-id="a2927-276">True</span><span class="sxs-lookup"><span data-stu-id="a2927-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="a2927-277">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a2927-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2927-278">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2927-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a2927-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2927-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2927-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="a2927-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-281">Search-Flags</span></span>           | <span data-ttu-id="a2927-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2927-283">System-Flags</span></span>           | <span data-ttu-id="a2927-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2927-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a2927-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a2927-285">Classes used in</span></span>        | [<span data-ttu-id="a2927-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a2927-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="a2927-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a2927-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





