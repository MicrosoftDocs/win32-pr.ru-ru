---
title: Sync — атрибут с идентификатором SID
description: Для синхронизации встроенного объекта Group/локальной политики SAM это локальная группа, которой соответствует объект.
ms.assetid: b983210d-1c54-4355-bc37-771e51016175
ms.tgt_platform: multiple
keywords:
- Схема AD с атрибутом "sync-with-SID"
- Схема AD атрибута Синквиссид
topic_type:
- apiref
api_name:
- Sync-With-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845a95b737a56a853fa7fb4e77d5612f1efc3c37
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138755"
---
# <a name="sync-with-sid-attribute"></a><span data-ttu-id="45d57-105">Sync — атрибут с идентификатором SID</span><span class="sxs-lookup"><span data-stu-id="45d57-105">Sync-With-SID attribute</span></span>

<span data-ttu-id="45d57-106">Для синхронизации встроенного объекта Group/локальной политики SAM это локальная группа, которой соответствует объект.</span><span class="sxs-lookup"><span data-stu-id="45d57-106">For the SAM builtin group object/ local policy synchronization, this is the local group to which an object corresponds.</span></span>



| <span data-ttu-id="45d57-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-107">Entry</span></span> | <span data-ttu-id="45d57-108">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="45d57-109">CN</span><span class="sxs-lookup"><span data-stu-id="45d57-109">CN</span></span>                | <span data-ttu-id="45d57-110">Синхронизация с ИД безопасности</span><span class="sxs-lookup"><span data-stu-id="45d57-110">Sync-With-SID</span></span>                        |
| <span data-ttu-id="45d57-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="45d57-111">Ldap-Display-Name</span></span> | <span data-ttu-id="45d57-112">синквиссид</span><span class="sxs-lookup"><span data-stu-id="45d57-112">syncWithSID</span></span>                          |
| <span data-ttu-id="45d57-113">Размер</span><span class="sxs-lookup"><span data-stu-id="45d57-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="45d57-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="45d57-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="45d57-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="45d57-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="45d57-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-116">Attribute-Id</span></span>      | <span data-ttu-id="45d57-117">1.2.840.113556.1.4.667</span><span class="sxs-lookup"><span data-stu-id="45d57-117">1.2.840.113556.1.4.667</span></span>               |
| <span data-ttu-id="45d57-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="45d57-118">System-Id-Guid</span></span>    | <span data-ttu-id="45d57-119">037651e5-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="45d57-119">037651e5-441d-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="45d57-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45d57-120">Syntax</span></span>            | [<span data-ttu-id="45d57-121">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="45d57-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="45d57-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="45d57-122">Implementations</span></span>

