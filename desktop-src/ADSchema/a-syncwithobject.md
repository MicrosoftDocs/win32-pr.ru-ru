---
title: Sync — атрибут объекта
description: Различающееся имя синхронизированного объекта для синхронизации встроенной группы SAM или локальной политики.
ms.assetid: d7f4c855-7f53-4e6b-b39b-cb6ce76c6561
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "Sync-on-Object"
- Схема AD атрибута Синквисобжект
topic_type:
- apiref
api_name:
- Sync-With-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901f5b87b5bfca6118213c6ba6f535aada4a4b3d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804541"
---
# <a name="sync-with-object-attribute"></a><span data-ttu-id="3c346-105">Sync — атрибут объекта</span><span class="sxs-lookup"><span data-stu-id="3c346-105">Sync-With-Object attribute</span></span>

<span data-ttu-id="3c346-106">Различающееся имя синхронизированного объекта для синхронизации встроенной группы SAM или локальной политики.</span><span class="sxs-lookup"><span data-stu-id="3c346-106">Distinguished name of the object being synchronized for the SAM builtin group/local policy synchronization.</span></span>



| <span data-ttu-id="3c346-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-107">Entry</span></span> | <span data-ttu-id="3c346-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3c346-109">CN</span><span class="sxs-lookup"><span data-stu-id="3c346-109">CN</span></span>                | <span data-ttu-id="3c346-110">Синхронизация с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="3c346-110">Sync-With-Object</span></span>                        |
| <span data-ttu-id="3c346-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3c346-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3c346-112">синквисобжект</span><span class="sxs-lookup"><span data-stu-id="3c346-112">syncWithObject</span></span>                          |
| <span data-ttu-id="3c346-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3c346-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="3c346-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3c346-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="3c346-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3c346-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="3c346-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-116">Attribute-Id</span></span>      | <span data-ttu-id="3c346-117">1.2.840.113556.1.4.664</span><span class="sxs-lookup"><span data-stu-id="3c346-117">1.2.840.113556.1.4.664</span></span>                  |
| <span data-ttu-id="3c346-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3c346-118">System-Id-Guid</span></span>    | <span data-ttu-id="3c346-119">037651e2-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3c346-119">037651e2-441d-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="3c346-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c346-120">Syntax</span></span>            | [<span data-ttu-id="3c346-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3c346-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3c346-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3c346-122">Implementations</span></span>

