---
title: Атрибут ms-DS-AZ-Domain-timeout
description: Время в миллисекундах, после которого домен будет недоступен и до повторной попытки.
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени ожидания в домене MS-DS-AZ-domain
- Схема AD атрибута msDS-Аздомаинтимеаут
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893529"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="09cb6-105">Атрибут ms-DS-AZ-Domain-timeout</span><span class="sxs-lookup"><span data-stu-id="09cb6-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="09cb6-106">Время в миллисекундах, после которого домен будет недоступен и до повторной попытки.</span><span class="sxs-lookup"><span data-stu-id="09cb6-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="09cb6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="09cb6-107">Entry</span></span> | <span data-ttu-id="09cb6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="09cb6-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="09cb6-109">CN</span><span class="sxs-lookup"><span data-stu-id="09cb6-109">CN</span></span>                | <span data-ttu-id="09cb6-110">MS-DS-AZ-Domain-timeout</span><span class="sxs-lookup"><span data-stu-id="09cb6-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="09cb6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="09cb6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="09cb6-112">msDS-Аздомаинтимеаут</span><span class="sxs-lookup"><span data-stu-id="09cb6-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="09cb6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="09cb6-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="09cb6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="09cb6-114">Update Privilege</span></span>  | <span data-ttu-id="09cb6-115">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="09cb6-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="09cb6-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="09cb6-116">Update Frequency</span></span>  | <span data-ttu-id="09cb6-117">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="09cb6-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="09cb6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09cb6-118">Attribute-Id</span></span>      | <span data-ttu-id="09cb6-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="09cb6-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="09cb6-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="09cb6-120">System-Id-Guid</span></span>    | <span data-ttu-id="09cb6-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="09cb6-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="09cb6-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09cb6-122">Syntax</span></span>            | [<span data-ttu-id="09cb6-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="09cb6-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="09cb6-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="09cb6-124">Implementations</span></span>

