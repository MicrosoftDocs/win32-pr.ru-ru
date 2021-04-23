---
title: ACS-ДСБМ — атрибут priority
description: Эти атрибуты содержат приоритет для этого диспетчера пропускной способности подсети (СБМ).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-ДСБМ — схема AD атрибута priority
- Схема AD атрибута Аксдсбмприорити
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139142"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="ba933-105">ACS-ДСБМ — атрибут priority</span><span class="sxs-lookup"><span data-stu-id="ba933-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="ba933-106">Эти атрибуты содержат приоритет для этого диспетчера пропускной способности подсети (СБМ).</span><span class="sxs-lookup"><span data-stu-id="ba933-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="ba933-107">Если необходимо указать новый назначенный диспетчер пропускной способности подсети (ДСБМ), это значение отправляется в другие СБМС в домене как часть сообщения с \_ запросом ДСБМ.</span><span class="sxs-lookup"><span data-stu-id="ba933-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="ba933-108">СБМ с наивысшим приоритетом выбирается в качестве нового ДСБМ.</span><span class="sxs-lookup"><span data-stu-id="ba933-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="ba933-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-109">Entry</span></span> | <span data-ttu-id="ba933-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ba933-111">CN</span><span class="sxs-lookup"><span data-stu-id="ba933-111">CN</span></span>                | <span data-ttu-id="ba933-112">ACS — ДСБМ — приоритет</span><span class="sxs-lookup"><span data-stu-id="ba933-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="ba933-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ba933-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ba933-114">аксдсбмприорити</span><span class="sxs-lookup"><span data-stu-id="ba933-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="ba933-115">Размер</span><span class="sxs-lookup"><span data-stu-id="ba933-115">Size</span></span>              | <span data-ttu-id="ba933-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="ba933-116">4 bytes</span></span>                              |
| <span data-ttu-id="ba933-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ba933-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ba933-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ba933-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ba933-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-119">Attribute-Id</span></span>      | <span data-ttu-id="ba933-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="ba933-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="ba933-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ba933-121">System-Id-Guid</span></span>    | <span data-ttu-id="ba933-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ba933-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="ba933-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba933-123">Syntax</span></span>            | [<span data-ttu-id="ba933-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ba933-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ba933-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ba933-125">Implementations</span></span>

