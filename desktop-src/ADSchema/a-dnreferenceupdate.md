---
title: DN — ссылка — атрибут обновления
description: При переименовании объекта этот атрибут используется для трассировки всех предыдущих и текущих имен, назначенных объекту, чтобы связанные объекты могли его найти.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- DN — ссылка — схема AD атрибута
- Схема AD атрибута Днреференцеупдате
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655501"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="c97c1-105">DN — ссылка — атрибут обновления</span><span class="sxs-lookup"><span data-stu-id="c97c1-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="c97c1-106">При переименовании объекта этот атрибут используется для трассировки всех предыдущих и текущих имен, назначенных объекту, чтобы связанные объекты могли его найти.</span><span class="sxs-lookup"><span data-stu-id="c97c1-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="c97c1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-107">Entry</span></span> | <span data-ttu-id="c97c1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c97c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="c97c1-109">CN</span></span>                | <span data-ttu-id="c97c1-110">DN — ссылка — обновление</span><span class="sxs-lookup"><span data-stu-id="c97c1-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="c97c1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c97c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c97c1-112">днреференцеупдате</span><span class="sxs-lookup"><span data-stu-id="c97c1-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="c97c1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c97c1-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c97c1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c97c1-114">Update Privilege</span></span>  | <span data-ttu-id="c97c1-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c97c1-115">This is set by the system.</span></span>              |
| <span data-ttu-id="c97c1-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c97c1-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c97c1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-117">Attribute-Id</span></span>      | <span data-ttu-id="c97c1-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="c97c1-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="c97c1-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c97c1-119">System-Id-Guid</span></span>    | <span data-ttu-id="c97c1-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="c97c1-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="c97c1-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c97c1-121">Syntax</span></span>            | [<span data-ttu-id="c97c1-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c97c1-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c97c1-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c97c1-123">Implementations</span></span>

-   [<span data-ttu-id="c97c1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c97c1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c97c1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c97c1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c97c1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c97c1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c97c1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c97c1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c97c1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c97c1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c97c1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c97c1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c97c1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c97c1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c97c1-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-131">Entry</span></span> | <span data-ttu-id="c97c1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c97c1-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c97c1-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c1-135">System-Only</span></span>            | <span data-ttu-id="c97c1-136">True</span><span class="sxs-lookup"><span data-stu-id="c97c1-136">True</span></span>                                                               |
| <span data-ttu-id="c97c1-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c97c1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c1-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-138">False</span></span>                                                              |
| <span data-ttu-id="c97c1-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c97c1-139">Is Indexed</span></span>             | <span data-ttu-id="c97c1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-140">False</span></span>                                                              |
| <span data-ttu-id="c97c1-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c97c1-141">In Global Catalog</span></span>      | <span data-ttu-id="c97c1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-142">False</span></span>                                                              |
| <span data-ttu-id="c97c1-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c97c1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c1-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c97c1-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c97c1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c1-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c1-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-147">Search-Flags</span></span>           | <span data-ttu-id="c97c1-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c97c1-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="c97c1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-149">System-Flags</span></span>           | <span data-ttu-id="c97c1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c1-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="c97c1-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c97c1-151">Classes used in</span></span>        | [<span data-ttu-id="c97c1-152">**Инфраструктура — обновление**</span><span class="sxs-lookup"><span data-stu-id="c97c1-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c97c1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c97c1-153">Windows Server 2003</span></span>



| <span data-ttu-id="c97c1-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-154">Entry</span></span> | <span data-ttu-id="c97c1-155">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c97c1-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c97c1-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c1-158">System-Only</span></span>            | <span data-ttu-id="c97c1-159">True</span><span class="sxs-lookup"><span data-stu-id="c97c1-159">True</span></span>                                                               |
| <span data-ttu-id="c97c1-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c97c1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c1-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-161">False</span></span>                                                              |
| <span data-ttu-id="c97c1-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c97c1-162">Is Indexed</span></span>             | <span data-ttu-id="c97c1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-163">False</span></span>                                                              |
| <span data-ttu-id="c97c1-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c97c1-164">In Global Catalog</span></span>      | <span data-ttu-id="c97c1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-165">False</span></span>                                                              |
| <span data-ttu-id="c97c1-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c97c1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c1-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c97c1-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c97c1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c1-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c1-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-170">Search-Flags</span></span>           | <span data-ttu-id="c97c1-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c97c1-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="c97c1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-172">System-Flags</span></span>           | <span data-ttu-id="c97c1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c1-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="c97c1-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c97c1-174">Classes used in</span></span>        | [<span data-ttu-id="c97c1-175">**Инфраструктура — обновление**</span><span class="sxs-lookup"><span data-stu-id="c97c1-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c97c1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c97c1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c97c1-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-177">Entry</span></span> | <span data-ttu-id="c97c1-178">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c97c1-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c97c1-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c1-181">System-Only</span></span>            | <span data-ttu-id="c97c1-182">True</span><span class="sxs-lookup"><span data-stu-id="c97c1-182">True</span></span>                                                               |
| <span data-ttu-id="c97c1-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c97c1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c1-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-184">False</span></span>                                                              |
| <span data-ttu-id="c97c1-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c97c1-185">Is Indexed</span></span>             | <span data-ttu-id="c97c1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-186">False</span></span>                                                              |
| <span data-ttu-id="c97c1-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c97c1-187">In Global Catalog</span></span>      | <span data-ttu-id="c97c1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-188">False</span></span>                                                              |
| <span data-ttu-id="c97c1-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c97c1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c1-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c97c1-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c97c1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c1-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c1-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-193">Search-Flags</span></span>           | <span data-ttu-id="c97c1-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c97c1-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="c97c1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-195">System-Flags</span></span>           | <span data-ttu-id="c97c1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c1-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="c97c1-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c97c1-197">Classes used in</span></span>        | [<span data-ttu-id="c97c1-198">**Инфраструктура — обновление**</span><span class="sxs-lookup"><span data-stu-id="c97c1-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c97c1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c97c1-199">Windows Server 2008</span></span>



| <span data-ttu-id="c97c1-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-200">Entry</span></span> | <span data-ttu-id="c97c1-201">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c97c1-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c97c1-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c1-204">System-Only</span></span>            | <span data-ttu-id="c97c1-205">True</span><span class="sxs-lookup"><span data-stu-id="c97c1-205">True</span></span>                                                               |
| <span data-ttu-id="c97c1-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c97c1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c1-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-207">False</span></span>                                                              |
| <span data-ttu-id="c97c1-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c97c1-208">Is Indexed</span></span>             | <span data-ttu-id="c97c1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-209">False</span></span>                                                              |
| <span data-ttu-id="c97c1-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c97c1-210">In Global Catalog</span></span>      | <span data-ttu-id="c97c1-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-211">False</span></span>                                                              |
| <span data-ttu-id="c97c1-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c97c1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c1-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c97c1-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c97c1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c1-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c1-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-216">Search-Flags</span></span>           | <span data-ttu-id="c97c1-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c97c1-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="c97c1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-218">System-Flags</span></span>           | <span data-ttu-id="c97c1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c1-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="c97c1-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c97c1-220">Classes used in</span></span>        | [<span data-ttu-id="c97c1-221">**Инфраструктура — обновление**</span><span class="sxs-lookup"><span data-stu-id="c97c1-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c97c1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c97c1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c97c1-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-223">Entry</span></span> | <span data-ttu-id="c97c1-224">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c97c1-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c97c1-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c1-227">System-Only</span></span>            | <span data-ttu-id="c97c1-228">True</span><span class="sxs-lookup"><span data-stu-id="c97c1-228">True</span></span>                                                               |
| <span data-ttu-id="c97c1-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c97c1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c1-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-230">False</span></span>                                                              |
| <span data-ttu-id="c97c1-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c97c1-231">Is Indexed</span></span>             | <span data-ttu-id="c97c1-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-232">False</span></span>                                                              |
| <span data-ttu-id="c97c1-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c97c1-233">In Global Catalog</span></span>      | <span data-ttu-id="c97c1-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-234">False</span></span>                                                              |
| <span data-ttu-id="c97c1-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c97c1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c1-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c97c1-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c97c1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c1-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c1-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-239">Search-Flags</span></span>           | <span data-ttu-id="c97c1-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c97c1-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="c97c1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-241">System-Flags</span></span>           | <span data-ttu-id="c97c1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c1-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="c97c1-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c97c1-243">Classes used in</span></span>        | [<span data-ttu-id="c97c1-244">**Инфраструктура — обновление**</span><span class="sxs-lookup"><span data-stu-id="c97c1-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c97c1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c97c1-245">Windows Server 2012</span></span>



| <span data-ttu-id="c97c1-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="c97c1-246">Entry</span></span> | <span data-ttu-id="c97c1-247">Значение</span><span class="sxs-lookup"><span data-stu-id="c97c1-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c97c1-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c97c1-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c1-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c97c1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c1-250">System-Only</span></span>            | <span data-ttu-id="c97c1-251">True</span><span class="sxs-lookup"><span data-stu-id="c97c1-251">True</span></span>                                                               |
| <span data-ttu-id="c97c1-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c97c1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c1-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-253">False</span></span>                                                              |
| <span data-ttu-id="c97c1-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c97c1-254">Is Indexed</span></span>             | <span data-ttu-id="c97c1-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-255">False</span></span>                                                              |
| <span data-ttu-id="c97c1-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c97c1-256">In Global Catalog</span></span>      | <span data-ttu-id="c97c1-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c97c1-257">False</span></span>                                                              |
| <span data-ttu-id="c97c1-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c97c1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c1-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c97c1-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c97c1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c1-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c1-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c97c1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-262">Search-Flags</span></span>           | <span data-ttu-id="c97c1-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c97c1-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="c97c1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c1-264">System-Flags</span></span>           | <span data-ttu-id="c97c1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c1-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="c97c1-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c97c1-266">Classes used in</span></span>        | [<span data-ttu-id="c97c1-267">**Инфраструктура — обновление**</span><span class="sxs-lookup"><span data-stu-id="c97c1-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





