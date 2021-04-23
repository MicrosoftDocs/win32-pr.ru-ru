---
title: Атрибут ACS-Enable-ACS-Service
description: Значение true, если служба ACS должна быть включена.
ms.assetid: 376f80a7-f07f-44ef-a12f-8c732ec514c4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута службы ACS-Enable-ACS
- Схема AD атрибута Аксенаблеакссервице
topic_type:
- apiref
api_name:
- ACS-Enable-ACS-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2eb4994157d90562cc15ccaaa03de8a03383e0c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139139"
---
# <a name="acs-enable-acs-service-attribute"></a><span data-ttu-id="a1a3f-105">Атрибут ACS-Enable-ACS-Service</span><span class="sxs-lookup"><span data-stu-id="a1a3f-105">ACS-Enable-ACS-Service attribute</span></span>

<span data-ttu-id="a1a3f-106">Значение true, если служба ACS должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="a1a3f-106">True if ACS service is to be enabled.</span></span>



| <span data-ttu-id="a1a3f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-107">Entry</span></span> | <span data-ttu-id="a1a3f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a1a3f-109">CN</span><span class="sxs-lookup"><span data-stu-id="a1a3f-109">CN</span></span>                | <span data-ttu-id="a1a3f-110">ACS-Enable-ACS-Service</span><span class="sxs-lookup"><span data-stu-id="a1a3f-110">ACS-Enable-ACS-Service</span></span>               |
| <span data-ttu-id="a1a3f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a1a3f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a1a3f-112">аксенаблеакссервице</span><span class="sxs-lookup"><span data-stu-id="a1a3f-112">aCSEnableACSService</span></span>                  |
| <span data-ttu-id="a1a3f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a1a3f-113">Size</span></span>              | <span data-ttu-id="a1a3f-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="a1a3f-114">4 bytes</span></span>                              |
| <span data-ttu-id="a1a3f-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a1a3f-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a1a3f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a1a3f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a1a3f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-117">Attribute-Id</span></span>      | <span data-ttu-id="a1a3f-118">1.2.840.113556.1.4.770</span><span class="sxs-lookup"><span data-stu-id="a1a3f-118">1.2.840.113556.1.4.770</span></span>               |
| <span data-ttu-id="a1a3f-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a1a3f-119">System-Id-Guid</span></span>    | <span data-ttu-id="a1a3f-120">7f561287-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a1a3f-120">7f561287-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="a1a3f-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1a3f-121">Syntax</span></span>            | [<span data-ttu-id="a1a3f-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a1a3f-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a1a3f-123">Implementations</span></span>