-   [<span data-ttu-id="ba933-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba933-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba933-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba933-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba933-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba933-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba933-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba933-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba933-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba933-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba933-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba933-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba933-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba933-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ba933-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-133">Entry</span></span> | <span data-ttu-id="ba933-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba933-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ba933-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba933-137">System-Only</span></span>            | <span data-ttu-id="ba933-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-138">False</span></span>                                        |
| <span data-ttu-id="ba933-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ba933-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ba933-140">True</span><span class="sxs-lookup"><span data-stu-id="ba933-140">True</span></span>                                         |
| <span data-ttu-id="ba933-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ba933-141">Is Indexed</span></span>             | <span data-ttu-id="ba933-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-142">False</span></span>                                        |
| <span data-ttu-id="ba933-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ba933-143">In Global Catalog</span></span>      | <span data-ttu-id="ba933-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-144">False</span></span>                                        |
| <span data-ttu-id="ba933-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ba933-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba933-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ba933-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba933-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba933-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba933-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba933-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba933-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-149">Search-Flags</span></span>           | <span data-ttu-id="ba933-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba933-150">0x00000000</span></span>                                   |
| <span data-ttu-id="ba933-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-151">System-Flags</span></span>           | <span data-ttu-id="ba933-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba933-152">0x00000010</span></span>                                   |
| <span data-ttu-id="ba933-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ba933-153">Classes used in</span></span>        | [<span data-ttu-id="ba933-154">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ba933-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba933-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba933-155">Windows Server 2003</span></span>



| <span data-ttu-id="ba933-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-156">Entry</span></span> | <span data-ttu-id="ba933-157">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba933-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ba933-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba933-160">System-Only</span></span>            | <span data-ttu-id="ba933-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-161">False</span></span>                                        |
| <span data-ttu-id="ba933-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ba933-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ba933-163">True</span><span class="sxs-lookup"><span data-stu-id="ba933-163">True</span></span>                                         |
| <span data-ttu-id="ba933-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ba933-164">Is Indexed</span></span>             | <span data-ttu-id="ba933-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-165">False</span></span>                                        |
| <span data-ttu-id="ba933-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ba933-166">In Global Catalog</span></span>      | <span data-ttu-id="ba933-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-167">False</span></span>                                        |
| <span data-ttu-id="ba933-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ba933-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba933-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ba933-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba933-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba933-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba933-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba933-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba933-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-172">Search-Flags</span></span>           | <span data-ttu-id="ba933-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba933-173">0x00000000</span></span>                                   |
| <span data-ttu-id="ba933-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-174">System-Flags</span></span>           | <span data-ttu-id="ba933-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba933-175">0x00000010</span></span>                                   |
| <span data-ttu-id="ba933-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ba933-176">Classes used in</span></span>        | [<span data-ttu-id="ba933-177">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ba933-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba933-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba933-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba933-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-179">Entry</span></span> | <span data-ttu-id="ba933-180">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba933-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ba933-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba933-183">System-Only</span></span>            | <span data-ttu-id="ba933-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-184">False</span></span>                                        |
| <span data-ttu-id="ba933-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ba933-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ba933-186">True</span><span class="sxs-lookup"><span data-stu-id="ba933-186">True</span></span>                                         |
| <span data-ttu-id="ba933-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ba933-187">Is Indexed</span></span>             | <span data-ttu-id="ba933-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-188">False</span></span>                                        |
| <span data-ttu-id="ba933-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ba933-189">In Global Catalog</span></span>      | <span data-ttu-id="ba933-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-190">False</span></span>                                        |
| <span data-ttu-id="ba933-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ba933-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba933-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ba933-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba933-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba933-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba933-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba933-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba933-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-195">Search-Flags</span></span>           | <span data-ttu-id="ba933-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba933-196">0x00000000</span></span>                                   |
| <span data-ttu-id="ba933-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-197">System-Flags</span></span>           | <span data-ttu-id="ba933-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba933-198">0x00000010</span></span>                                   |
| <span data-ttu-id="ba933-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ba933-199">Classes used in</span></span>        | [<span data-ttu-id="ba933-200">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ba933-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba933-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba933-201">Windows Server 2008</span></span>



| <span data-ttu-id="ba933-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-202">Entry</span></span> | <span data-ttu-id="ba933-203">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba933-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ba933-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba933-206">System-Only</span></span>            | <span data-ttu-id="ba933-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-207">False</span></span>                                        |
| <span data-ttu-id="ba933-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ba933-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ba933-209">True</span><span class="sxs-lookup"><span data-stu-id="ba933-209">True</span></span>                                         |
| <span data-ttu-id="ba933-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ba933-210">Is Indexed</span></span>             | <span data-ttu-id="ba933-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-211">False</span></span>                                        |
| <span data-ttu-id="ba933-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ba933-212">In Global Catalog</span></span>      | <span data-ttu-id="ba933-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-213">False</span></span>                                        |
| <span data-ttu-id="ba933-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ba933-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba933-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ba933-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba933-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba933-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba933-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba933-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba933-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-218">Search-Flags</span></span>           | <span data-ttu-id="ba933-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba933-219">0x00000000</span></span>                                   |
| <span data-ttu-id="ba933-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-220">System-Flags</span></span>           | <span data-ttu-id="ba933-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba933-221">0x00000010</span></span>                                   |
| <span data-ttu-id="ba933-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ba933-222">Classes used in</span></span>        | [<span data-ttu-id="ba933-223">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ba933-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba933-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba933-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba933-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-225">Entry</span></span> | <span data-ttu-id="ba933-226">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba933-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ba933-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba933-229">System-Only</span></span>            | <span data-ttu-id="ba933-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-230">False</span></span>                                        |
| <span data-ttu-id="ba933-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ba933-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ba933-232">True</span><span class="sxs-lookup"><span data-stu-id="ba933-232">True</span></span>                                         |
| <span data-ttu-id="ba933-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ba933-233">Is Indexed</span></span>             | <span data-ttu-id="ba933-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-234">False</span></span>                                        |
| <span data-ttu-id="ba933-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ba933-235">In Global Catalog</span></span>      | <span data-ttu-id="ba933-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-236">False</span></span>                                        |
| <span data-ttu-id="ba933-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ba933-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba933-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ba933-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba933-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba933-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba933-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba933-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba933-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-241">Search-Flags</span></span>           | <span data-ttu-id="ba933-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba933-242">0x00000000</span></span>                                   |
| <span data-ttu-id="ba933-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-243">System-Flags</span></span>           | <span data-ttu-id="ba933-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba933-244">0x00000010</span></span>                                   |
| <span data-ttu-id="ba933-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ba933-245">Classes used in</span></span>        | [<span data-ttu-id="ba933-246">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ba933-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba933-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba933-247">Windows Server 2012</span></span>



| <span data-ttu-id="ba933-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba933-248">Entry</span></span> | <span data-ttu-id="ba933-249">Значение</span><span class="sxs-lookup"><span data-stu-id="ba933-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba933-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ba933-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba933-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba933-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba933-252">System-Only</span></span>            | <span data-ttu-id="ba933-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-253">False</span></span>                                        |
| <span data-ttu-id="ba933-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ba933-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ba933-255">True</span><span class="sxs-lookup"><span data-stu-id="ba933-255">True</span></span>                                         |
| <span data-ttu-id="ba933-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ba933-256">Is Indexed</span></span>             | <span data-ttu-id="ba933-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-257">False</span></span>                                        |
| <span data-ttu-id="ba933-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ba933-258">In Global Catalog</span></span>      | <span data-ttu-id="ba933-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="ba933-259">False</span></span>                                        |
| <span data-ttu-id="ba933-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ba933-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba933-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ba933-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba933-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba933-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba933-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba933-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba933-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-264">Search-Flags</span></span>           | <span data-ttu-id="ba933-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba933-265">0x00000000</span></span>                                   |
| <span data-ttu-id="ba933-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba933-266">System-Flags</span></span>           | <span data-ttu-id="ba933-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba933-267">0x00000010</span></span>                                   |
| <span data-ttu-id="ba933-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ba933-268">Classes used in</span></span>        | [<span data-ttu-id="ba933-269">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ba933-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





