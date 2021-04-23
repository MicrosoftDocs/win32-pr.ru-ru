---
title: ACS-ДСБМ-обновить атрибут
description: Этот атрибут содержит значение интервала таймера, которое определяет, когда заданный диспетчер пропускной способности подсети (ДСБМ) отправляет сообщение об обновлении ( \_ \_ ДСБМ) всем диспетчерам пропускной способности подсети в домене.
ms.assetid: 018fd748-ca2e-41e1-a920-224a32e13e21
ms.tgt_platform: multiple
keywords:
- ACS-ДСБМ — обновление схемы AD атрибута
- Схема AD атрибута Аксдсбмрефреш
topic_type:
- apiref
api_name:
- ACS-DSBM-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d662b886a8c97f3d155d3c1b40efcef67f7f1f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989583"
---
# <a name="acs-dsbm-refresh-attribute"></a><span data-ttu-id="21c99-105">ACS-ДСБМ-обновить атрибут</span><span class="sxs-lookup"><span data-stu-id="21c99-105">ACS-DSBM-Refresh attribute</span></span>

<span data-ttu-id="21c99-106">Этот атрибут содержит значение интервала таймера, которое определяет, когда заданный диспетчер пропускной способности подсети (ДСБМ) отправляет сообщение об обновлении ( \_ \_ ДСБМ) всем диспетчерам пропускной способности подсети в домене.</span><span class="sxs-lookup"><span data-stu-id="21c99-106">This attribute contains the interval timer value that determines when the Designated Subnet Bandwidth Manager (DSBM) sends out a refresh message (I\_AM\_DSBM) to all of the Subnet Bandwidth Managers in a domain.</span></span>



| <span data-ttu-id="21c99-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-107">Entry</span></span> | <span data-ttu-id="21c99-108">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="21c99-109">CN</span><span class="sxs-lookup"><span data-stu-id="21c99-109">CN</span></span>                | <span data-ttu-id="21c99-110">ACS-ДСБМ — обновление</span><span class="sxs-lookup"><span data-stu-id="21c99-110">ACS-DSBM-Refresh</span></span>                     |
| <span data-ttu-id="21c99-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="21c99-111">Ldap-Display-Name</span></span> | <span data-ttu-id="21c99-112">аксдсбмрефреш</span><span class="sxs-lookup"><span data-stu-id="21c99-112">aCSDSBMRefresh</span></span>                       |
| <span data-ttu-id="21c99-113">Размер</span><span class="sxs-lookup"><span data-stu-id="21c99-113">Size</span></span>              | <span data-ttu-id="21c99-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="21c99-114">4 bytes</span></span>                              |
| <span data-ttu-id="21c99-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="21c99-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="21c99-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="21c99-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="21c99-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-117">Attribute-Id</span></span>      | <span data-ttu-id="21c99-118">1.2.840.113556.1.4.777</span><span class="sxs-lookup"><span data-stu-id="21c99-118">1.2.840.113556.1.4.777</span></span>               |
| <span data-ttu-id="21c99-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="21c99-119">System-Id-Guid</span></span>    | <span data-ttu-id="21c99-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="21c99-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="21c99-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21c99-121">Syntax</span></span>            | [<span data-ttu-id="21c99-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="21c99-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="21c99-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="21c99-123">Implementations</span></span>

