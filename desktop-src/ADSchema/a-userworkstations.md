---
title: Атрибут User-Workstations
description: Содержит имена NetBIOS или DNS компьютеров под управлением Windows NT Workstation или Windows 2000 Professional, с которых пользователь может войти в систему.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута User-Workstations
- Схема AD атрибута Усерворкстатионс
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893242"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="6cd2b-105">Атрибут User-Workstations</span><span class="sxs-lookup"><span data-stu-id="6cd2b-105">User-Workstations attribute</span></span>

<span data-ttu-id="6cd2b-106">Содержит имена NetBIOS или DNS компьютеров под управлением Windows NT Workstation или Windows 2000 Professional, с которых пользователь может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="6cd2b-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="6cd2b-107">Каждое NetBIOS-имя разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="6cd2b-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="6cd2b-108">Несколько имен следует разделять запятыми.</span><span class="sxs-lookup"><span data-stu-id="6cd2b-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="6cd2b-109">Этот пользовательский атрибут больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="6cd2b-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="6cd2b-110">Чтобы управлять тем, какие учетные записи могут входить в систему на каких рабочих станциях, рекомендуется использовать параметр "локальный вход в систему" и "Запретить локальный вход в систему" или "разрешить вход в систему с помощью службы удаленных рабочих столов" и "запретить вход через службы удаленных рабочих столов".</span><span class="sxs-lookup"><span data-stu-id="6cd2b-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="6cd2b-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-111">Entry</span></span> | <span data-ttu-id="6cd2b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd2b-113">CN</span><span class="sxs-lookup"><span data-stu-id="6cd2b-113">CN</span></span>                | <span data-ttu-id="6cd2b-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="6cd2b-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="6cd2b-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6cd2b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="6cd2b-116">усерворкстатионс</span><span class="sxs-lookup"><span data-stu-id="6cd2b-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="6cd2b-117">Размер</span><span class="sxs-lookup"><span data-stu-id="6cd2b-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="6cd2b-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6cd2b-118">Update Privilege</span></span>  | <span data-ttu-id="6cd2b-119">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6cd2b-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="6cd2b-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6cd2b-120">Update Frequency</span></span>  | <span data-ttu-id="6cd2b-121">Когда пользовательская запись создается и каждый раз при необходимости изменения прав входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="6cd2b-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="6cd2b-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-122">Attribute-Id</span></span>      | <span data-ttu-id="6cd2b-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="6cd2b-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="6cd2b-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6cd2b-124">System-Id-Guid</span></span>    | <span data-ttu-id="6cd2b-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6cd2b-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="6cd2b-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cd2b-126">Syntax</span></span>            | [<span data-ttu-id="6cd2b-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="6cd2b-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6cd2b-128">Implementations</span></span>

-   [<span data-ttu-id="6cd2b-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6cd2b-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6cd2b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6cd2b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6cd2b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6cd2b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6cd2b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6cd2b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6cd2b-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-136">Entry</span></span> | <span data-ttu-id="6cd2b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6cd2b-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6cd2b-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cd2b-140">System-Only</span></span>            | <span data-ttu-id="6cd2b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-141">False</span></span>                             |
| <span data-ttu-id="6cd2b-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6cd2b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6cd2b-143">True</span><span class="sxs-lookup"><span data-stu-id="6cd2b-143">True</span></span>                              |
| <span data-ttu-id="6cd2b-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6cd2b-144">Is Indexed</span></span>             | <span data-ttu-id="6cd2b-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-145">False</span></span>                             |
| <span data-ttu-id="6cd2b-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6cd2b-146">In Global Catalog</span></span>      | <span data-ttu-id="6cd2b-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-147">False</span></span>                             |
| <span data-ttu-id="6cd2b-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6cd2b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cd2b-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6cd2b-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6cd2b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cd2b-150">Range-Lower</span></span>            | <span data-ttu-id="6cd2b-151">0</span><span class="sxs-lookup"><span data-stu-id="6cd2b-151">0</span></span>                                 |
| <span data-ttu-id="6cd2b-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cd2b-152">Range-Upper</span></span>            | <span data-ttu-id="6cd2b-153">1024</span><span class="sxs-lookup"><span data-stu-id="6cd2b-153">1024</span></span>                              |
| <span data-ttu-id="6cd2b-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-154">Search-Flags</span></span>           | <span data-ttu-id="6cd2b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-155">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-156">System-Flags</span></span>           | <span data-ttu-id="6cd2b-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-157">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6cd2b-158">Classes used in</span></span>        | [<span data-ttu-id="6cd2b-159">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6cd2b-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6cd2b-160">Windows Server 2003</span></span>



| <span data-ttu-id="6cd2b-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-161">Entry</span></span> | <span data-ttu-id="6cd2b-162">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6cd2b-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6cd2b-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cd2b-165">System-Only</span></span>            | <span data-ttu-id="6cd2b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-166">False</span></span>                             |
| <span data-ttu-id="6cd2b-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6cd2b-167">Is-Single-Valued</span></span>       | <span data-ttu-id="6cd2b-168">True</span><span class="sxs-lookup"><span data-stu-id="6cd2b-168">True</span></span>                              |
| <span data-ttu-id="6cd2b-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6cd2b-169">Is Indexed</span></span>             | <span data-ttu-id="6cd2b-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-170">False</span></span>                             |
| <span data-ttu-id="6cd2b-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6cd2b-171">In Global Catalog</span></span>      | <span data-ttu-id="6cd2b-172">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-172">False</span></span>                             |
| <span data-ttu-id="6cd2b-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6cd2b-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cd2b-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6cd2b-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6cd2b-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cd2b-175">Range-Lower</span></span>            | <span data-ttu-id="6cd2b-176">0</span><span class="sxs-lookup"><span data-stu-id="6cd2b-176">0</span></span>                                 |
| <span data-ttu-id="6cd2b-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cd2b-177">Range-Upper</span></span>            | <span data-ttu-id="6cd2b-178">1024</span><span class="sxs-lookup"><span data-stu-id="6cd2b-178">1024</span></span>                              |
| <span data-ttu-id="6cd2b-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-179">Search-Flags</span></span>           | <span data-ttu-id="6cd2b-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-180">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-181">System-Flags</span></span>           | <span data-ttu-id="6cd2b-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-182">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-183">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6cd2b-183">Classes used in</span></span>        | [<span data-ttu-id="6cd2b-184">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6cd2b-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6cd2b-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6cd2b-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-186">Entry</span></span> | <span data-ttu-id="6cd2b-187">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6cd2b-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6cd2b-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cd2b-190">System-Only</span></span>            | <span data-ttu-id="6cd2b-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-191">False</span></span>                             |
| <span data-ttu-id="6cd2b-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6cd2b-192">Is-Single-Valued</span></span>       | <span data-ttu-id="6cd2b-193">True</span><span class="sxs-lookup"><span data-stu-id="6cd2b-193">True</span></span>                              |
| <span data-ttu-id="6cd2b-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6cd2b-194">Is Indexed</span></span>             | <span data-ttu-id="6cd2b-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-195">False</span></span>                             |
| <span data-ttu-id="6cd2b-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6cd2b-196">In Global Catalog</span></span>      | <span data-ttu-id="6cd2b-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-197">False</span></span>                             |
| <span data-ttu-id="6cd2b-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6cd2b-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cd2b-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6cd2b-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6cd2b-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cd2b-200">Range-Lower</span></span>            | <span data-ttu-id="6cd2b-201">0</span><span class="sxs-lookup"><span data-stu-id="6cd2b-201">0</span></span>                                 |
| <span data-ttu-id="6cd2b-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cd2b-202">Range-Upper</span></span>            | <span data-ttu-id="6cd2b-203">1024</span><span class="sxs-lookup"><span data-stu-id="6cd2b-203">1024</span></span>                              |
| <span data-ttu-id="6cd2b-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-204">Search-Flags</span></span>           | <span data-ttu-id="6cd2b-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-205">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-206">System-Flags</span></span>           | <span data-ttu-id="6cd2b-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-207">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6cd2b-208">Classes used in</span></span>        | [<span data-ttu-id="6cd2b-209">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6cd2b-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cd2b-210">Windows Server 2008</span></span>



| <span data-ttu-id="6cd2b-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-211">Entry</span></span> | <span data-ttu-id="6cd2b-212">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6cd2b-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6cd2b-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cd2b-215">System-Only</span></span>            | <span data-ttu-id="6cd2b-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-216">False</span></span>                             |
| <span data-ttu-id="6cd2b-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6cd2b-217">Is-Single-Valued</span></span>       | <span data-ttu-id="6cd2b-218">True</span><span class="sxs-lookup"><span data-stu-id="6cd2b-218">True</span></span>                              |
| <span data-ttu-id="6cd2b-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6cd2b-219">Is Indexed</span></span>             | <span data-ttu-id="6cd2b-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-220">False</span></span>                             |
| <span data-ttu-id="6cd2b-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6cd2b-221">In Global Catalog</span></span>      | <span data-ttu-id="6cd2b-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-222">False</span></span>                             |
| <span data-ttu-id="6cd2b-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6cd2b-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cd2b-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6cd2b-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6cd2b-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cd2b-225">Range-Lower</span></span>            | <span data-ttu-id="6cd2b-226">0</span><span class="sxs-lookup"><span data-stu-id="6cd2b-226">0</span></span>                                 |
| <span data-ttu-id="6cd2b-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cd2b-227">Range-Upper</span></span>            | <span data-ttu-id="6cd2b-228">1024</span><span class="sxs-lookup"><span data-stu-id="6cd2b-228">1024</span></span>                              |
| <span data-ttu-id="6cd2b-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-229">Search-Flags</span></span>           | <span data-ttu-id="6cd2b-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-230">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-231">System-Flags</span></span>           | <span data-ttu-id="6cd2b-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-232">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6cd2b-233">Classes used in</span></span>        | [<span data-ttu-id="6cd2b-234">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6cd2b-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6cd2b-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6cd2b-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-236">Entry</span></span> | <span data-ttu-id="6cd2b-237">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6cd2b-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6cd2b-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cd2b-240">System-Only</span></span>            | <span data-ttu-id="6cd2b-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-241">False</span></span>                             |
| <span data-ttu-id="6cd2b-242">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6cd2b-242">Is-Single-Valued</span></span>       | <span data-ttu-id="6cd2b-243">True</span><span class="sxs-lookup"><span data-stu-id="6cd2b-243">True</span></span>                              |
| <span data-ttu-id="6cd2b-244">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6cd2b-244">Is Indexed</span></span>             | <span data-ttu-id="6cd2b-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-245">False</span></span>                             |
| <span data-ttu-id="6cd2b-246">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6cd2b-246">In Global Catalog</span></span>      | <span data-ttu-id="6cd2b-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-247">False</span></span>                             |
| <span data-ttu-id="6cd2b-248">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6cd2b-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cd2b-249">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6cd2b-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6cd2b-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cd2b-250">Range-Lower</span></span>            | <span data-ttu-id="6cd2b-251">0</span><span class="sxs-lookup"><span data-stu-id="6cd2b-251">0</span></span>                                 |
| <span data-ttu-id="6cd2b-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cd2b-252">Range-Upper</span></span>            | <span data-ttu-id="6cd2b-253">1024</span><span class="sxs-lookup"><span data-stu-id="6cd2b-253">1024</span></span>                              |
| <span data-ttu-id="6cd2b-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-254">Search-Flags</span></span>           | <span data-ttu-id="6cd2b-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-255">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-256">System-Flags</span></span>           | <span data-ttu-id="6cd2b-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-257">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-258">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6cd2b-258">Classes used in</span></span>        | [<span data-ttu-id="6cd2b-259">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6cd2b-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cd2b-260">Windows Server 2012</span></span>



| <span data-ttu-id="6cd2b-261">Ввод</span><span class="sxs-lookup"><span data-stu-id="6cd2b-261">Entry</span></span> | <span data-ttu-id="6cd2b-262">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd2b-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6cd2b-263">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6cd2b-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cd2b-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6cd2b-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cd2b-265">System-Only</span></span>            | <span data-ttu-id="6cd2b-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-266">False</span></span>                             |
| <span data-ttu-id="6cd2b-267">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6cd2b-267">Is-Single-Valued</span></span>       | <span data-ttu-id="6cd2b-268">True</span><span class="sxs-lookup"><span data-stu-id="6cd2b-268">True</span></span>                              |
| <span data-ttu-id="6cd2b-269">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6cd2b-269">Is Indexed</span></span>             | <span data-ttu-id="6cd2b-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-270">False</span></span>                             |
| <span data-ttu-id="6cd2b-271">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6cd2b-271">In Global Catalog</span></span>      | <span data-ttu-id="6cd2b-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="6cd2b-272">False</span></span>                             |
| <span data-ttu-id="6cd2b-273">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6cd2b-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cd2b-274">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6cd2b-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6cd2b-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cd2b-275">Range-Lower</span></span>            | <span data-ttu-id="6cd2b-276">0</span><span class="sxs-lookup"><span data-stu-id="6cd2b-276">0</span></span>                                 |
| <span data-ttu-id="6cd2b-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cd2b-277">Range-Upper</span></span>            | <span data-ttu-id="6cd2b-278">1024</span><span class="sxs-lookup"><span data-stu-id="6cd2b-278">1024</span></span>                              |
| <span data-ttu-id="6cd2b-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-279">Search-Flags</span></span>           | <span data-ttu-id="6cd2b-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-280">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cd2b-281">System-Flags</span></span>           | <span data-ttu-id="6cd2b-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cd2b-282">0x00000010</span></span>                        |
| <span data-ttu-id="6cd2b-283">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6cd2b-283">Classes used in</span></span>        | [<span data-ttu-id="6cd2b-284">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="6cd2b-284">**User**</span></span>](c-user.md)<br/> |



 

 