-   [<span data-ttu-id="45d57-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="45d57-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="45d57-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="45d57-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="45d57-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="45d57-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="45d57-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="45d57-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="45d57-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="45d57-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="45d57-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="45d57-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="45d57-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45d57-129">Windows 2000 Server</span></span>



| <span data-ttu-id="45d57-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-130">Entry</span></span> | <span data-ttu-id="45d57-131">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="45d57-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45d57-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d57-134">System-Only</span></span>            | <span data-ttu-id="45d57-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-135">False</span></span>        |
| <span data-ttu-id="45d57-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45d57-136">Is-Single-Valued</span></span>       | <span data-ttu-id="45d57-137">True</span><span class="sxs-lookup"><span data-stu-id="45d57-137">True</span></span>         |
| <span data-ttu-id="45d57-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45d57-138">Is Indexed</span></span>             | <span data-ttu-id="45d57-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-139">False</span></span>        |
| <span data-ttu-id="45d57-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45d57-140">In Global Catalog</span></span>      | <span data-ttu-id="45d57-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-141">False</span></span>        |
| <span data-ttu-id="45d57-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45d57-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d57-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45d57-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="45d57-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d57-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="45d57-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d57-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="45d57-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-146">Search-Flags</span></span>           | <span data-ttu-id="45d57-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d57-147">0x00000000</span></span>   |
| <span data-ttu-id="45d57-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-148">System-Flags</span></span>           | <span data-ttu-id="45d57-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d57-149">0x00000010</span></span>   |
| <span data-ttu-id="45d57-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45d57-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="45d57-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45d57-151">Windows Server 2003</span></span>



| <span data-ttu-id="45d57-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-152">Entry</span></span> | <span data-ttu-id="45d57-153">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="45d57-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45d57-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d57-156">System-Only</span></span>            | <span data-ttu-id="45d57-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-157">False</span></span>        |
| <span data-ttu-id="45d57-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45d57-158">Is-Single-Valued</span></span>       | <span data-ttu-id="45d57-159">True</span><span class="sxs-lookup"><span data-stu-id="45d57-159">True</span></span>         |
| <span data-ttu-id="45d57-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45d57-160">Is Indexed</span></span>             | <span data-ttu-id="45d57-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-161">False</span></span>        |
| <span data-ttu-id="45d57-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45d57-162">In Global Catalog</span></span>      | <span data-ttu-id="45d57-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-163">False</span></span>        |
| <span data-ttu-id="45d57-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45d57-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d57-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45d57-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="45d57-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d57-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="45d57-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d57-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="45d57-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-168">Search-Flags</span></span>           | <span data-ttu-id="45d57-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d57-169">0x00000000</span></span>   |
| <span data-ttu-id="45d57-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-170">System-Flags</span></span>           | <span data-ttu-id="45d57-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d57-171">0x00000010</span></span>   |
| <span data-ttu-id="45d57-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45d57-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="45d57-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="45d57-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="45d57-174">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-174">Entry</span></span> | <span data-ttu-id="45d57-175">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="45d57-176">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45d57-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d57-178">System-Only</span></span>            | <span data-ttu-id="45d57-179">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-179">False</span></span>        |
| <span data-ttu-id="45d57-180">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45d57-180">Is-Single-Valued</span></span>       | <span data-ttu-id="45d57-181">True</span><span class="sxs-lookup"><span data-stu-id="45d57-181">True</span></span>         |
| <span data-ttu-id="45d57-182">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45d57-182">Is Indexed</span></span>             | <span data-ttu-id="45d57-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-183">False</span></span>        |
| <span data-ttu-id="45d57-184">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45d57-184">In Global Catalog</span></span>      | <span data-ttu-id="45d57-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-185">False</span></span>        |
| <span data-ttu-id="45d57-186">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45d57-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d57-187">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45d57-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="45d57-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d57-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="45d57-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d57-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="45d57-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-190">Search-Flags</span></span>           | <span data-ttu-id="45d57-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d57-191">0x00000000</span></span>   |
| <span data-ttu-id="45d57-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-192">System-Flags</span></span>           | <span data-ttu-id="45d57-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d57-193">0x00000010</span></span>   |
| <span data-ttu-id="45d57-194">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45d57-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="45d57-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45d57-195">Windows Server 2008</span></span>



| <span data-ttu-id="45d57-196">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-196">Entry</span></span> | <span data-ttu-id="45d57-197">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="45d57-198">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45d57-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d57-200">System-Only</span></span>            | <span data-ttu-id="45d57-201">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-201">False</span></span>        |
| <span data-ttu-id="45d57-202">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45d57-202">Is-Single-Valued</span></span>       | <span data-ttu-id="45d57-203">True</span><span class="sxs-lookup"><span data-stu-id="45d57-203">True</span></span>         |
| <span data-ttu-id="45d57-204">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45d57-204">Is Indexed</span></span>             | <span data-ttu-id="45d57-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-205">False</span></span>        |
| <span data-ttu-id="45d57-206">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45d57-206">In Global Catalog</span></span>      | <span data-ttu-id="45d57-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-207">False</span></span>        |
| <span data-ttu-id="45d57-208">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45d57-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d57-209">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45d57-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="45d57-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d57-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="45d57-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d57-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="45d57-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-212">Search-Flags</span></span>           | <span data-ttu-id="45d57-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d57-213">0x00000000</span></span>   |
| <span data-ttu-id="45d57-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-214">System-Flags</span></span>           | <span data-ttu-id="45d57-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d57-215">0x00000010</span></span>   |
| <span data-ttu-id="45d57-216">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45d57-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="45d57-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45d57-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="45d57-218">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-218">Entry</span></span> | <span data-ttu-id="45d57-219">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="45d57-220">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45d57-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d57-222">System-Only</span></span>            | <span data-ttu-id="45d57-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-223">False</span></span>        |
| <span data-ttu-id="45d57-224">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45d57-224">Is-Single-Valued</span></span>       | <span data-ttu-id="45d57-225">True</span><span class="sxs-lookup"><span data-stu-id="45d57-225">True</span></span>         |
| <span data-ttu-id="45d57-226">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45d57-226">Is Indexed</span></span>             | <span data-ttu-id="45d57-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-227">False</span></span>        |
| <span data-ttu-id="45d57-228">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45d57-228">In Global Catalog</span></span>      | <span data-ttu-id="45d57-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-229">False</span></span>        |
| <span data-ttu-id="45d57-230">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45d57-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d57-231">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45d57-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="45d57-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d57-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="45d57-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d57-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="45d57-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-234">Search-Flags</span></span>           | <span data-ttu-id="45d57-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d57-235">0x00000000</span></span>   |
| <span data-ttu-id="45d57-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-236">System-Flags</span></span>           | <span data-ttu-id="45d57-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d57-237">0x00000010</span></span>   |
| <span data-ttu-id="45d57-238">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45d57-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="45d57-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45d57-239">Windows Server 2012</span></span>



| <span data-ttu-id="45d57-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="45d57-240">Entry</span></span> | <span data-ttu-id="45d57-241">Значение</span><span class="sxs-lookup"><span data-stu-id="45d57-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="45d57-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="45d57-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d57-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="45d57-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d57-244">System-Only</span></span>            | <span data-ttu-id="45d57-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-245">False</span></span>        |
| <span data-ttu-id="45d57-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="45d57-246">Is-Single-Valued</span></span>       | <span data-ttu-id="45d57-247">True</span><span class="sxs-lookup"><span data-stu-id="45d57-247">True</span></span>         |
| <span data-ttu-id="45d57-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="45d57-248">Is Indexed</span></span>             | <span data-ttu-id="45d57-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-249">False</span></span>        |
| <span data-ttu-id="45d57-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="45d57-250">In Global Catalog</span></span>      | <span data-ttu-id="45d57-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="45d57-251">False</span></span>        |
| <span data-ttu-id="45d57-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="45d57-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d57-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45d57-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="45d57-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d57-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="45d57-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d57-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="45d57-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-256">Search-Flags</span></span>           | <span data-ttu-id="45d57-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d57-257">0x00000000</span></span>   |
| <span data-ttu-id="45d57-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d57-258">System-Flags</span></span>           | <span data-ttu-id="45d57-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d57-259">0x00000010</span></span>   |
| <span data-ttu-id="45d57-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="45d57-260">Classes used in</span></span>        | \-           |



 

 




