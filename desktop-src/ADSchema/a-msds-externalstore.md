---
title: Атрибут ms-DS-External-Store
description: Строка, определяющая расположение внешнего хранилища, например базы данных.
ms.assetid: 93c8ac85-521f-464b-a32f-6ae4c941899e
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута внешнего хранилища MS-DS-External-Store
- Схема AD атрибута msDS-Екстерналсторе
topic_type:
- apiref
api_name:
- ms-DS-External-Store
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d127c2a9f4aa91c3866803a749d225b5403e68fb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804696"
---
# <a name="ms-ds-external-store-attribute"></a><span data-ttu-id="511b6-105">Атрибут ms-DS-External-Store</span><span class="sxs-lookup"><span data-stu-id="511b6-105">ms-DS-External-Store attribute</span></span>

<span data-ttu-id="511b6-106">Строка, определяющая расположение внешнего хранилища, например базы данных.</span><span class="sxs-lookup"><span data-stu-id="511b6-106">A string that identifies the location of an external store, such as a database.</span></span>



| <span data-ttu-id="511b6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="511b6-107">Entry</span></span> | <span data-ttu-id="511b6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="511b6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="511b6-109">CN</span><span class="sxs-lookup"><span data-stu-id="511b6-109">CN</span></span>                | <span data-ttu-id="511b6-110">MS-DS-External-Store</span><span class="sxs-lookup"><span data-stu-id="511b6-110">ms-DS-External-Store</span></span>                        |
| <span data-ttu-id="511b6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="511b6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="511b6-112">msDS-Екстерналсторе</span><span class="sxs-lookup"><span data-stu-id="511b6-112">msDS-ExternalStore</span></span>                          |
| <span data-ttu-id="511b6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="511b6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="511b6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="511b6-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="511b6-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="511b6-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="511b6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="511b6-116">Attribute-Id</span></span>      | <span data-ttu-id="511b6-117">1.2.840.113556.1.4.1834</span><span class="sxs-lookup"><span data-stu-id="511b6-117">1.2.840.113556.1.4.1834</span></span>                     |
| <span data-ttu-id="511b6-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="511b6-118">System-Id-Guid</span></span>    | <span data-ttu-id="511b6-119">604877cd-9cdb-47c7-b03d-3daadb044910</span><span class="sxs-lookup"><span data-stu-id="511b6-119">604877cd-9cdb-47c7-b03d-3daadb044910</span></span>        |
| <span data-ttu-id="511b6-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="511b6-120">Syntax</span></span>            | [<span data-ttu-id="511b6-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="511b6-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="511b6-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="511b6-122">Implementations</span></span>

