---
title: Атрибут Server-Reference
description: Найдено в объекте компьютера сайта. Содержит различающееся имя контроллера домена в контексте именования домена.
ms.assetid: 6c0ebe85-b4ed-4284-ad96-0b711d5acce7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Server-Reference
- Схема AD атрибута Серверреференце
topic_type:
- apiref
api_name:
- Server-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83fed3b44feeaccb87cb1f55435bbac915c1c262
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893657"
---
# <a name="server-reference-attribute"></a><span data-ttu-id="80cf7-106">Атрибут Server-Reference</span><span class="sxs-lookup"><span data-stu-id="80cf7-106">Server-Reference attribute</span></span>

<span data-ttu-id="80cf7-107">Найдено в объекте компьютера сайта.</span><span class="sxs-lookup"><span data-stu-id="80cf7-107">Found in a site computer object.</span></span> <span data-ttu-id="80cf7-108">Содержит различающееся имя контроллера домена в контексте именования домена.</span><span class="sxs-lookup"><span data-stu-id="80cf7-108">Contains the distinguished name of the domain controller in the domain naming context.</span></span>



| <span data-ttu-id="80cf7-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-109">Entry</span></span> | <span data-ttu-id="80cf7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="80cf7-111">CN</span><span class="sxs-lookup"><span data-stu-id="80cf7-111">CN</span></span>                | <span data-ttu-id="80cf7-112">Server-Reference</span><span class="sxs-lookup"><span data-stu-id="80cf7-112">Server-Reference</span></span>                        |
| <span data-ttu-id="80cf7-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="80cf7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="80cf7-114">серверреференце</span><span class="sxs-lookup"><span data-stu-id="80cf7-114">serverReference</span></span>                         |
| <span data-ttu-id="80cf7-115">Размер</span><span class="sxs-lookup"><span data-stu-id="80cf7-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="80cf7-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="80cf7-116">Update Privilege</span></span>  | <span data-ttu-id="80cf7-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="80cf7-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="80cf7-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="80cf7-118">Update Frequency</span></span>  | <span data-ttu-id="80cf7-119">При создании сайта.</span><span class="sxs-lookup"><span data-stu-id="80cf7-119">Whenever a site is created.</span></span>             |
| <span data-ttu-id="80cf7-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-120">Attribute-Id</span></span>      | <span data-ttu-id="80cf7-121">1.2.840.113556.1.4.515</span><span class="sxs-lookup"><span data-stu-id="80cf7-121">1.2.840.113556.1.4.515</span></span>                  |
| <span data-ttu-id="80cf7-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="80cf7-122">System-Id-Guid</span></span>    | <span data-ttu-id="80cf7-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="80cf7-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="80cf7-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80cf7-124">Syntax</span></span>            | [<span data-ttu-id="80cf7-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="80cf7-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="80cf7-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="80cf7-126">Implementations</span></span>

