---
title: ACS-Service-тип — атрибут
description: Тип службы ACS. Управляемая нагрузка или гарантированная пропускная способность.
ms.assetid: 3de23f2b-16dc-48c0-a8c5-e3130cd84ba8
ms.tgt_platform: multiple
keywords:
- ACS — схема AD атрибута Service-Type
- Схема AD атрибута Акссервицетипе
topic_type:
- apiref
api_name:
- ACS-Service-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b7dc97c17e9f7b38fa2f6f0ea863099bbef838a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138322"
---
# <a name="acs-service-type-attribute"></a><span data-ttu-id="51db7-106">ACS-Service-тип — атрибут</span><span class="sxs-lookup"><span data-stu-id="51db7-106">ACS-Service-Type attribute</span></span>

<span data-ttu-id="51db7-107">Тип службы ACS.</span><span class="sxs-lookup"><span data-stu-id="51db7-107">The ACS service type.</span></span> <span data-ttu-id="51db7-108">Управляемая нагрузка или гарантированная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="51db7-108">Controlled load or guaranteed bandwidth.</span></span>



| <span data-ttu-id="51db7-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-109">Entry</span></span> | <span data-ttu-id="51db7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="51db7-111">CN</span><span class="sxs-lookup"><span data-stu-id="51db7-111">CN</span></span>                | <span data-ttu-id="51db7-112">ACS-Service-Type</span><span class="sxs-lookup"><span data-stu-id="51db7-112">ACS-Service-Type</span></span>                     |
| <span data-ttu-id="51db7-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="51db7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="51db7-114">акссервицетипе</span><span class="sxs-lookup"><span data-stu-id="51db7-114">aCSServiceType</span></span>                       |
| <span data-ttu-id="51db7-115">Размер</span><span class="sxs-lookup"><span data-stu-id="51db7-115">Size</span></span>              | <span data-ttu-id="51db7-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="51db7-116">4 bytes</span></span>                              |
| <span data-ttu-id="51db7-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="51db7-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="51db7-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="51db7-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="51db7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-119">Attribute-Id</span></span>      | <span data-ttu-id="51db7-120">1.2.840.113556.1.4.762</span><span class="sxs-lookup"><span data-stu-id="51db7-120">1.2.840.113556.1.4.762</span></span>               |
| <span data-ttu-id="51db7-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="51db7-121">System-Id-Guid</span></span>    | <span data-ttu-id="51db7-122">7f56127f-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="51db7-122">7f56127f-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="51db7-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51db7-123">Syntax</span></span>            | [<span data-ttu-id="51db7-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="51db7-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="51db7-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="51db7-125">Implementations</span></span>

