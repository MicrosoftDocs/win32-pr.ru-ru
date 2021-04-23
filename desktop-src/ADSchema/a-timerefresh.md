---
title: Атрибут Time-Refresh
description: Этот атрибут имеет интервал, в течение которого запись ресурса, содержащаяся в интегрированной зоне Active Directory, должна быть обновлена для DNS-сервера. Интервал по умолчанию составляет 7 дней.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Time-Refresh
- Схема AD атрибута Тимерефреш
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989758"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="2cbf4-106">Атрибут Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="2cbf4-106">Time-Refresh attribute</span></span>

<span data-ttu-id="2cbf4-107">Этот атрибут имеет интервал, в течение которого запись ресурса, содержащаяся в интегрированной зоне Active Directory, должна быть обновлена для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="2cbf4-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="2cbf4-108">Интервал по умолчанию составляет 7 дней.</span><span class="sxs-lookup"><span data-stu-id="2cbf4-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="2cbf4-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-109">Entry</span></span> | <span data-ttu-id="2cbf4-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2cbf4-111">CN</span><span class="sxs-lookup"><span data-stu-id="2cbf4-111">CN</span></span>                | <span data-ttu-id="2cbf4-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="2cbf4-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="2cbf4-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2cbf4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2cbf4-114">тимерефреш</span><span class="sxs-lookup"><span data-stu-id="2cbf4-114">timeRefresh</span></span>                          |
| <span data-ttu-id="2cbf4-115">Размер</span><span class="sxs-lookup"><span data-stu-id="2cbf4-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="2cbf4-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2cbf4-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2cbf4-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2cbf4-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2cbf4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-118">Attribute-Id</span></span>      | <span data-ttu-id="2cbf4-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="2cbf4-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="2cbf4-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2cbf4-120">System-Id-Guid</span></span>    | <span data-ttu-id="2cbf4-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="2cbf4-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="2cbf4-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbf4-122">Syntax</span></span>            | [<span data-ttu-id="2cbf4-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2cbf4-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2cbf4-124">Implementations</span></span>

