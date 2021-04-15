---
title: атрибут "время до кристалла" MS-DS-Entry
description: Содержит абсолютный срок действия динамического объекта в каталоге.
ms.assetid: 233a61a7-3e95-409e-89c3-1eeeca562173
ms.tgt_platform: multiple
keywords:
- Схема AD с атрибутом "время до кристалла" MS-DS-Entry
- Схема AD атрибута msDS-Time-to-кристалла
topic_type:
- apiref
api_name:
- ms-DS-Entry-Time-To-Die
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074fbd5300cca87a437d4624100a0bd4734a52a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655453"
---
# <a name="ms-ds-entry-time-to-die-attribute"></a><span data-ttu-id="d37c4-105">атрибут "время до кристалла" MS-DS-Entry</span><span class="sxs-lookup"><span data-stu-id="d37c4-105">ms-DS-Entry-Time-To-Die attribute</span></span>

<span data-ttu-id="d37c4-106">Содержит абсолютный срок действия динамического объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="d37c4-106">Holds the absolute expiration time of a dynamic object in the directory.</span></span>



| <span data-ttu-id="d37c4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-107">Entry</span></span> | <span data-ttu-id="d37c4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-108">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="d37c4-109">CN</span><span class="sxs-lookup"><span data-stu-id="d37c4-109">CN</span></span>                | <span data-ttu-id="d37c4-110">MS-DS-ввод-время до кристалла</span><span class="sxs-lookup"><span data-stu-id="d37c4-110">ms-DS-Entry-Time-To-Die</span></span>                                       |
| <span data-ttu-id="d37c4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d37c4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d37c4-112">msDS-запись-время до кристалла</span><span class="sxs-lookup"><span data-stu-id="d37c4-112">msDS-Entry-Time-To-Die</span></span>                                        |
| <span data-ttu-id="d37c4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d37c4-113">Size</span></span>              | \-                                                            |
| <span data-ttu-id="d37c4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d37c4-114">Update Privilege</span></span>  | <span data-ttu-id="d37c4-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="d37c4-115">This value is set by the system.</span></span>                              |
| <span data-ttu-id="d37c4-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d37c4-116">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="d37c4-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-117">Attribute-Id</span></span>      | <span data-ttu-id="d37c4-118">1.2.840.113556.1.4.1622</span><span class="sxs-lookup"><span data-stu-id="d37c4-118">1.2.840.113556.1.4.1622</span></span>                                       |
| <span data-ttu-id="d37c4-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d37c4-119">System-Id-Guid</span></span>    | <span data-ttu-id="d37c4-120">e1e9bad7-c6dd-4101-a843-794cec85b038</span><span class="sxs-lookup"><span data-stu-id="d37c4-120">e1e9bad7-c6dd-4101-a843-794cec85b038</span></span>                          |
| <span data-ttu-id="d37c4-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d37c4-121">Syntax</span></span>            | [<span data-ttu-id="d37c4-122">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="d37c4-122">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="d37c4-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d37c4-123">Implementations</span></span>

-   [<span data-ttu-id="d37c4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d37c4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d37c4-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d37c4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d37c4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d37c4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d37c4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d37c4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d37c4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d37c4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d37c4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d37c4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d37c4-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d37c4-130">Windows Server 2003</span></span>



| <span data-ttu-id="d37c4-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-131">Entry</span></span> | <span data-ttu-id="d37c4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d37c4-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d37c4-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d37c4-135">System-Only</span></span>            | <span data-ttu-id="d37c4-136">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-136">True</span></span>                                                 |
| <span data-ttu-id="d37c4-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d37c4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d37c4-138">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-138">True</span></span>                                                 |
| <span data-ttu-id="d37c4-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d37c4-139">Is Indexed</span></span>             | <span data-ttu-id="d37c4-140">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-140">True</span></span>                                                 |
| <span data-ttu-id="d37c4-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d37c4-141">In Global Catalog</span></span>      | <span data-ttu-id="d37c4-142">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-142">True</span></span>                                                 |
| <span data-ttu-id="d37c4-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d37c4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d37c4-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d37c4-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d37c4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d37c4-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d37c4-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-147">Search-Flags</span></span>           | <span data-ttu-id="d37c4-148">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d37c4-148">0x00000009</span></span>                                           |
| <span data-ttu-id="d37c4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-149">System-Flags</span></span>           | <span data-ttu-id="d37c4-150">0x00000018</span><span class="sxs-lookup"><span data-stu-id="d37c4-150">0x00000018</span></span>                                           |
| <span data-ttu-id="d37c4-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d37c4-151">Classes used in</span></span>        | [<span data-ttu-id="d37c4-152">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="d37c4-152">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d37c4-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="d37c4-153">ADAM</span></span>



| <span data-ttu-id="d37c4-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-154">Entry</span></span> | <span data-ttu-id="d37c4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d37c4-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d37c4-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d37c4-158">System-Only</span></span>            | <span data-ttu-id="d37c4-159">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-159">True</span></span>                                                 |
| <span data-ttu-id="d37c4-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d37c4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d37c4-161">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-161">True</span></span>                                                 |
| <span data-ttu-id="d37c4-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d37c4-162">Is Indexed</span></span>             | <span data-ttu-id="d37c4-163">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-163">True</span></span>                                                 |
| <span data-ttu-id="d37c4-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d37c4-164">In Global Catalog</span></span>      | <span data-ttu-id="d37c4-165">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-165">True</span></span>                                                 |
| <span data-ttu-id="d37c4-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d37c4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d37c4-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d37c4-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d37c4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d37c4-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d37c4-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-170">Search-Flags</span></span>           | <span data-ttu-id="d37c4-171">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d37c4-171">0x00000009</span></span>                                           |
| <span data-ttu-id="d37c4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-172">System-Flags</span></span>           | <span data-ttu-id="d37c4-173">0x00000018</span><span class="sxs-lookup"><span data-stu-id="d37c4-173">0x00000018</span></span>                                           |
| <span data-ttu-id="d37c4-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d37c4-174">Classes used in</span></span>        | [<span data-ttu-id="d37c4-175">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="d37c4-175">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d37c4-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d37c4-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d37c4-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-177">Entry</span></span> | <span data-ttu-id="d37c4-178">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d37c4-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d37c4-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d37c4-181">System-Only</span></span>            | <span data-ttu-id="d37c4-182">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-182">True</span></span>                                                 |
| <span data-ttu-id="d37c4-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d37c4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d37c4-184">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-184">True</span></span>                                                 |
| <span data-ttu-id="d37c4-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d37c4-185">Is Indexed</span></span>             | <span data-ttu-id="d37c4-186">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-186">True</span></span>                                                 |
| <span data-ttu-id="d37c4-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d37c4-187">In Global Catalog</span></span>      | <span data-ttu-id="d37c4-188">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-188">True</span></span>                                                 |
| <span data-ttu-id="d37c4-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d37c4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d37c4-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d37c4-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d37c4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d37c4-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d37c4-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-193">Search-Flags</span></span>           | <span data-ttu-id="d37c4-194">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d37c4-194">0x00000009</span></span>                                           |
| <span data-ttu-id="d37c4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-195">System-Flags</span></span>           | <span data-ttu-id="d37c4-196">0x00000018</span><span class="sxs-lookup"><span data-stu-id="d37c4-196">0x00000018</span></span>                                           |
| <span data-ttu-id="d37c4-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d37c4-197">Classes used in</span></span>        | [<span data-ttu-id="d37c4-198">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="d37c4-198">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d37c4-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d37c4-199">Windows Server 2008</span></span>



| <span data-ttu-id="d37c4-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-200">Entry</span></span> | <span data-ttu-id="d37c4-201">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d37c4-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d37c4-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d37c4-204">System-Only</span></span>            | <span data-ttu-id="d37c4-205">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-205">True</span></span>                                                 |
| <span data-ttu-id="d37c4-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d37c4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d37c4-207">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-207">True</span></span>                                                 |
| <span data-ttu-id="d37c4-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d37c4-208">Is Indexed</span></span>             | <span data-ttu-id="d37c4-209">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-209">True</span></span>                                                 |
| <span data-ttu-id="d37c4-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d37c4-210">In Global Catalog</span></span>      | <span data-ttu-id="d37c4-211">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-211">True</span></span>                                                 |
| <span data-ttu-id="d37c4-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d37c4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d37c4-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d37c4-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d37c4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d37c4-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d37c4-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-216">Search-Flags</span></span>           | <span data-ttu-id="d37c4-217">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d37c4-217">0x00000009</span></span>                                           |
| <span data-ttu-id="d37c4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-218">System-Flags</span></span>           | <span data-ttu-id="d37c4-219">0x00000018</span><span class="sxs-lookup"><span data-stu-id="d37c4-219">0x00000018</span></span>                                           |
| <span data-ttu-id="d37c4-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d37c4-220">Classes used in</span></span>        | [<span data-ttu-id="d37c4-221">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="d37c4-221">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d37c4-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d37c4-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d37c4-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-223">Entry</span></span> | <span data-ttu-id="d37c4-224">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d37c4-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d37c4-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d37c4-227">System-Only</span></span>            | <span data-ttu-id="d37c4-228">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-228">True</span></span>                                                 |
| <span data-ttu-id="d37c4-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d37c4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d37c4-230">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-230">True</span></span>                                                 |
| <span data-ttu-id="d37c4-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d37c4-231">Is Indexed</span></span>             | <span data-ttu-id="d37c4-232">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-232">True</span></span>                                                 |
| <span data-ttu-id="d37c4-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d37c4-233">In Global Catalog</span></span>      | <span data-ttu-id="d37c4-234">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-234">True</span></span>                                                 |
| <span data-ttu-id="d37c4-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d37c4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d37c4-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d37c4-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d37c4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d37c4-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d37c4-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-239">Search-Flags</span></span>           | <span data-ttu-id="d37c4-240">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d37c4-240">0x00000009</span></span>                                           |
| <span data-ttu-id="d37c4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-241">System-Flags</span></span>           | <span data-ttu-id="d37c4-242">0x00000018</span><span class="sxs-lookup"><span data-stu-id="d37c4-242">0x00000018</span></span>                                           |
| <span data-ttu-id="d37c4-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d37c4-243">Classes used in</span></span>        | [<span data-ttu-id="d37c4-244">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="d37c4-244">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d37c4-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d37c4-245">Windows Server 2012</span></span>



| <span data-ttu-id="d37c4-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="d37c4-246">Entry</span></span> | <span data-ttu-id="d37c4-247">Значение</span><span class="sxs-lookup"><span data-stu-id="d37c4-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d37c4-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d37c4-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d37c4-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d37c4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d37c4-250">System-Only</span></span>            | <span data-ttu-id="d37c4-251">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-251">True</span></span>                                                 |
| <span data-ttu-id="d37c4-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d37c4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d37c4-253">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-253">True</span></span>                                                 |
| <span data-ttu-id="d37c4-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d37c4-254">Is Indexed</span></span>             | <span data-ttu-id="d37c4-255">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-255">True</span></span>                                                 |
| <span data-ttu-id="d37c4-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d37c4-256">In Global Catalog</span></span>      | <span data-ttu-id="d37c4-257">True</span><span class="sxs-lookup"><span data-stu-id="d37c4-257">True</span></span>                                                 |
| <span data-ttu-id="d37c4-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d37c4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d37c4-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d37c4-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d37c4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d37c4-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d37c4-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d37c4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-262">Search-Flags</span></span>           | <span data-ttu-id="d37c4-263">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d37c4-263">0x00000009</span></span>                                           |
| <span data-ttu-id="d37c4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d37c4-264">System-Flags</span></span>           | <span data-ttu-id="d37c4-265">0x00000018</span><span class="sxs-lookup"><span data-stu-id="d37c4-265">0x00000018</span></span>                                           |
| <span data-ttu-id="d37c4-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d37c4-266">Classes used in</span></span>        | [<span data-ttu-id="d37c4-267">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="d37c4-267">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