-   [<span data-ttu-id="511b6-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="511b6-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="511b6-124">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="511b6-124">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="511b6-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="511b6-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="511b6-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="511b6-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="511b6-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="511b6-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="511b6-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="511b6-128">Windows Server 2003</span></span>



| <span data-ttu-id="511b6-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="511b6-129">Entry</span></span> | <span data-ttu-id="511b6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="511b6-130">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="511b6-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="511b6-131">Link-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="511b6-132">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="511b6-133">System-Only</span></span>            | <span data-ttu-id="511b6-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-134">False</span></span>        |
| <span data-ttu-id="511b6-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="511b6-135">Is-Single-Valued</span></span>       | <span data-ttu-id="511b6-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-136">False</span></span>        |
| <span data-ttu-id="511b6-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="511b6-137">Is Indexed</span></span>             | <span data-ttu-id="511b6-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-138">False</span></span>        |
| <span data-ttu-id="511b6-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="511b6-139">In Global Catalog</span></span>      | <span data-ttu-id="511b6-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-140">False</span></span>        |
| <span data-ttu-id="511b6-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="511b6-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="511b6-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="511b6-142">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="511b6-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="511b6-143">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="511b6-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="511b6-144">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="511b6-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-145">Search-Flags</span></span>           | <span data-ttu-id="511b6-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-146">0x00000000</span></span>   |
| <span data-ttu-id="511b6-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-147">System-Flags</span></span>           | <span data-ttu-id="511b6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-148">0x00000000</span></span>   |
| <span data-ttu-id="511b6-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="511b6-149">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="511b6-150">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="511b6-150">Windows Server 2003 R2</span></span>



| <span data-ttu-id="511b6-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="511b6-151">Entry</span></span> | <span data-ttu-id="511b6-152">Значение</span><span class="sxs-lookup"><span data-stu-id="511b6-152">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="511b6-153">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="511b6-153">Link-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="511b6-154">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="511b6-155">System-Only</span></span>            | <span data-ttu-id="511b6-156">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-156">False</span></span>        |
| <span data-ttu-id="511b6-157">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="511b6-157">Is-Single-Valued</span></span>       | <span data-ttu-id="511b6-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-158">False</span></span>        |
| <span data-ttu-id="511b6-159">Индексируется</span><span class="sxs-lookup"><span data-stu-id="511b6-159">Is Indexed</span></span>             | <span data-ttu-id="511b6-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-160">False</span></span>        |
| <span data-ttu-id="511b6-161">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="511b6-161">In Global Catalog</span></span>      | <span data-ttu-id="511b6-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-162">False</span></span>        |
| <span data-ttu-id="511b6-163">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="511b6-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="511b6-164">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="511b6-164">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="511b6-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="511b6-165">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="511b6-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="511b6-166">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="511b6-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-167">Search-Flags</span></span>           | <span data-ttu-id="511b6-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-168">0x00000000</span></span>   |
| <span data-ttu-id="511b6-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-169">System-Flags</span></span>           | <span data-ttu-id="511b6-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-170">0x00000000</span></span>   |
| <span data-ttu-id="511b6-171">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="511b6-171">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="511b6-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="511b6-172">Windows Server 2008</span></span>



| <span data-ttu-id="511b6-173">Ввод</span><span class="sxs-lookup"><span data-stu-id="511b6-173">Entry</span></span> | <span data-ttu-id="511b6-174">Значение</span><span class="sxs-lookup"><span data-stu-id="511b6-174">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="511b6-175">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="511b6-175">Link-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-176">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="511b6-176">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-177">System-Only</span><span class="sxs-lookup"><span data-stu-id="511b6-177">System-Only</span></span>            | <span data-ttu-id="511b6-178">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-178">False</span></span>        |
| <span data-ttu-id="511b6-179">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="511b6-179">Is-Single-Valued</span></span>       | <span data-ttu-id="511b6-180">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-180">False</span></span>        |
| <span data-ttu-id="511b6-181">Индексируется</span><span class="sxs-lookup"><span data-stu-id="511b6-181">Is Indexed</span></span>             | <span data-ttu-id="511b6-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-182">False</span></span>        |
| <span data-ttu-id="511b6-183">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="511b6-183">In Global Catalog</span></span>      | <span data-ttu-id="511b6-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-184">False</span></span>        |
| <span data-ttu-id="511b6-185">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="511b6-185">NT-Security-Descriptor</span></span> | <span data-ttu-id="511b6-186">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="511b6-186">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="511b6-187">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="511b6-187">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="511b6-188">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="511b6-188">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="511b6-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-189">Search-Flags</span></span>           | <span data-ttu-id="511b6-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-190">0x00000000</span></span>   |
| <span data-ttu-id="511b6-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-191">System-Flags</span></span>           | <span data-ttu-id="511b6-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-192">0x00000000</span></span>   |
| <span data-ttu-id="511b6-193">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="511b6-193">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="511b6-194">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="511b6-194">Windows Server 2008 R2</span></span>



| <span data-ttu-id="511b6-195">Ввод</span><span class="sxs-lookup"><span data-stu-id="511b6-195">Entry</span></span> | <span data-ttu-id="511b6-196">Значение</span><span class="sxs-lookup"><span data-stu-id="511b6-196">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="511b6-197">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="511b6-197">Link-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-198">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="511b6-198">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-199">System-Only</span><span class="sxs-lookup"><span data-stu-id="511b6-199">System-Only</span></span>            | <span data-ttu-id="511b6-200">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-200">False</span></span>        |
| <span data-ttu-id="511b6-201">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="511b6-201">Is-Single-Valued</span></span>       | <span data-ttu-id="511b6-202">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-202">False</span></span>        |
| <span data-ttu-id="511b6-203">Индексируется</span><span class="sxs-lookup"><span data-stu-id="511b6-203">Is Indexed</span></span>             | <span data-ttu-id="511b6-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-204">False</span></span>        |
| <span data-ttu-id="511b6-205">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="511b6-205">In Global Catalog</span></span>      | <span data-ttu-id="511b6-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-206">False</span></span>        |
| <span data-ttu-id="511b6-207">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="511b6-207">NT-Security-Descriptor</span></span> | <span data-ttu-id="511b6-208">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="511b6-208">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="511b6-209">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="511b6-209">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="511b6-210">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="511b6-210">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="511b6-211">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-211">Search-Flags</span></span>           | <span data-ttu-id="511b6-212">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-212">0x00000000</span></span>   |
| <span data-ttu-id="511b6-213">System-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-213">System-Flags</span></span>           | <span data-ttu-id="511b6-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-214">0x00000000</span></span>   |
| <span data-ttu-id="511b6-215">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="511b6-215">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="511b6-216">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="511b6-216">Windows Server 2012</span></span>



| <span data-ttu-id="511b6-217">Ввод</span><span class="sxs-lookup"><span data-stu-id="511b6-217">Entry</span></span> | <span data-ttu-id="511b6-218">Значение</span><span class="sxs-lookup"><span data-stu-id="511b6-218">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="511b6-219">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="511b6-219">Link-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-220">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="511b6-220">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="511b6-221">System-Only</span><span class="sxs-lookup"><span data-stu-id="511b6-221">System-Only</span></span>            | <span data-ttu-id="511b6-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-222">False</span></span>        |
| <span data-ttu-id="511b6-223">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="511b6-223">Is-Single-Valued</span></span>       | <span data-ttu-id="511b6-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-224">False</span></span>        |
| <span data-ttu-id="511b6-225">Индексируется</span><span class="sxs-lookup"><span data-stu-id="511b6-225">Is Indexed</span></span>             | <span data-ttu-id="511b6-226">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-226">False</span></span>        |
| <span data-ttu-id="511b6-227">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="511b6-227">In Global Catalog</span></span>      | <span data-ttu-id="511b6-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="511b6-228">False</span></span>        |
| <span data-ttu-id="511b6-229">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="511b6-229">NT-Security-Descriptor</span></span> | <span data-ttu-id="511b6-230">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="511b6-230">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="511b6-231">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="511b6-231">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="511b6-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="511b6-232">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="511b6-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-233">Search-Flags</span></span>           | <span data-ttu-id="511b6-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-234">0x00000000</span></span>   |
| <span data-ttu-id="511b6-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="511b6-235">System-Flags</span></span>           | <span data-ttu-id="511b6-236">0x00000000</span><span class="sxs-lookup"><span data-stu-id="511b6-236">0x00000000</span></span>   |
| <span data-ttu-id="511b6-237">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="511b6-237">Classes used in</span></span>        | \-           |



 

 




