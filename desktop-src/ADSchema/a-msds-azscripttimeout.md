---
title: Атрибут ms-DS-AZ-Script-timeout
description: Максимальное время ожидания скриптом завершения аудита определенной политики (в миллисекундах).
ms.assetid: 166d87a3-8768-42d9-9041-21f272059fbf
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени ожидания MS-DS-AZ-Script-timeout
- Схема AD атрибута msDS-Азскрипттимеаут
topic_type:
- apiref
api_name:
- ms-DS-Az-Script-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67de4230c3f4710a3eefe6edab896d4fcadcb91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416336"
---
# <a name="ms-ds-az-script-timeout-attribute"></a><span data-ttu-id="93d0b-105">Атрибут ms-DS-AZ-Script-timeout</span><span class="sxs-lookup"><span data-stu-id="93d0b-105">ms-DS-Az-Script-Timeout attribute</span></span>

<span data-ttu-id="93d0b-106">Максимальное время ожидания скриптом завершения аудита определенной политики (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="93d0b-106">The maximum time, in milliseconds, to wait for a script to finish auditing a specific policy.</span></span>



| <span data-ttu-id="93d0b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="93d0b-107">Entry</span></span> | <span data-ttu-id="93d0b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="93d0b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="93d0b-109">CN</span><span class="sxs-lookup"><span data-stu-id="93d0b-109">CN</span></span>                | <span data-ttu-id="93d0b-110">MS-DS-AZ-Script-timeout</span><span class="sxs-lookup"><span data-stu-id="93d0b-110">ms-DS-Az-Script-Timeout</span></span>                 |
| <span data-ttu-id="93d0b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="93d0b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="93d0b-112">msDS-Азскрипттимеаут</span><span class="sxs-lookup"><span data-stu-id="93d0b-112">msDS-AzScriptTimeout</span></span>                    |
| <span data-ttu-id="93d0b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="93d0b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="93d0b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="93d0b-114">Update Privilege</span></span>  | <span data-ttu-id="93d0b-115">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="93d0b-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="93d0b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="93d0b-116">Update Frequency</span></span>  | <span data-ttu-id="93d0b-117">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="93d0b-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="93d0b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93d0b-118">Attribute-Id</span></span>      | <span data-ttu-id="93d0b-119">1.2.840.113556.1.4.1797</span><span class="sxs-lookup"><span data-stu-id="93d0b-119">1.2.840.113556.1.4.1797</span></span>                 |
| <span data-ttu-id="93d0b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="93d0b-120">System-Id-Guid</span></span>    | <span data-ttu-id="93d0b-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span><span class="sxs-lookup"><span data-stu-id="93d0b-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span></span>    |
| <span data-ttu-id="93d0b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93d0b-122">Syntax</span></span>            | [<span data-ttu-id="93d0b-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="93d0b-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="93d0b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="93d0b-124">Implementations</span></span>

-   [<span data-ttu-id="93d0b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93d0b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93d0b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93d0b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93d0b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93d0b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93d0b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93d0b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93d0b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93d0b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="93d0b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93d0b-130">Windows Server 2003</span></span>



| <span data-ttu-id="93d0b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="93d0b-131">Entry</span></span> | <span data-ttu-id="93d0b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="93d0b-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="93d0b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93d0b-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d0b-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d0b-135">System-Only</span></span>            | <span data-ttu-id="93d0b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-136">False</span></span>                                                              |
| <span data-ttu-id="93d0b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93d0b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="93d0b-138">True</span><span class="sxs-lookup"><span data-stu-id="93d0b-138">True</span></span>                                                               |
| <span data-ttu-id="93d0b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93d0b-139">Is Indexed</span></span>             | <span data-ttu-id="93d0b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-140">False</span></span>                                                              |
| <span data-ttu-id="93d0b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93d0b-141">In Global Catalog</span></span>      | <span data-ttu-id="93d0b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-142">False</span></span>                                                              |
| <span data-ttu-id="93d0b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93d0b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d0b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d0b-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="93d0b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d0b-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d0b-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-147">Search-Flags</span></span>           | <span data-ttu-id="93d0b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d0b-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="93d0b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-149">System-Flags</span></span>           | <span data-ttu-id="93d0b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d0b-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="93d0b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93d0b-151">Classes used in</span></span>        | [<span data-ttu-id="93d0b-152">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="93d0b-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93d0b-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93d0b-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93d0b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="93d0b-154">Entry</span></span> | <span data-ttu-id="93d0b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="93d0b-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="93d0b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93d0b-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d0b-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d0b-158">System-Only</span></span>            | <span data-ttu-id="93d0b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-159">False</span></span>                                                              |
| <span data-ttu-id="93d0b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93d0b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="93d0b-161">True</span><span class="sxs-lookup"><span data-stu-id="93d0b-161">True</span></span>                                                               |
| <span data-ttu-id="93d0b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93d0b-162">Is Indexed</span></span>             | <span data-ttu-id="93d0b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-163">False</span></span>                                                              |
| <span data-ttu-id="93d0b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93d0b-164">In Global Catalog</span></span>      | <span data-ttu-id="93d0b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-165">False</span></span>                                                              |
| <span data-ttu-id="93d0b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93d0b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d0b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d0b-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="93d0b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d0b-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d0b-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-170">Search-Flags</span></span>           | <span data-ttu-id="93d0b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d0b-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="93d0b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-172">System-Flags</span></span>           | <span data-ttu-id="93d0b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d0b-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="93d0b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93d0b-174">Classes used in</span></span>        | [<span data-ttu-id="93d0b-175">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="93d0b-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93d0b-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93d0b-176">Windows Server 2008</span></span>



| <span data-ttu-id="93d0b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="93d0b-177">Entry</span></span> | <span data-ttu-id="93d0b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="93d0b-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="93d0b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93d0b-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d0b-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d0b-181">System-Only</span></span>            | <span data-ttu-id="93d0b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-182">False</span></span>                                                              |
| <span data-ttu-id="93d0b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93d0b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="93d0b-184">True</span><span class="sxs-lookup"><span data-stu-id="93d0b-184">True</span></span>                                                               |
| <span data-ttu-id="93d0b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93d0b-185">Is Indexed</span></span>             | <span data-ttu-id="93d0b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-186">False</span></span>                                                              |
| <span data-ttu-id="93d0b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93d0b-187">In Global Catalog</span></span>      | <span data-ttu-id="93d0b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-188">False</span></span>                                                              |
| <span data-ttu-id="93d0b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93d0b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d0b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d0b-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="93d0b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d0b-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d0b-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-193">Search-Flags</span></span>           | <span data-ttu-id="93d0b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d0b-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="93d0b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-195">System-Flags</span></span>           | <span data-ttu-id="93d0b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d0b-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="93d0b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93d0b-197">Classes used in</span></span>        | [<span data-ttu-id="93d0b-198">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="93d0b-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93d0b-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93d0b-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93d0b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="93d0b-200">Entry</span></span> | <span data-ttu-id="93d0b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="93d0b-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="93d0b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93d0b-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d0b-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d0b-204">System-Only</span></span>            | <span data-ttu-id="93d0b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-205">False</span></span>                                                              |
| <span data-ttu-id="93d0b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93d0b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="93d0b-207">True</span><span class="sxs-lookup"><span data-stu-id="93d0b-207">True</span></span>                                                               |
| <span data-ttu-id="93d0b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93d0b-208">Is Indexed</span></span>             | <span data-ttu-id="93d0b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-209">False</span></span>                                                              |
| <span data-ttu-id="93d0b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93d0b-210">In Global Catalog</span></span>      | <span data-ttu-id="93d0b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-211">False</span></span>                                                              |
| <span data-ttu-id="93d0b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93d0b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d0b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d0b-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="93d0b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d0b-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d0b-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-216">Search-Flags</span></span>           | <span data-ttu-id="93d0b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d0b-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="93d0b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-218">System-Flags</span></span>           | <span data-ttu-id="93d0b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d0b-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="93d0b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93d0b-220">Classes used in</span></span>        | [<span data-ttu-id="93d0b-221">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="93d0b-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93d0b-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93d0b-222">Windows Server 2012</span></span>



| <span data-ttu-id="93d0b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="93d0b-223">Entry</span></span> | <span data-ttu-id="93d0b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="93d0b-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="93d0b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="93d0b-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d0b-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="93d0b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d0b-227">System-Only</span></span>            | <span data-ttu-id="93d0b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-228">False</span></span>                                                              |
| <span data-ttu-id="93d0b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="93d0b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="93d0b-230">True</span><span class="sxs-lookup"><span data-stu-id="93d0b-230">True</span></span>                                                               |
| <span data-ttu-id="93d0b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="93d0b-231">Is Indexed</span></span>             | <span data-ttu-id="93d0b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-232">False</span></span>                                                              |
| <span data-ttu-id="93d0b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="93d0b-233">In Global Catalog</span></span>      | <span data-ttu-id="93d0b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="93d0b-234">False</span></span>                                                              |
| <span data-ttu-id="93d0b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="93d0b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d0b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d0b-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="93d0b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d0b-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d0b-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="93d0b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-239">Search-Flags</span></span>           | <span data-ttu-id="93d0b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d0b-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="93d0b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d0b-241">System-Flags</span></span>           | <span data-ttu-id="93d0b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d0b-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="93d0b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="93d0b-243">Classes used in</span></span>        | [<span data-ttu-id="93d0b-244">**MS-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="93d0b-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