-   [<span data-ttu-id="3c346-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3c346-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3c346-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3c346-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3c346-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3c346-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3c346-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3c346-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3c346-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3c346-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3c346-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3c346-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3c346-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c346-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3c346-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-130">Entry</span></span> | <span data-ttu-id="3c346-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3c346-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3c346-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c346-134">System-Only</span></span>            | <span data-ttu-id="3c346-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-135">False</span></span>        |
| <span data-ttu-id="3c346-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3c346-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3c346-137">True</span><span class="sxs-lookup"><span data-stu-id="3c346-137">True</span></span>         |
| <span data-ttu-id="3c346-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3c346-138">Is Indexed</span></span>             | <span data-ttu-id="3c346-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-139">False</span></span>        |
| <span data-ttu-id="3c346-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3c346-140">In Global Catalog</span></span>      | <span data-ttu-id="3c346-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-141">False</span></span>        |
| <span data-ttu-id="3c346-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3c346-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c346-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3c346-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3c346-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c346-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3c346-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c346-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3c346-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-146">Search-Flags</span></span>           | <span data-ttu-id="3c346-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c346-147">0x00000000</span></span>   |
| <span data-ttu-id="3c346-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-148">System-Flags</span></span>           | <span data-ttu-id="3c346-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c346-149">0x00000010</span></span>   |
| <span data-ttu-id="3c346-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3c346-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="3c346-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c346-151">Windows Server 2003</span></span>



| <span data-ttu-id="3c346-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-152">Entry</span></span> | <span data-ttu-id="3c346-153">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3c346-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3c346-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c346-156">System-Only</span></span>            | <span data-ttu-id="3c346-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-157">False</span></span>        |
| <span data-ttu-id="3c346-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3c346-158">Is-Single-Valued</span></span>       | <span data-ttu-id="3c346-159">True</span><span class="sxs-lookup"><span data-stu-id="3c346-159">True</span></span>         |
| <span data-ttu-id="3c346-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3c346-160">Is Indexed</span></span>             | <span data-ttu-id="3c346-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-161">False</span></span>        |
| <span data-ttu-id="3c346-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3c346-162">In Global Catalog</span></span>      | <span data-ttu-id="3c346-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-163">False</span></span>        |
| <span data-ttu-id="3c346-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3c346-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c346-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3c346-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3c346-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c346-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3c346-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c346-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3c346-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-168">Search-Flags</span></span>           | <span data-ttu-id="3c346-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c346-169">0x00000000</span></span>   |
| <span data-ttu-id="3c346-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-170">System-Flags</span></span>           | <span data-ttu-id="3c346-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c346-171">0x00000010</span></span>   |
| <span data-ttu-id="3c346-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3c346-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3c346-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3c346-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3c346-174">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-174">Entry</span></span> | <span data-ttu-id="3c346-175">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3c346-176">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3c346-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c346-178">System-Only</span></span>            | <span data-ttu-id="3c346-179">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-179">False</span></span>        |
| <span data-ttu-id="3c346-180">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3c346-180">Is-Single-Valued</span></span>       | <span data-ttu-id="3c346-181">True</span><span class="sxs-lookup"><span data-stu-id="3c346-181">True</span></span>         |
| <span data-ttu-id="3c346-182">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3c346-182">Is Indexed</span></span>             | <span data-ttu-id="3c346-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-183">False</span></span>        |
| <span data-ttu-id="3c346-184">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3c346-184">In Global Catalog</span></span>      | <span data-ttu-id="3c346-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-185">False</span></span>        |
| <span data-ttu-id="3c346-186">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3c346-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c346-187">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3c346-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3c346-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c346-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3c346-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c346-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3c346-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-190">Search-Flags</span></span>           | <span data-ttu-id="3c346-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c346-191">0x00000000</span></span>   |
| <span data-ttu-id="3c346-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-192">System-Flags</span></span>           | <span data-ttu-id="3c346-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c346-193">0x00000010</span></span>   |
| <span data-ttu-id="3c346-194">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3c346-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="3c346-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c346-195">Windows Server 2008</span></span>



| <span data-ttu-id="3c346-196">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-196">Entry</span></span> | <span data-ttu-id="3c346-197">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3c346-198">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3c346-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c346-200">System-Only</span></span>            | <span data-ttu-id="3c346-201">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-201">False</span></span>        |
| <span data-ttu-id="3c346-202">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3c346-202">Is-Single-Valued</span></span>       | <span data-ttu-id="3c346-203">True</span><span class="sxs-lookup"><span data-stu-id="3c346-203">True</span></span>         |
| <span data-ttu-id="3c346-204">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3c346-204">Is Indexed</span></span>             | <span data-ttu-id="3c346-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-205">False</span></span>        |
| <span data-ttu-id="3c346-206">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3c346-206">In Global Catalog</span></span>      | <span data-ttu-id="3c346-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-207">False</span></span>        |
| <span data-ttu-id="3c346-208">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3c346-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c346-209">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3c346-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3c346-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c346-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3c346-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c346-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3c346-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-212">Search-Flags</span></span>           | <span data-ttu-id="3c346-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c346-213">0x00000000</span></span>   |
| <span data-ttu-id="3c346-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-214">System-Flags</span></span>           | <span data-ttu-id="3c346-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c346-215">0x00000010</span></span>   |
| <span data-ttu-id="3c346-216">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3c346-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3c346-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c346-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3c346-218">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-218">Entry</span></span> | <span data-ttu-id="3c346-219">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3c346-220">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3c346-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c346-222">System-Only</span></span>            | <span data-ttu-id="3c346-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-223">False</span></span>        |
| <span data-ttu-id="3c346-224">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3c346-224">Is-Single-Valued</span></span>       | <span data-ttu-id="3c346-225">True</span><span class="sxs-lookup"><span data-stu-id="3c346-225">True</span></span>         |
| <span data-ttu-id="3c346-226">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3c346-226">Is Indexed</span></span>             | <span data-ttu-id="3c346-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-227">False</span></span>        |
| <span data-ttu-id="3c346-228">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3c346-228">In Global Catalog</span></span>      | <span data-ttu-id="3c346-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-229">False</span></span>        |
| <span data-ttu-id="3c346-230">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3c346-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c346-231">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3c346-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3c346-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c346-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3c346-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c346-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3c346-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-234">Search-Flags</span></span>           | <span data-ttu-id="3c346-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c346-235">0x00000000</span></span>   |
| <span data-ttu-id="3c346-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-236">System-Flags</span></span>           | <span data-ttu-id="3c346-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c346-237">0x00000010</span></span>   |
| <span data-ttu-id="3c346-238">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3c346-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="3c346-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c346-239">Windows Server 2012</span></span>



| <span data-ttu-id="3c346-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="3c346-240">Entry</span></span> | <span data-ttu-id="3c346-241">Значение</span><span class="sxs-lookup"><span data-stu-id="3c346-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3c346-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3c346-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c346-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3c346-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c346-244">System-Only</span></span>            | <span data-ttu-id="3c346-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-245">False</span></span>        |
| <span data-ttu-id="3c346-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3c346-246">Is-Single-Valued</span></span>       | <span data-ttu-id="3c346-247">True</span><span class="sxs-lookup"><span data-stu-id="3c346-247">True</span></span>         |
| <span data-ttu-id="3c346-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3c346-248">Is Indexed</span></span>             | <span data-ttu-id="3c346-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-249">False</span></span>        |
| <span data-ttu-id="3c346-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3c346-250">In Global Catalog</span></span>      | <span data-ttu-id="3c346-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="3c346-251">False</span></span>        |
| <span data-ttu-id="3c346-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3c346-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c346-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3c346-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3c346-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c346-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="3c346-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c346-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="3c346-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-256">Search-Flags</span></span>           | <span data-ttu-id="3c346-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c346-257">0x00000000</span></span>   |
| <span data-ttu-id="3c346-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c346-258">System-Flags</span></span>           | <span data-ttu-id="3c346-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c346-259">0x00000010</span></span>   |
| <span data-ttu-id="3c346-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3c346-260">Classes used in</span></span>        | \-           |



 

 