-   [<span data-ttu-id="09cb6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09cb6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09cb6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09cb6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09cb6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09cb6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09cb6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09cb6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09cb6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09cb6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="09cb6-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09cb6-130">Windows Server 2003</span></span>



| <span data-ttu-id="09cb6-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="09cb6-131">Entry</span></span> | <span data-ttu-id="09cb6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="09cb6-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="09cb6-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09cb6-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09cb6-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="09cb6-135">System-Only</span></span>            | <span data-ttu-id="09cb6-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-136">False</span></span>                                                              |
| <span data-ttu-id="09cb6-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09cb6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="09cb6-138">True</span><span class="sxs-lookup"><span data-stu-id="09cb6-138">True</span></span>                                                               |
| <span data-ttu-id="09cb6-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09cb6-139">Is Indexed</span></span>             | <span data-ttu-id="09cb6-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-140">False</span></span>                                                              |
| <span data-ttu-id="09cb6-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09cb6-141">In Global Catalog</span></span>      | <span data-ttu-id="09cb6-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-142">False</span></span>                                                              |
| <span data-ttu-id="09cb6-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09cb6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="09cb6-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09cb6-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="09cb6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09cb6-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09cb6-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-147">Search-Flags</span></span>           | <span data-ttu-id="09cb6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09cb6-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="09cb6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-149">System-Flags</span></span>           | <span data-ttu-id="09cb6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09cb6-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="09cb6-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09cb6-151">Classes used in</span></span>        | [<span data-ttu-id="09cb6-152">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="09cb6-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09cb6-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09cb6-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09cb6-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="09cb6-154">Entry</span></span> | <span data-ttu-id="09cb6-155">Значение</span><span class="sxs-lookup"><span data-stu-id="09cb6-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="09cb6-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09cb6-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09cb6-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="09cb6-158">System-Only</span></span>            | <span data-ttu-id="09cb6-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-159">False</span></span>                                                              |
| <span data-ttu-id="09cb6-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09cb6-160">Is-Single-Valued</span></span>       | <span data-ttu-id="09cb6-161">True</span><span class="sxs-lookup"><span data-stu-id="09cb6-161">True</span></span>                                                               |
| <span data-ttu-id="09cb6-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09cb6-162">Is Indexed</span></span>             | <span data-ttu-id="09cb6-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-163">False</span></span>                                                              |
| <span data-ttu-id="09cb6-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09cb6-164">In Global Catalog</span></span>      | <span data-ttu-id="09cb6-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-165">False</span></span>                                                              |
| <span data-ttu-id="09cb6-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09cb6-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="09cb6-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09cb6-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="09cb6-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09cb6-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09cb6-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-170">Search-Flags</span></span>           | <span data-ttu-id="09cb6-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09cb6-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="09cb6-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-172">System-Flags</span></span>           | <span data-ttu-id="09cb6-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09cb6-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="09cb6-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09cb6-174">Classes used in</span></span>        | [<span data-ttu-id="09cb6-175">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="09cb6-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09cb6-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09cb6-176">Windows Server 2008</span></span>



| <span data-ttu-id="09cb6-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="09cb6-177">Entry</span></span> | <span data-ttu-id="09cb6-178">Значение</span><span class="sxs-lookup"><span data-stu-id="09cb6-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="09cb6-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09cb6-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09cb6-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="09cb6-181">System-Only</span></span>            | <span data-ttu-id="09cb6-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-182">False</span></span>                                                              |
| <span data-ttu-id="09cb6-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09cb6-183">Is-Single-Valued</span></span>       | <span data-ttu-id="09cb6-184">True</span><span class="sxs-lookup"><span data-stu-id="09cb6-184">True</span></span>                                                               |
| <span data-ttu-id="09cb6-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09cb6-185">Is Indexed</span></span>             | <span data-ttu-id="09cb6-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-186">False</span></span>                                                              |
| <span data-ttu-id="09cb6-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09cb6-187">In Global Catalog</span></span>      | <span data-ttu-id="09cb6-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-188">False</span></span>                                                              |
| <span data-ttu-id="09cb6-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09cb6-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="09cb6-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09cb6-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="09cb6-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09cb6-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09cb6-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-193">Search-Flags</span></span>           | <span data-ttu-id="09cb6-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09cb6-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="09cb6-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-195">System-Flags</span></span>           | <span data-ttu-id="09cb6-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09cb6-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="09cb6-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09cb6-197">Classes used in</span></span>        | [<span data-ttu-id="09cb6-198">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="09cb6-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09cb6-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09cb6-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09cb6-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="09cb6-200">Entry</span></span> | <span data-ttu-id="09cb6-201">Значение</span><span class="sxs-lookup"><span data-stu-id="09cb6-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="09cb6-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09cb6-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09cb6-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="09cb6-204">System-Only</span></span>            | <span data-ttu-id="09cb6-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-205">False</span></span>                                                              |
| <span data-ttu-id="09cb6-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09cb6-206">Is-Single-Valued</span></span>       | <span data-ttu-id="09cb6-207">True</span><span class="sxs-lookup"><span data-stu-id="09cb6-207">True</span></span>                                                               |
| <span data-ttu-id="09cb6-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09cb6-208">Is Indexed</span></span>             | <span data-ttu-id="09cb6-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-209">False</span></span>                                                              |
| <span data-ttu-id="09cb6-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09cb6-210">In Global Catalog</span></span>      | <span data-ttu-id="09cb6-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-211">False</span></span>                                                              |
| <span data-ttu-id="09cb6-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09cb6-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="09cb6-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09cb6-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="09cb6-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09cb6-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09cb6-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-216">Search-Flags</span></span>           | <span data-ttu-id="09cb6-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09cb6-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="09cb6-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-218">System-Flags</span></span>           | <span data-ttu-id="09cb6-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09cb6-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="09cb6-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09cb6-220">Classes used in</span></span>        | [<span data-ttu-id="09cb6-221">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="09cb6-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09cb6-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09cb6-222">Windows Server 2012</span></span>



| <span data-ttu-id="09cb6-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="09cb6-223">Entry</span></span> | <span data-ttu-id="09cb6-224">Значение</span><span class="sxs-lookup"><span data-stu-id="09cb6-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="09cb6-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09cb6-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09cb6-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="09cb6-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="09cb6-227">System-Only</span></span>            | <span data-ttu-id="09cb6-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-228">False</span></span>                                                              |
| <span data-ttu-id="09cb6-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09cb6-229">Is-Single-Valued</span></span>       | <span data-ttu-id="09cb6-230">True</span><span class="sxs-lookup"><span data-stu-id="09cb6-230">True</span></span>                                                               |
| <span data-ttu-id="09cb6-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09cb6-231">Is Indexed</span></span>             | <span data-ttu-id="09cb6-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-232">False</span></span>                                                              |
| <span data-ttu-id="09cb6-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09cb6-233">In Global Catalog</span></span>      | <span data-ttu-id="09cb6-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="09cb6-234">False</span></span>                                                              |
| <span data-ttu-id="09cb6-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09cb6-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="09cb6-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09cb6-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="09cb6-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09cb6-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09cb6-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="09cb6-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-239">Search-Flags</span></span>           | <span data-ttu-id="09cb6-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09cb6-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="09cb6-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09cb6-241">System-Flags</span></span>           | <span data-ttu-id="09cb6-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09cb6-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="09cb6-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09cb6-243">Classes used in</span></span>        | [<span data-ttu-id="09cb6-244">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="09cb6-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