-   [<span data-ttu-id="2cbf4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2cbf4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2cbf4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2cbf4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2cbf4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2cbf4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2cbf4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2cbf4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2cbf4-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-132">Entry</span></span> | <span data-ttu-id="2cbf4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbf4-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cbf4-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cbf4-136">System-Only</span></span>            | <span data-ttu-id="2cbf4-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cbf4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2cbf4-139">True</span><span class="sxs-lookup"><span data-stu-id="2cbf4-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="2cbf4-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cbf4-140">Is Indexed</span></span>             | <span data-ttu-id="2cbf4-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cbf4-142">In Global Catalog</span></span>      | <span data-ttu-id="2cbf4-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cbf4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cbf4-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cbf4-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2cbf4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cbf4-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cbf4-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-148">Search-Flags</span></span>           | <span data-ttu-id="2cbf4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cbf4-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-150">System-Flags</span></span>           | <span data-ttu-id="2cbf4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cbf4-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cbf4-152">Classes used in</span></span>        | [<span data-ttu-id="2cbf4-153">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="2cbf4-154">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2cbf4-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2cbf4-155">Windows Server 2003</span></span>



| <span data-ttu-id="2cbf4-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-156">Entry</span></span> | <span data-ttu-id="2cbf4-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbf4-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cbf4-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cbf4-160">System-Only</span></span>            | <span data-ttu-id="2cbf4-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cbf4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2cbf4-163">True</span><span class="sxs-lookup"><span data-stu-id="2cbf4-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="2cbf4-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cbf4-164">Is Indexed</span></span>             | <span data-ttu-id="2cbf4-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cbf4-166">In Global Catalog</span></span>      | <span data-ttu-id="2cbf4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cbf4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cbf4-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cbf4-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2cbf4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cbf4-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cbf4-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-172">Search-Flags</span></span>           | <span data-ttu-id="2cbf4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cbf4-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-174">System-Flags</span></span>           | <span data-ttu-id="2cbf4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cbf4-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cbf4-176">Classes used in</span></span>        | [<span data-ttu-id="2cbf4-177">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="2cbf4-178">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2cbf4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2cbf4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2cbf4-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-180">Entry</span></span> | <span data-ttu-id="2cbf4-181">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbf4-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cbf4-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cbf4-184">System-Only</span></span>            | <span data-ttu-id="2cbf4-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cbf4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2cbf4-187">True</span><span class="sxs-lookup"><span data-stu-id="2cbf4-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="2cbf4-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cbf4-188">Is Indexed</span></span>             | <span data-ttu-id="2cbf4-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cbf4-190">In Global Catalog</span></span>      | <span data-ttu-id="2cbf4-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cbf4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cbf4-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cbf4-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2cbf4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cbf4-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cbf4-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-196">Search-Flags</span></span>           | <span data-ttu-id="2cbf4-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cbf4-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-198">System-Flags</span></span>           | <span data-ttu-id="2cbf4-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cbf4-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cbf4-200">Classes used in</span></span>        | [<span data-ttu-id="2cbf4-201">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="2cbf4-202">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2cbf4-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cbf4-203">Windows Server 2008</span></span>



| <span data-ttu-id="2cbf4-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-204">Entry</span></span> | <span data-ttu-id="2cbf4-205">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbf4-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cbf4-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cbf4-208">System-Only</span></span>            | <span data-ttu-id="2cbf4-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cbf4-210">Is-Single-Valued</span></span>       | <span data-ttu-id="2cbf4-211">True</span><span class="sxs-lookup"><span data-stu-id="2cbf4-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="2cbf4-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cbf4-212">Is Indexed</span></span>             | <span data-ttu-id="2cbf4-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cbf4-214">In Global Catalog</span></span>      | <span data-ttu-id="2cbf4-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cbf4-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cbf4-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cbf4-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2cbf4-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cbf4-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cbf4-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-220">Search-Flags</span></span>           | <span data-ttu-id="2cbf4-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cbf4-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-222">System-Flags</span></span>           | <span data-ttu-id="2cbf4-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cbf4-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cbf4-224">Classes used in</span></span>        | [<span data-ttu-id="2cbf4-225">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="2cbf4-226">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2cbf4-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2cbf4-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2cbf4-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-228">Entry</span></span> | <span data-ttu-id="2cbf4-229">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbf4-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cbf4-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cbf4-232">System-Only</span></span>            | <span data-ttu-id="2cbf4-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cbf4-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2cbf4-235">True</span><span class="sxs-lookup"><span data-stu-id="2cbf4-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="2cbf4-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cbf4-236">Is Indexed</span></span>             | <span data-ttu-id="2cbf4-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cbf4-238">In Global Catalog</span></span>      | <span data-ttu-id="2cbf4-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cbf4-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cbf4-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cbf4-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2cbf4-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cbf4-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cbf4-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-244">Search-Flags</span></span>           | <span data-ttu-id="2cbf4-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cbf4-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-246">System-Flags</span></span>           | <span data-ttu-id="2cbf4-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cbf4-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cbf4-248">Classes used in</span></span>        | [<span data-ttu-id="2cbf4-249">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="2cbf4-250">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2cbf4-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cbf4-251">Windows Server 2012</span></span>



| <span data-ttu-id="2cbf4-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cbf4-252">Entry</span></span> | <span data-ttu-id="2cbf4-253">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbf4-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbf4-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cbf4-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cbf4-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cbf4-256">System-Only</span></span>            | <span data-ttu-id="2cbf4-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cbf4-258">Is-Single-Valued</span></span>       | <span data-ttu-id="2cbf4-259">True</span><span class="sxs-lookup"><span data-stu-id="2cbf4-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="2cbf4-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cbf4-260">Is Indexed</span></span>             | <span data-ttu-id="2cbf4-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cbf4-262">In Global Catalog</span></span>      | <span data-ttu-id="2cbf4-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cbf4-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="2cbf4-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cbf4-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cbf4-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cbf4-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="2cbf4-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cbf4-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cbf4-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="2cbf4-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-268">Search-Flags</span></span>           | <span data-ttu-id="2cbf4-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cbf4-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cbf4-270">System-Flags</span></span>           | <span data-ttu-id="2cbf4-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cbf4-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="2cbf4-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cbf4-272">Classes used in</span></span>        | [<span data-ttu-id="2cbf4-273">**Link-Track-ОМТ-Entry**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="2cbf4-274">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="2cbf4-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