-   [<span data-ttu-id="51db7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51db7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51db7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51db7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51db7-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51db7-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51db7-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51db7-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51db7-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51db7-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51db7-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51db7-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51db7-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51db7-132">Windows 2000 Server</span></span>



| <span data-ttu-id="51db7-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-133">Entry</span></span> | <span data-ttu-id="51db7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51db7-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51db7-135">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-136">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="51db7-137">System-Only</span></span>            | <span data-ttu-id="51db7-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-138">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51db7-139">Is-Single-Valued</span></span>       | <span data-ttu-id="51db7-140">True</span><span class="sxs-lookup"><span data-stu-id="51db7-140">True</span></span>                                                                                                       |
| <span data-ttu-id="51db7-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51db7-141">Is Indexed</span></span>             | <span data-ttu-id="51db7-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-142">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51db7-143">In Global Catalog</span></span>      | <span data-ttu-id="51db7-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-144">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51db7-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="51db7-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51db7-146">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="51db7-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51db7-147">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51db7-148">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-149">Search-Flags</span></span>           | <span data-ttu-id="51db7-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51db7-150">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="51db7-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-151">System-Flags</span></span>           | <span data-ttu-id="51db7-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51db7-152">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="51db7-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51db7-153">Classes used in</span></span>        | [<span data-ttu-id="51db7-154">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="51db7-154">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="51db7-155">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="51db7-155">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51db7-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51db7-156">Windows Server 2003</span></span>



| <span data-ttu-id="51db7-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-157">Entry</span></span> | <span data-ttu-id="51db7-158">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51db7-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51db7-159">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-160">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="51db7-161">System-Only</span></span>            | <span data-ttu-id="51db7-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-162">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51db7-163">Is-Single-Valued</span></span>       | <span data-ttu-id="51db7-164">True</span><span class="sxs-lookup"><span data-stu-id="51db7-164">True</span></span>                                                                                                       |
| <span data-ttu-id="51db7-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51db7-165">Is Indexed</span></span>             | <span data-ttu-id="51db7-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-166">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51db7-167">In Global Catalog</span></span>      | <span data-ttu-id="51db7-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-168">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51db7-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="51db7-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51db7-170">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="51db7-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51db7-171">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51db7-172">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-173">Search-Flags</span></span>           | <span data-ttu-id="51db7-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51db7-174">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="51db7-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-175">System-Flags</span></span>           | <span data-ttu-id="51db7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51db7-176">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="51db7-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51db7-177">Classes used in</span></span>        | [<span data-ttu-id="51db7-178">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="51db7-178">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="51db7-179">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="51db7-179">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51db7-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51db7-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51db7-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-181">Entry</span></span> | <span data-ttu-id="51db7-182">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51db7-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51db7-183">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-184">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="51db7-185">System-Only</span></span>            | <span data-ttu-id="51db7-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-186">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51db7-187">Is-Single-Valued</span></span>       | <span data-ttu-id="51db7-188">True</span><span class="sxs-lookup"><span data-stu-id="51db7-188">True</span></span>                                                                                                       |
| <span data-ttu-id="51db7-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51db7-189">Is Indexed</span></span>             | <span data-ttu-id="51db7-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-190">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51db7-191">In Global Catalog</span></span>      | <span data-ttu-id="51db7-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-192">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51db7-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="51db7-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51db7-194">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="51db7-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51db7-195">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51db7-196">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-197">Search-Flags</span></span>           | <span data-ttu-id="51db7-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51db7-198">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="51db7-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-199">System-Flags</span></span>           | <span data-ttu-id="51db7-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51db7-200">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="51db7-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51db7-201">Classes used in</span></span>        | [<span data-ttu-id="51db7-202">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="51db7-202">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="51db7-203">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="51db7-203">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51db7-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51db7-204">Windows Server 2008</span></span>



| <span data-ttu-id="51db7-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-205">Entry</span></span> | <span data-ttu-id="51db7-206">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51db7-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51db7-207">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-208">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="51db7-209">System-Only</span></span>            | <span data-ttu-id="51db7-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-210">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51db7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="51db7-212">True</span><span class="sxs-lookup"><span data-stu-id="51db7-212">True</span></span>                                                                                                       |
| <span data-ttu-id="51db7-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51db7-213">Is Indexed</span></span>             | <span data-ttu-id="51db7-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-214">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51db7-215">In Global Catalog</span></span>      | <span data-ttu-id="51db7-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-216">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51db7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="51db7-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51db7-218">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="51db7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51db7-219">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51db7-220">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-221">Search-Flags</span></span>           | <span data-ttu-id="51db7-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51db7-222">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="51db7-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-223">System-Flags</span></span>           | <span data-ttu-id="51db7-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51db7-224">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="51db7-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51db7-225">Classes used in</span></span>        | [<span data-ttu-id="51db7-226">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="51db7-226">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="51db7-227">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="51db7-227">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51db7-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51db7-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51db7-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-229">Entry</span></span> | <span data-ttu-id="51db7-230">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51db7-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51db7-231">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-232">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="51db7-233">System-Only</span></span>            | <span data-ttu-id="51db7-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-234">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51db7-235">Is-Single-Valued</span></span>       | <span data-ttu-id="51db7-236">True</span><span class="sxs-lookup"><span data-stu-id="51db7-236">True</span></span>                                                                                                       |
| <span data-ttu-id="51db7-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51db7-237">Is Indexed</span></span>             | <span data-ttu-id="51db7-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-238">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51db7-239">In Global Catalog</span></span>      | <span data-ttu-id="51db7-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-240">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51db7-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="51db7-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51db7-242">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="51db7-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51db7-243">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51db7-244">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-245">Search-Flags</span></span>           | <span data-ttu-id="51db7-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51db7-246">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="51db7-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-247">System-Flags</span></span>           | <span data-ttu-id="51db7-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51db7-248">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="51db7-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51db7-249">Classes used in</span></span>        | [<span data-ttu-id="51db7-250">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="51db7-250">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="51db7-251">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="51db7-251">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51db7-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51db7-252">Windows Server 2012</span></span>



| <span data-ttu-id="51db7-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="51db7-253">Entry</span></span> | <span data-ttu-id="51db7-254">Значение</span><span class="sxs-lookup"><span data-stu-id="51db7-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51db7-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51db7-255">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51db7-256">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="51db7-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="51db7-257">System-Only</span></span>            | <span data-ttu-id="51db7-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-258">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51db7-259">Is-Single-Valued</span></span>       | <span data-ttu-id="51db7-260">True</span><span class="sxs-lookup"><span data-stu-id="51db7-260">True</span></span>                                                                                                       |
| <span data-ttu-id="51db7-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51db7-261">Is Indexed</span></span>             | <span data-ttu-id="51db7-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-262">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51db7-263">In Global Catalog</span></span>      | <span data-ttu-id="51db7-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="51db7-264">False</span></span>                                                                                                      |
| <span data-ttu-id="51db7-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51db7-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="51db7-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51db7-266">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="51db7-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51db7-267">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51db7-268">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="51db7-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-269">Search-Flags</span></span>           | <span data-ttu-id="51db7-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51db7-270">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="51db7-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51db7-271">System-Flags</span></span>           | <span data-ttu-id="51db7-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51db7-272">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="51db7-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51db7-273">Classes used in</span></span>        | [<span data-ttu-id="51db7-274">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="51db7-274">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="51db7-275">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="51db7-275">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



 

 