-   [<span data-ttu-id="a1a3f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1a3f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1a3f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1a3f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1a3f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1a3f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1a3f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1a3f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a1a3f-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-131">Entry</span></span> | <span data-ttu-id="a1a3f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1a3f-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1a3f-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a3f-135">System-Only</span></span>            | <span data-ttu-id="a1a3f-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-136">False</span></span>                                        |
| <span data-ttu-id="a1a3f-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1a3f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a3f-138">True</span><span class="sxs-lookup"><span data-stu-id="a1a3f-138">True</span></span>                                         |
| <span data-ttu-id="a1a3f-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1a3f-139">Is Indexed</span></span>             | <span data-ttu-id="a1a3f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-140">False</span></span>                                        |
| <span data-ttu-id="a1a3f-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1a3f-141">In Global Catalog</span></span>      | <span data-ttu-id="a1a3f-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-142">False</span></span>                                        |
| <span data-ttu-id="a1a3f-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1a3f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a3f-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1a3f-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1a3f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a3f-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a3f-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-147">Search-Flags</span></span>           | <span data-ttu-id="a1a3f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1a3f-148">0x00000000</span></span>                                   |
| <span data-ttu-id="a1a3f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-149">System-Flags</span></span>           | <span data-ttu-id="a1a3f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1a3f-150">0x00000010</span></span>                                   |
| <span data-ttu-id="a1a3f-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1a3f-151">Classes used in</span></span>        | [<span data-ttu-id="a1a3f-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1a3f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1a3f-153">Windows Server 2003</span></span>



| <span data-ttu-id="a1a3f-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-154">Entry</span></span> | <span data-ttu-id="a1a3f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1a3f-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1a3f-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a3f-158">System-Only</span></span>            | <span data-ttu-id="a1a3f-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-159">False</span></span>                                        |
| <span data-ttu-id="a1a3f-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1a3f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a3f-161">True</span><span class="sxs-lookup"><span data-stu-id="a1a3f-161">True</span></span>                                         |
| <span data-ttu-id="a1a3f-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1a3f-162">Is Indexed</span></span>             | <span data-ttu-id="a1a3f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-163">False</span></span>                                        |
| <span data-ttu-id="a1a3f-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1a3f-164">In Global Catalog</span></span>      | <span data-ttu-id="a1a3f-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-165">False</span></span>                                        |
| <span data-ttu-id="a1a3f-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1a3f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a3f-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1a3f-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1a3f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a3f-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a3f-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-170">Search-Flags</span></span>           | <span data-ttu-id="a1a3f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1a3f-171">0x00000000</span></span>                                   |
| <span data-ttu-id="a1a3f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-172">System-Flags</span></span>           | <span data-ttu-id="a1a3f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1a3f-173">0x00000010</span></span>                                   |
| <span data-ttu-id="a1a3f-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1a3f-174">Classes used in</span></span>        | [<span data-ttu-id="a1a3f-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1a3f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1a3f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1a3f-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-177">Entry</span></span> | <span data-ttu-id="a1a3f-178">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1a3f-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1a3f-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a3f-181">System-Only</span></span>            | <span data-ttu-id="a1a3f-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-182">False</span></span>                                        |
| <span data-ttu-id="a1a3f-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1a3f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a3f-184">True</span><span class="sxs-lookup"><span data-stu-id="a1a3f-184">True</span></span>                                         |
| <span data-ttu-id="a1a3f-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1a3f-185">Is Indexed</span></span>             | <span data-ttu-id="a1a3f-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-186">False</span></span>                                        |
| <span data-ttu-id="a1a3f-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1a3f-187">In Global Catalog</span></span>      | <span data-ttu-id="a1a3f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-188">False</span></span>                                        |
| <span data-ttu-id="a1a3f-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1a3f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a3f-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1a3f-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1a3f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a3f-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a3f-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-193">Search-Flags</span></span>           | <span data-ttu-id="a1a3f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1a3f-194">0x00000000</span></span>                                   |
| <span data-ttu-id="a1a3f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-195">System-Flags</span></span>           | <span data-ttu-id="a1a3f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1a3f-196">0x00000010</span></span>                                   |
| <span data-ttu-id="a1a3f-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1a3f-197">Classes used in</span></span>        | [<span data-ttu-id="a1a3f-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1a3f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1a3f-199">Windows Server 2008</span></span>



| <span data-ttu-id="a1a3f-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-200">Entry</span></span> | <span data-ttu-id="a1a3f-201">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1a3f-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1a3f-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a3f-204">System-Only</span></span>            | <span data-ttu-id="a1a3f-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-205">False</span></span>                                        |
| <span data-ttu-id="a1a3f-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1a3f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a3f-207">True</span><span class="sxs-lookup"><span data-stu-id="a1a3f-207">True</span></span>                                         |
| <span data-ttu-id="a1a3f-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1a3f-208">Is Indexed</span></span>             | <span data-ttu-id="a1a3f-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-209">False</span></span>                                        |
| <span data-ttu-id="a1a3f-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1a3f-210">In Global Catalog</span></span>      | <span data-ttu-id="a1a3f-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-211">False</span></span>                                        |
| <span data-ttu-id="a1a3f-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1a3f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a3f-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1a3f-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1a3f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a3f-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a3f-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-216">Search-Flags</span></span>           | <span data-ttu-id="a1a3f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1a3f-217">0x00000000</span></span>                                   |
| <span data-ttu-id="a1a3f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-218">System-Flags</span></span>           | <span data-ttu-id="a1a3f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1a3f-219">0x00000010</span></span>                                   |
| <span data-ttu-id="a1a3f-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1a3f-220">Classes used in</span></span>        | [<span data-ttu-id="a1a3f-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1a3f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1a3f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1a3f-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-223">Entry</span></span> | <span data-ttu-id="a1a3f-224">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1a3f-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1a3f-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a3f-227">System-Only</span></span>            | <span data-ttu-id="a1a3f-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-228">False</span></span>                                        |
| <span data-ttu-id="a1a3f-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1a3f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a3f-230">True</span><span class="sxs-lookup"><span data-stu-id="a1a3f-230">True</span></span>                                         |
| <span data-ttu-id="a1a3f-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1a3f-231">Is Indexed</span></span>             | <span data-ttu-id="a1a3f-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-232">False</span></span>                                        |
| <span data-ttu-id="a1a3f-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1a3f-233">In Global Catalog</span></span>      | <span data-ttu-id="a1a3f-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-234">False</span></span>                                        |
| <span data-ttu-id="a1a3f-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1a3f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a3f-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1a3f-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1a3f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a3f-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a3f-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-239">Search-Flags</span></span>           | <span data-ttu-id="a1a3f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1a3f-240">0x00000000</span></span>                                   |
| <span data-ttu-id="a1a3f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-241">System-Flags</span></span>           | <span data-ttu-id="a1a3f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1a3f-242">0x00000010</span></span>                                   |
| <span data-ttu-id="a1a3f-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1a3f-243">Classes used in</span></span>        | [<span data-ttu-id="a1a3f-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1a3f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1a3f-245">Windows Server 2012</span></span>



| <span data-ttu-id="a1a3f-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="a1a3f-246">Entry</span></span> | <span data-ttu-id="a1a3f-247">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a3f-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1a3f-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a1a3f-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a3f-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1a3f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a3f-250">System-Only</span></span>            | <span data-ttu-id="a1a3f-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-251">False</span></span>                                        |
| <span data-ttu-id="a1a3f-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a1a3f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a3f-253">True</span><span class="sxs-lookup"><span data-stu-id="a1a3f-253">True</span></span>                                         |
| <span data-ttu-id="a1a3f-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a1a3f-254">Is Indexed</span></span>             | <span data-ttu-id="a1a3f-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-255">False</span></span>                                        |
| <span data-ttu-id="a1a3f-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a1a3f-256">In Global Catalog</span></span>      | <span data-ttu-id="a1a3f-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="a1a3f-257">False</span></span>                                        |
| <span data-ttu-id="a1a3f-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a1a3f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a3f-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a1a3f-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1a3f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a3f-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a3f-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1a3f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-262">Search-Flags</span></span>           | <span data-ttu-id="a1a3f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1a3f-263">0x00000000</span></span>                                   |
| <span data-ttu-id="a1a3f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a3f-264">System-Flags</span></span>           | <span data-ttu-id="a1a3f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1a3f-265">0x00000010</span></span>                                   |
| <span data-ttu-id="a1a3f-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a1a3f-266">Classes used in</span></span>        | [<span data-ttu-id="a1a3f-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="a1a3f-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





