---
title: Атрибут ms-DS-AZ-Class-ID
description: Идентификатор класса, необходимый пользовательскому интерфейсу Азролес для объекта Азаппликатион.
ms.assetid: cbbdc898-82b2-410e-8c9d-ae4f9641ac1a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-AZ-Class-ID
- Схема AD атрибута msDS-Азклассид
topic_type:
- apiref
api_name:
- ms-DS-Az-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77d7ae6376deceaf23a9b7fa3c85ee8cb2b9748
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138971"
---
# <a name="ms-ds-az-class-id-attribute"></a><span data-ttu-id="51c68-105">Атрибут ms-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="51c68-105">ms-DS-Az-Class-ID attribute</span></span>

<span data-ttu-id="51c68-106">Идентификатор класса, необходимый пользовательскому интерфейсу Азролес для объекта Азаппликатион.</span><span class="sxs-lookup"><span data-stu-id="51c68-106">A class ID required by the AzRoles UI on the AzApplication object.</span></span>



| <span data-ttu-id="51c68-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="51c68-107">Entry</span></span> | <span data-ttu-id="51c68-108">Значение</span><span class="sxs-lookup"><span data-stu-id="51c68-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="51c68-109">CN</span><span class="sxs-lookup"><span data-stu-id="51c68-109">CN</span></span>                | <span data-ttu-id="51c68-110">MS-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="51c68-110">ms-DS-Az-Class-ID</span></span>                           |
| <span data-ttu-id="51c68-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="51c68-111">Ldap-Display-Name</span></span> | <span data-ttu-id="51c68-112">msDS-Азклассид</span><span class="sxs-lookup"><span data-stu-id="51c68-112">msDS-AzClassId</span></span>                              |
| <span data-ttu-id="51c68-113">Размер</span><span class="sxs-lookup"><span data-stu-id="51c68-113">Size</span></span>              | <span data-ttu-id="51c68-114">36 символов</span><span class="sxs-lookup"><span data-stu-id="51c68-114">36 characters</span></span>                               |
| <span data-ttu-id="51c68-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="51c68-115">Update Privilege</span></span>  | <span data-ttu-id="51c68-116">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="51c68-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="51c68-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="51c68-117">Update Frequency</span></span>  | <span data-ttu-id="51c68-118">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="51c68-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="51c68-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51c68-119">Attribute-Id</span></span>      | <span data-ttu-id="51c68-120">1.2.840.113556.1.4.1816</span><span class="sxs-lookup"><span data-stu-id="51c68-120">1.2.840.113556.1.4.1816</span></span>                     |
| <span data-ttu-id="51c68-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="51c68-121">System-Id-Guid</span></span>    | <span data-ttu-id="51c68-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span><span class="sxs-lookup"><span data-stu-id="51c68-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span></span>        |
| <span data-ttu-id="51c68-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51c68-123">Syntax</span></span>            | [<span data-ttu-id="51c68-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="51c68-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="51c68-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="51c68-125">Implementations</span></span>

-   [<span data-ttu-id="51c68-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51c68-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51c68-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51c68-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51c68-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51c68-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51c68-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51c68-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51c68-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51c68-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="51c68-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51c68-131">Windows Server 2003</span></span>



| <span data-ttu-id="51c68-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="51c68-132">Entry</span></span> | <span data-ttu-id="51c68-133">Значение</span><span class="sxs-lookup"><span data-stu-id="51c68-133">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="51c68-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51c68-134">Link-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51c68-135">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="51c68-136">System-Only</span></span>            | <span data-ttu-id="51c68-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-137">False</span></span>        |
| <span data-ttu-id="51c68-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51c68-138">Is-Single-Valued</span></span>       | <span data-ttu-id="51c68-139">True</span><span class="sxs-lookup"><span data-stu-id="51c68-139">True</span></span>         |
| <span data-ttu-id="51c68-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51c68-140">Is Indexed</span></span>             | <span data-ttu-id="51c68-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-141">False</span></span>        |
| <span data-ttu-id="51c68-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51c68-142">In Global Catalog</span></span>      | <span data-ttu-id="51c68-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-143">False</span></span>        |
| <span data-ttu-id="51c68-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51c68-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="51c68-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51c68-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="51c68-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51c68-146">Range-Lower</span></span>            | <span data-ttu-id="51c68-147">0</span><span class="sxs-lookup"><span data-stu-id="51c68-147">0</span></span>            |
| <span data-ttu-id="51c68-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51c68-148">Range-Upper</span></span>            | <span data-ttu-id="51c68-149">40</span><span class="sxs-lookup"><span data-stu-id="51c68-149">40</span></span>           |
| <span data-ttu-id="51c68-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-150">Search-Flags</span></span>           | <span data-ttu-id="51c68-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51c68-151">0x00000000</span></span>   |
| <span data-ttu-id="51c68-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-152">System-Flags</span></span>           | <span data-ttu-id="51c68-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51c68-153">0x00000010</span></span>   |
| <span data-ttu-id="51c68-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51c68-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51c68-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51c68-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51c68-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="51c68-156">Entry</span></span> | <span data-ttu-id="51c68-157">Значение</span><span class="sxs-lookup"><span data-stu-id="51c68-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="51c68-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51c68-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51c68-159">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="51c68-160">System-Only</span></span>            | <span data-ttu-id="51c68-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-161">False</span></span>        |
| <span data-ttu-id="51c68-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51c68-162">Is-Single-Valued</span></span>       | <span data-ttu-id="51c68-163">True</span><span class="sxs-lookup"><span data-stu-id="51c68-163">True</span></span>         |
| <span data-ttu-id="51c68-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51c68-164">Is Indexed</span></span>             | <span data-ttu-id="51c68-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-165">False</span></span>        |
| <span data-ttu-id="51c68-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51c68-166">In Global Catalog</span></span>      | <span data-ttu-id="51c68-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-167">False</span></span>        |
| <span data-ttu-id="51c68-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51c68-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="51c68-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51c68-169">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="51c68-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51c68-170">Range-Lower</span></span>            | <span data-ttu-id="51c68-171">0</span><span class="sxs-lookup"><span data-stu-id="51c68-171">0</span></span>            |
| <span data-ttu-id="51c68-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51c68-172">Range-Upper</span></span>            | <span data-ttu-id="51c68-173">40</span><span class="sxs-lookup"><span data-stu-id="51c68-173">40</span></span>           |
| <span data-ttu-id="51c68-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-174">Search-Flags</span></span>           | <span data-ttu-id="51c68-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51c68-175">0x00000000</span></span>   |
| <span data-ttu-id="51c68-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-176">System-Flags</span></span>           | <span data-ttu-id="51c68-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51c68-177">0x00000010</span></span>   |
| <span data-ttu-id="51c68-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51c68-178">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="51c68-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51c68-179">Windows Server 2008</span></span>



| <span data-ttu-id="51c68-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="51c68-180">Entry</span></span> | <span data-ttu-id="51c68-181">Значение</span><span class="sxs-lookup"><span data-stu-id="51c68-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="51c68-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51c68-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51c68-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="51c68-184">System-Only</span></span>            | <span data-ttu-id="51c68-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-185">False</span></span>        |
| <span data-ttu-id="51c68-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51c68-186">Is-Single-Valued</span></span>       | <span data-ttu-id="51c68-187">True</span><span class="sxs-lookup"><span data-stu-id="51c68-187">True</span></span>         |
| <span data-ttu-id="51c68-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51c68-188">Is Indexed</span></span>             | <span data-ttu-id="51c68-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-189">False</span></span>        |
| <span data-ttu-id="51c68-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51c68-190">In Global Catalog</span></span>      | <span data-ttu-id="51c68-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-191">False</span></span>        |
| <span data-ttu-id="51c68-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51c68-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="51c68-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51c68-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="51c68-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51c68-194">Range-Lower</span></span>            | <span data-ttu-id="51c68-195">0</span><span class="sxs-lookup"><span data-stu-id="51c68-195">0</span></span>            |
| <span data-ttu-id="51c68-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51c68-196">Range-Upper</span></span>            | <span data-ttu-id="51c68-197">40</span><span class="sxs-lookup"><span data-stu-id="51c68-197">40</span></span>           |
| <span data-ttu-id="51c68-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-198">Search-Flags</span></span>           | <span data-ttu-id="51c68-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51c68-199">0x00000000</span></span>   |
| <span data-ttu-id="51c68-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-200">System-Flags</span></span>           | <span data-ttu-id="51c68-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51c68-201">0x00000010</span></span>   |
| <span data-ttu-id="51c68-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51c68-202">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51c68-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51c68-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51c68-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="51c68-204">Entry</span></span> | <span data-ttu-id="51c68-205">Значение</span><span class="sxs-lookup"><span data-stu-id="51c68-205">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="51c68-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51c68-206">Link-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51c68-207">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="51c68-208">System-Only</span></span>            | <span data-ttu-id="51c68-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-209">False</span></span>        |
| <span data-ttu-id="51c68-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51c68-210">Is-Single-Valued</span></span>       | <span data-ttu-id="51c68-211">True</span><span class="sxs-lookup"><span data-stu-id="51c68-211">True</span></span>         |
| <span data-ttu-id="51c68-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51c68-212">Is Indexed</span></span>             | <span data-ttu-id="51c68-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-213">False</span></span>        |
| <span data-ttu-id="51c68-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51c68-214">In Global Catalog</span></span>      | <span data-ttu-id="51c68-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-215">False</span></span>        |
| <span data-ttu-id="51c68-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51c68-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="51c68-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51c68-217">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="51c68-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51c68-218">Range-Lower</span></span>            | <span data-ttu-id="51c68-219">0</span><span class="sxs-lookup"><span data-stu-id="51c68-219">0</span></span>            |
| <span data-ttu-id="51c68-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51c68-220">Range-Upper</span></span>            | <span data-ttu-id="51c68-221">40</span><span class="sxs-lookup"><span data-stu-id="51c68-221">40</span></span>           |
| <span data-ttu-id="51c68-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-222">Search-Flags</span></span>           | <span data-ttu-id="51c68-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51c68-223">0x00000000</span></span>   |
| <span data-ttu-id="51c68-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-224">System-Flags</span></span>           | <span data-ttu-id="51c68-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51c68-225">0x00000010</span></span>   |
| <span data-ttu-id="51c68-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51c68-226">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="51c68-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51c68-227">Windows Server 2012</span></span>



| <span data-ttu-id="51c68-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="51c68-228">Entry</span></span> | <span data-ttu-id="51c68-229">Значение</span><span class="sxs-lookup"><span data-stu-id="51c68-229">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="51c68-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="51c68-230">Link-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51c68-231">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="51c68-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="51c68-232">System-Only</span></span>            | <span data-ttu-id="51c68-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-233">False</span></span>        |
| <span data-ttu-id="51c68-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="51c68-234">Is-Single-Valued</span></span>       | <span data-ttu-id="51c68-235">True</span><span class="sxs-lookup"><span data-stu-id="51c68-235">True</span></span>         |
| <span data-ttu-id="51c68-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="51c68-236">Is Indexed</span></span>             | <span data-ttu-id="51c68-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-237">False</span></span>        |
| <span data-ttu-id="51c68-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="51c68-238">In Global Catalog</span></span>      | <span data-ttu-id="51c68-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="51c68-239">False</span></span>        |
| <span data-ttu-id="51c68-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="51c68-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="51c68-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51c68-241">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="51c68-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51c68-242">Range-Lower</span></span>            | <span data-ttu-id="51c68-243">0</span><span class="sxs-lookup"><span data-stu-id="51c68-243">0</span></span>            |
| <span data-ttu-id="51c68-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51c68-244">Range-Upper</span></span>            | <span data-ttu-id="51c68-245">40</span><span class="sxs-lookup"><span data-stu-id="51c68-245">40</span></span>           |
| <span data-ttu-id="51c68-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-246">Search-Flags</span></span>           | <span data-ttu-id="51c68-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51c68-247">0x00000000</span></span>   |
| <span data-ttu-id="51c68-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51c68-248">System-Flags</span></span>           | <span data-ttu-id="51c68-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51c68-249">0x00000010</span></span>   |
| <span data-ttu-id="51c68-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="51c68-250">Classes used in</span></span>        | \-           |



 

 




