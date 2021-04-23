---
title: Атрибут Repl-Interval
description: Атрибут Site-Link объектов, который определяет интервал (в минутах) между циклами репликации между сайтами в списке сайтов.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Repl-Interval
- Схема AD атрибута Реплинтервал
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138506"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="1ab1a-105">Атрибут Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="1ab1a-105">Repl-Interval attribute</span></span>

<span data-ttu-id="1ab1a-106">Атрибут Site-Link объектов, который определяет интервал (в минутах) между циклами репликации между сайтами в списке сайтов.</span><span class="sxs-lookup"><span data-stu-id="1ab1a-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="1ab1a-107">Должен быть кратен 15 минутам (детализация репликации межсайтовых каталогов), не менее 15 минут и не более 10 080 минут (одна неделя).</span><span class="sxs-lookup"><span data-stu-id="1ab1a-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="1ab1a-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-108">Entry</span></span> | <span data-ttu-id="1ab1a-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="1ab1a-110">CN</span><span class="sxs-lookup"><span data-stu-id="1ab1a-110">CN</span></span>                | <span data-ttu-id="1ab1a-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="1ab1a-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="1ab1a-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1ab1a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="1ab1a-113">реплинтервал</span><span class="sxs-lookup"><span data-stu-id="1ab1a-113">replInterval</span></span>                                   |
| <span data-ttu-id="1ab1a-114">Размер</span><span class="sxs-lookup"><span data-stu-id="1ab1a-114">Size</span></span>              | <span data-ttu-id="1ab1a-115">4 байта</span><span class="sxs-lookup"><span data-stu-id="1ab1a-115">4 bytes</span></span>                                        |
| <span data-ttu-id="1ab1a-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1ab1a-116">Update Privilege</span></span>  | <span data-ttu-id="1ab1a-117">Администратор предприятия</span><span class="sxs-lookup"><span data-stu-id="1ab1a-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="1ab1a-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1ab1a-118">Update Frequency</span></span>  | <span data-ttu-id="1ab1a-119">При необходимости изменения интервала репликации.</span><span class="sxs-lookup"><span data-stu-id="1ab1a-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="1ab1a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-120">Attribute-Id</span></span>      | <span data-ttu-id="1ab1a-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="1ab1a-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="1ab1a-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1ab1a-122">System-Id-Guid</span></span>    | <span data-ttu-id="1ab1a-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="1ab1a-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="1ab1a-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ab1a-124">Syntax</span></span>            | [<span data-ttu-id="1ab1a-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="1ab1a-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1ab1a-126">Implementations</span></span>

-   [<span data-ttu-id="1ab1a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ab1a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ab1a-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1ab1a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ab1a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ab1a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ab1a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ab1a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ab1a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="1ab1a-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-135">Entry</span></span> | <span data-ttu-id="1ab1a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-139">System-Only</span></span>            | <span data-ttu-id="1ab1a-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-140">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-142">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-142">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-143">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-144">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-145">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-146">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-151">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-153">System-Flags</span></span>           | <span data-ttu-id="1ab1a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-155">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-156">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-157">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ab1a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ab1a-158">Windows Server 2003</span></span>



| <span data-ttu-id="1ab1a-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-159">Entry</span></span> | <span data-ttu-id="1ab1a-160">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-163">System-Only</span></span>            | <span data-ttu-id="1ab1a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-164">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-166">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-166">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-167">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-168">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-169">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-170">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-175">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-177">System-Flags</span></span>           | <span data-ttu-id="1ab1a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-179">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-180">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-181">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1ab1a-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="1ab1a-182">ADAM</span></span>



| <span data-ttu-id="1ab1a-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-183">Entry</span></span> | <span data-ttu-id="1ab1a-184">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-187">System-Only</span></span>            | <span data-ttu-id="1ab1a-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-188">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-190">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-190">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-191">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-192">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-193">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-194">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-199">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-201">System-Flags</span></span>           | <span data-ttu-id="1ab1a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-203">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-204">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-205">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ab1a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ab1a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ab1a-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-207">Entry</span></span> | <span data-ttu-id="1ab1a-208">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-211">System-Only</span></span>            | <span data-ttu-id="1ab1a-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-212">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-213">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-214">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-214">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-215">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-216">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-217">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-218">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-223">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-225">System-Flags</span></span>           | <span data-ttu-id="1ab1a-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-227">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-228">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-229">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ab1a-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ab1a-230">Windows Server 2008</span></span>



| <span data-ttu-id="1ab1a-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-231">Entry</span></span> | <span data-ttu-id="1ab1a-232">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-235">System-Only</span></span>            | <span data-ttu-id="1ab1a-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-236">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-237">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-238">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-238">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-239">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-240">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-241">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-242">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-247">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-249">System-Flags</span></span>           | <span data-ttu-id="1ab1a-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-251">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-252">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-253">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ab1a-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ab1a-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ab1a-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-255">Entry</span></span> | <span data-ttu-id="1ab1a-256">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-259">System-Only</span></span>            | <span data-ttu-id="1ab1a-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-260">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-261">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-262">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-262">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-263">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-264">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-265">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-266">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-271">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-273">System-Flags</span></span>           | <span data-ttu-id="1ab1a-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-275">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-276">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-277">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ab1a-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ab1a-278">Windows Server 2012</span></span>



| <span data-ttu-id="1ab1a-279">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ab1a-279">Entry</span></span> | <span data-ttu-id="1ab1a-280">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab1a-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab1a-281">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ab1a-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab1a-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1ab1a-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab1a-283">System-Only</span></span>            | <span data-ttu-id="1ab1a-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-284">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ab1a-285">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab1a-286">True</span><span class="sxs-lookup"><span data-stu-id="1ab1a-286">True</span></span>                                                                                                       |
| <span data-ttu-id="1ab1a-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ab1a-287">Is Indexed</span></span>             | <span data-ttu-id="1ab1a-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-288">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ab1a-289">In Global Catalog</span></span>      | <span data-ttu-id="1ab1a-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ab1a-290">False</span></span>                                                                                                      |
| <span data-ttu-id="1ab1a-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ab1a-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab1a-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab1a-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1ab1a-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab1a-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab1a-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1ab1a-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-295">Search-Flags</span></span>           | <span data-ttu-id="1ab1a-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab1a-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab1a-297">System-Flags</span></span>           | <span data-ttu-id="1ab1a-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ab1a-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1ab1a-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ab1a-299">Classes used in</span></span>        | [<span data-ttu-id="1ab1a-300">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="1ab1a-301">**Ссылка на сайт**</span><span class="sxs-lookup"><span data-stu-id="1ab1a-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





