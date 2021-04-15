---
title: Атрибут периода сборки мусора-Coll
description: Этот атрибут расположен в службе каталогов CN, CN Windows NT, CN Services, CN Configuration,... объектами. Он представляет время (в часах) между запуском сборки мусора DS.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута периода с мусором-Coll
- Схема AD атрибута Гарбажеколлпериод
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654835"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="1dcb5-106">Атрибут периода сборки мусора-Coll</span><span class="sxs-lookup"><span data-stu-id="1dcb5-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="1dcb5-107">Этот атрибут находится в общем = службе каталогов, CN = Windows NT, CN = Services, CN = Configuration,... объектами.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="1dcb5-108">Он представляет время (в часах) между запуском сборки мусора DS.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="1dcb5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-109">Entry</span></span> | <span data-ttu-id="1dcb5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1dcb5-111">CN</span><span class="sxs-lookup"><span data-stu-id="1dcb5-111">CN</span></span>                | <span data-ttu-id="1dcb5-112">Мусор-Coll-период</span><span class="sxs-lookup"><span data-stu-id="1dcb5-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="1dcb5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1dcb5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1dcb5-114">гарбажеколлпериод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="1dcb5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="1dcb5-115">Size</span></span>              | <span data-ttu-id="1dcb5-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="1dcb5-116">4 bytes</span></span>                              |
| <span data-ttu-id="1dcb5-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1dcb5-117">Update Privilege</span></span>  | <span data-ttu-id="1dcb5-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="1dcb5-118">Domain administrator</span></span>                 |
| <span data-ttu-id="1dcb5-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1dcb5-119">Update Frequency</span></span>  | <span data-ttu-id="1dcb5-120">Очень редки.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-120">Very rare.</span></span>                           |
| <span data-ttu-id="1dcb5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-121">Attribute-Id</span></span>      | <span data-ttu-id="1dcb5-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="1dcb5-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="1dcb5-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1dcb5-123">System-Id-Guid</span></span>    | <span data-ttu-id="1dcb5-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="1dcb5-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="1dcb5-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dcb5-125">Syntax</span></span>            | [<span data-ttu-id="1dcb5-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1dcb5-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1dcb5-127">Implementations</span></span>

-   [<span data-ttu-id="1dcb5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1dcb5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1dcb5-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1dcb5-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1dcb5-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1dcb5-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1dcb5-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1dcb5-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1dcb5-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1dcb5-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-136">Entry</span></span> | <span data-ttu-id="1dcb5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="1dcb5-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-139">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-140">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="1dcb5-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-141">System-Only</span></span>            | <span data-ttu-id="1dcb5-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-142">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-144">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-144">True</span></span>                                                                                                  |
| <span data-ttu-id="1dcb5-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-145">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-146">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-147">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-148">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="1dcb5-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-153">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-155">System-Flags</span></span>           | <span data-ttu-id="1dcb5-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-157">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-158">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="1dcb5-159">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1dcb5-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1dcb5-160">Windows Server 2003</span></span>



| <span data-ttu-id="1dcb5-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-161">Entry</span></span> | <span data-ttu-id="1dcb5-162">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="1dcb5-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-164">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-165">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="1dcb5-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-166">System-Only</span></span>            | <span data-ttu-id="1dcb5-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-167">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-168">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-169">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-169">True</span></span>                                                                                                  |
| <span data-ttu-id="1dcb5-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-170">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-171">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-172">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-173">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="1dcb5-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-178">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-180">System-Flags</span></span>           | <span data-ttu-id="1dcb5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-182">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-183">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="1dcb5-184">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1dcb5-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="1dcb5-185">ADAM</span></span>



| <span data-ttu-id="1dcb5-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-186">Entry</span></span> | <span data-ttu-id="1dcb5-187">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1dcb5-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1dcb5-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-189">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-190">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-190">0x80AF</span></span>                                           |
| <span data-ttu-id="1dcb5-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-191">System-Only</span></span>            | <span data-ttu-id="1dcb5-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-192">False</span></span>                                            |
| <span data-ttu-id="1dcb5-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-193">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-194">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-194">True</span></span>                                             |
| <span data-ttu-id="1dcb5-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-195">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-196">False</span></span>                                            |
| <span data-ttu-id="1dcb5-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-197">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-198">False</span></span>                                            |
| <span data-ttu-id="1dcb5-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1dcb5-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1dcb5-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1dcb5-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-203">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-204">0x00000000</span></span>                                       |
| <span data-ttu-id="1dcb5-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-205">System-Flags</span></span>           | <span data-ttu-id="1dcb5-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-206">0x00000010</span></span>                                       |
| <span data-ttu-id="1dcb5-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-207">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-208">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1dcb5-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1dcb5-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-210">Entry</span></span> | <span data-ttu-id="1dcb5-211">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="1dcb5-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-213">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-214">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="1dcb5-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-215">System-Only</span></span>            | <span data-ttu-id="1dcb5-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-216">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-217">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-218">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-218">True</span></span>                                                                                                  |
| <span data-ttu-id="1dcb5-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-219">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-220">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-221">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-222">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="1dcb5-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-227">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-229">System-Flags</span></span>           | <span data-ttu-id="1dcb5-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-231">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-232">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="1dcb5-233">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1dcb5-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dcb5-234">Windows Server 2008</span></span>



| <span data-ttu-id="1dcb5-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-235">Entry</span></span> | <span data-ttu-id="1dcb5-236">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="1dcb5-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-238">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-239">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="1dcb5-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-240">System-Only</span></span>            | <span data-ttu-id="1dcb5-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-241">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-242">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-242">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-243">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-243">True</span></span>                                                                                                  |
| <span data-ttu-id="1dcb5-244">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-244">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-245">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-246">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-246">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-247">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-248">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-249">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="1dcb5-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-252">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-254">System-Flags</span></span>           | <span data-ttu-id="1dcb5-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-256">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-256">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-257">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="1dcb5-258">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1dcb5-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1dcb5-260">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-260">Entry</span></span> | <span data-ttu-id="1dcb5-261">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-262">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="1dcb5-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-263">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-264">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="1dcb5-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-265">System-Only</span></span>            | <span data-ttu-id="1dcb5-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-266">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-267">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-267">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-268">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-268">True</span></span>                                                                                                  |
| <span data-ttu-id="1dcb5-269">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-269">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-270">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-271">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-271">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-272">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-273">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-274">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="1dcb5-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-277">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-279">System-Flags</span></span>           | <span data-ttu-id="1dcb5-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-281">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-281">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-282">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="1dcb5-283">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1dcb5-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1dcb5-284">Windows Server 2012</span></span>



| <span data-ttu-id="1dcb5-285">Ввод</span><span class="sxs-lookup"><span data-stu-id="1dcb5-285">Entry</span></span> | <span data-ttu-id="1dcb5-286">Значение</span><span class="sxs-lookup"><span data-stu-id="1dcb5-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-287">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1dcb5-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="1dcb5-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dcb5-288">MAPI-Id</span></span>                | <span data-ttu-id="1dcb5-289">0x80AF</span><span class="sxs-lookup"><span data-stu-id="1dcb5-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="1dcb5-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dcb5-290">System-Only</span></span>            | <span data-ttu-id="1dcb5-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-291">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-292">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1dcb5-292">Is-Single-Valued</span></span>       | <span data-ttu-id="1dcb5-293">True</span><span class="sxs-lookup"><span data-stu-id="1dcb5-293">True</span></span>                                                                                                  |
| <span data-ttu-id="1dcb5-294">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1dcb5-294">Is Indexed</span></span>             | <span data-ttu-id="1dcb5-295">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-295">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-296">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1dcb5-296">In Global Catalog</span></span>      | <span data-ttu-id="1dcb5-297">Неверно</span><span class="sxs-lookup"><span data-stu-id="1dcb5-297">False</span></span>                                                                                                 |
| <span data-ttu-id="1dcb5-298">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1dcb5-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dcb5-299">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1dcb5-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="1dcb5-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dcb5-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dcb5-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="1dcb5-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-302">Search-Flags</span></span>           | <span data-ttu-id="1dcb5-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dcb5-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dcb5-304">System-Flags</span></span>           | <span data-ttu-id="1dcb5-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dcb5-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="1dcb5-306">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1dcb5-306">Classes used in</span></span>        | [<span data-ttu-id="1dcb5-307">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="1dcb5-308">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