-   [<span data-ttu-id="21c99-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21c99-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21c99-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21c99-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21c99-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21c99-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21c99-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21c99-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21c99-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21c99-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21c99-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21c99-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21c99-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21c99-130">Windows 2000 Server</span></span>



| <span data-ttu-id="21c99-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-131">Entry</span></span> | <span data-ttu-id="21c99-132">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="21c99-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21c99-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="21c99-135">System-Only</span></span>            | <span data-ttu-id="21c99-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-136">False</span></span>                                        |
| <span data-ttu-id="21c99-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21c99-137">Is-Single-Valued</span></span>       | <span data-ttu-id="21c99-138">True</span><span class="sxs-lookup"><span data-stu-id="21c99-138">True</span></span>                                         |
| <span data-ttu-id="21c99-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21c99-139">Is Indexed</span></span>             | <span data-ttu-id="21c99-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-140">False</span></span>                                        |
| <span data-ttu-id="21c99-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21c99-141">In Global Catalog</span></span>      | <span data-ttu-id="21c99-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-142">False</span></span>                                        |
| <span data-ttu-id="21c99-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21c99-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="21c99-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21c99-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="21c99-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21c99-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="21c99-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21c99-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="21c99-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-147">Search-Flags</span></span>           | <span data-ttu-id="21c99-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21c99-148">0x00000000</span></span>                                   |
| <span data-ttu-id="21c99-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-149">System-Flags</span></span>           | <span data-ttu-id="21c99-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21c99-150">0x00000010</span></span>                                   |
| <span data-ttu-id="21c99-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21c99-151">Classes used in</span></span>        | [<span data-ttu-id="21c99-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="21c99-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21c99-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21c99-153">Windows Server 2003</span></span>



| <span data-ttu-id="21c99-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-154">Entry</span></span> | <span data-ttu-id="21c99-155">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="21c99-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21c99-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="21c99-158">System-Only</span></span>            | <span data-ttu-id="21c99-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-159">False</span></span>                                        |
| <span data-ttu-id="21c99-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21c99-160">Is-Single-Valued</span></span>       | <span data-ttu-id="21c99-161">True</span><span class="sxs-lookup"><span data-stu-id="21c99-161">True</span></span>                                         |
| <span data-ttu-id="21c99-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21c99-162">Is Indexed</span></span>             | <span data-ttu-id="21c99-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-163">False</span></span>                                        |
| <span data-ttu-id="21c99-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21c99-164">In Global Catalog</span></span>      | <span data-ttu-id="21c99-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-165">False</span></span>                                        |
| <span data-ttu-id="21c99-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21c99-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="21c99-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21c99-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="21c99-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21c99-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="21c99-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21c99-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="21c99-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-170">Search-Flags</span></span>           | <span data-ttu-id="21c99-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21c99-171">0x00000000</span></span>                                   |
| <span data-ttu-id="21c99-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-172">System-Flags</span></span>           | <span data-ttu-id="21c99-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21c99-173">0x00000010</span></span>                                   |
| <span data-ttu-id="21c99-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21c99-174">Classes used in</span></span>        | [<span data-ttu-id="21c99-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="21c99-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21c99-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21c99-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21c99-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-177">Entry</span></span> | <span data-ttu-id="21c99-178">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="21c99-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21c99-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="21c99-181">System-Only</span></span>            | <span data-ttu-id="21c99-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-182">False</span></span>                                        |
| <span data-ttu-id="21c99-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21c99-183">Is-Single-Valued</span></span>       | <span data-ttu-id="21c99-184">True</span><span class="sxs-lookup"><span data-stu-id="21c99-184">True</span></span>                                         |
| <span data-ttu-id="21c99-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21c99-185">Is Indexed</span></span>             | <span data-ttu-id="21c99-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-186">False</span></span>                                        |
| <span data-ttu-id="21c99-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21c99-187">In Global Catalog</span></span>      | <span data-ttu-id="21c99-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-188">False</span></span>                                        |
| <span data-ttu-id="21c99-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21c99-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="21c99-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21c99-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="21c99-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21c99-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="21c99-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21c99-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="21c99-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-193">Search-Flags</span></span>           | <span data-ttu-id="21c99-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21c99-194">0x00000000</span></span>                                   |
| <span data-ttu-id="21c99-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-195">System-Flags</span></span>           | <span data-ttu-id="21c99-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21c99-196">0x00000010</span></span>                                   |
| <span data-ttu-id="21c99-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21c99-197">Classes used in</span></span>        | [<span data-ttu-id="21c99-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="21c99-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21c99-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21c99-199">Windows Server 2008</span></span>



| <span data-ttu-id="21c99-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-200">Entry</span></span> | <span data-ttu-id="21c99-201">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="21c99-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21c99-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="21c99-204">System-Only</span></span>            | <span data-ttu-id="21c99-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-205">False</span></span>                                        |
| <span data-ttu-id="21c99-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21c99-206">Is-Single-Valued</span></span>       | <span data-ttu-id="21c99-207">True</span><span class="sxs-lookup"><span data-stu-id="21c99-207">True</span></span>                                         |
| <span data-ttu-id="21c99-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21c99-208">Is Indexed</span></span>             | <span data-ttu-id="21c99-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-209">False</span></span>                                        |
| <span data-ttu-id="21c99-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21c99-210">In Global Catalog</span></span>      | <span data-ttu-id="21c99-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-211">False</span></span>                                        |
| <span data-ttu-id="21c99-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21c99-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="21c99-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21c99-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="21c99-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21c99-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="21c99-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21c99-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="21c99-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-216">Search-Flags</span></span>           | <span data-ttu-id="21c99-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21c99-217">0x00000000</span></span>                                   |
| <span data-ttu-id="21c99-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-218">System-Flags</span></span>           | <span data-ttu-id="21c99-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21c99-219">0x00000010</span></span>                                   |
| <span data-ttu-id="21c99-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21c99-220">Classes used in</span></span>        | [<span data-ttu-id="21c99-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="21c99-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21c99-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21c99-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21c99-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-223">Entry</span></span> | <span data-ttu-id="21c99-224">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="21c99-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21c99-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="21c99-227">System-Only</span></span>            | <span data-ttu-id="21c99-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-228">False</span></span>                                        |
| <span data-ttu-id="21c99-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21c99-229">Is-Single-Valued</span></span>       | <span data-ttu-id="21c99-230">True</span><span class="sxs-lookup"><span data-stu-id="21c99-230">True</span></span>                                         |
| <span data-ttu-id="21c99-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21c99-231">Is Indexed</span></span>             | <span data-ttu-id="21c99-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-232">False</span></span>                                        |
| <span data-ttu-id="21c99-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21c99-233">In Global Catalog</span></span>      | <span data-ttu-id="21c99-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-234">False</span></span>                                        |
| <span data-ttu-id="21c99-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21c99-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="21c99-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21c99-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="21c99-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21c99-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="21c99-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21c99-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="21c99-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-239">Search-Flags</span></span>           | <span data-ttu-id="21c99-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21c99-240">0x00000000</span></span>                                   |
| <span data-ttu-id="21c99-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-241">System-Flags</span></span>           | <span data-ttu-id="21c99-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21c99-242">0x00000010</span></span>                                   |
| <span data-ttu-id="21c99-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21c99-243">Classes used in</span></span>        | [<span data-ttu-id="21c99-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="21c99-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21c99-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21c99-245">Windows Server 2012</span></span>



| <span data-ttu-id="21c99-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="21c99-246">Entry</span></span> | <span data-ttu-id="21c99-247">Значение</span><span class="sxs-lookup"><span data-stu-id="21c99-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="21c99-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21c99-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21c99-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="21c99-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="21c99-250">System-Only</span></span>            | <span data-ttu-id="21c99-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-251">False</span></span>                                        |
| <span data-ttu-id="21c99-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21c99-252">Is-Single-Valued</span></span>       | <span data-ttu-id="21c99-253">True</span><span class="sxs-lookup"><span data-stu-id="21c99-253">True</span></span>                                         |
| <span data-ttu-id="21c99-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21c99-254">Is Indexed</span></span>             | <span data-ttu-id="21c99-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-255">False</span></span>                                        |
| <span data-ttu-id="21c99-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21c99-256">In Global Catalog</span></span>      | <span data-ttu-id="21c99-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="21c99-257">False</span></span>                                        |
| <span data-ttu-id="21c99-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21c99-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="21c99-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21c99-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="21c99-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21c99-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="21c99-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21c99-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="21c99-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-262">Search-Flags</span></span>           | <span data-ttu-id="21c99-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21c99-263">0x00000000</span></span>                                   |
| <span data-ttu-id="21c99-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21c99-264">System-Flags</span></span>           | <span data-ttu-id="21c99-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21c99-265">0x00000010</span></span>                                   |
| <span data-ttu-id="21c99-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21c99-266">Classes used in</span></span>        | [<span data-ttu-id="21c99-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="21c99-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





