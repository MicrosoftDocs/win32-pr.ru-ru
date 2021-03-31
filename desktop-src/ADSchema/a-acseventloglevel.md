---
title: ACS-Event-атрибут уровня журнала
description: Уровень ведения журнала RSVP.
ms.assetid: 2f3c645d-a064-40fb-965c-388b2fac61bc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута на уровне журнала ACS-событий
- Схема AD атрибута Аксевентлоглевел
topic_type:
- apiref
api_name:
- ACS-Event-Log-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bb5701f665a3685845368eb2adc72fc33d10bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804469"
---
# <a name="acs-event-log-level-attribute"></a><span data-ttu-id="1ae98-105">ACS-Event-атрибут уровня журнала</span><span class="sxs-lookup"><span data-stu-id="1ae98-105">ACS-Event-Log-Level attribute</span></span>

<span data-ttu-id="1ae98-106">Уровень ведения журнала RSVP.</span><span class="sxs-lookup"><span data-stu-id="1ae98-106">RSVP logging level.</span></span>



| <span data-ttu-id="1ae98-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-107">Entry</span></span> | <span data-ttu-id="1ae98-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1ae98-109">CN</span><span class="sxs-lookup"><span data-stu-id="1ae98-109">CN</span></span>                | <span data-ttu-id="1ae98-110">ACS-Event-уровень журнала</span><span class="sxs-lookup"><span data-stu-id="1ae98-110">ACS-Event-Log-Level</span></span>                     |
| <span data-ttu-id="1ae98-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1ae98-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1ae98-112">аксевентлоглевел</span><span class="sxs-lookup"><span data-stu-id="1ae98-112">aCSEventLogLevel</span></span>                        |
| <span data-ttu-id="1ae98-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1ae98-113">Size</span></span>              | <span data-ttu-id="1ae98-114">4 байта могут иметь значения 0, 1, 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="1ae98-114">4 bytes can have values 0, 1, 2, and 3.</span></span> |
| <span data-ttu-id="1ae98-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1ae98-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="1ae98-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1ae98-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="1ae98-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-117">Attribute-Id</span></span>      | <span data-ttu-id="1ae98-118">1.2.840.113556.1.4.769</span><span class="sxs-lookup"><span data-stu-id="1ae98-118">1.2.840.113556.1.4.769</span></span>                  |
| <span data-ttu-id="1ae98-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1ae98-119">System-Id-Guid</span></span>    | <span data-ttu-id="1ae98-120">7f561286-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1ae98-120">7f561286-5301-11d1-a9c5-0000f80367c1</span></span>    |
| <span data-ttu-id="1ae98-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ae98-121">Syntax</span></span>            | [<span data-ttu-id="1ae98-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="1ae98-122">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="1ae98-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1ae98-123">Implementations</span></span>

-   [<span data-ttu-id="1ae98-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ae98-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ae98-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ae98-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ae98-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ae98-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ae98-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ae98-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ae98-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ae98-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ae98-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ae98-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ae98-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ae98-130">Windows 2000 Server</span></span>



| <span data-ttu-id="1ae98-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-131">Entry</span></span> | <span data-ttu-id="1ae98-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1ae98-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ae98-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ae98-135">System-Only</span></span>            | <span data-ttu-id="1ae98-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-136">False</span></span>                                        |
| <span data-ttu-id="1ae98-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ae98-137">Is-Single-Valued</span></span>       | <span data-ttu-id="1ae98-138">True</span><span class="sxs-lookup"><span data-stu-id="1ae98-138">True</span></span>                                         |
| <span data-ttu-id="1ae98-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ae98-139">Is Indexed</span></span>             | <span data-ttu-id="1ae98-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-140">False</span></span>                                        |
| <span data-ttu-id="1ae98-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ae98-141">In Global Catalog</span></span>      | <span data-ttu-id="1ae98-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-142">False</span></span>                                        |
| <span data-ttu-id="1ae98-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ae98-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ae98-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ae98-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1ae98-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ae98-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ae98-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-147">Search-Flags</span></span>           | <span data-ttu-id="1ae98-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ae98-148">0x00000000</span></span>                                   |
| <span data-ttu-id="1ae98-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-149">System-Flags</span></span>           | <span data-ttu-id="1ae98-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ae98-150">0x00000010</span></span>                                   |
| <span data-ttu-id="1ae98-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ae98-151">Classes used in</span></span>        | [<span data-ttu-id="1ae98-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1ae98-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ae98-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ae98-153">Windows Server 2003</span></span>



| <span data-ttu-id="1ae98-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-154">Entry</span></span> | <span data-ttu-id="1ae98-155">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1ae98-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ae98-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ae98-158">System-Only</span></span>            | <span data-ttu-id="1ae98-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-159">False</span></span>                                        |
| <span data-ttu-id="1ae98-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ae98-160">Is-Single-Valued</span></span>       | <span data-ttu-id="1ae98-161">True</span><span class="sxs-lookup"><span data-stu-id="1ae98-161">True</span></span>                                         |
| <span data-ttu-id="1ae98-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ae98-162">Is Indexed</span></span>             | <span data-ttu-id="1ae98-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-163">False</span></span>                                        |
| <span data-ttu-id="1ae98-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ae98-164">In Global Catalog</span></span>      | <span data-ttu-id="1ae98-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-165">False</span></span>                                        |
| <span data-ttu-id="1ae98-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ae98-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ae98-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ae98-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1ae98-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ae98-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ae98-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-170">Search-Flags</span></span>           | <span data-ttu-id="1ae98-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ae98-171">0x00000000</span></span>                                   |
| <span data-ttu-id="1ae98-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-172">System-Flags</span></span>           | <span data-ttu-id="1ae98-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ae98-173">0x00000010</span></span>                                   |
| <span data-ttu-id="1ae98-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ae98-174">Classes used in</span></span>        | [<span data-ttu-id="1ae98-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1ae98-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ae98-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ae98-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ae98-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-177">Entry</span></span> | <span data-ttu-id="1ae98-178">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1ae98-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ae98-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ae98-181">System-Only</span></span>            | <span data-ttu-id="1ae98-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-182">False</span></span>                                        |
| <span data-ttu-id="1ae98-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ae98-183">Is-Single-Valued</span></span>       | <span data-ttu-id="1ae98-184">True</span><span class="sxs-lookup"><span data-stu-id="1ae98-184">True</span></span>                                         |
| <span data-ttu-id="1ae98-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ae98-185">Is Indexed</span></span>             | <span data-ttu-id="1ae98-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-186">False</span></span>                                        |
| <span data-ttu-id="1ae98-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ae98-187">In Global Catalog</span></span>      | <span data-ttu-id="1ae98-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-188">False</span></span>                                        |
| <span data-ttu-id="1ae98-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ae98-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ae98-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ae98-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1ae98-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ae98-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ae98-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-193">Search-Flags</span></span>           | <span data-ttu-id="1ae98-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ae98-194">0x00000000</span></span>                                   |
| <span data-ttu-id="1ae98-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-195">System-Flags</span></span>           | <span data-ttu-id="1ae98-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ae98-196">0x00000010</span></span>                                   |
| <span data-ttu-id="1ae98-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ae98-197">Classes used in</span></span>        | [<span data-ttu-id="1ae98-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1ae98-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ae98-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ae98-199">Windows Server 2008</span></span>



| <span data-ttu-id="1ae98-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-200">Entry</span></span> | <span data-ttu-id="1ae98-201">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1ae98-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ae98-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ae98-204">System-Only</span></span>            | <span data-ttu-id="1ae98-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-205">False</span></span>                                        |
| <span data-ttu-id="1ae98-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ae98-206">Is-Single-Valued</span></span>       | <span data-ttu-id="1ae98-207">True</span><span class="sxs-lookup"><span data-stu-id="1ae98-207">True</span></span>                                         |
| <span data-ttu-id="1ae98-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ae98-208">Is Indexed</span></span>             | <span data-ttu-id="1ae98-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-209">False</span></span>                                        |
| <span data-ttu-id="1ae98-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ae98-210">In Global Catalog</span></span>      | <span data-ttu-id="1ae98-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-211">False</span></span>                                        |
| <span data-ttu-id="1ae98-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ae98-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ae98-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ae98-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1ae98-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ae98-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ae98-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-216">Search-Flags</span></span>           | <span data-ttu-id="1ae98-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ae98-217">0x00000000</span></span>                                   |
| <span data-ttu-id="1ae98-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-218">System-Flags</span></span>           | <span data-ttu-id="1ae98-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ae98-219">0x00000010</span></span>                                   |
| <span data-ttu-id="1ae98-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ae98-220">Classes used in</span></span>        | [<span data-ttu-id="1ae98-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1ae98-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ae98-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ae98-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ae98-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-223">Entry</span></span> | <span data-ttu-id="1ae98-224">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1ae98-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ae98-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ae98-227">System-Only</span></span>            | <span data-ttu-id="1ae98-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-228">False</span></span>                                        |
| <span data-ttu-id="1ae98-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ae98-229">Is-Single-Valued</span></span>       | <span data-ttu-id="1ae98-230">True</span><span class="sxs-lookup"><span data-stu-id="1ae98-230">True</span></span>                                         |
| <span data-ttu-id="1ae98-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ae98-231">Is Indexed</span></span>             | <span data-ttu-id="1ae98-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-232">False</span></span>                                        |
| <span data-ttu-id="1ae98-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ae98-233">In Global Catalog</span></span>      | <span data-ttu-id="1ae98-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-234">False</span></span>                                        |
| <span data-ttu-id="1ae98-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ae98-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ae98-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ae98-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1ae98-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ae98-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ae98-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-239">Search-Flags</span></span>           | <span data-ttu-id="1ae98-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ae98-240">0x00000000</span></span>                                   |
| <span data-ttu-id="1ae98-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-241">System-Flags</span></span>           | <span data-ttu-id="1ae98-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ae98-242">0x00000010</span></span>                                   |
| <span data-ttu-id="1ae98-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ae98-243">Classes used in</span></span>        | [<span data-ttu-id="1ae98-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1ae98-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ae98-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ae98-245">Windows Server 2012</span></span>



| <span data-ttu-id="1ae98-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ae98-246">Entry</span></span> | <span data-ttu-id="1ae98-247">Значение</span><span class="sxs-lookup"><span data-stu-id="1ae98-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1ae98-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ae98-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ae98-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1ae98-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ae98-250">System-Only</span></span>            | <span data-ttu-id="1ae98-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-251">False</span></span>                                        |
| <span data-ttu-id="1ae98-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ae98-252">Is-Single-Valued</span></span>       | <span data-ttu-id="1ae98-253">True</span><span class="sxs-lookup"><span data-stu-id="1ae98-253">True</span></span>                                         |
| <span data-ttu-id="1ae98-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ae98-254">Is Indexed</span></span>             | <span data-ttu-id="1ae98-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-255">False</span></span>                                        |
| <span data-ttu-id="1ae98-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ae98-256">In Global Catalog</span></span>      | <span data-ttu-id="1ae98-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ae98-257">False</span></span>                                        |
| <span data-ttu-id="1ae98-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ae98-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ae98-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ae98-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1ae98-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ae98-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ae98-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1ae98-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-262">Search-Flags</span></span>           | <span data-ttu-id="1ae98-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ae98-263">0x00000000</span></span>                                   |
| <span data-ttu-id="1ae98-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ae98-264">System-Flags</span></span>           | <span data-ttu-id="1ae98-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ae98-265">0x00000010</span></span>                                   |
| <span data-ttu-id="1ae98-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ae98-266">Classes used in</span></span>        | [<span data-ttu-id="1ae98-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1ae98-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