-   [<span data-ttu-id="80cf7-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80cf7-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80cf7-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80cf7-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80cf7-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="80cf7-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="80cf7-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80cf7-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80cf7-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80cf7-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80cf7-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80cf7-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80cf7-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80cf7-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80cf7-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80cf7-134">Windows 2000 Server</span></span>



| <span data-ttu-id="80cf7-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-135">Entry</span></span> | <span data-ttu-id="80cf7-136">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-137">Link-Id</span></span>                | <span data-ttu-id="80cf7-138">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-138">94</span></span>                                                                                                                              |
| <span data-ttu-id="80cf7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-139">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="80cf7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-140">System-Only</span></span>            | <span data-ttu-id="80cf7-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-141">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-143">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-143">True</span></span>                                                                                                                            |
| <span data-ttu-id="80cf7-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-144">Is Indexed</span></span>             | <span data-ttu-id="80cf7-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-145">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-146">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-147">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-149">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="80cf7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-150">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-151">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-152">Search-Flags</span></span>           | <span data-ttu-id="80cf7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-153">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-154">System-Flags</span></span>           | <span data-ttu-id="80cf7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-155">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-156">Classes used in</span></span>        | [<span data-ttu-id="80cf7-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-158">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="80cf7-158">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="80cf7-159">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-159">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80cf7-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80cf7-160">Windows Server 2003</span></span>



| <span data-ttu-id="80cf7-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-161">Entry</span></span> | <span data-ttu-id="80cf7-162">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-162">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-163">Link-Id</span></span>                | <span data-ttu-id="80cf7-164">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-164">94</span></span>                                                                                                                              |
| <span data-ttu-id="80cf7-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-165">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="80cf7-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-166">System-Only</span></span>            | <span data-ttu-id="80cf7-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-167">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-168">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-169">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-169">True</span></span>                                                                                                                            |
| <span data-ttu-id="80cf7-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-170">Is Indexed</span></span>             | <span data-ttu-id="80cf7-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-172">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-173">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-175">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="80cf7-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-176">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-177">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-178">Search-Flags</span></span>           | <span data-ttu-id="80cf7-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-179">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-180">System-Flags</span></span>           | <span data-ttu-id="80cf7-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-181">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-182">Classes used in</span></span>        | [<span data-ttu-id="80cf7-183">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-183">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-184">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="80cf7-184">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="80cf7-185">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-185">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="80cf7-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="80cf7-186">ADAM</span></span>



| <span data-ttu-id="80cf7-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-187">Entry</span></span> | <span data-ttu-id="80cf7-188">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-188">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-189">Link-Id</span></span>                | <span data-ttu-id="80cf7-190">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-190">94</span></span>                                                                             |
| <span data-ttu-id="80cf7-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-191">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="80cf7-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-192">System-Only</span></span>            | <span data-ttu-id="80cf7-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-193">False</span></span>                                                                          |
| <span data-ttu-id="80cf7-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-194">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-195">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-195">True</span></span>                                                                           |
| <span data-ttu-id="80cf7-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-196">Is Indexed</span></span>             | <span data-ttu-id="80cf7-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-197">False</span></span>                                                                          |
| <span data-ttu-id="80cf7-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-198">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-199">False</span></span>                                                                          |
| <span data-ttu-id="80cf7-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-201">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="80cf7-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-202">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="80cf7-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-203">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="80cf7-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-204">Search-Flags</span></span>           | <span data-ttu-id="80cf7-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-205">0x00000000</span></span>                                                                     |
| <span data-ttu-id="80cf7-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-206">System-Flags</span></span>           | <span data-ttu-id="80cf7-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-207">0x00000010</span></span>                                                                     |
| <span data-ttu-id="80cf7-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-208">Classes used in</span></span>        | [<span data-ttu-id="80cf7-209">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-209">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-210">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-210">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80cf7-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80cf7-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80cf7-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-212">Entry</span></span> | <span data-ttu-id="80cf7-213">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-213">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-214">Link-Id</span></span>                | <span data-ttu-id="80cf7-215">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-215">94</span></span>                                                                                                                              |
| <span data-ttu-id="80cf7-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-216">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="80cf7-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-217">System-Only</span></span>            | <span data-ttu-id="80cf7-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-218">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-219">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-220">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-220">True</span></span>                                                                                                                            |
| <span data-ttu-id="80cf7-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-221">Is Indexed</span></span>             | <span data-ttu-id="80cf7-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-222">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-223">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-224">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-226">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="80cf7-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-227">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-228">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-229">Search-Flags</span></span>           | <span data-ttu-id="80cf7-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-230">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-231">System-Flags</span></span>           | <span data-ttu-id="80cf7-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-232">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-233">Classes used in</span></span>        | [<span data-ttu-id="80cf7-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-235">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="80cf7-235">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="80cf7-236">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-236">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80cf7-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80cf7-237">Windows Server 2008</span></span>



| <span data-ttu-id="80cf7-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-238">Entry</span></span> | <span data-ttu-id="80cf7-239">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-240">Link-Id</span></span>                | <span data-ttu-id="80cf7-241">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-241">94</span></span>                                                                                                                              |
| <span data-ttu-id="80cf7-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-242">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="80cf7-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-243">System-Only</span></span>            | <span data-ttu-id="80cf7-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-244">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-245">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-246">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-246">True</span></span>                                                                                                                            |
| <span data-ttu-id="80cf7-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-247">Is Indexed</span></span>             | <span data-ttu-id="80cf7-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-248">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-249">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-250">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-252">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="80cf7-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-253">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-254">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-255">Search-Flags</span></span>           | <span data-ttu-id="80cf7-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-256">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-257">System-Flags</span></span>           | <span data-ttu-id="80cf7-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-258">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-259">Classes used in</span></span>        | [<span data-ttu-id="80cf7-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-261">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="80cf7-261">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="80cf7-262">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-262">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80cf7-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80cf7-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80cf7-264">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-264">Entry</span></span> | <span data-ttu-id="80cf7-265">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-265">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-266">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-266">Link-Id</span></span>                | <span data-ttu-id="80cf7-267">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-267">94</span></span>                                                                                                                              |
| <span data-ttu-id="80cf7-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-268">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="80cf7-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-269">System-Only</span></span>            | <span data-ttu-id="80cf7-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-270">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-271">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-271">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-272">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-272">True</span></span>                                                                                                                            |
| <span data-ttu-id="80cf7-273">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-273">Is Indexed</span></span>             | <span data-ttu-id="80cf7-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-274">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-275">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-275">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-276">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-277">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-278">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-278">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="80cf7-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-279">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-280">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-281">Search-Flags</span></span>           | <span data-ttu-id="80cf7-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-282">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-283">System-Flags</span></span>           | <span data-ttu-id="80cf7-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-284">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-285">Classes used in</span></span>        | [<span data-ttu-id="80cf7-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-287">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="80cf7-287">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="80cf7-288">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-288">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80cf7-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80cf7-289">Windows Server 2012</span></span>



| <span data-ttu-id="80cf7-290">Ввод</span><span class="sxs-lookup"><span data-stu-id="80cf7-290">Entry</span></span> | <span data-ttu-id="80cf7-291">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf7-291">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf7-292">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80cf7-292">Link-Id</span></span>                | <span data-ttu-id="80cf7-293">94</span><span class="sxs-lookup"><span data-stu-id="80cf7-293">94</span></span>                                                                                                                              |
| <span data-ttu-id="80cf7-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80cf7-294">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="80cf7-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="80cf7-295">System-Only</span></span>            | <span data-ttu-id="80cf7-296">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-296">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-297">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80cf7-297">Is-Single-Valued</span></span>       | <span data-ttu-id="80cf7-298">True</span><span class="sxs-lookup"><span data-stu-id="80cf7-298">True</span></span>                                                                                                                            |
| <span data-ttu-id="80cf7-299">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80cf7-299">Is Indexed</span></span>             | <span data-ttu-id="80cf7-300">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-300">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-301">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80cf7-301">In Global Catalog</span></span>      | <span data-ttu-id="80cf7-302">Неверно</span><span class="sxs-lookup"><span data-stu-id="80cf7-302">False</span></span>                                                                                                                           |
| <span data-ttu-id="80cf7-303">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80cf7-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="80cf7-304">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80cf7-304">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="80cf7-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80cf7-305">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80cf7-306">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="80cf7-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-307">Search-Flags</span></span>           | <span data-ttu-id="80cf7-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80cf7-308">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80cf7-309">System-Flags</span></span>           | <span data-ttu-id="80cf7-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80cf7-310">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="80cf7-311">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80cf7-311">Classes used in</span></span>        | [<span data-ttu-id="80cf7-312">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="80cf7-312">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="80cf7-313">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="80cf7-313">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="80cf7-314">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="80cf7-314">**Server**</span></span>](c-server.md)<br/> |



 

 





