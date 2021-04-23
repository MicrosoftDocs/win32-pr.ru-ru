---
title: ACS-ДСБМ-Деадтиме, атрибут
description: Этот атрибут содержит интервал времени неработающего выборов (Дсбмдеадинтервал) для домена.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ACS-ДСБМ-Деадтиме
- Схема AD атрибута Аксдсбмдеадтиме
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138339"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="ab15f-105">ACS-ДСБМ-Деадтиме, атрибут</span><span class="sxs-lookup"><span data-stu-id="ab15f-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="ab15f-106">Этот атрибут содержит интервал времени неработающего выборов (Дсбмдеадинтервал) для домена.</span><span class="sxs-lookup"><span data-stu-id="ab15f-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="ab15f-107">Если указанный диспетчер пропускной способности подсети не отправляет \_ объявление о \_ ДСБМ в течение этого интервала, другие диспетчеры пропускной способности подсети (СБМС) в домене выберет новый ДСБМ.</span><span class="sxs-lookup"><span data-stu-id="ab15f-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="ab15f-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-108">Entry</span></span> | <span data-ttu-id="ab15f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ab15f-110">CN</span><span class="sxs-lookup"><span data-stu-id="ab15f-110">CN</span></span>                | <span data-ttu-id="ab15f-111">ACS-ДСБМ-Деадтиме</span><span class="sxs-lookup"><span data-stu-id="ab15f-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="ab15f-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ab15f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ab15f-113">аксдсбмдеадтиме</span><span class="sxs-lookup"><span data-stu-id="ab15f-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="ab15f-114">Размер</span><span class="sxs-lookup"><span data-stu-id="ab15f-114">Size</span></span>              | <span data-ttu-id="ab15f-115">4 байта</span><span class="sxs-lookup"><span data-stu-id="ab15f-115">4 bytes</span></span>                              |
| <span data-ttu-id="ab15f-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ab15f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ab15f-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ab15f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ab15f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-118">Attribute-Id</span></span>      | <span data-ttu-id="ab15f-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="ab15f-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="ab15f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ab15f-120">System-Id-Guid</span></span>    | <span data-ttu-id="ab15f-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ab15f-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="ab15f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab15f-122">Syntax</span></span>            | [<span data-ttu-id="ab15f-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ab15f-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ab15f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ab15f-124">Implementations</span></span>

