---
title: Атрибут System-Flags
description: Целочисленное значение, содержащее флаги, определяющие дополнительные свойства класса.
ms.assetid: ce24322c-fb01-462a-aefe-cb422851f782
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута System-Flags
- Схема AD атрибута systemFlags
topic_type:
- apiref
api_name:
- System-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34bf4286cbdadc84bf340eea3f6cbec741c7920
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493917"
---
# <a name="system-flags-attribute"></a><span data-ttu-id="e9002-105">Атрибут System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-105">System-Flags attribute</span></span>

<span data-ttu-id="e9002-106">Целочисленное значение, содержащее флаги, определяющие дополнительные свойства класса.</span><span class="sxs-lookup"><span data-stu-id="e9002-106">An integer value that contains flags that define additional properties of the class.</span></span> <span data-ttu-id="e9002-107">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e9002-107">See Remarks.</span></span>



| <span data-ttu-id="e9002-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-108">Entry</span></span> | <span data-ttu-id="e9002-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="e9002-110">CN</span><span class="sxs-lookup"><span data-stu-id="e9002-110">CN</span></span>                | <span data-ttu-id="e9002-111">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-111">System-Flags</span></span>                                   |
| <span data-ttu-id="e9002-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e9002-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e9002-113">systemFlags</span><span class="sxs-lookup"><span data-stu-id="e9002-113">systemFlags</span></span>                                    |
| <span data-ttu-id="e9002-114">Размер</span><span class="sxs-lookup"><span data-stu-id="e9002-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="e9002-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e9002-115">Update Privilege</span></span>  | <span data-ttu-id="e9002-116">Это значение задается администратором схемы.</span><span class="sxs-lookup"><span data-stu-id="e9002-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="e9002-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e9002-117">Update Frequency</span></span>  | <span data-ttu-id="e9002-118">При изменении состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="e9002-118">Whenever the state of the object changes.</span></span>      |
| <span data-ttu-id="e9002-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-119">Attribute-Id</span></span>      | <span data-ttu-id="e9002-120">1.2.840.113556.1.4.375</span><span class="sxs-lookup"><span data-stu-id="e9002-120">1.2.840.113556.1.4.375</span></span>                         |
| <span data-ttu-id="e9002-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e9002-121">System-Id-Guid</span></span>    | <span data-ttu-id="e9002-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="e9002-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span></span>           |
| <span data-ttu-id="e9002-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9002-123">Syntax</span></span>            | [<span data-ttu-id="e9002-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="e9002-124">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="e9002-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e9002-125">Implementations</span></span>

-   [<span data-ttu-id="e9002-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9002-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9002-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9002-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9002-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e9002-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e9002-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9002-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9002-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9002-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9002-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9002-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9002-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9002-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9002-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9002-133">Windows 2000 Server</span></span>



| <span data-ttu-id="e9002-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-134">Entry</span></span> | <span data-ttu-id="e9002-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-138">System-Only</span></span>            | <span data-ttu-id="e9002-139">True</span><span class="sxs-lookup"><span data-stu-id="e9002-139">True</span></span>                            |
| <span data-ttu-id="e9002-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-141">True</span><span class="sxs-lookup"><span data-stu-id="e9002-141">True</span></span>                            |
| <span data-ttu-id="e9002-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-142">Is Indexed</span></span>             | <span data-ttu-id="e9002-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-143">False</span></span>                           |
| <span data-ttu-id="e9002-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-144">In Global Catalog</span></span>      | <span data-ttu-id="e9002-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-145">False</span></span>                           |
| <span data-ttu-id="e9002-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-150">Search-Flags</span></span>           | <span data-ttu-id="e9002-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-151">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-152">System-Flags</span></span>           | <span data-ttu-id="e9002-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-153">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-154">Classes used in</span></span>        | [<span data-ttu-id="e9002-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9002-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9002-156">Windows Server 2003</span></span>



| <span data-ttu-id="e9002-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-157">Entry</span></span> | <span data-ttu-id="e9002-158">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-161">System-Only</span></span>            | <span data-ttu-id="e9002-162">True</span><span class="sxs-lookup"><span data-stu-id="e9002-162">True</span></span>                            |
| <span data-ttu-id="e9002-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-164">True</span><span class="sxs-lookup"><span data-stu-id="e9002-164">True</span></span>                            |
| <span data-ttu-id="e9002-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-165">Is Indexed</span></span>             | <span data-ttu-id="e9002-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-166">False</span></span>                           |
| <span data-ttu-id="e9002-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-167">In Global Catalog</span></span>      | <span data-ttu-id="e9002-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-168">False</span></span>                           |
| <span data-ttu-id="e9002-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-173">Search-Flags</span></span>           | <span data-ttu-id="e9002-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-174">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-175">System-Flags</span></span>           | <span data-ttu-id="e9002-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-176">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-177">Classes used in</span></span>        | [<span data-ttu-id="e9002-178">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e9002-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="e9002-179">ADAM</span></span>



| <span data-ttu-id="e9002-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-180">Entry</span></span> | <span data-ttu-id="e9002-181">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-184">System-Only</span></span>            | <span data-ttu-id="e9002-185">True</span><span class="sxs-lookup"><span data-stu-id="e9002-185">True</span></span>                            |
| <span data-ttu-id="e9002-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-187">True</span><span class="sxs-lookup"><span data-stu-id="e9002-187">True</span></span>                            |
| <span data-ttu-id="e9002-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-188">Is Indexed</span></span>             | <span data-ttu-id="e9002-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-189">False</span></span>                           |
| <span data-ttu-id="e9002-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-190">In Global Catalog</span></span>      | <span data-ttu-id="e9002-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-191">False</span></span>                           |
| <span data-ttu-id="e9002-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-196">Search-Flags</span></span>           | <span data-ttu-id="e9002-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-197">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-198">System-Flags</span></span>           | <span data-ttu-id="e9002-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-199">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-200">Classes used in</span></span>        | [<span data-ttu-id="e9002-201">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9002-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9002-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9002-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-203">Entry</span></span> | <span data-ttu-id="e9002-204">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-207">System-Only</span></span>            | <span data-ttu-id="e9002-208">True</span><span class="sxs-lookup"><span data-stu-id="e9002-208">True</span></span>                            |
| <span data-ttu-id="e9002-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-210">True</span><span class="sxs-lookup"><span data-stu-id="e9002-210">True</span></span>                            |
| <span data-ttu-id="e9002-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-211">Is Indexed</span></span>             | <span data-ttu-id="e9002-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-212">False</span></span>                           |
| <span data-ttu-id="e9002-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-213">In Global Catalog</span></span>      | <span data-ttu-id="e9002-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-214">False</span></span>                           |
| <span data-ttu-id="e9002-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-219">Search-Flags</span></span>           | <span data-ttu-id="e9002-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-220">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-221">System-Flags</span></span>           | <span data-ttu-id="e9002-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-222">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-223">Classes used in</span></span>        | [<span data-ttu-id="e9002-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9002-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9002-225">Windows Server 2008</span></span>



| <span data-ttu-id="e9002-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-226">Entry</span></span> | <span data-ttu-id="e9002-227">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-230">System-Only</span></span>            | <span data-ttu-id="e9002-231">True</span><span class="sxs-lookup"><span data-stu-id="e9002-231">True</span></span>                            |
| <span data-ttu-id="e9002-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-233">True</span><span class="sxs-lookup"><span data-stu-id="e9002-233">True</span></span>                            |
| <span data-ttu-id="e9002-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-234">Is Indexed</span></span>             | <span data-ttu-id="e9002-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-235">False</span></span>                           |
| <span data-ttu-id="e9002-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-236">In Global Catalog</span></span>      | <span data-ttu-id="e9002-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-237">False</span></span>                           |
| <span data-ttu-id="e9002-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-242">Search-Flags</span></span>           | <span data-ttu-id="e9002-243">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-243">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-244">System-Flags</span></span>           | <span data-ttu-id="e9002-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-245">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-246">Classes used in</span></span>        | [<span data-ttu-id="e9002-247">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9002-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9002-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9002-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-249">Entry</span></span> | <span data-ttu-id="e9002-250">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-253">System-Only</span></span>            | <span data-ttu-id="e9002-254">True</span><span class="sxs-lookup"><span data-stu-id="e9002-254">True</span></span>                            |
| <span data-ttu-id="e9002-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-255">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-256">True</span><span class="sxs-lookup"><span data-stu-id="e9002-256">True</span></span>                            |
| <span data-ttu-id="e9002-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-257">Is Indexed</span></span>             | <span data-ttu-id="e9002-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-258">False</span></span>                           |
| <span data-ttu-id="e9002-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-259">In Global Catalog</span></span>      | <span data-ttu-id="e9002-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-260">False</span></span>                           |
| <span data-ttu-id="e9002-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-265">Search-Flags</span></span>           | <span data-ttu-id="e9002-266">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-266">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-267">System-Flags</span></span>           | <span data-ttu-id="e9002-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-268">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-269">Classes used in</span></span>        | [<span data-ttu-id="e9002-270">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9002-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9002-271">Windows Server 2012</span></span>



| <span data-ttu-id="e9002-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9002-272">Entry</span></span> | <span data-ttu-id="e9002-273">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9002-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9002-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9002-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e9002-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9002-276">System-Only</span></span>            | <span data-ttu-id="e9002-277">True</span><span class="sxs-lookup"><span data-stu-id="e9002-277">True</span></span>                            |
| <span data-ttu-id="e9002-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9002-278">Is-Single-Valued</span></span>       | <span data-ttu-id="e9002-279">True</span><span class="sxs-lookup"><span data-stu-id="e9002-279">True</span></span>                            |
| <span data-ttu-id="e9002-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9002-280">Is Indexed</span></span>             | <span data-ttu-id="e9002-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-281">False</span></span>                           |
| <span data-ttu-id="e9002-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9002-282">In Global Catalog</span></span>      | <span data-ttu-id="e9002-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9002-283">False</span></span>                           |
| <span data-ttu-id="e9002-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9002-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9002-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9002-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9002-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9002-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9002-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9002-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9002-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-288">Search-Flags</span></span>           | <span data-ttu-id="e9002-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9002-289">0x00000008</span></span>                      |
| <span data-ttu-id="e9002-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9002-290">System-Flags</span></span>           | <span data-ttu-id="e9002-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9002-291">0x00000010</span></span>                      |
| <span data-ttu-id="e9002-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9002-292">Classes used in</span></span>        | [<span data-ttu-id="e9002-293">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="e9002-293">**Top**</span></span>](c-top.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e9002-294">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9002-294">Remarks</span></span>

<span data-ttu-id="e9002-295">Этот атрибут может быть нулевым или сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9002-295">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="e9002-296">Значение</span><span class="sxs-lookup"><span data-stu-id="e9002-296">Value</span></span>                   | <span data-ttu-id="e9002-297">Описание</span><span class="sxs-lookup"><span data-stu-id="e9002-297">Description</span></span>                                                                                                                                                                                                                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9002-298">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e9002-298">1 (0x00000001)</span></span>          | <span data-ttu-id="e9002-299">При применении к атрибуту репликация атрибута не выполняется. При применении к объекту [**перекрестной ссылки**](c-crossref.md) контекст именования находится в NTDS.</span><span class="sxs-lookup"><span data-stu-id="e9002-299">When applied to an attribute, the attribute will not be replicated.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is in NTDS.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e9002-300">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e9002-300">2 (0x00000002)</span></span>          | <span data-ttu-id="e9002-301">При применении к атрибуту этот атрибут будет реплицирован в глобальный каталог. При применении к объекту [**перекрестной ссылки**](c-crossref.md) контекстом именования является домен.</span><span class="sxs-lookup"><span data-stu-id="e9002-301">When applied to an attribute, the attribute will be replicated to the global catalog.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is a domain.</span></span><br/>                                                                                                       |
| <span data-ttu-id="e9002-302">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e9002-302">4 (0x00000004)</span></span>          | <span data-ttu-id="e9002-303">При применении к атрибуту создается атрибут.</span><span class="sxs-lookup"><span data-stu-id="e9002-303">When applied to an attribute, the attribute is constructed.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="e9002-304">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e9002-304">16 (0x00000010)</span></span>         | <span data-ttu-id="e9002-305">Если этот параметр задан, то объект является объектом Category 1.</span><span class="sxs-lookup"><span data-stu-id="e9002-305">When set, indicates the object is a category 1 object.</span></span> <span data-ttu-id="e9002-306">Объект Category 1 — это класс или атрибут, включенный в базовую схему, включенную в систему.</span><span class="sxs-lookup"><span data-stu-id="e9002-306">A category 1 object is a class or attribute that is included in the base schema included with the system.</span></span>                                                                                                                                |
| <span data-ttu-id="e9002-307">33554432 (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-307">33554432 (0x02000000)</span></span>   | <span data-ttu-id="e9002-308">Объект не перемещается в контейнер удаленных объектов при удалении.</span><span class="sxs-lookup"><span data-stu-id="e9002-308">The object is not moved to the Deleted Objects container when it is deleted.</span></span> <span data-ttu-id="e9002-309">Он будет удален немедленно.</span><span class="sxs-lookup"><span data-stu-id="e9002-309">It will be deleted immediately.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="e9002-310">67108864 (0x04000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-310">67108864 (0x04000000)</span></span>   | <span data-ttu-id="e9002-311">Объект не может быть перемещен.</span><span class="sxs-lookup"><span data-stu-id="e9002-311">The object cannot be moved.</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e9002-312">134217728 (0x08000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-312">134217728 (0x08000000)</span></span>  | <span data-ttu-id="e9002-313">Объект не может быть переименован.</span><span class="sxs-lookup"><span data-stu-id="e9002-313">The object cannot be renamed.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e9002-314">268435456 (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-314">268435456 (0x10000000)</span></span>  | <span data-ttu-id="e9002-315">Для объектов в разделе конфигурации, если этот флаг установлен, объект можно перемещать с ограничениями. в противном случае объект не может быть перемещен.</span><span class="sxs-lookup"><span data-stu-id="e9002-315">For objects in the configuration partition, if this flag is set, the object can be moved with restrictions; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="e9002-316">По умолчанию этот флаг не установлен для новых объектов, созданных в разделе конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e9002-316">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="e9002-317">Этот флаг можно задать только во время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="e9002-317">This flag can only be set during object creation.</span></span> |
| <span data-ttu-id="e9002-318">536870912 (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-318">536870912 (0x20000000)</span></span>  | <span data-ttu-id="e9002-319">Для объектов в разделе конфигурации, если этот флаг установлен, объект можно переместить. в противном случае объект не может быть перемещен.</span><span class="sxs-lookup"><span data-stu-id="e9002-319">For objects in the configuration partition, if this flag is set, the object can be moved; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="e9002-320">По умолчанию этот флаг не установлен для новых объектов, созданных в разделе конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e9002-320">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="e9002-321">Этот флаг можно задать только во время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="e9002-321">This flag can only be set during object creation.</span></span>                   |
| <span data-ttu-id="e9002-322">1073741824 (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-322">1073741824 (0x40000000)</span></span> | <span data-ttu-id="e9002-323">Для объектов в разделе конфигурации, если этот флаг установлен, объект можно переименовать; в противном случае объект не может быть переименован.</span><span class="sxs-lookup"><span data-stu-id="e9002-323">For objects in the configuration partition, if this flag is set, the object can be renamed; otherwise, the object cannot be renamed.</span></span> <span data-ttu-id="e9002-324">По умолчанию этот флаг не установлен для новых объектов, созданных в разделе конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e9002-324">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="e9002-325">Этот флаг можно задать только во время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="e9002-325">This flag can only be set during object creation.</span></span>               |
| <span data-ttu-id="e9002-326">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="e9002-326">2147483648 (0x80000000)</span></span> | <span data-ttu-id="e9002-327">Не удается удалить объект.</span><span class="sxs-lookup"><span data-stu-id="e9002-327">The object cannot be deleted.</span></span>                                                                                                                                                                                                                                                                   |



 

 

 





