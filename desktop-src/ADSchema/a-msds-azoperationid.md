---
title: Атрибут ms-DS-AZ-Operation-ID
description: Идентификатор, зависящий от приложения, который делает операцию уникальной для приложения.
ms.assetid: 0d0fc8ce-7044-481a-8df2-489e33264412
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-AZ-Operation-ID
- Схема AD атрибута msDS-Азоператионид
topic_type:
- apiref
api_name:
- ms-DS-Az-Operation-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58cc05338fa3960185a795422c62256a63e6f1ca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262254"
---
# <a name="ms-ds-az-operation-id-attribute"></a><span data-ttu-id="3b180-105">Атрибут ms-DS-AZ-Operation-ID</span><span class="sxs-lookup"><span data-stu-id="3b180-105">ms-DS-Az-Operation-ID attribute</span></span>

<span data-ttu-id="3b180-106">Идентификатор, зависящий от приложения, который делает операцию уникальной для приложения.</span><span class="sxs-lookup"><span data-stu-id="3b180-106">An application specific ID that makes the operation unique to the application.</span></span>



| <span data-ttu-id="3b180-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3b180-107">Entry</span></span> | <span data-ttu-id="3b180-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3b180-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3b180-109">CN</span><span class="sxs-lookup"><span data-stu-id="3b180-109">CN</span></span>                | <span data-ttu-id="3b180-110">MS-DS-AZ-Operation-ID</span><span class="sxs-lookup"><span data-stu-id="3b180-110">ms-DS-Az-Operation-ID</span></span>                   |
| <span data-ttu-id="3b180-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3b180-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3b180-112">msDS-Азоператионид</span><span class="sxs-lookup"><span data-stu-id="3b180-112">msDS-AzOperationID</span></span>                      |
| <span data-ttu-id="3b180-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3b180-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="3b180-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3b180-114">Update Privilege</span></span>  | <span data-ttu-id="3b180-115">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="3b180-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="3b180-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3b180-116">Update Frequency</span></span>  | <span data-ttu-id="3b180-117">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="3b180-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="3b180-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3b180-118">Attribute-Id</span></span>      | <span data-ttu-id="3b180-119">1.2.840.113556.1.4.1800</span><span class="sxs-lookup"><span data-stu-id="3b180-119">1.2.840.113556.1.4.1800</span></span>                 |
| <span data-ttu-id="3b180-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3b180-120">System-Id-Guid</span></span>    | <span data-ttu-id="3b180-121">a5f3b553-5d76-4cbe-ba3f-4312152cab18</span><span class="sxs-lookup"><span data-stu-id="3b180-121">a5f3b553-5d76-4cbe-ba3f-4312152cab18</span></span>    |
| <span data-ttu-id="3b180-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b180-122">Syntax</span></span>            | [<span data-ttu-id="3b180-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="3b180-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="3b180-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3b180-124">Implementations</span></span>

-   [<span data-ttu-id="3b180-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3b180-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3b180-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3b180-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3b180-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3b180-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3b180-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3b180-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3b180-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3b180-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3b180-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b180-130">Windows Server 2003</span></span>



| <span data-ttu-id="3b180-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="3b180-131">Entry</span></span> | <span data-ttu-id="3b180-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3b180-132">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3b180-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3b180-133">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b180-134">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b180-135">System-Only</span></span>            | <span data-ttu-id="3b180-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-136">False</span></span>        |
| <span data-ttu-id="3b180-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3b180-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3b180-138">True</span><span class="sxs-lookup"><span data-stu-id="3b180-138">True</span></span>         |
| <span data-ttu-id="3b180-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3b180-139">Is Indexed</span></span>             | <span data-ttu-id="3b180-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-140">False</span></span>        |
| <span data-ttu-id="3b180-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3b180-141">In Global Catalog</span></span>      | <span data-ttu-id="3b180-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-142">False</span></span>        |
| <span data-ttu-id="3b180-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3b180-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b180-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b180-144">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3b180-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b180-145">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3b180-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b180-146">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3b180-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-147">Search-Flags</span></span>           | <span data-ttu-id="3b180-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b180-148">0x00000000</span></span>   |
| <span data-ttu-id="3b180-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-149">System-Flags</span></span>           | <span data-ttu-id="3b180-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b180-150">0x00000010</span></span>   |
| <span data-ttu-id="3b180-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3b180-151">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3b180-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3b180-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3b180-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="3b180-153">Entry</span></span> | <span data-ttu-id="3b180-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3b180-154">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3b180-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3b180-155">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b180-156">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b180-157">System-Only</span></span>            | <span data-ttu-id="3b180-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-158">False</span></span>        |
| <span data-ttu-id="3b180-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3b180-159">Is-Single-Valued</span></span>       | <span data-ttu-id="3b180-160">True</span><span class="sxs-lookup"><span data-stu-id="3b180-160">True</span></span>         |
| <span data-ttu-id="3b180-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3b180-161">Is Indexed</span></span>             | <span data-ttu-id="3b180-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-162">False</span></span>        |
| <span data-ttu-id="3b180-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3b180-163">In Global Catalog</span></span>      | <span data-ttu-id="3b180-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-164">False</span></span>        |
| <span data-ttu-id="3b180-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3b180-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b180-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b180-166">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3b180-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b180-167">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3b180-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b180-168">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3b180-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-169">Search-Flags</span></span>           | <span data-ttu-id="3b180-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b180-170">0x00000000</span></span>   |
| <span data-ttu-id="3b180-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-171">System-Flags</span></span>           | <span data-ttu-id="3b180-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b180-172">0x00000010</span></span>   |
| <span data-ttu-id="3b180-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3b180-173">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="3b180-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b180-174">Windows Server 2008</span></span>



| <span data-ttu-id="3b180-175">Ввод</span><span class="sxs-lookup"><span data-stu-id="3b180-175">Entry</span></span> | <span data-ttu-id="3b180-176">Значение</span><span class="sxs-lookup"><span data-stu-id="3b180-176">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3b180-177">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3b180-177">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b180-178">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b180-179">System-Only</span></span>            | <span data-ttu-id="3b180-180">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-180">False</span></span>        |
| <span data-ttu-id="3b180-181">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3b180-181">Is-Single-Valued</span></span>       | <span data-ttu-id="3b180-182">True</span><span class="sxs-lookup"><span data-stu-id="3b180-182">True</span></span>         |
| <span data-ttu-id="3b180-183">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3b180-183">Is Indexed</span></span>             | <span data-ttu-id="3b180-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-184">False</span></span>        |
| <span data-ttu-id="3b180-185">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3b180-185">In Global Catalog</span></span>      | <span data-ttu-id="3b180-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-186">False</span></span>        |
| <span data-ttu-id="3b180-187">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3b180-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b180-188">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b180-188">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3b180-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b180-189">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3b180-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b180-190">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3b180-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-191">Search-Flags</span></span>           | <span data-ttu-id="3b180-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b180-192">0x00000000</span></span>   |
| <span data-ttu-id="3b180-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-193">System-Flags</span></span>           | <span data-ttu-id="3b180-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b180-194">0x00000010</span></span>   |
| <span data-ttu-id="3b180-195">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3b180-195">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3b180-196">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b180-196">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3b180-197">Ввод</span><span class="sxs-lookup"><span data-stu-id="3b180-197">Entry</span></span> | <span data-ttu-id="3b180-198">Значение</span><span class="sxs-lookup"><span data-stu-id="3b180-198">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3b180-199">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3b180-199">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b180-200">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b180-201">System-Only</span></span>            | <span data-ttu-id="3b180-202">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-202">False</span></span>        |
| <span data-ttu-id="3b180-203">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3b180-203">Is-Single-Valued</span></span>       | <span data-ttu-id="3b180-204">True</span><span class="sxs-lookup"><span data-stu-id="3b180-204">True</span></span>         |
| <span data-ttu-id="3b180-205">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3b180-205">Is Indexed</span></span>             | <span data-ttu-id="3b180-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-206">False</span></span>        |
| <span data-ttu-id="3b180-207">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3b180-207">In Global Catalog</span></span>      | <span data-ttu-id="3b180-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-208">False</span></span>        |
| <span data-ttu-id="3b180-209">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3b180-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b180-210">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b180-210">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3b180-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b180-211">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3b180-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b180-212">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3b180-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-213">Search-Flags</span></span>           | <span data-ttu-id="3b180-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b180-214">0x00000000</span></span>   |
| <span data-ttu-id="3b180-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-215">System-Flags</span></span>           | <span data-ttu-id="3b180-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b180-216">0x00000010</span></span>   |
| <span data-ttu-id="3b180-217">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3b180-217">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="3b180-218">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b180-218">Windows Server 2012</span></span>



| <span data-ttu-id="3b180-219">Ввод</span><span class="sxs-lookup"><span data-stu-id="3b180-219">Entry</span></span> | <span data-ttu-id="3b180-220">Значение</span><span class="sxs-lookup"><span data-stu-id="3b180-220">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3b180-221">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3b180-221">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-222">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b180-222">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3b180-223">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b180-223">System-Only</span></span>            | <span data-ttu-id="3b180-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-224">False</span></span>        |
| <span data-ttu-id="3b180-225">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3b180-225">Is-Single-Valued</span></span>       | <span data-ttu-id="3b180-226">True</span><span class="sxs-lookup"><span data-stu-id="3b180-226">True</span></span>         |
| <span data-ttu-id="3b180-227">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3b180-227">Is Indexed</span></span>             | <span data-ttu-id="3b180-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-228">False</span></span>        |
| <span data-ttu-id="3b180-229">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3b180-229">In Global Catalog</span></span>      | <span data-ttu-id="3b180-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="3b180-230">False</span></span>        |
| <span data-ttu-id="3b180-231">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3b180-231">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b180-232">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b180-232">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3b180-233">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b180-233">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3b180-234">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b180-234">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3b180-235">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-235">Search-Flags</span></span>           | <span data-ttu-id="3b180-236">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b180-236">0x00000000</span></span>   |
| <span data-ttu-id="3b180-237">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b180-237">System-Flags</span></span>           | <span data-ttu-id="3b180-238">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b180-238">0x00000010</span></span>   |
| <span data-ttu-id="3b180-239">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3b180-239">Classes used in</span></span>        | \-           |



 

 