-   [<span data-ttu-id="ab15f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ab15f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ab15f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab15f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab15f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab15f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab15f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab15f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab15f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab15f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab15f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab15f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ab15f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab15f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ab15f-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-132">Entry</span></span> | <span data-ttu-id="ab15f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab15f-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab15f-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab15f-136">System-Only</span></span>            | <span data-ttu-id="ab15f-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-137">False</span></span>                                        |
| <span data-ttu-id="ab15f-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab15f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ab15f-139">True</span><span class="sxs-lookup"><span data-stu-id="ab15f-139">True</span></span>                                         |
| <span data-ttu-id="ab15f-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab15f-140">Is Indexed</span></span>             | <span data-ttu-id="ab15f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-141">False</span></span>                                        |
| <span data-ttu-id="ab15f-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab15f-142">In Global Catalog</span></span>      | <span data-ttu-id="ab15f-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-143">False</span></span>                                        |
| <span data-ttu-id="ab15f-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab15f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab15f-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab15f-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab15f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab15f-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab15f-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-148">Search-Flags</span></span>           | <span data-ttu-id="ab15f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab15f-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ab15f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-150">System-Flags</span></span>           | <span data-ttu-id="ab15f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab15f-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ab15f-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab15f-152">Classes used in</span></span>        | [<span data-ttu-id="ab15f-153">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab15f-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ab15f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab15f-154">Windows Server 2003</span></span>



| <span data-ttu-id="ab15f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-155">Entry</span></span> | <span data-ttu-id="ab15f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab15f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab15f-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab15f-159">System-Only</span></span>            | <span data-ttu-id="ab15f-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-160">False</span></span>                                        |
| <span data-ttu-id="ab15f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab15f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ab15f-162">True</span><span class="sxs-lookup"><span data-stu-id="ab15f-162">True</span></span>                                         |
| <span data-ttu-id="ab15f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab15f-163">Is Indexed</span></span>             | <span data-ttu-id="ab15f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-164">False</span></span>                                        |
| <span data-ttu-id="ab15f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab15f-165">In Global Catalog</span></span>      | <span data-ttu-id="ab15f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-166">False</span></span>                                        |
| <span data-ttu-id="ab15f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab15f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab15f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab15f-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab15f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab15f-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab15f-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-171">Search-Flags</span></span>           | <span data-ttu-id="ab15f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab15f-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ab15f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-173">System-Flags</span></span>           | <span data-ttu-id="ab15f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab15f-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ab15f-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab15f-175">Classes used in</span></span>        | [<span data-ttu-id="ab15f-176">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab15f-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab15f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab15f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab15f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-178">Entry</span></span> | <span data-ttu-id="ab15f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab15f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab15f-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab15f-182">System-Only</span></span>            | <span data-ttu-id="ab15f-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-183">False</span></span>                                        |
| <span data-ttu-id="ab15f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab15f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ab15f-185">True</span><span class="sxs-lookup"><span data-stu-id="ab15f-185">True</span></span>                                         |
| <span data-ttu-id="ab15f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab15f-186">Is Indexed</span></span>             | <span data-ttu-id="ab15f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-187">False</span></span>                                        |
| <span data-ttu-id="ab15f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab15f-188">In Global Catalog</span></span>      | <span data-ttu-id="ab15f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-189">False</span></span>                                        |
| <span data-ttu-id="ab15f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab15f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab15f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab15f-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab15f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab15f-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab15f-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-194">Search-Flags</span></span>           | <span data-ttu-id="ab15f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab15f-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ab15f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-196">System-Flags</span></span>           | <span data-ttu-id="ab15f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab15f-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ab15f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab15f-198">Classes used in</span></span>        | [<span data-ttu-id="ab15f-199">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab15f-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab15f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab15f-200">Windows Server 2008</span></span>



| <span data-ttu-id="ab15f-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-201">Entry</span></span> | <span data-ttu-id="ab15f-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab15f-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab15f-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab15f-205">System-Only</span></span>            | <span data-ttu-id="ab15f-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-206">False</span></span>                                        |
| <span data-ttu-id="ab15f-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab15f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ab15f-208">True</span><span class="sxs-lookup"><span data-stu-id="ab15f-208">True</span></span>                                         |
| <span data-ttu-id="ab15f-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab15f-209">Is Indexed</span></span>             | <span data-ttu-id="ab15f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-210">False</span></span>                                        |
| <span data-ttu-id="ab15f-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab15f-211">In Global Catalog</span></span>      | <span data-ttu-id="ab15f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-212">False</span></span>                                        |
| <span data-ttu-id="ab15f-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab15f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab15f-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab15f-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab15f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab15f-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab15f-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-217">Search-Flags</span></span>           | <span data-ttu-id="ab15f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab15f-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ab15f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-219">System-Flags</span></span>           | <span data-ttu-id="ab15f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab15f-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ab15f-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab15f-221">Classes used in</span></span>        | [<span data-ttu-id="ab15f-222">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab15f-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab15f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab15f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab15f-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-224">Entry</span></span> | <span data-ttu-id="ab15f-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab15f-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab15f-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab15f-228">System-Only</span></span>            | <span data-ttu-id="ab15f-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-229">False</span></span>                                        |
| <span data-ttu-id="ab15f-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab15f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ab15f-231">True</span><span class="sxs-lookup"><span data-stu-id="ab15f-231">True</span></span>                                         |
| <span data-ttu-id="ab15f-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab15f-232">Is Indexed</span></span>             | <span data-ttu-id="ab15f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-233">False</span></span>                                        |
| <span data-ttu-id="ab15f-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab15f-234">In Global Catalog</span></span>      | <span data-ttu-id="ab15f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-235">False</span></span>                                        |
| <span data-ttu-id="ab15f-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab15f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab15f-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab15f-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab15f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab15f-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab15f-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-240">Search-Flags</span></span>           | <span data-ttu-id="ab15f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab15f-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ab15f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-242">System-Flags</span></span>           | <span data-ttu-id="ab15f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab15f-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ab15f-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab15f-244">Classes used in</span></span>        | [<span data-ttu-id="ab15f-245">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab15f-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab15f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab15f-246">Windows Server 2012</span></span>



| <span data-ttu-id="ab15f-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab15f-247">Entry</span></span> | <span data-ttu-id="ab15f-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ab15f-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab15f-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab15f-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab15f-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab15f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab15f-251">System-Only</span></span>            | <span data-ttu-id="ab15f-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-252">False</span></span>                                        |
| <span data-ttu-id="ab15f-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab15f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ab15f-254">True</span><span class="sxs-lookup"><span data-stu-id="ab15f-254">True</span></span>                                         |
| <span data-ttu-id="ab15f-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab15f-255">Is Indexed</span></span>             | <span data-ttu-id="ab15f-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-256">False</span></span>                                        |
| <span data-ttu-id="ab15f-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab15f-257">In Global Catalog</span></span>      | <span data-ttu-id="ab15f-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab15f-258">False</span></span>                                        |
| <span data-ttu-id="ab15f-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab15f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab15f-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab15f-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab15f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab15f-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab15f-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab15f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-263">Search-Flags</span></span>           | <span data-ttu-id="ab15f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab15f-264">0x00000000</span></span>                                   |
| <span data-ttu-id="ab15f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab15f-265">System-Flags</span></span>           | <span data-ttu-id="ab15f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab15f-266">0x00000010</span></span>                                   |
| <span data-ttu-id="ab15f-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab15f-267">Classes used in</span></span>        | [<span data-ttu-id="ab15f-268">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab15f-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





